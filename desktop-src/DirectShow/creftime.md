---
description: Die Klasse "kreftime" ist eine Hilfsklasse zum Verwalten von Verweis Zeiten.
ms.assetid: 4be0fc23-77fb-4c45-a899-c1dfc6ee89b9
title: Up-Time-Klasse (Ref time. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRefTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 01e83520943abafd814425b6ff3fb53f48775627
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364957"
---
# <a name="creftime-class"></a>Klasse "up"

![Klassenhierarchie in der Klasse](images/cutil05.png)

Die- `CRefTime` Klasse ist eine Hilfsklasse zum Verwalten von Verweis Zeiten.

Eine *Verweis Zeit* ist eine Zeiteinheit, die in 100-Nanosecond-Einheiten dargestellt wird. Diese Klasse nutzt dasselbe Datenlayout wie der [**Verweis \_ Zeit**](reference-time.md) -Datentyp, fügt jedoch einige Methoden und Operatoren hinzu, die Vergleichs-, Konvertierungs-und arithmetische Funktionen bereitstellen. Weitere Informationen zu Referenz Zeiten finden Sie unter [Zeit und Uhren in DirectShow](time-and-clocks-in-directshow.md).



| Öffentliche Element Variablen                                                 | BESCHREIBUNG                                           |
|-------------------------------------------------------------------------|-------------------------------------------------------|
| [**m \_ Zeit**](creftime-m-time.md)                                      | Gibt den **Verweis \_ Zeitwert** an.              |
| Öffentliche Methoden                                                          | BESCHREIBUNG                                           |
| [**Zeitpunkt der Aktualisierung**](creftime-creftime.md)                                   | Konstruktormethode.                                   |
| [**Getunits**](creftime-getunits.md)                                   | Ruft die Verweis Zeit in 100-Nanosekunden-Einheiten ab. |
| [**Millisekunden**](creftime-millisecs.md)                                 | Konvertiert die Verweis Zeit in Millisekunden.          |
| Operatoren                                                               | Beschreibung                                           |
| [**Operator Verweis \_ Zeit ()**](creftime-operator-reference-time-.md) | Wandelt das Objekt in einen **Verweis \_ Zeit** Datentyp um.  |
| [**Operator =**](creftime-operator-assign.md)                           | Weist eine neue Verweis Zeit zu.                         |
| [**Operator + =**](creftime-operator-plus-assign.md)                     | Addiert zwei Verweis Zeiten.                             |
| [**Operator =**](creftime-operator-minus-assign.md)                    | Subtrahiert eine Verweis Zeit von einer anderen.            |



 

## <a name="remarks"></a>Bemerkungen

Bei der Verwendung dieser Klasse ist ein möglicher pitfallwert vorhanden. Wenn Sie den Operator "+ =" mit einem "up"-Objekt als linken Operanden **und einer Variablen** vom Typ " **Long** " als den rechten Operanden anwenden, wandelt der Compiler den rechten Operanden implizit **in ein "** up"-Objekt um. Diese Umwandlung **verwendet den "** up"-Konstruktor, der Millisekunden in Bezugs \_ Zeiteinheiten konvertiert. Folglich wird der rechte Operand mit 10.000 multipliziert:


```
CRefTime rt;   // rt.m_time is 0.
LONG val = 20;
rt += val;    // Coerce val to CRefTime, rt.m_time is now 200,000.
```



Dies geschieht jedoch nicht mit dem Operator +:


```
CRefTime rt;   // rt.m_time is 0.
LONG val = 20;
rt = rt + val; // CRefTime, rt.m_time is 20.
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ref time. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



 

 




