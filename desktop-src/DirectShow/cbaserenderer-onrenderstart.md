---
description: Die onrenderstart-Methode wird aufgerufen, wenn das Rendering gerade gestartet wird.
ms.assetid: 46af24cf-9075-4ebc-a49b-85f8f0c3da6f
title: Cbaserderderer. onrenderstart-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnRenderStart
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a7838b0ba43c1e570b745541882a2f2f815dd948
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367015"
---
# <a name="cbaserendereronrenderstart-method"></a>Cbaserderderer. onrenderstart-Methode

Die- `OnRenderStart` Methode wird aufgerufen, wenn das Rendering gerade gestartet wird.

## <a name="syntax"></a>Syntax


```C++
virtual void OnRenderStart(
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

 

 




