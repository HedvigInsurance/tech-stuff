# Making payments (charges)

The charging should take place 26th of every month before 12 for the money to be pulled from the members' accounts on the 27th.

## Steps

1. Get how payments went last month by calling endpoints XYZ and counting the returned results to get # of failed (CHARGE_FAILED - insufficient funds, CHARGE_REQUEST_FAILED - dd not connected), successful (CHARGE_COMPLETED - it worked and we got the money 🎉)  and skipped (CHARGED_SKIPPED, we don't know why - everything else) charges. Send this to Emma and Kajsa (iex) for their information.
1. Make a little dance - kubetail all account service pods (since work is load balanced) to see that everything is ok along the way. 
1. Resets - reset the payments state machine by calling the endpoint BLA. You can tell progress by checking the member ids. Some may have "forbidden transitions" and thats ok (unless theres too many) but most should jump into `WAITING_FOR_SUBSCRIPTION` state.
1. Fetch what everyone owes us, so the monthly premium ends up in their account by calling endpoint BLABLABLA.

