---
title: ld_structured (SM5-ASM)
description: Zufälliger Lesezugriff auf 1-4 32-Bit-Komponenten aus einem strukturierten Puffer.
ms.assetid: ED572B76-FF6C-405E-9110-4B12AD5E5AE6
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00a34bafdcfbe0658723dd83d62507e255ff4bfa
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104389556"
---
# <a name="ld_structured-sm5---asm"></a>LD \_ strukturiert (SM5-ASM)

Zufälliger Lesezugriff auf 1-4 32-Bit-Komponenten aus einem strukturierten Puffer.



| : LD \_ strukturiert dst0 \[ . mask \] , srcaddress \[ . Select \_ Component \] , srcbyteoffset \[ . Select \_ Component \] , src0 \[ . Swizzle\] |
|-------------------------------------------------------------------------------------------------------------------------|



 



| Element                                                                                                                       | BESCHREIBUNG                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="dst0"></span><span id="DST0"></span>*dst0*<br/>                                                            | \[in \] der Adresse der Ergebnisse des Vorgangs.<br/>                                                                                             |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcaddress*<br/>             | \[in \] gibt den Index der zu lesenden-Struktur an.<br/>                                                                                            |
| <span id="srcByteOffset"></span><span id="srcbyteoffset"></span><span id="SRCBYTEOFFSET"></span>*srcbyteoffset*<br/> | \[in \] gibt den Byte Offset in der-Struktur an, ab dem gelesen werden soll. <br/>                                                                       |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                                            | Der Puffer, aus dem gelesen werden soll. Dieser Parameter muss ein SRV (t \# ), UAV (u \# ) sein. Im COMPUTE-Shader kann es sich auch um einen Thread Gruppen-Shared Memory (g \# ) handeln. <br/> |



 

## <a name="remarks"></a>Bemerkungen

Die aus der-Struktur gelesenen Daten entsprechen dem folgenden Pseudocode: wobei der Offset, die Adresse, der Zeiger auf den Pufferinhalt, der Schritt der Quelle und die Daten linear gespeichert sind.

``` syntax
                    BYTE *BufferContents;         // from SRV or UAV
                    UINT BufferStride;            // from base resource
                    UINT srcAddress, srcByteOffset;   // from source registers
                    BYTE *ReadLocation;           // value to calculate
                    ReadLocation = BufferContents 
                                + BufferStride * srcByteOffset
                                + srcOffset;

                    UINT32 Temp[4];  // used to make code shorter

                    // apply the source resource swizzle on source data
                    Temp = read_and_swizzle(ReadLocation, srcSwizzle);

                    // write the components to the output based on mask
                    ApplyWriteMask(dstRegister, dstWriteMask, Temp);
```

Dieser Pseudo Code zeigt, wie der Vorgang funktioniert, aber die tatsächlichen Daten müssen nicht linear gespeichert werden. Wenn die Daten nicht linear gespeichert werden, muss die tatsächliche Operation der Anweisung mit dem Verhalten des obigen Vorgangs identisch sein.

Die Out-of-Bounds-Adressierung für die u- \# /t \# einer bestimmten 32-Bit-Komponente gibt 0 für diese Komponente zurück. mit Ausnahme von *srcbyteoffset* und Swizzle, was den Zugriff auf Sie \# /t verursacht \# , ist der zurückgegebene Wert für alle Komponenten nicht definiert.

Die Adressierung auf g \# (die Begrenzungen dieses bestimmten g \# , im Gegensatz zum gesamten Shared Memory) für eine bestimmte 32-Bit-Komponente gibt ein nicht definiertes Ergebnis zurück.

*srcbyteoffset* ist ein separates Argument von *srcaddress* , da es sich häufig um einen Literalwert handelt. Diese Parameter Trennung wurde nicht für Atomics in strukturiertem Arbeitsspeicher durchgeführt.

CS \_ 4 \_ 0 und CS \_ 4 \_ 1 unterstützen diese Anweisung für UAV, SRV und TGSM.

Diese Anweisung gilt für die folgenden Shader-Phasen:



| Scheitelpunkt | Hülle | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

Da UAVs in allen Shader-Phasen für Direct3D 11,1 verfügbar sind, gilt diese Anweisung für alle Shader-Phasen für UAVs für die Direct3D 11,1-Laufzeit, die ab Windows 8 verfügbar ist.



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



 

CS \_ 4 \_ 0 und CS \_ 4 \_ 1 unterstützen diese Anweisung für UAV, SRV und TGSM.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shader Model 5-Assembly (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





