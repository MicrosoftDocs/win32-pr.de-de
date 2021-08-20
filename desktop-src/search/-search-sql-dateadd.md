---
description: Die DATEADD-Funktion führt Zeit- und Datumsberechnungen für übereinstimmende Eigenschaften mit Datumstypen durch. Verwenden Sie die DATEADD-Funktion, um Datums- und Uhrzeitangaben in einer angegebenen Zeitspanne vor dem Aktuellen abzurufen.
ms.assetid: 83ef098d-85ef-4883-a1e1-9229e050247f
title: DATEADD-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 875855ac69809c6312a4911b82dd3dd627965331946e206863cfc29a8a090c38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117680734"
---
# <a name="dateadd-function"></a>DATEADD-Funktion

Die DATEADD-Funktion führt Zeit- und Datumsberechnungen für übereinstimmende Eigenschaften mit Datumstypen durch. Verwenden Sie die DATEADD-Funktion, um Datums- und Uhrzeitangaben in einer angegebenen Zeitspanne vor dem Aktuellen abzurufen.

## <a name="syntax"></a>Syntax


```
DATEADD (DateTimeUnits, OffsetValue, DateTime)
```



## <a name="arguments"></a>Argumente

*DateTimeUnits*

Gibt die Einheiten des *DateTime-Parameters* an: YEAR, QUARTER, MONTH, WEEK, DAY, HOUR, MINUTE oder SECOND. Bei diesem Wert wird die Groß-/Kleinschreibung beachtet, und für den Parameter sind keine Anführungszeichen erforderlich.

*OffsetValue*

Gibt den Zeitoffset in den vom *DateTimeUnits-Parameter angegebenen* Einheiten an. **OffsetValue** muss eine negative ganze Zahl sein. Positive Werte werden nicht unterstützt.

*DateTime*

Gibt einen Zeitstempel an, aus dem der Offset berechnet werden soll. Dies kann kein Datumsliteral sein. Dies muss entweder GETGMTDATE oder das Ergebnis einer anderen DATEADD-Funktion sein.

## <a name="remarks"></a>Hinweise

Die DATEADD-Funktion kann nur in Literalwertvergleichen und nur auf der rechten Seite des Vergleichsoperators verwendet werden.

Die GETGMTDATE-Funktion gibt das aktuelle Datum und die aktuelle Uhrzeit in Greenwich Mean Time (GMT) zurück. Denken Sie daran, dass dieser Wert möglicherweise nicht mit der lokalen Zeit Ihres Computers identisch ist.

Verwenden Sie nicht den Vergleichsoperator equals (=), da die interne Zeitdarstellung Rundungsfehler erzeugen kann, die zu unerwarteten Übereinstimmungsergebnissen führen.

Sie können mehrere DATEADD-Funktionen verwenden, um Offseteinheiten zu kombinieren.

### <a name="examples"></a>Beispiele

Die folgende WHERE-Beispielklausel entspricht Dokumenten, die innerhalb der letzten fünf Tage geändert wurden:


```
...WHERE System.DateModified <=DATEADD (DAY, -5, GETGMTDATE())
```



Die folgende WHERE-Beispielklausel entspricht Dokumenten, die innerhalb der letzten zwei Tage und vier Stunden geändert wurden:


```
...WHERE System.DateModified <=DATEADD (DAY, -2, DATEADD (HOUR, -4, GETGMTDATE()))
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Referenz**
</dt> <dt>

[Literalwertvergleich](-search-sql-literalvaluecomparison.md)
</dt> <dt>

[Mehrwertige Vergleiche (ARRAY)](-search-sql-multivaluedcomparisons.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Volltextprädikate](-search-sql-fulltextpredicates.md)
</dt> <dt>

[Nicht-Volltextprädikate](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



