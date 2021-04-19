---
description: Ruft ein CMSG-Objekt in der Warteschlange ab, das eine Anforderung enthält.
ms.assetid: 65b76121-c21c-4525-8dde-138783a4964e
title: Cmsgthread. getthreadmsg-Methode (msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.GetThreadMsg
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1b1851ac36590992aca6fa4413119be1df7427bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365472"
---
# <a name="cmsgthreadgetthreadmsg-method"></a>Cmsgthread. getthreadmsg-Methode

Ruft ein [**CMSG**](cmsg.md) -Objekt in der Warteschlange ab, das eine Anforderung enthält.

## <a name="syntax"></a>Syntax


```C++
virtual void GetThreadMsg(
   CMsg *msg
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*msg* 
</dt> <dd>

Zeiger auf ein zugeordneter [**CMSG**](cmsg.md) -Objekt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Member-Funktion wird von der privaten [**ThreadProc**](camthread-threadproc.md) -Funktion des Arbeitsthreads aufgerufen, um die nächste Member-Funktion abzurufen. Der *msg* -Parameter sollte auf ein zugeordneter [**CMSG**](cmsg.md) -Objekt zeigen, das mit den Parametern der nächsten Anforderung in der Warteschlange aufgefüllt wird. Wenn keine Anforderungen in der Warteschlange vorliegen, wird diese Element Funktion blockiert, bis die nächste Anforderung in die Warteschlange eingereiht wird (durch einen aufrufenden Befehl der [**cmsgthread::P utthreadmsg**](cmsgthread-putthreadmsg.md) -Member-Funktion).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Msgthrd. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cmsgthread-Klasse**](cmsgthread.md)
</dt> </dl>

 

 




