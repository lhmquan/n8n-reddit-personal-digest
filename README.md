# n8n Reddit Personal Discussion Digest

A lightweight, strictly read-only self-hosted **n8n** workflow that fetches top posts and comment replies from selected subreddits to compile a personal daily reading list.

## Workflow Architecture
1. **Schedule Trigger**: Runs periodically (once or twice daily).
2. **Reddit Node (Get Many Posts)**: Reads recent posts from curated subreddits (limit: 15 posts).
3. **Reddit Node (Get Many Comments)**: Retrieves the comment tree and replies for selected discussions.
4. **Local Output**: Formats titles, comment context, and original Reddit permalinks into a personal reading workspace.

## Responsible Builder Policy Compliance
- **Read-Only**: Uses only GET operations (post:getAll, postComment:getAll). No automated posting, replying, voting, or messaging.
- **Low Volume**: Throttled execution well within Reddit API rate limits.
- **Personal Use Only**: No commercial data redistribution, bulk scraping, or AI/LLM model training.