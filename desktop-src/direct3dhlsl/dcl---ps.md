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
ms.openlocfilehash: dab377a36cb1323daf450b9566e419b60edc1fb80dde54591a932b2e0f28223a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118793466"
---
# <a name="dcl---sm2-sm3---ps-asm"></a>dcl - (sm2, sm3 - ps asm)

Deklarieren Sie ein Pixel-Shader-Eingaberegister.

## <a name="syntax"></a>Syntax

dcl \[ \_ pp \] dest \[ .mask\]



 

Hierbei gilt:

-   \[\_pp \] ist optional partielle Genauigkeit. Weitere Informationen [finden Sie unter Partielle Genauigkeit.](dx9-graphics-reference-asm-ps-instructions-modifiers-ps-2-0.md)
-   dest ist ein Zielregister. Es muss entweder ein [Eingabefarbregister](dx9-graphics-reference-asm-ps-registers-input-color.md) (vn) oder ein [Texturkoordinatenregister](dx9-graphics-reference-asm-ps-registers-texture-coordinate.md) (tn) sein.
-   \[.mask ist eine optionale Schreibmaske, die steuert, in welche Komponenten des \] Zielregisters geschrieben werden kann. Weitere Informationen finden [Sie unter Zielregister-Schreibmaske.](dx9-graphics-reference-asm-ps-registers-modifiers-write-mask.md)

## <a name="remarks"></a>Hinweise



| Pixel-Shaderversionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| Dcl                   |      |      |      |      | x    | x    | x     | x    | x     |



 

Alle dcl-Anweisungen müssen vor der ersten ausführbaren Anweisung angezeigt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anweisungen für Pixel-Shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




