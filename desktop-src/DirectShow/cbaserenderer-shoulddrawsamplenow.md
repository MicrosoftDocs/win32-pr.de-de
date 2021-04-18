---
description: Die Methode "schulddrawsamplenow" bestimmt, wie ein Beispiel für das Rendering geplant wird.
ms.assetid: 92994f1f-53d5-42d4-90a2-2984b693e4c0
title: Cbasererderderer. schulddrawsamplenow-Methode (renbase. h)
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
ms.openlocfilehash: 27fbf603fd670cac2a39831114a7f141b17ffd2e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352136"
---
# <a name="cbaserenderershoulddrawsamplenow-method"></a>Cbasererderer. schulddrawsamplenow-Methode

Die- `ShouldDrawSampleNow` Methode bestimmt, wie ein Beispiel für das Rendering geplant wird.

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

*pmediasample* 
</dt> <dd>

Zeiger auf die [**imediasample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) -Schnittstelle des Beispiels.

</dd> <dt>

*pstarttime* 
</dt> <dd>

Ein Zeiger auf eine Variable, die die Startzeit des Beispiels enthält.

</dd> <dt>

*Zeit* 
</dt> <dd>

Ein Zeiger auf eine Variable, die die Endzeit des Beispiels enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt " \_ false" zurück. Wenn die abgeleitete Klasse diese Methode überschreibt, geben Sie einen der in der folgenden Tabelle aufgeführten Werte zurück.



| Rückgabecode                                                                               | Beschreibung                                                                        |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Das Beispiel sollte sofort gerendert werden.<br/>                              |
| <dl> <dt>**S \_ false**</dt> </dl>   | Das Beispiel sollte basierend auf den Zeitstempeln für das Rendering geplant werden.<br/> |
| <dl> <dt>**Fehlercode**</dt> </dl> | Führen Sie dieses Beispiel nicht aus.<br/>                                              |



 

## <a name="remarks"></a>Bemerkungen

Die [**cbaserdenderer:: getsampletimes**](cbaserenderer-getsampletimes.md) -Methode ruft diese Methode auf. Standardmäßig werden Stichproben immer basierend auf Ihren Zeitstempeln für das Rendering geplant. Diese Methode kann von der abgeleiteten Klasse überschrieben werden. So implementieren Sie z. b. die Qualitätskontrolle.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbaserderderer-Klasse**](cbaserenderer.md)
</dt> </dl>

 

 




