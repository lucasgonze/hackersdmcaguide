# Hacker's Guide to DMCA Takedowns

Developers have a hard time getting clear and simple guidance on how to handle copyright infringement notices.

In some ways this is justified, because the law is complex and unclear. But many aspects of the law are simple enough, and anyway, developers don't have a choice about whether to simplify. They can't hire a lawyer for every little bit of noise that comes through. If lawyers can't write clear and simple instructions, the hackers must do it for themselves.

Improvements to this document are welcome. It is on Github for a reason.

Warnings:

1.  These instructions are for informal projects with little infringement
2.   No lawyers wrote this. This is not legal advice. 

## How-To

### Setup

1.  Formal Steps Required for DMCA Compliance
    1.  Get an email address just for DMCA complaints
    2.  Register an agent with the US Copyright Office. See [http://copyright.gov/onlinesp](http://copyright.gov/onlinesp)
    3.  Publish notice about how to reach you to file a takedown request
        1.  Put a link in a site-wide footer
        2.  At that link put the contact information from your registration with the US Copyright office
        3.  In your terms of service document reserve the right to take down content and disconnect accounts. State that you have a policy of disconnecting repeat infringers.
2.  Get lawyer input and create legal policies
    1.  When to count a complaint as an infringement for the purpose of disconnecting repeat infringers. (default: always)
    2.  How many infringements are enough to disconnect a repeat infringer? (default: two)
    3.  When to decrement the infringement count for an repeat infringer (default: never)
    4.  Time limit for responding to a notice (default: one day)
    5.  Vet the guidance in this document
3.  Figure out the technology to
    1.  Disable and re-enable access to content
    2.  Get email address of account which owns a link you host
    3.  Disable and re-enable an account
    4.  Track repeat infringements

### When a Complaint Arrives

When a notice of alleged infringement arrives from the copyright owner or their agent, via email, snail mail, or fax...

1.  Verify that all required fields (see "Required fields for notices of alleged infringement") are filled in and the values make sense. If not, reject the notification.
2.  Verify that the request contains enough information to figure out where in the web site (or app) the alleged infringement is occurring. If not, reject the notificaiton.
3.  Disable access to the content. Take care to not damage it in a way that prevents you from re-enabling access..
4.  Inform the user that you have taken down the content. Inform them of their right to file a counter notice and give them a pointer to info on doing them. Here is an example from Github: [https://help.github.com/articles/guide-to-submitting-a-dmca-counter-notice/](https://help.github.com/articles/guide-to-submitting-a-dmca-counter-notice/)
5.  Increment the infringement count for the user
6.  Look up the infringement count for the user. If it is greater than the maximum, disconnect the users account.

### Counter-Notice

When a counter-notice arrives from the user/uploader, inbound via email, snail mail, or fax...

1.  Verify that the three day window has not expired. If it has expired, reject the counter-notice.
2.  Verify that all the fields are filled in and the values are correct. (DMCA Section 512(g)(1) is the canonical source of info. See [http://www.copyright.gov/title17/92chap5.html#512](http://www.copyright.gov/title17/92chap5.html#512))
3.  Forward the counter notice to the copyright owner.
4.  Set a ten-day timer to put back the content if the copyright owner has not filed suit against the user and informed you.
5.  Consider decrementing the infringement counter for this user.

### Ten-Day Timer

When the ten-day timer goes off...

1.  Verify that you have not received a notice that the copyright owner has filed a lawsuit. If not, put back the content and (if you haven't already) decrement your repeat infringement counter.
