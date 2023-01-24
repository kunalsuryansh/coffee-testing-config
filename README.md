# coffee-testing-config

const accessToken = 'YOUR_ACCESS_TOKEN';
const bitbucketUrl = 'https://api.bitbucket.org/2.0';

const getRepositories = async () => {
  try {
    const response = await fetch(`${bitbucketUrl}/repositories/`, {
      headers: {
        Authorization: `Bearer ${accessToken}`,
      },
    });
    const json = await response.json();
    return json;
  } catch (error) {
    console.error(error);
  }
};
