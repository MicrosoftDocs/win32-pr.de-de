---
title: Shadermodell 5.1-Objekte
description: Die folgenden Objekte wurden dem Shadermodell 5.1 hinzugefügt.
ms.assetid: 2958618D-54C6-4860-9910-B45AAB73CCFD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f253c9d6a82e5a464e55761625ba8f88dd7953e3f293fc142a69019a3889830
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119671631"
---
# <a name="shader-model-51-objects"></a>Shadermodell 5.1-Objekte

Die folgenden Objekte wurden dem Shadermodell 5.1 hinzugefügt.

Für die [Rasterizer-Auftragsansichten](/windows/desktop/direct3d11/rasterizer-order-views) (verfügbar in D3D11.3 und D3D12) sind die folgenden Objekte neu und nur im Pixelshader zulässig. Beachten Sie, dass die unterstützten Methoden mit den entsprechenden UAV-Objekten identisch sind.



| Rasterizer-Objekt                                   | UAV-Objekt                                                              |
|------------------------------------|---------------------------------------------------------------|
| RasterizerOrderedBuffer            | [**Rwbuffer**](sm5-object-rwbuffer.md)                       |
| RasterizerOrderedByteAddressBuffer | [**RWByteAddressBuffer**](sm5-object-rwbyteaddressbuffer.md) |
| RasterizerOrderedStructuredBuffer  | [**RWStructuredBuffer**](sm5-object-rwstructuredbuffer.md)   |
| RasterizerOrderedTexture1D         | [**RWTexture1D**](sm5-object-rwtexture1d.md)                 |
| RasterizerOrderedTexture1DArray    | [**RWTexture1DArray**](sm5-object-rwtexture1darray.md)       |
| RasterizerOrderedTexture2D         | [**RWTexture2D**](sm5-object-rwtexture2d.md)                 |
| RasterizerOrderedTexture2DArray    | [**RWTexture2DArray**](sm5-object-rwtexture2darray.md)       |
| RasterizerOrderedTexture3D         | [**RWTexture3D**](sm5-object-rwtexture3d.md)                 |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shadermodell 5.1](shader-model-5-1.md)
</dt> <dt>

[HLSL Shader Model 5.1 Features for Direct3D 12 (HLSL-Shadermodell 5.1-Features für Direct3D 12)](hlsl-shader-model-5-1-features-for-direct3d-12.md)
</dt> </dl>

 

 
