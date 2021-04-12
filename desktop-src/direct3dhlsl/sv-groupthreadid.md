---
title: SV_GroupThreadID
description: Indizes, für die ein einzelner Thread in einer Thread Gruppe, in der ein Compute-Shader ausgeführt wird, ausgeführt wird.
ms.assetid: be944592-c4ea-43c9-88bc-98a9a190a437
keywords:
- SV_GroupThreadID HLSL
topic_type:
- apiref
api_name:
- SV_GroupThreadID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3d4d35766bdbdc2d69c98983a85f336ab784d24d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316268"
---
# <a name="sv_groupthreadid"></a>SV \_ groupthreadid

Indizes, für die ein einzelner Thread in einer Thread Gruppe, in der ein Compute-Shader ausgeführt wird, ausgeführt wird. SV \_ groupthreadid variiert in dem Bereich, der für den Compute-Shader im [numThreads](sm5-attributes-numthreads.md) -Attribut angegeben ist. Wenn z. b. numThreads (3, 2, 1) angegeben wurden, haben die Werte für den \_ Eingabe Wert SV groupthreadid diesen Wertebereich (0-2, 0-1, 0).

## <a name="type"></a>Typ



|       |
|-------|
| Typ  |
| uint3 |



 

## <a name="remarks"></a>Bemerkungen

Dieser System Wert ist optional und liegt immer innerhalb der Grenzen der Werte, die an das [numThreads](sm5-attributes-numthreads.md) -Attribut übermittelt werden.

Die folgende Abbildung zeigt die Beziehung zwischen den Parametern, die an [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch)weitergeleitet werden. Dispatch (5, 3, 2), die im [numThreads](sm5-attributes-numthreads.md) -Attribut angegebenen Werte, numThreads (10, 8, 3) und Werte, die an den Compute-Shader für die Thread bezogenen System Werte ([SV \_ groupIndex](sv-groupindex.md),[SV \_ dispatchthreadid](sv-dispatchthreadid.md), SV \_ groupthreadid,[SV \_ GroupID](sv-groupid.md)) weitergegeben werden.

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

 

 