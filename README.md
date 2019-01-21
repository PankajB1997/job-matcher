## Submitted to NUS Hack-N-Roll 2019 (Group DL)

## Student Codes
1. Pankaj Bhootra - 0324
2. Aadit Kamat - 0294
3. Latane Bullock - 0552

## Inspiration
A lot of university students face difficulties finding the right job for a career. This tool takes in your professional experience and extracts keywords relevant to your previous experience and skill set, which are then matched to online job listings on various job portals. 

## What it does
The current prototype takes in a linkedin generated pdf document summarizing your profile (linkedin resume) as input and parses it to extract keywords such as your top skills and previous job titles. It then runs a keyword matching algorithm against various job listings posted on Indeed (only jobs posted in last 7 days are considered) and ranks the job results according to frequency of occurrence of keywords. This list of job results are displayed in ordered tabular format with a link to the job portal for each job where the candidate may submit their job application!

## How we built it
We used React for front-end and Flask for back-end, along with other libraries to help us retrieve job postings and parse the candidate's resume file. We coded up methods to perform tasks such as keyword extraction from candidate profile and keyword matching against job listings.

## Challenges we ran into
1. Most of the open-source APIs we initially tried to use for various essential functions (such as converting pdf to text) where found to be broken. So, we had to take the best available option and modify their code to meet our requirement.
2. We spent a lot of time trying to setup a LinkedIn authentication service on our app, with the intention that we would be able to scrape information directly from the user's LinkedIn profile upon logging in. However, we ran into several access issues as LinkedIn has recently severely limited access to its full_profile APIs and it also blocks any scrapers from making unauthenticated requests. In the end, we decided to parse resume file directly instead of retrieving the user's LinkedIn profile.

## Accomplishments that we're proud of
1. We managed to learn several intricacies of web development and information retrieval.
2. We successfully developed a Sign In with LinkedIn option on our web app, which gave us knowledge of how to develop a web login system using login from services like Google, Facebook, etc.

## What we learned
We learnt how to develop web apps using React and Flask, both of which turned out to be powerful yet simple services to use within the time constraints of a Hackathon. The best part about the team was our patience in dealing with several frustrating issues that came along the way, such as developing a Sign In with LinkedIn feature successfully and then scrapping it later due to LinkedIn API's limited access privileges. It was also a sobering experience to experiment with various open source APIs for our various essential functions, just to find that most of them are broken and not actively maintained. This taught us how open source tools come with various caveats and it is important to do previous homework on them and make well-informed decisions taking into account the pros and cons of what's available.

## What's next for Job Matcher - Matching your profiles to job listings!
1. Add more custom filters to provide users with more flexibility in only getting job recommendations that match certain criteria (such as job location or job type such as Internship or full time jobs).
2. Recommend jobs from more portals other than Indeed, such as Monster or LinkedIn.
3. Another challenging improvement would be to use a deep learning technique to match jobs to resumes rather than using the currently implemented keyword matching approach, in order to provide even better recommendations.
