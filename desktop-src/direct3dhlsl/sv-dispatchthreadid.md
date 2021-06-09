---
title: SV_DispatchThreadID
description: Indizes für die kombinierte Thread- und Threadgruppe, in der ein Compute-Shader ausgeführt wird.
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
ms.openlocfilehash: 8e2713aaa50206660f7672688a43e644873b1c13
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/09/2021
ms.locfileid: "111827059"
---
# <a name="sv_dispatchthreadid"></a>SV \_ DispatchThreadID

Indizes für die kombinierte Thread- und Threadgruppe, in der ein Compute-Shader ausgeführt wird. SV \_ DispatchThreadID ist die Summe aus SV \_ GroupID \* numthreads und GroupThreadID. Sie variiert über den unter [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch) und [numthreads angegebenen](sm5-attributes-numthreads.md)Bereich. Wenn z. B. Dispatch(2,2,2) für einen Compute-Shader mit numthreads(3,3,3) SV \_ DispatchThreadID aufgerufen wird, hat für jede Dimension einen Bereich von 0,.5.

## <a name="type"></a>Typ



| Typ      |
|-------|
| uint3 |



 

## <a name="remarks"></a>Hinweise

Dieser Systemwert ist optional.

Die folgende Abbildung zeigt die Beziehung zwischen den parametern, die an [**Dispatch,**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch)Dispatch(5,3,2) übergeben werden, den im [numthreads-Attribut angegebenen](sm5-attributes-numthreads.md) Werten, numthreads(10,8,3) und Werten, die an den Compute-Shader für die threadbezogenen Systemwerte übergeben werden ([SV \_ GroupIndex](sv-groupindex.md), SV \_ DispatchThreadID,[SV \_ GroupThreadID](sv-groupthreadid.md),[SV \_ GroupID](sv-groupid.md)).

![Abbildung der Beziehung zwischen Dispatch, Threadgruppen und Threads](images/threadgroupids.png)

Diese Funktion wird in den folgenden Shadertypen unterstützt:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | x       |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Semantik](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[Shadermodell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
