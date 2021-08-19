---
description: Die Werte für Breite, Höhe und Tiefe der D3D12_DISPATCH_RAYS_DESC im ursprünglichen DispatchRays-Aufruf angegebenen Struktur.
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
ms.openlocfilehash: 4f68b7bdd5f5ea92074b366b9f981f490a9801079b29def17ba66770abd3c5f1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989490"
---
# <a name="dispatchraysdimensions"></a>DispatchRaysDimensions

Die Werte für Breite, Höhe und Tiefe der **D3D12 \_ DISPATCH \_ RAY \_ DESC-Struktur,** die im ursprünglichen [**DispatchRays-Aufruf angegeben**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-dispatchrays) sind.

## <a name="syntax"></a>Syntax

```
uint3 DispatchRaysDimensions();
```

## <a name="remarks"></a>Hinweise

Diese Funktion kann von den folgenden Raytracing-Shadertypen aufgerufen werden:

* [**Any Hit-Shader**](any-hit-shader.md)
* [**Callable-Shader**](callable-shader.md)
* [**Closest Hit-Shader**](closest-hit-shader.md)
* [**Intersection-Shader**](intersection-shader.md)
* [**Miss-Shader**](miss-shader.md)
* [**Ray Generation-Shader**](ray-generation-shader.md)

## <a name="see-also"></a>Weitere Informationen

* [Direct3D 12-Raytracing, HLSL-Referenz](direct3d-12-raytracing-hlsl-reference.md)
