# Nexus appointment desk — static version

Open index.html directly or use any static web host. No PHP, API credentials, build step, or installation is required.

## GitHub Pages

Upload this project to your GitHub repository. In Settings → Pages, choose Deploy from a branch, select your branch and / (root), and save. The root index.html opens the dashboard in AS/. Alternatively upload just the contents of AS/ at the repository root.

Share the Pages URL once deployment finishes. No repository or deployment has been created automatically.

## Using the dashboard

1. Expand Workspace setup. Enter the meeting owner's email and choose the meeting time zone. Save settings on each setter's device.
2. Enter customer and meeting details, then save the appointment draft.
3. On its card, choose Open Google Calendar. Review time, calendar, guests, and availability; save the event and send invitations in Google Calendar.

Google Calendar uses the Google account signed in on the setter's device. The owner email is included as a guest, not the organizer. For direct creation on the owner's calendar, grant the setter calendar editing permissions and have them select that calendar before saving. Otherwise the owner receives an invitation, subject to their Google Calendar invitation settings.

## Current limits

- This public static page has no sign-in or shared database. Drafts and settings stay in browser localStorage, with no sync between devices or setters. Clearing site data removes them. People using the same browser profile can access them.
- Local draft overlaps are checked; live calendar availability is not checked.
- Drafts do not create events or send invitations. Opening Calendar does not confirm a save. Drafts remain labeled as drafts.
- Delete draft removes only the local copy. It does not cancel a Google Calendar event. Reopening and saving a draft again can create duplicates.
- Times use the chosen IANA time zone with daylight saving offsets. Skipped spring-forward times are rejected. Verify the intended offset for a repeated fall-back hour in Google Calendar before saving.
- Customer details are included in Google Calendar links when opened. Never put API secrets or passwords in static files.

Shared team data, individual accounts, and automatic calendar booking can be added later with a backend.
