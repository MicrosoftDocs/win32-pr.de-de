---
title: dcl_samplerType (sm3 – vs asm)
description: Deklarieren Sie einen Vertex-Shader-Sampler.
ms.assetid: 733307ac-24ab-4db7-bf70-58a83b4c39b1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 048246f8a48430dca26a763e9266f00edd61215e769f4ff5385036054aebc34b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726570"
---
# <a name="dcl_samplertype-sm3---vs-asm"></a>dcl \_ samplerType (sm3 – vs asm)

Deklarieren Sie einen Vertex-Shader-Sampler.

## <a name="syntax"></a>Syntax

dcl \_ samplerType s\#



 

Dabei gilt:

-   \_samplerType definiert den Samplerdatentyp. Dadurch wird bestimmt, wie viele Koordinaten von jeder Texturkoordinate beim Sampling benötigt werden. Die folgenden Texturkoordinatendimensionen sind definiert.
    -   \_2d
    -   \_Cube
    -   \_Volumen
-   s \# identifiziert einen Sampler, wobei s eine Abkürzung für den Sampler und \# die Samplernummer ist. [Sampler (Direct3D 9 asm-vs)](dx9-graphics-reference-asm-vs-registers-sampler.md)sind Pseudoregister, da sie nicht direkt gelesen oder geschrieben werden können.

## <a name="remarks"></a>Hinweise



| Vertex-Shaderversionen | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| dcl \_ samplerType       |      |      |      |       | x    | x     |



 

Alle dcl \_ samplerType-Anweisungen müssen vor der ersten ausführbaren Anweisung angezeigt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Shaderanweisungen](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




