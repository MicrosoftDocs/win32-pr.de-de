---
title: Sampler (Direct3D 9 ASM-vs)
description: Ein Sampler ist ein Eingabe-Pseudo Register für einen Vertex-Shader, der zum Identifizieren der Samplingphase verwendet wird. Es gibt vier Vertex-Shader-Samplern S0 in S3. Vier Textur Oberflächen können in einem einzelnen shaderdurchlauf gelesen werden.
ms.assetid: a4588ced-24e2-4d4e-93e4-35a985bafaa4
keywords:
- Sampler, Type (Direct3D 9 ASM-vs)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 685f261da9d56dc29c0632d01cabbf29cd13a00f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390956"
---
# <a name="sampler-direct3d-9-asm-vs"></a>Sampler (Direct3D 9 ASM-vs)

Ein Sampler ist ein Eingabe-Pseudo Register für einen Vertex-Shader, der zum Identifizieren der Samplingphase verwendet wird. Es gibt vier Vertex-Shader-Samplers: S0 bis S3. Vier Textur Oberflächen können in einem einzelnen shaderdurchlauf gelesen werden.

Sampler (Direct3D 9 ASM-vs) s sind Pseudo Register, da Sie Sie nicht direkt lesen oder schreiben können.

Eine samplingeinheit entspricht der Phase der Textur Stichprobe und kapselt den samplingspezifischen Zustand, der von [**setsamplerstate**](/windows/desktop/api/d3d9/nf-d3d9-idirect3ddevice9-setsamplerstate)bereitgestellt wird. Jeder Sampler identifiziert eindeutig eine einzelne Textur Oberfläche, die auf den entsprechenden Sampler mithilfe von [**SetTexture**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture)festgelegt wird. Allerdings kann die gleiche Textur Oberfläche bei mehreren Samplers festgelegt werden.

Bei der zeichnungszeit kann eine Textur nicht gleichzeitig als Renderziel und Textur in einer Phase festgelegt werden.

Da vier Samplers vorhanden sind, können bis zu vier Textur Oberflächen in einem einzelnen shaderdurchlauf aus gelesen werden. Ein Sampler kann als einziges Argument in der Textur Lade Anweisung angezeigt werden: [texldl-vs](texldl---vs.md).

Wenn in vs \_ 3 \_ 0 ein Sampler verwendet wird, muss er am Anfang des Shader-Programms mithilfe der [DCL \_ -Anweisung samplertype (SM3-vs ASM)](dcl-samplertype---vs.md) deklariert werden.



| Vertex-Shader-Versionen | 1\_1 | 2 \_ 0 | 2 \_ SW | 2 \_ x | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|-------|------|------|-------|
| Sampler                |      |      |       |      | x    | x     |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Shader-Register](dx9-graphics-reference-asm-vs-registers.md)
</dt> <dt>

[Scheitelpunkt Texturen in vs \_ 3 \_ 0 (DirectX HLSL)](/windows/desktop/direct3d9/vertex-textures-in-vs-3-0)
</dt> </dl>

 

 