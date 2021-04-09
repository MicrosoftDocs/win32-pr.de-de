---
description: Die DateAdd-Funktion führt Zeit-und Datumsberechnungen für übereinstimmende Eigenschaften mit Datums Typen aus. Verwenden Sie die Funktion DateAdd, um Datumsangaben und Uhrzeiten in einem angegebenen Zeitraum vor dem aktuellen abzurufen.
ms.assetid: 83ef098d-85ef-4883-a1e1-9229e050247f
title: DATEADD-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c0b193e75ec644eb3312a61c723edeac43ee264
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128549"
---
# <a name="dateadd-function"></a>DATEADD-Funktion

Die DateAdd-Funktion führt Zeit-und Datumsberechnungen für übereinstimmende Eigenschaften mit Datums Typen aus. Verwenden Sie die Funktion DateAdd, um Datumsangaben und Uhrzeiten in einem angegebenen Zeitraum vor dem aktuellen abzurufen.

## <a name="syntax"></a>Syntax


```
DATEADD (DateTimeUnits, OffsetValue, DateTime)
```



## <a name="arguments"></a>Argumente

*Datetimeunits*

Gibt die Einheiten des *DateTime* -Parameters an: Jahr, Quartal, Monat, Woche, Tag, Stunde, Minute oder Sekunde. Bei diesem Wert wird die Groß-/Kleinschreibung beachtet, und für den Parameter sind keine Anführungszeichen erforderlich.

*Offsetvalue*

Gibt den Zeit Offset in den Einheiten an, die durch den *datetimeunits* -Parameter angegeben werden. **Offsetvalue** muss eine negative Ganzzahl sein. Positive Werte werden nicht unterstützt.

*DateTime*

Gibt einen Zeitstempel an, aus dem der Offset berechnet werden soll. Dies darf kein Datumsliteral sein. Es muss entweder getgmtdate oder das Ergebnis einer anderen DateAdd-Funktion sein.

## <a name="remarks"></a>Bemerkungen

Die DateAdd-Funktion kann nur in literalen Wert vergleichen und nur auf der rechten Seite des Vergleichs Operators verwendet werden.

Die getgmtdate-Funktion gibt das aktuelle Datum und die aktuelle Uhrzeit in der Ortszeit (Ortszeit) zurück. Beachten Sie, dass dieser Wert möglicherweise nicht mit der lokalen Zeit des Computers identisch ist.

Verwenden Sie den Vergleichs Operator "gleich" (=) nicht, da die interne Zeit Darstellung Rundungsfehler verursachen kann, die zu unerwarteten übereinstimmenden Ergebnissen führen.

Sie können mehrere DateAdd-Funktionen verwenden, um Offset Einheiten zu kombinieren.

### <a name="examples"></a>Beispiele

Die folgende Beispiel-WHERE-Klausel stimmt mit Dokumenten überein, die innerhalb der letzten fünf Tage geändert wurden:


```
...WHERE System.DateModified <=DATEADD (DAY, -5, GETGMTDATE())
```



Die folgende Beispiel-WHERE-Klausel stimmt mit Dokumenten überein, die innerhalb der letzten zwei Tage und vier Stunden geändert wurden:


```
...WHERE System.DateModified <=DATEADD (DAY, -2, DATEADD (HOUR, -4, GETGMTDATE()))
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Referenz**
</dt> <dt>

[Vergleich von literalen Werten](-search-sql-literalvaluecomparison.md)
</dt> <dt>

[Mehrwertige Vergleiche (Array)](-search-sql-multivaluedcomparisons.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Voll Text Prädikate](-search-sql-fulltextpredicates.md)
</dt> <dt>

[Nicht-voll Text Prädikate](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



