---
description: Die OnRenderEnd-Methode wird aufgerufen, nachdem ein Beispiel gerendert wurde.
ms.assetid: c9b3a3b2-a5c0-4a08-9e55-53c27a4d1032
title: CBaseRenderer.OnRenderEnd-Methode (Renbase.h)
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
ms.openlocfilehash: 5fe720ecaa6cc72a0efae3fceda3bb307573077caee6de5ac4309207883c994d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119526536"
---
# <a name="cbaserendereronrenderend-method"></a>CBaseRenderer.OnRenderEnd-Methode

Die `OnRenderEnd` -Methode wird aufgerufen, nachdem ein Beispiel gerendert wurde.

## <a name="syntax"></a>Syntax


```C++
virtual void OnRenderEnd(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pMediaSample* 
</dt> <dd>

Zeiger auf die [**IMediaSample-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-imediasample) des Beispiels.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Die [**CBaseRenderer::Render-Methode**](cbaserenderer-render.md) ruft diese Methode auf. Sie führt in der Basisklasse nichts aus, aber die abgeleitete Klasse kann sie überschreiben. z. B. zum Sammeln von Qualitätskontrolldaten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CBaseRenderer-Klasse**](cbaserenderer.md)
</dt> </dl>

 

 




