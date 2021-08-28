---
description: Optionales Ereignis, das signalisiert wird, wenn das Objekt ein Beispiel aus der Warteschlange entfernt. Der Wert ist anfänglich NULL. Rufen Sie die COutputQueue::SetPopEvent-Methode auf, um ein Ereignishand handle anzugeben.
ms.assetid: f2602532-b045-4384-b87c-b28cc34c81b0
title: COutputQueue::m_hEventPop Member (Outputq.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_hEventPop
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bb401cf9755260c797ebfb382d9f2248d9d04c5f8d9e9b49e319c390de1664c5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087210"
---
# <a name="coutputqueuem_heventpop-member"></a>COutputQueue::m \_ hEventPop-Member

Optionales Ereignis, das signalisiert wird, wenn das Objekt ein Beispiel aus der Warteschlange entfernt. Der Wert ist anfänglich **NULL.** Rufen Sie die [**COutputQueue::SetPopEvent-Methode**](coutputqueue-setpopevent.md) auf, um ein Ereignishand handle anzugeben.

## <a name="syntax"></a>Syntax


```C++
HANDLE m_hEventPop;
```



## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Outputq.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**COutputQueue-Klasse**](coutputqueue.md)
</dt> </dl>

 

 




