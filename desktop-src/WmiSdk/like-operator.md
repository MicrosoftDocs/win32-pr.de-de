---
description: Der Like-Operator bestimmt, ob eine Zeichenfolge mit einem angegebenen Muster übereinstimmt.
ms.assetid: 6cafe696-891d-4b17-8802-4b872f76fc78
ms.tgt_platform: multiple
title: Like-Operator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9091f44dd131d5d2c30d2d46aa4fc109dcdf02b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106355636"
---
# <a name="like-operator"></a>Like-Operator

Der Like-Operator bestimmt, ob eine Zeichenfolge mit einem angegebenen Muster übereinstimmt. Das angegebene Muster kann genau die Zeichen enthalten, die übereinstimmen müssen, oder es kann Meta-Zeichen enthalten. Der Like-Operator gleicht die Teil Zeichenfolgen in der folgenden Tabelle mit den Platzhalter Zeichen ab.



| Zeichen       | BESCHREIBUNG                                                                                                                                                                                 |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \[ \]           | Ein beliebiges Zeichen innerhalb des angegebenen Bereichs ( \[ a-f \] ) oder Set ( \[ abcdef \] ).                                                                                                                 |
| ^               | Ein beliebiges Zeichen, das nicht innerhalb des Bereichs ( \[ ^ a-f \] ) oder der festgelegten Menge ( \[ ^ abcdef \] ) liegt.                                                                                                                     |
| %               | Eine beliebige Zeichenfolge mit 0 (null) oder mehr Zeichen. Im folgenden Beispiel werden alle-Instanzen gesucht, bei denen "Win" an einer beliebigen Stelle im Klassennamen gefunden wird: `SELECT * FROM meta_class WHERE __Class LIKE "%Win%"` |
| \_ (Unterstrich) | Ein beliebiges Zeichen. Jeder Literale unterstrich, der in der Abfrage Zeichenfolge verwendet wird, muss mit Escapezeichen versehen werden \[ \] (eckige Klammern).                                                             |



 

Beispielsweise ruft der folgende PowerShell-Code alle Instanzen der Win32- **\_ OperatingSystem** -Klasse ab, deren **Name** -Eigenschaft mit **FirstName** beginnt:

`Get-WmiObject win32_computerSystem -filter "Name LIKE 'FirstName%'"`

Da der Unterstrich ein Meta-Zeichen ist, muss die Escapezeichen, wenn das Abfrage Ziel einen Unterstrich aufweist, \[ \] umschließen. Beispielsweise können Sie alle Klassen Abfragen, die einen doppelten Unterstrich im Namen aufweisen.

Wenn Sie alle Klassen mit einem doppelten Unterstrich im Namen suchen möchten, müssen Sie beide Unterstriche mit \[ \] (eckigen Klammern) versehen, z. b.:

`SELECT * FROM meta_class WHERE __CLASS LIKE "%[_][_]%"`

Sie können eine like-Anweisung mit Not negieren. Stellen Sie zu diesem Zweck sicher, dass nicht direkt vor dem Feldnamen steht. Beispiel:

`  Get-WmiObject -computerName "." -query 'Select * FROM Win32_Printer WHERE Local="TRUE"      AND Network ="False" AND DriverName LIKE "%HP%"      AND NOT PortName LIKE "%10.%" AND NOT PortName LIKE "%\\%"'`

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WQL-Operatoren](wql-operators.md)
</dt> </dl>

 

 



