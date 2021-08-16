---
description: Die NotifyEndOfStream-Methode sendet ein EC \_ COMPLETE-Ereignis an den Filtergraph-Manager.
ms.assetid: 9eec5b65-654d-4b2e-be39-93225a7674a5
title: CBaseRenderer.NotifyEndOfStream-Methode (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.NotifyEndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 05504b2ca1520320777b93c1c066e91edd5135798e4710c6514dbe858737760b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118402811"
---
# <a name="cbaserenderernotifyendofstream-method"></a>CBaseRenderer.NotifyEndOfStream-Methode

Die `NotifyEndOfStream` -Methode sendet ein [**EC \_ COMPLETE-Ereignis**](ec-complete.md) an den Filtergraph-Manager.

## <a name="syntax"></a>Syntax


```C++
void NotifyEndOfStream();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseRenderer-Klasse**](cbaserenderer.md)
</dt> <dt>

[**CBaseRenderer::EndOfStream**](cbaserenderer-endofstream.md)
</dt> <dt>

[**CBaseRenderer::SendEndOfStream**](cbaserenderer-sendendofstream.md)
</dt> </dl>

 

 




