---
description: Die Windows-Benutzeroberfläche ermöglicht Benutzern den Zugriff auf eine Vielzahl von Objekten, die zum Ausführen von Anwendungen und zum Verwalten des Betriebssystems erforderlich sind.
title: Shellentwickler Handbuch
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 8f88ef25-3645-4f54-9453-41f919c0fc0a
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 1be17ca90b7138294be3e1b34fa3fcb4dcb4227a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104993854"
---
# <a name="shell-developers-guide"></a>Shellentwickler Handbuch

Die Windows-Benutzeroberfläche ermöglicht Benutzern den Zugriff auf eine Vielzahl von Objekten, die zum Ausführen von Anwendungen und zum Verwalten des Betriebssystems erforderlich sind. Die häufigsten und vertrauten Objekte sind die Ordner und Dateien, die sich auf Computer Laufwerken befinden. Es gibt auch eine Reihe von virtuellen Objekten, die es dem Benutzer ermöglichen, Aufgaben auszuführen, z. b. das Senden von Dateien an Remote Drucker oder den Zugriff auf den Papierkorb. Die Shell organisiert diese Objekte in einem hierarchischen Namespace und bietet Benutzern und Anwendungen eine konsistente und effiziente Möglichkeit, auf Objekte zuzugreifen und diese zu verwalten.

## <a name="in-this-section"></a>In diesem Abschnitt

-   [Überlegungen zur Sicherheit: Microsoft Windows Shell](sec-shell.md)
-   [Leitfaden für die Implementierung von In-Process-Erweiterungen](shell-and-managed-code.md)
-   [Versionen der Shell und der allgemeinen Steuerelemente](versions.md)
-   [Implementieren der grundlegenden Ordner Objekt Schnittstellen](nse-implement.md)
-   [Implementieren eines benutzerdefinierten Datei Formats](customizing-file-types-bumper.md)
-   [Shellerweiterbarkeit (Erstellen einer Datenquelle)](shell-extensibility-bumper.md)
-   [Implementieren von System Steuerungselementen](control-panel-applications.md)
-   [Unterstützen von Shellanwendungen](application-support-bumper.md)
-   [Legacy-shellthemen](miscellaneous-topics-bumper.md)

## <a name="document-conventions"></a>Dokument Konventionen

Das shellentwickler Handbuch befolgt die üblichen Dokument Konventionen des Windows Software Development Kit (SDK). Insbesondere müssen zwei Konventionen beachtet werden:

-   Der Beispielcode lässt normalen Fehlerkorrektur Code aus. Dieser Code wurde nur entfernt, um den Code lesbarer zu machen. Sie sollten den entsprechenden Fehlerkorrektur Code in Ihre eigenen Anwendungen einschließen.
-   Um Beispiel Registrierungseinträge zu löschen, werden Schlüssel, Unterschlüssel und Eintrags Namen sowie Werte mit einer Standard Schriftart angezeigt. Benutzer-oder Anwendungs definierte Elementnamen werden kursiv formatiert.

 

 



