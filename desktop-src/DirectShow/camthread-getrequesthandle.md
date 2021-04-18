---
description: 'Die getrequesthandle-Methode ruft ein Handle für das Ereignis ab, das von der camthread:: callworker-Methode signalisiert wird.'
ms.assetid: 6e4496ae-a635-4b55-ae7a-31748f21068b
title: Camthread. getrequesthandle-Methode (wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.GetRequestHandle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 051a6a3e3daed1dae6df3bdbb42e36f07b852d85
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358676"
---
# <a name="camthreadgetrequesthandle-method"></a>Camthread. getrequesthandle-Methode

Die- `GetRequestHandle` Methode ruft ein Handle für das-Ereignis ab, das von der [**camthread:: callworker**](camthread-callworker.md) -Methode signalisiert wird.

## <a name="syntax"></a>Syntax


```C++
HANDLE GetRequestHandle() const;
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt ein Ereignis Handle zurück.

## <a name="remarks"></a>Bemerkungen

Die Klasse "camevent" behält ein privates Manuelles Zurücksetzungs Ereignis bei, das von callworker festgelegt und durch die Methode " [**camthread:: Reply**](camthread-reply.md) " zurückgesetzt wird.

Wenn Sie eine Funktion wie WaitForMultipleObjects aufrufen, verwenden Sie getrequesthandle, um das Ereignis Handle abzurufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil. h (Include Streams. h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Camthread-Klasse**](camthread.md)
</dt> </dl>

 

 




