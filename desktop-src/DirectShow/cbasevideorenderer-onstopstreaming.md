---
description: Die onstopstreaming-Methode wird am Ende des Streamings aufgerufen, um die Zeit für den Bericht der Eigenschaften Seite zu korrigieren.
ms.assetid: 92174edb-2f6c-4bad-91c5-769aaebcc495
title: Cbasevideorenderer. onstopstreaming-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.OnStopStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 08cf23fd2e1a7e854625d8a369d15290591386fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368312"
---
# <a name="cbasevideorendereronstopstreaming-method"></a>Cbasevideorenderer. onstopstreaming-Methode

Die- `OnStopStreaming` Methode wird am Ende des Streamings aufgerufen, um die Zeit für den Bericht der Eigenschaften Seite zu korrigieren.

## <a name="syntax"></a>Syntax


```C++
HRESULT OnStopStreaming();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen **HRESULT** -Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Member-Funktion wird zweimal aufgerufen, einmal beim Anhalten und wiederholen, wenn der Stream tatsächlich angehalten wird.

Diese Member-Funktion überschreibt [**cbaserenderer:: onstopstreaming**](cbaserenderer-onstopstreaming.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasevideorenderer-Klasse**](cbasevideorenderer.md)
</dt> </dl>

 

 




