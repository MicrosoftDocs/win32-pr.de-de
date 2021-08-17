---
description: Die Render-Methode rendert ein Beispiel.
ms.assetid: 82b47777-2900-4821-ab79-1856da432832
title: CBaseRenderer.Render-Methode (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Render
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 185baf6818d2022dbe7b64cfab888945e1a2405433eefa925d2de70dcca286e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016858"
---
# <a name="cbaserendererrender-method"></a>CBaseRenderer.Render-Methode

Die `Render` -Methode rendert ein Beispiel.

## <a name="syntax"></a>Syntax


```C++
virtual Render(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pMediaSample* 
</dt> <dd>

Zeiger auf die [**IMediaSample-Schnittstelle des**](/windows/desktop/api/Strmif/nn-strmif-imediasample) Beispiels.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück. Mögliche Werte sind die werte in der folgenden Tabelle.



| Rückgabecode                                                                             | Beschreibung                                                      |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl> | Der Filter wird beendet, oder *pMediaSample ist* **NULL.**<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Erfolg.<br/>                                              |



 

## <a name="remarks"></a>Hinweise

Diese Methode ruft die reine virtuelle [**Methode CBaseRenderer::D oRenderSample**](cbaserenderer-dorendersample.md)auf, die die eigentliche Arbeit übernimmt. Die abgeleitete Klasse muss **DoRenderSample implementieren.**

Unmittelbar vor dem **Aufruf von DoRenderSample** ruft diese Methode die [**CBaseRenderer::OnRenderStart-Methode**](cbaserenderer-onrenderstart.md) auf. Unmittelbar danach wird die [**CBaseRenderer::OnRenderEnd-Methode**](cbaserenderer-onrenderend.md) aufruft. Die abgeleitete Klasse kann diese beiden Methoden nach Bedarf überschreiben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseRenderer-Klasse**](cbaserenderer.md)
</dt> </dl>

 

 




