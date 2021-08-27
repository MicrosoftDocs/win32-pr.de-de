---
description: Flag, das angibt, ob das Objekt Stichproben in genauen Batches liefert.
ms.assetid: 1a37c78f-4499-4ebb-92b4-b71ba3ff1a02
title: COutputQueue::m_bBatchExact Member (Outputq.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bBatchExact
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6b5859744c3670ccc789ae5d87a619b3b32c3731580d473ff8cc6d775348771f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087250"
---
# <a name="coutputqueuem_bbatchexact-member"></a>COutputQueue::m \_ bBatchExact-Member

Flag, das angibt, ob das Objekt Stichproben in genauen Batches liefert.

## <a name="syntax"></a>Syntax


```C++
const BOOL m_bBatchExact;
```



## <a name="remarks"></a>Hinweise

Wenn der Wert **TRUE ist,** wartet das Objekt, bis es über einen vollständigen Batch von Medienbeispielen verfügt, bevor ein beliebiges -Objekt zutrifft. Andernfalls werden Stichproben bei Ihrer Ankunft zu verfügung stellt. Die [**COutputQueue::m \_ lBatchSize-Membervariable**](coutputqueue-m-lbatchsize.md) definiert die Batchgröße.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Outputq.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**COutputQueue-Klasse**](coutputqueue.md)
</dt> </dl>

 

 




