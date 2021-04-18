---
description: ICEM03 überprüft, ob alle Aktionen im Modul entweder Basis Aktionen sind oder von einer gültigen Basis Aktion abgeleitet werden.
ms.assetid: 8e2b5921-32cf-45e8-9906-30002574a712
title: ICEM03
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f368fa50a71153c41eebaa9ee5084449cf824993
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106368807"
---
# <a name="icem03"></a>ICEM03

ICEM03 überprüft, ob alle Aktionen im Modul entweder Basis Aktionen sind oder von einer gültigen Basis Aktion abgeleitet werden.

Das Mergemodul "ICES" wird in der Datei "Merge Module. Cub" mit dem Namen "Mergemod. Cub" und nicht in der CUB-Datei gespeichert, die die für die Paketüberprüfung verwendeten Verb

## <a name="result"></a>Ergebnis

ICEM03 veröffentlicht die Fehlermeldungen für ein Modul, das Aktionen in einer Sequenz Tabelle enthält, bei der es sich nicht um eine Basis Aktion handelt oder die von einer gültigen Basis Aktion abgeleitet ist.

## <a name="example"></a>Beispiel

ICEM03 gibt die folgenden Fehlermeldungen für ein Modul mit den unten gezeigten Datenbankeinträgen aus.

``` syntax
The action 'Action1' in the 'ModuleInstallExecuteSequence' table is 
orphaned. It is not a valid base action and does not derive from a 
valid base action.
The action 'Action2' in the 'ModuleInstallExecuteSequence' table is 
orphaned. It is not a valid base action and does not derive from a 
valid base action.
```

[Moduleinstallexecutesequence-Tabelle](moduleinstallexecutesequence-table.md)



| Aktion  | Sequenz | Baseaction | Nach | Bedingung |
|---------|----------|------------|-------|-----------|
| Action1 |          | Action2    | 0     |           |
| Action2 |          | Action1    | 0     |           |



 

ICEM03 gibt Fehler für diese beiden Aktionen aus, da Sie als Basis Aktionen in der Tabelle moduleinstallexecutesequence aufeinander verweisen. Alle Aktionen in den Tabellen " [moduleadminuisequence](moduleadminuisequence-table.md)", " [moduleadminexecutesequence](moduleadminexecutesequence-table.md)", " [moduleadvtuisequence](moduleadvtuisequence-table.md)", " [moduleadvtexecutesequence](moduleadvtexecutesequence-table.md)", " [moduleinstalluisequence](moduleinstalluisequence-table.md)" und " [moduleinstallexecutesequence](moduleinstallexecutesequence-table.md) " müssen entweder Basis Aktionen sein oder ihre Position aus der Kombination einer anderen

Um diesen Fehler zu beheben, bestimmen Sie die Basis Aktionen für die beiden Aktionen. Fügen Sie einen Datensatz für die Basis Aktionen mit einer Standard Sequenznummer hinzu. Geben Sie für Action1 und Action2 die Basis Aktions Namen in der Spalte baseaction und in der Spalte after den Wert 0 oder 1 ein.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Eisverweis für Mergemodul](merge-module-ice-reference.md)
</dt> </dl>

 

 



