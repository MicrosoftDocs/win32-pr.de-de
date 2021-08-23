---
description: Die SetSink-Methode legt das IQualityControl-Objekt fest, das Qualitätsmeldungen empfängt.
ms.assetid: f5789781-1871-4fea-9d1f-bd1a21b70439
title: CBaseVideoRenderer.SetSink-Methode (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.SetSink
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5b5fef3eb6bd1b959c6c7246e4aeebf5b42a01ddcecd211f3e1d7860102a6381
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119697900"
---
# <a name="cbasevideorenderersetsink-method"></a>CBaseVideoRenderer.SetSink-Methode

Die `SetSink` -Methode legt das [**IQualityControl-Objekt**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) fest, das Qualitätsmeldungen empfängt.

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

Zeiger auf das [**IQualityControl-Objekt,**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) an das die Benachrichtigungen gesendet werden sollen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück.

## <a name="remarks"></a>Hinweise

Diese Memberfunktion implementiert die [**IQualityControl::SetSink-Methode**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink) für den Videorenderer.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseVideoRenderer-Klasse**](cbasevideorenderer.md)
</dt> </dl>

 

 




