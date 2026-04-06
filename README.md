# Insight-on-Asake-and-Dj-Snake--Worship-A-power-Bi-dashboard-
This is a YouTube/social media comment analytics dashboard built to analyse audience engagement on the song "Worship" by Asake featuring DJ Snake. It tracks 4,061 total comments and 16K likes on those comments, examining engagement patterns across days of the week, time of day, artist attribution, user activity, and day-of-month distribution. This project was built with Power BI and Google Sheets, which were used for exporting all comments and likes for Asake's YouTube page using JavaScript. This project provides a detailed picture of when fans are most active, which artists' fanbase is driving conversation, and which individual users are the most prolific commenters — making it a useful tool for music marketing, social listening, and audience analysis.

![Thumbnail](https://i.ytimg.com/vi/XvzafoUpWNg/maxresdefault.jpg)

## Data Cleaning Steps (Inferred)
1. Comment scraping and export structuring — Raw comments were extracted using either the YouTube Data API v3 via googlesheets. Each record would contain fields such as: comment text, author username (user ID), timestamp, like count, and reply count. These were imported into a Google Sheet before being loaded into the BI tool.
2. Timestamp parsing and time field extraction — Raw comment timestamps were parsed to extract: date, day of month, day of week name, hour of day, and a custom "Time Group" label. The time groups (e.g., "12:00 AM–2:59 AM", "3:00 AM–5:59 AM") were defined as bucketed categories using conditional logic applied to the extracted hour field.
3. Day-of-week labelling — Each comment's date was used to derive a weekday name (Sunday through Saturday) via a date function. The order of days (Sun–Sat) was then set manually to ensure correct chronological display rather than alphabetical sorting.
4. Day-of-month extraction — The numeric day (1–31) was extracted from each timestamp to populate the "All Comments by Day" visual on the right panel, revealing the release-day spike on day 20.
5. Artist attribution tagging — Comment text was scanned using keyword matching to tag each comment as belonging to "ASAKE", "DJ SNAKE", or "Unspecified." 
6. Username anonymisation and truncation — User IDs are displayed in truncated form (e.g., "@LordNairaOffi…", "@JuniorGazaariel") to respect privacy and fit the visual. Full usernames were either truncated to a fixed character length or partially masked during the data preparation step.


## Key Performance Indicators (KPIs)
-- **Total comments = ** 4,061 across all users

-- **Total likes on comments =** 16K community endorsements

-- **% likes on comments =** 11.23% like-to-comment engagement rate

-- **Total replies to comments =** 456 11.2% reply rate

-- **Top weekday =** Thursday 2,022 comments

-- **Top artist attribution =** ASAKE 498 tagged comments

-- **Peak time group =** 12:00–2:59 AM, highest comment volume

## Observation 
-- 86.4% of comments have no artist attribution: 3,511 of 4,061 comments are labelled "Unspecified" in the Artist Popularity chart. Only 498 are tagged to ASAKE and 52 to DJ SNAKE, revealing that the artist tagging logic captures a very small fraction of the audience conversation.

-- Asake's fanbase is 10 times more vocal than DJ Snake's: Among tagged comments, ASAKE has 498 vs DJ SNAKE's 52 — a 9.6 times ratio. This confirms the song is being driven overwhelmingly by Asake's Afrobeats audience, with DJ Snake's electronic fanbase contributing minimally.

-- Thursday dominates the week with 2,022 comments: Thursday alone accounts for nearly half the weekly comment volume. Sunday (334) and Monday (208) are the next highest, while Wednesday (113) and Thursday are at opposite ends of the spectrum, a striking mid-week spike.

-- Wednesday is the quietest day at just 113 comments: Wednesday records the lowest comment count across the full week,  which was 18 times fewer than Thursday. 

-- 12:00 AM–2:59 AM is the single busiest time block: The late-night/early-morning window generates the highest comment volume of any time group. Combined with 9:00 PM–11:59 PM also being active, this confirms the audience is primarily engaging in evening and nighttime hours — typical for Afrobeats/nightlife-adjacent content.

-- Day 20 has a massive spike of 1,953 comments: The "All Comments by Day" bar chart on the right shows an enormous concentration on the 20th of the month (1,953 comments), with much smaller counts on surrounding days. This was because the song was released on the 20th of March, 2026.

-- 456 replies represent an 11.2% reply-to-comment rate: Out of 4,061 total comments, 456 generated a reply thread, indicating active back-and-forth conversation among fans. This is a reasonable engagement depth for a music video comment section.

-- 11.23% like-to-comment ratio signals passive engagement: With 16K likes spread across 4,061 comments (averaging ~3.9 likes per comment), many comments are being written but not widely endorsed. A higher like rate would indicate more comments resonating as "community sentiments" rather than individual reactions.

## Conclusion
The "Worship" collaboration between Asake and DJ Snake has generated meaningful organic engagement, with 4,061 comments and 16K comment likes reflecting an active and vocal fanbase. The data tells a clear story: this is fundamentally an Asake-driven release. His fanbase accounts for nearly 10 times the tagged engagement of DJ Snake's, and the overall comment tone and timing — peaking at midnight and in the late evening- aligns perfectly with the Afrobeats listening culture of nighttime, social, and emotional engagement. The 11.23% like-to-comment ratio and modest reply rate suggest fans are commenting individually but not heavily engaging with each other's thoughts — a surface-level engagement pattern rather than a deep community conversation.

## Recommendations
1. Maximise future release timing on Thursdays or Fridays. The data clearly shows that Thursday is the highest-engagement day for this audience. Scheduling future releases, teasers, or music video premieres on Thursday, ideally timed for the late-night window (9:00 PM–midnight), would align perfectly with when this fanbase is most active online.
2. Target the 12:00 AM–3:00 AM window for social media pushes. Since the peak comment time is the late-night/early-morning block, Instagram, X (Twitter), and TikTok promotional posts for Asake's future projects should be scheduled between 11:00 PM and 2:00 AM to catch maximum organic engagement while the audience is already active.
3. Develop a DJ Snake cross-audience activation strategy. With only 52 tagged comments from DJ Snake's fanbase versus 498 from Asake's, the collaboration has not meaningfully bridged into the electronic audience. DJ Snake's team could run targeted campaigns — TikTok challenges, electronic remix drops, or DJ set features to draw his Western audience into the conversation and expand the song's global reach.
4. Encourage community-to-community engagement to lift the reply rate. The 11.2% reply rate indicates fans are mostly leaving standalone comments rather than conversations. Pinned comments from the official channel asking fans a direct question (e.g., "What line hits hardest?"), or creator responses to top-liked comments, can spark reply threads and deepen the community feel around the song.
