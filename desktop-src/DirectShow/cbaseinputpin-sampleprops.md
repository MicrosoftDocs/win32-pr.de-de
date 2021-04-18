---
description: Die sampleproperties-Methode ruft die Eigenschaften des neuesten Beispiels in einer am \_ SAMPLE2 \_ Properties-Struktur ab.
ms.assetid: d4c98c35-f8b2-4111-bae9-4e0f58a0cc8a
title: Cbaseingeputpin. samplerequismethode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.SampleProps
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 45663cfd221c7a31abe5f85a494869b24d1ddd8e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371343"
---
# <a name="cbaseinputpinsampleprops-method"></a>Cbaseingeputpin. samplerequismethode

Die- `SampleProps` Methode ruft die Eigenschaften des neuesten Beispiels in einer [**am \_ SAMPLE2 \_ Properties**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) -Struktur ab.

## <a name="syntax"></a>Syntax


```C++
AM_SAMPLE2_PROPERTIES* SampleProps();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt die Adresse der [**cbaseingeputpin:: m \_ samplerequis-Member**](cbaseinputpin-m-sampleprops.md) -Variable zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbaseingeputpin-Klasse**](cbaseinputpin.md)
</dt> </dl>

 

 




