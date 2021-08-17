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

Der Microsoft Installer ermöglicht Benutzern das Installieren und Entfernen von Anwendungsfunktionalitätsblöcken, die als [Windows Installerfunktionen](windows-installer-features.md)bezeichnet werden. In diesem Abschnitt fügen Sie der Installationsdatenbank Informationen zu den Features hinzu, die für das Editor-Beispiel verfügbar sind. Weitere Informationen finden Sie unter [Core Tables Group](core-tables-group.md) und Components and [Features](components-and-features.md).

Im Editor Beispiel werden Funktionen in einer Hierarchie von übergeordneten und untergeordneten Features installiert. In der folgenden Liste werden untergeordnete Features relativ zu ihrer übergeordneten Funktion eingerückt. Die Features sollten in dieser Reihenfolge im [SelectionTree-Steuerelement](selectiontree-control.md) der Benutzeroberfläche angezeigt werden.

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

Verwenden Sie einen Datenbank-Editor, um MNP2000.msi zu öffnen und die folgenden Daten in die leere [Featuretabelle](feature-table.md)einzugeben.



| Komponente  | \_Übergeordnetes Feature | Titel         | BESCHREIBUNG                | Anzeige | Ebene | Verzeichnis\_ | Attribute |
|----------|-----------------|---------------|----------------------------|---------|-------|-------------|------------|
| Kunst     |                 | Kunst          | Events in Red Park.   | 20      | 3     | NOTEPADDIR  | 0          |
| Baseball | Sport           | Baseball      | Baseball-Spiele             | 17      | 3     | SPORTDIR    | 32         |
| Konzert  | Kunst            | Konzert       | Concert events at Red Park | 21      | 3     | SIDEDIR     | 2          |
| Tanz    | Kunst            | Tanz         | Events in Red Park   | 23      | 3     | SIDEDIR     | 2          |
| Fußball | Sport           | Fußball      | Football-Spiele             | 19      | 3     | SPORTDIR    | 2          |
| Gate     |                 | Gate          | Eintritte in Red Park      | 6       | 3     | NOTEPADDIR  | 0          |
| Hilfe     | Editor         | Hilfe          | Hilfedatei.                 | 5       | 3     | NOTEPADDIR  | 1          |
| January  | Gate            | January       | Januar-Zulassungen         | 10      | 3     | MONDIR      | 2          |
| NewYears | January         | Neujahrstag | New Years Day Admissions   | 11      | 3     | HOLDIR      | 2          |
| Editor  |                 | Editor       | Editor Editor             | 1       | 3     | NOTEPADDIR  | 0          |
| Infodatei   | Editor         | Infodatei        | Readme-Datei                | 3       | 3     | NOTEPADDIR  | 0          |
| Sport    |                 | Sportereignisse  | Sportereignisse im Red Park   | 14      | 3     | NOTEPADDIR  | 0          |



 

[Fortsetzen](specifying-feature-component-relationships.md)

 

 



