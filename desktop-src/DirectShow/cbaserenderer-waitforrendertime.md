---
description: Die WaitForRenderTime-Methode wartet auf die Präsentationszeit des aktuellen Beispiels.
ms.assetid: a6acb780-48df-4f73-adcb-cfa4e54b19ac
title: CBaseRenderer.WaitForRenderTime-Methode (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.WaitForRenderTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e590a09c2c6d4cc34728f5ec29db0d8f650d3a1e9cb663e5993acd2cebe4793f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118157354"
---
# <a name="cbaserendererwaitforrendertime-method"></a>CBaseRenderer.WaitForRenderTime-Methode

Die `WaitForRenderTime` -Methode wartet auf die Präsentationszeit des aktuellen Beispiels.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT WaitForRenderTime();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen der folgenden **HRESULT-Werte** zurück.



| Rückgabecode                                                                                           | Beschreibung                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Erfolg.<br/>                                                       |
| <dl> <dt>**VFW \_ E \_ STATUS \_ GEÄNDERT**</dt> </dl> | Der Filterstatus wurde geändert, bevor die Präsentationszeit eingetroffen ist.<br/> |



 

## <a name="remarks"></a>Hinweise

Diese Methode wartet, bis eine der folgenden Bedingungen eintritt:

-   Die Präsentationszeit des Beispiels ist erreicht, und an diesem Punkt kann das Beispiel gerendert werden.
-   Der Filter beendet oder beginnt mit dem Leeren von Daten.

Wenn die Präsentationszeit eintrifft, wird das [**CBaseRenderer::m \_ RenderEvent-Ereignis**](cbaserenderer-m-renderevent.md) signalisiert. Wenn sich der Zustand ändert, wird das [**CBaseRenderer::m \_ ThreadSignal-Ereignis**](cbaserenderer-m-threadsignal.md) signalisiert. Diese Methode wartet auf beide Ereignisse. Die abgeleitete Klasse kann diese Methode überschreiben, um bei Bedarf auf zusätzliche Ereignisse zu warten.

Diese Methode ruft die [**CBaseRenderer::OnWaitStart-Methode**](cbaserenderer-onwaitstart.md) auf, wenn der Wartelauf beginnt, und die [**CBaseRenderer::OnWaitEnd-Methode,**](cbaserenderer-onwaitend.md) wenn der Wartelauf erfolgt ist. Keine der Methoden führt etwas in der Basisklasse aus, aber die abgeleitete Klasse kann sie überschreiben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseRenderer-Klasse**](cbaserenderer.md)
</dt> </dl>

 

 




