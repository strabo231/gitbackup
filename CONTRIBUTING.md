# Contributing to GitBackup

Thanks for your interest! 🎉

## Reporting Bugs

- Check existing issues first
- Include your OS and bash version
- Provide the command you ran
- Include error messages
- Describe expected vs actual behavior

## Suggesting Features

- Check if already suggested
- Explain the use case
- Describe how it would work
- Consider if it fits the project scope

## Pull Requests

1. Fork the repository
2. Create feature branch
3. Test thoroughly with real repos
4. Follow existing code style
5. Update README if needed
6. Submit PR with clear description

## Testing

```bash
# Test with sample repos
mkdir -p /tmp/test-repos/project1
cd /tmp/test-repos/project1
git init
echo "test" > file.txt
git add .
git commit -m "Initial commit"

# Test gitbackup
chmod +x gitbackup
./gitbackup scan /tmp/test-repos
./gitbackup list
./gitbackup backup -d /tmp/backup-test
```

## Code Style

- 4 spaces indentation
- Clear variable names
- Comment complex logic
- Follow existing patterns

## License

By contributing, you agree your contributions will be licensed under MIT.
