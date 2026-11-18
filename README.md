<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:4A0D2E,50:C2185B,100:FF8FC7&height=210&section=header&text=Taleem%20AI&fontSize=56&fontColor=FFFFFF&fontAlignY=36&desc=Curriculum-grounded%20bilingual%20AI%20tutor%20for%20Pakistani%20students&descSize=16&descAlignY=58" width="100%" alt="Taleem AI"/>

<p>
  <img src="https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=nextdotjs&logoColor=white" alt="Next.js"/>
  <img src="https://img.shields.io/badge/Firebase-FFCA28?style=for-the-badge&logo=firebase&logoColor=black" alt="Firebase"/>
  <img src="https://img.shields.io/badge/Groq-F55036?style=for-the-badge" alt="Groq"/>
  <img src="https://img.shields.io/badge/Gemini-8E75B2?style=for-the-badge&logo=googlegemini&logoColor=white" alt="Gemini"/>
  <img src="https://img.shields.io/badge/Vercel-000000?style=for-the-badge&logo=vercel&logoColor=white" alt="Vercel"/>
</p>

**[Live demo](https://taleem-ai.vercel.app)** · English / اردو

</div>

---

## The idea

Most students in Pakistan prepare for board exams by memorising, and general-purpose chatbots do not help much: they answer from the whole internet, drift away from the syllabus, and sometimes make things up. **Taleem AI** is a study companion that only teaches from what the student is actually examined on: official curriculum textbooks, board papers and the notes the student uploads. It works in English and Urdu, by text or by voice.

---

## Features

**Tutor that stays inside the syllabus.** A retrieval-augmented tutor searches the student's curriculum material and answers only from it. If the answer is not in the sources, it says so instead of inventing one. Available as a text chat and as a spoken conversation.

**Voice first, in two languages.** Students can ask questions, request notes or move around the app by speaking English or Urdu, which makes it usable for learners who are less comfortable typing.

**Study suite from any document.** Upload a PDF or paste text and generate:
- structured notes with key terms and concept maps
- quizzes with instant scoring
- flashcards for quick revision
- slide presentations
- past-paper analysis that shows which topics come up most often

**YouTube lecture summaries.** Paste a lecture link and get the main ideas in organised sections with timestamps.

**Learning that feels like a game.** Levels from Beginner to Ustaad, badges, daily streaks, points and subject leaderboards, plus a dashboard showing progress, quiz accuracy and suggested next steps.

**Six educational games**

| Game | Subject |
|---|---|
| Map Master Pakistan | Geography |
| Subject Sprint | General knowledge |
| Vocabulary Voyage | English vocabulary |
| Timeline Tangle | History |
| Urdu Haroof Hero | Urdu literacy |
| Science Detective | Scientific reasoning |

---

## How it works

```
Student (voice / text / files, English or Urdu)
        |
   Next.js app  -->  Server Actions  -->  AI flows (tutor, notes, quiz, flashcards,
        |                                  mind maps, slides, past papers, YouTube)
        |                                          |               |
   Firebase (Auth + Firestore)  <------  RAG retrieval      Groq / Gemini
```

## Tech stack

| Layer | Technology |
|---|---|
| App | Next.js (App Router, Server Actions), React |
| UI | Tailwind CSS, shadcn/ui, Framer Motion |
| LLMs | Groq (Llama 3.3 70B), Gemini through Google Genkit |
| Retrieval | Embeddings and RAG over curriculum and uploaded documents |
| Auth and data | Firebase Authentication, Firestore |
| Extras | Mermaid mind maps, Recharts, PptxGenJS, YouTube transcripts, Web Speech API |
| Hosting | Vercel |

---

## Run it locally

Requirements: Node.js 18+, a Groq API key, and optionally a Firebase project.

```bash
git clone https://github.com/21Afnan/Taleem-AI.git
cd Taleem-AI
npm install
cp .env.example .env.local   # add GROQ_API_KEY and, if used, Gemini and Firebase keys
npm run dev                  # http://localhost:3000
```

---

## Team

Taleem AI is a team project built by **Afnan Shoukat** and **Usama Shahid** (BS Artificial Intelligence, NUML Islamabad). The original repository is [fewgets/Taleem-AI](https://github.com/fewgets/Taleem-AI); this copy keeps the full commit history.

## Contact

For a demo, feedback or collaboration:

<div align="center">

<a href="mailto:afnanshoukat35@gmail.com?subject=Taleem%20AI">
  <img src="https://img.shields.io/badge/Email-afnanshoukat35%40gmail.com-FF4FA3?style=for-the-badge&logo=gmail&logoColor=white&labelColor=4A0D2E" alt="Email"/>
</a>
<a href="https://www.linkedin.com/in/afnanshoukat">
  <img src="https://img.shields.io/badge/LinkedIn-Afnan%20Shoukat-FF4FA3?style=for-the-badge&logo=linkedin&logoColor=white&labelColor=4A0D2E" alt="LinkedIn"/>
</a>
<a href="https://github.com/21Afnan">
  <img src="https://img.shields.io/badge/GitHub-21Afnan-FF4FA3?style=for-the-badge&logo=github&logoColor=white&labelColor=4A0D2E" alt="GitHub"/>
</a>

</div>
