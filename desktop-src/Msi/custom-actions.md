---
description: Der Windows Installer bietet viele integrierte Aktionen zum Ausführen des Installationsprozesses. Eine Liste dieser Aktionen finden Sie in der Referenz zu Standardaktionen.
ms.assetid: 4a1f3ccc-4904-47d0-bfc6-013e404de47e
title: Benutzerdefinierte Aktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d3e2eb466934d7d332307e0d5288d6d328297d7664d884e62c406eb3409728a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947901"
---
# <a name="custom-actions"></a>Benutzerdefinierte Aktionen

Der Windows Installer bietet viele integrierte Aktionen zum Ausführen des Installationsprozesses. Eine Liste dieser Aktionen finden Sie in der [Referenz zu Standardaktionen.](standard-actions-reference.md)

Standardaktionen sind in den meisten Fällen ausreichend, um eine Installation auszuführen. Es gibt jedoch Situationen, in denen der Entwickler eines Installationspakets es für erforderlich hält, eine benutzerdefinierte Aktion zu schreiben. Beispiel:

-   Sie möchten eine ausführbare Datei während der Installation starten, die auf dem Computer des Benutzers oder mit der Anwendung installiert wird.
-   Sie möchten während einer Installation spezielle Funktionen aufrufen, die in einer Dynamic Link Library (DLL) definiert sind.
-   Sie möchten Funktionen verwenden, die während einer Installation in den Entwicklungssprachen Microsoft Visual Basic Scripting Edition oder Microsoft JScript Literalskripttext geschrieben wurden.
-   Sie möchten die Ausführung einiger Aktionen bis zum Zeitpunkt der Ausführung des Installationsskripts zurück verzögerungen.
-   Sie möchten einem ProgressBar-Steuerelement und einem TimeRemaining Text-Steuerelement Zeit- und Fortschrittsinformationen hinzufügen.

In den folgenden Abschnitten werden benutzerdefinierte Aktionen und deren Integration in ein Installationspaket beschrieben:

-   [Informationen zu benutzerdefinierten Aktionen](about-custom-actions.md)
-   [Verwenden benutzerdefinierter Aktionen](using-custom-actions.md)
-   [Referenz zu benutzerdefinierten Aktionen](custom-action-reference.md)
-   [Zusammenfassungsliste aller benutzerdefinierten Aktionstypen](summary-list-of-all-custom-action-types.md)

 

 



