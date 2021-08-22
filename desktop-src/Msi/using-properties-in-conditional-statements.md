---
description: Der logische Wert einer Eigenschaft, die festgelegt wurde, ist True.
ms.assetid: aee818aa-912d-4e59-b061-61cd35993593
title: Verwenden von Eigenschaften in bedingten Anweisungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f5dcee5c2d657b8014ac98c0d4d1ce5b56f0f3614a597cd63611ae965e30720
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119499210"
---
# <a name="using-properties-in-conditional-statements"></a>Verwenden von Eigenschaften in bedingten Anweisungen

Der logische Wert einer Eigenschaft, die festgelegt wurde, ist True. Um zu bestimmen, ob eine Eigenschaft festgelegt wird, ohne tatsächlich ihren Wert zu erhalten, testen Sie den logischen Ausdruck "MyProperty" oder "Not MyProperty". Wenn die MyProperty-Eigenschaft festgelegt ist, wird ersteres als True und letztere als False ausgewertet.

Eine oder mehrere Eigenschaften können mit Operatoren kombiniert werden, um logische Ausdrücke zu bilden, die in bedingungsbedingten Anweisungen verwendet werden. Weitere Informationen zu den Operatoren, die in bedingten Anweisungen verwendet werden können, finden Sie unter [Conditional Statement Syntax](conditional-statement-syntax.md).

Eine bedingte Anweisung, die Eigenschaften verwendet, kann in die Spalte Bedingung der [Tabelle Bedingung](condition-table.md) eingegeben werden, um den Auswahlzustand eines eintrags in der [Featuretabelle zu ändern.](feature-table.md)

Bedingte Anweisungen mit mindestens einer Eigenschaft werden häufig in der Spalte Bedingung von Datenbanktabellen verwendet.

Die folgenden Tabellen enthalten jeweils eine Spalte für bedingte Ausdrücke:

-   [Bedingungstabelle](condition-table.md)
-   [ControlEvent-Tabelle](controlevent-table.md)
-   [LaunchCondition-Tabelle](launchcondition-table.md)
-   [InstallUISequence-Tabelle](installuisequence-table.md)
-   [InstallExecuteSequence-Tabelle](installexecutesequence-table.md)
-   [ControlCondition-Tabelle](controlcondition-table.md)
-   [AdminExecuteSequence-Tabelle](adminexecutesequence-table.md)
-   [Tabelle "AdvtExecuteSequence"](advtexecutesequence-table.md)
-   [AdminUISequence-Tabelle](adminuisequence-table.md)

Beachten Sie, dass die sechs Aktionssequenztabellen Felder für eine Bedingung enthalten. Wenn der bedingte Ausdruck in diesem Feld falseausgewertet wird, überspringt das Installationsprogramm diese Aktion.

Wenn Sie eine [private Eigenschaft](private-properties.md) in der Sequenz der Benutzeroberfläche festlegen, indem Sie eine benutzerdefinierte Aktion in einer der Sequenztabellen der Benutzeroberfläche erstellen, wird diese Eigenschaft nicht in der Ausführungssequenz festgelegt. Um die -Eigenschaft in der Ausführungssequenz festlegen zu können, müssen Sie auch eine benutzerdefinierte Aktion in einer Ausführungssequenztabelle festlegen. Alternativ können Sie die Eigenschaft zu einer öffentlichen [Eigenschaft](public-properties.md) machen und in die [**SecureCustomProperties-Eigenschaft**](securecustomproperties.md) enthalten.

Weitere Informationen finden Sie unter [Verwenden einer Sequenztabelle oder](using-a-sequence-table.md) Verwenden von [Eigenschaften.](using-properties.md)

 

 



