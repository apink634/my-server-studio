# Lesson 01 · Conversation evidence

AI-drafted task summary, not a transcript or grade. It may be public. Use actual
short quotes or labeled paraphrases, name any help supplied, and link actual
work. Leave missing contributions Pending. A learner can review, correct or
remove excerpts before publication; accuracy approval is not proof of learning.
Label role-play honestly rather than treating it as an actual learner response.

## 

## \*\*Lesson:\*\* STUDIO-001. \*\*Available conversation context:\*\* Notes from my working session with an AI coach (Claude). Quotes are my own words from my notes, with typos fixed.

## 

## \## Prediction

## 

## Written before I ran the checks (Nov 5, 2026):

## 

## 1\. /health: "The /health link would lead to a version of the site that shows the page status."

## 2\. 6 x 7: "The calculator would return 42."

## 3\. My existing sites while the calculator is deployed: "I'm not sure about this one but maybe the site would say it is busy? or there would be an error? or it would reorganise the info." After a hint from the coach: "Maybe nothing would happen then."

## 4\. How a request reaches the calculator: "My prediction is that the request is sent to the calculator through the server."

## 

## Did my predictions match, and why? 

My predictions were a little off. I did not fully understand how the request reached the calculator and I learned that the containers matter. My prediction for #2 was correct and the /health prediction was also right.

## 

## \## Check interpretation

## 

## I entered 6 and 7 and expected 42. I got 42. In my words: "the result shows that the calculator is working correctly."

## 

## After the coach explained the Traefik Host-rule label, I corrected prediction 4: "so traefik looks at the host name and decides which container is appropriate"

## 

## I compared my calculator with my professor's at calc.mywebclass.org: "it is almost the same calculator. this one is built by my professor. the only difference is that his has a different domain name." Later: "the professors calculator is similar"

## 

## \## Browser observation

## 

## /health: "it gave me the status of my page along with other things that i don't understand. im surprised its in such a basic single string format, although i dont know what else i was expecting"

## 6 x 7: "it gave me 42, as expected"

## My other sites: "yay they work"

## Padlock: "I didn't see a padlock at first, but it was because I had to click on the page settings icon to see it"

## 

## \## Keep decision

## 

## Keep it as it is. In my words: "I would keep the calculator the way it is since it is understandable and serves its purpose"

## Earlier, I chose to adopt the already-running calculator instead of replacing it: "i would adopt the existing calculator because it is less risky since there are fewer steps"

## 

## \## Review

## 

## Pending. I will read this file once more before publishing and correct anything that is not accurate.

## 

## \## AI work and next step

## 

## The AI coach explained terms when I asked (/health, what a request is, the Traefik Host rule, what `doctor` does, adopt vs replace), told me which commands to run and read my output, and drafted the wording of issue #1 and the SPEC.md edits, which I read and pasted. It also supplied the script I used to rebuild my server after I deleted the original droplet by mistake. I wrote my own predictions, observations and decisions.

## Not run: full local E2E (no local Docker). Pylint and pytest fail on my Windows laptop because of Linux-only functions; the GitHub CI result is pending.

