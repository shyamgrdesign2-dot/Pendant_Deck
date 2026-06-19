# Tatva Pendant

*A one-pager for the next presentation. Source notes, not the final deck.*

---

## What we noticed after launching

The IP shipped, and the product worked. The thing that kept showing up in the actual flow was a quiet dependency on hardware. In a lot of hospitals, the **computer on wheels** either isn't great or isn't there. A **doctor or a nurse holding an iPad** through a patient conversation looks fascinating, and you watch their attention split between the patient and the screen. None of this is a blocker. It works. The honest question we started asking was simpler:

> *It works. What if we could make it even easier, faster, and more in the flow?*

That single question is what Tatva Pendant is built around.

---

## What we built

The pendant is the smallest part of the story. The IP is the layer between the ambient audio and the EMR, and it's all software we own.

- **Capture.** Ambient audio off any clean microphone. The pendant is what we use today; anything cleaner can replace it tomorrow without rewriting a line of the rest.
- **Understand.** An in-house ASR pipeline trained on clinical audio. It handles accents, abbreviations, drug names, and the way clinicians actually talk to each other.
- **Resolve.** A context engine that knows the clinician, the time of day, the schedule, the patient roster, and the ward/bed map. Encounters get identified, not guessed.
- **Structure.** Conversations get chunked into clinical sections — OPD encounter, IPD round, observations, plan, vitals — automatically mapped to the EMR's fields.
- **Write.** The structured note lands inside the existing EMR. The clinician reviews it, edits if needed, and saves and prints from the same screen they already use.

The clinician never opens a second app. Nobody re-types anything. The conversation does the work.

---

## One pipeline, every clinician

The system doesn't care which role you play. It identifies the clinician, the encounter, and the right destination in the EMR.

- **Doctor.** OPD consult or IPD round. The encounter is resolved against the schedule, the bed map, and the patient name. The note lands on the active episode.
- **Nurse.** Intake, observations, bedside checks. Nursing entries are routed to the right admission, ready for the next clinician on shift.
- **Bedside team.** Rounds, handovers, post-procedure debriefs. Multi-speaker captures are attributed correctly and chunked into the right sections of the inpatient record.
- **Anyone, really.** Wherever a clinician speaks and an EMR field needs filling, the same in-house stack closes the loop.

The clinician doesn't think about OPD versus IPD — that is the system's job.

---

## A point we want to be explicit about

**The pendant is just a model. It is not the product.**

We are not married to this specific piece of hardware. It happens to be a clean, unobtrusive way to capture ambient audio at the bedside, and that's why we picked it for the first cut. Everything that gives the product its value — the ASR pipeline, the context engine, the chunker, the EMR integration, the clinician-facing UX — is built in-house and lives independently of the device.

If a better capture device walks in tomorrow — a sharper lapel mic, a different pendant, a phone in a coat pocket that picks up the room cleanly — it slots into the same pipeline. The hardware is interchangeable. The IP is not.

---

## Why this matters now

- The product works. We are not solving a blocker; we are taking a working thing and making it lighter.
- The dependency on hardware-at-the-bedside is real and uneven across hospitals.
- We have a working capture-to-EMR loop already integrated, already in clinicians' hands on mobile.
- We are device-agnostic by design, so we can ride whichever capture form-factor wins.

This is the foundation. The first product on top of it is the bedside capture workflow for doctors, nurses, and the IPD team. The next ones are already lining up.

---

## Let's see it

We've staged the next slide in the light prototype. Open it on the device, walk through the round as the doctor would, and watch the note find its way back into the EMR.
