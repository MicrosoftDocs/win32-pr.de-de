---
description: Die onrenderend-Methode wird aufgerufen, nachdem ein Beispiel gerendert wurde.
ms.assetid: c9b3a3b2-a5c0-4a08-9e55-53c27a4d1032
title: Cbaserenderer. onrenderend-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnRenderEnd
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5859cf81a5fd0306f3470ee0fc6d54476e99833d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370838"
---
# <a name="cbaserendereronrenderend-method"></a>Cbaserenderer. onrenderend-Methode

Die- `OnRenderEnd` Methode wird aufgerufen, nachdem ein Beispiel gerendert wurde.

## <a name="syntax"></a>Syntax


```C++
virtual void OnRenderEnd(
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

Die [**cbaserdenderer:: Rendering**](cbaserenderer-render.md) -Methode ruft diese Methode auf. Es wird keine Aktion in der Basisklasse durchführt, aber die abgeleitete Klasse kann Sie überschreiben. beispielsweise, um Qualitäts Steuerungsdaten zu erfassen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase. h (Include Streams. h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbaserderderer-Klasse**](cbaserenderer.md)
</dt> </dl>

 

 




