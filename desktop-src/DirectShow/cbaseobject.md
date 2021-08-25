---
description: Die CBaseObject-Klasse ist eine abstrakte Klasse zum Implementieren von DirectShow-Objekten. Verwenden Sie Component Object Model CUnknown-Klasse, die von CBaseObject abgeleitet ist, um com-Objekte (COM) zu implementieren.
ms.assetid: 4b651d43-b177-4081-8c76-f6615ff2830c
title: CBaseObject-Klasse (Combase.h)
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
ms.openlocfilehash: 7809ec53746730f02f9b095ede3ae00b53f1fe55c21116c22d854c3d4b193e97
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119910620"
---
# <a name="cbaseobject-class"></a>CBaseObject-Klasse

Die **CBaseObject-Klasse** ist eine abstrakte Klasse zum Implementieren von DirectShow-Objekten. Zum Implementieren Component Object Model (COM)-Objekten verwenden Sie die [**CUnknown-Klasse,**](cunknown.md) die von **CBaseObject abgeleitet wird.**



| Klassenmethoden                                      | Beschreibung                            |
|----------------------------------------------------|----------------------------------------|
| [**CBaseObject**](cbaseobject-cbaseobject.md)     | Konstruktormethode.                    |
| [**~CBaseObject**](cbaseobject--cbaseobject.md)   | Destruktormethode.                     |
| [**ObjectsActive**](cbaseobject-objectsactive.md) | Ruft die Anzahl der aktiven Objekte ab. |



 

## <a name="remarks"></a>Hinweise

Die meisten DirectShow-Basisklassen werden von **CBaseObject abgeleitet.** Diese Klasse bietet Unterstützung beim Debuggen, indem die Anzahl aller DirectShow-Objekte zur Laufzeit aktiv ist. Die Objektanzahl wird in einer klassen statischen Membervariablen gespeichert:


```
class CBaseObject
{
private:
    static LONG m_cObjects;  // Total number of objects active. 
/* ... */
};
```



In Debugbuilds gibt die DLL zu, wenn sie entladen wird, während die Objektanzahl größer als 0 (null) ist. Dadurch können Lecks, die durch Probleme mit der Verweiszählung verursacht werden, leichter nachverfolgt werden.

Der **CBaseObject-Konstruktor** verwendet ein Argument, einen Debugnamen für das Objekt. Dieser Name wird in einer globalen Tabelle in der DLL gespeichert. Die [**DbgDumpObjectRegister-Funktion**](dbgdumpobjectregister.md) formatiert eine Liste der in der DLL aktiven Objekte und sendet sie an die Debugausgabe.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Combase.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[DirectShow-Basisklassen](directshow-base-classes.md)
</dt> </dl>

 

 




