---
description: Ruft das Handle für den Thread im cmsgthread-Objekt ab.
ms.assetid: dacbdc68-91a0-46d4-805f-fe51cb047e19
title: Cmsgthread. getthreadhandle-Methode (msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.GetThreadHandle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b61d7bfb11f78be3c1d23275589c8cb1c62259bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354209"
---
# <a name="cmsgthreadgetthreadhandle-method"></a>Cmsgthread. getthreadhandle-Methode

Ruft das Handle für den Thread im [**cmsgthread**](cmsgthread.md) -Objekt ab.

## <a name="syntax"></a>Syntax


```C++
HANDLE GetThreadHandle();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt das Thread Handle zurück.

## <a name="remarks"></a>Bemerkungen

Das Thread Handle kann an Wait-Funktionen wie [**WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects)übermittelt werden. Das Thread Handle wird signalisiert, wenn der Thread beendet wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Msgthrd. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cmsgthread-Klasse**](cmsgthread.md)
</dt> </dl>

 

