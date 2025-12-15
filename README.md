# GitBackup - Automated Git Repository Backup Manager

Never lose your code again! GitBackup automatically discovers and backs up all your git repositories with one command.

## Why GitBackup?

Every developer's nightmare: **"My hard drive died and I lost 3 months of work."**

- 🔍 **Auto-discovers** all git repos
- 💾 **One-command backups** to external drives
- ⚡ **Incremental** - only backup what changed
- ⚠️ **Detects uncommitted changes**
- 📦 **Compression** - save space
- 📊 **Status tracking**
- 📝 **Backup logs**

## Installation

```bash
curl -sSL https://raw.githubusercontent.com/strabo231/gitbackup/main/install.sh | bash
```

## Quick Start

```bash
# Scan your projects
gitbackup scan ~/Projects ~/Work

# See what was found
gitbackup list

# Backup to external drive
gitbackup backup -d /media/backup --compress

# Check status
gitbackup status
```

## Commands

**Scan for repos:**
```bash
gitbackup scan ~/Projects
```

**List tracked repos:**
```bash
gitbackup list
```

**Backup all repos:**
```bash
gitbackup backup -d /media/backup --compress
gitbackup backup -d /media/backup --incremental  # Only changed repos
```

**Check status:**
```bash
gitbackup status  # Shows uncommitted changes, etc.
```

**Restore:**
```bash
gitbackup restore /media/backup/myproject.tar.gz ~/restored
```

**View history:**
```bash
gitbackup log
```

## Use Cases

**Daily backup:**
```bash
gitbackup backup -d /media/usb --incremental
```

**Weekly full backup:**
```bash
gitbackup backup -d /mnt/nas/backups --compress
```

**Setup cron:**
```bash
# Daily at 6 PM
crontab -e
0 18 * * * gitbackup backup -d /media/backup --incremental
```

## Features

✅ Auto-discovers git repos recursively  
✅ Detects uncommitted work  
✅ Incremental backups (only changed repos)  
✅ Compressed archives (.tar.gz)  
✅ Smart filtering (skips node_modules, venv, etc.)  
✅ Backup logs with timestamps  
✅ Restore from backups  
✅ Status overview  

## Command Reference

```
scan <dir>              Find git repos
list                    List tracked repos
backup -d <dest>        Backup all repos
  --compress            Create .tar.gz
  --incremental         Only changed repos
  --exclude <pattern>   Skip matching repos
status                  Show repo states
restore <file> [dest]   Restore backup
log                     Show history
```

## License

MIT License - see [LICENSE](LICENSE)

## Author

Sean - [@strabo231](https://github.com/strabo231)

---

**Don't risk losing your work. Backup your repos today.** 💾
