# api-plumber
An alternative to Postman/Newman that should be scriptable, and enable usage of your favorite
editor and VCS.

Currently, this is just a collection of the ideal way to test REST-ful (and hopefully other)
APIs.

## Failings of Postman/Newman

Currently, Postman collections are stored as a single, monolith JSON file, which makes
version control very difficult.

Additionally, the most effective way to edit Postman collections is through a Postman-type
UI (Postman, Milkman, etc.), as the complexity of the JSON single file format requires this
type of editing.

Both of these issues can be traced back to one particular design flaw (in my opinion at
least): each collection is only really exported as a single file. This makes large collections
with a huge number of requests difficult to manage for long-lived applications.

Perhaps most critical for users is that the Postman application **requires** an account.
This leads to very understandable discomfort if misused, as that opens the option for
uploading sensitive environment details to the Postman cloud with some misconfiguration.

## Major successes of Postman/Newman

The most impactful element of Postman are the pre-request/post-request/authorization/testing/etc.
scrtips that a tester can write and contribute to.

The ability to have collection/environment scoped variables greatly improves the usefulness
of Postman, specifically for things like the authentication.

## Alternatives

As mentioned earlier, Milkman is a potential alternative to Postman, but largely carries
over my earlier complaints about the fundemental issue with dealing with larger-scale
collections (namely that they are all still stored in one single file, at least when
exporting the files). 

Another promising alternative is `reqman`. This might require significant investigation.
I might try this to compare and see it's benefits/shortcomings. Here is the
[GitHub page](https://github.com/manatlan/reqman).
