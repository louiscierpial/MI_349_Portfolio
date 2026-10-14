All prompts and results from AI usage for this projecy:
Prompt: "I am running into an issue with modulating text size based on different dimensions of screens. I'm looking to have a mobile-first approach utilizing @media queries for modulating text size and other proportions for different screen dimensions, using the min-width property within media queries. Can you help me develop some code that modulates <p> text size based on screen dimensions? Please only modify CSS code and do not touch any HTML."
Result: "Updated style.css with mobile-first sizing: paragraph text starts at 1rem, increases to 1.2rem from 600px, and reaches 1.4rem from 1000px. I also made the body and main container responsive and adjusted navigation and contact spacing for smaller screens.

No HTML was changed. git diff --check passed; no CSS-specific test or lint command was configured."
AI-generated code: 
*{
    box-sizing: border-box;
}

p{
    line-height: 1.6;
    margin-bottom: 1rem;
    font-size: 1rem;
}
(changed font size to 1rem)

header{
    text-align: center;
    width: 100%;
}

@media (min-width: 600px){
    p{
        font-size: 1.2rem;
    }

    nav{
        padding: 1rem 1.5rem;
    }

    nav ul{
        gap: 2rem;
    }

    nav a{
        font-size: 1.5rem;
    }

@media (min-width: 1000px){
    body{
        padding: 75px;
    }

    main{
        padding: 50px;
    }

    p{
        font-size: 1.4rem;
    }

    nav{
        padding: 1rem 1.9rem;
    }

    nav ul{
        gap: 3.75rem;
    }

    nav a{
        font-size: 2.2rem;
    }

    #contact address{
    font-style: normal;
    margin-left: 0;
    font-size: 1rem;
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 1rem;
} (added flex-wrap: wrap; ONLY)

@media (min-width: 600px){
    #contact address{
        font-size: 1.15rem;
        gap: 2rem;
    }
}

@media (min-width: 1000px){
    #contact address{
        margin-left: var(--standardGap);
        font-size: 1.3rem;
        gap: 60px;
    }
}

Prompt: "Help me develop CSS code that makes all images in my #projects ID centered and wrapping properly for any screen width (from 0px to 1024+px). Please only use CSS and do not modify any of my HTML file."
Results:"Updated style.css so project images center and wrap naturally within each project card. Images are constrained to the card width and retain their proportions; headings and paragraphs remain left-aligned.

No HTML was changed. git diff --check passed."
AI-Generated Code:
#projects article{
    margin: 0;
    padding: 20px;
    background: #EFEFF0;
    text-align: center;
}

#projects article h3,
#projects article p{
    text-align: left;
}

    max-width: calc(100% - 0.5rem);
    height: auto;
    margin: 0.5rem 0.25rem; 
(in #projects img{})
