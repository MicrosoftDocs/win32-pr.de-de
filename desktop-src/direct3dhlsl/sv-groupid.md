---
title: SV_GroupID
description: Indizes für die Thread Gruppe, in der ein Compute-Shader ausgeführt wird.
ms.assetid: 1b90ca74-a2b6-4a5f-aa4a-1ec879360593
keywords:
- SV_GroupID HLSL
topic_type:
- apiref
api_name:
- SV_GroupID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a2588474a4c6f2cfc6d616cdb70940277389fd1f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101787"
---
# <a name="sv_groupid"></a>SV \_ GroupID

Indizes für die Thread Gruppe, in der ein Compute-Shader ausgeführt wird. Die Indizes gelten für die gesamte Gruppe und nicht für einen einzelnen Thread. Mögliche Werte variieren in dem Bereich, der als Parameter an [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch)weitergegeben wird. Der Aufruf von Dispatch (2, 1, 1) führt beispielsweise zu möglichen Werten von 0, 0, 0 und 1, 0, 0.

Definiert den Gruppen Offset in einem [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch) -Befehl pro Dimension des dispatchaufrufes.

## <a name="type"></a>Typ



|       |
|-------|
| Typ  |
| uint3 |



 

## <a name="remarks"></a>Bemerkungen

Dieser System Wert ist optional.

Die folgende Abbildung zeigt die Beziehung zwischen den Parametern, die an [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch)weitergeleitet werden. Dispatch (5, 3, 2), die im [numThreads](sm5-attributes-numthreads.md) -Attribut angegebenen Werte, numThreads (10, 8, 3) und Werte, die an den Compute-Shader für die Thread bezogenen System Werte ([SV \_ groupIndex](sv-groupindex.md),[SV \_ dispatchthreadid](sv-dispatchthreadid.md),[SV \_ groupthreadid](sv-groupthreadid.md), SV \_ GroupID) weitergegeben werden.

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

 

 