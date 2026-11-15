# AI Integration Builder · Prototype

A clickable prototype of a **human-in-the-loop guarded agentic solution** that turns an app's API documentation into tested integration code. It was built for a product assignment, with Calendly as the example app.

**Live demo:** https://nayeemaslam05.github.io/API-Integration/

## What it shows

The flow follows nine steps, and every step in the top bar is clickable:

1. Choose to build with AI or manually
2. Point the agent at the API docs (HTML, PDF or Swagger/OpenAPI)
3. Watch the agent read the docs, with a source cited for every finding
4. Choose read-only endpoints (write actions stay locked)
5. Review the schema and the generated integration code, and refine it in plain English
6. Connect a test account (the token goes to a vault, and the AI only sees masked data)
7. Run eight tests. The first run fails on pagination completeness, the agent proposes a fix, and a person confirms the user count
8. A second person approves the integration for production
9. Go live in shadow mode, with monitoring, versions, an audit log and support cases

A safety panel on every screen tracks the eight gates every integration passes.

All account data is simulated. No real API calls are made.

## Run locally

It is a single static page with no build step. Open `index.html` in a browser, or serve the folder:

```bash
python3 -m http.server 8000
```

## Credits

Built with [Vue 3](https://vuejs.org) (MIT), loaded from the jsDelivr CDN.
