---
description: Die Werte für Breite, Höhe und Tiefe aus der D3D12_DISPATCH_RAYS_DESC Struktur, die in den ursprünglichen dispatchrays-aufrufen angegeben sind.
ms.assetid: ''
title: DispatchRaysDimensions
ms.localizationpriority: low
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DispatchRaysDimensions
api_type:
- NA
ms.openlocfilehash: e35c967ad831c82912d2962da72d9ad17eab1c15
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106339712"
---
# <a name="dispatchraysdimensions"></a>DispatchRaysDimensions

Die Werte für Breite, Höhe und Tiefe der **D3D12 \_ Dispatch \_ Rays \_** -Struktur, die in den ursprünglichen [**dispatchrays**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-dispatchrays) -aufrufen angegeben sind.

## <a name="syntax"></a>Syntax

```
uint3 DispatchRaysDimensions();
```

## <a name="remarks"></a>Bemerkungen

Diese Funktion kann von den folgenden Raytracing-shadertypen aufgerufen werden:

* [**Any Hit-Shader**](any-hit-shader.md)
* [**Callable-Shader**](callable-shader.md)
* [**Closest Hit-Shader**](closest-hit-shader.md)
* [**Intersection-Shader**](intersection-shader.md)
* [**Miss-Shader**](miss-shader.md)
* [**Ray Generation-Shader**](ray-generation-shader.md)

## <a name="see-also"></a>Siehe auch

* [Direct3D 12-Raytracing, HLSL-Referenz](direct3d-12-raytracing-hlsl-reference.md)
