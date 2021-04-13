---
title: DCL-(SM2, SM3-PS ASM)
description: Deklarieren Sie ein Pixel-Shader-Eingabe Register.
ms.assetid: d6fcd94e-80d7-4e8a-8b4f-ff86c980cc38
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ad61ea8d733ed01fcd2e57ba06c38e0b3efac682
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104389566"
---
# <a name="dcl---sm2-sm3---ps-asm"></a>DCL-(SM2, SM3-PS ASM)

Deklarieren Sie ein Pixel-Shader-Eingabe Register.

## <a name="syntax"></a>Syntax



|                           |
|---------------------------|
| DCL- \[ \_ PP \] \[ : dest. Mask\] |



 

Hierbei gilt:

-   \[\_PP \] ist eine optionale partielle Genauigkeit. Siehe [partielle Genauigkeit](dx9-graphics-reference-asm-ps-instructions-modifiers-ps-2-0.md).
-   dest ist ein Ziel Register. Dabei muss es sich entweder um ein [Eingabe Farbregister](dx9-graphics-reference-asm-ps-registers-input-color.md) (VN) oder um ein [Texturkoordinaten Register](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (TN) handeln.
-   \[. mask \] ist eine optionale Schreib Maske, mit der gesteuert wird, auf welche Komponenten des Ziel Registers geschrieben werden kann. Siehe [Ziel Registrierung schreiben Mask](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md).

## <a name="remarks"></a>Bemerkungen



| Pixel-Shader-Versionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| DCL                   |      |      |      |      | x    | x    | x     | x    | x     |



 

Alle DCL-Anweisungen müssen vor der ersten ausführbaren Anweisung angezeigt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixelshaderanweisungen](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




