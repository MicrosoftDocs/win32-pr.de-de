---
description: ICE46 überprüft benutzerdefinierte Eigenschaften in Bedingungen, formatiertem Text und anderen Speicherorten, die sich von einer System definierten Eigenschaft nur durch die Groß-/Kleinschreibung von einem oder mehreren Zeichen unterscheiden.
ms.assetid: 892d7462-0222-4fa0-b14c-17742a266c0a
title: ICE46
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2e24a76560b02a3a0ce3afa681c7ba74fcc7a2e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756223"
---
# <a name="ice46"></a>ICE46

ICE46 überprüft benutzerdefinierte Eigenschaften in Bedingungen, formatiertem Text und anderen Speicherorten, die sich von einer System definierten Eigenschaft nur durch die Groß-/Kleinschreibung von einem oder mehreren Zeichen unterscheiden.

## <a name="result"></a>Ergebnis

ICE46 gibt eine Informations Meldung aus, wenn eine benutzerdefinierte Eigenschaft in einer Bedingung, einem formatierten Text und einem anderen Speicherort vorhanden ist, der sich von einer System definierten Eigenschaft nur im Fall von mindestens einem Zeichen unterscheidet.

## <a name="example"></a>Beispiel

ICE46 meldet die folgenden Fehler für das gezeigte Beispiel.



| ICE46-Fehler                                                                                                                                            | BESCHREIBUNG                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Die in der Eigenschaften Tabelle definierte Eigenschaft "REINSTALLMODE" unterscheidet sich von einer anderen definierten Eigenschaft nur durch den Fall                                                   | Der vom System definierte Eigenschaftsname " **REINSTALLMODE** " unterscheidet sich nur in der Groß-/Kleinschreibung von Bei Eigenschaften wird die Groß-/Kleinschreibung beachtet, sodass die benutzerdefinierte Eigenschaft nicht mit der System Eigenschaft identisch ist. Dies ist eine häufige Ursache für Fehler. |
| Die Eigenschaft "MyProperty", auf die in der Spalte "InstallExecuteSequence" verwiesen wird. Die Bedingung ' der Zeile ' InstallFinalize ' unterscheidet sich von einer definierten Eigenschaft nur nach Groß-/Kleinschreibung. | In der Eigenschafts Tabelle ist die MyProperty-Tabelle definiert, aber die referenzierte Eigenschaft ist MyProperty. Bei den Eigenschaften wird die Groß-/Kleinschreibung beachtet, sodass die beiden Eigenschaften nicht identisch sind. Dies ist eine häufige Ursache für Fehler.                          |



 

[Eigenschaften Tabelle](property-table.md)



| Eigenschaft      | Wert   |
|---------------|---------|
| Rein Stall Mode | omus REINSTALL    |
| MyProperty    | ein-Wert |



 

[InstallExecuteSequence-Tabelle](installexecutesequence-table.md) (partiell)



| Aktion          | Bedingung  |
|-----------------|------------|
| InstallFinalize wurde | MyProperty |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ice-Referenz](ice-reference.md)
</dt> </dl>

 

 



