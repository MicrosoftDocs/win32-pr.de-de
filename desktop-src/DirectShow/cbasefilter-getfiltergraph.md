---
description: Die GetFilterGraph-Methode ruft einen Zeiger auf den Filterdiagramm-Manager ab.
ms.assetid: 80b41272-2ca1-40db-8624-0d99d66f3c34
title: CBaseFilter.GetFilterGraph-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetFilterGraph
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6f35b40febff058d5bbd9f48c5ac6d10168d48d6e587b51ab2730704724e48c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056650"
---
# <a name="cbasefiltergetfiltergraph-method"></a>CBaseFilter.GetFilterGraph-Methode

Die `GetFilterGraph` -Methode ruft einen Zeiger auf den Filterdiagramm-Manager ab.

## <a name="syntax"></a>Syntax


```C++
IFilterGraph* GetFilterGraph();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt den Wert von [**CBaseFilter::m \_ pGraph zurück.**](cbasefilter-m-pgraph.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseFilter-Klasse**](cbasefilter.md)
</dt> </dl>

 

 




