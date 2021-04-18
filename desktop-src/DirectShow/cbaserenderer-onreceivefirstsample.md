---
description: Die onreceivefirstsample-Methode wird aufgerufen, wenn der Filter eine Stichprobe empfängt, während Sie angehalten wird.
ms.assetid: 5bd481bf-a62d-4d3c-b875-b94298d12730
title: Cbaserderderer. onreceivefirstsample-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnReceiveFirstSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2368b0e2abda3bcdd08872d730f8b9902dad43ac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371788"
---
# <a name="cbaserendereronreceivefirstsample-method"></a>Cbaserderderer. onreceivefirstsample-Methode

Die- `OnReceiveFirstSample` Methode wird aufgerufen, wenn der Filter eine Stichprobe empfängt, während Sie angehalten wird.

## <a name="syntax"></a>Syntax


```C++
virtual void OnReceiveFirstSample(
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

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Die [**cbaserdenderer:: Receive**](cbaserenderer-receive.md) -Methode ruft diese Methode auf. Es wird keine Aktion in der Basisklasse durchführt, aber die abgeleitete Klasse kann Sie überschreiben. Diese Methode ist hauptsächlich für Videorenderer vorgesehen. Wenn ein Videorenderer angehalten wird, wird das erste Beispiel in der Regel als Bild angezeigt.

Wenn Sie das Diagramm im angehaltenen Zustand suchen, wird auch diese Methode aufgerufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbaserderderer-Klasse**](cbaserenderer.md)
</dt> </dl>

 

 




