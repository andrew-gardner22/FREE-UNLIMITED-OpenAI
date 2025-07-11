# FREE UNLIMITED OpenAI
A tutorial of how to get free unlimited OpenAI API
---  
[Tutorial Website](andrew-garner22.github.io/FREE-UNLIMITED-OpenAI)
---
This tutorial will show you how to use Puter.js to access OpenAI API capabilities for free, without needing an OpenAI API key. Puter.js is completely free and open-source, allowing you to provide your users with powerful AI capabilities without any API keys or usage restrictions. Using Puter.js, you can access GPT-4o, GPT-4.1, GPT-4.5, o1, o3, o4, DALL-E, ... directly from your frontend code without any server-side setup.\
\
**Getting Started**\
You can use puter.js without any API keys or sign-ups. To start using Puter.js, include the following script tag in your HTML file, either in the <head> or <body> section:
```
<script src="https://js.puter.com/v2/"></script>
```
\
Nothing else is required to start using Puter.js for free access to OpenAI API models and capabilities.\
\
**Example 1**\
Use GPT-4o for text generation\
To generate text using GPT-4o, use the **puter.ai.chat()** function:
```
puter.ai.chat("What are the benefits of exercise?")
    .then(response => {
        puter.print(response);
    });
```
Full code example:
```
<html>
<body>
    <script src="https://js.puter.com/v2/"></script>
    <script>
        puter.ai.chat("What are the benefits of exercise?")
            .then(response => {
                puter.print(response);
            });
    </script>
</body>
</html>
```
**Example 2**\
Generate images with DALL-E 3\
To create images using DALL-E 3, use the **puter.ai.txt2img()** function:
```
puter.ai.txt2img("A futuristic cityscape at night")
    .then(imageElement => {
        document.body.appendChild(imageElement);
    });
```
Full code example:

```
<html>
<body>
    <script src="https://js.puter.com/v2/"></script>
    <script>
        puter.ai.txt2img("A futuristic cityscape at night")
            .then(imageElement => {
                document.body.appendChild(imageElement);
            });
    </script>
</body>
</html>
```

**Example 3**\
Analyze images with GPT-4o Vision
To analyze images using GPT-4o Vision, provide an image URL to **puter.ai.chat()**:
```
puter.ai.chat(
    "What do you see in this image?", 
    "https://assets.puter.site/doge.jpeg"
)
.then(response => {
    puter.print(response);
});
```
Full code example:
```
<html>
<body>
    <script src="https://js.puter.com/v2/"></script>
    <script>
        puter.ai.chat(
            "What do you see in this image?", 
            "https://assets.puter.site/doge.jpeg"
        )
        .then(response => {
            puter.print(response);
        });
    </script>
</body>
</html>
```
**Example 4**\
Use different OpenAI models\
You can specify different OpenAI models using the model parameter, for example gpt-4.1, o3-mini, o1-mini, or gpt-4o:

```
// Using gpt-4.1 model
puter.ai.chat(
    "Write a short poem about coding",
    { model: "gpt-4.1" }
).then(response => {
    puter.print(response);
});

// Using o3-mini model
puter.ai.chat(
    "Write a short poem about coding",
    { model: "o3-mini" }
).then(response => {
    puter.print(response);
});

// Using o1-mini model
puter.ai.chat(
    "Write a short poem about coding",
    { model: "o1-mini" }
).then(response => {
    puter.print(response);
});

// Using 4o model
puter.ai.chat(
    "Write a short poem about coding",
    { model: "gpt-4o" }
).then(response => {
    puter.print(response);
});
```
Full code example:
```
<html>
<body>
    <script src="https://js.puter.com/v2/"></script>
    <script>
        // Using gpt-4.1 model
        puter.ai.chat(
            "Write a short poem about coding",
            { model: "gpt-4.1" }
        ).then(response => {
            puter.print("<h2>Using gpt-4.1 model</h2>");
            puter.print(response);
        });

        // Using o3-mini model
        puter.ai.chat(
            "Write a short poem about coding",
            { model: "o3-mini" }
        ).then(response => {
            puter.print("<h2>Using o3-mini model</h2>");
            puter.print(response);
        });

        // Using o1-mini model
        puter.ai.chat(
            "Write a short poem about coding",
            { model: "o1-mini" }
        ).then(response => {
            puter.print("<h2>Using o1-mini model</h2>");
            puter.print(response);
        });

        // Using 4o model
        puter.ai.chat(
            "Write a short poem about coding",
            { model: "gpt-4o" }
        ).then(response => {
            puter.print("<h2>Using gpt-4o model</h2>");
            puter.print(response);
        });
    </script>
</body>
</html>
```
**Example 5**\
Stream responses for longer queries
For longer responses, use streaming to get results in real-time:
```
async function streamResponse() {
    const response = await puter.ai.chat(
        "Explain the theory of relativity in detail", 
        {stream: true}
    );
    
    for await (const part of response) {
        puter.print(part?.text);
    }
}

streamResponse();
```
Full code example:
```
<html>
<body>
    <script src="https://js.puter.com/v2/"></script>
    <script>
        async function streamResponse() {
            const response = await puter.ai.chat(
                "Explain the theory of relativity in detail", 
                {stream: true}
            );
            
            for await (const part of response) {
                puter.print(part?.text);
            }
        }

        streamResponse();
    </script>
</body>
</html>
```
List of supported models
The following OpenAI models are supported by Puter.js:
```
gpt-4.1
gpt-4.1-mini
gpt-4.1-nano
gpt-4.5-preview
gpt-4o
gpt-4o-mini
o1
o1-mini
o1-pro
o3
o3-mini
o4-mini
```

**_That's it!_** You now have a free alternative to the OpenAI API using Puter.js. This allows you to access GPT-4o, o4, o3-mini, o1-mini, DALL-E, ... capabilities without needing an API key or a backend. True serverless AI!  

**_If you found this helpful or want to use it in your project please star this repo! Happy Coding!_**
