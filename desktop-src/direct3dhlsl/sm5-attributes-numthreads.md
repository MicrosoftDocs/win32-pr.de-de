---
title: numthreads
description: Definiert die Anzahl der Threads, die in einer einzelnen Threadgruppe ausgeführt werden sollen, wenn ein Compute-Shader verteilt wird (siehe ID3D11DeviceContext Dispatch).
ms.assetid: ec6b751c-d81c-4221-ae80-166d2a3707fe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f790548fb8ab629b7f6e7af345fa535d28a0d2216f570d02e851ce18618bbae2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118510119"
---
# <a name="numthreads"></a>numthreads

Definiert die Anzahl der Threads, die in einer einzelnen Threadgruppe ausgeführt werden sollen, wenn ein Compute-Shader verteilt wird (siehe [**ID3D11DeviceContext::D ispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch)).


```
numthreads(X, Y, Z)    
```



Die Werte X, Y und Z geben die Größe der Threadgruppe in einer bestimmten Richtung an, und die Summe von X \* Y \* Z gibt die Anzahl der Threads in der Gruppe an. Die Möglichkeit, die Größe der Threadgruppe über drei Dimensionen hinweg anzugeben, ermöglicht den logischen Zugriff auf einzelne Threads mit 2D- und 3D-Datenstrukturen.

Wenn beispielsweise ein Compute-Shader eine 4x4-Matrixhinzufügung vornimmt, können numthreads auf numthreads(4,4,1) festgelegt werden, und die Indizierung in den einzelnen Threads würde automatisch mit den Matrixeinträgen übereinstimmen. Der Compute-Shader könnte auch eine Threadgruppe mit der gleichen Anzahl von Threads (16) mit numthreads(16,1,1) deklarieren, müsste dann jedoch den aktuellen Matrixeintrag basierend auf der aktuellen Threadnummer berechnen.

Die zulässigen Parameterwerte für **numthreads** hängen von der Compute-Shaderversion ab.



| Compute-Shader | Maximale Anzahl von Z | Maximale Anzahl von Threads (X \* Y \* Z) |
|----------------|-----------|---------------------------|
| cs \_ 4 \_ x       | 1         | 768                       |
| CS \_ 5 \_ 0       | 64        | 1024                      |



 

Die folgende Abbildung zeigt die Beziehung zwischen den Parametern, die an [**ID3D11DeviceContext::D ispatch,**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch)Dispatch(5,3,2), den im attribut numthreads angegebenen Werten, numthreads(10,8,3) und werten, die an den Compute-Shader für die threadbezogenen Systemwerte übergeben werden ([SV \_ GroupIndex](sv-groupindex.md),[SV \_ DispatchThreadID](sv-dispatchthreadid.md),[SV \_ GroupThreadID](sv-groupthreadid.md),[SV \_ GroupID](sv-groupid.md)).

![Abbildung der Beziehung zwischen Dispatch, Threadgruppen und Threads](images/threadgroupids.png)

Dieses Attribut wird in den folgenden Shadertypen unterstützt:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | x       |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shadermodell 5-Attribute](d3d11-graphics-reference-sm5-attributes.md)
</dt> <dt>

[Shadermodell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 