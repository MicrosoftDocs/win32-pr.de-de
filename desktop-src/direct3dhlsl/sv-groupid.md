---
title: SV_GroupID
description: Indizes für die Threadgruppe, in der ein Compute-Shader ausgeführt wird.
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
ms.openlocfilehash: ab94cef0a9a33f23947e11b93a5487c65eee3890
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/09/2021
ms.locfileid: "111827039"
---
# <a name="sv_groupid"></a>SV \_ GroupID

Indizes für die Threadgruppe, in der ein Compute-Shader ausgeführt wird. Die Indizes gelten für die gesamte Gruppe und nicht für einen einzelnen Thread. Mögliche Werte variieren in dem Bereich, der als Parameter an [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch)übergeben wird. Beispielsweise führt der Aufruf von Dispatch(2,1,1) zu möglichen Werten von 0,0,0 und 1,0,0.

Definiert den Gruppenoffset innerhalb eines [**Dispatchaufrufs**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch) pro Dimension des Dispatchaufrufs.

## <a name="type"></a>Typ



| Typ      |
|-------|
| uint3 |



 

## <a name="remarks"></a>Hinweise

Dieser Systemwert ist optional.

Die folgende Abbildung zeigt die Beziehung zwischen den Parametern, die an [**Dispatch,**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch)Dispatch(5,3,2) übergeben werden, den im [attribut numthreads angegebenen](sm5-attributes-numthreads.md) Werten, numthreads(10,8,3) und Werten, die an den Compute-Shader für die threadbezogenen Systemwerte übergeben werden ([SV \_ GroupIndex](sv-groupindex.md),[SV \_ DispatchThreadID](sv-dispatchthreadid.md),[SV \_ GroupThreadID](sv-groupthreadid.md), SV \_ GroupID).

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

 

 
