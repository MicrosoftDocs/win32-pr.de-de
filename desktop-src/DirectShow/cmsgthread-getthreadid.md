---
description: Ruft den Bezeichner des Threads ab.
ms.assetid: c2b25342-841a-46cb-862c-01761fc60363
title: CMsgThread.GetThreadID-Methode (Msgthrd.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.GetThreadID
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4f3b0837a7f050f09794b06e490f45012e0704e187b02668cd2af2a5bf8edf34
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119214099"
---
# <a name="cmsgthreadgetthreadid-method"></a>CMsgThread.GetThreadID-Methode

Ruft den Bezeichner des Threads ab.

## <a name="syntax"></a>Syntax


```C++
DWORD GetThreadID();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt den **privaten m \_ ThreadId-Daten** member zurück.

## <a name="remarks"></a>Hinweise

Diese Funktion gibt den Microsoft Win32-Bezeichner für den Arbeitsthread zurück. Sie können diese Memberfunktion entweder für den Arbeitsthread oder einen Clientthread aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Msgthrd.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CMsgThread-Klasse**](cmsgthread.md)
</dt> </dl>

 

 




