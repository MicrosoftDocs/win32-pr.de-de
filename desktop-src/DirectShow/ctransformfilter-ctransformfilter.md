---
description: Konstruktormethode.
ms.assetid: a64c3e29-91f2-455f-aac1-1e4ecce6958d
title: Ctransformfilter. ctransformfilter-Konstruktor (Transfrm. h)
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
ms.openlocfilehash: 39569dff69c2ab1ebb635cb69a4c71602a7400d8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359413"
---
# <a name="ctransformfilterctransformfilter-constructor"></a>Ctransformfilter. ctransformfilter-Konstruktor

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

*pobjectname* 
</dt> <dd>

Zeichenfolge, die den debugnamen des Filters enthält. Weitere Informationen finden Sie unter [**cbaseobject**](cbaseobject.md).

</dd> <dt>

*lpUnk* 
</dt> <dd>

Zeiger auf den Besitzer dieses Objekts. Wenn das Objekt aggregiert wird, übergeben Sie einen Zeiger an die **IUnknown** -Schnittstelle des Aggregations Objekts. Andernfalls legen Sie diesen Parameter auf **null** fest.

</dd> <dt>

*CLSID* 
</dt> <dd>

Klassen Bezeichner des Filters.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der Konstruktor erstellt nicht die Pins des Filters. Dies geschieht beim ersten Aufrufen der [**getpin**](ctransformfilter-getpin.md) -Methode. Der Konstruktor initialisiert die [**m \_ pinput**](ctransformfilter-m-pinput.md) -und [**m \_ poutput**](ctransformfilter-m-poutput.md) -Element Variablen auf **null**.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ctransformfilter-Klasse**](ctransformfilter.md)
</dt> </dl>

 

 




