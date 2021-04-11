---
description: Der Windows Installer bietet viele integrierte Aktionen für die Ausführung des Installationsvorgangs. Eine Liste dieser Aktionen finden Sie in der Referenz zu Standard Aktionen.
ms.assetid: 4a1f3ccc-4904-47d0-bfc6-013e404de47e
title: Benutzerdefinierte Aktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9623351bdcd4cd109d2112724d13e0f9ccaa6b2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042396"
---
# <a name="custom-actions"></a>Benutzerdefinierte Aktionen

Der Windows Installer bietet viele integrierte Aktionen für die Ausführung des Installationsvorgangs. Eine Liste dieser Aktionen finden Sie in der [Referenz zu Standard Aktionen](standard-actions-reference.md).

Standard Aktionen sind ausreichend, um in den meisten Fällen eine Installation auszuführen. Es gibt jedoch Situationen, in denen der Entwickler eines Installationspakets es zum Schreiben einer benutzerdefinierten Aktion findet. Beispiel:

-   Sie möchten eine ausführbare Datei während der Installation starten, die auf dem Computer des Benutzers installiert ist oder mit der Anwendung installiert wird.
-   Sie möchten spezielle Funktionen während einer Installation, die in einer Dynamic Link Library (dll) definiert sind, aufzurufen.
-   Sie möchten Funktionen verwenden, die in den Entwicklungs Sprachen Microsoft Visual Basic Scripting Edition oder literalskript Text von Microsoft JScript während einer Installation geschrieben wurden.
-   Sie möchten die Ausführung einiger Aktionen bis zu dem Zeitpunkt verzögern, zu dem das Installationsskript ausgeführt wird.
-   Sie möchten einem ProgressBar-Steuerelement und einem timeremainung-Text Steuerelement Zeit-und Fortschrittsinformationen hinzufügen.

In den folgenden Abschnitten werden benutzerdefinierte Aktionen beschrieben und erläutert, wie Sie in ein Installationspaket integriert werden:

-   [Informationen zu benutzerdefinierten Aktionen](about-custom-actions.md)
-   [Verwenden von benutzerdefinierten Aktionen](using-custom-actions.md)
-   [Referenz zu benutzerdefinierten Aktionen](custom-action-reference.md)
-   [Zusammenfassungs Liste aller benutzerdefinierten Aktions Typen](summary-list-of-all-custom-action-types.md)

 

 



