---
description: Handle für den Thread.
ms.assetid: 93d1182a-58f0-4570-8568-fe0fded762cb
title: CABThread::m_hThread-Member (Wxutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_hThread
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f7293a97373a53d102887e5958c4296aff3dcfe3d392c80492ed773af62a8f11
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118158911"
---
# <a name="camthreadm_hthread-member"></a>ELEMENTSThread::m \_ hThread-Member

Handle für den Thread.

## <a name="syntax"></a>Syntax


```C++
HANDLE m_hThread;
```



## <a name="remarks"></a>Hinweise

Diese Variable wird als **NULL** initialisiert. Die [**METHODE VONTHREAD::Create**](camthread-create.md) legt diese Variable auf das Threadhandle fest. Um zu bestimmen, ob der Thread vorhanden ist, rufen Sie die [**METHODE BEDThread::ThreadExists auf.**](camthread-threadexists.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wxutil.h (include Streams.h)</dt> </dl>                                                                                    |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**WEBCAMThread-Klasse**](camthread.md)
</dt> </dl>

 

 




