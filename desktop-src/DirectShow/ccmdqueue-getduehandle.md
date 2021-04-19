---
description: Die getduehandle-Methode ruft das Ereignis Handle ab, das signalisiert werden soll.
ms.assetid: 495ea76d-8b94-48a9-8025-06ab18b66693
title: Ccmdqueue. getduehandle-Methode (winutil. h)
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
ms.openlocfilehash: 4cb7c8c965c72abe6343a8a75863e0e6969dc5c6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106350769"
---
# <a name="ccmdqueuegetduehandle-method"></a>Ccmdqueue. getduehandle-Methode

Die- `GetDueHandle` Methode ruft das Ereignis Handle ab, das signalisiert werden soll.

## <a name="syntax"></a>Syntax


```C++
HANDLE GetDueHandle();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt das Ereignis Handle zurück.

## <a name="remarks"></a>Bemerkungen

Gibt das Ereignis Handle zurück, wenn verzögerte Befehle vorhanden sind, die für die Ausführung fällig sind (wenn [**ccmdqueue:: getduecommand**](ccmdqueue-getduecommand.md) nicht blockiert wird).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Winutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ccmdqueue-Klasse**](ccmdqueue.md)
</dt> </dl>

 

 




