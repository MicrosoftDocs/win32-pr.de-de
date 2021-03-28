---
title: BFI (SM5-ASM)
description: Wenn ein Bitbereich vom lsb einer Zahl ist, platzieren Sie die Anzahl der Bits in einem beliebigen Offset in einer anderen Zahl.
ms.assetid: BA84C882-A141-4AD2-8FD9-C60F1483FC65
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a14f8b9f6ef126ec3c6a31bf330dfd89cf0770c4
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104038346"
---
# <a name="bfi-sm5---asm"></a>BFI (SM5-ASM)

Wenn ein Bitbereich vom lsb einer Zahl ist, platzieren Sie die Anzahl der Bits in einem beliebigen Offset in einer anderen Zahl.



| BFI dest \[ . mask \] , src0 \[ . Swizzle \] , Quelle1 \[ . Swizzle \] , Quelle2 \[ . Swizzle \] , src3 \[ . Swizzle\] |
|-------------------------------------------------------------------------------------------|



 



| Element                                                            | BESCHREIBUNG                                                         |
|-----------------------------------------------------------------|---------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[in \] der Adresse der Ergebnisse.<br/>                       |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] der bitfeldbreite, die von *Quelle2* übernommen werden soll.<br/>           |
| <span id="src1"></span><span id="SRC1"></span>*Quelle1*<br/> | \[im \] Bitfeld-Offset zum Ersetzen von Bits in *src3*.<br/> |
| <span id="src2"></span><span id="SRC2"></span>*Quelle2*<br/> | \[in \] der Zahl, von der die Bits entnommen werden. <br/>              |
| <span id="src3"></span><span id="SRC3"></span>*src3*<br/> | \[in \] der Zahl mit Bits, die ersetzt werden sollen.<br/>              |



 

## <a name="remarks"></a>Bemerkungen

Die lsb 5 Bits von *src0* geben die Bitfeld Breite (0-31) an, die von *Quelle2* genommen werden soll.

Die lsb 5-Bits von *Quelle1* stellen den Bitfeld-Offset (0-31) bereit, um die Bits in der von *src3* gelesenen Zahl zu ersetzen.

``` syntax
Given width, offset:
                bitmask = (((1 << width)-1) << offset) & 0xffffffff
                dest = ((src2 << offset) & bitmask) | (src3 & ~bitmask)
```

Diese Anweisung wird zum Packen von Ganzzahlen oder Flags verwendet.

Diese Anweisung gilt für die folgenden Shader-Phasen:



| Scheitelpunkt | Hülle | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Minimaler Shader-Modell

Diese Anweisung wird in den folgenden shadermodellen unterstützt:



| Shadermodell                                              | Unterstützt |
|-----------------------------------------------------------|-----------|
| [Shader-Modell 5](d3d11-graphics-reference-sm5.md)        | ja       |
| [Shadermodell 4,1](dx-graphics-hlsl-sm4.md)              | nein        |
| [Shadermodell 4](dx-graphics-hlsl-sm4.md)                | nein        |
| [Shader-Modell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | nein        |
| [Shader-Modell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | nein        |
| [Shader-Modell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | nein        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shader Model 5-Assembly (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





