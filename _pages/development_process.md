---
layout:     default
title:      "The Squeak Development Process"
permalink:  /development_process/
---
{::options parse_block_html="true" /}

The Squeak Development Process supports the improvement of Squeak—the core of the system and its supporting libraries—by its community. The process builds on few basic ideas: the use of Monticello as the primary source code management system, free access for the developers to the main repositories, and an incremental update process for both developers and users.

<div class="row">
<div class="col-md-6 col-lg-6">

## Monticello  Repositories

The main development repository is **[The Trunk](http://source.squeak.org/trunk.html)**:

* <http://source.squeak.org/trunk>

New code will be committed here; the repository is world-readable and writable for the group of core developers.

The main contribution repository is **[The Inbox](http://source.squeak.org/inbox.html)**:

* <http://source.squeak.org/inbox>

This repository is intended as dropbox. It is world-readable *and* world-writable. Everyone is encouraged to contribute code here. Code that the community, after discussion, accepts as fitting will be moved to the *trunk*. 

If contributions do not work or are deemed unfitting, they are moved to **[The Treated Inbox](http://source.squeak.org/treated)** for future reference:

* <http://source.squeak.org/treated>


## Developer access

[The board](/board/) manages developer access to the repositories at <http://source.squeak.org/>. Very active contributors can ask the board for direct write access to the *trunk*. Anybody can suggest other contributors for *trunk* access.

## License

All code submitted to the repositories must be licensed under [The MIT License](https://opensource.org/licenses/MIT).

## How Commits to the Inbox are Merged
If a change in the inbox is accepted the following should be done by a core developer to merge it:
 
 1. Merge the commit in an up-to-date trunk image
 2. Make sure the commit works with the up-to-date image
 3. Commit the merged version
 4. The merge commit has now two ancestors: the previous head of the trunk repository and the commit from the inbox. To provide a consistent history, we have to move the inbox commit to the trunk repository. Therefore go to <http://source.squeak.org/inbox> and look for the commit under versions. After clicking on the version you see details of the version and two buttons which allow you to move the version either to trunk or the treated inbox. Use the move to trunk button to move the change to the trunk.

In case there are no new commits in the trunk repository, core developers can also simply use the "Move to Trunk" button on <http://source.squeak.org/inbox>.

</div>
<div class="col-md-6 col-lg-6">

## Rules of Engagement

Here are some useful guidelines:

* **Merge often.** In particular when you pick up work and immediately before you intend to commit.

* **Exercise caution.** This is a running system and breaking it carelessly is generally frowned upon.

* **Restrain yourself.** Getting developer access does not mean you are free to put in every extension you always wanted to have without discussion.

* **If in doubt, ask.** This is the corollary to the restrain yourself rule. You are not under pressure to ship a product, so you have the time to send a note saying something like “I am planning to fix this old issue and it may have some side effect here or there. Please advise.”

* **You break it, you fix it.** If you change something, you are generally expected to take care of problems caused by this change. Though there are exceptions. If in doubt, please ask.

* **Do good and talk about it.** When you are done with whatever you have been working on, let people know about it. It can be as short as a note to Squeak-dev saying “I have fixed the long standing bug with *xyz.* Please update and enjoy.”

* **Unit Testing.** Unit tests are an essential part of maintaining the reliability of our releases. New unit tests are always welcome. Keep in mind that a unit test should take as little time to run as possible.  Maintaining the reliability of Squeak is always easier when all tests pass: If you break something, the appearance of a new failure or error is immediately obvious and the cause is more easily found. To that end fixes for failures or errors are extremely valuable. Also, please avoid submitting changes that cause failures or errors themselves.


</div>
