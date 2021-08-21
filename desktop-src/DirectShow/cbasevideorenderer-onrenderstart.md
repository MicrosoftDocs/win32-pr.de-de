---
description: Die OnRenderStart-Methode legt Informationen für das Rendering fest.
ms.assetid: 698fe778-e2cb-4b87-a668-084b6c12c71f
title: CBaseVideoRenderer.OnRenderStart-Methode (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.OnRenderStart
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 78c82b00b8b719b03d096ac0f83e43c8471ea98d56eab7bf67d28b0adae852f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118157035"
---
# <a name="cbasevideorendereronrenderstart-method"></a>CBaseVideoRenderer.OnRenderStart-Methode

Die `OnRenderStart` -Methode legt Informationen für das Rendering fest.

## <a name="syntax"></a>Syntax


```C++
void OnRenderStart(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pMediaSample* 
</dt> <dd>

Zeiger auf das Medienbeispiel.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Diese Memberfunktion ruft die aktuelle Uhrzeit aus dem System ab und speichert sie in einer Membervariablen, die verwendet werden soll, wenn die Zeichnung abgeschlossen ist. Die Funktion führt auch die Leistungsprotokollierung durch. Diese Memberfunktion sollte direkt vor dem Zeichnen aufgerufen werden.

Diese Memberfunktion überschreibt [**CBaseRenderer::OnRenderStart**](cbaserenderer-onrenderstart.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseVideoRenderer-Klasse**](cbasevideorenderer.md)
</dt> </dl>

 

 




