---
description: Mit dem Microsoft Installer können Benutzer Blöcke von Anwendungsfunktionen installieren und entfernen, die als Windows Installer Features bezeichnet werden.
ms.assetid: 88268c5c-57c5-49f8-92df-1ad8f30a70c2
title: Angeben von Features
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cf7463b30247e921fb440ada1cd6f00f8e96a96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216351"
---
# <a name="specifying-features"></a>Angeben von Features

Mit dem Microsoft Installer können Benutzer Blöcke von Anwendungsfunktionen installieren und entfernen, die als [Windows Installer Features](windows-installer-features.md)bezeichnet werden. In diesem Abschnitt fügen Sie der-Installations Datenbank Informationen zu den Features hinzu, die für das Notepad-Beispiel verfügbar sind. Weitere Informationen finden Sie unter [Gruppe "Core Tables](core-tables-group.md) " und [Komponenten und Funktionen](components-and-features.md).

Das Notepad-Beispiel installiert Funktionen in einer Hierarchie von übergeordneten und untergeordneten Funktionen. In der folgenden Liste werden die untergeordneten Funktionen relativ zu ihrer übergeordneten Funktion eingezogen. Die Funktionen sollten in dieser Reihenfolge im [SelectionTree-Steuer](selectiontree-control.md) Element der Benutzeroberfläche (UI) angezeigt werden.

Editor

-   Infodatei
-   Hilfe

Tors

-   January
    -   Newyears

Sport

-   Ball
-   Verbandes

Grafiken

-   Konzert
-   Abhängigkeit

Öffnen Sie MNP2000.msi mit einem Datenbank-Editor, und geben Sie die folgenden Daten in die leere [Funktions Tabelle](feature-table.md)ein.



| Funktion  | Über \_ geordnetes Element | Titel         | BESCHREIBUNG                | Anzeige | Ebene | Verzeichnis\_ | Attribute |
|----------|-----------------|---------------|----------------------------|---------|-------|-------------|------------|
| Grafiken     |                 | Grafiken          | Kunstveranstaltungen im red Park.   | 20      | 3     | Notepaddir  | 0          |
| Ball | Sport           | Ball      | Baseball Spiele             | 17      | 3     | Sportdir    | 32         |
| Konzert  | Grafiken            | Konzert       | Konzertveranstaltungen im roten Park | 21      | 3     | Argsdir     | 2          |
| Abhängigkeit    | Grafiken            | Abhängigkeit         | Tanz Ereignisse im red Park   | 23      | 3     | Argsdir     | 2          |
| Verbandes | Sport           | Verbandes      | Fußballspiele             | 19      | 3     | Sportdir    | 2          |
| Tors     |                 | Tors          | Zulassung von Red Park      | 6       | 3     | Notepaddir  | 0          |
| Hilfe     | Editor         | Hilfe          | Hilfedatei.                 | 5       | 3     | Notepaddir  | 1          |
| January  | Tors            | January       | Januar-Zuweisungen         | 10      | 3     | Mondir      | 2          |
| Newyears | January         | Neuer Arbeitstag | Eintritts Zeit für neue Jahre   | 11      | 3     | Holdir      | 2          |
| Editor  |                 | Editor       | Editor für Notepad             | 1       | 3     | Notepaddir  | 0          |
| Infodatei   | Editor         | Infodatei        | Infodatei                | 3       | 3     | Notepaddir  | 0          |
| Sport    |                 | Sport Veranstaltungen  | Sport Veranstaltungen im roten Park   | 14      | 3     | Notepaddir  | 0          |



 

[Fortsetzen](specifying-feature-component-relationships.md)

 

 



