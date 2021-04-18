---
description: Die CheckRequest-Methode überprüft, ob eine Anforderung vorhanden ist, ohne zu blockieren.
ms.assetid: 46d0840e-a304-41e3-9016-9f35e404cd30
title: Camthread. CheckRequest-Methode (wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.CheckRequest
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5a004e0f5303cf6702c03e78c292a6a2d832a489
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361503"
---
# <a name="camthreadcheckrequest-method"></a>Camthread. CheckRequest-Methode

Die- `CheckRequest` Methode überprüft, ob eine Anforderung vorhanden ist, ohne zu blockieren.

## <a name="syntax"></a>Syntax


```C++
BOOL CheckRequest(
   DWORD *pParam
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pParam* 
</dt> <dd>

Ein Zeiger auf eine Variable, die den Wert empfängt, der beim letzten Aufruf der Methode " [**camthread:: callworker**](camthread-callworker.md) " übermittelt wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **true** zurück, wenn eine ausstehende Anforderung vorhanden ist, andernfalls **false** .

## <a name="remarks"></a>Bemerkungen

Diese Methode ist eine nicht blockierende Version der [**camthread:: GetRequest**](camthread-getrequest.md) -Methode.

Wenn ein anderer Thread auf einen Aufruf von callworker wartet, ruft diese Methode den Anforderungs Parameter ab und gibt **true** zurück. Andernfalls wird **false** zurückgegeben. Wenn die Methode **true** zurückgibt, wird die Methode " [**camthread:: Reply**](camthread-reply.md) " aufgerufen, um den anfordernden Thread freizugeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Camthread-Klasse**](camthread.md)
</dt> </dl>

 

 




