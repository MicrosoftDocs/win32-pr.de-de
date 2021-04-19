---
description: Ein Merge-Tool wertet die moduleinstallexecutesequence-Tabelle aus und fügt dann die berechneten Aktionen in die InstallExecuteSequence-Tabelle mit einer korrekten Sequenznummer ein.
ms.assetid: 6cd04d9a-5489-4fde-951e-aa962e9bd755
title: Moduleinstallexecutesequence-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d294ddfdf06028bf18d518e1086d37a0719f8c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366285"
---
# <a name="moduleinstallexecutesequence-table"></a>Moduleinstallexecutesequence-Tabelle

Ein Merge-Tool wertet die moduleinstallexecutesequence-Tabelle aus und fügt dann die berechneten Aktionen in die [InstallExecuteSequence-Tabelle](installexecutesequence-table.md) mit einer korrekten Sequenznummer ein.

Die moduleinstallexecutesequence-Tabelle enthält die folgenden Spalten.



| Spalte     | Typ                         | Schlüssel | Nullwerte zulässig |
|------------|------------------------------|-----|----------|
| Aktion     | [Bezeichner](identifier.md) | J   | N        |
| Sequenz   | [Integer](integer.md)       |     | J        |
| Baseaction | [Bezeichner](identifier.md) |     | J        |
| Nach      | [Integer](integer.md)       |     | J        |
| Bedingung  | [Condition](condition.md)   |     | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>Hinspiel
</dt> <dd>

Aktion, die in die Sequenz eingefügt werden soll. Bezieht sich auf eine der [Standard Aktionen](standard-actions.md)des-Installers oder einen Eintrag in der [CustomAction-Tabelle](customaction-table.md)des Merge-Moduls oder in der [Dialog Feld Tabelle](dialog-table.md).

Wenn eine [Standardaktion](standard-actions.md) in der Aktionsspalte einer mergemodulsequenz-Tabelle verwendet wird, müssen die baseaction-und After-Spalten dieses Datensatzes Null sein.

</dd> <dt>

<span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequenz
</dt> <dd>

Die Sequenznummer einer Standardaktion. Wenn eine benutzerdefinierte Aktion oder ein benutzerdefiniertes Dialogfeld in die Aktionsspalte dieser Zeile eingegeben wird, muss dieses Feld auf NULL festgelegt werden.

Bei Verwendung von [Standard Aktionen](standard-actions.md) in Mergemodul-Sequenz Tabellen sollte der Wert in der Sequence-Spalte die empfohlene Aktions Sequenznummer sein. Wenn sich die Sequenznummer im Mergemodul von der Sequenznummer für die gleiche Aktion in der MSI-Datei Sequenz Tabelle unterscheidet, verwendet das Mergetool die Sequenznummer aus der MSI-Datei. Informationen zu den empfohlenen Sequenznummern von Standard Aktionen finden [Sie unter Verwenden einer Sequenz Tabelle](using-a-sequence-table.md) für vorgeschlagene Sequenzen.

</dd> <dt>

<span id="BaseAction"></span><span id="baseaction"></span><span id="BASEACTION"></span>Baseaction
</dt> <dd>

Die baseaction-Spalte kann eine Standardaktion, eine benutzerdefinierte Aktion, die in der benutzerdefinierten Aktionstabelle des Merge-Moduls angegeben ist, oder ein Dialogfeld enthalten, das in der Dialog Tabelle des Moduls angegeben ist. Die baseaction-Spalte ist ein Schlüssel in der Aktionsspalte dieser Tabelle. Dabei kann es sich nicht um einen Fremdschlüssel in einer anderen MERGE-Tabelle oder-Tabelle in der Windows Installer Datei handeln. Dies bedeutet, dass jede Standardaktion, benutzerdefinierte Aktion oder ein Dialogfeld, das in der Spalte baseaction aufgeführt ist, auch in der Aktionsspalte eines anderen Datensatzes in dieser Tabelle aufgeführt werden muss.

</dd> <dt>

<span id="After"></span><span id="after"></span><span id="AFTER"></span>Nachdem
</dt> <dd>

Boolescher Wert, der ist, ob Action vor oder nach baseaction steht.



| Wert | Bedeutung                          |
|-------|----------------------------------|
| 0     | Aktion, die vor baseaction erfolgen soll |
| 1     | Aktion, die nach baseaction erfolgen soll  |



 

</dd> <dt>

<span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Anlage
</dt> <dd>

Eine Bedingungs Anweisung, die angibt, ob die Aktion ausgeführt werden soll. Ein NULL-Wert wird als true ausgewertet.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Wenn die [moduleinstallexecutesequence-Tabelle](installexecutesequence-table.md) vorhanden ist, muss auch die [InstallExecuteSequence-Tabelle](installexecutesequence-table.md) im Mergemodul vorhanden sein.

 

 



