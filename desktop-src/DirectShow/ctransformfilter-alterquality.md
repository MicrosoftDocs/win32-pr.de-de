---
description: Die AlterQuality-Methode benachrichtigt den Filter, dass eine Qualitätsänderung angefordert wird.
ms.assetid: 46743d6b-65cf-4d63-8913-114277d76da4
title: CTransformFilter.AlterQuality-Methode (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.AlterQuality
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 06b9b136217c23f64bcd779f5c96189ca993646ffb29ce5316cf5913de8c9abd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119317150"
---
# <a name="ctransformfilteralterquality-method"></a>CTransformFilter.AlterQuality-Methode

Die `AlterQuality` -Methode benachrichtigt den Filter, dass eine Qualitätsänderung angefordert wird.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT AlterQuality(
   Quality q
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Q* 
</dt> <dd>

[**Qualitätsstruktur,**](/windows/win32/api/strmif/ns-strmif-quality) die die Qualitätskontrollmeldung enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Mögliche Werte sind die in der folgenden Tabelle gezeigten Werte.



| Rückgabecode                                                                             | Beschreibung                                                                           |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | Die Qualitätsmeldung wurde nicht verarbeitet. Die Nachricht sollte upstream übergeben werden.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Die Qualitätsmeldung wurde verarbeitet. Es sind keine weiteren Aktionen erforderlich.<br/>               |



 

## <a name="remarks"></a>Hinweise

Überschreiben Sie diese Methode, wenn der Filter die Qualitätskontrolle ausführen kann. Weitere Informationen finden Sie unter [Quality-Control Management](quality-control-management.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CTransformFilter-Klasse**](ctransformfilter.md)
</dt> </dl>

 

 




