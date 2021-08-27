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
ms.openlocfilehash: 35443d212fc244c80da958f2f87d03363c59348be4189393c1c3493521a0439b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076580"
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

## <a name="remarks"></a>Hinweise

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

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Combase.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseObject-Klasse**](cbaseobject.md)
</dt> </dl>

 

 




