# AI-Facebook-Automation-Workflow #
In n8n, we start with a manual trigger. Then, we define our content parameters in a Set node — things like the topic, brand tone, target audience, platform, emoji usage, and language.
Next, we use the Gemini AI node to generate platform-specific content in a structured JSON format. This AI output is then cleaned and parsed using a Function node, ensuring we get the exact caption we want. Finally, we store it in another Set node as fb_caption.
With the caption ready, we send it to Facebook using an HTTP Request node. The request points to the Facebook Graph API endpoint for our page, and the message parameter contains the caption we just generated.
Once executed, the post appears live on your Facebook page automatically — no manual copy-pasting, no missed posting times.
