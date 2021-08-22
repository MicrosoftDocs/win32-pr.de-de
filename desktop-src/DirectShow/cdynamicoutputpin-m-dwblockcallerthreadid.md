---
description: Der Bezeichner des Threads, der zuletzt die IPinFlowControl::Block-Methode auf diesem Pin aufgerufen hat. Diese Membervariable ist nur gültig, während die Stecknadel blockiert wird.
ms.assetid: 7f8429c5-7e58-49a1-9f36-01088379a193
title: CDynamicOutputPin::m_dwBlockCallerThreadID-Member (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_dwBlockCallerThreadID
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b52bd7f718798ea9dd2cf9d227f6d22e069d2c1a59bb8591f6126c20599af9f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119539750"
---
# <a name="cdynamicoutputpinm_dwblockcallerthreadid-member"></a>CDynamicOutputPin::m \_ dwBlockCallerThreadID-Member

Der Bezeichner des Threads, der zuletzt die [**IPinFlowControl::Block-Methode**](/windows/desktop/api/Strmif/nf-strmif-ipinflowcontrol-block) auf diesem Pin aufgerufen hat. Diese Membervariable ist nur gültig, während die Stecknadel blockiert wird.

## <a name="syntax"></a>Syntax


```C++
DWORD m_dwBlockCallerThreadID;
```



## <a name="remarks"></a>Hinweise

Bevor Sie auf diese Variable zugreifen, speichern Sie den kritischen Abschnitt [**CDynamicOutputPin::m \_ BlockStateLock.**](cdynamicoutputpin-m-blockstatelock.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CDynamicOutputPin-Klasse**](cdynamicoutputpin.md)
</dt> </dl>

 

 




