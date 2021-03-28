---
title: Shader-Modell 5,1-Objekte
description: Die folgenden Objekte wurden dem Shader-Modell 5,1 hinzugefügt.
ms.assetid: 2958618D-54C6-4860-9910-B45AAB73CCFD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 616afd8e4036988b6f91cb09cddf0db26c1dd480
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315573"
---
# <a name="shader-model-51-objects"></a>Shader-Modell 5,1-Objekte

Die folgenden Objekte wurden dem Shader-Modell 5,1 hinzugefügt.

Die folgenden Objekte sind für die [Reihenfolge Sichten der Rasterizer](/windows/desktop/direct3d11/rasterizer-order-views) (verfügbar in D3D 11.3 und D3D12) neu und nur im Pixelshader zulässig. Beachten Sie, dass die Methoden, die Sie unterstützen, mit den entsprechenden UAV-Objekten identisch sind.



|                                    |                                                               |
|------------------------------------|---------------------------------------------------------------|
| Rasterizer-Objekt                  | UAV-Objekt                                                    |
| Rasterizerorderedbuffer            | [**Rwbuffer**](sm5-object-rwbuffer.md)                       |
| Rasterizerorderedbyteaddressbuffer | [**Rwbyteaddressbuffer**](sm5-object-rwbyteaddressbuffer.md) |
| Rasterizerorderedstructuredbuffer  | [**Rwstructuredbuffer**](sm5-object-rwstructuredbuffer.md)   |
| RasterizerOrderedTexture1D         | [**RWTexture1D**](sm5-object-rwtexture1d.md)                 |
| RasterizerOrderedTexture1DArray    | [**RWTexture1DArray**](sm5-object-rwtexture1darray.md)       |
| RasterizerOrderedTexture2D         | [**RWTexture2D**](sm5-object-rwtexture2d.md)                 |
| RasterizerOrderedTexture2DArray    | [**RWTexture2DArray**](sm5-object-rwtexture2darray.md)       |
| RasterizerOrderedTexture3D         | [**RWTexture3D**](sm5-object-rwtexture3d.md)                 |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shadermodell 5,1](shader-model-5-1.md)
</dt> <dt>

[HLSL-Shader-Modell 5,1 Features für Direct3D 12](hlsl-shader-model-5-1-features-for-direct3d-12.md)
</dt> </dl>

 

 