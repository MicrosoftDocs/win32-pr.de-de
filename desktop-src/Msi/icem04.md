---
description: ICEM04 überprüft, ob die erforderlichen leeren Tabellen des Mergemoduls leer sind. Fehler beim Beheben eines Fehlers, dass ICEM04-Berichte zu einer falschen Zusammenführung des Mergemoduls führen können.
ms.assetid: c6f64f5e-be65-485b-8831-e377535bd335
title: ICEM04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8388cbccd576b89a70716dd7c2ca6c82ac49fb30c8c39776904753de00b68dba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050160"
---
# <a name="icem04"></a>ICEM04

ICEM04 überprüft, ob die erforderlichen leeren Tabellen des Mergemoduls leer sind. Fehler beim Beheben eines Fehlers, dass ICEM04-Berichte zu einer falschen Zusammenführung des Mergemoduls führen können.

## <a name="result"></a>Ergebnis

ICEM04 gibt einen Fehler aus, wenn die erforderlichen leeren Tabellen des Mergemoduls nicht leer sind.

## <a name="example"></a>Beispiel

ICEM04 sendet die folgenden Fehlermeldungen für ein Modul, das die angezeigten Datenbankeinträge enthält.

``` syntax
An empty FeatureComponents table is required in a Merge Module.

The Merge Module contains the 'ModuleInstallExecuteSequence' table. It 
must therefore have an empty 'InstallExecuteSequence' table.

Action 'CostInitialize' found in the AdvtExecuteSequence table. This 
table must be empty in a Merge Module
```

Die folgende Tabelle zeigt eine partielle [AdvtExecuteSequence-Tabelle.](advtexecutesequence-table.md)



| Aktion         | Sequenz |
|----------------|----------|
| CostInitialize | 1        |



 

In der folgenden Liste werden die Teilinhalte von MergeModule angezeigt:

-   ModuleInstallExecuteSequence
-   ModuleAdvtExecuteSequence
-   InstallUISequence

Das folgende Beispiel zeigt einen weiteren möglichen Fehler.

``` syntax
Feature-Component '[1].[2]' found in the FeatureComponents table. The 
FeatureComponents table must be empty in a Merge Module.
```

Wenn ein Mergemodul eine Modulsequenztabelle enthält, muss es die entsprechende leere Sequenztabelle enthalten, unabhängig davon, ob die Modulsequenztabelle leer ist oder nicht. Wenn das Mergemodul beispielsweise die [Tabelle ModuleAdminExecuteSequence](moduleadminexecutesequence-table.md)enthält, muss es auch eine leere AdminExecuteSequence-Tabelle enthalten.

Die [FeatureComponents-Tabelle](featurecomponents-table.md) ist in allen Mergemodulen erforderlich und muss leer sein.

Im folgenden Verfahren wird gezeigt, wie Sie Fehler beheben.

**So beheben Sie die Fehler**

1.  Fügen Sie dem Mergemodul eine leere [FeatureComponents-Tabelle](featurecomponents-table.md) hinzu.
2.  Fügen Sie dem Mergemodul eine leere [InstallExecuteSequence-Tabelle](installexecutesequence-table.md) hinzu.
3.  Entfernen Sie die Aktion "CostInitialize" aus der [Tabelle AdvtExecuteSequence.](advtexecutesequence-table.md)
    > [!Note]  
    > Diese Tabelle muss in einem Mergemodul leer sein. Aktionen sollten nur in der Tabelle ModuleAdvtExecuteSequence angezeigt werden.

     

## <a name="tables-used-during-execution"></a>Während der Ausführung verwendete Tabellen

Die folgende Liste identifiziert die Tabellen, die während der Ausführung verwendet werden:

-   [Tabelle "FeatureComponents"](featurecomponents-table.md)
-   \*Modulsequenztabellen und entsprechende \* Sequenztabellen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu Mergemodulen](about-merge-modules.md)
</dt> <dt>

[ICE-Referenz zum Mergemodul](merge-module-ice-reference.md)
</dt> </dl>

 

 



