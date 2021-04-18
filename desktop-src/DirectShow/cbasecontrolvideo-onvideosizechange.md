---
description: Übergibt eine an \_ \_ \_ den Filter Diagramm-Manager geänderte Meldung mit einer gewechselten EC-Video Größe.
ms.assetid: 39cb4f30-c12d-49bd-8d8a-70bf686b680d
title: Cbasecontrolvideo. onvideosizechange-Methode (ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.OnVideoSizeChange
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 37caa05d164c23484c749730796d6a5f10d67d57
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364424"
---
# <a name="cbasecontrolvideoonvideosizechange-method"></a>Cbasecontrolvideo. onvideosizechange-Methode

Übergibt eine an \_ \_ \_ den Filter Diagramm-Manager geänderte Meldung mit einer gewechselten EC-Video Größe.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT OnVideoSizeChange();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück, der von der Implementierung abhängig ist. kann einen der folgenden Werte oder andere nicht aufgelistete Werte aufweisen.



| Rückgabecode                                                                                   | Beschreibung               |
|-----------------------------------------------------------------------------------------------|---------------------------|
| <dl> <dt>**E \_ fehlschlagen**</dt> </dl>        | Fehler.<br/>       |
| <dl> <dt>**E \_ outo-Memory**</dt> </dl> | Nicht genügend Arbeitsspeicher.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Ein Videorenderer sollte diese Member-Funktion jedes Mal, wenn die Videogröße geändert wird, abrufen. Dies wird in der Regel einmal nach der anfänglichen Verbindung aufgerufen. Wenn der Renderer dynamische Formatänderungen unterstützen kann (von 320 x 240 bis 160 x 120), sollte er nach jeder Änderung auch aufgerufen werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasecontrolvideo-Klasse**](cbasecontrolvideo.md)
</dt> </dl>

 

 




