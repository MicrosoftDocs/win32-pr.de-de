---
description: Der logische Wert einer Eigenschaft, die festgelegt wurde, ist "true".
ms.assetid: aee818aa-912d-4e59-b061-61cd35993593
title: Verwenden von Eigenschaften in Bedingungs Anweisungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73596c465c4bcc0864caf8512e97c92d68f05fc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354488"
---
# <a name="using-properties-in-conditional-statements"></a>Verwenden von Eigenschaften in Bedingungs Anweisungen

Der logische Wert einer Eigenschaft, die festgelegt wurde, ist "true". Um zu ermitteln, ob eine Eigenschaft festgelegt wurde, ohne tatsächlich ihren Wert zu erhalten, testen Sie den logischen Ausdruck "MyProperty" oder "Not MyProperty". Wenn die Eigenschaft MyProperty festgelegt ist, wird die erste als true ausgewertet und letztere als false.

Eine oder mehrere Eigenschaften können mit Operatoren kombiniert werden, um logische Ausdrücke zu bilden, die in Bedingungs Anweisungen verwendet werden. Weitere Informationen zu den Operatoren, die in Bedingungs Anweisungen verwendet werden können, finden Sie unter [bedingte Anweisungs Syntax](conditional-statement-syntax.md).

Eine Bedingungs Anweisung, die Eigenschaften verwendet, kann in die Spalte Bedingung der Bedingungs [Tabelle](condition-table.md) eingegeben werden, um den Auswahl Zustand eines beliebigen Eintrags in der [Featuretabelle](feature-table.md)zu ändern.

Bedingte Anweisungen mit einer oder mehreren Eigenschaften werden häufig in der Spalte Bedingung der Datenbanktabellen verwendet.

Die folgenden Tabellen verfügen jeweils über eine-Spalte für bedingte Ausdrücke:

-   [Bedingungs Tabelle](condition-table.md)
-   [ControlEvent-Tabelle](controlevent-table.md)
-   [LaunchCondition-Tabelle](launchcondition-table.md)
-   [InstallUISequence-Tabelle](installuisequence-table.md)
-   [InstallExecuteSequence-Tabelle](installexecutesequence-table.md)
-   [ControlCondition-Tabelle](controlcondition-table.md)
-   [AdminExecuteSequence-Tabelle](adminexecutesequence-table.md)
-   [AdvtExecuteSequence-Tabelle](advtexecutesequence-table.md)
-   [AdminUISequence-Tabelle](adminuisequence-table.md)

Beachten Sie, dass die sechs Aktions Sequenz Tabellen Felder für eine Bedingung aufweisen. Wenn der bedingte Ausdruck in diesem Feld false ergibt, überspringt das Installationsprogramm diese Aktion.

Wenn Sie in der UI-Sequenz eine [private Eigenschaft](private-properties.md) festlegen, indem Sie eine benutzerdefinierte Aktion in einer der Benutzeroberflächen-Sequenz Tabellen erstellen, wird diese Eigenschaft nicht in der Ausführungssequenz festgelegt. Wenn Sie die-Eigenschaft in der Ausführungssequenz festlegen möchten, müssen Sie auch eine benutzerdefinierte Aktion in eine Ausführungssequenz Tabelle einfügen. Alternativ können Sie die Eigenschaft zu einer [öffentlichen Eigenschaft](public-properties.md) machen und in der [**securecustomproperties**](securecustomproperties.md) -Eigenschaft einschließen.

Weitere Informationen finden Sie unter [Verwenden einer Sequenz Tabelle](using-a-sequence-table.md) oder [Verwenden von Eigenschaften](using-properties.md).

 

 



