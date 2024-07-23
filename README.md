<h3 align="center">I'm a 3rd year student pursuing Bachelor's in Electronics and Communication Engineering🎓 from BIT MESRA. I'm a passionate learner who's always willing to learn and work across technologies and domains. I love to explore new technologies and leverage them to solve real-life problems. I'm currently into Web Development and working on my Data Structures and Algorithms skills.</h3>
<img align="right" alt="Coding" width = "400" src="https://user-images.githubusercontent.com/57133330/188281408-c67df9ee-fd1f-4b37-833b-f02848f1ce02.gif">

<br>
<h3 align="left">Languages and Tools:</h3>
<p align="left"> <a href="https://www.cprogramming.com/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/c/c-original.svg" alt="c" width="40" height="40"/> </a> <a href="https://www.w3schools.com/css/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/css3/css3-original-wordmark.svg" alt="css3" width="40" height="40"/> </a>  <a href="https://www.w3.org/html/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/html5/html5-original-wordmark.svg" alt="html5" width="40" height="40"/> </a> <a href="https://www.java.com" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/java/java-original.svg" alt="java" width="40" height="40"/> </a> <a href="https://developer.mozilla.org/en-US/docs/Web/JavaScript" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/javascript/javascript-original.svg" alt="javascript" width="40" height="40"/> </a> <a href="https://www.mongodb.com/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/mongodb/mongodb-original-wordmark.svg" alt="mongodb" width="40" height="40"/> </a> <a href="https://www.mysql.com/" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/mysql/mysql-original-wordmark.svg" alt="mysql" width="40" height="40"/> </a> <a href="https://nodejs.org" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/nodejs/nodejs-original-wordmark.svg" alt="nodejs" width="40" height="40"/> </a> <a href="https://www.python.org" target="_blank" rel="noreferrer"> <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg" alt="python" width="40" height="40"/> </a> </p>
<br>
<h3 align="left">Socials:</h3>
<p align="left">
<a href="https://twitter.com/prtkv3" target="blank"><img align="center" src="https://cdn.prod.website-files.com/5d66bdc65e51a0d114d15891/64cebdd90aef8ef8c749e848_X-EverythingApp-Logo-Twitter.jpg" alt="prtkv3" height="30" width="40" /></a>
<a href="https://linkedin.com/in/prateekverma0" target="blank"><img align="center" src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/linked-in-alt.svg" alt="prateekverma0" height="30" width="40" /></a>
</p><p>Mail: <a href="mailto:prateek222rithik@gmail.com">prateek222rithik@gmail.com</a></p>
<!-- languages mostly used -->
<div id="stats"></div>
    <script>
        const fetchStats = async () => {
            const repos = await (await fetch(`https://api.github.com/users/prtkvs/repos`)).json();
            const stats = {};
            for (const repo of repos) {
                const langs = await (await fetch(repo.languages_url)).json();
                for (const [lang, bytes] of Object.entries(langs)) stats[lang] = (stats[lang] || 0) + bytes;
            }
            const sortedStats = Object.entries(stats).sort((a, b) => b[1] - a[1]);
            const totalBytes = sortedStats.reduce((sum, [, bytes]) => sum + bytes, 0);
            document.getElementById('stats').innerHTML = sortedStats.map(([lang, bytes]) => `
                <div class="language">
                    <span>${lang}</span>
                    <div style="width: ${((bytes / totalBytes) * 100).toFixed(2)}%; background-color: ${'#' + Math.floor(Math.random() * 16777215).toString(16)};" class="bar"></div>
                    <span>${((bytes / totalBytes) * 100).toFixed(2)}%</span>
                </div>
            `).join('');
        };
        fetchStats();
    </script>
