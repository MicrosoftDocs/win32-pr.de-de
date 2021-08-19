---
title: earlydepthstencil
description: Erzwingt Tiefenschablonentests, bevor ein Shader ausgeführt wird.
ms.assetid: f8a9fee7-4a8a-4a34-bf7c-56906592caac
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ed108d4f8e9d8d719d36fc859d5cc01a2317db4756bfbc6b0a548b669d9ca025
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986170"
---
# <a name="earlydepthstencil"></a>earlydepthstencil

Erzwingt Tiefenschablonentests, bevor ein Shader ausgeführt wird.


```
earlydepthstencil   
```



## <a name="remarks"></a>Hinweise

Tiefenschablonentests werden normalerweise während der Pixelverarbeitung durch einen Pixel-Shader durchgeführt. Das Erzwingen eines frühen Tiefenschablonentests führt dazu, dass die Tests vor der Shaderausführung durchgeführt werden. Der Zweck besteht in der Verbesserung der Leistung pro Pixel durch Culling/Reduzierung/Vermeidung unnötiger Pixelverarbeitung.

Eine Anwendung kann frühe Tiefenschablonentests erzwingen, indem das -Attribut bereitgestellt wird, oder die Hardware kann frühe Tiefenschablonentests ausführen, sofern keine Tiefenwerte geschrieben werden und keine ungeordneten Zugriffsvorgänge in einem Shader als Optimierung ausgeführt werden.

Dieses Attribut wird in den folgenden Shadertypen unterstützt:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     |         |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shader Model 5-Attribute](d3d11-graphics-reference-sm5-attributes.md)
</dt> <dt>

[Shadermodell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




