# minproxy

Minimal HTTP proxy server for logging traffic.

## Setup

```bash
pip install -r requirements.txt
```

## Usage

Start the proxy:
```bash
python proxy.py --output traffic.log
```

Make requests through the proxy:
```bash
curl -x http://127.0.0.1:8080 http://example.com
```

View the logs:
```bash
cat /tmp/traffic.log
```

## Output Format

Each request is logged as a single JSON line:
```json
{"method": "GET", "path": "http://example.com/", "response": 200, "content_type": "text/html"}
```