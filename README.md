# One source → six B2B content drafts

A small, local content-repurposing helper: prepare a source-grounded AI prompt, then package the response into a reviewable text file. No API key, paid service or account access is built into the script. Python 3 and the standard library are enough.

**Need this done for you?** I offer an AI-assisted [B2B repurposing pilot on Fiverr](https://www.fiverr.com/fghjhbcv/repurpose-b2b-content-into-linkedin-posts-emails-and-video-scripts): **$50**, three LinkedIn posts, one email draft and two short-video scripts, three-day delivery after complete requirements, one consolidated revision. Up to 2,000 source words and 1,000 delivery words total. I operate this service; this repository is a demonstration and a free starting point, not a customer-results case study.

## A concrete before and after

**Fictional original source:** A weekly handoff note can include the task, owner, next action and due date. If the work is unclear, have a conversation first.

**LinkedIn draft:** Your handoff note needs a named owner and an explicit next action. If the task is unclear, talk before sharing it.

The value is editorial selection and source checking. The script does not establish that any generated claim is true.

## Try it locally

```sh
python3 pipeline.py prepare sample-source.txt --out demo
```

Open `demo/prompt.txt` in your existing AI chat and save its JSON-only reply as `demo/response.json`. This AI step is manual; available usage depends on the chat account. Use only content you own or are authorized to process, and remove confidential or personal information first.

To try packaging without any AI service, use the included fictional response:

```sh
python3 pipeline.py pack sample-response.json --out demo
```

Open `demo/delivery-draft.txt`. The output includes three LinkedIn drafts, one newsletter/email draft and two video scripts, with source references for review.

## The review that makes the draft useful

1. Compare each claim against the original. A real source ID can still be attached to an unsupported claim.
2. Remove invented outcomes, numbers and testimonials.
3. Give each post a distinct point; do not repeat the same opening six times.
4. Check audience, terminology, voice and the call to action.
5. Have the content owner approve it before publishing.

Included sample files are fictional demonstrations written for this project. They are not paid client work or evidence of engagement, time saved or revenue.

## What the helper validates

It checks JSON structure and the presence of text and source references. It does **not** verify factual accuracy, tone, originality or source-ID correctness. It never posts to accounts, sends messages or delivers orders.

## If you prefer a finished pack

[View the Fiverr service and send your brief](https://www.fiverr.com/fghjhbcv/repurpose-b2b-content-into-linkedin-posts-emails-and-video-scripts).

AI assists the drafting and editing workflow. The service is written content only: video production, design, account management and automatic publishing are excluded. No traffic or revenue results are promised. All service orders, payment and delivery stay on Fiverr.
