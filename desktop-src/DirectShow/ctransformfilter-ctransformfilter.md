---
description: 'CTransformFilter.CTransformFilter-Konstruktor : Konstruktormethode.'
ms.assetid: a64c3e29-91f2-455f-aac1-1e4ecce6958d
title: CTransformFilter.CTransformFilter-Konstruktor (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.CTransformFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 44061a753ef61c784298fe23e70f21fe410a9f0ad5f360acc10cb1fd16dd5f80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907689"
---
# <a name="ctransformfilterctransformfilter-constructor"></a>CTransformFilter.CTransformFilter-Konstruktor

Konstruktormethode.

## <a name="syntax"></a>Syntax


```C++
CTransformFilter(
   TCHAR     *pObjectName,
   LPUNKNOWN lpUnk,
   CLSID     clsid
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pObjectName* 
</dt> <dd>

Zeichenfolge, die den Debugnamen des Filters enthält. Weitere Informationen finden Sie unter [**CBaseObject**](cbaseobject.md).

</dd> <dt>

*lpUnk* 
</dt> <dd>

Zeiger auf den Besitzer dieses Objekts. Wenn das Objekt aggregiert wird, übergeben Sie einen Zeiger auf die **IUnknown-Schnittstelle** des aggregierenden Objekts. Legen Sie andernfalls diesen Parameter auf **NULL** fest.

</dd> <dt>

*Clsid* 
</dt> <dd>

Klassenbezeichner des Filters.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Der Konstruktor erstellt keine Stecknadeln des Filters. Dies geschieht beim ersten Aufruf der [**GetPin-Methode.**](ctransformfilter-getpin.md) Der Konstruktor initialisiert die Membervariablen [**m \_ pInput**](ctransformfilter-m-pinput.md) und [**m \_ pOutput**](ctransformfilter-m-poutput.md) mit **NULL.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CTransformFilter-Klasse**](ctransformfilter.md)
</dt> </dl>

 

 




