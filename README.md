# NETWORKWALKS-EMMANUEL_EYO-B084-WK3-PM1-PM2-PASSWORD-CRACKING

## Week 3: Password Cracking with JtR and NetworkWalks Tools

Documentation and redacted evidence for the Week 3 password security tasks: Password Cracking with JtR and Password Cracking with NetworkWalks Tools. This repository is intended for authorized training labs and defensive learning.

> Screenshots in `evidence/` are shareable copies with recovered passwords, raw PDF hashes, and challenge flags obscured. The original evidence remains with the project owner. The locked practice PDFs and wordlists are intentionally not included.

## Project overview

The project used three provided password-protected PDF practice files to explore password recovery in a controlled course environment. The two parts were:

1. **John the Ripper (JtR) and Johnny:** extract a PDF hash with `pdf2john`, test the course-provided sample in the local password-auditing setup, and verify the result by opening the corresponding practice PDF.
2. **NetworkWalks tools:** use the NetworkWalks Hash Calculator to extract a hash from a practice PDF, then use the Password Cracker's dictionary attack workflow and verify the result against the practice file.

The screenshots show successful results in both workflows. The evidence index identifies what each redacted screenshot demonstrates. Exact recovered values and challenge flags are intentionally omitted from this public write-up.

## Safety and authorization

- Work only on systems and password hashes you own or have explicit written authorization to assess.
- Use intentionally created lab accounts and sample hashes. Never upload real password hashes, credentials, private keys, or personal data.
- Keep cracking work offline and within the lab scope. Do not use recovered passwords to access accounts or services.
- Stop if the target or scope is unclear. Report findings through the approved course or security process.
- Prefer long, unique passwords stored in a password manager, and enable multifactor authentication where available.

## Suggested repository layout

```text
password-security-lab-guide/
├── README.md
├── evidence/
│   └── README.md
└── .gitignore
```

## Part 1: John the Ripper (JtR)

John the Ripper is a password auditing tool. In a training lab, it can test whether deliberately weak sample passwords are guessable from their hashes. Follow your instructor's exact setup and commands; the steps below are a high-level record-keeping guide, not a target-specific cracking recipe.

### Record your workflow

1. **Define scope:** write down the lab machine, authorized account or provided sample, and the task objective.
2. **Prepare a harmless sample:** use a course-provided test hash or create a disposable local test account. Do not use a production credential.
3. **Identify the hash format:** use the lab instructions and JtR's supported-format documentation. Record the format and why it applies.
4. **Run only the assigned audit:** use the provided wordlist or rules within the lab. Record the command at a level approved by your course; redact sensitive paths or values.
5. **Review the result:** note whether a sample was recovered, the elapsed time if shown, and the limits of that result. A missed password does not prove it is strong.
6. **Clean up:** remove temporary lab files and reset disposable credentials when the exercise is complete.

### Findings to explain

- A hash is a one-way representation used to verify a password; it is not encryption that should be reversed.
- Fast or outdated password-hashing schemes make guesses cheaper. Modern password storage should use a purpose-built, salted password-hashing scheme with appropriate work factors.
- A successful guess shows the sample was vulnerable to the tested guesses; it does not establish that other accounts are compromised.
- Defensive actions include unique long passwords, multifactor authentication, and modern password hashing with salts and suitable work factors.

## Part 2: NetworkWalks tools

The course workflow used the NetworkWalks **Hash Calculator** and **Password Cracker** on the supplied practice PDFs:

1. Select the PDF option in the Hash Calculator and choose a course-provided practice PDF.
2. Review the extracted PDF hash in the lab interface. Do not publish the hash or send it to unrelated online services.
3. Copy the hash into the Password Cracker's hash field and select the built-in or course-authorized wordlist.
4. Run the dictionary attack in the authorized course lab and record the result without including the recovered password in this public repository.
5. Verify the result by opening only the corresponding practice PDF locally.

The supplied evidence shows the NetworkWalks tool's extracted-hash screen, dictionary-attack progress and successful match, plus course completion screens. Values that could expose the practice credentials or challenge answers have been redacted from public copies.

## Evidence screenshots

The redacted screenshots are listed in [`evidence/README.md`](evidence/README.md). They show the JtR/Johnny results and NetworkWalks hash and dictionary-attack workflow.

Before sharing, check every screenshot for passwords, hashes, tokens, email addresses, usernames, private IPs/hostnames, browser profile details, and unrelated personal information. Crop or redact sensitive content while preserving enough context to verify the task. Keep original evidence privately if your course requires it.

## Reproduction and tools

Install tools only from their official sources and follow the license and course requirements. Versions and commands can vary by operating system and JtR build; record the versions used in your lab notes. No passwords, hash dumps, wordlists, or cracking scripts are included in this repository.

## Reflection

The exercises demonstrated that simple dictionary guesses can recover weak passwords protecting documents. A successful test is evidence about the tested sample and wordlist, not a measure of security for other accounts. For real data, use strong unique passwords, store them in a password manager, and protect important accounts with multifactor authentication. Organizations should use modern salted password-hashing schemes for account passwords and review any exposure through approved incident-response processes.

## License

Unless you add a license file, all rights are reserved by the repository owner. Only publish screenshots and materials you have the right to share.
