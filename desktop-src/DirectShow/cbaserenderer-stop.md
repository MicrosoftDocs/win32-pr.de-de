---
description: Die Stop-Methode beendet den Filter.
ms.assetid: 80eac207-5db3-4b06-bbae-eca72e37d09d
title: CBaseRenderer.Stop-Methode (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Stop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 942fae3ee1ea2c7481f475dc2d8dba421fd21d44290c98b822b9bc489ee25334
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117822620"
---
# <a name="cbaserendererstop-method"></a>CBaseRenderer.Stop-Methode

Die `Stop` -Methode beendet den Filter.

## <a name="syntax"></a>Syntax


```C++
HRESULT Stop();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Hinweise

Diese Methode überschreibt die [**CBaseFilter::Stop-Methode.**](cbasefilter-stop.md) Es führt die folgenden Aktionen aus:

-   Ruft [**CBaseFilter::Stop auf.**](cbasefilter-stop.md)
-   Dekommitiert die Zuweisung. (Siehe [**IMemAllocator::D ecommit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit).)
-   Bricht alle geplanten Renderings ab und gibt den Streamingthread frei.
-   Wartet auf den  Abschluss eines ausstehenden Empfangsaufrufs.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseRenderer-Klasse**](cbaserenderer.md)
</dt> </dl>

 

 




