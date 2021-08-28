---
description: Die Create-Methode erstellt den Thread.
ms.assetid: 453972eb-7cf6-43c6-820e-c1992675260e
title: WEBCAMThread.Create-Methode (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.Create
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 135af6dd12bb53a2fa1e7ec14425c12e1c0bcc99bf9c82ce7aeaccb72df544f2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103320"
---
# <a name="camthreadcreate-method"></a>CAMThread.Create-Methode

Die `Create` -Methode erstellt den Thread.

## <a name="syntax"></a>Syntax


```C++
BOOL Create();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE zurück,** wenn erfolgreich, andernfalls **FALSE.**

## <a name="remarks"></a>Hinweise

Diese Methode erstellt den Thread mithilfe der [**METHODE WEBCAMThread::InitialThreadProc**](camthread-initialthreadproc.md) für die Threadprozedur und `this` für das Threadargument.

Die Methode schlägt fehl, wenn der Thread bereits vorhanden ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CAMThread-Klasse**](camthread.md)
</dt> </dl>

 

 




