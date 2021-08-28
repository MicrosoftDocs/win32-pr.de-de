---
description: Übergibt eine \_ EC VIDEO \_ SIZE \_ CHANGED-Meldung an den Filtergraph-Manager.
ms.assetid: 39cb4f30-c12d-49bd-8d8a-70bf686b680d
title: CBaseControlVideo.OnVideoSizeChange-Methode (Ctlutil.h)
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
ms.openlocfilehash: 689f6f14426d88270136d6cc3687f9e214b72d6e42e2af44f3d189510d61f327
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076690"
---
# <a name="cbasecontrolvideoonvideosizechange-method"></a>CBaseControlVideo.OnVideoSizeChange-Methode

Übergibt eine \_ EC VIDEO \_ SIZE \_ CHANGED-Meldung an den Filtergraph-Manager.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT OnVideoSizeChange();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT-Wert** zurück, der von der Implementierung abhängt. kann einer der folgenden Werte sein, oder andere Werte, die nicht aufgeführt sind.



| Rückgabecode                                                                                   | Beschreibung               |
|-----------------------------------------------------------------------------------------------|---------------------------|
| <dl> <dt>**E \_ FAIL**</dt> </dl>        | Fehler.<br/>       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Nicht genügend Arbeitsspeicher.<br/> |



 

## <a name="remarks"></a>Hinweise

Ein Videorenderer sollte diese Memberfunktion jedes Mal aufrufen, wenn die Videogröße geändert wird. dieser wird in der Regel einmal nach der ersten Verbindung aufgerufen. Wenn der Renderer dynamische Formatänderungen unterstützen kann (von 320 x 240 auf 160 x 120), sollte er es auch nach jeder Änderung aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Ctlutil.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseControlVideo-Klasse**](cbasecontrolvideo.md)
</dt> </dl>

 

 




