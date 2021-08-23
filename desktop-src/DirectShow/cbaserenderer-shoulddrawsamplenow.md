---
description: Die ShouldDrawSampleNow-Methode bestimmt, wie ein Beispiel für das Rendering geplant wird.
ms.assetid: 92994f1f-53d5-42d4-90a2-2984b693e4c0
title: CBaseRenderer.ShouldDrawSampleNow-Methode (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.ShouldDrawSampleNow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 818a7682fed504028ebee1c3a5ff5d35a268e1daad8756b110bcfcb2ca8d9f80
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016868"
---
# <a name="cbaserenderershoulddrawsamplenow-method"></a>CBaseRenderer.ShouldDrawSampleNow-Methode

Die `ShouldDrawSampleNow` -Methode bestimmt, wie ein Beispiel für das Rendering geplant wird.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT ShouldDrawSampleNow(
   IMediaSample   *pMediaSample,
   REFERENCE_TIME *pStartTime,
   REFERENCE_TIME *pEndTime
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pMediaSample* 
</dt> <dd>

Zeiger auf die [**IMediaSample-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-imediasample) des Beispiels.

</dd> <dt>

*pStartTime* 
</dt> <dd>

Zeiger auf eine Variable, die die Startzeit des Beispiels enthält.

</dd> <dt>

*pEndTime* 
</dt> <dd>

Zeiger auf eine Variable, die die Endzeit des Beispiels enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt S \_ FALSE zurück. Wenn die abgeleitete Klasse diese Methode überschreibt, geben Sie einen der in der folgenden Tabelle aufgeführten Werte zurück.



| Rückgabecode                                                                               | Beschreibung                                                                        |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Das Beispiel sollte sofort gerendert werden.<br/>                              |
| <dl> <dt>**S \_ FALSE**</dt> </dl>   | Das Beispiel sollte basierend auf den Zeitstempeln für das Rendering geplant werden.<br/> |
| <dl> <dt>**Fehlercode**</dt> </dl> | Rendern Sie dieses Beispiel nicht.<br/>                                              |



 

## <a name="remarks"></a>Hinweise

Die [**CBaseRenderer::GetSampleTimes-Methode**](cbaserenderer-getsampletimes.md) ruft diese Methode auf. Standardmäßig werden Stichproben immer basierend auf ihren Zeitstempeln für das Rendering geplant. Die abgeleitete Klasse kann diese Methode überschreiben. beispielsweise, um die Qualitätskontrolle zu implementieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseRenderer-Klasse**](cbaserenderer.md)
</dt> </dl>

 

 




