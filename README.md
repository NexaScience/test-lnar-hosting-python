# test-lnar-hosting-python

## 起動方法

### 1. 依存関係のインストール

```bash
uv sync
```

### 2. FastAPI サーバーを起動（ターミナル 1）

```bash
uvicorn api:app --reload
```

API ドキュメント: http://localhost:8000/docs

### 3. MCP サーバーを起動（ターミナル 2）

stdio transport（Claude Desktop / MCP Inspector などで使用）:

```bash
python mcp_server.py
```

または mcp CLI で起動:

```bash
mcp run mcp_server.py
```

### 4. MCP Inspector で動作確認

```bash
npx @modelcontextprotocol/inspector python mcp_server.py
```

## 環境変数

| 変数名 | 説明 | デフォルト値 |
|---|---|---|
| `API_BASE_URL` | FastAPI サーバーの URL | `http://localhost:8000` |
