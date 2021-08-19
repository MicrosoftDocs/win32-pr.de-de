---
description: Die COARefTime-Klasse konvertiert Verweiszeiten zwischen Sekunden und Einheiten von 100 Nanosekunden.
ms.assetid: 724420fc-9252-468f-9516-174be0a82999
title: COARefTime-Klasse (Ctlutil.h)
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
ms.openlocfilehash: 569da24d4487a1c7259c71ac0e2cda3ae7f31a88b69a74575186bdeb3b21445b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087270"
---
# <a name="coareftime-class"></a>COARefTime-Klasse

![coareftime-Klassenhierarchie](images/cutil05.png)

Die `COARefTime` -Klasse konvertiert Verweiszeiten zwischen Sekunden und Einheiten von 100 Nanosekunden.

Diese Klasse konvertiert zwischen Verweiszeiten, die mit Automation kompatibel sind, und Verweiszeiten, die mit C/C++ kompatibel sind. Automatisierungskompatible Schnittstellen verwenden **doppelte** Werte, um die Zeit in Sekunden darzustellen. Andere Schnittstellen verwenden 64-Bit-LONGLONG-Werte, um die Zeit in Einheiten von 100 Nanosekunden darzustellen.  Für diese Werte werden die folgenden Typen definiert:

``` syntax
typedef LONGLONG  REFERENCE_TIME;
typedef double    REFTIME;
```

Filter können die `COARefTime` -Klasse verwenden, um zwischen den beiden Formaten zu konvertieren. Diese Klasse wird von der [**CRefTime-Klasse**](creftime.md) abgeleitet.



| Öffentliche Methoden                                          | BESCHREIBUNG                                                           |
|---------------------------------------------------------|-----------------------------------------------------------------------|
| [**COARefTime**](coareftime-coareftime.md)             | Konstruktormethode.                                                   |
| Operatoren                                               | Beschreibung                                                           |
| [**double**](coareftime-double.md)                     | Konvertiert die Verweiszeit in einen **double-Wert.**                    |
| [**\_REFERENZZEIT**](coareftime-reference-time.md)    | Gibt das -Objekt in einen **REFERENCE \_ TIME-Wert** um.                      |
| [**operator =**](coareftime-operator-assign.md)        | Weist eine neue Verweiszeit zu.                                         |
| [**operator ==**](coareftime-operator-eq.md)           | Überprüft die Gleichheit zwischen zwei Verweiszeiten.                       |
| [**Operator !=**](cmediatype-operator-neq.md)          | Testet auf Ungleichheit zwischen zwei Verweiszeiten.                     |
| [**operator <**](coareftime-operator-lt.md)         | Testet, ob eine Referenzzeit kleiner als eine andere ist.                     |
| [**operator >**](coareftime-operator-gt.md)         | Testet, ob eine Referenzzeit größer als eine andere ist.                  |
| [**operator <=**](coareftime-operator-lteq.md)      | Testet, ob eine Verweiszeit kleiner oder gleich einer anderen ist.         |
| [**operator >=**](coareftime-operator-gteq.md)      | Testet, ob eine Verweiszeit größer oder gleich einer anderen ist.      |
| [**Operator +**](coareftime-operator-plus.md)          | Fügt zwei Verweiszeiten hinzu.                                             |
| [**Operator **](coareftime-operator-minus.md)         | Subtrahiert eine Verweiszeit von einer anderen.                            |
| [**Operator +=**](coareftime-operator-plus-assign.md)  | Fügt zwei Verweiszeiten hinzu und weist diesem Objekt das Ergebnis zu.      |
| [**operator =**](coareftime-operator-minus-assign.md) | Subtrahiert zwei Verweiszeiten und weist das Ergebnis diesem Objekt zu. |
| [**Operator \***](coareftime-operator-mult.md)         | Multipliziert eine Verweiszeit mit einem Wert.                               |
| [**operator/**](coareftime-operator-div.md)           | Dividiert eine Verweiszeit durch einen Wert.                                  |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



 

 




