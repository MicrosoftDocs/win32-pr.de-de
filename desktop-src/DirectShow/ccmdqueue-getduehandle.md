---
description: Die GetDueHandle-Methode ruft das zu signalisierende Ereignishandle ab.
ms.assetid: 495ea76d-8b94-48a9-8025-06ab18b66693
title: CCmdQueue.GetDueHandle-Methode (Winutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.GetDueHandle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 62fbe0e38e24891add93e63e0c03d521289ed345078e8e567a376e9bd639d997
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016418"
---
# <a name="ccmdqueuegetduehandle-method"></a>CCmdQueue.GetDueHandle-Methode

Die `GetDueHandle` -Methode ruft das Ereignishand handle ab, das signalisiert werden soll.

## <a name="syntax"></a>Syntax


```C++
HANDLE GetDueHandle();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt das Ereignishand handle zurück.

## <a name="remarks"></a>Hinweise

Gibt das Ereignishandler zurück, wenn verzögerte Befehle zur Ausführung fällig sind (wenn [**CCmdQueue::GetDueCommand**](ccmdqueue-getduecommand.md) nicht blockiert wird).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CCmdQueue-Klasse**](ccmdqueue.md)
</dt> </dl>

 

 




