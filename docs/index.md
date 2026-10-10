---
title: AI-Sandbox rclone
---

# AI-Sandbox rclone

Diese Seite beschreibt eine private Google-OAuth-Anwendung für die Software [rclone](https://rclone.org/).

## Wofür wird die Anwendung verwendet?

Über rclone verbindet der Betreiber seinen Google-Drive-Datenbestand mit einer selbst betriebenen Linux-Umgebung („AI-Sandbox“). So können Dateien für die persönliche Wissensverwaltung gelesen und, soweit autorisiert, erstellt, bearbeitet, verschoben oder gelöscht werden.

Diese Website dient nur der Information. Sie führt selbst keine Google-Anmeldung durch und verarbeitet keine Google-Drive-Dateien.

## Google-Drive-Berechtigungen

Die Anwendung nutzt Google OAuth für den Drive-Zugriff. Die konfigurierte rclone-Ordnerwurzel begrenzt die im Mount sichtbaren Dateien, nicht den technischen Umfang des OAuth-Tokens.

Die Anwendung ist ausschließlich für den privaten Eigengebrauch vorgesehen.

## Datenschutz und Kontakt

Bitte lies die [Datenschutzerklärung](privacy.html). Fragen können über das [GitHub-Repository](https://github.com/ji79haxz/ai-sandbox-oauth/issues) gestellt werden.

*Dieses Projekt ist nicht offiziell mit Google, GitHub oder rclone verbunden.*
