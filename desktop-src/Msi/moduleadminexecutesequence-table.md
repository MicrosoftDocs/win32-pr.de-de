---
description: Ein Mergetool wertet die Tabelle ModuleAdminExecuteSequence aus und fügt dann die berechneten Aktionen mit einer richtigen Sequenznummer in die Tabelle AdminExecuteSequence ein.
ms.assetid: 26cc5e15-8dfd-4bf5-8830-225164302278
title: Tabelle "ModuleAdminExecuteSequence"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e820c721fbbaa7d8925b07ee584cbb0b97fee66eac05fd7b8dafbe38f3f319d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118628716"
---
# <a name="moduleadminexecutesequence-table"></a>Tabelle "ModuleAdminExecuteSequence"

Ein Mergetool wertet die Tabelle ModuleAdminExecuteSequence aus und fügt dann die berechneten Aktionen mit einer richtigen Sequenznummer in die [Tabelle AdminExecuteSequence](adminexecutesequence-table.md) ein.

Die Tabelle ModuleAdminExecuteSequence enthält die folgenden Spalten.



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

Aktion, die in die Sequenz eingefügt werden soll. Bezieht sich auf eine der [Standardaktionen](standard-actions.md)des Installationsprogramms oder einen Eintrag in der [CustomAction-Tabelle](customaction-table.md) oder [der Dialogtabelle](dialog-table.md)des Mergemoduls.

Wenn eine [Standardaktion](standard-actions.md) in der Spalte Aktion einer Mergemodulsequenztabelle verwendet wird, müssen die Spalten BaseAction und After dieses Datensatzes NULL sein.

</dd> <dt>

<span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequenz
</dt> <dd>

Die Sequenznummer einer Standardaktion. Wenn eine benutzerdefinierte Aktion oder ein benutzerdefiniertes Dialogfeld in die Spalte Aktion dieser Zeile eingegeben wird, muss dieses Feld auf NULL festgelegt werden.

Wenn [Sie Standardaktionen](standard-actions.md) in Mergemodulsequenztabellen verwenden, sollte der Wert in der Spalte Sequenz die empfohlene Aktionssequenznummer sein. Wenn sich die Sequenznummer im Mergemodul von der für dieselbe Aktion in der .msi Dateisequenztabelle unterscheidet, verwendet das Mergetool die Sequenznummer aus der .msi Datei. Die empfohlenen Sequenznummern von Standardaktionen finden Sie in den vorgeschlagenen Sequenzen unter [Verwenden einer Sequenztabelle.](using-a-sequence-table.md)

</dd> <dt>

<span id="BaseAction"></span><span id="baseaction"></span><span id="BASEACTION"></span>BaseAction
</dt> <dd>

Die Spalte BaseAction kann eine Standardaktion, eine benutzerdefinierte Aktion, die in der benutzerdefinierten Aktionstabelle des Mergemoduls angegeben ist, oder ein Dialogfeld enthalten, das in der Dialogtabelle des Moduls angegeben ist. Die BaseAction-Spalte ist ein Schlüssel in der Action-Spalte dieser Tabelle. Es darf kein Fremdschlüssel in einer anderen Mergetabelle oder Tabelle in der .msi-Datei sein. Dies bedeutet, dass jede Standardaktion, jede benutzerdefinierte Aktion oder jedes Dialogfeld, die in der Spalte BaseAction aufgeführt sind, auch in der Spalte Aktion eines anderen Datensatzes in dieser Tabelle aufgeführt werden muss.

</dd> <dt>

<span id="After"></span><span id="after"></span><span id="AFTER"></span>Nach
</dt> <dd>

Boolescher Wert für die Angabe, ob Die Aktion vor oder nach BaseAction erfolgt.



| Wert | Bedeutung                          |
|-------|----------------------------------|
| 0     | Aktion, die vor BaseAction gestellt werden soll |
| 1     | Nach BaseAction zu ergreifende Aktion  |



 

</dd> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Zustand
</dt> <dd>

Eine bedingte Anweisung, die angibt, ob die Aktion ausgeführt wird. NULL wird als TRUE ausgewertet.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Wenn diese Tabelle vorhanden ist, muss die [Tabelle AdminExecuteSequence](adminexecutesequence-table.md) auch im Mergemodul vorhanden sein.

 

 



