---
title: SV_GroupIndex
description: Der \ 0034; vereinfacht \ 0034; der Index eines Compute-Shader-Threads innerhalb einer Thread Gruppe, der den mehrdimensionalen SV \_ groupthreadid in einen 1D-Wert umwandelt. SV \_ groupIndex variiert zwischen 0 und (numthreadsx \ numthreadsy \ numthreadsz) \ 8211; 1.
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
ms.openlocfilehash: 952a94378a0570d5bb7bc4f08959074bc8a4da4d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728177"
---
# <a name="sv_groupindex"></a>SV \_ groupIndex

Der "vereinfachte" Index eines Compute-Shader-Threads innerhalb einer Thread Gruppe, der den mehrdimensionalen SV \_ groupthreadid in einen 1D-Wert umwandelt. SV \_ groupIndex variiert zwischen 0 und (numthreadsx \* \* numthreadsz) – 1.

## <a name="type"></a>Typ



| Typ |
|------|
| uint |



 

## <a name="remarks"></a>Bemerkungen


```
SV_GroupIndex = SV_GroupThreadID.z*dimx*dimy + 
                      SV_GroupThreadID.y*dimx + 
                      SV_GroupThreadID.x
```



Dabei sind "dimx" und "dimy" die Dimensionen, die im [numThreads](sm5-attributes-numthreads.md) -Attribut für den Einstiegspunkt angegeben sind.

Dieser System Wert ist optional. Durch die Verwendung wird jedoch sichergestellt, dass ein Thread nur in den zugewiesenen Speicherbereich in der groupshared-Variablen schreibt.

Die folgende Abbildung zeigt die Beziehung zwischen den Parametern, die an Verknüpfung id3d11devicecontext aus übermittelt werden [**::D ispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), Dispatch (5, 3, 2), die im [numThreads](sm5-attributes-numthreads.md) -Attribut angegebenen Werte, numThreads (10, 8, 3) und Werte, die an den Compute-Shader für die Thread bezogenen System Werte (SV \_ groupIndex,[SV \_ dispatchthreadid](sv-dispatchthreadid.md),[SV \_ groupthreadid](sv-groupthreadid.md),[SV \_ GroupID](sv-groupid.md)) weitergegeben werden.

![Darstellung der Beziehung zwischen Dispatch, Thread Gruppen und Threads](images/threadgroupids.png)

Diese Funktion wird in den folgenden Typen von Shadern unterstützt:



| Scheitelpunkt | Hülle | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | x       |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Semantik](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[Shader-Modell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 