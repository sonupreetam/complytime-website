# [CPLYTM-1162] ComplyTime Website Skeleton

**Author:** Sonu Preetam
**Date:** February 5, 2026
**Status:** Implemented
**JIRA:** CPLYTM-1162

---

## 1. Objective

Create a **website skeleton** for the unified ComplyTime site, with the capability to **aggregate existing content from the complyscribe site** into a single consolidated ComplyTime website.

---

## 2. Scope

### In Scope
- Basic website skeleton structure
- Page templates and layout framework
- Navigation structure
- Content aggregation plan from complyscribe site
- Placeholder pages for future content
- Tutorials section with placeholder entries

### Out of Scope (Future Work)
- Advanced interactive features
- Custom animations/effects
- Full content writing
- API documentation auto-generation
- Architecture Diagrams

---

## 3. Current State

### ComplyTime Website (complytime.dev)
- Built with Hugo + Doks theme
- Contains: Homepage, Getting Started, Projects (4), Architecture, Tutorials (4 placeholders), Contributing
- Deployed via GitHub Pages (GitHub Actions CI/CD)

### ComplySribe Site (aggregated)
- Separate documentation for complyscribe project
- Repository: [github.com/complytime/complyscribe](https://github.com/complytime/complyscribe)
- Content includes: Installation, Quick Start, Templates, Configuration, Integration guides
- Key content has been aggregated into `/docs/projects/complyscribe/`

---

## 4. Implemented Website Structure

### 4.1 Site Structure

```
complytime.dev/
├── /                              # Homepage (custom layout)
├── /docs/
│   ├── /getting-started/          # Unified getting started
│   │
│   ├── /projects/                 # All ComplyTime projects
│   │   ├── /complyctl/            # CLI tool for compliance workflows
│   │   ├── /complyscribe/         # ← Aggregated from complyscribe site
│   │   ├── /collector-components/ # Observability toolkit
│   │   └── /compliance-to-policy/ # C2P framework
│   │
│   ├── /architecture/             # Technical architecture
│   │   └── /oscal/                # OSCAL integration
│   │
│   ├── /tutorials/                # Step-by-step guides
│   │   ├── /complyscribe-github/  # complyscribe + GitHub Actions
│   │   ├── /complyctl-quickstart/ # complyctl quickstart
│   │   ├── /c2p-mapping-guide/    # C2P mapping guide
│   │   └── /collector-components-setup/ # Collector setup
│   │
│   └── /contributing/             # Contribution guide
│
└── /privacy/                      # Privacy policy
```

### 4.2 Navigation

| Menu       | Item       | URL                       |
|------------|------------|---------------------------|
| Main navbar | Docs      | `/docs/getting-started/`  |
| Main navbar | Projects  | `/docs/projects/`         |
| Main navbar | Tutorials | `/docs/tutorials/`        |
| Main navbar | Community | `/docs/contributing/`     |
| Docs sidebar | Getting Started | `/docs/getting-started/` |
| Docs sidebar | Projects  | `/docs/projects/`         |
| Docs sidebar | Concepts | `/docs/concepts/`  |
| Docs sidebar | Tutorials | `/docs/tutorials/`        |
| Docs sidebar | Contributing | `/docs/contributing/`  |

### 4.3 Custom Layouts

| Layout | Purpose |
|--------|---------|
| `layouts/home.html` | Custom homepage with hero, features grid, projects showcase, and CTA |
| `layouts/docs/list.html` | Custom docs listing layout with wider content area, sidebar, TOC, and breadcrumbs |

### 4.4 Implemented Pages

| Page | Type | Description |
|------|------|-------------|
| `/docs/tutorials/` | Landing page | Styled card grid linking to tutorial entries |
| `/docs/tutorials/complyscribe-github/` | Placeholder | complyscribe GitHub Actions workflow tutorial |
| `/docs/tutorials/complyctl-quickstart/` | Placeholder | complyctl quickstart guide |
| `/docs/tutorials/c2p-mapping-guide/` | Placeholder | C2P mapping tutorial |
| `/docs/tutorials/collector-components-setup/` | Placeholder | Collector components setup guide |
| `/docs/projects/complyscribe/` | Updated | Expanded with aggregated complyscribe documentation |

---

## 5. Content Aggregation Plan

### 5.1 From ComplySribe Site → ComplyTime

| Source Content | Target Location | Action | Status |
|----------------|-----------------|--------|--------|
| Installation docs | `/docs/projects/complyscribe/#installation` | Merge | ✅ |
| Quick Start | `/docs/projects/complyscribe/#quick-start` | Merge | ✅ |
| Templates reference | `/docs/projects/complyscribe/#templates` | Merge | Pending |
| Configuration guide | `/docs/projects/complyscribe/#configuration` | Merge | Pending |
| CI/CD Integration | `/docs/projects/complyscribe/#integration` | Merge | ✅ |
| API Reference (if any) | `/docs/projects/complyscribe/#api` | Add | Pending |

### 5.2 Content Migration Checklist

- [x] Audit complyscribe site for all existing content
- [x] Map complyscribe URLs to new ComplyTime URLs
- [x] Update internal links to point to unified site
- [x] Ensure consistent formatting with ComplyTime docs style
- [x] Add cross-references between related projects

---

## 6. Skeleton Templates

### 6.1 Placeholder Page Template

```markdown
---
title: "Section Title"
description: "Brief description"
lead: "This section is coming soon."
date: 2026-02-05T00:00:00+00:00
draft: false
weight: 100
toc: false
---

## Coming Soon

This section is under development. Check back soon for updates!

In the meantime, you can:

- [Explore our documentation](/docs/getting-started/)
- [View our projects](/docs/projects/)
- [Join the community](https://github.com/complytime/community)

Have questions? [Open a discussion](https://github.com/orgs/complytime/discussions).
```

### 6.2 Tutorial Page Template

```markdown
---
title: "Tutorial Title"
description: "What the reader will learn"
lead: "A brief summary of the tutorial."
date: 2026-02-05T00:00:00+00:00
draft: false
weight: 110
toc: true
---

## Overview

Introduction to what this tutorial covers.

## Prerequisites

- Requirement 1
- Requirement 2

## What You'll Learn

- Learning objective 1
- Learning objective 2

## Steps

> 🚧 **Coming Soon** — This tutorial is under development.

## Related Resources

- [Related Project Page](/docs/projects/...)
- [Project on GitHub](https://github.com/complytime/...)
```

---

## 7. Implementation Tasks

### Phase 1: Skeleton Setup (Week 1)

| Task | Effort | Status |
|------|--------|--------|
| Create `/docs/tutorials/_index.md` landing page | 1 hr | ✅ |
| Create tutorial placeholder pages (4 entries) | 2 hrs | ✅ |
| Update navigation menus for new sections | 1 hr | ✅ |
| Replace Blog with Tutorials in navigation | 30 min | ✅ |
| Create custom `layouts/docs/list.html` | 2 hrs | ✅ |
| Verify site builds correctly | 30 min | ✅ |

### Phase 2: Content Aggregation (Week 2)

| Task | Effort | Status |
|------|--------|--------|
| Audit complyscribe site content | 2 hrs | ✅ |
| Expand `/docs/projects/complyscribe.md` | 3 hrs | ✅ |
| Add cross-references between projects | 1 hr | ✅ |
| Update internal documentation links | 1 hr | ✅ |

### Phase 3: Review & Polish (Week 3)

| Task | Effort | Status |
|------|--------|--------|
| Review all content for consistency | 2 hrs | ☐ |
| Test all navigation and links | 1 hr | ☐ |
| Get team feedback | Async | ☐ |
| Address feedback | 2 hrs | ☐ |
| Deploy to production | 30 min | ☐ |

---

## 8. Questions for Team

1. **Content Depth:** Should `/docs/projects/complyscribe/` be expanded to multiple sub-pages?

2. **Tutorials:** Which placeholder tutorials should be prioritized for full content?

3. **Community Page:** Should `/docs/contributing/` be expanded with more community resources?

---

## 9. Success Criteria

- [x] Website skeleton structure implemented
- [x] All placeholder pages created and accessible
- [x] ComplySribe content successfully aggregated
- [x] Navigation updated to reflect new structure (Blog → Tutorials)
- [x] No broken links
- [x] CI/CD workflow configured for GitHub Pages deployment
- [ ] Site deploys successfully to production

---

## 10. Next Steps

1. **Review** this proposal with the team
2. **Answer** the remaining questions in Section 8
3. **Complete** Phase 3 review and polish tasks
4. **Write** full tutorial content for prioritized entries
5. **Deploy** to production

---

*Document Version: 2.0 | JIRA: CPLYTM-1162*
