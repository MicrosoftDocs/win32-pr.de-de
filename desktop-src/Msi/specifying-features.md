---
description: Der Microsoft Installer ermöglicht Benutzern das Installieren und Entfernen von Anwendungsfunktionalitätsblöcken, die als Windows Installer-Features bezeichnet werden.
ms.assetid: 88268c5c-57c5-49f8-92df-1ad8f30a70c2
title: Angeben von Features
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8356020ce79881948b0886cfb83f634789f1ec9cfa55e7b150eb275ea1b81fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118624694"
---
# <a name="specifying-features"></a>Angeben von Features

Der Microsoft Installer ermöglicht Benutzern das Installieren und Entfernen von Anwendungsfunktionalitätsblöcken, die als Windows [Installer-Features bezeichnet werden.](windows-installer-features.md) In diesem Abschnitt fügen Sie der Installationsdatenbank Informationen zu den Funktionen hinzu, die für das Beispiel Editor sind. Weitere Informationen finden Sie unter [Kerntabellengruppe und](core-tables-group.md) [Komponenten und Funktionen](components-and-features.md).

Im Editor beispiel werden Features in einer Hierarchie von übergeordneten und untergeordneten Features installiert. In der folgenden Liste werden untergeordnete Features relativ zum übergeordneten Feature eingerückt. Die Features sollten in dieser Reihenfolge im [SelectionTree-Steuerelement der](selectiontree-control.md) Benutzeroberfläche angezeigt werden.

Editor

-   Infodatei
-   Hilfe

Gate

-   January
    -   NewYears

Sport

-   Baseball
-   Fußball

Kunst

-   Konzert
-   Tanz

Verwenden Sie einen Datenbank-Editor, um MNP2000.msi, und geben Sie die folgenden Daten in die leere [Featuretabelle ein.](feature-table.md)



| Komponente  | Übergeordnetes \_ Feature | Titel         | Beschreibung                | Anzeige | Ebene | Verzeichnis\_ | Attribute |
|----------|-----------------|---------------|----------------------------|---------|-------|-------------|------------|
| Kunst     |                 | Kunst          | Events in Red Park.   | 20      | 3     | NOTEPADDIR  | 0          |
| Baseball | Sport           | Baseball      | Baseball-Spiele             | 17      | 3     | SPORTDIR    | 32         |
| Konzert  | Kunst            | Konzert       | Concert events at Red Park | 21      | 3     | MEMODIR     | 2          |
| Tanz    | Kunst            | Tanz         | Sportereignisse in Red Park   | 23      | 3     | MEMODIR     | 2          |
| Fußball | Sport           | Fußball      | Football-Spiele             | 19      | 3     | SPORTDIR    | 2          |
| Gate     |                 | Gate          | Red Park es Admissions      | 6       | 3     | NOTEPADDIR  | 0          |
| Hilfe     | Editor         | Hilfe          | Hilfedatei.                 | 5       | 3     | NOTEPADDIR  | 1          |
| January  | Gate            | January       | Januar-Zulassungen         | 10      | 3     | MONDIR      | 2          |
| NewYears | January         | New Years Day | New Years Day Admissions   | 11      | 3     | HOLDIR      | 2          |
| Editor  |                 | Editor       | Editor Editor             | 1       | 3     | NOTEPADDIR  | 0          |
| Infodatei   | Editor         | Infodatei        | Readme-Datei                | 3       | 3     | NOTEPADDIR  | 0          |
| Sport    |                 | Sportereignisse  | Sportereignisse im Red Park   | 14      | 3     | NOTEPADDIR  | 0          |



 

[Fortsetzen](specifying-feature-component-relationships.md)

 

 



