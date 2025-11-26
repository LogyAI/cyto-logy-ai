# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a static website project for cyto.logy.ai, a server startup/status page that handles AWS Lambda instance wake-up functionality. The project consists of a single HTML file that serves as a loading screen while the main server boots up.

## Architecture

- **Frontend**: Single-page application built with vanilla HTML, CSS, and JavaScript
- **Deployment**: Static hosting via GitHub Pages (configured with CNAME for cyto.logy.ai domain)
- **Infrastructure**: Integrates with AWS Lambda at `qecietn55i.execute-api.us-east-1.amazonaws.com` to wake up the main server

## Key Files

- `index.html`: Main startup page with progress tracking and server status checking
- `CNAME`: Domain configuration for GitHub Pages hosting
- `README.md`: Basic project description

## Development

This is a static site with no build process, package dependencies, or test suite. Changes can be made directly to `index.html` and deployed via git push to the main branch.

## Main Functionality

The startup page:
1. Checks if the target server (cyto.logy.ai) is already online
2. If offline, triggers the AWS Lambda wake-up endpoint
3. Displays progress bar and status updates during 2-minute startup window
4. Polls the target server every 5 seconds until it comes online
5. Redirects to the main site once the server is responsive

## Deployment

Changes are automatically deployed via GitHub Pages when pushed to the main branch.