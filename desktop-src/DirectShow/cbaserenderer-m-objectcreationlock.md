---
description: Sperren Sie , um die Erstellung von Objekten innerhalb des Filters zu schützen.
ms.assetid: ad1d2584-0d9e-42a8-83ea-0c1907ddcf33
title: CBaseRenderer::m_ObjectCreationLock-Member (Renbase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_ObjectCreationLock
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6b0925aab0345d5eed8da19e12f355c417d66c1f36a1384a05950a87d4c95b3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119429310"
---
# <a name="cbaserendererm_objectcreationlock-member"></a>CBaseRenderer::m \_ ObjectCreationLock-Member

Sperren Sie , um die Erstellung von Objekten innerhalb des Filters zu schützen. Der Filter hält diese Sperre bei der Erstellung des Eingabepins ([**CBaseRenderer::m \_ pInputPin**](cbaserenderer-m-pinputpin.md)) oder des [**CRendererPosPassThru-Objekts**](crendererpospassthru.md) ([**CBaseRenderer::m \_ pPosition**](cbaserenderer-m-pposition.md)) bei. Diese Sperre verhindert, dass mehrere Threads gleichzeitig versuchen, eines dieser Objekte zu erstellen.

## <a name="syntax"></a>Syntax


```C++
CCritSec m_ObjectCreationLock;
```



## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Renbase.h (include Streams.h)</dt> </dl>                                                                                   |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**CBaseRenderer-Klasse**](cbaserenderer.md)
</dt> </dl>

 

 




