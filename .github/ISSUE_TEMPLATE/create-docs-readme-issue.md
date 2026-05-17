---
name: "Add Content to Project Management Process Docs"
description: "Request to add new content or updates to an existing program management process document."
title: "[Process Doc Update]: Create README for OctoAcme Project Management Docs with Process Summary and Links"
labels: ["documentation", "process improvement"]
body:
  - type: dropdown
    id: process_doc
    attributes:
      label: "Which process document do you want to update? (If this is a new document, select '')"
      description: "Select the program management process document you want to add content to. If this is a new process doc, choose ''."
      options:
        - octoacme-project-management-overview.md
        - octoacme-project-initiation.md
        - octoacme-project-planning.md
        - octoacme-execution-and-tracking.md
        - octoacme-risks-and-communication.md
        - octoacme-release-and-deployment.md
        - octoacme-retrospective-and-continuous-improvement.md
        - octoacme-roles-and-personas.md
        - 
    validations:
      required: true

  - type: textarea
    id: content_summary
    attributes:
      label: "Summary of New Content"
      description: "Briefly describe the new content or update you want to add."
      placeholder: "E.g., Add clarification to risk escalation paths, new checklist for releases, additional role responsibilities, etc."
      value: |
        Create a comprehensive README file for the OctoAcme Project Management Docs (`docs/README.md`) that:
        - Provides a brief introduction to OctoAcme's project management framework
        - Contains a summary of the seven core project management processes
        - Includes organized links to all process documentation files in the docs/ folder
        - Serves as the entry point and navigation hub for the project management process documentation
    validations:
      required: true

  - type: textarea
    id: rationale
    attributes:
      label: "Why is this update needed?"
      description: "Explain the reason for this addition. Is it to address a gap, improve clarity, incorporate a best practice, etc.?"
      placeholder: "E.g., Identified gap in process, team feedback, alignment with industry standards, etc."
      value: |
        **Documentation Gap**: Currently, there is no centralized entry point or index for the OctoAcme project management processes. New team members and stakeholders lack a single source of truth for:
        - Understanding how the project management pieces fit together
        - Finding the right document for a specific situation
        - Getting a quick overview of the entire OctoAcme methodology

        **Benefits**:
        - Accelerates onboarding by providing a guided introduction to OctoAcme's approach
        - Improves discoverability of existing documentation across the docs/ folder
        - Establishes a clear conceptual model of the five core project management phases
        - Serves as a reference for stakeholders and external teams
        - Aligns with the purpose of this Copilot Space to scale institutional knowledge
    validations:
      required: true

  - type: textarea
    id: example_content
    attributes:
      label: "Suggested Content (optional)"
      description: "Paste the proposed new text, checklist, diagram, or example content you'd like to add. (Optional)"
      placeholder: "E.g., - New checklist items, - Copy for a new section, - Example scenario, etc."
      value: |
        ## Proposed docs/README.md Structure

        The README should include:

        1. **Title & Welcome** — Sets context for what the docs cover
        2. **Quick Navigation** — Clickable links to all 8 process docs:
           - Project Management Overview
           - Project Initiation Guide
           - Project Planning
           - Execution & Tracking
           - Risk Management & Communication
           - Release & Deployment Guide
           - Retrospective & Continuous Improvement
           - Roles & Personas

        3. **OctoAcme Project Management Approach** — Explains 5 core principles:
           - Customer-First
           - Iterative Delivery
           - Clear Ownership
           - Data-Informed Decisions
           - Psychological Safety

        4. **Project Lifecycle at a Glance** — Table format showing:
           - Phase (Initiation → Planning → Execution → Release → Close & Retrospective)
           - Focus areas for each phase
           - Key deliverables

        5. **Core Roles** — One-liner descriptions of:
           - Project Manager (PM)
           - Product Manager (PdM)
           - Developers
           - QA/Testing
           - Stakeholders

        6. **Key Artifacts** — Bulleted list of critical project documents and outputs

        7. **Communication Cadence** — Meeting schedules by frequency:
           - Daily standups
           - Weekly syncs
           - Bi-weekly or per-sprint reviews
           - Monthly stakeholder updates

        8. **Getting Started** — Role-based and phase-based navigation

        9. **Contributing & Feedback** — Instructions for proposing improvements

  - type: checkboxes
    id: acceptance_criteria
    attributes:
      label: "Acceptance Criteria"
      description: "Check all that apply:"
      options:
        - label: "Content aligns with existing process docs"
          required: true
        - label: "Update improves clarity or closes a documented gap"
          required: true
        - label: "Proposed content has been reviewed with stakeholders (if needed)"
          required: true
