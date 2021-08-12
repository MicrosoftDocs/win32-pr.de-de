---
description: Zeiger auf einen kritischen Abschnitt, der zum Serialisieren von Zustandsänderungen verwendet wird.
ms.assetid: 4fecd9a6-54df-49d7-bf2f-5dcaef919ad7
title: CBaseFilter::m_pLock-Member (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pLock
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3bc8d3b627e6cd8c3ae4821864f6980db5acd251c721bb8841be40e04377ad55
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118659793"
---
# <a name="cbasefilterm_plock-member"></a>CBaseFilter::m \_ pLock-Member

Zeiger auf einen kritischen Abschnitt, der zum Serialisieren von Zustandsänderungen verwendet wird.

## <a name="syntax"></a>Syntax


```C++
CCritSec *m_pLock;
```



## <a name="remarks"></a>Hinweise

Diese Variable wird im Klassenkonstruktor initialisiert. siehe [**CBaseFilter::CBaseFilter**](cbasefilter-cbasefilter.md).

Halten Sie diesen kritischen Abschnitt während Zustandsübergängen oder wenn eine Methode über mehrere Vorgänge auf den Zustand zutritt. Die Basisklasse enthält den kritischen Abschnitt in den folgenden Methoden:

-   [**CBaseFilter::FindPin**](cbasefilter-findpin.md)
-   [**CBaseFilter::GetSyncSource**](cbasefilter-getsyncsource.md)
-   [**CBaseFilter::JoinFilterGraph**](cbasefilter-joinfiltergraph.md)
-   [**CBaseFilter::IsActive**](cbasefilter-isactive.md)
-   [**CBaseFilter::SetSyncSource**](cbasefilter-setsyncsource.md)
-   [**CBaseFilter::P ause**](cbasefilter-pause.md)
-   [**CBaseFilter::Run**](cbasefilter-run.md)
-   [**CBaseFilter::Stop**](cbasefilter-stop.md)

Halten Sie diesen kritischen Abschnitt nicht während Streamingvorgängen (d. h. bei der Bereitstellung von Stichproben an einen Downstreamfilter) ab. Serialisieren Sie Streamingvorgänge mithilfe eines anderen kritischen Abschnitts. Andernfalls kann dies zu einem Deadlock führen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> <dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CBaseFilter-Klasse**](cbasefilter.md)
</dt> <dt>

[Threads und kritische Abschnitte](threads-and-critical-sections.md)
</dt> </dl>

 

 




