# Password Strength Checker

A browser-based tool that rates how strong a password is, shows a colored strength bar, and estimates how long it would take to crack. Built with plain HTML, CSS, and JavaScript, with no libraries and nothing to install.

**Live demo:** https://fevenadane586-design.github.io/password-strength-checker/

## Features

- Strength score from 1 to 5 with a colored bar (red to green)
- Rule-based scoring: length, upper and lower case letters, numbers, symbols
- Detects common passwords and keyboard patterns (for example `password`, `qwerty`, `123qwe`) and caps their score
- Estimated time to crack, based on length and character variety
- Show/hide password checkbox
- Runs fully in the browser: the password is never sent anywhere or stored

## How it works

**Scoring.** The password earns one point for each rule it passes: at least 8 characters, at least 12 characters, both upper and lower case, a number, and a symbol.

**Common password check.** If the password contains a known weak pattern, the score is capped at 2 out of 5, no matter how many rules it passes. Attackers try common words and patterns first, so these passwords are weak even when they look complex.

**Crack time.** The tool estimates the number of possible combinations from the password length and the character types used, then divides by an assumed 10 billion guesses per second.

## What I learned

- How password strength depends on length and unpredictability, not just on character types
- Why rule-based checkers can be fooled by predictable patterns, such as `123qweASD##`
- How to use JavaScript to react to user input and update the page
- How to publish a project with GitHub Pages

## Limitations and future improvements

- The common-password list is small. A better version would check against a larger list.
- The crack-time estimate is simplified and assumes random characters.
- Planned: breach check using the Have I Been Pwned API (k-anonymity), and a passphrase generator.

## Run it locally

Download `index.html` and open it in any browser.

## License

MIT
