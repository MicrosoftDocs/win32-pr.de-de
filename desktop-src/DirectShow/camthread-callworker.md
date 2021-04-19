---
description: Die callworker-Methode signalisiert dem Thread eine Anforderung.
ms.assetid: 51431688-bf55-4778-afc0-91b6ab336aa3
title: Camthread. callworker-Methode (wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.CallWorker
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7410fbee4ece729d1579f525731bddaceded1153
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372668"
---
# <a name="camthreadcallworker-method"></a>Camthread. callworker-Methode

Die- `CallWorker` Methode signalisiert dem Thread eine-Anforderung.

## <a name="syntax"></a>Syntax


```C++
DWORD CallWorker(
   DWORD dwParam
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dwparam* 
</dt> <dd>

Anforderungs Parameter. Die abgeleitete Klasse definiert die Bedeutung des Parameters.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen Wert zurück, der von der abgeleiteten Klasse definiert wird.

## <a name="remarks"></a>Bemerkungen

Die Methoden " [**camthread:: GetRequest**](camthread-getrequest.md) " und " [**camthread:: CheckRequest**](camthread-checkrequest.md) " rufen den Wert des Parameters " *dwparam* " ab. Die GetRequest-Methode blockiert, bis `CallWorker` aufgerufen wird.

Diese Methode wird blockiert, bis die Methode " [**camthread:: Reply**](camthread-reply.md) " aufgerufen wird. Der Rückgabewert ist der Parameter, der für die Antwort angegeben wird.

Diese Methode enthält die " [**camthread:: m \_ accesslock**](camthread-m-accesslock.md) "-Sperre zum Serialisieren von Anforderungen. Daher müssen Sie diese Methode aus dem Thread selbst oder aus einer beliebigen Member-Funktion, die im Kontext des Threads ausgeführt wird, abrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Camthread-Klasse**](camthread.md)
</dt> </dl>

 

 




