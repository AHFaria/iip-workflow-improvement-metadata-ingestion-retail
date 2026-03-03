# iip-workflow-improvement-metadata-ingestion-retail
From the Description:
Workflow created for a sample 30-day vendor product catalog upload for a retail product information management system.  Includes a multi-sheet workbook, notes for file issue tracking, and a Quick Stats sheet with pivot tables.  Highlights skills in: data governance, metadata intake &amp; triage, data quality, pivot reporting &amp; dashboard metrics.


# 🗂️ Retail Metadata Ingestion and Workflow Improvement

**Skills demonstrated:** Data governance · Metadata intake & triage · Data quality · Workflow design · Vendor escalation tracking · Pivot reporting & dashboard metrics

## 📋 Overview

When a system receives hundreds of vendor file uploads with thousands of elements, the raw data tells you what came in. It does not tell you what to do with it, what is broken, or what files keep coming back with the same problem week after week.

This workflow is based on a real process I developed and used during my time as a metadata analyst at a publishing systems company. I adapted it here using a simulated retail product catalog scenario to show how the logic translates across industries.

## ❓ The Problem

A retail product information management system receives vendor catalog files on a rolling basis. Vendors submit their files at different frequencies whether that is daily, weekly, once a quarter, or whatever best works for them.  A query is run to return an output log of all files an analyst recieves related to their portfolio during an established time frame. Files arrive in different formats with varying quantities of records and while some records ingest cleanly files with errors are sent on to the analyst for resolution. In some instances the same file can keep coming back with the same issue every single cycle.

Without structure, all of that lands in one flat log. There is no easy way to see why something needs attention, what has already been worked, what is fully resolved, and what is simply not going to resolve without escalation or client contact.

## 🔧 What I Built

Starting from the raw 30 day upload sample log, I designed a multi-sheet workbook that separates the data into actionable categories, while adding a tracking layer the original output was missing with the use of inserted notes.

**Workbook tabs:**

* **About This File**: Disclaimer, file description, and workflow notes
* **30 Day Upload Log**: The raw query output, unmodified
* **Formatted for Weekly Workflow**: The structured working view with status columns and inline notes
* **To Be Worked**: Files with unresolved errors still requiring action
* **Completed**: Files fully ingested with no outstanding errors
* **Completed with Errors**: Files that were worked and actioned but still carry remaining errors
* **Quick Stats**: Summary and rolling pivot metrics by vendor and file

## 📝 The Notes

The notes are one of the most important additions to the formatted workflow tab. This is where I document what was actually done at the file level. Not just that an error existed, but what steps were taken to address it and in some instances examples of the error.

Notes capture the contact method used such as email, Jira ticket, or vendor portal. They also capture the escalation path including sales rep notification or tech team involvement, research findings like confirming a vendor's status through a corporate press release or state business registry, and anything still open that needs further action.

This kind of inline documentation means anyone picking up the file partway through a cycle knows exactly where things stand without having to ask or wait for the analyst to provide progress insight.

<img width="1600" height="915" alt="Formatted Weekly Workflow with Notes" src="https://github.com/user-attachments/assets/8ad2675d-9088-47d5-a88f-41bd1dca0b98" />

## ⚠️ Worked vs. Resolved

A file being worked is not the same as a file being resolved. This workflow captures that difference on purpose.

The Completed tab contains files that were fully ingested with no errors remaining. The Completed with Errors tab contains files that were actioned, meaning vendor contacted, ticket created, and team notified, but where errors are still outstanding even if the analyst was able to resolve some issues for ingestion. Both tabs use a binary flag column that feeds the pivot tables in Quick Stats to keep counts accurate and auditable.

This distinction matters because it separates what you can close out from what needs ongoing monitoring. Tracking action taken separately from outcome achieved is a core part of responsible data governance and it shows up clearly in how this workbook is structured.  This information can then be used by the analyst the following week by carrying over relevant notes on returning problem files, thus shortening work time by avoiding re-working problem files and allowing the analyst to spot patterns that may arise from specific vendors.

## 🔁 The Persistent Format Issue

One example of a persistent problem is a vendor, Hexford Wholesale, which submits exclusively in PDF format. In this case, the ingestion system cannot process PDF files. Every upload attempt results in zero records ingested.

Hexford appears in Completed with Errors rather than To Be Worked because vendor contact was made and documented. The format issue remains unresolved because the vendor has not changed their submission format. This is a very common real world scenario in metadata intake work.  A case like this, if not caught and noted, can result in skewed metrics and reporting for both the analyst and department.

Some problems are not technical issues you can fix on your end. They are vendor compliance issues you can only track, escalate, and document until something changes on their side.

## 📊 Quick Stats Dashboard

The Quick Stats tab provides two pivot views side by side.

The Original Upload section shows total errors at the start of the cycle by vendor, expandable to the individual file level. The Rolling Stats section shows current errors remaining by vendor, ranked from highest to lowest, also expandable to the file level.

Summary metrics across the top show total errors at upload, errors still to be worked, errors resolved, and standing errors in completed files. Together they give a clear picture of where the cycle stands without scrolling through hundreds of rows.

These pivot tables and metrics can later be compared to future workflows not only to compare stats, but also to locate ways to streamline vendor file frequencies, turnaround time, or average files recieved or worked.

<img width="1305" height="919" alt="Quick Stats Pivot Table" src="https://github.com/user-attachments/assets/808c94b6-b596-4670-bab5-5816303b24b7" />

## ⚙️ Tools Used

* Google Sheets
* Pivot tables for summary and rolling metrics
* Conditional formatting for visual triage indicators
* Inline notes for escalation and research documentation

## ⚠️ Disclaimer

All vendor names, IDs, and associated data in this file are entirely fictional and have been generated for portfolio demonstration purposes only. Any resemblance to real companies, active or inactive, is coincidental. The workflow structure is based on real professional experience adapted at scale for public portfolio use.

*A.H. Faria | Data Governance & Metadata Professional*
