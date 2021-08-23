---
description: Kritischer Abschnitt, der den Zugriff auf den Thread durch andere Threads sperrt.
ms.assetid: 9bc360be-52d6-4db1-b384-8bc9e25c0914
title: CAMThread::m_AccessLock-Member (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_AccessLock
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 72e5823b7acadd3c1c0f3752606825d1b2981aac4a64903c5944e3df82252aaa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119017598"
---
# <a name="camthreadm_accesslock-member"></a>ACCESSThread::m \_ AccessLock-Member

Kritischer Abschnitt, der den Zugriff auf den Thread durch andere Threads sperrt.

## <a name="syntax"></a>Syntax


```C++
CCritSec m_AccessLock;
```



## <a name="remarks"></a>Hinweise

Die [**MethodenCAMThread::Create**](camthread-create.md) und [**WEBCAMThread::CallWorker**](camthread-callworker.md) halten diese Sperre, um Vorgänge für den Thread zu serialisieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CAMThread-Klasse**](camthread.md)
</dt> </dl>

 

 




