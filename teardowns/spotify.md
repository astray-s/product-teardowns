# Spotify — Product Teardown

**Date:** September 2026  
**Category:** Music / Audio Streaming  
**Framework:** Problem → What Works → What I'd Change → Success Metrics → PM Insight

---

## What problem does it solve?

Spotify solves a deceptively hard problem: it gives you something to listen to when you don't know what you want to hear. Music discovery used to require effort — digging through blogs, borrowing CDs, waiting for radio. Spotify collapsed all of that into a single interface where 100+ million tracks are one tap away.

But the real product insight isn't *access* — it's *curation*. The hard part isn't having all the music; it's surfacing the right song at the right moment.

---

## What it does well

### 1. Discover Weekly and algorithmic playlists are genuinely good
This is where Spotify's collaborative filtering and audio-feature models shine. Discover Weekly feels personal in a way most recommendation systems don't — it surfaces tracks that match my taste profile without just recycling what I've already played.

As someone interested in how AI systems model human preferences, I find this fascinating: Spotify is essentially building a low-resolution cognitive model of each listener's aesthetic instincts. The blend of collaborative filtering ("people like you also listened to") and audio feature analysis (BPM, valence, energy, instrumentalness) produces recommendations that feel intuitive rather than algorithmic.

### 2. Context-aware listening
Spotify doesn't just know *what* I like — it's learning *when* I like it. Morning mixes trend calmer; workout playlists push energy. This is smart because music preference is deeply contextual, not static. The product reflects real psychoacoustic research: mood, arousal, and environment all shape what sounds "right."

### 3. Spotify Wrapped turned passive data into a social identity artifact
Transforming listening data into something users *want* to broadcast is brilliant product thinking. It doubles as organic acquisition — millions of users voluntarily share Spotify's branding every December. It's a masterclass in making engagement visible without making it feel extractive.

---

## What I'd change

### 1. The search experience for moods and activities is weak
**The problem:** If I type "music for deep focus while coding at 2am," Spotify gives me a handful of editorial playlists. The natural-language understanding is shallow.

**The fix:** A prompt-driven search layer that translates how people *actually think* about music into the audio feature parameters Spotify already uses internally. With Spotify's existing feature data (valence, energy, instrumentalness, BPM) and modern LLM tooling, parsing "chill but not sad, no lyrics, ~120 BPM" into filter parameters is technically feasible today.

**Why this matters:** People don't search for music like they search for information. They search by feeling, context, and activity. The current search treats music like a database query. It should work more like a conversation.

### 2. Podcast and music coexist awkwardly in the same feed
**The problem:** The listening modes are fundamentally different — music is ambient and interruptible; podcasts demand sustained attention. Spotify pushes podcasts aggressively into the music feed, which creates intent friction.

**The fix:** A simple mode toggle ("music mode" vs. "listening mode") so the algorithm knows what kind of session you're in. Home feed content would adapt accordingly. This isn't a hard engineering problem — it's a product framing problem.

**Why this matters:** Right now it feels like Spotify is optimizing for engagement minutes at the expense of user intent clarity. Those aren't always the same thing.

### 3. Collaborative playlists have barely evolved
**The problem:** Group playlists are a huge social use case — road trips, parties, shared gym playlists — but the feature is barebones. No voting, no commenting, no "suggest a track" queue.

**The fix:** Lightweight social mechanics: upvote/downvote within a shared playlist, async track suggestions the owner can approve, and a live listening session mode with a shared queue.

**Why this matters:** The social graph already exists (followers, shared playlists). Spotify hasn't done much to make it interactive. This is low-hanging fruit for engagement and retention among friend groups.

---

## How I'd measure success

For the **natural-language search** improvement:
- **Primary:** Search-to-play conversion rate — did the user actually start listening after searching?
- **Primary:** Session length post-search — did they stay longer?
- **Secondary:** Reduction in the "search → back → browse → give up" abandon loop, measurable through funnel analysis
- **Guardrail:** Don't cannibalize Discover Weekly or Daily Mix engagement — those are core retention drivers

---

## PM insight

Good product thinking means noticing the gap between how users *think* about what they want and how the product *asks* them to express it — then closing that gap without adding complexity.

Spotify's core discovery experience does this exceptionally well. Its search doesn't.

---

*Part of [product-teardowns](https://github.com/astray-s/product-teardowns) by [@astray-s](https://github.com/astray-s)*
