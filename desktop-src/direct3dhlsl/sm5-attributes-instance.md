---
title: instance
description: Verwenden Sie dieses Attribut, um einen Geometry-Shader zu verwenden.
ms.assetid: 0e487e52-53d0-4193-99b2-fd018a061b42
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4749e11db00b38e5e223e11315de86656b2f6488
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104038353"
---
# <a name="instance"></a>instance

Verwenden Sie dieses Attribut, um einen Geometry-Shader zu verwenden.


```
instance(X)   
```



## <a name="remarks"></a>Bemerkungen

X ist ein ganzzahliger Index, der die Anzahl der Instanzen angibt, die für jedes gezeichnete Element ausgeführt werden sollen (z. b. für jedes Dreieck). Verwenden Sie bei Verwendung dieses Attributs [SV \_ gsinstanceid](sv-gsinstanceid.md) , um zu ermitteln, welche Instanz eines Geometry-Shaders ausgeführt wird.

Dieses Attribut wird in den folgenden Typen von Shadern unterstützt:



| Scheitelpunkt | Hülle | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        | x        |       |         |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shader Model 5-Attribute](d3d11-graphics-reference-sm5-attributes.md)
</dt> <dt>

[Shader-Modell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




