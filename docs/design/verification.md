# Verification Strategy

## Critical behaviors

- A changed source becomes visible through the content-loading path.
- Search results lead to the correct page and section.
- Malformed content produces an understandable error.
- Long documents retain coherent headings, navigation and readable code examples.

## Test layers

| Layer | Focus |
|---|---|
| Unit | Domain rules, validation and state changes without live external dependencies. |
| Integration | Consistency across application services and their storage or external-service adapters. |
| User journey | A complete path from a user action to its visible outcome, including failure states. |

## Environment checks

The portal provides documentation and guidance; it does not execute remote administration commands.
