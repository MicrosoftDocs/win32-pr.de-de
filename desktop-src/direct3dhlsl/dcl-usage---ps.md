---
title: dcl_semantics (SM3-PS ASM)
description: Deklarieren Sie die Zuordnung zwischen der Vertex-Shader-Ausgabe und der Pixel-Shadereingabe.
ms.assetid: 4f4dc6fe-0efa-4d84-aefd-583e90ab9a61
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 944ddd2b581c6179ac4a3fe22f2b687f85aecfdc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101958"
---
# <a name="dcl_semantics-sm3---ps-asm"></a>DCL \_ -Semantik (SM3-PS ASM)

Deklarieren Sie die Zuordnung zwischen der Vertex-Shader-Ausgabe und der Pixel-Shadereingabe.

## <a name="syntax"></a>Syntax



|                                                   |
|---------------------------------------------------|
| DCL- \_ Semantik \[ \_ Schwerpunkt \] DST \[ . Write \_ Mask\] |



 

Hierbei gilt:

-   \_Semantik: identifiziert die beabsichtigte Datenverwendung und kann beliebige Werte in [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) (ohne das \_ Präfix D3DDECLUSAGE) sein. Außerdem kann ein ganzzahliger Index an die Semantik angehängt werden, um Parameter zu unterscheiden, die eine ähnliche Semantik verwenden.
-   \[\_Schwerpunkt [](dx9-graphics-reference-asm-ps-instructions-modifiers-ps-2-0.md) \] ist ein optionaler Anweisungs Modifizierer. Sie wird in DCL \_ -Verwendungs Anweisungen unterstützt, die die Eingabe Register deklarieren, und in den Anweisungen für die Textur Suche. Dem Schwerpunkt wird kein Leerzeichen angefügt.
-   DST: Ziel Register. Siehe [PS \_ 3 \_ 0-Register](dx9-graphics-reference-asm-ps-registers-ps-3-0.md).
-   Schreib \_ Maske: dasselbe Ausgabe Register kann mehrmals deklariert werden, jedes Mal mit einer eindeutigen Schreib Maske (damit eine andere Semantik auf einzelne Komponenten angewendet werden kann). Die gleiche Semantik kann jedoch nicht mehrmals in einer Deklaration verwendet werden. Dies bedeutet, dass Vektoren vier Komponenten oder weniger sein müssen und nicht über vier Komponenten Register Grenzen (einzelne Ausgabe Register) hinausgehen können. Wenn die \_ Psize-Semantik verwendet wird, sollte Sie über eine vollständige Schreib Maske verfügen, da Sie als Skalar angesehen wird. Wenn die \_ Positions Semantik verwendet wird, sollte Sie über eine vollständige Schreib Maske verfügen, da alle vier Komponenten geschrieben werden müssen.

## <a name="remarks"></a>Bemerkungen



| Pixel-Shader-Versionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| DCL- \_ Verwendung            |      |      |      |      |      |      |       | x    | x     |



 

Alle DCL- \_ Verwendungs Anweisungen müssen vor der ersten ausführbaren Anweisung angezeigt werden.

## <a name="declaration-examples"></a>Deklarations Beispiele


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

[Beispiel für AntiAlias](https://msdn.microsoft.com/library/Ee415231(v=VS.85).aspx)
</dt> </dl>

 

 