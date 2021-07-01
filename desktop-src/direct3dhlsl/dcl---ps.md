---
title: dcl - (sm2, sm3 - ps asm)
description: Deklarieren Sie ein Pixel-Shader-Eingaberegister.
ms.assetid: d6fcd94e-80d7-4e8a-8b4f-ff86c980cc38
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4f2ba81650611351970ff4068edaa75d27d34fc4
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/01/2021
ms.locfileid: "113130099"
---
# <a name="dcl---sm2-sm3---ps-asm"></a>dcl - (sm2, sm3 - ps asm)

Deklarieren Sie ein Pixel-Shader-Eingaberegister.

## <a name="syntax"></a>Syntax

dcl \[ \_ pp \] dest \[ .mask\]



 

Hierbei gilt:

-   \[\_pp \] ist eine optionale partielle Genauigkeit. Weitere Informationen finden Sie unter [Partielle Genauigkeit.](dx9-graphics-reference-asm-ps-instructions-modifiers-ps-2-0.md)
-   dest ist ein Zielregister. Dabei muss es sich entweder um ein [Eingabefarbregister](dx9-graphics-reference-asm-ps-registers-input-color.md) (vn) oder um ein [Texturkoordinatenregister](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (tn) handelt.
-   \[.mask \] ist eine optionale Schreibmaske, die steuert, in welche Komponenten des Zielregisters geschrieben werden kann. Weitere Informationen finden Sie unter [Zielregister-Schreibmaske.](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md)

## <a name="remarks"></a>Bemerkungen



| Pixelshaderversionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| Dcl                   |      |      |      |      | x    | x    | x     | x    | x     |



 

Alle dcl-Anweisungen müssen vor der ersten ausführbaren Anweisung angezeigt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixelshaderanweisungen](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




