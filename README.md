---

🚀 Build an Agentic AI Video & YouTube Summarizer with Streamlit and Gemini
By Akram Mohammad

---

🌌 Introduction: Why This Matters
We live in an era of endless recorded lectures, webinars, YouTube talks, and project videos.
 But time is limited - we can't watch everything.
 As a PhD student and AI developer, I constantly face this pain point: How do I extract the important parts of hours-long videos, without wasting time?
This question inspired me to build Agentic AI Video & YouTube Summarizer, an AI-powered web app that automatically:
🌿 Accepts any video file or YouTube link
 🌿 Uses Gemini's multimodal capabilities to analyze the video
 🌿 Generates clear, actionable summaries - instantly
 🌿 Runs fully in your browser - no installation needed, no local processing
In this article, I'll break down:
 🔹 Why you should care
 🔹 How the tool works (step-by-step, no fluff)
 🔹 What frameworks and tools make this possible
 🔹 How you can deploy your own version for free
 🔹 How to grow it into a product or monetizable asset later

---

🎬 Why You Should Read This
This guide is for students, researchers, developers, or creators who want to:
🔹 Save hours summarizing lectures or meetings
 🔹 Build a real AI-powered tool you can showcase in your portfolio
 🔹 Learn how to deploy AI apps without backend headaches
 🔹 Start small - then scale your idea into a paid SaaS, mobile app, or niche tool

---

🌐 What This Tool Does
🌿 Upload any .mp4, .mov, or .avi file
 🌿 Or paste any YouTube link
 🌿 The AI downloads (if YouTube), processes, and summarizes the content
 🌿 You ask specific questions ("Give me key points," "Summarize for non-tech audience") - the AI tailors the summary
 🌿 Outputs appear instantly in your browser - ready for notes or reports

---

🧩 How It Works ?
Let's break down the whole flow:
🔹 1️⃣ Input: User uploads a file or pastes a YouTube link.
 🔹 2️⃣ Download: If it's YouTube, the app uses yt_dlp to download and merge video/audio.
 🔹 3️⃣ Processing: Google Gemini handles the core analysis with its multimodal capability.
 🔹 4️⃣ Agentic Orchestration: The Phi Agent coordinates what to do - fetching the user's question, adding context if needed (via DuckDuckGo).
 🔹 5️⃣ Summarization: Gemini generates a custom summary matching your query.
 🔹 6️⃣ Delivery: Streamlit displays the result cleanly, with zero friction.

---

🧩 Key Frameworks & Tools: 
Below is a practical breakdown - what each tool is, why I chose it, and how it fits in.

---

🛠️ 1️⃣ Streamlit
📌 What is it?
 An open-source Python library that turns Python scripts into shareable web apps - no web dev needed.
📌 Why is it great?
 🔹 Interactive widgets: buttons, file uploaders, text boxes
 🔹 Instant feedback in the browser - changes appear live
 🔹 Supports cloud deployment for free with Streamlit Community Cloud
📌 How I use it:
 The entire user interface: upload section, YouTube input, progress spinners, and final summary display - all powered by Streamlit.

---

🛠️ 2️⃣ Google Gemini API
📌 What is it?
 A powerful multimodal AI model that can process text, images, and video content - and generate high-quality text outputs.
📌 Why is it great?
 🔹 Handles complex reasoning
 🔹 Works with large context inputs (e.g., transcribed video content)
 🔹 Supports advanced, custom instructions
📌 How I use it:
 Gemini is the core engine that digests the video and your question - then writes a human-friendly, actionable summary.

---

🛠️ 3️⃣ Phi Agent Framework
📌 What is it?
 A lightweight Python framework for building AI agents that can do multi-step reasoning, call tools, and produce structured output.
📌 Why is it great?
 🔹 Lets you chain tools - not just call an LLM once
 🔹 Makes it easy to plug in external tools like web search
 🔹 Produces better, more grounded answers
📌 How I use it:
 The Phi Agent calls Gemini and DuckDuckGo search if needed, merging external context with the video insights.

---

🛠️ 4️⃣ yt_dlp
📌 What is it?
 A modern, faster fork of youtube-dl - the best way to programmatically download YouTube videos and extract audio/video streams.
📌 Why is it great?
 🔹 Handles different YouTube formats
 🔹 Merges video and audio using ffmpeg behind the scenes
 🔹 Lets the app accept YouTube links instead of only file uploads
📌 How I use it:
 When you paste a YouTube link, yt_dlp downloads it, converts it to a local file, and hands it off to Gemini for processing.

---

🛠️ 5️⃣ DuckDuckGo Search
📌 What is it?
 A simple search tool that lets your agent fetch real-time context to supplement Gemini's output.
📌 Why is it great?
 🔹 Helps fill gaps - e.g., if the video mentions references, the agent can look them up
 🔹 Adds freshness to static summaries
 🔹 Fully integrated with Phi for agentic control
📌 How I use it:
 The agent can call DuckDuckGo in the background to enrich the summary if needed - all behind the scenes.

---

🛠️ 6️⃣ Streamlit Community Cloud
📌 What is it?
 A free hosting platform by Streamlit that deploys your Python app with one click - giving you a public URL.
📌 Why is it great?
 🔹 No servers or DevOps knowledge needed
 🔹 Auto-builds from your GitHub repo
 🔹 Handles scaling for small prototypes and demos
📌 How I use it:
 I deploy my summarizer here so anyone with the link can try it - on any device, anywhere.

---

✨ How To Use This Beyond Today
Here's how you can take this idea further:
🌿 Add speech-to-text for raw video processing - so even silent lectures without subtitles can be summarized.
🌿 Build a mobile app wrapper - using Flutter or React Native to turn your Streamlit or FastAPI backend into an iOS/Android app.
🌿 Offer premium tiers - e.g., free short summaries, paid detailed reports or meeting minutes.
🌿 Integrate PDF or slide summarization - so the same agent can summarize documents too.
🌿 Monetize - Package it as a freemium SaaS: add Stripe, set user quotas, charge for heavy usage.
🌿 Expand your agent - Add custom tools like Google Scholar search for academic context, or ArXiv integration for auto citations.

---

🌌 Final Thoughts
📌 Why did I write this?
 Because the world does not need more information overload - it needs tools that convert raw info into insights instantly.
 This summarizer is one small step in that direction.
📌 Why should you care?
 Because AI is powerful only when deployed practically - and this project shows how anyone can build & ship a real AI tool, today.

---

🌿 Try It Yourself
You can deploy your own version:
1️⃣ Upload your app.py + requirements.txt to GitHub
 2️⃣ Connect it to Streamlit Community Cloud
 3️⃣ Click Deploy - get your public URL in seconds
 4️⃣ Share it with your friends, team, or lab

---

🎯 Ready to Save Hours?
If you found this helpful:
 🔹 Bookmark this guide
 🔹 Follow me on Medium for more practical AI workflows
 🔹 Connect on LinkedIn - I love meeting builders working on AI for real productivity
💡 Ready to Dive In?
🌿 Here is the GitHub link with all the code files for this project:
🔗 GitHub Repository
🌿 Connect with me on LinkedIn to share your builds or discuss collaboration:
🔗 LinkedIn Profile
🌿 Contact me directly if you have any questions or need guidance:
📧 akramuk66@gmail.com

#ArtificialIntelligence #MachineLearning #Streamlit #Gemini #Python #Productivity #SaaS #AIAgents #GenAI #AgenticAI

---

Let's use AI to work smarter, learn faster, and build better tools - together. 🚀

---

Akram Mohammad
