---
description: Die Windows-Benutzeroberfläche bietet Benutzern Zugriff auf eine Vielzahl von Objekten, die zum Ausführen von Anwendungen und verwalten des Betriebssystems erforderlich sind.
title: Entwicklerhandbuch für Shell
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 8f88ef25-3645-4f54-9453-41f919c0fc0a
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 7e6fbef1a8e34746d3b430faa5cb03f93613bc7c35e047cdd35afeb4921a37fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032298"
---
# <a name="shell-developers-guide"></a>Entwicklerhandbuch für Shell

Die Windows-Benutzeroberfläche bietet Benutzern Zugriff auf eine Vielzahl von Objekten, die zum Ausführen von Anwendungen und verwalten des Betriebssystems erforderlich sind. Die zahlreichsten und vertrautsten dieser Objekte sind die Ordner und Dateien, die sich auf Computerdatenträgern befinden. Es gibt auch eine Reihe von virtuellen Objekten, mit denen der Benutzer Aufgaben ausführen kann, z. B. das Senden von Dateien an Remotedrucker oder das Zugreifen auf die Papierkorb. Die Shell organisiert diese Objekte in einem hierarchischen Namespace und bietet Benutzern und Anwendungen eine konsistente und effiziente Möglichkeit, auf Objekte zuzugreifen und diese zu verwalten.

## <a name="in-this-section"></a>In diesem Abschnitt

-   [Sicherheitsüberlegungen: Microsoft Windows Shell](sec-shell.md)
-   [Leitfaden zum Implementieren von In-Process-Erweiterungen](shell-and-managed-code.md)
-   [Versionen von Shell und allgemeinen Steuerelementen](versions.md)
-   [Implementieren der grundlegenden Ordnerobjektschnittstellen](nse-implement.md)
-   [Implementieren eines benutzerdefinierten Dateiformats](customizing-file-types-bumper.md)
-   [Shellerweiterbarkeit (Erstellen einer Datenquelle)](shell-extensibility-bumper.md)
-   [Implementieren von Systemsteuerung Elementen](control-panel-applications.md)
-   [Unterstützen von Shellanwendungen](application-support-bumper.md)
-   [Themen zur Legacyshell](miscellaneous-topics-bumper.md)

## <a name="document-conventions"></a>Dokumentkonventionen

Das Shell Developers es Guide folgt den üblichen Windows SDK-Dokumentkonventionen (Software Development Kit). Es sollten insbesondere zwei Konventionen beachtet werden:

-   Der Beispielcode lässt normalen Fehlerkorrekturcode aus. Dieser Code wurde nur entfernt, um den Code lesbarer zu machen. Sie sollten den gesamten entsprechenden Fehlerkorrekturcode in Ihre eigenen Anwendungen einschließen.
-   Um Beispielregistrierungseinträge zu löschen, werden Schlüssel-, Unterschlüssel- und Eintragsnamen sowie Werte mit einer Standardschriftart angezeigt. Benutzerdefinierte oder anwendungsdefinierte Elementnamen werden italisiert.

 

 



