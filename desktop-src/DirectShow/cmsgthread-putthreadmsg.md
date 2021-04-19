---
description: Fügt eine Anforderung zur Ausführung durch den Arbeits Thread in die Warteschlange ein.
ms.assetid: a854f962-143d-4776-bf98-119d003867df
title: Cmsgthread. putthreadmsg-Methode (msgthrd. h)
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
ms.openlocfilehash: 3445d9af4ec9c7abe6a4401e219fc305e254d555
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372199"
---
# <a name="cmsgthreadputthreadmsg-method"></a>Cmsgthread. putthreadmsg-Methode

Fügt eine Anforderung zur Ausführung durch den Arbeits Thread in die Warteschlange ein.

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

*Umschlag* 
</dt> <dd>

Anforderungs Code.

</dd> <dt>

*dwmsgflags* 
</dt> <dd>

Optionaler Flags-Parameter.

</dd> <dt>

*lpmsgparam* 
</dt> <dd>

Optionaler Zeiger auf einen Datenblock mit zusätzlichen Parametern oder Rückgabe Werten. Muss statisch oder Heap zugeordnet sein, nicht automatisch.

</dd> <dt>

*Peer Event* 
</dt> <dd>

Optionaler Zeiger auf ein Ereignis Objekt, das nach Abschluss signalisiert werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Member-Funktion fügt eine Anforderung zur Ausführung durch den Arbeits Thread in die Warteschlange ein. Die Parameter dieser Member-Funktion werden in die Warteschlange eingereiht (in einem [**CMSG**](cmsg.md) -Objekt) und an die [**cmsgthread:: threadmessageproc**](cmsgthread-threadmessageproc.md) -Member-Funktion des Arbeits Thread übergeben. Diese Member-Funktion gibt sofort zurück, nachdem die Anforderung in die Warteschlange eingereiht wurde, und wartet nicht, bis der Thread die Anforderung erfüllt. Die **cmsgthread:: threadmessageproc** -Member-Funktion der abgeleiteten Klasse definiert die vier Parameter.

Diese Member-Funktion verwendet eine Multithreadsichere Liste, sodass mehrere Aufrufe dieser Element Funktion aus unterschiedlichen Threads sicher durchgeführt werden können.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Msgthrd. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cmsgthread-Klasse**](cmsgthread.md)
</dt> </dl>

 

 




