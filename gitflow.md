
### Gitflow Development
```mermaid

```

### Gitflow Infrastructure
```mermaid
gitGraph
    commit id:"Initial commit"
    commit id:"Release" tag:"1.0.0"

    branch develop
    checkout develop
    commit id:"Develop starts (long-lived)"

    branch "feature/alpha"
    checkout "feature/alpha"
    commit id:"Alpha work"
    commit id:"Alpha done"
    checkout develop
    merge "feature/alpha"

    branch "feature/beta"
    checkout "feature/beta"
    commit id:"Beta work"
    commit id:"Beta done"
    checkout develop
    merge "feature/beta"

    checkout main
    branch "hotfix/1.0.1"
    checkout "hotfix/1.0.1"
    commit id:"Hotfix changes"
    commit id:"Hotfix complete"

    checkout main
    merge "hotfix/1.0.1"
    commit id:"Release" tag:"1.0.1"

    checkout develop
    merge main
    commit id:"Develop synced with main (hotfix back-merge)"

```