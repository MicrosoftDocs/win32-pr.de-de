---
description: Die CheckRequest-Methode überprüft, ob eine Anforderung ohne Blockierung vor liegt.
ms.assetid: 46d0840e-a304-41e3-9016-9f35e404cd30
title: WEBCAMThread.CheckRequest-Methode (Wxutil.h)
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
ms.openlocfilehash: 292f8a7fb1ed4f12ad558993d6b1932b2ddff4656bada5e0a89067bac1baa9c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118662356"
---
# <a name="camthreadcheckrequest-method"></a>CAMThread.CheckRequest-Methode

Die `CheckRequest` -Methode überprüft, ob eine Anforderung ohne Blockierung vor liegt.

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

Zeiger auf eine Variable, die den Wert empfängt, der beim letzten Aufruf an [**dieCAMThread::CallWorker-Methode übergeben**](camthread-callworker.md) wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** wenn eine ausstehende Anforderung vorsteht, andernfalls **FALSE.**

## <a name="remarks"></a>Hinweise

Diese Methode ist eine nicht blockierende Version der [**METHODECAMThread::GetRequest.**](camthread-getrequest.md)

Wenn ein anderer Thread auf einen Aufruf von CallWorker wartet, ruft diese Methode den Anforderungsparameter ab und gibt **TRUE zurück.** Andernfalls wird **FALSE zurückgegeben.** Wenn die Methode **TRUE zurückgibt,** rufen Sie die [**METHODECAMThread::Reply auf,**](camthread-reply.md) um den anfordernden Thread frei zu geben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CAMThread-Klasse**](camthread.md)
</dt> </dl>

 

 




