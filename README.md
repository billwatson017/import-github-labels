Useful labeling system used in all my repositories.

- Visit the labels page https://github.com/{user}/{repo}/labels
- Click on "New Label"
- Open the Developer Console
- Paste this snippet and hit enter

```js
const labels = [
  {
    "name": "DO NOT MERGE",
    "description": "Do not merge this pull request",
    "color": "e11d21"
  },
  {
    "name": "Impacts: API",
    "description": "Pull request changes impact the API only",
    "color": "00E9FE"
  },
  {
    "name": "Impacts: UI + API",
    "description": "Pull request changes impact the UI & API",
    "color": "FEB1D5"
  },
  {
    "name": "Impacts: UI",
    "description": "Pull request changes impact the UI only",
    "color": "00FEB9"
  },
  {
    "name": "Priority: Critical",
    "description": "Bug, issue, or pull request is a P0",
    "color": "FD8E8E"
  },
  {
    "name": "Priority: High",
    "description": "Bug, issue, or pull request is a P1",
    "color": "FFA28B"
  },
  {
    "name": "Priority: Low",
    "description": "Bug, issue, or pull request is a P3",
    "color": "8DE6A0"
  },
  {
    "name": "Priority: Medium",
    "description": "Bug, issue, or pull request is a P2",
    "color": "FFDB8B"
  },
  {
    "name": "Severity: Critical",
    "description": "The issue is blocking a release",
    "color": "FD8E8E"
  },
  {
    "name": "Severity: High",
    "description": "The issue results in data loss, crashes, makes the system unresponsive",
    "color": "FFA28B"
  },
  {
    "name": "Severity: Low",
    "description": "Bug or issue is of low severity",
    "color": "8DE6A0"
  },
  {
    "name": "Severity: Medium",
    "description": "The issue is related to incorrect/bad functionality or confusing UX",
    "color": "FFDB8B"
  },
  {
    "name": "Status: Approved",
    "description": "This pull request has been approved",
    "color": "74DB75"
  },
  {
    "name": "Status: Blocked",
    "description": "This pull request is blocked by something",
    "color": "dd114e"
  },
  {
    "name": "Status: Do Not Review",
    "description": "Do not review this pull request",
    "color": "dff99d"
  },
  {
    "name": "Status: Info Needed",
    "description": "The issue needs more information before it can be verified and merged",
    "color": "dff99d"
  },
  {
    "name": "Status: Invalid",
    "description": "The reported issue is not valid or the functionality is intended.",
    "color": "dd114e"
  },
  {
    "name": "Status: Needs Changes",
    "description": "The pull request needs additional changes before it can be merged",
    "color": "F0A7DC"
  },
  {
    "name": "Status: Needs Docs",
    "description": "The pull requests requires documentation of feature or changes",
    "color": "F0A7DC"
  },
  {
    "name": "Status: Needs Tests",
    "description": "The pull request is missing or does not have adequate tests",
    "color": "F0A7DC"
  },
  {
    "name": "Status: Not Reproducible",
    "description": "The reported issue is not reproducible",
    "color": "FFDB8B"
  },
  {
    "name": "Status: On Hold",
    "description": "This pull request is not being worked on",
    "color": "FFF7AD"
  },{
    "name": "Status: Review Needed",
    "description": "This pull request needs a review",
    "color": "FFDB8B"
  },
  {
    "name": "Status: WIP",
    "description": "This pull request is in progress",
    "color": "ffec84"
  },
  {
    "name": "Status: Won't Fix",
    "description": "The issue is not legitimate",
    "color": "dd114e"
  },
  {
    "name": "Type: Bug",
    "description": "Something isn't working",
    "color": "dd114e"
  },
  {
    "name": "Type: CI/CD",
    "description": "Issue or pull request contain infrastructure changes only",
    "color": "FFF7AD"
  },
  {
    "name": "Type: Duplicate",
    "description": "This issue or pull request already exists",
    "color": "FFDB8B"
  },
  {
    "name": "Type: Refactor",
    "description": "Enhancements, deletions, etc. to existing code",
    "color": "84B6EC"
  },
  {
    "name": "Type: Feature",
    "description": "A new feature or functionality",
    "color": "00FED8"
  },
  {
    "name": "Type: Housekeeping",
    "description": "General maintenance and package upgrades",
    "color": "ffec84"
  },
  {
    "name": "Type: Proposal",
    "description": "Issue or pull requests contains a new proposal",
    "color": "f97f63"
  },
  {
    "name": "Type: Question",
    "description": "Issue or pull requests contains questions that need answers",
    "color": "FF96C9"
  }
]

const name = document.getElementById('label-name-');
const description = document.getElementById('label-description-');
const color = document.getElementById('label-color-');
const submit = document.querySelector('.js-label-form .btn.btn-primary');

labels.forEach((label) => addNewLabel(label));

function addNewLabel (label) {
  name.value = label.name;
  description.value = label.description;
  color.value = '#' + label.color;
  submit.removeAttribute('disabled');
  submit.click();
}
```
