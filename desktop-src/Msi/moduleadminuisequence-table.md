---
description: Ein Mergetool wertet die Tabelle "moduleadminuisequence" aus und fügt dann die berechneten Aktionen in die Tabelle "AdminUISequence" mit einer korrekten Sequenznummer ein.
ms.assetid: c71477e7-22bc-420a-9902-39bbf98b4ee5
title: Moduleadminuisequence-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e128aebd6481c077827f4d1ba2b487eafe6132d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362655"
---
# <a name="moduleadminuisequence-table"></a>Moduleadminuisequence-Tabelle

Ein Mergetool wertet die Tabelle "moduleadminuisequence" aus und fügt dann die berechneten Aktionen in die [Tabelle "AdminUISequence](adminuisequence-table.md) " mit einer korrekten Sequenznummer ein.

Die moduleadminuisequence-Tabelle weist die folgenden Spalten auf.



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

Aktion, die in die Sequenz eingefügt werden soll. Bezieht sich auf eine der [Standard Aktionen](standard-actions.md)des-Installers oder einen Eintrag in der [CustomAction-Tabelle](customaction-table.md) oder- [Dialog Tabelle](dialog-table.md)des Merge-Moduls.

Wenn eine [Standardaktion](standard-actions.md) in der Aktionsspalte einer mergemodulsequenz-Tabelle verwendet wird, müssen die baseaction-und After-Spalten dieses Datensatzes Null sein.

</dd> <dt>

<span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>Sequenz
</dt> <dd>

Die Sequenznummer einer Standardaktion. Wenn eine benutzerdefinierte Aktion oder ein benutzerdefiniertes Dialogfeld in die Aktionsspalte dieser Zeile eingegeben wird, muss dieses Feld auf NULL festgelegt werden.

Bei Verwendung von [Standard Aktionen](standard-actions.md) in Mergemodul-Sequenz Tabellen sollte der Wert in der Sequence-Spalte die empfohlene Aktions Sequenznummer sein. Wenn sich die Sequenznummer im Mergemodul von der Sequenznummer für die gleiche Aktion in der MSI-Datei Sequenz Tabelle unterscheidet, verwendet das Mergetool die Sequenznummer aus der MSI-Datei. Informationen zu den empfohlenen Sequenznummern von Standard Aktionen finden [Sie unter Verwenden einer Sequenz Tabelle](using-a-sequence-table.md) für vorgeschlagene Sequenzen.

</dd> <dt>

<span id="BaseAction"></span><span id="baseaction"></span><span id="BASEACTION"></span>Baseaction
</dt> <dd>

Die baseaction-Spalte kann eine Standardaktion, eine benutzerdefinierte Aktion, die in der benutzerdefinierten Aktionstabelle des Merge-Moduls angegeben ist, oder ein Dialogfeld enthalten, das in der Dialog Tabelle des Moduls angegeben ist. Die baseaction-Spalte ist ein Schlüssel in der Aktionsspalte dieser Tabelle. Dabei kann es sich nicht um einen Fremdschlüssel in einer anderen MERGE-Tabelle oder-Tabelle in der MSI-Datei handeln. Dies bedeutet, dass jede Standardaktion, benutzerdefinierte Aktion oder ein Dialogfeld, das in der Spalte baseaction aufgeführt ist, auch in der Aktionsspalte eines anderen Datensatzes in dieser Tabelle aufgeführt werden muss.

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

Eine Bedingungs Anweisung, die angibt, ob die Aktion ausgeführt wird. NULL wird als true ausgewertet.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

<dl> <dt>

<span id="If_this_table_is_present_the__AdminUISequence_Table_must_also_be_present_in_the_merge_module."></span><span id="if_this_table_is_present_the__adminuisequence_table_must_also_be_present_in_the_merge_module."></span><span id="IF_THIS_TABLE_IS_PRESENT_THE__ADMINUISEQUENCE_TABLE_MUST_ALSO_BE_PRESENT_IN_THE_MERGE_MODULE."></span>Wenn diese Tabelle vorhanden ist, muss auch die [Tabelle AdminUISequence](adminuisequence-table.md) im Mergemodul vorhanden sein.
</dt> <dd></dd> </dl>

 

 



