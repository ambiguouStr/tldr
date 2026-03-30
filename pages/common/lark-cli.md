# lark-cli

> Command-line interface for the Lark/Feishu open platform API.
> Supports documents, calendars, messaging, wikis, and more.
> More information: <https://github.com/larksuite/cli>.

- Initialize configuration with an app ID and secret:

`lark-cli config init`

- Log in as a user with recommended permissions (opens browser for OAuth):

`lark-cli auth login --recommend`

- Log in with additional specific permissions:

`lark-cli auth login --scope "{{search:docs:read}}"`

- Search documents:

`lark-cli docs +search --query "{{keyword}}" --as user`

- Fetch a document's content as Markdown:

`lark-cli docs +fetch --doc {{token_or_url}} --as user`

- Create a new document in a folder:

`lark-cli docs +create --title "{{title}}" --folder-token {{folder_token}} --markdown "{{content}}" --as user`

- Update an existing document (overwrite all content):

`lark-cli docs +update --doc {{token_or_url}} --mode overwrite --markdown "{{content}}" --as user`

- Make a raw API call:

`lark-cli api {{GET|POST|PUT|DELETE}} {{/open-apis/path}} --as {{user|bot}} --params '{{"key": "value"}}'`
