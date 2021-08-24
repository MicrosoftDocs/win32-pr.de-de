---
title: Sampler (Direct3D 9 asm-vs)
description: Ein Sampler ist ein Eingabe-Pseudoregister für einen Vertex-Shader, der zum Identifizieren der Samplingphase verwendet wird. Es gibt vier Vertex-Shader-Sampler s0 bis s3. Vier Texturoberflächen können in einem einzelnen Shaderdurchlauf gelesen werden.
ms.assetid: a4588ced-24e2-4d4e-93e4-35a985bafaa4
keywords:
- Sampler, Type (Direct3D 9 asm-vs)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3bd822dc085243adeb97a4baaedce35b150db311ab6b98c531a3e33731635666
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119789080"
---
# <a name="sampler-direct3d-9-asm-vs"></a>Sampler (Direct3D 9 asm-vs)

Ein Sampler ist ein Eingabe-Pseudoregister für einen Vertex-Shader, der zum Identifizieren der Samplingphase verwendet wird. Es gibt vier Vertex-Shader-Sampler: s0 bis s3. Vier Texturoberflächen können in einem einzelnen Shaderdurchlauf gelesen werden.

Sampler (Direct3D 9 asm-vs)s sind Pseudoregister, da sie nicht direkt gelesen oder geschrieben werden können.

Eine Samplingeinheit entspricht der Textursamplingphase, die den samplingspezifischen Zustand von [**SetSamplerState**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setsamplerstate)kapselt. Jeder Sampler identifiziert eindeutig eine einzelne Texturoberfläche, die mithilfe von [**SetTexture**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture)auf den entsprechenden Sampler festgelegt wird. Die gleiche Texturoberfläche kann jedoch an mehreren Samplern festgelegt werden.

Zur Zeichnenzeit kann eine Textur nicht gleichzeitig als Renderziel und textur in einer Phase festgelegt werden.

Da es vier Sampler gibt, können bis zu vier Texturoberflächen in einem einzelnen Shaderdurchlauf gelesen werden. Ein Sampler kann als einziges Argument in der Texturladeanweisung angezeigt werden: [texldl - vs](texldl---vs.md).

Wenn \_ ein \_ Sampler im Vergleich zu 3 0 verwendet wird, muss er am Anfang des Shaderprogramms mithilfe der [dcl \_ samplerType-Anweisung (sm3 - vs asm)](dcl-samplertype---vs.md) deklariert werden.



| Vertex-Shaderversionen | 1\_1 | 2 \_ 0 | 2 \_ sw | 2 \_ x | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|-------|------|------|-------|
| Sampler                |      |      |       |      | x    | x     |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Shaderregister](dx9-graphics-reference-asm-vs-registers.md)
</dt> <dt>

[Scheitelpunkttexturen im Vergleich \_ zu 3 \_ 0 (DirectX HLSL)](/windows/desktop/direct3d9/vertex-textures-in-vs-3-0)
</dt> </dl>

 

 