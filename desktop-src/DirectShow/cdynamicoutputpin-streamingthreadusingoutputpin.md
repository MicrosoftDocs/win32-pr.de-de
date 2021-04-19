---
description: Die streamingthreadusingoutputpin-Methode bestimmt, ob ein Thread einen Streamingvorgang auf der PIN ausführt.
ms.assetid: b6432a11-4e8b-4eb4-ad8e-aaff9398641b
title: Cdynamicoutputpin. streamingthreadusingoutputpin-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.StreamingThreadUsingOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 797dcb94e227861642de2a05e6edf24f675bb4e7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352076"
---
# <a name="cdynamicoutputpinstreamingthreadusingoutputpin-method"></a>Cdynamicoutputpin. streamingthreadusingoutputpin-Methode

Die streamingthreadusingoutputpin-Methode bestimmt, ob ein Thread einen Streamingvorgang auf der PIN ausführt.

## <a name="syntax"></a>Syntax


```C++
virtual bool StreamingThreadUsingOutputPin();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt " **true** " zurück, wenn ein Thread einen Streamingvorgang auf der PIN ausführt. Andernfalls wird **false** zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Wenn Threads von der [**cdynamicoutputpin:: startusingoutputpin**](cdynamicoutputpin-startusingoutputpin.md) -Methode erfolgreich zurückgegeben wurden und kein entsprechender Aufrufen der [**cdynamicoutputpin:: stopusingoutputpin**](cdynamicoutputpin-stopusingoutputpin.md) -Methode vorgenommen wurden, gibt diese Methode **true** zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cdynamicoutputpin-Klasse**](cdynamicoutputpin.md)
</dt> </dl>

 

 




