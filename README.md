# 🌟 Amphora Starred Repositories

This repository serves as a comprehensive backup and documentation of all repositories starred by [@KingRwaz](https://github.com/KingRwaz) on GitHub. It includes both streamlined and detailed JSON exports for easy browsing and analysis.

## 📊 Repository Contents

### Files

- **`starred_repos_streamlined.json`** - Essential information about each starred repository
  - Repository name, owner, URL, and description
  - Lightweight and easy to parse
  - Best for: Quick browsing and list compilation

- **`starred_repos_detailed.json`** - Comprehensive metadata for each repository
  - Includes stars count, language, license, topics, creation date, last push time
  - Full repository statistics and metadata
  - Best for: Analysis, categorization, and detailed research

### Quick Stats

- **Total Repositories**: 500+
- **Last Updated**: 2026-06-29
- **Update Frequency**: Periodic updates (typically monthly)
- **Access**: All repositories linked to their GitHub URLs

## 🎯 Usage

### Viewing in Browser

1. Open either JSON file directly in GitHub's interface
2. Use [JSONCrush](https://www.jsoncrush.com/) for better visualization
3. Search for repositories by name using `Ctrl+F`

### Parsing with Code

**Python Example:**
```python
import json

# Load streamlined version
with open('starred_repos_streamlined.json', 'r') as f:
    repos = json.load(f)

# Get all repo names
repo_names = [repo['name'] for repo in repos['repositories']]
print(f"Total repos: {len(repo_names)}")
```

**JavaScript Example:**
```javascript
fetch('starred_repos_detailed.json')
  .then(r => r.json())
  .then(data => {
    console.log(`Total repos: ${data.repositories.length}`);
    console.log(`Languages: ${Object.keys(data.stats.by_language)}`);
  });
```

## 📈 Statistics

The detailed JSON includes:

- **By Language**: Distribution of repositories across programming languages
- **By Owner Type**: Organizations vs Individual Users
- **By Topic**: Categories and tags used in repositories
- **Top Repositories**: Highest starred repositories in the collection

## 🔄 Update Workflow

This repository is updated periodically to reflect the latest starred repositories. Updates are typically done:

- **Monthly**: Full comprehensive refresh
- **On Demand**: When major changes occur
- **Automated**: Via GitHub Actions (optional - can be configured)

### How to Update

1. Run the starred repos collection script
2. Generate fresh JSON files
3. Push updates to this repository
4. Version control tracks all changes

## 🛠️ Using with Other Tools

### Import into Tools

- **Notion**: Copy JSON data and use database import
- **Google Sheets**: Use JSON import add-on
- **Datadog**: Set up as a custom metric source
- **Your Own App**: Use the JSON as a data source
- **Excel**: Import JSON and convert to table format

### Search & Filter

To find specific repositories using command line tools:

```bash
# Search by name (using jq)
jq '.repositories[] | select(.name | contains("ai"))' starred_repos_detailed.json

# Filter by language
jq '.repositories[] | select(.language == "Python")' starred_repos_detailed.json

# Find most-starred
jq '.repositories | sort_by(.stargazers_count) | reverse | .[0:10]' starred_repos_detailed.json

# Count by language
jq '.repositories | group_by(.language) | map({language: .[0].language, count: length})' starred_repos_detailed.json
```

## 📋 File Formats

### Streamlined JSON Structure

```json
{
  "metadata": {
    "user": "KingRwaz",
    "total_repositories": 500,
    "generated_at": "2026-06-29",
    "note": "This file contains the first 500 starred repositories..."
  },
  "repositories": [
    {
      "id": 1197515131,
      "name": "awesome-design-md",
      "owner": "VoltAgent",
      "url": "https://github.com/VoltAgent/awesome-design-md",
      "description": "A collection of DESIGN.md files analysis by popular brand design systems...",
      "stargazers_count": 451,
      "language": "TypeScript"
    }
  ]
}
```

### Detailed JSON Structure

```json
{
  "metadata": {
    "user": "KingRwaz",
    "total_repositories": 500,
    "generated_at": "2026-06-29"
  },
  "repositories": [
    {
      "id": 1197515131,
      "name": "awesome-design-md",
      "owner": "VoltAgent",
      "full_name": "VoltAgent/awesome-design-md",
      "url": "https://github.com/VoltAgent/awesome-design-md",
      "description": "A collection of DESIGN.md files analysis...",
      "stargazers_count": 451,
      "language": "TypeScript",
      "license": {"key": "mit", "name": "MIT License"},
      "created_at": "2024-01-15",
      "pushed_at": "2026-06-28",
      "forks_count": 23,
      "open_issues_count": 5,
      "topics": ["design", "ai", "agents"],
      "homepage": "https://example.com",
      "is_archived": false,
      "is_fork": false,
      "visibility": "public"
    }
  ],
  "stats": {
    "by_language": {
      "Python": 145,
      "TypeScript": 98,
      "JavaScript": 67,
      "Go": 35,
      "Rust": 28
    },
    "by_owner_type": {
      "organizations": 156,
      "users": 344
    },
    "by_topic": {
      "ai": 89,
      "agent": 76,
      "opensource": 65
    }
  }
}
```

## 🔍 Repository Categories

Browse by interest area:

### 💡 AI & Agents
- AI coding agents and frameworks
- LLM tools and utilities
- Agent orchestration platforms
- Claude Code and Codex alternatives

### 🎨 Design & UI
- Design systems and components
- UI frameworks and libraries
- Design tools and plugins
- Icons and graphics collections

### 🛠️ Development Tools
- CLI tools and utilities
- Code editors and IDEs
- Build tools and bundlers
- Testing and debugging tools

### 📚 Open Source Collections
- Awesome lists and curated resources
- Documentation and guides
- Learning materials and tutorials
- Community-maintained datasets

### 🔒 Security & OSINT
- Penetration testing tools
- OSINT frameworks
- Security analysis tools
- Vulnerability scanners

### 📊 Data & Analytics
- Databases and data stores
- Data processing pipelines
- Analytics platforms
- Visualization tools

### 🚀 Infrastructure & DevOps
- Container and orchestration tools
- Cloud platforms
- Deployment automation
- Monitoring and logging

## 📞 Support & Contributions

This is a personal backup repository for tracking starred projects. To:

- **Report Issues**: Create an issue in this repository
- **Suggest Updates**: Open a pull request with improvements
- **View Original Stars**: Check [KingRwaz's starred repositories](https://github.com/KingRwaz?tab=stars)

## 📅 Update History

| Version | Date | Repositories | Changes |
|---------|------|--------------|---------|
| 1.0 | 2026-06-29 | 500+ | Initial release with comprehensive exports (pages 1-5) |

*Updates will be logged here as new versions are released*

## ⭐ How to Use This Repository

### For Personal Use
1. **Clone or Download** the repository
2. **Import JSON** into your preferred tool (Notion, Excel, custom app)
3. **Search and filter** repositories by category, language, or stars
4. **Track changes** by watching this repository

### For Development
1. **Parse the JSON** in your application
2. **Build tools** for analyzing repository trends
3. **Create dashboards** with repository statistics
4. **Automate workflows** based on repository metadata

### For Research
1. **Analyze trends** across programming languages
2. **Study repository patterns** in the starred collection
3. **Discover emerging technologies** and tools
4. **Track ecosystem growth** over time

## 🔗 Related Resources

- **My GitHub Profile**: [@KingRwaz](https://github.com/KingRwaz)
- **My Starred Repositories**: [View on GitHub](https://github.com/KingRwaz?tab=stars)
- **GitHub API Docs**: [REST API Documentation](https://docs.github.com/en/rest)
- **JSON Online Tools**: [JSONCrush](https://www.jsoncrush.com/), [JSON Formatter](https://jsonformatter.org/)

## 📝 Data Privacy & Licensing

- This repository contains metadata about **public** repositories only
- All linked repositories retain their original licenses
- Repository data is collected from public GitHub API
- This backup repository is released under **CC0 1.0 Universal** (public domain)

## 🎯 Future Enhancements

Potential features for future versions:

- [ ] Automated monthly updates via GitHub Actions
- [ ] Categorized index by technology/language
- [ ] Top 100 most-starred repositories list
- [ ] Repository trend analysis
- [ ] Filter by license type
- [ ] Web interface for browsing

---

**📌 Last Updated**: 2026-06-29  
**👤 Repository Owner**: [@KingRwaz](https://github.com/KingRwaz)  
**📄 License**: CC0 1.0 Universal (Public Domain)  
**⚡ Status**: Active - Regular Updates
