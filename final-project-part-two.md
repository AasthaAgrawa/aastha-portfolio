| [home page](https://cmustudent.github.io/tswd-portfolio-templates/) | [data viz examples](dataviz-examples) | [critique by design](critique-by-design) | [final project I](final-project-part-one) | [final project II](final-project-part-two) | [final project III](final-project-part-three) |

When Campus AI Hits Its Limits: Part II
Developing the story after Part I
My Part I feedback helped me identify a gap in the explanation: I had shown two periods when requests frequently hit usage limits without clearly establishing the overall observation period or what “during the burst” meant. Readers could reasonably wonder whether I was examining known campus events, such as competitions or assignment deadlines.

The project examines general request patterns in 30 days of simulated OpenAI and Gemini logs covering October 1–30, 2026. The two spikes were identified through the request data. They were not selected because of a known campus event, and the logs do not establish what caused them.

For Part II, I am developing the project into a guided story for campus technology decision-makers. I want readers to understand the comparison, recognize what remains unknown, and leave with a concrete monitoring approach they could test.
Audience and intended takeaway
My primary audience is campus IT leaders and staff responsible for managing shared AI services. They may understand technology operations without being familiar with the structure of these particular request logs.

My central question is:

Where should campus IT teams focus their monitoring to identify short periods when AI requests hit usage limits?

The intended takeaway is that monitoring should examine both the number and percentage of requests hitting limits within individual hours and accounts. A monthly summary provides context, while hourly comparisons help identify periods that deserve investigation.
Defining the data and comparison periods
An AI request is a call sent to a provider’s service. In this project, a request “hit a usage limit” when the log recorded an HTTP 429 response. This counts requests, rather than individual people.
Term	Meaning in this project
Overall observation period	October 1–30, 2026, in the supplied simulated logs
Gemini spike	October 14, 9 a.m.–1 p.m., Pittsburgh time, for the selected enterprise project
OpenAI spike	October 21, 5–8 a.m., Pittsburgh time, for the selected production organization
During the spike	Requests within the specified date, time window, and organization or project
Same hours on other dates	Requests during the corresponding hours on other dates in the dataset, for that same organization or project


The time windows use an exclusive endpoint: Gemini includes the hours beginning at 9, 10, 11 a.m., and noon. OpenAI includes the hours beginning at 5, 6, and 7 a.m.

Here, “spike” describes the two selected periods with unusually high percentages of requests hitting limits. It does not imply that I know the cause or that these hours will repeatedly cause problems.
Storyboard and draft visualizations
Section 1: Establish the monthly context
Proposed heading: “What can a monthly summary tell us—and what needs a closer look?”

The opening will introduce the simulated dataset and explain usage limits in plain language. It will show 202,650 total requests and 4,124 requests that hit limits, approximately 2.0% overall.

I plan to develop the full-month timeline proposed in Part I, with separate panels for the selected Gemini project and OpenAI organization. It will help readers locate the two spikes within the broader observation period. I will distinguish the dataset-wide summary figures from the account-specific timelines.

Insert the monthly overview wireframe here. Identify it as a proposed layout until the actual timeline is built.
Section 2: Compare the spikes with corresponding hours
Draft heading: “About four in ten requests hit limits during two short spikes.”

The horizontal bar chart compares each spike with the same hours on other dates for the corresponding organization or project.
Provider and selected account	During the spike	Same hours on other dates
Gemini enterprise project	41.1% — 69 of 168 requests	2.1% — 108 of 5,090 requests
OpenAI production organization	43.9% — 61 of 139 requests	1.8% — 79 of 4,357 requests


The chart uses orange for the selected spike and blue for the comparison period. I will include dates, time windows, and request counts beside the chart so readers can understand the comparison without searching elsewhere.

Insert the individual bar-chart image here.
Section 3: Follow each spike hour by hour
Draft heading: “The selected spikes lasted four hours for Gemini and three for OpenAI.”

The hourly line charts show the periods surrounding each spike. Each point represents the hour beginning at the displayed time. Separate provider panels and a shared percentage scale support comparison.

This section adds timing and duration to the previous chart. I will retain the peak labels and make the Pittsburgh time zone explicit.

Insert the individual hourly-chart image here.
Section 4: Explain what an IT team could test
Proposed heading: “Use hourly alerts to decide where to investigate.”

My recommendation is to pilot monitoring on real campus AI logs, grouped by provider and organization or project. For each hour, the monitoring view should show:
- Total requests.
- Requests that hit usage limits.
- The percentage of requests that hit limits.
- A comparison with corresponding hours on other dates.
Alerts should consider both counts and percentages so that a high percentage based on very few requests does not receive the same interpretation as a large volume of rejected requests. Alert thresholds would need to be tested against real operating patterns.

When an alert identifies an unusual period, staff could investigate request timing, token usage, and the applicable account limits. These are investigation steps; the current analysis does not establish which intervention would resolve either spike.
Context, limitations, and transferability
The data was supplied for CMU’s Student IronViz competition and is simulated. The results demonstrate an analytical approach rather than documenting actual disruption to CMU services.

The logs do not show assignment deadlines, competitions, user identities, waiting times, or whether a later retry succeeded. I therefore cannot conclude that a particular campus activity caused a spike or quantify its effect on students.

The monitoring approach could be useful at other institutions that manage shared AI accounts. However, their request volumes, account structures, provider limits, and patterns of use may differ. Each institution would need to establish its own comparison periods and alert thresholds.

View the existing IronViz dashboard used as the starting point
User research protocol
Research goals
I want to test whether readers understand the observation period, the selected spike windows, and the comparison groups. These questions directly address the feedback on Part I.

I also want to learn whether readers can distinguish the findings from possible explanations and identify a useful next action.
Participant selection
I plan to interview three individuals, seeking perspectives relevant to the intended audience: someone with IT or software experience, someone with management or operational decision-making experience, and someone who uses campus AI tools.

I will describe their backgrounds broadly, without names or identifying details. I will also explain any limitations in how closely the participants represent campus IT decision-makers.
Procedure and interview script
I will show each participant the same draft and allow them to explore it before explaining the intended message. I will record their answers, points of hesitation, and questions.

Opening script:

“Thank you for reviewing my draft. I’m testing how clearly it communicates a story about simulated AI request data. Please tell me what you understand and anything that feels confusing.”

Questions:
1. What do you think the main message is?
2. What dates and time periods does the story cover?
3. What does “during the spike” mean? What is it being compared with?
4. What does a request hitting a usage limit mean to you?
5. What does the hourly chart add to the bar-chart comparison?
6. What can you conclude about the causes of the spikes and their effect on users?
7. If you were responsible for these services, what would you do next?
8. Which labels, explanations, or visual elements would you change?
I will use follow-up questions such as “What made you think that?” to understand how participants reached their interpretations.
Interview findings
Complete this section after conducting the three interviews. Include specific observations and accurately recorded quotes.
Topic	Participant 1	Participant 2	Participant 3
Broad relevant background			
Main message understood			
Interpretation of dates and spike windows			
Interpretation of comparison periods			
Understanding of limitations			
Suggested next action			
Specific confusion or useful quote			


Synthesis and planned revisions
After the interviews, explain where feedback agreed or differed. Connect each proposed change to an actual observation.
Finding from interviews	Planned revision	How it should help
		
		
		


Sources and acknowledgements
The datasets originated in CMU’s Student IronViz competition. The organizers confirmed that they may be reused and shared publicly.
- Dataset 1
- Dataset 2
The bar chart, hourly charts, and combined dashboard were originally developed for my individual IronViz submission. My class project builds on that work through an expanded narrative, clearer definitions, additional context, and user research.
AI acknowledgement
I used ChatGPT to help interpret assignment feedback, organize the storyboard and interview protocol, and draft text that I reviewed and adapted. ChatGPT also generated the proposed monthly overview wireframe in Part I. Interview findings and quotations will come from the individuals I interview.
