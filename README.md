<p align="center">
  <img src="https://github.com/user-attachments/assets/3dd6d1f5-2673-4d56-9c50-b57ddde29a15" alt="Dryz3R Banner" style="width:100%; max-width:100%;">
</p>

<style>
  /* Keyframe Animations */
  @keyframes pulse {
    0% {
      transform: scale(1);
      box-shadow: 0 0 0 rgba(0, 0, 0, 0);
    }
    50% {
      transform: scale(1.05);
      box-shadow: 0 0 20px rgba(0, 0, 0, 0.3);
    }
    100% {
      transform: scale(1);
      box-shadow: 0 0 0 rgba(0, 0, 0, 0);
    }
  }

  @keyframes slideInLeft {
    0% {
      transform: translateX(-100%);
      opacity: 0;
    }
    100% {
      transform: translateX(0);
      opacity: 1;
    }
  }

  @keyframes slideInRight {
    0% {
      transform: translateX(100%);
      opacity: 0;
    }
    100% {
      transform: translateX(0);
      opacity: 1;
    }
  }

  @keyframes fadeIn {
    0% {
      opacity: 0;
    }
    100% {
      opacity: 1;
    }
  }

  @keyframes rotate {
    0% {
      transform: rotate(0deg);
    }
    100% {
      transform: rotate(360deg);
    }
  }

  @keyframes bounce {
    0%, 20%, 50%, 80%, 100% {
      transform: translateY(0);
    }
    40% {
      transform: translateY(-10px);
    }
    60% {
      transform: translateY(-5px);
    }
  }

  @keyframes shimmer {
    0% {
      background-position: -1000px 0;
    }
    100% {
      background-position: 1000px 0;
    }
  }

  @keyframes gradient {
    0% {
      background-position: 0% 50%;
    }
    50% {
      background-position: 100% 50%;
    }
    100% {
      background-position: 0% 50%;
    }
  }

  /* General Styling for README */
  /* Applying styles to the body or a main container might not work directly in all README environments. */
  /* We'll target specific HTML elements commonly used in READMEs. */

  /* Ensure images are responsive */
  img {
    max-width: 100%;
    height: auto;
    display: block; /* Prevent extra space below images */
    margin: 0 auto; /* Center images if they are block elements */
  }

  /* Styling for the main banner image */
  .banner-image {
    width: 100%;
    max-width: 100%;
    border-radius: 0 !important; /* Ensure banner is not rounded */
    margin-bottom: 30px;
    animation: fadeIn 2s ease-out;
  }

  h1 {
    text-align: center;
    color: #333;
    margin-bottom: 20px;
    animation: bounce 2s infinite ease-in-out;
    text-shadow: 2px 2px 5px rgba(0, 0, 0, 0.1);
  }

  p {
    text-align: center;
    margin-bottom: 20px;
    color: #555;
  }

  hr {
    border: 0;
    height: 2px;
    background: linear-gradient(90deg, rgba(0,0,0,0) 0%, #ccc 50%, rgba(0,0,0,0) 100%);
    margin: 50px 0;
  }

  h2 {
    text-align: center;
    color: #444;
    margin-bottom: 40px;
    font-size: 1.8em;
    position: relative;
    animation: slideInLeft 1s ease-out;
  }

  h2::after {
    content: '';
    display: block;
    width: 80px;
    height: 4px;
    background: linear-gradient(90deg, #e73c7e, #23a6d5);
    margin: 10px auto 0;
    border-radius: 2px;
    animation: pulse 1.5s infinite ease-in-out; /* Animate the underline */
  }


  /* Styling for paragraph containing badges */
  p.project-badges, p.skill-badges, p.stats-badges, p.contact-badges {
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
    gap: 20px;
    margin-bottom: 30px;
    text-align: center; /* Ensure text inside is centered if any */
  }

  /* Styling for links around badges */
  p.project-badges a, p.contact-badges a {
     text-decoration: none;
     display: inline-block;
     animation: pulse 2s infinite ease-in-out;
     border-radius: 12px; /* Make badges rounder */
     overflow: hidden; /* Ensure inner content respects border-radius */
  }


  /* Styling for the badge images themselves */
  p.project-badges img, p.skill-badges img, p.stats-badges img, p.contact-badges img {
    border-radius: 12px !important; /* Apply border-radius to images within links */
    transition: transform 0.3s ease-in-out, box-shadow 0.3s ease-in-out;
    display: inline-block; /* Ensure badges sit side-by-side */
    margin: 0; /* Remove default paragraph margins */
  }

  /* Hover effects for badges */
  p.project-badges a:hover img, p.contact-badges a:hover img, p.skill-badges img:hover, p.stats-badges img:hover, p.repo-stats a:hover img {
    transform: translateY(-5px) rotate(2deg);
    box-shadow: 0 8px 15px rgba(0, 0, 0, 0.2);
    background: linear-gradient(45deg, #ff9a9e 0%, #fad0c4 99%, #fad0c4 100%);
    background-size: 200% 200%;
    animation: gradient 3s ease infinite;
  }

  /* Animations for badges on load */
  p.skill-badges img {
    animation: fadeIn 1.5s ease-out;
    transition: transform 0.3s ease-in-out;
  }

  p.skill-badges img:nth-child(odd) {
    animation-delay: 0.2s;
  }

  p.skill-badges img:nth-child(even) {
    animation-delay: 0.4s;
  }

  /* Styling for stats images */
  p.stats-badges {
    gap: 10px; /* Adjust gap for stats images */
  }

  p.stats-badges img {
    width: 48%; /* Maintain original width */
    margin: 0; /* Remove individual margins */
    animation: slideInRight 1s ease-out;
  }

  /* Styling for key repository stats (stars/forks) */
  p.repo-stats {
      gap: 10px; /* Adjust gap for repo stats badges */
  }

  p.repo-stats a {
      animation: none; /* Remove pulse animation from star/fork badges */
  }

  p.repo-stats img {
      animation: fadeIn 1.5s ease-out;
      transition: transform 0.3s ease-in-out;
  }

  p.repo-stats a:nth-child(odd) img {
    animation-delay: 0.3s;
  }

  p.repo-stats a:nth-child(even) img {
    animation-delay: 0.6s;
  }

</style>

<h1 align="center">Hello, I'm Dryz3R!</h1>

<p align="center">
  Welcome to my GitHub profile. Here, you will find my projects, contributions, and an overview of my skills.
</p>

---

## Featured Projects

<p align="center">
  Explore some of my most notable projects:
</p>

<p align="center">
  <!-- Project XIWA-TOOL -->
  <a href="https://github.com/dryzer0dev/XIWA-TOOL/">
    <img src="https://img.shields.io/badge/XIWA--TOOL-Repository-%23003366?style=for-the-badge&logo=github&logoColor=white" alt="XIWA-TOOL Repository">
  </a>
  &nbsp;&nbsp;&nbsp;&nbsp; <!-- Spacing -->
  <!-- Project xiwa-air-crackers -->
  <a href="https://github.com/dryzer0dev/xiwa-air-crackers">
    <img src="https://img.shields.io/badge/xiwa--air--crackers-Repository-%23660000?style=for-the-badge&logo=github&logoColor=white" alt="xiwa-air-crackers Repository">
  </a>
</p>

<p align="center">
  Check out my other repositories for more exciting projects!
</p>

---

## About Me

<p align="center">
  I am a developer passionate about creating and exploring new technologies.
</p>

<p align="center">
  My skills include:
  <br><br>
  <img src="https://img.shields.io/badge/-Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python">
  <img src="https://img.shields.io/badge/-HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white" alt="HTML5">
  <img src="https://img.shields.io/badge/-CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white" alt="CSS3">
  <img src="https://img.shields.io/badge/-JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black" alt="JavaScript">
  <img src="https://img.shields.io/badge/-React-61DAFB?style=for-the-badge&logo=react&logoColor=black" alt="React">
  <img src="https://img.shields.io/badge/-C++-00599C?style=for-the-badge&logo=c%2B%2B&logoColor=white" alt="C++">
  <img src="https://img.shields.io/badge/-C-A8B9CC?style=for-the-badge&logo=c&logoColor=white" alt="C">
  <img src="https://img.shields.io/badge/-C%23-239120?style=for-the-badge&logo=c-sharp&logoColor=white" alt="C#">
</p>

<p align="center">
  Currently, I am expanding my knowledge in **ASM** and **Ruby**.
</p>

<p align="center">
  I am the official creator of all **XIWA** projects and the **python simplifier** project.
</p>

---

## GitHub Statistics

<p align="center">
  An overview of my activity on GitHub:
</p>

<p align="center">
  <!-- GitHub Stats -->
  <img src="https://github-readme-stats.vercel.app/api?username=dryzer0dev&show_icons=true&theme=radical&include_all_commits=true" alt="Dryz3R's GitHub Stats" style="width: 48%; margin: 5px;">
  <!-- GitHub Streak Stats -->
  <img src="https://github-readme-streak-stats.herokuapp.com/?user=dryzer0dev&theme=radical&hide_border=true" alt="Dryz3R's GitHub Streak" style="width: 48%; margin: 5px;">
</p>

### Key Repository Statistics

<p align="center">
  <!-- siplifier.py Stats -->
  <a href="https://github.com/dryzer0dev/siplifier.py/stargazers">
    <img src="https://img.shields.io/github/stars/dryzer0dev/siplifier.py?style=for-the-badge&logo=star&logoColor=white&color=FFD700" alt="GitHub stars">
  </a>
  <a href="https://github.com/dryzer0dev/siplifier.py/network/members">
    <img src="https://img.shields.io/github/forks/dryzer0dev/siplifier.py?style=for-the-badge&logo=git-fork&logoColor=white&color=00CED1" alt="GitHub forks">
  </a>
  <br><br> <!-- Spacing -->

  <!-- WIXA_SKID_PANEL Stats -->
  <a href="https://github.com/dryzer0dev/WIXA_SKID_PANEL/stargazers">
    <img src="https://img.shields.io/github/stars/dryzer0dev/WIXA_SKID_PANEL?style=for-the-badge&logo=star&logoColor=white&color=FFD700" alt="GitHub stars">
  </a>
  <a href="https://github.com/dryzer0dev/WIXA_SKID_PANEL/network/members">
    <img src="https://img.shields.io/github/forks/dryzer0dev/WIXA_SKID_PANEL?style=for-the-badge&logo=git-fork&logoColor=white&color=00CED1" alt="GitHub forks">
  </a>
</p>

---

## Contact Me

<p align="center">
  Feel free to reach out if you have any questions or collaboration opportunities!
</p>

<p align="center">
  <a href="mailto:shiraka0dev@gmail.com">
    <img src="https://img.shields.io/badge/-Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email">
  </a>
  &nbsp;&nbsp;&nbsp;&nbsp; <!-- Spacing -->
  <a href="mailto:dryzer0dev@gmail.com">
    <img src="https://img.shields.io/badge/-Email-D14836?style=for-the-badge&logo=gmail&logoColor=white" alt="Email">
  </a>
  &nbsp;&nbsp;&nbsp;&nbsp; <!-- Spacing -->
   <img src="https://img.shields.io/badge/-Discord-7289DA?style=for-the-badge&logo=discord&logoColor=white" alt="Discord">
   &nbsp;_.shiraka
</p>

---

<p align="center">
  Thanks for visiting!
</p>
