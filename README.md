# Instaclone

## issues
에러
```json
{
  "errors": [
    {
      "message": "\nInvalid `prisma.movie.create()` invocation:\n\n\n  connect ECONNREFUSED ::1:50623",
      "locations": [
        {
          "line": 2,
          "column": 3
        }
      ],
      "path": [
        "createMovie"
      ],
      "extensions": {
        "code": "INTERNAL_SERVER_ERROR",
        "exception": {
          "code": "ECONNREFUSED",
          "clientVersion": "2.30.3",
          "stacktrace": [
            "Error: ",
            "Invalid `prisma.movie.create()` invocation:",
            "",
            "",
            "  connect ECONNREFUSED ::1:50623",
            "    at cb (/Users/hwang-isaac/dcs/nomad/apollo-instagram-clone-be/node_modules/@prisma/client/runtime/index.js:36494:17)",
            "    at processTicksAndRejections (node:internal/process/task_queues:95:5)"
          ]
        }
      }
    }
  ],
  "data": {
    "createMovie": null
  }
}
```

해결 : 최신버전의 prisma 적용
```bash
npm install @prisma/client@latest
npm install prisma@latest
npx prisma generate
npm run migrate
npm run dev
```