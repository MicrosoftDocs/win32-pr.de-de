---
title: SV_GroupIndex
description: '\ 0034;flattened \ 0034; Index eines Compute-Shaderthreads innerhalb einer Threadgruppe, wodurch die mehrdimensionale SV \_ GroupThreadID in einen 1D-Wert umgewandelt wird. SV \_ GroupIndex variiert von 0 bis (numthreadsX \ numthreadsY \ numThreadsZ) \ 8211; 1.'
ms.assetid: e793be10-7c83-478c-859a-4b0a2c537570
keywords:
- SV_GroupIndex HLSL
topic_type:
- apiref
api_name:
- SV_GroupIndex
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fd8c10212a2dd91e4ecbe7fd48a427e4019b2cd79b3d56457635ab9ef9d9262a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118508250"
---
# <a name="sv_groupindex"></a>SV \_ GroupIndex

Der "vereinfachte" Index eines Compute-Shaderthreads innerhalb einer Threadgruppe, der die mehrdimensionale SV \_ GroupThreadID in einen 1D-Wert umsetzt. SV \_ GroupIndex variiert von 0 bis (numthreadsX \* numthreadsY \* numThreadsZ) – 1.

## <a name="type"></a>Typ



| Typ |
|------|
| uint |



 

## <a name="remarks"></a>Hinweise


```
SV_GroupIndex = SV_GroupThreadID.z*dimx*dimy + 
                      SV_GroupThreadID.y*dimx + 
                      SV_GroupThreadID.x
```



dabei sind dimx und dimy die Dimensionen, die im [numthreads-Attribut](sm5-attributes-numthreads.md) für den Einstiegspunkt angegeben sind.

Dieser Systemwert ist optional. Durch seine Verwendung wird jedoch sichergestellt, dass ein Thread nur in den zugewiesenen Speicherbereich in der groupshared-Variablen schreibt.

Die folgende Abbildung zeigt die Beziehung zwischen den Parametern, die an [**ID3D11DeviceContext::D ispatch,**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch)Dispatch(5,3,2), den im [attribut numthreads angegebenen](sm5-attributes-numthreads.md) Werten, numthreads(10,8,3) und werten, die an den Compute-Shader für die threadbezogenen Systemwerte (SV \_ GroupIndex,[SV \_ DispatchThreadID,](sv-dispatchthreadid.md)[SV \_ GroupThreadID](sv-groupthreadid.md),[SV \_ GroupID)](sv-groupid.md)übergeben werden.

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

 

 