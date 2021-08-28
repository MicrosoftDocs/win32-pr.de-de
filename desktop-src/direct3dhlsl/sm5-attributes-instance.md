---
title: instance
description: Verwenden Sie dieses Attribut, um einen Geometrie-Shader zu instanzig machen.
ms.assetid: 0e487e52-53d0-4193-99b2-fd018a061b42
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 77c19b26107228bb04007d1c2c69ac34b464c7c361966ac9858d9bcdb09b4c4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986160"
---
# <a name="instance"></a>instance

Verwenden Sie dieses Attribut, um einen Geometrie-Shader zu instanzig machen.


```
instance(X)   
```



## <a name="remarks"></a>Hinweise

X ist ein ganzzahliger Index, der die Anzahl der Instanzen angibt, die für jedes gezeichnete Element ausgeführt werden sollen (z. B. für jedes Dreieck). Verwenden Sie bei Verwendung dieses [Attributs SV \_ GSInstanceID,](sv-gsinstanceid.md) um zu identifizieren, welche Instanz eines Geometrie-Shaders ausgeführt wird.

Dieses Attribut wird in den folgenden Shadertypen unterstützt:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        | x        |       |         |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shader Model 5-Attribute](d3d11-graphics-reference-sm5-attributes.md)
</dt> <dt>

[Shadermodell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




