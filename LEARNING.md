# Lesson 01 · Conversation evidence

AI-drafted task summary, not a transcript or grade. It may be public. Use actual
short quotes or labeled paraphrases, name any help supplied, and link actual
work. Leave missing contributions Pending. A learner can review, correct or
remove excerpts before publication; accuracy approval is not proof of learning.
Label role-play honestly rather than treating it as an actual learner response.

**Lesson:** STUDIO-001. **Available conversation context:** October 27, 2026 setup and deployment conversation. The learner reviewed the summary and approved its inclusion in the public repository on October 27, 2026.

## Prediction

Learner quote: “first dns gives the ip, then traefik handles the https request, then it loads the page”.

AI help: added that Traefik uses the hostname to route to the calculator container, which returns the page through Traefik.

## Check interpretation

Learner quote: “I think it confirms that the live API is reachable and correctly handles that specific multiplication request. It doesn’t prove every calculation works, invalid inputs are handled properly, the interface works end to end, or the app is secure and reliable under load.”

Context: AI presented the actual 6 × 7 API check, its expected result of 42, and the observed HTTP 200/result 42, then asked what it establishes and leaves open.

## Browser observation

Classroom example only: the learner reported entering 6 and 9, choosing divide, and seeing `0.6666666667`. AI explained that this is 6 ÷ 9 rounded to ten decimal places.

At https://calc.lwdgyasteri.com, after being asked to try 6 × 7, the learner reported: “both the browser result and api result show 42 and it says results match”. This is separate from the AI's earlier browser check.

## Keep decision

Learner quote: “I would keep it because both the browser and API showed 42 and the results matched.”

## Review

Learner approval on October 27, 2026: “yes that looks accurate, you can include it in the public repo.” Approval covers the summary reviewed in this conversation; it establishes record accuracy, not a separate assessment of understanding.

## AI work and next step

AI cloned the learner's repository, read the lesson, prepared Python 3.12 tools and Chromium, inspected the existing server read-only, and drafted a file-provider routing adaptation. The learner added calculator DNS in GoDaddy, chose the hostname, and explicitly approved setup and deployment. Local prepared checks passed: Black, Pylint, 91 unit/integration tests and 2 Docker/Chromium E2E tests. These checks alone do not establish the public deployment or learner understanding.

GitHub SSH authentication now works. The lesson [issue #1](https://github.com/Y-Just-Y/373_hosting_dfp/issues/1) records the approved scope after deployment. Public deployment evidence belongs in SPEC and the sanitized report. The learner has now supplied the check interpretation, own-site observation and keep decision above. The summary is approved for publication. Next: complete the PR/CI/merge workflow; see SPEC for current GitHub evidence. Deployment evidence: [SPEC](SPEC.md), [sanitized report](studio/evidence.json), and [additional checks](studio/deployment-plan/additional-evidence.json).
