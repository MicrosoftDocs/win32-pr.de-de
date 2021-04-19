---
description: Die coaref-Zeit Klasse konvertiert Verweis Zeiten zwischen Sekunden und 100-Nanosekunden-Einheiten.
ms.assetid: 724420fc-9252-468f-9516-174be0a82999
title: Coaref Time-Klasse (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COARefTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 851495d69a1e34bd1723c20f88dc4bb86b7a8025
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367527"
---
# <a name="coareftime-class"></a>Coaref Time-Klasse

![coaref Time-Klassenhierarchie](images/cutil05.png)

Die `COARefTime` -Klasse konvertiert Verweis Zeiten zwischen Sekunden und 100-Nanosekunden-Einheiten.

Diese Klasse konvertiert zwischen Verweis Zeiten, die mit Automatisierungs-und Bezugszeiten kompatibel sind, die mit C/C++ kompatibel sind. Automation-kompatible Schnittstellen verwenden **doppelte** Werte, um die Zeit in Sekunden darzustellen. Andere Schnittstellen verwenden 64-Bit- **Longlong** -Werte, um die Zeit in 100-Nanosecond-Einheiten darzustellen. Die folgenden Typen werden für diese Werte definiert:

``` syntax
typedef LONGLONG  REFERENCE_TIME;
typedef double    REFTIME;
```

Filter können die- `COARefTime` Klasse verwenden, um zwischen den beiden Formaten zu konvertieren. Diese Klasse wird [**von der Klasse "Klasse"**](creftime.md) abgeleitet.



| Öffentliche Methoden                                          | BESCHREIBUNG                                                           |
|---------------------------------------------------------|-----------------------------------------------------------------------|
| [**Coaref-Zeit**](coareftime-coareftime.md)             | Konstruktormethode.                                                   |
| Operatoren                                               | Beschreibung                                                           |
| [**double**](coareftime-double.md)                     | Konvertiert die Verweis Zeit in einen **Double** -Wert.                    |
| [**Verweis \_ Zeit**](coareftime-reference-time.md)    | Wandelt das Objekt in einen **Verweis \_ Zeitwert** um.                      |
| [**Operator =**](coareftime-operator-assign.md)        | Weist eine neue Verweis Zeit zu.                                         |
| [**Operator = =**](coareftime-operator-eq.md)           | Testet auf Gleichheit zwischen zwei Verweis Zeiten.                       |
| [**Operator! =**](cmediatype-operator-neq.md)          | Prüft auf Ungleichheit zwischen zwei Verweis Zeiten.                     |
| [**Operator <**](coareftime-operator-lt.md)         | Testet, ob eine Verweis Zeit kleiner als eine andere ist.                     |
| [**Operator >**](coareftime-operator-gt.md)         | Testet, ob eine Verweis Zeit größer als eine andere ist.                  |
| [**Operator <=**](coareftime-operator-lteq.md)      | Testet, ob eine Verweis Zeit kleiner als oder gleich einem anderen ist.         |
| [**Operator >=**](coareftime-operator-gteq.md)      | Testet, ob eine Verweis Zeit größer oder gleich einer anderen ist.      |
| [**Operator +**](coareftime-operator-plus.md)          | Addiert zwei Verweis Zeiten.                                             |
| [* *-Operator * *](coareftime-operator-minus.md)         | Subtrahiert eine Verweis Zeit von einer anderen.                            |
| [**Operator + =**](coareftime-operator-plus-assign.md)  | Addiert zwei Verweis Zeiten und weist das Ergebnis diesem-Objekt zu.      |
| [**Operator =**](coareftime-operator-minus-assign.md) | Subtrahiert zwei Verweis Zeiten und weist das Ergebnis diesem-Objekt zu. |
| [**KOM \***](coareftime-operator-mult.md)         | Multipliziert eine Verweis Zeit mit einem Wert.                               |
| [**KOM**](coareftime-operator-div.md)           | Dividiert eine Verweis Zeit durch einen-Wert.                                  |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



 

 




