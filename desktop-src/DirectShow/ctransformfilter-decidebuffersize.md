---
description: Die decidebuffersize-Methode legt die Puffer Anforderungen der Ausgabe-PIN fest.
ms.assetid: 33e41668-b4f6-4142-b22e-2ddfb96332df
title: Ctransformfilter. decidebuffersize-Methode (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.DecideBufferSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 71a506a9c9cd16a014418b24ad3fbd1186d6f48f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371148"
---
# <a name="ctransformfilterdecidebuffersize-method"></a>Ctransformfilter. decidebuffersize-Methode

Die `DecideBufferSize` -Methode legt die Puffer Anforderungen der Ausgabe-PIN fest.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT DecideBufferSize(
   IMemAllocator        *pAlloc,
   ALLOCATOR_PROPERTIES *ppropInputRequest
) = 0;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*palloc* 
</dt> <dd>

Zeiger auf die [**imemzuordcator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) -Schnittstelle für die Zuweisung der Ausgabe-PIN.

</dd> <dt>

*ppropinputrequest* 
</dt> <dd>

Ein Zeiger auf eine [**\_ zuordnereigenschafts**](/windows/win32/api/strmif/ns-strmif-allocator_properties) Struktur, die Puffer Anforderungen aus der nachgeschalteten Eingabe-PIN enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK oder einen anderen **HRESULT** -Wert zurück.

## <a name="remarks"></a>Bemerkungen

Die [**ctransformoutputpin::D ecidebuffersize**](ctransformoutputpin-decidebuffersize.md) -Methode der Ausgabe-PIN ruft diese Methode auf. Diese Methode muss von der abgeleiteten Klasse implementiert werden. Weitere Informationen finden Sie unter [**cbaseoutputpin::D ecidebuffersize**](cbaseoutputpin-decidebuffersize.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ctransformfilter-Klasse**](ctransformfilter.md)
</dt> </dl>

 

 




