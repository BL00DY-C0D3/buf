# Contributing to buf

Thank you for your interest in contributing to buf! This document provides guidelines and instructions for contributing.

## Getting Started

1. Fork the repository
2. Clone your fork: `git clone https://github.com/YOUR_USERNAME/buf.git`
3. Create a new branch: `git checkout -b feature/your-feature-name`

## Development Setup

### Dependencies

**For building:**
- gcc
- make

**For running:**
- mount/umount
- wipefs
- lsblk
- blockdev
- df
- parted
- 7z
- dosfstools
- ntfs-3g
- grub2-common/grub-pc-bin
- wget

### Installing Dependencies

```bash
# Ubuntu/Debian
sudo apt install build-essential parted dosfstools ntfs-3g grub2-common grub-pc-bin p7zip-full wget

# Arch Linux
sudo pacman -S base-devel parted dosfstools ntfs-3g grub p7zip wget

# Fedora/RHEL
sudo dnf install gcc make parted dosfstools ntfs-3g grub2-tools p7zip p7zip-plugins wget
```

### Building

```bash
make && make install
```

### Testing

After building, test with:
```bash
sudo buf -h
```

## Commit Message Guidelines

We use a commit message template to maintain consistent and meaningful commit history. To set it up:

```bash
git config commit.template .gitmessage
```

### Commit Message Format

```
<type>: <subject>

<body>

<footer>
```

**Types:**
- `feat`: A new feature
- `fix`: A bug fix
- `docs`: Documentation only changes
- `style`: Code style changes (formatting, missing semi colons, etc)
- `refactor`: Code changes that neither fix a bug nor add a feature
- `perf`: Performance improvements
- `test`: Adding or updating tests
- `build`: Changes to build system or dependencies
- `ci`: Changes to CI configuration
- `chore`: Other changes (maintenance, etc)

**Example:**
```
feat: Add support for ext4 filesystem

Added ext4 filesystem support for creating bootable USB drives.
This allows users to create bootable drives with ext4 instead of
being limited to FAT32 and NTFS.

Fixes #42
```

### Subject Line Guidelines

- Use imperative mood ("Add feature" not "Added feature" or "Adds feature")
- Keep it under 50 characters
- Don't end with a period
- Capitalize the first letter

## Code Style

- Follow the existing code style in the project
- Use meaningful variable and function names
- Add comments for complex logic
- Keep functions focused and small

## Pull Request Process

1. Update documentation if you're adding or changing functionality
2. Make sure your code compiles without errors
3. Test your changes thoroughly
4. Follow the commit message guidelines
5. Create a pull request with a clear title and description
6. Link any related issues in the PR description

## Questions?

Feel free to open an issue for any questions or concerns!
