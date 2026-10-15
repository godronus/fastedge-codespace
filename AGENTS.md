# FastEdge codespace

## Signing in to Gcore

When the FastEdge MCP server needs a remote sign-in and gives you a
`login --code --seal-to <key>` command, don't ask the user to copy that command
(copying from an agent's output is hard in a browser codespace). Instead:

1. Run `fastedge-login --save <key>` yourself. It only saves the key.
2. Tell the user to open a new terminal (the + in the terminal panel), run
   `fastedge-login`, and follow its steps: open the portal link, choose the manual
   option, approve, then paste the connect code at the prompt.
3. Wait for the user to say it succeeded, then retry the request.

Never ask for the connect code in the chat, and never open the portal link yourself.
