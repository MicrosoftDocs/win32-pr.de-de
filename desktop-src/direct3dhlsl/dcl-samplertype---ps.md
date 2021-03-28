---
title: dcl_samplerType (SM2, SM3-PS ASM)
description: Deklarieren Sie einen Pixel-Shadersampler.
ms.assetid: c90ff5b6-f89a-4993-8a5d-dbbc4a7896b0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 934931d6063ac264a2e6685104f8ed6fbdaaa64e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104038369"
---
# <a name="dcl_samplertype-sm2-sm3---ps-asm"></a>DCL- \_ samplertype (SM2, SM3-PS ASM)

Deklarieren Sie einen Pixel-Shadersampler.

## <a name="syntax"></a>Syntax



|                      |
|----------------------|
| DCL- \_ samplertype s\# |



 

Dabei gilt:

-   \_samplertype definiert den samplerdatentyp. Dies bestimmt, wie viele Koordinaten bei der Stichprobenentnahme für jede Textur Koordinate erforderlich sind. Die folgenden Texturkoordinaten Dimensionen sind definiert.
    -   \_2D
    -   \_Cube
    -   \_Handels
-   s \# identifiziert einen Sampler, bei dem s eine Abkürzung für den Sampler und \# die samplernummer ist. Samplers sind Pseudo Register, da Sie Sie nicht direkt lesen oder schreiben können.

## <a name="remarks"></a>Bemerkungen



| Pixel-Shader-Versionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| DCL- \_ samplertype      |      |      |      |      | x    | x    | x     | x    | x     |



 

Alle DCL- \_ samplertype-Anweisungen müssen vor der ersten ausführbaren Anweisung angezeigt werden.

## <a name="example"></a>Beispiel


```
dcl_cube t0.rgb;  // Define a 3D texture map.

add r0, r0, t0;   // Perturb texture coordinates. 
texld r0, s0, r0; // Load r0 with a color sampled from stage0
                  //   at perturbed texture coordinates r0.
                  // This is a dependent texture read.
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixelshaderanweisungen](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




