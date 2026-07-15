# SafePaste

**Catch sensitive information before it is sent online.**

SafePaste is a privacy-first Chrome extension that helps prevent accidental
sharing of API keys, access tokens, private keys, card numbers, and personal
information. It runs locally in your browser: scanned text does not leave your
device.

## What SafePaste does

- Warns when pasted or submitted text appears to contain sensitive data.
- Lets you redact selected values and review a redacted preview first.
- Adds a second confirmation for high-risk secrets.
- Lets you create personal "Never allow sending" rules for data that must
  never be submitted.
- Adds extra protection for common AI tools and support platforms.
- Supports organization-managed blocking rules through Chrome policies.

SafePaste helps reduce accidental disclosure. It does not replace secret
rotation, access controls, endpoint protection, or legal review.

## Privacy

SafePaste processes pasted text, form values, and selected text locally in the
browser. It does not collect pasted content, API keys, tokens, passwords,
private keys, form values, detection results, browsing history, or clipboard
history.

Read the full [Privacy Policy](PRIVACY.md).

## Plans

| Plan | Price | Includes |
| --- | ---: | --- |
| Free | €0 | Local warnings, basic detection, and anonymization. |
| Pro | €3.99/month | Personal never-send rules, custom patterns, and advanced local controls. |
| Team | Coming later | Central administration, seats, and policy synchronization. |

Pro payments are handled through ExtensionPay and Stripe. Team administration
currently works with Chrome policies; automated Team billing and an admin panel
are planned for a future release.

## For teams

IT administrators can enforce selected categories, such as API keys and
tokens, on managed Windows devices without accessing employee content. See the
[Team Windows Guide](docs/TEAM_WINDOWS_GUIDE.md).

## Help and security

- Product and setup questions: see [.github/SUPPORT.md](.github/SUPPORT.md).
- Security vulnerabilities: follow [SECURITY.md](SECURITY.md). Do not disclose
  secrets or customer data in a public issue.
- Bugs: use the [bug-report template](.github/ISSUE_TEMPLATE/bug_report.md)
  with sanitized examples only.

## Development

To test an unpublished build locally, run `npm.cmd run build`, open
`chrome://extensions`, enable Developer mode, choose **Load unpacked**, and
select the `dist` folder. Run `npm.cmd test` and `npm.cmd run lint` before
packaging a release with `npm.cmd run package`.

More details for maintainers are in [docs](docs/README.md), including the
[ExtensionPay and GitHub guide](docs/MONETIZATION_AND_GITHUB_GUIDE.md).

## License

SafePaste is proprietary software. See [LICENSE](LICENSE).
