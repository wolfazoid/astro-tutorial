# The 1 Hour Website

It’s better to get a prototype in place immediately when the stakes are low and the interest is speed to market. This is a very fast way to get a single page website built and deployed with a shareable link. The time will vary depending on the references you have available, your familiarity with the platforms, and of course how “optimal” you want the site to look before sharing it with clients or working project partners. If you’re ok with a scrappy first draft and have good reference materials, this can easily be done in under an hour.

## Ingredients

1. Claude Code
2. ChatGPT
3. Visual Studio
4. Vercel
5. Git
6. Brand brief (prepared separately)
7. Color palette (prepared separately)
8. Any other reference materials (screenshots of competitor sites, design files, whatever you want to feed into the agent’s context)

## Recipe

1. Open a new project folder in Visual Studio Code.
2. Set up a private git repo (easiest in the github.com UI) with a Readme.md. Follow the directions to pull this into your project folder
3. Set up a new Vercel project and connect your repo
4. Put your Brand Brief (in Markdown, PDF, or text format) and any brand, asset, and color references in a folder within your project (name the folder something simple like “References”, doesn’t really matter). Add this to your .gitignore file so you don’t upload these documents to Github (unless you want to).
5. Initialize Claude Code from your project folder in VS Code terminal. Prompt it to build you a single page website to be hosted in Vercel. Give it the business context, primary goals of the website (e.g., “newsletter sign up”, or “booking client discovery calls”), and any relevant context for what you need for output. Ensure you’re in “plan” mode so you can validate what the agent’s about to do before it gets started coding. Here’s a sample prompt:
   \> I’m building a simple single page website. The website is for a website strategy and development agency. The primary goal is to get visitors to book a discovery call with me. Our ideal client are small-to-medium sized businesses that are selling D2C products in an e-commerce business model. The site should include sections that capture our unique value proposition (features designed, tested, and launched fast at a fraction of the usual agency cost), who we are, our selection of services, how to work with us, and social proof and testimonial sections. We’ll also have a couple of case studies hosted that customers can download and review from the single page. I have a full set of references to help you understand our business and brand in the “References” folder in this project, review those in full before you start. Make sure the website is fully responsive, as many clients will be visiting the website from mobile phones or tablets when I meet them on the road or at networking events.
6. Once Claude has worked through the prompt, references, and provided a plan, if you like the plan, let it get to work. If you don’t like the plan, continue to refine the project until it’s in a place that you like.
7. After the initial build, you can push the changes to GitHub. With Vercel properly configured, you’ll have a new deployment link in your Vercel dashboard which you can copy and paste into a web browser to view the site. You can also send it to yourself to view the mobile (and tablet if you have one) layouts in a real context. This tends to be better than simply going to console view and resizing the screen on your computer.

   _Alternatively, you can spin up a local server with Python or your server of choice (or have Claude do it for you) and visit the site on your local machine at localhost:8000 (or whatever port you launch to). This is a little more advanced, but saves you the extra step of deploying before you know you have something you like. Really up to you, I tend to stay in local until I'm close to something good, then deploy and test on various devices. But always be committing (ABC!), as it helps to revert bad changes more easily when you get into refinement stage._

8. Continue to iterate and refine with Claude or on your own depending on how comfortable you are with HTML and CSS. I often find I do a bit of manual refinement since communicating about the UI is hard and AI agents still struggle with pure CSS-related prompting. (It’s really hard to test CSS as a machine).
9. Once you have the layout where you like it, ask Claude to print the text content in your HTML to Markdown in a sub-folder. Take that markdown file (or files, if you went for a multi-page website), to ChatGPT and do some prompting to refine your initial prototype copy with the tone and language you like. (Personal preference here, I find ChatGPT better for this kind of work. You could do it in any agent. Just don’t do it in Claude Code, it’s not as good at “creative copy” tasks like this.) Download the final markdown how you like it, put it back into your markdown sub-folder, and have Claude Code replace the copy in your site files with the copy from your new markdown file.
10. Deploy everything to GitHub, grab your new vercel link, and congratulations you have yourself a prototype website. Get the feedback you need from the people you trust, refine, iterate, and then you can buy a domain and deploy directly from Vercel or rebuild in the web builder of your choice based on your prototype (might feel silly, but can be valuable if it’s for a client that will manage the content themselves.)

Remember, the value here is getting from idea to functional prototype _fast_. There’s still plenty of time to be spent getting the right content and experience built. But you should be able to get much more effective feedback with a working prototype, and get to the final result in half the time.
