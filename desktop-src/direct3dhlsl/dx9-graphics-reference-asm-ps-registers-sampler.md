---
title: Sampler (Direct3D 9 ASM-PS)
description: Ein Sampler ist ein Eingabe-Pseudo Register für einen PixelShader, der zum Identifizieren der Samplingphase verwendet wird.
ms.assetid: 37cc28ae-fbd0-4f81-9e8e-f9609980d84e
keywords:
- Sampler, Typ (Direct3D 9 ASM-PS)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 77875eed0827ad6bcb6d89111b13b6a31232dd86
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039168"
---
# <a name="sampler-direct3d-9-asm-ps"></a>Sampler (Direct3D 9 ASM-PS)

Ein Sampler ist ein Eingabe-Pseudo Register für einen PixelShader, der zum Identifizieren der Samplingphase verwendet wird. Es gibt 16 Pixel-Shader-samplingstaging-Register: S0 in S15. Daher können bis zu 16 Textur Oberflächen in einem einzelnen shaderdurchlauf gelesen werden. Die Anweisungen, die ein Samplerregister verwenden, sind texld und texldp.

Der Sampler muss vor der Verwendung mit der [DCL \_ -Anweisung samplertype (SM2, SM3-PS ASM)](dcl-samplertype---ps.md) deklariert werden.



| Pixel-Shader-Versionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ SW | 2 \_ x | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|-------|------|------|-------|
| Sampler               |      |      |      |      | x    | x     | x    | x    | x     |



 

Samplers sind Pseudo Register, da Sie Sie nicht direkt lesen oder schreiben können.

Eine samplingeinheit entspricht der Phase der Textur Stichprobe und kapselt den samplingspezifischen Zustand, der von [**setsamplerstate**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setsamplerstate)bereitgestellt wird. Jeder Sampler identifiziert eindeutig eine einzelne Textur Oberfläche, die auf den entsprechenden Sampler mithilfe von [**SetTexture**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture)festgelegt wird. Allerdings kann die gleiche Textur Oberfläche bei mehreren Samplers festgelegt werden.

Bei der zeichnungszeit kann eine Textur nicht gleichzeitig als Renderziel und Textur in einer Phase festgelegt werden.

Ein Sampler kann als einziges Argument in der Textur Lade Anweisung angezeigt werden: [texldl-PS](texldl---ps.md).

Wenn in PS \_ 3 \_ 0 ein Sampler verwendet wird, muss er am Anfang des Shader-Programms mithilfe der [DCL-Anweisung \_ samplertype (SM2, SM3-PS ASM)](dcl-samplertype---ps.md) deklariert werden.

Das Sampling einer Textur mit einer höheren Dimension als in den Texturkoordinaten vorhanden ist ungültig. Das Sampling einer Textur mit einer niedrigeren Dimension als in den Texturkoordinaten vorhanden ist, ignoriert die zusätzlichen Texturkoordinaten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Register](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 