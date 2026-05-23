import axios from "axios";

export default async function handler(req, res) {
  const { name, page } = req.query;

  const options = {
    method: "GET",
    url: "https://skip-tracing-working-api.p.rapidapi.com/search/byname",
    params: { name, page },
    headers: {
      "x-rapidapi-key": process.env.RAPIDAPI_KEY,
      "x-rapidapi-host": "skip-tracing-working-api.p.rapidapi.com",
      "Content-Type": "application/json"
    }
  };

  try {
    const response = await axios.request(options);
    res.status(200).json(response.data);
  } catch (error) {
    res.status(500).json({ error: error.message });
  }
}
