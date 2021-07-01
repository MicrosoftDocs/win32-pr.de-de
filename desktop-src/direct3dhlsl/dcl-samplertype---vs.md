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
ms.openlocfilehash: 2fbcb934ad591274d743f09c810de2db42278261
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129868"
---
# <a name="dcl_samplertype-sm3---vs-asm"></a>dcl \_ samplerType (sm3 – vs asm)

Deklarieren Sie einen Vertex-Shader-Sampler.

## <a name="syntax"></a>Syntax

dcl \_ samplerType s\#



 

Dabei gilt:

-   \_samplerType definiert den Samplerdatentyp. Dadurch wird bestimmt, wie viele Koordinaten für jede Texturkoordinate beim Sampling erforderlich sind. Die folgenden Texturkoordinatendimensionen sind definiert.
    -   \_2d
    -   \_Cube
    -   \_Volumen
-   s \# identifiziert einen Sampler, wobei s eine Abkürzung für den \# Sampler und die Samplernummer ist. [Sampler (Direct3D 9 asm-vs)](dx9-graphics-reference-asm-vs-registers-sampler.md)sind Pseudoregister, da sie nicht direkt gelesen oder geschrieben werden können.

## <a name="remarks"></a>Bemerkungen



| Vertex-Shaderversionen | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| dcl \_ samplerType       |      |      |      |       | x    | x     |



 

Alle dcl \_ samplerType-Anweisungen müssen vor der ersten ausführbaren Anweisung angezeigt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Shaderanweisungen](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




