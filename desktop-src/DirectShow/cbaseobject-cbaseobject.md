---
description: 'CBaseObject.CBaseObject-Konstruktor : Konstruktormethode.'
ms.assetid: 20c3c4af-b22f-4b74-a6b6-5ee309de4eef
title: CBaseObject.CBaseObject-Konstruktor (Combase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseObject.CBaseObject
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 14fa2d3d38d42fa0feb387b477205cc51e0b6b87
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099618"
---
# <a name="cbaseobjectcbaseobject-constructor"></a>CBaseObject.CBaseObject-Konstruktor

Konstruktormethode.

## <a name="syntax"></a>Syntax


```C++
CBaseObject(
   const TCHAR *pName
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pName* 
</dt> <dd>

Zeichenfolge, die den Namen des Objekts zu Debugzwecken enthält.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Methode erhöht die Anzahl der aktiven Objekte. (Siehe [**CBaseObject::ObjectsActive**](cbaseobject-objectsactive.md).)

Ordnen Sie den *pName-Parameter* im statischen Speicher zu:


```C++
// Correct.
CBaseObject *pObject = new CBaseObject(NAME("My Object"));

// Incorrect.
TCHAR ObjectName[] = TEXT("My Object");
CBaseObject *pObject = new CObject(ObjectName);
```



Das [**NAME-Makro**](name.md) wird in Verkaufsbuilds zu **NULL** kompiliert, sodass statische Zeichenfolgen nur in Debugbuilds angezeigt werden. Weitere Informationen finden Sie unter [**DbgDumpObjectRegister**](dbgdumpobjectregister.md).

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Combase.h (einschließlich Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseObject-Klasse**](cbaseobject.md)
</dt> </dl>

 

 




