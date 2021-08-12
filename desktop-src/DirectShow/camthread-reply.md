---
description: Die Reply-Methode antwortet auf eine Anforderung.
ms.assetid: 90e91b99-6a1c-46a2-b83d-eba483f1832a
title: WEBCAMThread.Reply-Methode (Wxutil.h)
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
ms.openlocfilehash: 9783703d711800b8002aa0372292349d83620eafb097be2256ffde6ab2c91c09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118662366"
---
# <a name="camthreadreply-method"></a>CAMThread.Reply-Methode

Die `Reply` -Methode antwortet auf eine Anforderung.

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

Wert, der in [**derCAMThread::CallWorker-Methode zurückgeben werden**](camthread-callworker.md) soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Die CallWorker-Methode wird blockiert, bis diese Methode aufgerufen wird. Der *dw-Parameter* gibt den Rückgabewert für CallWorker an. Rufen Sie diese Methode in Ihrer Threadprozedur auf, nachdem Sie eine Anforderung abgerufen haben, um den anfordernden Thread frei zu geben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CAMThread-Klasse**](camthread.md)
</dt> </dl>

 

 




