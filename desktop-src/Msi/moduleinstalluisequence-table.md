---
description: Ein Mergetool wertet die Tabelle ModuleInstallUISequence aus und fügt dann die berechneten Aktionen mit einer richtigen Sequenznummer in die Tabelle InstallUISequence ein.
ms.assetid: a125aecc-57d9-4c8e-873e-d5315eaafa56
title: ModuleInstallUISequence-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bb8f2868fbad03439758cd45a79a71febb5e2a9b0b863c2ee9ea0597f5b112f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118945365"
---
# <a name="moduleinstalluisequence-table"></a>ModuleInstallUISequence-Tabelle

Ein Mergetool wertet die Tabelle ModuleInstallUISequence aus und fügt dann die berechneten Aktionen mit einer richtigen Sequenznummer in die [Tabelle InstallUISequence](installuisequence-table.md) ein.

Die Tabelle ModuleInstallUISequence enthält die folgenden Spalten.



| Spalte     | Typ                         | Key | Nullwerte zulässig |
|------------|------------------------------|-----|----------|
| Aktion     | [Identifier](identifier.md) | J   | N        |
| Sequenz   | [Integer](integer.md)       |     | J        |
| BaseAction | [Identifier](identifier.md) |     | J        |
| Danach      | [Integer](integer.md)       |     | J        |
| Bedingung  | [Condition](condition.md)   |     | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>Aktion
</dt> <dd>

Aktion, die in sequenziert eingefügt werden soll. Bezieht sich auf eine der Standardaktionen [des Installationsprogramms](standard-actions.md)oder auf einen Eintrag in der [CustomAction-Tabelle](customaction-table.md) oder Dialogtabelle des [Mergemoduls.](dialog-table.md)

Wenn eine [Standardaktion](standard-actions.md) in der Action -Spalte einer Mergemodulsequenztabelle verwendet wird, müssen die BaseAction- und After-Spalten dieses Datensatzes NULL sein.

</dd> <dt>

<span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequenz
</dt> <dd>

Die Sequenznummer einer Standardaktion. Wenn eine benutzerdefinierte Aktion oder ein benutzerdefiniertes Dialogfeld in die Spalte Aktion dieser Zeile eingegeben wird, muss dieses Feld auf NULL festgelegt werden.

Wenn Sie [Standardaktionen](standard-actions.md) in Mergemodulsequenztabellen verwenden, sollte der Wert in der Spalte Sequenz die empfohlene Aktionssequenznummer sein. Wenn sich die Sequenznummer im Mergemodul von der Sequenznummer für dieselbe Aktion in der .msi-Dateisequenztabelle unterscheidet, verwendet das Mergetool die Sequenznummer aus der .msi Datei. Die empfohlenen Sequenznummern von Standardaktionen finden Sie [in](using-a-sequence-table.md) den vorgeschlagenen Sequenzen unter Verwenden einer Sequenztabelle.

</dd> <dt>

<span id="BaseAction"></span><span id="baseaction"></span><span id="BASEACTION"></span>BaseAction
</dt> <dd>

Die BaseAction-Spalte kann eine Standardaktion, eine benutzerdefinierte Aktion, die in der benutzerdefinierten Aktionstabelle des Mergemoduls angegeben ist, oder einen Dialog enthalten, der in der Dialogtabelle des Moduls angegeben ist. Die BaseAction-Spalte ist ein Schlüssel in der Spalte Aktion dieser Tabelle. Es darf sich nicht um einen Fremdschlüssel in einer anderen Mergetabelle oder Tabelle in der .msi datei. Dies bedeutet, dass jede Standardaktion, benutzerdefinierte Aktion oder jeder Dialog, der in der Spalte BaseAction aufgeführt ist, auch in der Spalte Aktion eines anderen Datensatzes in dieser Tabelle aufgeführt werden muss.

</dd> <dt>

<span id="After"></span><span id="after"></span><span id="AFTER"></span>Nach
</dt> <dd>

Boolescher Wert für die Frage, ob Action vor oder nach BaseAction steht.



| Wert | Bedeutung                          |
|-------|----------------------------------|
| 0     | Aktion, die vor BaseAction kommen soll |
| 1     | Nach BaseAction zu ergreifende Aktion  |



 

</dd> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Zustand
</dt> <dd>

Eine bedingte Anweisung, die angibt, ob die Aktion ausgeführt wird. NULL wird als TRUE ausgewertet.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Wenn diese Tabelle vorhanden ist, muss [die InstallUISequence-Tabelle](installuisequence-table.md) auch im Mergemodul vorhanden sein.

 

 



