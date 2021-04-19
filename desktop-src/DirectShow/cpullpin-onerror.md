---
description: Die OnError-Methode wird aufgerufen, wenn beim Streaming ein Fehler auftritt. Diese Methode muss von der abgeleiteten Klasse implementiert werden.
ms.assetid: 0f135cab-611c-4464-9605-360a30de7eb3
title: Cpullpin. OnError-Methode (pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.OnError
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2dc8bf7f307ab56609b5f90f6955a1f666854270
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371681"
---
# <a name="cpullpinonerror-method"></a>Cpullpin. OnError-Methode

Die- `OnError` Methode wird aufgerufen, wenn beim Streaming ein Fehler auftritt. Diese Methode muss von der abgeleiteten Klasse implementiert werden.

## <a name="syntax"></a>Syntax


```C++
virtual void OnError(
   HRESULT hr
) = 0;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Std.* 
</dt> <dd>

Gibt den **HRESULT** -Wert an, der von der fehlerhaften Methode zurückgegeben wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Das-Objekt ruft diese Methode immer dann auf, wenn ein Fehler auftritt, der den datenzieh Thread stoppt. Der Filter kann diese Methode verwenden, um Streamingfehler ordnungsgemäß wiederherzustellen. In den meisten Fällen wird der Fehler vom upstreamfilter zurückgegeben, sodass der upstreamfilter dafür zuständig ist, ihn an den Filter Graph-Manager zu melden. Wenn der Fehler innerhalb der [**cpullpin:: Receive**](cpullpin-receive.md) -Methode auftritt, sollte der Filter ein [**EC \_ errorabort**](ec-errorabort.md) -Ereignis senden. (Weitere Informationen finden Sie unter [**imediaeventsink:: notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify).)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Pullpin. h</dt> </dl>                                                                                                       |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cpullpin-Klasse**](cpullpin.md)
</dt> </dl>

 

 




