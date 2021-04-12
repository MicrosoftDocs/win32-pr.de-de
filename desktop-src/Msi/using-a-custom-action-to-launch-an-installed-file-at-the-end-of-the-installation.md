---
description: Im folgenden Beispiel wird veranschaulicht, wie am Ende einer-Installation eine HTML-Datei gestartet wird.
ms.assetid: 6b082559-bcfa-4098-b072-27ee78092833
title: Verwenden einer benutzerdefinierten Aktion zum Starten einer installierten Datei am Ende der Installation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e5c039d58830ce6a01f76a0946bced474e5091b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216931"
---
# <a name="using-a-custom-action-to-launch-an-installed-file-at-the-end-of-the-installation"></a>Verwenden einer benutzerdefinierten Aktion zum Starten einer installierten Datei am Ende der Installation

Im folgenden Beispiel wird veranschaulicht, wie am Ende einer-Installation eine HTML-Datei gestartet wird. Das Installationsprogramm installiert die Komponente, die die Datei enthält, und veröffentlicht dann am Ende der Installation ein Steuerungs Ereignis, um eine benutzerdefinierte Aktion auszuführen, mit der die Datei geöffnet wird. Diese Vorgehensweise kann verwendet werden, um am Ende der ersten Installation einer Anwendung ein Hilfe-Tutorial zu starten.

Das Beispiel muss die folgenden Spezifikationen erfüllen.

-   Der Installer führt die benutzerdefinierte Aktion nur aus, wenn die [*vollständige Benutzer*](f-gly.md) Oberflächenebene zum Installieren einer Anwendung verwendet wird.
-   Das Installationsprogramm führt die benutzerdefinierte Aktion nur aus, wenn die Komponente, die die HTML-Datei enthält, für die lokale Ausführung auf dem Computer installiert ist.
-   Die benutzerdefinierte Aktion wird nur bei der ersten Installation der Anwendung ausgeführt.
-   Wenn die benutzerdefinierte Aktion fehlschlägt, schlägt die Installation fehl.

Das Beispiel enthält eine hypothetische Komponente mit dem Namen Tutorial, mit der mindestens eine Ressource, eine Datei mit dem Namen tutorial.htm, gesteuert wird. Der Bezeichner für diese Datei in der Spalte Datei der Dateitabelle ist Tutorial. In der folgenden Erläuterung wird davon ausgegangen, dass Sie bereits die für das Lernprogramm erforderlichen Ressourcen erstellt und alle erforderlichen Einträge in den Tabellen [Feature](feature-table.md), [Component](component-table.md), [File](file-table.md), [Directory](directory-table.md)und [FeatureComponents](featurecomponents-table.md) vorgenommen haben, um diese Komponente zu installieren. Weitere Informationen finden Sie unter [einem Installations Beispiel](an-installation-example.md).

Die folgenden Themen enthalten Informationen zum Erstellen erforderlicher benutzerdefinierter Aktionen und zum Hinzufügen zu einem-Installationspaket.

-   [Erstellen der benutzerdefinierten Aktion "starten"](authoring-the-launch-custom-action.md)
-   [Hinzufügen von Start zu den Tabellen CustomAction und Binary](adding-launch-to-the-customaction-and-binary-tables.md)
-   [Hinzufügen eines Steuerungs Ereignisses am Ende der Installation zum Ausführen des Starts](adding-a-control-event-at-the-end-of-the-installation-to-run-launch.md)

 

 



