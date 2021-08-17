---
description: Die CRefTime-Klasse ist eine Hilfsklasse zum Verwalten von Verweiszeiten.
ms.assetid: 4be0fc23-77fb-4c45-a899-c1dfc6ee89b9
title: CRefTime-Klasse (Reftime.h)
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
ms.openlocfilehash: 5d8f9d30b057c1c011dcbff1b7d8c88e9183d50ca1fc2b7dd046b79fe8279d37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953954"
---
# <a name="creftime-class"></a>CRefTime-Klasse

![creftime-Klassenhierarchie](images/cutil05.png)

Die `CRefTime` -Klasse ist eine Hilfsklasse zum Verwalten von Verweiszeiten.

Eine *Bezugszeit ist* eine Zeiteinheit, die in Einheiten von 100 Nanosekunden dargestellt wird. Diese Klasse verwendet das gleiche Datenlayout wie der [**REFERENCE \_ TIME-Datentyp,**](reference-time.md) fügt jedoch einige Methoden und Operatoren hinzu, die Vergleichs-, Konvertierungs- und arithmetische Funktionen bereitstellen. Weitere Informationen zu Referenzzeiten finden Sie unter [Zeit und Uhren in DirectShow](time-and-clocks-in-directshow.md).



| Öffentliche Membervariablen                                                 | Beschreibung                                           |
|-------------------------------------------------------------------------|-------------------------------------------------------|
| [**m \_ Zeit**](creftime-m-time.md)                                      | Gibt den **REFERENCE \_ TIME-Wert** an.              |
| Öffentliche Methoden                                                          | Beschreibung                                           |
| [**CRefTime**](creftime-creftime.md)                                   | Konstruktormethode.                                   |
| [**GetUnits**](creftime-getunits.md)                                   | Ruft die Referenzzeit in Einheiten von 100 Nanosekunden ab. |
| [**Millisecs**](creftime-millisecs.md)                                 | Konvertiert die Verweiszeit in Millisekunden.          |
| Operatoren                                                               | Beschreibung                                           |
| [**Operator REFERENCE \_ TIME()**](creftime-operator-reference-time-.md) | Casts the object to a **REFERENCE \_ TIME** data type.  |
| [**operator=**](creftime-operator-assign.md)                           | Weist eine neue Verweiszeit zu.                         |
| [**operator+=**](creftime-operator-plus-assign.md)                     | Fügt zwei Verweiszeiten hinzu.                             |
| [**operator =**](creftime-operator-minus-assign.md)                    | Subtrahiert eine Verweiszeit von einer anderen.            |



 

## <a name="remarks"></a>Hinweise

Die Verwendung dieser Klasse kann zu einem potenziellen Fallstrick werden. Wenn Sie den +=-Operator mit einem **CRefTime-Objekt** als linken Operanden und einer Variablen vom Typ **LONG** als rechten Operanden anwenden, reiht der Compiler den rechten Operanden implizit in ein **CRefTime-Objekt** um. Diese Koercion verwendet den **CRefTime-Konstruktor,** der Millisekunden in REFERENCE TIME-Einheiten konvertiert. Daher wird der rechte Operand mit \_ 10.000 multipliziert:


```
CRefTime rt;   // rt.m_time is 0.
LONG val = 20;
rt += val;    // Coerce val to CRefTime, rt.m_time is now 200,000.
```



DasSelbe geschieht jedoch nicht mit dem Operator + :


```
CRefTime rt;   // rt.m_time is 0.
LONG val = 20;
rt = rt + val; // CRefTime, rt.m_time is 20.
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Reftime.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



 

 




