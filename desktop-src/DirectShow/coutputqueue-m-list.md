---
description: Medien Beispiel Warteschlange.
ms.assetid: 910f1c0c-2ce9-452f-a97b-aa424da9a93e
title: 'Coutputqueue:: m_List-Member (outputq. h)'
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
ms.openlocfilehash: 32840ed0ed9f976cceb1e0dc6dc8debc3f774377
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368429"
---
# <a name="coutputqueuem_list-member"></a>Coutputqueue:: m- \_ Listenmember

Medien Beispiel Warteschlange.

## <a name="syntax"></a>Syntax


```C++
CSampleList *m_List;
```



## <a name="remarks"></a>Bemerkungen

Diese Member-Variable ist ein Zeiger auf ein [**cgenericlist**](cgenericlist.md) -Objekt, das [**imediasample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) -Zeiger enthält. Der **csamplelist** -Typ wird wie folgt definiert:

``` syntax
typedef CGenericList<IMediaSample> CSampleList;
```

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Outputq. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Coutputqueue-Klasse**](coutputqueue.md)
</dt> </dl>

 

 




