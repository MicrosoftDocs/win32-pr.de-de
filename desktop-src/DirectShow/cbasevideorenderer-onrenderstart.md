---
description: Die onrenderstart-Methode legt Informationen für das Rendering fest.
ms.assetid: 698fe778-e2cb-4b87-a668-084b6c12c71f
title: Cbasevideorenderer. onrenderstart-Methode (renbase. h)
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
ms.openlocfilehash: 7327d25aafa6f6673b7ed70b658f675a9dab8f4d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360316"
---
# <a name="cbasevideorendereronrenderstart-method"></a>Cbasevideorenderer. onrenderstart-Methode

Die- `OnRenderStart` Methode legt Informationen für das Rendering fest.

## <a name="syntax"></a>Syntax


```C++
void OnRenderStart(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pmediasample* 
</dt> <dd>

Zeiger auf das Medien Beispiel.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Diese Member-Funktion Ruft die aktuelle Uhrzeit aus dem System ab und speichert Sie in einer Element Variablen, die verwendet werden soll, wenn die Zeichnung beendet ist. Die Funktion führt auch die Leistungs Protokollierung aus. Diese Member-Funktion sollte direkt vor dem Zeichnen aufgerufen werden.

Diese Member-Funktion überschreibt [**cbaserenderer:: onrenderstart**](cbaserenderer-onrenderstart.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasevideorenderer-Klasse**](cbasevideorenderer.md)
</dt> </dl>

 

 




