---
description: Im folgenden Beispiel wird veranschaulicht, wie eine HTML-Datei am Ende einer Installation gestartet wird.
ms.assetid: 6b082559-bcfa-4098-b072-27ee78092833
title: Verwenden einer benutzerdefinierten Aktion zum Starten einer installierten Datei am Ende der Installation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 108ae06dae331660fe5c4f1ff8740a5fdb7e76f5eab27794fafcd7a4495296ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118141477"
---
# <a name="using-a-custom-action-to-launch-an-installed-file-at-the-end-of-the-installation"></a>Verwenden einer benutzerdefinierten Aktion zum Starten einer installierten Datei am Ende der Installation

Im folgenden Beispiel wird veranschaulicht, wie eine HTML-Datei am Ende einer Installation gestartet wird. Der Installer installiert die Komponente, die die Datei enthält, und veröffentlicht dann am Ende der Installation ein Steuerungsereignis, um eine benutzerdefinierte Aktion zum Öffnen der Datei ausführen zu können. Dieser Ansatz kann verwendet werden, um am Ende der ersten Installation einer Anwendung ein Hilfetutorial zu starten.

Das Beispiel muss die folgenden Spezifikationen erfüllen.

-   Der Installer führt die benutzerdefinierte [](f-gly.md) Aktion nur aus, wenn die vollständige Benutzeroberflächenebene zum Installieren einer Anwendung verwendet wird.
-   Der Installer führt die benutzerdefinierte Aktion nur aus, wenn die Komponente, die die HTML-Datei enthält, für die lokale Ausführung auf dem Computer installiert ist.
-   Die benutzerdefinierte Aktion wird nur bei der ersten Installation der Anwendung ausgeführt.
-   Die Installation schlägt nicht fehl, wenn die benutzerdefinierte Aktion fehlschlägt.

Das Beispiel enthält eine hypothetische Komponente namens Tutorial, die mindestens eine Ressource steuert, eine Datei namens tutorial.htm. Der Bezeichner für diese Datei in der Spalte Datei der Tabelle Datei ist Tutorial. Bei der folgenden Diskussion wird davon ausgegangen, dass Sie bereits die für das Tutorial erforderlichen Ressourcen erstellt und alle erforderlichen Einträge in den Tabellen [Feature](feature-table.md), [Component](component-table.md), [File](file-table.md), [Directory](directory-table.md)und [FeatureComponents](featurecomponents-table.md) vorgenommen haben, um diese Komponente zu installieren. Weitere Informationen finden Sie unter [Beispiel für eine Installation.](an-installation-example.md)

Die folgenden Themen enthalten Informationen zum Erstellen erforderlicher benutzerdefinierter Aktionen und zum Hinzufügen dieser Aktionen zu einem Installationspaket.

-   [Erstellen der benutzerdefinierten Aktion "Starten"](authoring-the-launch-custom-action.md)
-   [Hinzufügen von Launch zu CustomAction und Binärtabellen](adding-launch-to-the-customaction-and-binary-tables.md)
-   [Hinzufügen eines Steuerelementereignis am Ende der Installation zum Starten der Ausführung](adding-a-control-event-at-the-end-of-the-installation-to-run-launch.md)

 

 



