---
description: Sie können steuern, welche featureinstallationsoptionen für Benutzer und Anwendungen verfügbar sind, indem Sie die Featuretabelle und die Komponenten Tabelle erstellen.
ms.assetid: 3ce441e0-e709-415c-af64-b1ded7b04f6b
title: Steuern von Funktionsauswahl Zuständen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fadedf4b6038f8257d06671e0774afc258391898
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218204"
---
# <a name="controlling-feature-selection-states"></a>Steuern von Funktionsauswahl Zuständen

Sie können steuern, welche featureinstallationsoptionen für Benutzer und Anwendungen verfügbar sind, indem Sie die [Featuretabelle](feature-table.md) und die [Komponenten Tabelle](component-table.md)erstellen.

-   Um die Auswahl des Ankündigungs Status für eine Funktion zu verhindern, schließen Sie " **msidbfeatureattributesdisallowankündigungs** " in das Feld "Attribute" der Funktion in der [Featuretabelle](feature-table.md)ein.
-   Um zu verhindern, dass die Zustände "Run-From-Source" oder "run-from-Network" für eine Funktion ausgewählt werden, schließen Sie " **msidbcomponentattributeslocalonly** " in die Attribute-Felder in der [Komponenten Tabelle](component-table.md) für jede Komponente ein, die zur Funktion gehört. Wenn für eine Funktion keine Komponenten vorhanden sind, sind in der Funktion immer die Optionen "ausführen" und "ausführen-aus" für den Computer verfügbar.
-   Um die Auswahl des Status "Run-From-My-Computer" für eine Funktion zu verhindern, schließen Sie " **msidbcomponentattributessourceonly** " in die Attribute-Felder in der [Komponenten Tabelle](component-table.md) für jede Komponente ein, die zur Funktion gehört. Wenn für eine Funktion keine Komponenten vorhanden sind, sind in der Funktion immer die Optionen "ausführen" und "ausführen-aus" für den Computer verfügbar.
-   Neue untergeordnete Funktionen können erstellt werden, indem " **msidbfeatureattributesfollowparent** " und " **msidbfeatureattributesuidisallowmissing** " in das Feld "Attribute" der [Funktions Tabelle](feature-table.md)eingeschlossen werden.

 

 



