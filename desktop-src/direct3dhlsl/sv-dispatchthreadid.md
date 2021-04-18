---
title: SV_DispatchThreadID
description: Indizes, für die der kombinierte Thread und die Thread Gruppe, in der ein Compute-Shader ausgeführt wird.
ms.assetid: bad697f6-26d9-47cd-93e5-127621a161e8
keywords:
- SV_DispatchThreadID HLSL
topic_type:
- apiref
api_name:
- SV_DispatchThreadID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d55fcf7e291c561ecb51dd32dfac135c563974c7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104549872"
---
# <a name="sv_dispatchthreadid"></a>SV \_ dispatchthreadid

Indizes, für die der kombinierte Thread und die Thread Gruppe, in der ein Compute-Shader ausgeführt wird. SV \_ dispatchthreadid ist die Summe von SV \_ GroupID \* numThreads und groupthreadid. Sie variiert in dem Bereich, der in [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch) und [numThreads](sm5-attributes-numthreads.md)angegeben ist. Wenn z. b. Dispatch (2, 2, 2) auf einem Compute-Shader mit numThreads (3, 3, 3) aufgerufen wird, weist SV \_ dispatchthreadid einen Bereich von 0.. 5 für jede Dimension auf.

## <a name="type"></a>Typ



|       |
|-------|
| Typ  |
| uint3 |



 

## <a name="remarks"></a>Bemerkungen

Dieser System Wert ist optional.

Die folgende Abbildung zeigt die Beziehung zwischen den Parametern, die an [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch)weitergeleitet werden. Dispatch (5, 3, 2), die im [numThreads](sm5-attributes-numthreads.md) -Attribut angegebenen Werte, numThreads (10, 8, 3) und Werte, die an den Compute-Shader für die Thread bezogenen System Werte ([SV \_ groupIndex](sv-groupindex.md), SV \_ dispatchthreadid,[SV \_ groupthreadid](sv-groupthreadid.md),[SV \_ GroupID](sv-groupid.md)) weitergegeben werden.

![Darstellung der Beziehung zwischen Dispatch, Thread Gruppen und Threads](images/threadgroupids.png)

Diese Funktion wird in den folgenden Typen von Shadern unterstützt:



|        |      |        |          |       |         |
|--------|------|--------|----------|-------|---------|
| Scheitelpunkt | Hülle | Domain | Geometrie | Pixel | Compute |
|        |      |        |          |       | x       |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Semantik](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[Shader-Modell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 