# GoScreenAPI Examples

Simple examples for capturing website screenshots with GoScreenAPI.

## Why GoScreenAPI?
- Fast screenshot API
- Sync and batch support
- Affordable pricing: 10,000 screenshots for $10

## Get started
1. Create an account at https://goscreenapi.com/
2. Get your API key
3. Run the example below

## cURL Example

```bash
curl -X POST https://goscreenapi.com/api/v1/screenshot \
  -H "Authorization: Bearer YOUR_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "url": "https://example.com",
    "format": "png",
    "full_page": true
  }'

## Node.js Example

```js
async function run() {
  const response = await fetch("https://goscreenapi.com/api/v1/screenshot", {
    method: "POST",
    headers: {
      "Authorization": "Bearer YOUR_API_KEY",
      "Content-Type": "application/json"
    },
    body: JSON.stringify({
      url: "https://example.com",
      format: "png",
      full_page: true
    })
  });

  const data = await response.json();
  console.log(data);
}

run();

