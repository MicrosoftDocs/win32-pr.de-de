---
description: Die GetSampleTimes-Methode ruft die Zeitstempel aus einem Beispiel ab.
ms.assetid: a8fead22-a12c-489d-9c42-d5b61f480c25
title: CBaseRenderer.GetSampleTimes-Methode (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetSampleTimes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2d759cbcf2a9638b54e6194bcac7e7b24254c0d37987995d511fb4ffce85f1ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954959"
---
# <a name="cbaserenderergetsampletimes-method"></a>CBaseRenderer.GetSampleTimes-Methode

Die `GetSampleTimes` -Methode ruft die Zeitstempel aus einem Beispiel ab.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT GetSampleTimes(
   IMediaSample   *pMediaSample,
   REFERENCE_TIME *pStartTime,
   REFERENCE_TIME *pEndTime
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pMediaSample* 
</dt> <dd>

Zeiger auf die [**IMediaSample-Schnittstelle des**](/windows/desktop/api/Strmif/nn-strmif-imediasample) Beispiels.

</dd> <dt>

*pStartTime* 
</dt> <dd>

Zeiger auf eine Variable, die die Startzeit empfängt.

</dd> <dt>

*pEndTime* 
</dt> <dd>

Zeiger auf eine Variable, die die Endzeit empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Mögliche Werte sind die in der folgenden Tabelle gezeigten Werte.



| Rückgabecode                                                                                                    | Beschreibung                                                                        |
|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                           | Das Beispiel sollte sofort gerendert werden.<br/>                              |
| <dl> <dt>**S \_ FALSE**</dt> </dl>                        | Das Beispiel sollte basierend auf den Zeitstempeln für das Rendering geplant werden.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>                         | Rendern Sie dieses Beispiel nicht.<br/>                                              |
| <dl> <dt>**VFW \_ E \_ \_ STARTZEIT NACH \_ \_ ENDE**</dt> </dl> | Fehlerhafter Zeitstempel: Die Endzeit liegt vor der Startzeit.<br/>            |



 

## <a name="remarks"></a>Hinweise

Der Filter ruft diese Methode auf, um zu bestimmen, wie sie ein Beispiel behandeln soll. Wenn der Rückgabewert S \_ OK ist, rendert der Filter das Beispiel sofort. Wenn der Rückgabewert S FALSE ist, wird das Rendering des Beispiels basierend auf den \_ Zeitstempeln vom Filter geplant. Wenn der Rückgabewert ein Fehlercode ist, lehnt der Filter das Beispiel ab.

Diese Methode gibt S OK zurück, wenn das Beispiel über keine Zeitstempel verfügt oder wenn der Filter \_ keine Referenzuhr hat. Andernfalls wird der Wert der [**CBaseRenderer::ShouldDrawSampleNow-Methode**](cbaserenderer-shoulddrawsamplenow.md) zurückgegeben. In der Basisklasse gibt **ShouldDrawSampleNow** immer S \_ FALSE zurück. Die abgeleitete Klasse kann dieses Verhalten überschreiben. Wenn die abgeleitete Klasse z. B. die Qualitätskontrollverwaltung implementiert, wird möglicherweise E FAIL zum \_ Ablegen einer Stichprobe zurückgeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseRenderer-Klasse**](cbaserenderer.md)
</dt> </dl>

 

 




