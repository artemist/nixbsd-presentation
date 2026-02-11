---
title: "NixBSD: A New Frontier for NixOS"
---

# NixBSD
## A New Frontier for NixOS

---

## About Us
* Artemis Tosini
* Audrey Dutcher
* TODO: More info

---

## What is NixBSD?
* Uses existing work on Nixpkgs
* Uses NixOS tooling, but modules must be ported

---

# Background

-v-

## What is BSD?
* Derived from original Unix
* FreeBSD, NetBSD, OpenBSD, and more
* Independent Kernels
* TODO: Maybe put BSD tree image here?

-v-

## Not Linux
* Versioned together
* Many programs in-tree
* Packages and base system separate

---

# Nix

-v-

## Why does it need work?
* Not if cross-compiling
* Garbage collector
* Sandboxed builds

-v-

## Garbage Collector
* Linux scans `/proc`
* FreeBSD uses `libproc`
* TODO: maybe add in print-roots output

-v-

# Sandboxing
* Linux has Namespaces
* FreeBSD has Jails
* Not exactly the same
* Jails want manual configuration

-v-

## Read-Only `/nix/store`
* Not implemented
* FreeBSD can't use Linux method
* Maybe make `/nix/rw-store` workaround?

---

# Nixpkgs

-v-

## FreeBSD Packaging

-v-

## Unwinder

-v-

## Bootstrapping

-v-

## Autotools, my behated
* Wants to know FreeBSD version
* May try to guess from builder system

-v-

## Updating FreeBSD

-v-

## Linux-specific packages
* Disable features on FreeBSD
* Replace packages with equivalents
    * `libudev-devd`

---

# NixOS

-v-

## What is NixOS
* `evalModules` to make settings map
* `system.build.toplevel` contains configuration
* `activate` on boot and switch
* `switch-to-configuration` for setup
* `boot.json` describes how to boot
-v-

## Init Systems
* NixOS needs systemd
* No FreeBSD System
* Replace with `rc`

-v-

## Bootloader
* FreeBSD has own bootloader
* Script to turn bootspec into lua

---

# Status

-v-

## Upstreaming
* Nix: Needs work
* Nixpkgs: Core parts done
* NixOS: Needs work and agreement

## Status Quo
* NixBSD maintenance challenging
* Core devs busy

---

# Future Steps

-v-

## Multi-init-system NixOS
* Modular Services: Merged, not used much 
* Portable Services: Idea
* Initware: Requires work
* Unit-to-rc script: Might work

-v-

## CA Derivations
* Would make NixBSD more usable
* Possible to work around

-v-

## Other OSes
* OpenBSD: Some work done
* NetBSD: Nixpkgs, but no NixBSD
* Illumos: Possible

---

# Demo

---

# Questions
