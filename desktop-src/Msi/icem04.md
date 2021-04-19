---
description: ICEM04 überprüft, ob die erforderlichen leeren Tabellen des Mergemoduls leer sind. Fehler beim Beheben eines Fehlers, der dazu führt, dass ICEM04 Berichte zu einer falschen Zusammenführung des Mergemoduls führen können.
ms.assetid: c6f64f5e-be65-485b-8831-e377535bd335
title: ICEM04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2ef993690ae690e0651db1538196998c4dd28c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356829"
---
# <a name="icem04"></a>ICEM04

ICEM04 überprüft, ob die erforderlichen leeren Tabellen des Mergemoduls leer sind. Fehler beim Beheben eines Fehlers, der dazu führt, dass ICEM04 Berichte zu einer falschen Zusammenführung des Mergemoduls führen können.

## <a name="result"></a>Ergebnis

ICEM04 gibt einen Fehler aus, wenn die erforderlichen leeren Tabellen des Mergemoduls nicht leer sind.

## <a name="example"></a>Beispiel

ICEM04 gibt die folgenden Fehlermeldungen für ein Modul aus, das die angezeigten Datenbankeinträge enthält.

``` syntax
An empty FeatureComponents table is required in a Merge Module.

The Merge Module contains the 'ModuleInstallExecuteSequence' table. It 
must therefore have an empty 'InstallExecuteSequence' table.

Action 'CostInitialize' found in the AdvtExecuteSequence table. This 
table must be empty in a Merge Module
```

In der folgenden Tabelle wird eine partielle [AdvtExecuteSequence-Tabelle](advtexecutesequence-table.md)gezeigt.



| Aktion         | Sequenz |
|----------------|----------|
| Costinitialize | 1        |



 

Die folgende Liste zeigt den partiellen Inhalt von Mergemodule:

-   Moduleinstallexecutesequence
-   Moduleadvtexecutesequence
-   InstallUISequence

Das folgende Beispiel zeigt einen anderen möglichen Fehler.

``` syntax
Feature-Component '[1].[2]' found in the FeatureComponents table. The 
FeatureComponents table must be empty in a Merge Module.
```

Wenn ein Mergemodul eine Modul Sequenz Tabelle enthält, muss es die entsprechende leere Sequenz Tabelle enthalten, unabhängig davon, ob die Modul Sequenz Tabelle leer ist. Wenn das Mergemodul z. b. die [moduleadminexecutesequence-Tabelle](moduleadminexecutesequence-table.md)enthält, muss es auch eine leere AdminExecuteSequence-Tabelle enthalten.

Die [FeatureComponents-Tabelle](featurecomponents-table.md) ist in allen Mergemodulen erforderlich und muss leer sein.

Im folgenden Verfahren wird gezeigt, wie Sie Fehler beheben.

**So beheben Sie die Fehler**

1.  Fügen Sie dem Mergemodul eine leere [FeatureComponents-Tabelle](featurecomponents-table.md) hinzu.
2.  Fügen Sie dem Mergemodul eine leere [InstallExecuteSequence-Tabelle](installexecutesequence-table.md) hinzu.
3.  Entfernen Sie die Aktion "costinitialize" aus der [Tabelle "AdvtExecuteSequence](advtexecutesequence-table.md)".
    > [!Note]  
    > Diese Tabelle muss in einem Mergemodul leer sein. Aktionen sollten nur in der Tabelle "moduleadvtexecutesequence" angezeigt werden.

     

## <a name="tables-used-during-execution"></a>Während der Ausführung verwendete Tabellen

In der folgenden Liste sind die Tabellen aufgeführt, die während der Ausführung verwendet werden:

-   [FeatureComponents-Tabelle](featurecomponents-table.md)
-   Modul \* Sequenz Tabellen und entsprechende \* Sequenz Tabellen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu Mergemodulen](about-merge-modules.md)
</dt> <dt>

[Eisverweis für Mergemodul](merge-module-ice-reference.md)
</dt> </dl>

 

 



