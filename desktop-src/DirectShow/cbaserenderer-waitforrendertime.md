---
description: Die waitforrendertime-Methode wartet auf die Präsentationszeit des aktuellen Beispiels.
ms.assetid: a6acb780-48df-4f73-adcb-cfa4e54b19ac
title: Cbaserderderer. waitforrendertime-Methode (renbase. h)
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
ms.openlocfilehash: 43a537728ca0874fa1dfd69b4712bcc97cf23850
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364037"
---
# <a name="cbaserendererwaitforrendertime-method"></a>Cbaserderderer. waitforrendertime-Methode

Die `WaitForRenderTime` -Methode wartet auf die Präsentationszeit des aktuellen Beispiels.

## <a name="syntax"></a>Syntax


```C++
virtual HRESULT WaitForRenderTime();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt einen der folgenden **HRESULT** -Werte zurück.



| Rückgabecode                                                                                           | Beschreibung                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Erfolg.<br/>                                                       |
| <dl> <dt>**VFW \_ E \_ Status \_ geändert**</dt> </dl> | Der Filter Zustand wurde vor dem Eintreffen der Präsentationszeit geändert.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Methode wartet, bis eine der folgenden Aktionen auftritt:

-   Die Präsentationszeit des Beispiels kommt an, an der Stelle, an der das Beispiel gerendert werden kann.
-   Der Filter beendet oder beginnt mit dem leeren von Daten.

Wenn die Präsentationszeit erreicht wird, wird das Ereignis [**cbasererderderer:: m \_ renderevent**](cbaserenderer-m-renderevent.md) signalisiert. Wenn sich der Status ändert, wird das Ereignis [**cbaserererererertderer:: m \_ threadsignal**](cbaserenderer-m-threadsignal.md) signalisiert. Diese Methode wartet auf beide Ereignisse. Die abgeleitete Klasse kann diese Methode überschreiben, um ggf. auf zusätzliche Ereignisse zu warten.

Diese Methode ruft die [**cbaserenderer:: onwaitstart**](cbaserenderer-onwaitstart.md) -Methode auf, wenn der Warte Vorgang beginnt, und die [**cbaserenderer:: onwaitend**](cbaserenderer-onwaitend.md) -Methode, wenn der Warte Vorgang abgeschlossen ist. Keine der Methoden führt etwas in der Basisklasse aus, aber die abgeleitete Klasse kann Sie überschreiben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbaserderderer-Klasse**](cbaserenderer.md)
</dt> </dl>

 

 




