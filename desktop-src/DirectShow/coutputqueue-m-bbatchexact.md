---
description: Flag, das angibt, ob das Objekt Stichproben in exakten Batches bereitstellt.
ms.assetid: 1a37c78f-4499-4ebb-92b4-b71ba3ff1a02
title: 'Coutputqueue:: m_bBatchExact-Member (outputq. h)'
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
ms.openlocfilehash: a5f38d8a0e7335025688f52015ff9ed4d4892820
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372643"
---
# <a name="coutputqueuem_bbatchexact-member"></a>Coutputqueue:: m \_ bbatchexact-Member

Flag, das angibt, ob das Objekt Stichproben in exakten Batches bereitstellt.

## <a name="syntax"></a>Syntax


```C++
const BOOL m_bBatchExact;
```



## <a name="remarks"></a>Bemerkungen

Wenn der Wert **true** ist, wartet das Objekt, bis es über einen kompletten Batch von Medien Beispielen verfügt, bevor es bereitgestellt wird. Andernfalls werden bei ihrer Ankunft Beispiele bereitstellt. Die Element Variable [**coutputqueue:: m \_ lbatchsize**](coutputqueue-m-lbatchsize.md) definiert die Batch Größe.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Outputq. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Coutputqueue-Klasse**](coutputqueue.md)
</dt> </dl>

 

 




