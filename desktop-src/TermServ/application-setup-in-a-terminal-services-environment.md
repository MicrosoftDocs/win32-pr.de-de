---
title: Anwendungseinrichtung
description: Durch die Installation einer Anwendung für einen einzelnen Benutzer können Probleme in einer mehr Benutzer Remotedesktopdienste Umgebung entstehen.
ms.assetid: 3e60e95a-3580-48aa-a9f9-8fd899aa7fca
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58f3c53f2370f4123352489ac747546e3335c558
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316040"
---
# <a name="application-setup"></a>Anwendungseinrichtung

Das automatisierte Setup Verfahren für viele vorhandene Anwendungen setzt voraus, dass die Anwendung für einen einzelnen Benutzer installiert wird. In einer mehr Benutzer Remotedesktopdienste Umgebung kann diese Annahme folgende Probleme verursachen:

-   Wenn das Setup Verfahren die Registrierung und die Desktopumgebung nur für einen Benutzer aktualisiert, müssen zusätzliche Benutzer das gesamte Paket neu installieren, oder ein Administrator muss manuell Informationen aus der Registrierung und dem Desktop eines Benutzers an die anderen Benutzer kopieren.
-   Mit einigen Setup Verfahren können Sie die Anwendung zum Zeitpunkt der Installation anpassen, indem Sie Features ausschließen. Wenn der anfängliche Installer einen Teil der Anwendung ausschließt, müssen zusätzliche Benutzer die Anwendung neu installieren, um die ausgeschlossenen Features zu erhalten.

Um diese Probleme zu vermeiden, sollten beim Installieren einer Anwendung auf einem Remotedesktop-Sitzungshost-Server (RD-Sitzungshost) die folgenden Richtlinien beachtet werden:

-   Installieren Sie Anwendungen in der Standardbenutzer Umgebung, die allen Benutzern gemeinsam ist. Führen Sie vor dem Installieren der Anwendung den Befehl **Change user/install** Console aus, und führen Sie nach Abschluss der Installation den Befehl **Change user/execute** Console aus. Verwenden Sie ein Remotedesktopdienste Kompatibilitäts Skript für die-Installation.
-   Unterstützung der benutzerspezifischen Anpassung durch die Verwendung von Benutzerprofilen. Erstellen Sie hierzu ein Format für [Administrative Vorlagen Dateien](/previous-versions/windows/desktop/Policy/administrative-template-file-format) , damit ein Administrator die Registrierung so konfigurieren kann, dass die für die einzelnen Benutzer verfügbaren Features angezeigt werden. Die Anwendung kann dann zur Laufzeit Features aktivieren oder deaktivieren, abhängig von den Einstellungen in den Registrierungs Einstellungen des aktuellen Benutzers. Die Anwendung kann die Konfiguration pro Benutzer in der Registrierungs Struktur des **aktuellen HKEY-Benutzers** speichern und jedem Benutzer die Konfiguration der Anwendung entsprechend Ihren Einstellungen gestatten.

 

 