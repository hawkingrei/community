# Coprocessor SIG Constitution

This charter follows the TiKV Community charter and system, using the role definitions and responsibilities in [SIG Governace](/GOVERNACE-zh_CN.md).

## Scope

Coprocessor SIG focuses on the TiKV project Coprocessor module, which is the module in TiKV that handles TiDB's pushdown calculations. The primary responsibility of this SIG is to discuss, plan, develop, and maintain the future development of the Coprocessor module. Only Active Contributor or higher-level community members can become members of the SIG and participate in the matter, but the decisions and projects undertaken by the SIG will be made public.

## Routine Work

- Code range
  - Framework: Computational framework improvements, including expression calculation frameworks, operator execution frameworks, etc.
  - Executor: Improve existing operators and collaborate with TiDB to develop new operators;
  - Function: Maintain an existing UDF / AggrFn implementation or a new UDF / AggrFn implementation from the TiDB port;
  - Code location: [tidb_query](https://github.com/tikv/tikv/tree/master/components/tidb_query) module.

- Test Specification
  - The code needs to pass existing integration tests, and new changes need to be added to [copr-test](https://github.com/tikv/copr-test) to add new integration tests;
  - The function from the TiDB port needs to be a port unit test at the same time. If the unit test of TiDB does not cover all branches, you need to complete the unit test.
  - Expression's integration test requires constructing an operator that uses this Expression for testing.

- Design and Evolution Proposal
- Review related project code

## Other

- Code style, submission specification, PR Description template, etc. Please refer to [Documentation](https://github.com/tikv/tikv/blob/master/CONTRIBUTING.md)

- Task Assignment
  - SIG Tech Lead maintains a public [Member List](./membership.md) and [Task Map](./workflow-zh_CN.md) link at https://github.com/tikv/community.
  - New SIG members can have 2 weeks to learn more about each task and claim a task, or participate in the development or promotion of an existing task. If the task is not claimed within this time, the SIG will be removed.
  - SIG members are required to maintain a monthly development engagement or participate in the design and discussion of existing features or future plans. If it does not participate in development and discussion for one quarter, it is considered inactive and will be removed from the SIG. As acknowledgment, it will still be in the "Former Member" of the member list.

- Regularly synchronize progress, regular weekly meetings
  - Synchronize the development progress of each current project in document form every 2 weeks.
  - A full group progress meeting will be held every 2 weeks, depending on the available time of the participants. Members who are currently not developing a project are eligible to participate in order to understand the progress of each project. If the participating members are unable to participate, you must take time in advance and update your monthly progress to the document in advance.
  - A meeting is recorded by one member at each meeting, and the meeting minutes are completed and made public within 24 hours of the end of the meeting. The minutes of the meeting are executed by the team members in turn.
  - Slack: https://tikv-wg.slack.com #copr-sig-china

- Organize the activities of offline members

- Tech Leads additional responsibilities
  - Questions from SIG member need to be answered within 2 business days
  - Timely Review code
  - Timed release tasks (unfinished tasks need to be reassigned if SIG member exits)


## Promtion

- Assessment & Promotion System
  - Tech Leader evaluates team members on a monthly basis to determine whether members can be promoted to Reviewer by Active Contributor:
    - Familiar with the code base
    - Nominated for at least 2 TiKV Committer
    - PR contribution meets any of the following:
      - More than 10 Merge Coprocessor PR
      - Merge Coprocessor PR has more than 1000 lines
      - A task with a difficulty of Medium or above has been completed
      - Presenting design ideas and adopting them into more than 3 executable tasks

  - Tech Leader and TiKV Maintainer evaluate team members on a quarterly basis to determine whether members can be promoted from Reviewer to Committer:
    - Show good technical judgment
    - Nominated for at least 2 TiKV Maintainers
    - Complete at least two tasks with difficulty Medium or a task with difficulty High
    - The PR contribution meets at least two points:
      - Merge Coprocessor PR total line number exceeds 1500 lines within half a year
      - Valid Review Coprocessor PR totals over 10
      - Valid Review Coprocessor PR total number of lines exceeds 1000 lines

- Advance role rights & obligations
  - Reviewer
    - Participate in project design decisions
    - Participate in Coprocessor PR Review and quality control
    - Valid Approve / Request Change permission on Coprocessor module PR

  - Committer
    - Have the rights and obligations of Reviewer
    - Code quality of the overall control project
    - Guide Contributor and Reviewer

- Quit
  - SIG members will be removed from the SIG in the following cases, but retain the corresponding Active Contributor / Reviewer / Committer identity:
    - as a new member did not claim the task within the specified time
    - Inactive for one quarter in a row

  - Reviewer will cancel the Reviewer status and reclaim the right if one of the following conditions is met (recoverable after subsequent re-assessment):
    - No reviews for more than one quarter. Any Coprocessor related PR
    - More than 2 Committer thinks Reviewer is not capable or active enough
