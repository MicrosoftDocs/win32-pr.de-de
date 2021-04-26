---
title: SV_DispatchThreadID
description: Indizes, für die kombinierter Thread und Threadgruppe ein Compute-Shader ausgeführt wird.
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
ms.openlocfilehash: e9653d98ebbfef6dd25bb137af3358a14d177f3e
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996517"
---
# <a name="sv_dispatchthreadid"></a>SV \_ DispatchThreadID

Indizes, für die kombinierter Thread und Threadgruppe ein Compute-Shader ausgeführt wird. SV \_ DispatchThreadID ist die Summe aus SV \_ GroupID \* numthreads und GroupThreadID. Sie variiert im bereich, der in [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch) und [numthreads angegeben ist.](sm5-attributes-numthreads.md) Wenn z. B. Dispatch(2,2,2) für einen Compute-Shader mit numthreads(3,3,3) SV DispatchThreadID aufgerufen wird, hat für jede Dimension einen Bereich \_ von 0,5.

## <a name="type"></a>Typ



|       |
|-------|
| Typ  |
| uint3 |



 

## <a name="remarks"></a>Hinweise

Dieser Systemwert ist optional.

Die folgende Abbildung zeigt die Beziehung zwischen den Parametern, die an [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), Dispatch(5,3,2), die im [numthreads-Attribut](sm5-attributes-numthreads.md) angegebenen Werte, numthreads(10,8,3) und Werte übergeben werden, die an den Compute-Shader für die threadbezogenen Systemwerte übergeben werden ([SV \_ GroupIndex](sv-groupindex.md), SV \_ DispatchThreadID,[SV \_ GroupThreadID](sv-groupthreadid.md),[SV \_ GroupID](sv-groupid.md)).

![Abbildung der Beziehung zwischen Dispatch, Threadgruppen und Threads](images/threadgroupids.png)

Diese Funktion wird in den folgenden Shadertypen unterstützt:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | x       |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Semantik](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[Shadermodell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
