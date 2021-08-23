---
title: ld_structured (sm5 - asm)
description: Zufälliger Lesezugriff von 1-4 32-Bit-Komponenten aus einem strukturierten Puffer.
ms.assetid: ED572B76-FF6C-405E-9110-4B12AD5E5AE6
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfb3c19b56271a02c20ff85dd71352b545843f62b3d01292e87c2edbd6384d83
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119562310"
---
# <a name="ld_structured-sm5---asm"></a>ld \_ structured (sm5 - asm)

Zufälliger Lesezugriff von 1-4 32-Bit-Komponenten aus einem strukturierten Puffer.



| : ld \_ structured dst0 \[ .mask \] , srcAddress \[ .select component , \_ \] srcByteOffset \[ .select component , \_ \] src0 \[ .swizzle\] |
|-------------------------------------------------------------------------------------------------------------------------|



 



| Element                                                                                                                       | Beschreibung                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="dst0"></span><span id="DST0"></span>*dst0*<br/>                                                            | \[in \] Die Adresse der Ergebnisse des Vorgangs.<br/>                                                                                             |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>             | \[in \] Gibt den Index der zu lesenden Struktur an.<br/>                                                                                            |
| <span id="srcByteOffset"></span><span id="srcbyteoffset"></span><span id="SRCBYTEOFFSET"></span>*srcByteOffset*<br/> | \[in \] Gibt den Byteoffset in der -Struktur an, von der aus gelesen werden soll. <br/>                                                                       |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                                            | Der Puffer, aus dem gelesen werden soll. Dieser Parameter muss ein SRV (t \# ), UAV (u \# ) sein. Im Compute-Shader kann es sich auch um gemeinsam genutzten Threadgruppenspeicher (g ) \# sein. <br/> |



 

## <a name="remarks"></a>Hinweise

Die aus der -Struktur gelesenen Daten entsprechen dem folgenden Pseudocode: hier haben wir den Offset, die Adresse, den Zeiger auf den Pufferinhalt, den Schritt der Quelle und die linear gespeicherten Daten.

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

Dieser Pseudocode zeigt, wie der Vorgang funktioniert, aber die tatsächlichen Daten müssen nicht linear gespeichert werden. Wenn die Daten nicht linear gespeichert werden, muss der tatsächliche Vorgang der Anweisung mit dem Verhalten des oben genannten Vorgangs übereinstimmen.

Die Adressierung außerhalb der Grenzen für u /t einer bestimmten 32-Bit-Komponente gibt 0 für diese Komponente zurück, außer wenn \# \# *srcByteOffset* und swizzle den Zugriff außerhalb der Grenzen für \# Sie /t verursacht, ist der zurückgegebene Wert für alle Komponenten \# nicht definiert.

Die Adressierung für g (die Grenzen dieses bestimmten g im Gegensatz zum freigegebenen Speicher) für eine bestimmte \# 32-Bit-Komponente gibt ein nicht definiertes \# Ergebnis zurück.

*srcByteOffset* ist ein separates Argument von *srcAddress,* da es sich im Allgemeinen um ein Literal handelt. Diese Parametertrennung wurde für Atomardaten im strukturierten Speicher nicht durchgeführt.

cs \_ 4 \_ 0 und cs \_ 4 1 unterstützen diese Anweisung für \_ UAV, SRV und TGSM.

Diese Anweisung gilt für die folgenden Shaderstufen:



| Scheitelpunkt | Rumpf | Domäne | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

Da UAVs in allen Shaderstufen für Direct3D 11.1 verfügbar sind, gilt diese Anweisung für alle Shaderstufen für UAVs für die Direct3D 11.1-Runtime, die ab Windows 8.



| Scheitelpunkt | Rumpf | Domäne | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Minimales Shadermodell

Diese Anweisung wird in den folgenden Shadermodellen unterstützt:



| Shadermodell                                              | Unterstützt |
|-----------------------------------------------------------|-----------|
| [Shadermodell 5](d3d11-graphics-reference-sm5.md)        | Ja       |
| [Shadermodell 4.1](dx-graphics-hlsl-sm4.md)              | Nein        |
| [Shadermodell 4](dx-graphics-hlsl-sm4.md)                | Nein        |
| [Shadermodell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | Nein        |
| [Shadermodell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | Nein        |
| [Shadermodell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | Nein        |



 

cs \_ 4 \_ 0 und cs \_ 4 1 unterstützen diese Anweisung für \_ UAV, SRV und TGSM.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shader Model 5-Assembly (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





