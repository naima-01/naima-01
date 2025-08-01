<pre>
   ∧,,,∧      ┏━━━━━━━━━
(  ̳• · • ̳)  ~ ♡  Hi, I'm Naima! ♡
/       づ              ━━━━━━━━━┛
</pre>
<p>
I’m currently pursuing a degree in Computer Science with a minor in Math. I’m passionate about combining art and technology to create thoughtful, human-centered digital experiences. With a strong interest in ethical tech and AI, I’m especially drawn to projects that explore creativity, design, and social impact through code.
</p>

<hr style="border: none; height: 1px; background-color: #ccc; margin: 30px 0;" />

🛠  Technical Skills
<a name="technical-skills"></a>

[<img src="https://img.shields.io/badge/JavaScript-282C34?logo=javascript&logoColor=F7DF1E" alt="JavaScript logo" title="JavaScript" height="25" />][tech_tools_anchor]&nbsp;
[<img src="https://img.shields.io/badge/HTML5-282C34?logo=html5&logoColor=E34F26" alt="HTML5 logo" title="HTML5" height="25" />][tech_tools_anchor]&nbsp;
[<img src="https://img.shields.io/badge/CSS3-282C34?logo=css3&logoColor=1572B6" alt="CSS3 logo" title="CSS3" height="25" />][tech_tools_anchor]&nbsp;
[<img src="https://img.shields.io/badge/Python-282C34?logo=python&logoColor=3776AB" alt="Python logo" title="Python" height="25" />][tech_tools_anchor]&nbsp;
[<img src="https://img.shields.io/badge/C++-282C34?logo=c%2B%2B&logoColor=00599C" alt="C++ logo" title="C++" height="25" />][tech_tools_anchor]&nbsp;
[<img src="https://img.shields.io/badge/Godot-282C34?logo=godot-engine&logoColor=478CBF" alt="Godot logo" title="Godot" height="25" />][tech_tools_anchor]&nbsp;

[tech_tools_anchor]: #technical-skills

![Snake animation](https://github.com/madushadhanushka/github-readme/blob/output/github-contribution-snake.svg)
name: Contribution snake

on:
  schedule: # execute every 12 hours
    - cron: "* */12 * * *"
  workflow_dispatch:

jobs:
  build:
    name: Jobs to update snake grid
    runs-on: ubuntu-latest
    steps:
      - uses: Platane/snk@master
        id: snake-gif
        with:
          github_user_name: madushadhanushka
          svg_out_path: dist/github-contribution-snake.svg

      - uses: crazy-max/ghaction-github-pages@v2.1.3
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
