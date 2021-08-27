---
description: Die SetSink-Methode legt einen externen Qualitäts-Manager fest. Diese Methode implementiert die IQualityControl::SetSink-Methode.
ms.assetid: 714e6839-954e-4231-824d-72a45f270f59
title: CBasePin.SetSink-Methode (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.SetSink
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6e94dc561e378ab526eee04f82e0f54a90889ee4396996d96d01f6c8da8c34d4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108630"
---
# <a name="cbasepinsetsink-method"></a>CBasePin.SetSink-Methode

Die `SetSink` -Methode legt einen externen Qualitäts-Manager fest. Diese Methode implementiert die [**IQualityControl::SetSink-Methode.**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink)

## <a name="syntax"></a>Syntax


```C++
HRESULT SetSink(
   IQualityControl *piqc
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*piqc* 
</dt> <dd>

Zeiger auf die [**IQualityControl-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) des Qualitäts-Managers.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ OK zurück.

## <a name="remarks"></a>Hinweise

Rufen Sie diese Methode auf, um Qualitätskontrollnachrichten an einen externen Qualitätsmanager umzuleiten. Weitere Informationen finden Sie unter [Qualitätskontrollverwaltung.](quality-control-management.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBasePin-Klasse**](cbasepin.md)
</dt> </dl>

 

 




