---
description: Konstruktormethode.
ms.assetid: 20c3c4af-b22f-4b74-a6b6-5ee309de4eef
title: Cbaseobject. cbaseobject-Konstruktor (ComBase. h)
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
ms.openlocfilehash: 4b13fe906af1900dbf067e8aa9273d811b3c1ef3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369552"
---
# <a name="cbaseobjectcbaseobject-constructor"></a>Cbaseobject. cbaseobject-Konstruktor

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

Eine Zeichenfolge, die den Namen des Objekts zu Debuggingzwecken enthält.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Methode erhöht die Anzahl von aktiven Objekten. (Siehe [**cbaseobject:: objeczactive**](cbaseobject-objectsactive.md).)

Weisen Sie den *PName* -Parameter im statischen Arbeitsspeicher zu:


```C++
// Correct.
CBaseObject *pObject = new CBaseObject(NAME("My Object"));

// Incorrect.
TCHAR ObjectName[] = TEXT("My Object");
CBaseObject *pObject = new CObject(ObjectName);
```



Das [**Name**](name.md) -Makro wird in Einzelhandels Builds in **null** kompiliert, sodass statische Zeichen folgen nur in Debugbuilds angezeigt werden. Weitere Informationen finden Sie unter [**dbgdumpobjectregiester**](dbgdumpobjectregister.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>ComBase. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbaseobject-Klasse**](cbaseobject.md)
</dt> </dl>

 

 




