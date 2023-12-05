# Example curl commands for testing your server

Replace the IP address in the examples with the IP address of your **load balancer, not your servers!**

Run these commands from your host machine, not your server.

## Testing your frontend

```bash
curl http://146.190.12.184
```

## Testing your backend

```bash
curl http://146.190.12.184/hey
```

```bash
curl -X POST -H "Content-Type: application/json" \
  -d '{"message": "Hello from your server"}' \
  http://146.190.12.184/echo
```
