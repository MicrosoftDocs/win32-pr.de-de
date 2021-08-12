---
title: iadd (sm4 - asm)
description: Ganzzahlige Addition.
ms.assetid: EF78EA65-DC16-469A-9E45-52844FF4BD93
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9226223b5a065714ca17bd63775b8d4e8a3bc9b96de111cec87b879114728bf6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118285789"
---
# <a name="iadd-sm4---asm"></a>iadd (sm4 - asm)

Ganzzahlige Addition.



| iadd dest \[ .mask \] , \[ - \] src0 \[ .swizzle \] , \[ - \] src1 \[ .swizzle\] |
|------------------------------------------------------------------|



 



| Element                                                            | Beschreibung                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[in \] Die Adresse des Ergebnisses des Vorgangs.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] Die Zahl, die *src1 hinzugefügt werden soll.*<br/>           |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[in \] Die Zahl, die *src0* hinzugefügt werden soll.<br/>           |



 

## <a name="remarks"></a>Hinweise

Komponentenweises Hinzufügen der 32-Bit-Operanden *src0* und *src1,* das richtige 32-Bit-Ergebnis wird in *dest platziert.* Über die 32-Bit-Werte der einzelnen Komponenten hinaus wird kein Carry oder Borrow ausgeführt, sodass diese Anweisung nicht für die Signiertheit ihrer Operanden sensibel ist.

Der optionale Negatmodifizierer für Quellopernden nimmt vor dem Ausführen des Vorgangs ein Komplement von 2 an.

Diese Anweisung gilt für die folgenden Shaderstufen:



| Vertexshader | Geometrie-Shader | Pixelshader |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Minimales Shadermodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                              | Unterstützt |
|-----------------------------------------------------------|-----------|
| [Shadermodell 5](d3d11-graphics-reference-sm5.md)        | ja       |
| [Shadermodell 4.1](dx-graphics-hlsl-sm4.md)              | ja       |
| [Shadermodell 4](dx-graphics-hlsl-sm4.md)                | ja       |
| [Shadermodell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | nein        |
| [Shadermodell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | nein        |
| [Shadermodell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | nein        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shader Model 4-Assembly (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





