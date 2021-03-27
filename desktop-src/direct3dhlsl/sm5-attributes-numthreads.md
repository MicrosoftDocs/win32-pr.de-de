---
title: numThreads
description: Definiert die Anzahl der Threads, die in einer einzelnen Thread Gruppe ausgeführt werden sollen, wenn ein Compute-Shader versendet wird (siehe Verknüpfung id3d11devicecontext aus Dispatch).
ms.assetid: ec6b751c-d81c-4221-ae80-166d2a3707fe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: abcca751b58bc88ba984ac5c2210a563591d592e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390953"
---
# <a name="numthreads"></a>numThreads

Definiert die Anzahl der Threads, die in einer einzelnen Thread Gruppe ausgeführt werden sollen, wenn ein Compute-Shader versendet wird (siehe [**Verknüpfung id3d11devicecontext aus::D ispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch)).


```
numthreads(X, Y, Z)    
```



Der X-, y-und Z-Wert geben die Größe der Thread Gruppe in einer bestimmten Richtung an, und der Gesamtwert von x \* Y \* Z gibt die Anzahl der Threads in der Gruppe an. Durch die Möglichkeit, die Größe der Thread Gruppe über drei Dimensionen hinweg anzugeben, können auf einzelne Threads auf eine Weise zugegriffen werden, die logisch 2D-und 3D-Datenstrukturen ist.

Wenn z. b. ein Compute-Shader eine 4 x 4-Matrix Addition durchführt, können numThreads auf numThreads (4, 4, 1) festgelegt werden, und die Indizierung in den einzelnen Threads würde automatisch den Matrix Einträgen entsprechen. Der COMPUTE-Shader kann auch eine Thread Gruppe mit der gleichen Anzahl von Threads (16) mit numThreads (16, 1, 1) deklarieren, müsste jedoch den aktuellen Matrix Eintrag basierend auf der aktuellen Thread Nummer berechnen.

Die zulässigen Parameterwerte für **numThreads** sind von der COMPUTE-Shader-Version abhängig.



| Compute-Shader | Maximum Z | Maximale Threads (X \* Y \* Z) |
|----------------|-----------|---------------------------|
| CS \_ 4 \_ x       | 1         | 768                       |
| CS \_ 5 \_ 0       | 64        | 1024                      |



 

Die folgende Abbildung zeigt die Beziehung zwischen den Parametern, die an Verknüpfung id3d11devicecontext aus übermittelt werden [**::D ispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), Dispatch (5, 3, 2), die im numThreads-Attribut angegebenen Werte, numThreads (10, 8, 3) und Werte, die an den Compute-Shader für die Thread bezogenen System Werte ([SV \_ groupIndex](sv-groupindex.md),[SV \_ dispatchthreadid](sv-dispatchthreadid.md),[SV \_ groupthreadid](sv-groupthreadid.md),[SV \_ GroupID](sv-groupid.md)) weitergegeben werden.

![Darstellung der Beziehung zwischen Dispatch, Thread Gruppen und Threads](images/threadgroupids.png)

Dieses Attribut wird in den folgenden Typen von Shadern unterstützt:



| Scheitelpunkt | Hülle | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | x       |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shader Model 5-Attribute](d3d11-graphics-reference-sm5-attributes.md)
</dt> <dt>

[Shader-Modell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 