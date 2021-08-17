---
description: Ruft die aktuelle Position innerhalb der Breite, Höhe und Tiefe ab, die mit dem [**systeminternen DispatchRaysDimensions-Systemwert**](dispatchraysdimensions.md) ermittelt wird.
title: 'DispatchRaysIndex '
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DispatchRaysIndex
api_type:
- NA
ms.openlocfilehash: 1b40987c76f42d41d74b7cb3d41f35cc20bd5a6ac1414ae9b010cedcfa7ef9fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119124165"
---
# <a name="dispatchraysindex"></a>DispatchRaysIndex 

Ruft die aktuelle Position innerhalb der Breite, Höhe und Tiefe ab, die mit dem [**systeminternen DispatchRaysDimensions-Systemwert**](dispatchraysdimensions.md) ermittelt wird.

## <a name="syntax"></a>Syntax

```syntax
uint3 DispatchRaysIndex();
```

## <a name="remarks"></a>Hinweise

Diese Funktion kann von den folgenden Raytracing-Shadertypen aufgerufen werden.

* [**Any Hit-Shader**](any-hit-shader.md)
* [**Callable-Shader**](callable-shader.md)
* [**Closest Hit-Shader**](closest-hit-shader.md)
* [**Intersection-Shader**](intersection-shader.md)
* [**Miss-Shader**](miss-shader.md)
* [**Ray Generation-Shader**](ray-generation-shader.md)

## <a name="see-also"></a>Weitere Informationen

* [Direct3D 12-Raytracing, HLSL-Referenz](direct3d-12-raytracing-hlsl-reference.md)
