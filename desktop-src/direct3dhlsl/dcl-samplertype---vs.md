---
title: dcl_samplerType (SM3-vs ASM)
description: Deklarieren Sie einen Vertex-Shadersampler.
ms.assetid: 733307ac-24ab-4db7-bf70-58a83b4c39b1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 556655d793e94b9290fcd1a4a40fdf7f797e80ae
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993206"
---
# <a name="dcl_samplertype-sm3---vs-asm"></a>DCL \_ -samplertype (SM3-vs ASM)

Deklarieren Sie einen Vertex-Shadersampler.

## <a name="syntax"></a>Syntax



|                      |
|----------------------|
| DCL- \_ samplertype s\# |



 

Dabei gilt:

-   \_samplertype definiert den samplerdatentyp. Dies bestimmt, wie viele Koordinaten bei der Stichprobenentnahme für jede Textur Koordinate erforderlich sind. Die folgenden Texturkoordinaten Dimensionen sind definiert.
    -   \_2D
    -   \_Cube
    -   \_Handels
-   s \# identifiziert einen Sampler, bei dem s eine Abkürzung für den Sampler und \# die samplernummer ist. [Sampler (Direct3D 9 ASM-vs)](dx9-graphics-reference-asm-vs-registers-sampler.md)s sind Pseudo Register, da Sie Sie nicht direkt lesen oder schreiben können.

## <a name="remarks"></a>Bemerkungen



| Vertex-Shader-Versionen | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| DCL- \_ samplertype       |      |      |      |       | x    | x     |



 

Alle DCL- \_ samplertype-Anweisungen müssen vor der ersten ausführbaren Anweisung angezeigt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-shaderanweisungen](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




