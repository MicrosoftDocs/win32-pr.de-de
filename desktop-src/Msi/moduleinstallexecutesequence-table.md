---
description: Ein Mergetool wertet die Tabelle ModuleInstallExecuteSequence aus und fügt dann die berechneten Aktionen mit einer richtigen Sequenznummer in die Tabelle InstallExecuteSequence ein.
ms.assetid: 6cd04d9a-5489-4fde-951e-aa962e9bd755
title: Tabelle "ModuleInstallExecuteSequence"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6659c8223e41307766d67a4a5138699b46e03fbf3d50b514cb452bdc870c009c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120042846"
---
# <a name="moduleinstallexecutesequence-table"></a>Tabelle "ModuleInstallExecuteSequence"

Ein Mergetool wertet die Tabelle ModuleInstallExecuteSequence aus und fügt dann die berechneten Aktionen mit einer richtigen Sequenznummer in die [Tabelle InstallExecuteSequence](installexecutesequence-table.md) ein.

Die Tabelle ModuleInstallExecuteSequence enthält die folgenden Spalten.



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

Aktion, die in die Sequenz eingefügt werden soll. Bezieht sich auf eine der [Standardaktionen](standard-actions.md)des Installationsprogramms oder einen Eintrag in der [CustomAction-Tabelle](customaction-table.md)des Mergemoduls oder [in der Dialogtabelle](dialog-table.md).

Wenn eine [Standardaktion](standard-actions.md) in der Action -Spalte einer Mergemodulsequenztabelle verwendet wird, müssen die Spalten BaseAction und After dieses Datensatzes NULL sein.

</dd> <dt>

<span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequenz
</dt> <dd>

Die Sequenznummer einer Standardaktion. Wenn eine benutzerdefinierte Aktion oder ein benutzerdefiniertes Dialogfeld in die Spalte Aktion dieser Zeile eingegeben wird, muss dieses Feld auf NULL festgelegt werden.

Wenn [Sie Standardaktionen](standard-actions.md) in Mergemodulsequenztabellen verwenden, sollte der Wert in der Spalte Sequenz die empfohlene Aktionssequenznummer sein. Wenn sich die Sequenznummer im Mergemodul von der für dieselbe Aktion in der .msi Dateisequenztabelle unterscheidet, verwendet das Mergetool die Sequenznummer aus der datei .msi. Die empfohlenen Sequenznummern von Standardaktionen finden Sie in den vorgeschlagenen Sequenzen unter [Verwenden einer Sequenztabelle.](using-a-sequence-table.md)

</dd> <dt>

<span id="BaseAction"></span><span id="baseaction"></span><span id="BASEACTION"></span>BaseAction
</dt> <dd>

Die Spalte BaseAction kann eine Standardaktion, eine benutzerdefinierte Aktion, die in der benutzerdefinierten Aktionstabelle des Mergemoduls angegeben ist, oder ein Dialogfeld enthalten, das in der Dialogtabelle des Moduls angegeben ist. Die BaseAction-Spalte ist ein Schlüssel in der Action-Spalte dieser Tabelle. Es kann sich nicht um einen Fremdschlüssel in einer anderen Mergetabelle oder Tabelle in der Windows Installer-Datei sein. Dies bedeutet, dass jede Standardaktion, jede benutzerdefinierte Aktion oder jedes Dialogfeld, die in der Spalte BaseAction aufgeführt sind, auch in der Spalte Aktion eines anderen Datensatzes in dieser Tabelle aufgeführt werden muss.

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

Eine bedingte Anweisung, die angibt, ob die Aktion ausgeführt werden soll. Ein NULL-Wert wird als TRUE ausgewertet.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Wenn die [Tabelle ModuleInstallExecuteSequence](installexecutesequence-table.md) vorhanden ist, muss die [Tabelle InstallExecuteSequence](installexecutesequence-table.md) auch im Mergemodul vorhanden sein.

 

 



