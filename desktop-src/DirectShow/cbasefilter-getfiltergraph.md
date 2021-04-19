---
description: Die getfiltergraph-Methode ruft einen Zeiger auf den Filter Diagramm-Manager ab.
ms.assetid: 80b41272-2ca1-40db-8624-0d99d66f3c34
title: Cbasefilter. getfiltergraph-Methode (amfilter. h)
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
ms.openlocfilehash: c0843c7789afc1500565d2737d863cbc8af114d4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370153"
---
# <a name="cbasefiltergetfiltergraph-method"></a>Cbasefilter. getfiltergraph-Methode

Die- `GetFilterGraph` Methode ruft einen Zeiger auf den Filter Diagramm-Manager ab.

## <a name="syntax"></a>Syntax


```C++
IFilterGraph* GetFilterGraph();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt den Wert von [**cbasefilter:: m \_ PGraph**](cbasefilter-m-pgraph.md)zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasefilter-Klasse**](cbasefilter.md)
</dt> </dl>

 

 




