# buf

Quick implementation of Buf as an enhancement to gRPC protocol buffers. See my schema registry for the two defined APIs here: https://buf.build/jack-hughes

Key files:
- https://github.com/jack-hughes/buf/blob/main/.github/workflows/pull-request.yaml
  - Detect breaking changes in proto before merge to main
- https://github.com/jack-hughes/buf/blob/main/.github/workflows/push.yaml
  - Detect breaking changes on merge to main
  - If no failures - push tag to BSR
- https://github.com/bufbuild/buf-tour/blob/main/finish/buf.gen.yaml
  - Managed, remote code generation. See docs: https://docs.buf.build/bsr/remote-generation
  - Output plugins, in this instance only Go is supported
- https://github.com/jack-hughes/buf/blob/main/buf.work.yaml
  - Workspace definitions to collate APIs
- https://github.com/jack-hughes/buf/blob/main/petapis/buf.yaml
  - Dependencies, breaking change config and linter config
- https://github.com/jack-hughes/buf/blob/main/petapis/buf.md
  - Markdown description for API on BSR
- https://github.com/jack-hughes/buf/blob/main/petapis/buf.lock
  - Dependency lock file
