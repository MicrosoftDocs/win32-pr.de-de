---
description: Die GetDueCommand-Methode ruft einen Zeiger auf den nächsten fälligen Befehl ab.
ms.assetid: f23434a6-ad2c-4b64-90b1-2f486a16e7e6
title: CCmdQueue.GetDueCommand-Methode (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.GetDueCommand
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f6e7c8d133537dc2b185c755e65f3a4febbee762c5c2306de37ad0c627434df7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016428"
---
# <a name="ccmdqueuegetduecommand-method"></a>CCmdQueue.GetDueCommand-Methode

Die `GetDueCommand` -Methode ruft einen Zeiger auf den nächsten fälligen Befehl ab.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT GetDueCommand(
   CDeferredCommand **ppCmd,
   long             msTimeout
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppCmd* 
</dt> <dd>

Adresse eines Zeigers auf den verzögerten Befehl.

</dd> <dt>

*msTimeout* 
</dt> <dd>

Zeitspanne, die gewartet werden soll, bevor das Time out ausgeführt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt E \_ ABORT zurück, wenn ein Time out auftritt. Gibt S \_ OK zurück, wenn erfolgreich. Andernfalls wird ein Fehler zurückgegeben. Gibt ein Objekt zurück, das mit **IUnknown::AddRef** inkrementiert wurde.

## <a name="remarks"></a>Hinweise

Diese Memberfunktion wird blockiert, bis ein ausstehender Befehl fällig ist. Die Memberfunktion blockiert den Zeitraum in Millisekunden, der im *msTimeout-Parameter* angegeben ist. Streamzeitbefehle werden nur zwischen den Memberfunktionen [**CCmdQueue::Run**](ccmdqueue-run.md) und [**CCmdQueue::EndRun**](ccmdqueue-endrun.md) fällig. Der Befehl bleibt in der Warteschlange, bis er ausgeführt oder abgebrochen wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CCmdQueue-Klasse**](ccmdqueue.md)
</dt> </dl>

 

 




