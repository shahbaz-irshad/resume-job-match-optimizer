# Resume Job Match Optimizer

A portable [Agent Skills](https://agentskills.io/) workflow for analyzing a resume against a target job description (JD), identifying evidence-based gaps, estimating ATS alignment, and creating a truthful tailored resume.

The skill uses only the resume and JD supplied by the user. It does not claim access to an employer’s ATS, guarantee an interview, or invent skills, credentials, dates, outcomes, or metrics.

## What it does

- Compares the resume with required and preferred JD qualifications and responsibilities.
- Produces an explainable heuristic score with a 40% keyword, 30% structure, 20% impact, and 10% text/format breakdown.
- Identifies supported matches, requirements not evidenced in the resume, and prioritized improvements.
- Rewrites the resume when requested, preserves factual details, and rechecks the revised version against the same JD.
- Handles unreadable or incomplete inputs explicitly instead of guessing.

The score is an estimate, not a real ATS result, percentile, or hiring prediction. ATS systems and employer configurations vary. See [SKILL.md](./SKILL.md) for the full rubric and safeguards.

## Use it

Provide both a readable resume and the job description, then ask for the kind of help you want. For example:

- “Compare my resume with this job description and show the strongest matches and gaps.”
- “Tailor my resume to this role, keep every claim factual, and recheck the result.”
- “Review this resume for ATS readability. Do not rewrite it yet.”

If the agent cannot read the attachment, paste its text or provide a readable copy. The host AI tool must support access to uploaded files for attachment-based use; the skill itself does not grant file access.

## Install

### Claude.ai

1. Ensure **Code execution and file creation** (or **Create and edit files**) is enabled.
2. Zip the `resume-job-match-optimizer` folder so the ZIP contains the folder and its `SKILL.md`.
3. Open [Customize → Skills](https://claude.ai/customize/skills), choose **+ Create skill → Upload a skill**, and upload the ZIP.
4. Enable the skill in the Skills list.

See Anthropic’s current [Use skills in Claude](https://support.claude.com/en/articles/12512180-use-skills-in-claude) instructions for account and organization requirements.

### Claude Code on Windows

For a personal skill available across projects, copy or clone this repository so that `SKILL.md` is at:

`%USERPROFILE%\.claude\skills\resume-job-match-optimizer\SKILL.md`

For a repository-specific skill, place it at:

`<your-repository>\.claude\skills\resume-job-match-optimizer\SKILL.md`

Claude Code discovers skills from these folders. See the [Claude Code skills guide](https://code.claude.com/docs/en/skills) for current behavior and other installation options.

### Other Agent Skills-compatible tools

Use the host’s documented installation method for an Agent Skills folder. This package follows the open `SKILL.md` format, but support for particular metadata, automatic activation, file uploads, and document creation depends on each host.

## Privacy and limitations

The skill’s instructions do not guarantee local-only processing, control retention, or change the privacy practices of the AI host. Resume contents may include sensitive personal information; review the host’s privacy and file-handling terms before uploading. The skill does not use external research and should not inspect unrelated files.

## Repository contents

- `SKILL.md` — the complete portable skill instructions.
- `README.md` — this overview and installation guide.

## License

No license file is included. Public availability on GitHub does not by itself grant permission to reuse, modify, or redistribute this material. Add a license if you want to grant those permissions.