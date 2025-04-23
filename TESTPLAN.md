# Test Plan for Drag and Drop Deal from "Qualified" to "Negotiations Started"

## Objective
To verify that a user can successfully drag a deal from the "Qualified" column and drop it into the "Negotiations Started" column, and that the UI and backend reflect the correct state after the move.

## Test Scenarios

| ID   | Test Scenario                                         |
|------|-------------------------------------------------------|
| TC1  | Verify card can be selected from "Qualified"          |
| TC2  | Verify visual feedback during drag                    |
| TC3  | Verify "Negotiations Started" accepts drop            |
| TC4  | Verify deal is no longer in "Qualified"               |
| TC5  | Verify deal appears in "Negotiations Started"         |
| TC6  | Verify column totals are updated correctly            |
| TC7  | Verify backend/state is updated after drop            |
| TC8  | Verify drag is blocked for unauthorized users         |
| TC9  | Verify browser compatibility for this action          |

## Preconditions
+ User is logged in with proper permissions.
+ At least one deal is present in the "Qualified" column (e.g., "[Sample] EmpowerMove").
+ The "Negotiations Started" column is visible and unlocked.
+ Internet connection is stable.

## Test Steps

| Step | Action                                                                                      |
|------|----------------------------------------------------------------------------------------------|
| 1    | Log in to the application and open the deals pipeline board.                                |
| 2    | Locate a card under the "Qualified" column (e.g., "[Sample] EmpowerMove").                  |
| 3    | Click and hold the deal card to initiate drag.                                              |
| 4    | Move the cursor to the "Negotiations Started" column while holding the card.               |
| 5    | Drop the card into the "Negotiations Started" column.                                       |
| 6    | Observe any visual feedback, transition effects, or notifications.                          |
| 7    | Check if the card disappears from the "Qualified" column.                                   |
| 8    | Confirm that the card appears under "Negotiations Started".                                 |
| 9    | Check the updated totals in both columns.                                                   |
| 10   | Refresh the page and ensure the card remains in the new column.                             |
| 11   | (Optional) Use dev tools or API to confirm status has changed in backend.                   |


## Expected Results
+ Card can be selected and moved.
+ Visual drag feedback is shown.
+ Drop is accepted by "Negotiations Started".
+ Card disappears from "Qualified".
+ Card appears in "Negotiations Started".
+ Column totals are recalculated.
+ Backend reflects new deal stage.
+ Refresh keeps the new position.
+ Unauthorized users cannot perform the drag.

## Test Environments
Desktop: Chrome, Firefox, Safari (latest versions)

Tablet: iPad Safari

OS: macOS, Windows 11

## Negative Test Cases
Try dragging a card to an invalid column.

Try dragging without holding long enough.

Try moving the card with no network connection.

Try with a read-only or viewer role.
