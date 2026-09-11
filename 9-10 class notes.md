# 9-10 Class Notes — Overwatch

CSC 131 Computer Software Engineering, Section 8. Sacramento State, Fall 2026. Instructor Ahmed Salem.

## Team

- **Josh Lemos** — Project manager (joshualemos@csus.edu) *(Lead)*
- **Mohd Mahmodi** — Tech lead, infrastructure (mohdmahmodi@csus.edu)
- **Connor McKelvey** — Frontend (cmckelvey@csus.edu)
- **Ali Farooq** — Backend / Integration (alifarooq@csus.edu)
- **Ryan Sharma** — Backend Logic (rsharma3@csus.edu)
- **Parker Luu** — Frontend (UI/UX) (pluu@csus.edu)

## Client lecture — September 10, 2026, 12:00 PM

Zoom session with the Sac State Office of Energy and Sustainability. Laura Gonzalez manages the campus waste hauling account and answered most questions. Ryan Todd, Director of Energy and Sustainability, joined about 30 minutes late. Josh Maddox from Sac State also joined.

### The project

From the professor's email: Develop a waste collection survey and dashboard using Smartsheet. The system will allow drivers to document each pickup by submitting a photograph, bin fullness level, date, time, location, and driver information. The dashboard will organize and visualize the data to identify collection patterns, improve pickup schedules, reduce unnecessary trips, and make waste hauling more efficient. Students can use platforms such as Zabble as a model.

### About the client office (Laura intro)

- **Laura Gonzalez** is Waste and Sustainability Analyst at the Office of Sustainability (facilities / operations side, not teaching).
- Small team: about 3 full-time staff, 2 recyclers, plus interns, volunteers, and College Corps Fellows. Ambitious goals, limited budget.
- Campus is about 300 acres with 60+ buildings.
- **Zero waste by 2030** (presidential goal from 2018): divert 90%+ of waste from landfill.
- **Carbon neutral by 2040** (about 5 years ahead of California).
- Must follow state, CSU Chancellor Office, and some federal rules. **SB 1383** drives organic waste / compost collection, color-coded bins and signage, rising recovery targets since 2022, and edible-food recovery work with cafeterias.
- Commercial inspiration is Zabble (too expensive). CSUN students built a Smartsheet + dashboard version that inspired this project.

### What the client told us

- **The biggest problem is no data.** Laura cannot tell whether a driver showed up, whether the bin was full, or how much was taken. Nobody checks the bins after pickup.
- **The most important field is fullness at the time of service,** captured before the bin is emptied.
- **The users are the sustainability team, mostly Laura.** Drivers only fill out the survey. Custodians are not users.
- **Two fees per stop.** A fee for the truck to come to campus plus a weight fee. An empty bin still costs the visit fee.
- **Target is service at about 80% full.** Below that wastes fees. Overflowing bins are refused by the driver and need a paid return trip.
- **Around 100 dumpsters** across roughly 57 to 63 buildings. Each building has at least one bin per waste stream: landfill, recycling, organics. Sequoia Hall has 4 landfill, 3 recycling, and 4 organics carts. The University Union has the most.
- **Most academic buildings are serviced Monday, Wednesday, Friday.** Other buildings have their own schedules. No weekend service.
- **Bins already have hauler names.** Example: Modoc Hall shares a compactor with Napa Hall, coded roughly as Napa Modoc Compactor. We use their names from the master list.
- **Container types vary.** Regular dumpsters, compactors at the library, and organics carts. The library compactors come back a quarter full every two weeks and are still paid for.
- **Truck scales have been broken for years.** The hauler sends estimates. The public Power BI dashboard shows the same tonnage for most buildings every month.
- **Drivers already carry iPads** and log visits in their company system. The company told Laura they are fine using a better system if she has one.
- **One survey for the whole class.** Laura agreed it would be better if drivers only fill out one form.
- **Smartsheet is suggested, not required.** It works offline and the CSU already has a membership. Laura said twice she is not tied to it.
- **The survey keeps running after the class ends.** The dashboard is the tool to visualize it.
- **The hauling contract is going to bid** for a new five year term. Real service data would help the negotiation.
- **Color coded liners.** Recycling bags should be blue. A clear or green bag in recycling is contamination. Laura wants an AI check on photos eventually.
- **Known trouble spot.** The athletic center always has extra waste in, around, and next to the dumpsters, even after more service and bigger bins.
- **On-call service is separate.** Big projects like the theater department's spring cleanout get a dumpster serviced only on requested dates.
- **Reporting.** The department reports annually to the State of California and the CSU system and has zero waste goals.
- **Laura will send:** the master dumpster list with locations, map, and codes; the master service schedule; invoices from August and September onward; the survey template from the other campus; and access to survey responses for the teams.
- **Missed pickup alerts.** When asked if she would want them, Laura said that would be amazing.

### Contact

**Email**

[sustainability@csus.edu](mailto:sustainability@csus.edu?subject=CSC%20131%20Overwatch). Put CSC 131 in the subject line. Laura disconnected her phone because of complaint calls, so email is the fastest way to reach her.

**In person**

Email to schedule about a week ahead. Their office is in Modoc Hall. Dropping in is unlikely to work.

**Website**

[csus.edu sustainability](https://www.csus.edu/experience/innovation-creativity/sustainability/)

**Public dashboard**

[Power BI report](https://app.powerbi.com/view?r=eyJrIjoiNTNlZDc5MmUtZDFiZC00MzFmLTg5NDYtNTdlNmI0ZjA0YzZlIiwidCI6ImI2YjQ5MDAxLThiM2YtNDNmYS05OWExLTcwNmU4YzdlMzU5OCIsImMiOjZ9&pageName=ReportSection)

**CSUN example**

[csun-zero-waste.replit.app](https://csun-zero-waste.replit.app/). A dashboard hosted on Replit that reads live Smartsheet data.

## Questions and answers

Every question asked during the meeting and how the client answered. Grouped by topic.

### Survey questions and timing

*12:18 PM, Ahmed Salem*

**Q:** Would you like to see what the teams come up with for survey questions?

**Laura:** Yes. Start with the basics: day, time, location, and fullness based on a picture. If you have other suggestions, now is the time to add them.

*12:18 PM, Ahmed Salem*

**Q:** How soon do you need the survey back?

**Laura:** As soon as we get it. The sooner, the easier it is for you to have data to work with.

### Dumpster locations, sensors, and naming

*12:19 PM, Kyle*

**Q:** Will we know the dumpster locations? Will there be sensors, or do students or drivers check fullness?

**Laura:** Either way. If you want your own route I can provide the locations. I have a master list and a map. No sensors right now. We are exploring them but they are very expensive. Drivers are easier because they already do weekly routes. You are welcome to collect your own.

*12:20 PM, Kyle*

**Q:** Do drivers visit in a set order, or could we compute the best order?

**Laura:** I have a master schedule. I believe they go every day. But I have no data proving they follow the route. That is part of the problem: making sure service matches the contract and every location is taken care of.

*12:20 PM, Nick Salamy*

**Q:** Can you share the list of dumpster locations?

**Laura:** Yes.

*12:20 PM, Raji Sahansra*

**Q:** Is there a naming convention drivers recognize, or do we make our own?

**Laura:** They already have names. Modoc Hall has a recycling dumpster, a compost cart, and shares a compactor with Napa Hall. The driver code is something like Napa Modoc Compactor for trash. The master list has the location and name for every building.

*12:26 PM, Zainab Mahyar*

**Q:** Do you have the exact number of dumpsters on campus?

**Laura:** It is in the master service list I will provide. Not off the top of my head.

*12:39 PM, Kyle*

**Q:** Ballpark, hundreds or thousands of bins?

**Laura:** Around 100. About 57 to 63 buildings depending on which you count. Each has at least three bins, one per waste stream. Some larger buildings have several per stream.

*1:00 PM, Zainab Mahyar*

**Q:** How far are the dumpsters from each other? What is the max per building?

**Laura:** Almost every building has its own. A few share, like Lassen Hall and Kadema Hall, with enclosures between the buildings. The University Union has the most and they are very large. On the academic side Sequoia Hall is largest with 4 landfill, 3 recycling, and 4 organics carts.

*1:00 PM, Nick Salamy*

**Q:** Is all of that in the master sheet?

**Laura:** Yes. I will also check with the hauler so my list matches theirs and give you the most current version.

### Cost, how the hauler is paid, and the contract

*12:21 PM, Brian Peart*

**Q:** Will you give us cost data per visit, or do we research it?

**Laura:** I have the invoices and manage the account. I can provide what is paid, for example August and September. If the project starts at the end of September we can compare later in the semester and see how changes affect cost.

*12:24 PM, Zainab Mahyar*

**Q:** Are collectors paid by the hour, or by whether they collect?

**Laura:** By service and by fullness, meaning weight. We pay a fee just for them to come to campus, then a weight fee on top. Empty or a quarter full, we still pay the visit fee.

*12:24 PM, Zainab Mahyar*

**Q:** So they check every bin, you do not know if it is full, and you still pay?

**Laura:** Yes, that is it.

*12:30 PM, Jared*

**Q:** Do you have a target number for savings?

**Laura:** No. We are going into a bid process to renew the service contract, so actual cost versus what we pay will be very beneficial. The new contract runs five years.

*12:45 PM, Joshua Risley*

**Q:** Do the invoices already say how much waste is in each bin?

**Laura:** No. The trucks used to have scales and I had exact weights. The scales have not worked for years, so I get estimates and use them for our public dashboard. It is obvious it is not real data because most buildings show the same amount every month.

*12:47 PM, Jared*

**Q:** Is there a maximum time before a bin must be dumped even if not full?

**Laura:** No maximum. It is most efficient at about 80% full. Overflowing, the driver will not take it because things can fly out while lifting. Below, we still pay service and weight fees. At 80% it is the same every time.

*12:57 PM, Zainab Mahyar*

**Q:** Would it cost less to hire more custodians or rely on drivers?

**Laura:** Two different accounts. Custodians are campus employees with many other tasks. Their staffing does not change how full a dumpster gets. That depends on the building's occupants and whether drivers come on time. The campus pays the hauler to take waste to recycling, compost, or landfill. This project is about the hauler contract, not custodial hiring.

### Smartsheet and how data reaches us

*12:23 PM, Brian Peart*

**Q:** You mentioned a specific website we had to use. Slipstream?

**Laura:** No. I showed an example another group built at a different CSU. They use Smartsheet because it takes submissions without Wi-Fi or cell service, which is easier for the driver. I am not limiting you to it. It inspired this project. The CSU system has a Smartsheet membership, so it is cost friendly for students.

*12:29 PM, Brian Peart*

**Q:** So we write the questions, use the offline tool you showed, and that is cost effective?

**Laura:** Correct.

*12:29 PM, Brian Peart*

**Q:** Does the data go to you first, or do we get it immediately?

**Laura:** We can discuss. I think we can add the teams as data users so you have access immediately instead of going through me. I need to check how many people the survey tool allows to view responses.

*12:40 PM, Alexander Hartigan*

**Q:** Are all teams sharing the same survey data, or does each collect its own?

**Laura:** Up to you. One survey for the whole class, or your own resources like photographing dumpsters yourselves.

*12:40 PM, Alexander Hartigan*

**Q:** If a driver had to take three surveys from different teams, that would get annoying.

**Laura:** Yes. It would be beneficial if it is just one.

*12:42 PM, Alexander Hartigan*

**Q:** With one survey, is the data real time?

**Laura:** Ideally you have access as it comes in. We can create the survey so everyone gets the data. That is why I am asking for the questions you want for the first sprint, so we can put it together and start collecting.

*1:08 PM, Austin Young*

**Q:** If the class uses one universal survey, is each team's job analysis and visualization rather than collection?

**Ryan Todd:** Yes. If the core survey is the same, the data is the same. How you present it is what changes.

**Laura:** That can be a solution, but I do not want to limit the class. If you want to build new software with intake and results in one platform, that is up to you. That would be a different tool for the future.

**Ryan Todd:** Look at the end goal, not how you get there. We have a problem to solve and a potential solution, but that does not mean it is the way you have to do it, as long as the end product meets the need.

### What goes in the survey

*12:24 PM, Nick Salamy*

**Q:** We are looking at the big dumpsters a truck picks up, not small receptacles?

**Laura:** Yes.

*12:25 PM, Nick Salamy*

**Q:** So drivers update pictures or a template showing fullness on a daily or route basis?

**Laura:** Yes. A survey with date, time, maybe a picture of fullness, some questions, and we use that data for the dashboard.

*12:26 PM, Sam Yohanes*

**Q:** What are the non-negotiables for the data?

**Laura:** Any data is better than nothing, which is what we have. We are very open and I want you to use your creativity. The most critical thing is fullness at service, so we can adjust service and save cost.

*12:38 PM, Erika H*

**Q:** Does the survey cover past semesters or just this fall?

**Laura:** The survey should keep being used independently of the project. The point of this project is a tool to visualize that data, past this fall.

*12:45 PM, Jarim*

**Q:** Should the survey capture the bin before or after emptying?

**Laura:** Before, so we know how full it is. The company sends a separate volume based report. With before data we can compare and check it is similar.

*12:55 PM, Nick Salamy*

**Q:** How do we make sure the driver fills it out every time?

**Laura:** I already talked to the company. They said they are fine giving that information, so if we have a better system we can ask them to use it. They already carry iPads. It will not affect what they are doing.

### Project flow and Sprint 1

*12:27 PM, Brian Peart*

**Q:** Create a survey for the drivers, collect for two weeks, then build from the data. Is that right?

**Laura:** Yes. Two weeks, a month, or as long as you need for enough data.

*12:27 PM, Joshua Lemos*

**Q:** What needs to work for Sprint 1 to be a success on September 24?

**Laura:** If we get the survey done by then, with the questions you want to see. That is the most important and critical part so we can start collecting as soon as possible.

*12:28 PM, Ahmed Salem*

**Q:** Is the survey already drafted?

**Laura:** I have a version from a different campus we can use, and we are open to adding questions. I requested access this morning and do not have it yet, so I cannot share it on screen.

*12:29 PM, Ahmed Salem*

**Q:** Once the survey goes out, when do responses come back?

**Laura:** Drivers are on campus every day, so immediately once they have access.

*1:02 PM, Brian Peart*

**Q:** Sprint 1 is the survey, and the whole class works on one survey?

**Ahmed Salem:** Each team holds its own sprint planning session and decides its tasks. Sprint 1 is two weeks, today through September 24. I do not assign tasks. The team is self organized, self disciplined, and cross functional. The survey could be one item in the sprint, not the whole two weeks. At the end each team demos with the clients present, gets feedback, holds a retrospective on attendance, participation, task allocation, and the work, then plans Sprint 2.

*1:05 PM, Brian Peart*

**Q:** So you want more than the survey in Sprint 1, even though we need the data first? Programming, or designing?

**Ahmed Salem:** That is how industry works. The team lead decides what is reasonable for two weeks. The survey alone may not fill it. We only have until about December 9. Each team has five to seven people. Coding is up to you, but definitely design, and maybe some coding. Sprint 1 is not the end. You will see what other teams did and can pivot in Sprint 2.

*1:16 PM, Brian Peart*

**Q:** The Deliverable 1 link only asks for names and emails, but the doc asks for a cover page. Which do we submit?

**Ahmed Salem:** The full report with the cover page. The placeholder in the link was a misunderstanding and the TA will correct it.

*1:20 PM, Aqila Nasiry*

**Q:** Is the team selection deliverable due tonight?

**Ahmed Salem:** Yes, tonight by midnight.

### Users, purpose, and scope

*12:35 PM, Parker*

**Q:** Are we making a financial tool to optimize how much money goes into this?

**Laura:** We are trying to be more efficient. Efficiency leads to cost savings, hopefully.

*12:35 PM, Parker*

**Q:** Who are the users? You and your team, or someone else?

**Laura:** Our team, mostly me, to track what happens on campus. It could also be a partnership with the hauler to make sure they do what the contract says. Showing up to an empty bin wastes their time too. Beyond savings, it helps us understand what is happening and decide. If recycling or compost bins are always full, we increase their size. We want landfill numbers to go down. We have zero waste and compliance goals and report annually to the State of California, the CSU system, and two other entities.

*12:37 PM, Parker*

**Q:** Can the scope go beyond a financial tool? Can we do more?

**Laura:** Yes. I have a second project idea: AI waste contamination detection. When the driver takes the picture, detect contamination by material or by liner color. All bags in a recycling dumpster should be blue. A clear or green bag is contamination. That helps us train custodians and keep the streams clean.

*12:31 PM, George Tsetsegmaa*

**Q:** Are we hard set on surveys, or can we try cameras with vision?

**Laura:** I would love that. Not hard set. I was going for a simple version, but sensors or cameras are welcome.

*1:23 PM, Sam Yohanes*

**Q:** What is the biggest problem right now?

**Laura:** We do not have any data showing the services on campus. It is very hard to make decisions and changes without knowing what is going on.

*1:23 PM, Zainab Mahyar*

**Q:** So the first priority is the data, then we expand into missed pickups, scheduling, and savings?

**Laura:** Yes. And later maybe a contamination tool with AI or another approach. Keep expanding a software based product that shows what the company is doing and where the campus disposes its waste.

### Current service, missed pickups, and complaints

*12:32 PM, Zainab Mahyar*

**Q:** Is one main issue not knowing whether drivers pick up the right or full ones?

**Laura:** Right now I cannot say whether the library dumpster serviced today was full. We still get charged. I do not know if they showed up, if the route was completed, or how much was taken.

*12:33 PM, Aqila Nasiry*

**Q:** If dumpsters are not full, do you want drivers to skip them?

**Laura:** They still go, but if a bin is consistently not full, instead of every other day they can come once a week and save money. Yes, we would pay less.

*12:33 PM, Stein Clinten*

**Q:** How many days a week do they come now?

**Laura:** Most academic buildings three times a week: Monday, Wednesday, Friday. Other buildings have different schedules. The library has compactors, so it should need less service, but the data says it is a quarter full every time and we pay every two weeks when it could be once a month. I will share the master schedule with every building's days and times.

*12:43 PM, Sam Yohanes and Parker*

**Q:** Are there more complaints in certain areas?

**Laura:** Yes. The athletic center always has extra waste inside, around, and next to the dumpsters. We increased service and dumpster size and still have the same issue. Data could prove whether it is user error and training is needed, custodian error, or the company not servicing as much as we think. That is one building. There is always something happening on campus.

*12:41 PM, Zainab Mahyar*

**Q:** Is there an intermediate step from small trash cans to dumpsters, and do you pay for that?

**Laura:** Yes. Another class is working on the small trash cans, so we will have both. Everything from the small cans ends up in the dumpsters.

*12:48 PM, Zainab Mahyar*

**Q:** What happens when a bin is overflowing and the driver refuses it?

**Laura:** One of our two campus recyclers takes material out so the driver can pick it up, or uses heavy equipment to push the load down. If the driver left it, we pay for them to come back.

*12:49 PM, Sam Yohanes*

**Q:** If a bin is full and you get complaints, what do you prioritize?

**Laura:** Depends on the complaint. Waste always smells. Unserviced food waste gets an extra service immediately for safety. Regular dumpsters are serviced three times a week, so a Tuesday call is emptied Wednesday. A Friday night call waits until Monday because the hauler does not work weekends. This is why the dashboard matters: I could see the last pickup was Monday when they were supposed to come Wednesday, and push back when they try to charge me.

*12:51 PM, Nick Salamy*

**Q:** Would you like alerts on the dashboard when a pickup is missed?

**Laura:** Oh yes, that would be amazing.

*12:51 PM, Joshua Risley*

**Q:** How flexible is the schedule? Early pickups when near full, or canceled when empty?

**Laura:** Yes. Academic buildings and offices have regular schedules that can change in summer and breaks, though some buildings still hold summer classes. There is also on-call service for large projects. The theater department gets an on-call dumpster every spring and it is serviced only on the dates needed.

*12:59 PM, Sam Yohanes*

**Q:** Is anyone checking that bins were actually emptied?

**Laura:** No. I sometimes drive around and take pictures so I can call the company, but nobody checks daily. That would waste labor when sensors, cameras, or just knowing the services could tell us.

*1:00 PM, Zainab Mahyar*

**Q:** When an issue comes up, do you contact drivers directly or the company?

**Laura:** Both. Drivers and the company call me all day, and I call our account manager or customer service. But I am not on campus 24 hours. A 3 AM pickup issue waits until I wake up.

*1:19 PM, Sam Yohanes*

**Q:** How do you account for missed bins today?

**Laura:** We do not. I drive around, the recyclers on their route call me, campus customers call Facilities Management and requests reach me, and custodians report when something has been overflowing for more than three days. Eventually it reaches me and I call the company. There is no efficient way to track daily.

### Custodians

*12:53 PM, Zainab Mahyar*

**Q:** Could the people who move trash from small cans to dumpsters report when the big one is full?

**Laura:** Honest answer: very large campus, not enough custodians, especially the last year and a half. Three shifts, campus split into zones, different groups on different days, always rushing. That is why drivers are the easier source. They already log visits in their company's system, which I do not receive.

*12:56 PM, Alexander Hartigan*

**Q:** Could custodians send an alert only when a dumpster is around 75% full?

**Laura:** We can try to work with the leads and ask the director in charge if his team will do a trial. They do floors, bathrooms, and everything else, not just trash. I will take that note. That is a realistic goal.

### Budget, sensors, and cameras

*1:12 PM, Kyle*

**Q:** Is there any budget? Sensors are expensive but worth it long term.

**Laura:** We will absolutely look at that, especially if savings cover the cost. Without consulting my team: if you want a pilot, there is a student sustainability fund on the Sac State Sustainability website under the student involvement tab. It is small, so not 100 sensors, but maybe one to test. You apply, we interview the team, then decide. Fill out the form and meet with us before buying anything. We cannot reimburse. We can only purchase for you.

**Ryan Todd:** If the final solution needs a sensor on every bin, use common sense. $10,000 per sensor will not work. Around $50 might. A purchase is not out of the question for this project.

*1:21 PM, Zainab Mahyar*

**Q:** Could we use existing campus cameras to watch the dumpsters?

**Ryan Todd:** No. Those are police and campus security cameras. Completely different use case, they would not alter them, and our team has no clearance to access them. It would be a waste of time to ask.

### Reaching the client

*12:48 PM, Mohd Mahmodi*

**Q:** Can you share the link to the waste dashboard in the chat?

**Laura:** It is public on the sustainability website and someone already shared it. I cannot share it right now.

*1:17 PM, Yousef Khalaf*

**Q:** How do we contact Laura with questions?

**Laura:** I added the email to the chat. Put the class in the subject line so I can respond as soon as possible. There is a lot of information on the website too.

*1:18 PM, Joshua Lemos*

**Q:** Is email the fastest contact, or can we call?

**Laura:** I disconnected my phone because of complaints, so email is fastest. For in person, I can send times. I am on campus all week, and someone else on the team can help if I am not.

**Ryan Todd:** We can meet, but we are not always in the office. We need about a week to get it on the schedule. Showing up at Modoc Hall unannounced probably will not work. Email to coordinate and we can give availability for one to three of us.

*After students left*

## Professor + client follow-up

Short conversation after class between Ahmed Salem, Laura Gonzalez, Ryan Todd, and Josh Maddox.

- Students keep asking for the "bare minimum." Salem asked clients to expand the project description into clearer **features / functions / requirements** (even beyond what teams can fully finish), then narrow across sprints.
- Purpose: reduce confusion, create a scoring/rubric basis, and hold teams accountable to client needs.
- Ryan agreed this helps compare teams on functions. Target: get the expanded list to the professor by **Monday** (before Tuesday class), ideally for both related projects.

*During the call*

## Discord notes

What the team wrote in the server while the meeting was running.

- **12:11 PM** **Connor** — Posted an image of the example the client showed.
- **12:18 PM** **Josh** — Suggestion: survey creation for the data input by trash drivers. The group has no sensors.
- **12:20 PM** **Connor** — Data is reported by drivers on dumpster runs, goes to the sustainability department, then to us for processing and display. If we have survey question ideas, give them to the client.
- **12:23 PM** **Josh** — Laura can provide campus invoices.
- **12:27 PM** **Connor** — Main goal is reducing driver costs. Drivers are paid even for mostly empty dumpsters. Sending them to bins that are frequently full is more cost efficient, and our data can calculate that.
- **12:28 PM** **Connor** — Surveys may go directly to us through Smartsheet so we use the data directly.
- **12:28 PM** **Josh** — Collectors are paid by service and fullness. There is still a fee for visiting an empty bin. Most important: fullness at each location and its implications. The survey is the basic first requirement of Sprint 1 and should be collected continuously. No route info is presented during visits. The library has compactors so bins are less full there.
- **12:36 PM** **Josh** — The sustainability team is the user, not the drivers. Optional second feature: AI that scans trash photos for contamination.
- **12:48 PM** **Josh** — 80% fullness means schedule a pickup. Posted the Power BI link. Notification for the sustainability team when a pickup is missed. On-call dumpster service is separate.
- **12:49 PM** **Mohd** — Posted the Power BI link.
- **1:00 PM** **Josh** — Currently no person or technology checks the trash after pickup.
- **1:18 PM** **Connor** — Client contact is sustainability@csus.edu. Put the class in the subject line. Schedule in person meetings about a week ahead. Drop-ins are unlikely to work. Posted the CSUN Waste Hauling Dashboard link.
