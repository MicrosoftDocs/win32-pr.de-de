---
description: Ruft die aktuelle Position innerhalb der Breite, Höhe und Tiefe ab, die mit dem systeminternen [**dispatchraysdimensions**](dispatchraysdimensions.md) -System Wert abgerufen wird.
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
ms.openlocfilehash: aa26400c26aba4ee9e647bcd0a79bad3f3d52f7c
ms.sourcegitcommit: 4e4f9e7c90d25af0774deec1d44bd49fa9b6daa9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2020
ms.locfileid: "106338099"
---
# <a name="dispatchraysindex"></a>DispatchRaysIndex 

Ruft die aktuelle Position innerhalb der Breite, Höhe und Tiefe ab, die mit dem systeminternen [**dispatchraysdimensions**](dispatchraysdimensions.md) -System Wert abgerufen wird.

## <a name="syntax"></a>Syntax

```syntax
uint3 DispatchRaysIndex();
```

## <a name="remarks"></a>Bemerkungen

Diese Funktion kann von den folgenden Raytracing-shadertypen aufgerufen werden.

* [**Any Hit-Shader**](any-hit-shader.md)
* [**Callable-Shader**](callable-shader.md)
* [**Closest Hit-Shader**](closest-hit-shader.md)
* [**Intersection-Shader**](intersection-shader.md)
* [**Miss-Shader**](miss-shader.md)
* [**Ray Generation-Shader**](ray-generation-shader.md)

## <a name="see-also"></a>Siehe auch

* [Direct3D 12-Raytracing, HLSL-Referenz](direct3d-12-raytracing-hlsl-reference.md)
