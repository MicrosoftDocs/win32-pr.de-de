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
ms.openlocfilehash: fce67bbe22361bdbae0cd3e51768e0cf0743d97d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098718"
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

Zeichenfolge, die den Debugnamen des Filters enthält. Weitere Informationen finden Sie unter [**CBaseObject.**](cbaseobject.md)

</dd> <dt>

*lpUnk* 
</dt> <dd>

Zeiger auf den Besitzer dieses Objekts. Wenn das Objekt aggregiert wird, übergeben Sie einen Zeiger auf die **IUnknown-Schnittstelle** des aggregierenden Objekts. Legen Sie andernfalls diesen Parameter auf **NULL** fest.

</dd> <dt>

*Clsid* 
</dt> <dd>

Klassenbezeichner des Filters.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der Konstruktor erstellt keine Pins des Filters. Dies geschieht beim ersten Aufruf der [**GetPin-Methode.**](ctransformfilter-getpin.md) Der Konstruktor initialisiert die Membervariablen [**m \_ pInput**](ctransformfilter-m-pinput.md) und [**m \_ pOutput**](ctransformfilter-m-poutput.md) mit **NULL.**

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CTransformFilter-Klasse**](ctransformfilter.md)
</dt> </dl>

 

 




