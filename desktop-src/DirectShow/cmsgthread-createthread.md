---
description: Erstellt einen Thread.
ms.assetid: 40785522-dc6e-41af-8b27-9e8875a0dd84
title: CMsgThread.CreateThread-Methode (Msgthrd.h)
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
ms.openlocfilehash: 3681716af79d0c47ae08371caa2d03d236b9748d98b08098d7a6834a93ed9b2b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119831870"
---
# <a name="cmsgthreadcreatethread-method"></a>CMsgThread.CreateThread-Methode

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
| <dl> <dt>TRUE!</dt> </dl>  | Der Thread wurde erfolgreich erstellt.<br/>     |
| <dl> <dt>FALSE!</dt> </dl> | Der Thread wurde nicht erfolgreich erstellt.<br/> |



 

## <a name="remarks"></a>Hinweise

Der Thread wird eine Schleife durchlaufen, die blockiert, bis eine Anforderung in die Warteschlange eingereiht wird (über die [**Memberfunktion CMsgThread::P utThreadMsg)**](cmsgthread-putthreadmsg.md) und dann die [**CMsgThread::ThreadMessageProc-Memberfunktion**](cmsgthread-threadmessageproc.md) mit jeder Nachricht aufruft.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Msgthrd.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CMsgThread-Klasse**](cmsgthread.md)
</dt> </dl>

 

 




