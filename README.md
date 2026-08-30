# Why Is This Repo Popular?

Understand the measurable signals behind a GitHub repository's popularity.

Enter a public GitHub repository and get a structured report based on its publicly available GitHub data.

**No AI. No fake statistics. No framework. No build step.**

## What it does

Why Is This Repo Popular? analyzes a repository using measurable signals such as:

- Stars
- Forks
- Contributors
- Open issues
- Commit activity
- Releases
- Repository age
- License information
- Topics
- Homepage metadata
- Recent repository activity

The result is presented as a **Popularity Score** with individual signal scores and supporting evidence.

## Why this exists

A repository having a large number of stars does not necessarily explain why it became popular.

Two repositories can have similar star counts while having completely different:

- Growth patterns
- Community participation
- Development activity
- Ecosystem adoption
- Documentation signals

This project makes those differences easier to understand.

## How the score works

The overall score is calculated from five deterministic signals:

```text
Popularity Score
│
├── Growth
├── Ecosystem
├── Community
├── Development
└── Documentation
```

Each signal produces a value from `0` to `100`.

The final score is the arithmetic mean:

```text
Overall Score =
(Growth + Ecosystem + Community + Development + Documentation) / 5
```

The project does **not** use AI to generate the score.

All calculations are performed in the browser using data returned by GitHub's public API.

## Signals

### Growth

Measures the relationship between the repository's current star count and its age.

A repository that accumulated many stars over a relatively short period can receive a stronger growth signal than an older repository with the same number of stars.

### Ecosystem

Uses fork activity and its relationship to repository popularity.

Forks can indicate that people are doing more than simply starring a project.

### Community

Uses publicly observable community signals including:

- Contributors
- Forks
- Stars
- Issues

### Development

Uses:

- Recent commit activity
- Release history
- Repository freshness
- Archived status

### Documentation

Uses available repository metadata including:

- Description
- Homepage
- Topics
- License
- GitHub Pages
- Wiki availability

## What the score does not mean

The Popularity Score is **not**:

- A measure of software quality
- A security rating
- A recommendation
- A measure of developer skill
- A prediction of future popularity
- An official GitHub ranking
- An AI-generated opinion

A score of `90` does not mean GitHub considers the repository "90% good."

It means the repository scored highly according to this project's scoring model.

## Data source

Repository information comes from the GitHub REST API.

The application only requests publicly available repository information.

No private repository data is required.

## Privacy

The application does not require a GitHub account.

It does not ask users for:

- GitHub passwords
- Personal access tokens
- Private repository credentials

Only a public repository URL is required.

## Technology

The project intentionally uses a small technology stack:

```text
HTML
CSS
JavaScript
GitHub REST API
Canvas
```

There is no React application, bundler, or framework.

The project is designed to run as a single HTML file.

## Running locally

Clone the repository:

```bash
git clone https://github.com/YOUR_USERNAME/YOUR_REPOSITORY.git
```

Open `index.html`, or serve the directory with a static HTTP server:

```bash
python -m http.server
```

Then open:

```text
http://localhost:8000
```

## GitHub API limits

The application uses GitHub's public API.

Unauthenticated requests are subject to GitHub's API rate limits.

When the API limit is reached, the application reports the failure rather than inventing or displaying fabricated data.

For larger deployments, a server-side API layer can be added.

## Design

The interface follows a **Neural Expressive** design approach.

The goal is not to make the interface flashy.

Instead, the data influences the visual hierarchy.

Strong signals become more prominent.

Numbers transition into their final values.

Charts progressively reveal information.

Sections appear as analysis becomes available.

Animations are short and purposeful.

The result is an analytical experience rather than a conventional dashboard.

## Principles

### Real data

Repository statistics should originate from GitHub.

### No fabricated information

The application should never present an invented statistic as real data.

### Explainable calculations

The scoring model should remain understandable and inspectable.

### Minimal technology

A useful tool does not need a large framework.

### Accessibility

The interface should remain usable with keyboard navigation, readable contrast, responsive layouts, and reduced-motion preferences.

## Contributing

Contributions are welcome.

Before opening a pull request:

1. Keep the project dependency-free where practical.
2. Avoid unnecessary frameworks.
3. Keep calculations deterministic.
4. Do not add fabricated metrics.
5. Keep the interface focused on repository analysis.
6. Test against multiple public repositories.
7. Consider GitHub API rate limits.

For larger changes, open an issue first to discuss the approach.

## License

This project is open source.

See `LICENSE` for the applicable license.

## Built by

**Fahad**

Built with curiosity, public data, and a preference for simple tools that actually do something useful.