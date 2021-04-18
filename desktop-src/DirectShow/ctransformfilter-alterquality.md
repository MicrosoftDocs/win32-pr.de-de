---
description: Die alterquality-Methode benachrichtigt den Filter, dass eine Qualitätsänderung angefordert wird.
ms.assetid: 46743d6b-65cf-4d63-8913-114277d76da4
title: Ctransformfilter. alterquality-Methode (Transfrm. h)
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
ms.openlocfilehash: 592fc67dd5cee5e4f76b8171b6e842532d71371b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364843"
---
# <a name="ctransformfilteralterquality-method"></a>Ctransformfilter. alterquality-Methode

Die- `AlterQuality` Methode benachrichtigt den Filter, dass eine Qualitätsänderung angefordert wird.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT AlterQuality(
   Quality q
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Q1* 
</dt> <dd>

[**Qualitäts**](/windows/win32/api/strmif/ns-strmif-quality) Struktur, die die Qualitäts Steuerungs Meldung enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Mögliche Werte sind in der folgenden Tabelle aufgeführt.



| Rückgabecode                                                                             | Beschreibung                                                                           |
|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | Die Qualitäts Meldung konnte nicht verarbeitet werden. Die Nachricht sollte per Upstream übermittelt werden.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Die Qualitäts Meldung wurde verarbeitet. Es sind keine weiteren Aktionen erforderlich.<br/>               |



 

## <a name="remarks"></a>Bemerkungen

Überschreiben Sie diese Methode, wenn der Filter die Qualitätskontrolle ausführen kann. Weitere Informationen finden Sie unter [Qualitäts Steuerungs Verwaltung](quality-control-management.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Transfrm. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ctransformfilter-Klasse**](ctransformfilter.md)
</dt> </dl>

 

 




