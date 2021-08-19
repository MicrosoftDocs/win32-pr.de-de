---
description: Medienbeispielwarteschlange.
ms.assetid: 910f1c0c-2ce9-452f-a97b-aa424da9a93e
title: COutputQueue::m_List Member (Outputq.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_List
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3e261116961f23c845ec2e27c6f20748b2c50cd9c036d9bc7d42bfe24b9b4fb9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087070"
---
# <a name="coutputqueuem_list-member"></a>COutputQueue::m \_ List-Member

Medienbeispielwarteschlange.

## <a name="syntax"></a>Syntax


```C++
CSampleList *m_List;
```



## <a name="remarks"></a>Hinweise

Diese Membervariable ist ein Zeiger auf ein [**CGenericList-Objekt,**](cgenericlist.md) das [**IMediaSample-Zeiger**](/windows/desktop/api/Strmif/nn-strmif-imediasample) enthält. Der **CSampleList-Typ** ist wie folgt definiert:

``` syntax
typedef CGenericList<IMediaSample> CSampleList;
```

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Outputq.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**COutputQueue-Klasse**](coutputqueue.md)
</dt> </dl>

 

 




