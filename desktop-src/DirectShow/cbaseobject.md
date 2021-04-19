---
description: Die cbaseobject-Klasse ist eine abstrakte Klasse für die Implementierung von DirectShow-Objekten. Um Component Object Model (com)-Objekte zu implementieren, verwenden Sie die cunknown-Klasse, die von cbaseobject abgeleitet wird.
ms.assetid: 4b651d43-b177-4081-8c76-f6615ff2830c
title: Cbaseobject-Klasse (ComBase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseObject
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bbc3e072c31618dab6a7bc07048728f60dbcf0d2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358324"
---
# <a name="cbaseobject-class"></a>Cbaseobject-Klasse

Die **cbaseobject** -Klasse ist eine abstrakte Klasse für die Implementierung von DirectShow-Objekten. Um Component Object Model (com)-Objekte zu implementieren, verwenden Sie die [**cunknown**](cunknown.md) -Klasse, die von **cbaseobject** abgeleitet wird.



| Klassen Methoden                                      | BESCHREIBUNG                            |
|----------------------------------------------------|----------------------------------------|
| [**Cbaseobject**](cbaseobject-cbaseobject.md)     | Konstruktormethode.                    |
| [**~ Cbaseobject**](cbaseobject--cbaseobject.md)   | Dekonstruktormethode.                     |
| [**Objectatactive**](cbaseobject-objectsactive.md) | Ruft die Anzahl der aktiven-Objekte ab. |



 

## <a name="remarks"></a>Bemerkungen

Die meisten DirectShow-Basisklassen werden von **cbaseobject** abgeleitet. Diese Klasse stellt Debuggingunterstützung bereit, indem die Anzahl der während der Laufzeit aktiven DirectShow-Objekte beibehalten wird. Die Objekt Anzahl wird in einer klassenstatischen Element Variablen gespeichert:


```
class CBaseObject
{
private:
    static LONG m_cObjects;  // Total number of objects active. 
/* ... */
};
```



In Debugbuilds bestätigt die dll, dass Sie entladen wird, während die Objekt Anzahl größer als 0 (null) ist. Dies erleichtert das Ermitteln von Verlusten aufgrund von Problemen bei der Verweis Zählung.

Der **cbaseobject** -Konstruktor benötigt ein Argument, einen debugnamen für das Objekt. Dieser Name wird in einer globalen Tabelle in der dll gespeichert. Die Funktion [**dbgdumpobjectregiester**](dbgdumpobjectregister.md) formatiert eine Liste der in der dll aktiven Objekte und sendet Sie an die Debugausgabe.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>ComBase. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[DirectShow-Basisklassen](directshow-base-classes.md)
</dt> </dl>

 

 




