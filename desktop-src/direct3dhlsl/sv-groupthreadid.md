---
title: SV_GroupThreadID
description: Indizes, für die ein einzelner Thread innerhalb einer Threadgruppe einen Compute-Shader ausführt.
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
ms.openlocfilehash: 2d36e5639b017dfa94e0f3c9f84d6725f6b6a283
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996987"
---
# <a name="sv_groupthreadid"></a>SV \_ GroupThreadID

Indizes, für die ein einzelner Thread innerhalb einer Threadgruppe einen Compute-Shader ausführt. SV \_ GroupThreadID variiert je nach Bereich, der für den Compute-Shader im [numthreads-Attribut](sm5-attributes-numthreads.md) angegeben ist. Wenn beispielsweise numthreads(3,2,1) als mögliche Werte für den \_ SV GroupThreadID-Eingabewert angegeben wurde, haben Sie diesen Wertebereich (0-2,0-1,0).

## <a name="type"></a>Typ



|       |
|-------|
| Typ  |
| uint3 |



 

## <a name="remarks"></a>Hinweise

Dieser Systemwert ist optional und liegt immer innerhalb der Grenzen der Werte, die an das [numthreads-Attribut](sm5-attributes-numthreads.md) übergeben werden.

Die folgende Abbildung zeigt die Beziehung zwischen den Parametern, die an [**Dispatch,**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch)Dispatch(5,3,2) übergeben werden, den im [attribut numthreads angegebenen](sm5-attributes-numthreads.md) Werten, numthreads(10,8,3) und Werten, die an den Compute-Shader für die threadbezogenen Systemwerte übergeben werden ([SV \_ GroupIndex](sv-groupindex.md),[SV \_ DispatchThreadID](sv-dispatchthreadid.md), SV \_ GroupThreadID,[SV \_ GroupID](sv-groupid.md)).

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

 

 
