---
description: Der LIKE-Operator bestimmt, ob eine Zeichenfolge einem angegebenen Muster entspricht.
ms.assetid: 6cafe696-891d-4b17-8802-4b872f76fc78
ms.tgt_platform: multiple
title: LIKE-Operator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2e5df500091fac8b15bcdcb448b7a97fc00dc62807ba854757e447f07e6f4e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118317869"
---
# <a name="like-operator"></a>LIKE-Operator

Der LIKE-Operator bestimmt, ob eine Zeichenfolge einem angegebenen Muster entspricht. Das angegebene Muster kann genau die übereinstimmenden Zeichen oder Metazeichen enthalten. Tatsächlich gleicht der LIKE-Operator Teilzeichenfolgen mithilfe der Platzhalterzeichen in der folgenden Tabelle ab.



| Zeichen       | Beschreibung                                                                                                                                                                                 |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \[ \]           | Ein beliebiges Zeichen innerhalb des angegebenen Bereichs ( \[ a-f \] ) oder set ( \[ abcdef \] ).                                                                                                                 |
| ^               | Ein beliebiges Zeichen, das nicht innerhalb des Bereichs liegt ( \[ ^a-f \] ) oder festgelegt ( \[ ^abcdef \] .)                                                                                                                     |
| %               | Eine beliebige Zeichenfolge mit 0 (null) oder mehr Zeichen. Im folgenden Beispiel werden alle Instanzen gefunden, in denen "Win" an einer beliebigen Stelle im Klassennamen gefunden wird: `SELECT * FROM meta_class WHERE __Class LIKE "%Win%"` |
| \_ (Unterstrich) | Ein beliebiges Zeichen. Jeder literale Unterstrich, der in der Abfragezeichenfolge verwendet wird, muss mit Escapezeichen gesetzt werden, indem er in \[ \] eckige Klammern gesetzt wird.                                                             |



 

Der folgende Power Shell-Code ruft beispielsweise alle Instanzen der **Win32 \_ operatingSystem-Klasse** ab, deren **Name-Eigenschaft** mit **FirstName beginnt:**

`Get-WmiObject win32_computerSystem -filter "Name LIKE 'FirstName%'"`

Da es sich bei dem Unterstrich um ein Metazeichen handelt, müssen die Escapezeichen des Abfrageziels den Unterstrich \[ \] umschließen. Beispielsweise können Sie alle Klassen abfragen, die einen doppelten Unterstrich im Namen haben.

Um alle Klassen mit einem doppelten Unterstrich im Namen zu finden, müssen Sie beide Unterstriche mit (eckigen Klammern) um \[ \] escapen, z. B.:

`SELECT * FROM meta_class WHERE __CLASS LIKE "%[_][_]%"`

Sie können eine LIKE-Anweisung mit NOT negieren. Stellen Sie dazu sicher, dass Sie NOT direkt vor dem Feldnamen platzieren. Beispiel:

`  Get-WmiObject -computerName "." -query 'Select * FROM Win32_Printer WHERE Local="TRUE"      AND Network ="False" AND DriverName LIKE "%HP%"      AND NOT PortName LIKE "%10.%" AND NOT PortName LIKE "%\\%"'`

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WQL-Operatoren](wql-operators.md)
</dt> </dl>

 

 



