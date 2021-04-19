---
description: Die Antwortmethode antwortet auf eine Anforderung.
ms.assetid: 90e91b99-6a1c-46a2-b83d-eba483f1832a
title: Camthread. Reply-Methode (wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.Reply
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5e86e0bc0155e527aa11c26531ae5608e6828362
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362091"
---
# <a name="camthreadreply-method"></a>Camthread. Reply-Methode

Die- `Reply` Methode antwortet auf eine-Anforderung.

## <a name="syntax"></a>Syntax


```C++
void Reply(
   DWORD dw
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dw* 
</dt> <dd>

Wert, der in der Methode " [**camthread:: callworker**](camthread-callworker.md) " zurückgegeben werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Die callworker-Methode blockiert, bis diese Methode aufgerufen wird. Der *DW* -Parameter liefert den Rückgabewert für callworker. Rufen Sie diese Methode in ihrer Thread Prozedur auf, nachdem Sie eine Anforderung abgerufen haben, um den angeforderten Thread freizugeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Camthread-Klasse**](camthread.md)
</dt> </dl>

 

 




