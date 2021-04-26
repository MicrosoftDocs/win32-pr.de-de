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
ms.openlocfilehash: cf96e1db7dbb93c88ec741e309413dea3df2b01d
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996997"
---
# <a name="sv_groupid"></a>SV \_ GroupID

Indizes für die Threadgruppe, in der ein Compute-Shader ausgeführt wird. Die Indizes gelten für die gesamte Gruppe und nicht für einen einzelnen Thread. Mögliche Werte variieren im Bereich, der als Parameter an [**Dispatch übergeben wird.**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch) Beispielsweise führt der Aufruf von Dispatch(2,1,1) zu möglichen Werten von 0,0,0 und 1,0,0.

Definiert den Gruppenoffset innerhalb eines [**Dispatchaufrufs**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch) pro Dimension des Dispatchaufrufs.

## <a name="type"></a>Typ



|       |
|-------|
| Typ  |
| uint3 |



 

## <a name="remarks"></a>Hinweise

Dieser Systemwert ist optional.

Die folgende Abbildung zeigt die Beziehung zwischen den an [**Dispatch,**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch)Dispatch(5,3,2) übergebenen Parametern, den im [numthreads-Attribut](sm5-attributes-numthreads.md) angegebenen Werten, numthreads(10,8,3) und Werten, die für die threadbezogenen Systemwerte an den Compute-Shader übergeben werden ([SV \_ GroupIndex,](sv-groupindex.md)[SV \_ DispatchThreadID, SV](sv-dispatchthreadid.md)[ \_ GroupThreadID,](sv-groupthreadid.md)SV \_ GroupID).

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

 

 
