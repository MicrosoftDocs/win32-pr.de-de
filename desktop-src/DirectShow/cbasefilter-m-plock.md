---
description: Zeiger auf einen kritischen Abschnitt, der zum Serialisieren von Zustandsänderungen verwendet wird.
ms.assetid: 4fecd9a6-54df-49d7-bf2f-5dcaef919ad7
title: 'Cbasefilter:: m_pLock Member (amfilter. h)'
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
ms.openlocfilehash: 40b2f6ece048fc6463fda0a22792d57839d59e55
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351290"
---
# <a name="cbasefilterm_plock-member"></a>Cbasefilter:: m \_ Plock-Member

Zeiger auf einen kritischen Abschnitt, der zum Serialisieren von Zustandsänderungen verwendet wird.

## <a name="syntax"></a>Syntax


```C++
CCritSec *m_pLock;
```



## <a name="remarks"></a>Bemerkungen

Diese Variable wird im-Klassenkonstruktor initialisiert. Weitere Informationen finden Sie unter [**cbasefilter:: cbasefilter**](cbasefilter-cbasefilter.md).

Halten Sie diesen kritischen Abschnitt während der Zustandsübergänge oder wenn eine Methode über mehrere Vorgänge auf den Zustand zugreift. Die Basisklasse enthält den kritischen Abschnitt der folgenden Methoden:

-   [**Cbasefilter:: findpin**](cbasefilter-findpin.md)
-   [**Cbasefilter:: getsyncsource**](cbasefilter-getsyncsource.md)
-   [**Cbasefilter:: joinfiltergraph**](cbasefilter-joinfiltergraph.md)
-   [**Cbasefilter:: IsActive**](cbasefilter-isactive.md)
-   [**Cbasefilter:: setsyncsource**](cbasefilter-setsyncsource.md)
-   [**Cbasefilter::P ause**](cbasefilter-pause.md)
-   [**Cbasefilter:: Run**](cbasefilter-run.md)
-   [**Cbasefilter:: Beendigung**](cbasefilter-stop.md)

Behalten Sie diesen kritischen Abschnitt nicht bei Streamingvorgängen bei (d. h. beim Bereitstellen von Beispielen für einen downstreamfilter). Serialisieren von Streamingvorgängen mithilfe eines anderen kritischen Abschnitts. Andernfalls kann dies zu einem Deadlock führen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter. h (Include Streams. h)</dt> </dl>                                                                                  |
| Bibliothek<br/> | <dl> " <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Cbasefilter-Klasse**](cbasefilter.md)
</dt> <dt>

[Threads und kritische Abschnitte](threads-and-critical-sections.md)
</dt> </dl>

 

 




