# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

A static, single-file login page with no build process, no package manager, and no dependencies beyond Bootstrap 5.3.3 loaded via CDN.

## Running the Project

Open `index.html` directly in a browser — there is no dev server, build step, or install command. There are no tests or linters configured.

## Architecture

Everything lives in a single file: `index.html` contains all HTML structure, CSS (in a `<style>` block), and JavaScript (in a `<script>` block). There is no separation into external `.css` or `.js` files.

**Key implementation details:**
- Bootstrap 5.3.3 is loaded from CDN for form and button styling; all other styles are inline
- The form (`id="loginForm"`) uses `event.preventDefault()` and currently shows credentials in an `alert()` — there is no backend or real authentication
- Background uses a CSS linear gradient (`#273c75` → `#487eb0`)

## Conventions

- Keep all code in `index.html` unless explicitly restructuring into separate files
- Bootstrap utility classes handle layout; custom CSS in the `<style>` block handles the visual design (gradient, container sizing)
- The project targets modern browsers; no transpilation or polyfills are used
