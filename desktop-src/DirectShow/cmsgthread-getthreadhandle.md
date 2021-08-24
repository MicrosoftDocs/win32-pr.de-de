---
description: Ruft das Handle für den Thread im CMsgThread-Objekt ab.
ms.assetid: dacbdc68-91a0-46d4-805f-fe51cb047e19
title: CMsgThread.GetThreadHandle-Methode (Msgthrd.h)
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
ms.openlocfilehash: 0ecb968156302c4fd1a8c48d1c6f3175977059298d2f6af5207abc376a6e107a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119585690"
---
# <a name="cmsgthreadgetthreadhandle-method"></a>CMsgThread.GetThreadHandle-Methode

Ruft das Handle für den Thread im [**CMsgThread-Objekt**](cmsgthread.md) ab.

## <a name="syntax"></a>Syntax


```C++
HANDLE GetThreadHandle();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt das Threadhand handle zurück.

## <a name="remarks"></a>Hinweise

Das Threadhandl kann an Wartefunktionen wie [**WaitForMultipleObjects übergeben werden.**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects) Das Threadhand handle wird signalisiert, wenn der Thread beendet wurde.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Msgthrd.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CMsgThread-Klasse**](cmsgthread.md)
</dt> </dl>

 

