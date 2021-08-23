---
description: ICE46 überprüft benutzerdefinierte Eigenschaften in Bedingungen, formatiertem Text und anderen Positionen, die sich von einer vom System definierten Eigenschaft nur im Fall von einem oder mehreren Zeichen unterscheiden.
ms.assetid: 892d7462-0222-4fa0-b14c-17742a266c0a
title: ICE46
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbe334f973449ffe8bdbba1eb51347576c0b39c6b8eacfb8103970726dbc1ec6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119580990"
---
# <a name="ice46"></a>ICE46

ICE46 überprüft benutzerdefinierte Eigenschaften in Bedingungen, formatiertem Text und anderen Positionen, die sich von einer vom System definierten Eigenschaft nur im Fall von einem oder mehreren Zeichen unterscheiden.

## <a name="result"></a>Ergebnis

ICE46 gibt eine Informationsmeldung aus, wenn eine benutzerdefinierte Eigenschaft in einer Bedingung, in formatiertem Text und an einem anderen Speicherort enthalten ist, der sich nur bei einem oder mehr Zeichen von systemdefinierten Eigenschaften unterscheidet.

## <a name="example"></a>Beispiel

ICE46 meldet die folgenden Fehler für das gezeigte Beispiel.



| ICE46-Fehler                                                                                                                                            | Beschreibung                                                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Die in der Eigenschaftentabelle definierte Eigenschaft ReinstallMode unterscheidet sich nur nach Fall von einer anderen definierten Eigenschaft.                                                   | Der systemdefinierte Eigenschaftenname **REINSTALLMODE** unterscheidet sich nur nach Fall von der benutzerdefinierten Eigenschaft. Bei Eigenschaften wird die Kleinschreibung beachtet, sodass die benutzerdefinierte Eigenschaft nicht mit der Systemeigenschaft identisch ist. Dies ist eine häufige Ursache für Fehler. |
| Die Eigenschaft "Myproperty", auf die in der Spalte "InstallExecuteSequence" verwiesen wird. Die Bedingung der Zeile "InstallFinalize" unterscheidet sich von einer definierten Eigenschaft nur nach Fall. | Die Eigenschaftentabelle definiert die Tabelle MyProperty, aber die Eigenschaft, auf die verwiesen wird, ist Myproperty. Bei Eigenschaften wird die Kleinschreibung beachtet, sodass die beiden Eigenschaften NICHT identisch sind. Dies ist eine häufige Ursache für Fehler.                          |



 

[Eigenschaftentabelle](property-table.md)



| Eigenschaft      | Wert   |
|---------------|---------|
| Reinstallmode | omus    |
| MyProperty    | ein -Wert |



 

[InstallExecuteSequence-Tabelle](installexecutesequence-table.md) (partiell)



| Aktion          | Bedingung  |
|-----------------|------------|
| InstallFinalize | Myproperty |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ICE-Referenz](ice-reference.md)
</dt> </dl>

 

 



