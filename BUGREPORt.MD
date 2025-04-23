After spending some time with the pipedrive software I have not yet encountered a bug but here are some hypothetical bug reports that could occur on the deals interfce.

1. ### Drag Action Not Triggering on Card

Description: Users are unable to initiate drag on certain deal cards.

Steps to reproduce:

+ Hover over any card in the "Qualified" column.

+ Attempt to click and drag the card to another column.

Expected: The card should become draggable and follow the cursor.

Actual: Nothing happens; the card stays fixed.

Severity: Major

Environment: Chrome 123, macOS Ventura

 2. ### Drop Not Accepted by Valid Column

Description: Dropping cards into allowed columns does not register.

Steps:

+ Drag a deal from "Prospect Qualified" to "Needs Defined".

Expected: Card moves and appears under "Needs Defined".

Actual: Card snaps back to original column.

Severity: Major

Environment: Firefox 115, Windows 11

3. ### Incorrect Deal Status After Drop

Description: UI shows new column, but backend status remains old.

Steps:

+ Move a card from "Contact Made" to "Proposal Made".

+ Refresh the page.

Expected: Card stays in "Proposal Made".

Actual: Card reappears in "Contact Made".

Severity: Critical

Environment: Edge 124, Windows 10

4. ### Column Totals Not Updating After Move

Description: Monetary totals at the top of each column do not reflect card changes.

Steps:

+ Move a 30,000 € deal from "Contact Made" to "Proposal Made".

Expected: Totals update (subtract from "Contact Made", add to "Proposal Made").

Actual: Totals remain unchanged.

Severity: High

Environment: Safari 17.3, iPadOS

5. ### Undo After Card Move Does Not Work

Description: Undo feature does not restore card to previous column.

Steps:

+ Drag a deal to a different stage.

+ Press Cmd+Z (or click “Undo” if available).

Expected: Card reverts to original position.

Actual: Nothing happens.

Severity: Medium

Environment: Chrome 122, macOS

6. ### Visual Glitch on Dragging

Description: Card flashes and misaligns while being dragged.

Steps:

+ Click and drag any deal card across columns.

Expected: Smooth transition with consistent layout.

Actual: Card appears jittery or disappears momentarily.

Severity: Low

Environment: Chrome 123, Linux (Ubuntu)

7. Drop Highlight Not Appearing

Description: No visual feedback (highlight) when dragging over valid columns.

Steps:

+ Drag a card and hover over another column.

Expected: Column background changes or shows a drop indicator.

Actual: No visual change.

Severity: Low

Environment: Safari 16, macOS Monterey

8. ### User Without Permissions Can Move Cards

Description: Read-only users can drag and drop cards.

Steps:

+ Log in with a restricted account.

+ Drag a deal from one column to another.

Expected: Drag action should be disabled.

Actual: Card is moved and saved.

Severity: Critical

Environment: Chrome 123, Windows 10

 9. ### Cards Overlap After Drop

Description: Cards are visually overlapping or stacked.

Steps:

+ Move several cards quickly between columns.

Expected: Each card has proper spacing.

Actual: Cards are overlapping, causing readability issues.

Severity: Medium

Environment: Firefox 115, macOS Ventura

 10. ### Drag-and-Drop Broken on Mobile Devices

Description: Unable to drag or drop on touchscreens.

Steps:

Open the board on a tablet or phone.

Try to move a deal card with touch.

Expected: Card should follow finger and move smoothly.

Actual: Scroll happens instead, or nothing moves.

Severity: Major

Environment: Safari on iPadOS 17
