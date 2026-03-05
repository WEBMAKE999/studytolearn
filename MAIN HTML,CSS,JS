<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>AU Exam Library (Years 9–12)</title>

<style>

body{
font-family:-apple-system,BlinkMacSystemFont,"Segoe UI",Roboto,sans-serif;
margin:40px auto;
max-width:900px;
background:#fafafa;
color:#222;
}

h1{
font-weight:500;
font-size:1.8em;
}

.subtitle{
color:#666;
margin-bottom:30px;
}

.state{
margin-top:35px;
font-size:1.2em;
font-weight:500;
}

details{
border:1px solid #e5e5e5;
border-radius:8px;
padding:10px 15px;
margin:10px 0;
background:white;
}

summary{
cursor:pointer;
font-weight:500;
}

.paper{
margin:10px 0;
padding-left:10px;
}

.paper a{
text-decoration:none;
color:#111;
}

.paper a:hover{
text-decoration:underline;
}

.desc{
font-size:0.85em;
color:#666;
}

input{
width:100%;
padding:10px;
border:1px solid #ddd;
border-radius:6px;
margin-bottom:15px;
font-size:0.95em;
}

button{
padding:10px 16px;
border:none;
background:#111;
color:white;
border-radius:6px;
cursor:pointer;
margin-top:5px;
}

button:hover{
opacity:0.9;
}

.apiBox{
margin-top:25px;
padding:15px;
background:white;
border:1px solid #e5e5e5;
border-radius:8px;
}

footer{
margin-top:60px;
font-size:0.8em;
color:#888;
}

</style>

<script>

function searchPapers(){
let input=document.getElementById("search").value.toLowerCase();
let papers=document.getElementsByClassName("paper");

for(let i=0;i<papers.length;i++){
let text=papers[i].innerText.toLowerCase();
papers[i].style.display=text.includes(input)?"":"none";
}
}


async function wikiSearch(){

let query=document.getElementById("studySearch").value

let url=`https://en.wikipedia.org/api/rest_v1/page/summary/${query}`

let res=await fetch(url)

let data=await res.json()

document.getElementById("wikiResult").innerHTML=
"<b>"+data.title+"</b><p>"+data.extract+"</p>"

}



function youtubeSearch(){

let query=document.getElementById("studySearch").value

let embed=
`https://www.youtube.com/embed?listType=search&list=${query}+lesson`

document.getElementById("yt").innerHTML=
`<iframe width="100%" height="315" src="${embed}" frameborder="0" allowfullscreen></iframe>`

}



function generateFlashcards(){

let topic=document.getElementById("studySearch").value

let cards=[
`Define ${topic}`,
`Explain the main concept of ${topic}`,
`What are 3 key facts about ${topic}?`,
`Why is ${topic} important?`,
`Give an example of ${topic}`
]

let html=""

cards.forEach(c=>{
html+=`<p>🧠 ${c}</p>`
})

document.getElementById("flashcards").innerHTML=html

}



function randomTip(){

let tips=[
"Study 25 minutes then take a 5 minute break (Pomodoro).",
"Teach the topic to someone else to improve retention.",
"Do past exam papers under timed conditions.",
"Write summaries in your own words.",
"Mix subjects to improve memory retention.",
"Sleep improves memory consolidation."
]

let tip=tips[Math.floor(Math.random()*tips.length)]

document.getElementById("tip").innerHTML="💡 "+tip

}

</script>

</head>

<body>

<h1>✦ Australian Exam Library</h1>
<div class="subtitle">Free official test papers · Years 9–12 · All States</div>

<input id="search" onkeyup="searchPapers()" placeholder="Search papers by subject or state">

<div class="apiBox">

<h3>📚 Study Search</h3>

<input id="studySearch" placeholder="Type a topic (e.g algebra, WW2, photosynthesis)">

<button onclick="wikiSearch()">Explain Topic</button>
<button onclick="youtubeSearch()">Find Video Lesson</button>
<button onclick="generateFlashcards()">Generate Flashcards</button>
<button onclick="randomTip()">Study Tip</button>

<div id="wikiResult"></div>
<div id="yt"></div>
<div id="flashcards"></div>
<div id="tip"></div>

</div>


<div class="state">◦ Victoria (VIC)</div>

<details>
<summary>Year 12 — VCE</summary>

<div class="paper">
<a href="https://www.vcaa.vic.edu.au/assessment/vce/examination-specifications-past-examinations-and-external-assessment-reports" target="_blank">
VCE Past Exams (All Subjects)
</a>
<div class="desc">Official past exams + reports.</div>
</div>

</details>


<div class="state">◦ New South Wales (NSW)</div>

<details>
<summary>Year 12 — HSC</summary>

<div class="paper">
<a href="https://educationstandards.nsw.edu.au/wps/portal/nesa/resource-finder/hsc-exam-papers" target="_blank">
HSC Past Exam Papers
</a>
<div class="desc">Official HSC exams + marking guidelines.</div>
</div>

</details>


<div class="state">◦ Queensland (QLD)</div>

<details>
<summary>Year 12 — QCE</summary>

<div class="paper">
<a href="https://www.qcaa.qld.edu.au/senior/assessment/external-assessment/past-papers" target="_blank">
QCE External Exam Papers
</a>
<div class="desc">External assessment papers + answers.</div>
</div>

</details>


<div class="state">◦ Western Australia (WA)</div>

<details>
<summary>Year 12 — WACE</summary>

<div class="paper">
<a href="https://www.scsa.wa.edu.au/publications/examination-papers" target="_blank">
WACE Past Exam Papers
</a>
<div class="desc">Past papers + answer keys.</div>
</div>

</details>


<footer>

Minimal AU Exam Library · Free Study Tools · Updated 2026

</footer>

</body>
</html>
