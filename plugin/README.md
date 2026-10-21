# FeatPaper

Make documents and reports as desktop and mobile PDFs and register them on FeatPaper. Creating documents and downloading files works without login; registering uploads requires login.

Environment: production. The plugin connects to the FeatPaper MCP server at https://mcp.featpaper.com/mcp and contains one skill (featpaper) and one preview script, references/mobile-summary-kit.html. The assistant pastes that script into a mobile summary page it writes; it runs only inside that page and sends ready, section, activity and call-to-action messages to the frame that embeds the page (the FeatPaper viewer). Creating documents and downloading files works without login. Registering a document uploads your PDFs to FeatPaper and requires login. Installing this package does not deploy any server.
