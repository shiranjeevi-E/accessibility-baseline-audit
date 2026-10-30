# Accessibility Baseline & Repository Architecture Audit

## 1. Project details
- **Audit target:** India Post public website
- **Website:** https://www.indiapost.gov.in/
- **Audit date:** __________________
- **Auditor:** __________________
- **Device/browser:** __________________
- **Viewport:** Mobile / Desktop (circle one)
- **Pages and user journeys tested:** __________________

## 2. Purpose
The purpose of this focused audit is to establish an accessibility baseline for a public-facing service website and prepare a maintainable full-stack repository foundation. The review concentrates on keyboard access, form instructions, text alternatives, contrast and visible focus.

## 3. Tools and method
### Lighthouse
Run Lighthouse against the selected page using Chrome DevTools or Google PageSpeed Insights. Record the actual scores below and save a screenshot under `docs/screenshots/`.

| Metric | Actual result |
|---|---|
| Performance | To be measured |
| Accessibility | To be measured |
| Best Practices | To be measured |
| SEO | To be measured |

Lighthouse URL: https://pagespeed.web.dev/

### Keyboard-only pass
Without using a mouse:
1. Press Tab repeatedly and note the focus order.
2. Press Shift+Tab to verify reverse navigation.
3. Use Enter and Space on links and buttons.
4. Use Esc on menus/dialogs where applicable.
5. Try to reach and complete the main form or service journey.

Record the exact page, control, key pressed and observed result. Save screenshots where possible.

## 4. Five audit checks
The following are planned checks. They are not represented as confirmed defects until tested.

| ID | Component | WCAG reference | What to verify | Priority if failed |
|---|---|---|---|---|
| WEB-001 | Main navigation | 2.1.1 Keyboard | All navigation links and menus can be operated by keyboard. | High |
| WEB-002 | Service/search form | 3.3.2 Labels or Instructions | Inputs have clear labels/instructions and required formats are explained. | High |
| WEB-003 | Informative images/icons | 1.1.1 Non-text Content | Meaningful images have appropriate text alternatives; decorative images are ignored by assistive technology. | Medium |
| WEB-004 | Text and controls | 1.4.3 Contrast (Minimum) | Text has sufficient contrast against its background. | Medium |
| WEB-005 | Interactive controls | 2.4.7 Focus Visible | Keyboard users can clearly see which control currently has focus. | High |

Detailed evidence, user impact and fixes must be entered in `docs/accessibility-issues.csv` after testing.

## 5. Evidence register
Add evidence files to `docs/screenshots/` and list them here.

| Evidence file | What it demonstrates |
|---|---|
| `lighthouse-overview.png` | Actual Lighthouse report and scores |
| `keyboard-navigation.png` | Focus state or navigation result |
| `form-check.png` | Form label/instruction result |
| `contrast-check.png` | Contrast measurement/result |

Do not create or submit illustrative screenshots as if they were captured from the target website.

## 6. Remediation approach
Prioritize issues that prevent users from completing essential tasks. Fixes should be small, testable and verifiable. Examples include adding keyboard handlers only when native HTML controls are insufficient, associating labels with inputs, providing meaningful alt text, adjusting foreground/background colors, and ensuring visible focus styles.

## 7. Architecture summary
The repository separates frontend code (`client`), backend code (`server`), documentation (`docs`) and automated checks (`tests`). This separation supports independent development, testing and maintenance. See `architecture.md`.

## 8. Conclusion
This repository provides the documentation structure and starter architecture for a focused accessibility audit. The audit becomes evidence-complete only after the live Lighthouse run, keyboard-only pass, actual findings, scores and screenshots are added.
