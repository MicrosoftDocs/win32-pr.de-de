---
description: Erstellt einen Thread.
ms.assetid: 40785522-dc6e-41af-8b27-9e8875a0dd84
title: Cmsgthread. kreatethread-Methode (msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.CreateThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8951995de18158fe4d1e5f84b1d98da701067ab6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368562"
---
# <a name="cmsgthreadcreatethread-method"></a>Cmsgthread. kreatethread-Methode

Erstellt einen Thread.

## <a name="syntax"></a>Syntax


```C++
BOOL CreateThread();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen der folgenden Werte zurück.



| Rückgabecode                                                                              | Beschreibung                                     |
|------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <dt>TRUE * * * *</dt> </dl>  | Der Thread wurde erfolgreich erstellt.<br/>     |
| <dl> <dt>FALSE * * * *</dt> </dl> | Der Thread wurde nicht erfolgreich erstellt.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Der Thread führt eine Schleife aus, blockiert Sie, bis eine Anforderung in die Warteschlange eingereiht wird (über die Member-Funktion [**cmsgthread::P utthreadmsg**](cmsgthread-putthreadmsg.md) ) und ruft dann die [**cmsgthread:: threadmessageproc**](cmsgthread-threadmessageproc.md) -Member-Funktion für jede Nachricht auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Msgthrd. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cmsgthread-Klasse**](cmsgthread.md)
</dt> </dl>

 

 




