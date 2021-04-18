---
description: Die EOS-Methode aktualisiert die zwischengespeicherten Zeitstempel nach einer Datenstrom Benachrichtigung.
ms.assetid: 7fb2f964-ec15-47f5-902b-29b9b121e876
title: Crendererpospassthru. EOS-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererPosPassThru.EOS
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a9e6990d946f32b441f0a33ceba8c0a59fdae488
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358787"
---
# <a name="crendererpospassthrueos-method"></a>Crendererpospassthru. EOS-Methode

Die- `EOS` Methode aktualisiert die zwischengespeicherten Zeitstempel nach einer Datenstrom Benachrichtigung.

## <a name="syntax"></a>Syntax


```C++
HRESULT EOS();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück. Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.



| Rückgabecode                                                                            | Beschreibung                                               |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>   | Erfolg.<br/>                                       |
| <dl> <dt>**E \_ fehlschlagen**</dt> </dl> | Fehler. Möglicherweise wird der Filter nicht gestreamt.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Der Filter sollte diese Methode beim Empfang einer Streamende Benachrichtigung ([**IPin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream)) abrufen. Die-Methode legt beide zwischengespeicherten Zeitstempel auf die Position des Stopps fest. Dadurch wird sichergestellt, dass die [**imediaseeking:: GetCurrentPosition**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcurrentposition) -Methode die korrekten Werte am Ende des Streams zurückgibt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



 

 




