---
description: Reiht eine Anforderung zur Ausführung durch den Arbeitsthread in die Warteschlange ein.
ms.assetid: a854f962-143d-4776-bf98-119d003867df
title: CMsgThread.PutThreadMsg-Methode (Msgthrd.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.PutThreadMsg
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7eefa95c4fd6ab19c895b4d1d47dba3a19302023985a4631708c3cf7ccc10d06
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119585640"
---
# <a name="cmsgthreadputthreadmsg-method"></a>CMsgThread.PutThreadMsg-Methode

Reiht eine Anforderung zur Ausführung durch den Arbeitsthread in die Warteschlange ein.

## <a name="syntax"></a>Syntax


```C++
void PutThreadMsg(
   UINT     uMsg,
   DWORD    dwMsgFlags,
   LPVOID   lpMsgParam,
   CAMEvent *pEvent = NULL
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*uMsg* 
</dt> <dd>

Anforderungscode.

</dd> <dt>

*dwMsgFlags* 
</dt> <dd>

Optionaler Flagparameter.

</dd> <dt>

*lpMsgParam* 
</dt> <dd>

Optionaler Zeiger auf einen Datenblock, der zusätzliche Parameter oder Rückgabewerte enthält. Muss statisch oder heap-zugeordnet und nicht automatisch sein.

</dd> <dt>

*pEvent* 
</dt> <dd>

Optionaler Zeiger auf ein Ereignisobjekt, das nach Abschluss signalisiert werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Memberfunktion reiht eine Anforderung zur Ausführung durch den Arbeitsthread in die Warteschlange ein. Die Parameter dieser Memberfunktion werden in die Warteschlange gestellt (in einem [**CMsg-Objekt)**](cmsg.md) und an die [**CMsgThread::ThreadMessageProc-Memberfunktion**](cmsgthread-threadmessageproc.md) des Arbeitsthreads übergeben. Diese Memberfunktion gibt unmittelbar nach dem Einrücken der Anforderung in die Warteschlange zurück und wartet nicht, bis der Thread die Anforderung erfüllt. Die **CMsgThread::ThreadMessageProc-Memberfunktion** der abgeleiteten Klasse definiert die vier Parameter.

Diese Memberfunktion verwendet eine sichere Multithreadliste, sodass mehrere Aufrufe dieser Memberfunktion aus verschiedenen Threads sicher ausgeführt werden können.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Msgthrd.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CMsgThread-Klasse**](cmsgthread.md)
</dt> </dl>

 

 




