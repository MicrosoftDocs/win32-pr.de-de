---
title: dcl_samplerType (sm2, sm3 – ps asm)
description: Deklarieren Sie einen Pixelshader-Sampler.
ms.assetid: c90ff5b6-f89a-4993-8a5d-dbbc4a7896b0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7a6da220e50b43ce990c090c61d1caf84afec653
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129667"
---
# <a name="dcl_samplertype-sm2-sm3---ps-asm"></a>dcl \_ samplerType (sm2, sm3 – ps asm)

Deklarieren Sie einen Pixelshader-Sampler.

## <a name="syntax"></a>Syntax

dcl \_ samplerType s\#



 

Dabei gilt:

-   \_samplerType definiert den Samplerdatentyp. Dadurch wird bestimmt, wie viele Koordinaten für jede Texturkoordinate beim Sampling erforderlich sind. Die folgenden Texturkoordinatendimensionen sind definiert.
    -   \_2d
    -   \_Cube
    -   \_Volumen
-   s \# identifiziert einen Sampler, wobei s eine Abkürzung für den Sampler \# und die Samplernummer ist. Sampler sind Pseudoregister, da Sie sie nicht direkt lesen oder schreiben können.

## <a name="remarks"></a>Bemerkungen



| Pixelshaderversionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| dcl \_ samplerType      |      |      |      |      | x    | x    | x     | x    | x     |



 

Alle dcl \_ samplerType-Anweisungen müssen vor der ersten ausführbaren Anweisung angezeigt werden.

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

 

 




