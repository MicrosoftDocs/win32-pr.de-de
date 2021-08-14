---
title: dcl_semantics (sm3 – ps asm)
description: Deklarieren Sie die Zuordnung zwischen der Vertex-Shaderausgabe und der Pixel-Shadereingabe.
ms.assetid: 4f4dc6fe-0efa-4d84-aefd-583e90ab9a61
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 91a57ec2eabbef2cd62fec8fa95fbf9d2da47a5bfcdb339bf30ed8da5b11c9ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118792929"
---
# <a name="dcl_semantics-sm3---ps-asm"></a>\_dcl-Semantik (sm3 – ps asm)

Deklarieren Sie die Zuordnung zwischen der Vertex-Shaderausgabe und der Pixel-Shadereingabe.

## <a name="syntax"></a>Syntax

dcl \_ semantics \[ \_ schwerpunktid \] dst \[ .write \_ mask\]



 

Hierbei gilt:

-   \_semantics: Identifiziert die beabsichtigte Datenverwendung und kann einer der Werte in [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) sein (ohne das Präfix D3DDECLUSAGE). \_ Darüber hinaus kann ein ganzzahliger Index an die Semantik angefügt werden, um Parameter zu unterscheiden, die eine ähnliche Semantik verwenden.
-   \[\_[Schwerpunkt](dx9-graphics-reference-asm-ps-instructions-modifiers-ps-2-0.md) \] ist ein optionaler Anweisungsmodifizierer. Sie wird in \_ dcl-Verwendungsanweisungen unterstützt, die die Eingaberegister deklarieren, und in Anweisungen zur Textursuche. Der Schwerpunkt wird ohne Leerzeichen angefügt.
-   dst: Zielregister. Siehe [ps \_ 3 \_ 0 Registers](dx9-graphics-reference-asm-ps-registers-ps-3-0.md).
-   \_Schreibmaske: Das gleiche Ausgaberegister kann mehrmals deklariert werden, jedes Mal mit einer eindeutigen Schreibmaske (sodass verschiedene Semantik auf einzelne Komponenten angewendet werden kann). Dieselbe Semantik kann jedoch nicht mehrmals in einer Deklaration verwendet werden. Dies bedeutet, dass Vektoren mindestens vier Komponenten sein müssen und nicht über Vier-Komponenten-Registergrenzen (einzelne Ausgaberegister) hinausgehen können. Wenn die \_ Psize-Semantik verwendet wird, sollte sie über eine vollständige Schreibmaske verfügen, da sie als Skalar gilt. Wenn die \_ Positionssemantik verwendet wird, sollte sie über eine vollständige Schreibmaske verfügen, da alle vier Komponenten geschrieben werden müssen.

## <a name="remarks"></a>Hinweise



| Pixelshaderversionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| dcl \_ usage            |      |      |      |      |      |      |       | x    | x     |



 

Alle \_ dcl-Verwendungsanweisungen müssen vor der ersten ausführbaren Anweisung angezeigt werden.

## <a name="declaration-examples"></a>Deklarationsbeispiele


```
ps_3_0

; Declaring inputs
dcl_normal      v0.xyz
dcl_blendweight v0.w ; Must be same reg# as normal, matching vshader packing
dcl_texcoord1   v1.y ; Mask can be any subset of mask from vshader semantic
dcl_texcoord0   v1.zw; Has to be same reg# as texcoord1, to match vshader

; Declaring samplers
dcl_2d s0
dcl_2d s1

def c0, 0, 0, 0, 0

mov r0.x, v1.y ; texcoord1
mov r0.y, c0
texld r0, r0, s0

texld r1, v1.zw, s1
...
(output regs in ps_3_0 are same as ps_2_0: oC0-oC3, oDepth)
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixelshaderanweisungen](dx9-graphics-reference-asm-ps-instructions.md)
</dt> <dt>

[Antialias-Beispiel](https://msdn.microsoft.com/library/Ee415231(v=VS.85).aspx)
</dt> </dl>

 

 
