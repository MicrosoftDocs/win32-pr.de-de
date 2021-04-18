---
description: Die Rendermethode rendert ein Beispiel.
ms.assetid: 82b47777-2900-4821-ab79-1856da432832
title: Cbaserderderer. Rendering-Methode (renbase. h)
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
ms.openlocfilehash: 9fefd44fe1b913fbba0e3ebfaa6f750b88d40813
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371555"
---
# <a name="cbaserendererrender-method"></a>Cbaserderderer. Rendering-Methode

Die- `Render` Methode rendert ein Beispiel.

## <a name="syntax"></a>Syntax


```C++
virtual Render(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pmediasample* 
</dt> <dd>

Zeiger auf die [**imediasample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) -Schnittstelle des Beispiels.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.



| Rückgabecode                                                                             | Beschreibung                                                      |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl> | Der Filter wurde beendet, oder *pmediasample* ist **null**.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>    | Erfolg.<br/>                                              |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode ruft die reine virtuelle Methode [**cbasererderderer::D orendersample**](cbaserenderer-dorendersample.md)auf, die die eigentliche Arbeit übernimmt. Die abgeleitete Klasse muss " **dorendersample**" implementieren.

Direkt vor dem Aufruf von " **dorendersample**" ruft diese Methode die [**cbaserdenderer:: onrenderstart**](cbaserenderer-onrenderstart.md) -Methode auf. Unmittelbar danach wird die [**cbaserenderer:: onrenderend**](cbaserenderer-onrenderend.md) -Methode aufgerufen. Die abgeleitete Klasse kann diese beiden Methoden nach Bedarf überschreiben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbaserderderer-Klasse**](cbaserenderer.md)
</dt> </dl>

 

 




