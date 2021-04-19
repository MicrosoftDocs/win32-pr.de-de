---
description: Die Methode "beenden" beendet den Filter.
ms.assetid: 80eac207-5db3-4b06-bbae-eca72e37d09d
title: Cbaserenderer. stoppt-Methode (renbase. h)
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
ms.openlocfilehash: ddd8194bbf76c4a4311aa90335f94d1e7548a356
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367113"
---
# <a name="cbaserendererstop-method"></a>Cbaserenderer. stoppt-Methode

Die- `Stop` Methode beendet den Filter.

## <a name="syntax"></a>Syntax


```C++
HRESULT Stop();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Bemerkungen

Diese Methode überschreibt die [**cbasefilter:: stopmethode**](cbasefilter-stop.md) . Es führt die folgenden Aktionen aus:

-   Ruft [**cbasefilter:: Beendigung**](cbasefilter-stop.md)auf.
-   Führt einen Commit für die Zuweisung aus. (Weitere Informationen finden Sie unter [**imemzuzukator::D ecommit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-decommit).)
-   Bricht das geplante Rendering ab und gibt den streamingingthread frei.
-   Wartet, bis alle ausstehenden **Empfangs** Aufrufe abgeschlossen sind.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbaserderderer-Klasse**](cbaserenderer.md)
</dt> </dl>

 

 




