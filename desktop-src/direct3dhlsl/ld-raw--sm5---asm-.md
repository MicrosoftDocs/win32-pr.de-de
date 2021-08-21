---
title: ld_raw (sm5 - asm)
description: Random-access read of 1-4 32bit components from a raw buffer (Zufälliger Zugriff von 1-4 32-Bit-Komponenten aus einem Rohdatenpuffer).
ms.assetid: F7DBA80D-4DD5-4271-B571-24FB6188ABFE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85fd8ec84b574d506a02812b20f4728e3f7a996ec76ad8569645d4c1643b0ec6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118511090"
---
# <a name="ld_raw-sm5---asm"></a>ld \_ raw (sm5 - asm)

Random-access read of 1-4 32bit components from a raw buffer (Zufälliger Zugriff von 1-4 32-Bit-Komponenten aus einem Rohdatenpuffer).



| ld \_ raw dst0 \[ .mask , \] srcByteOffset \[ .select component , \_ \] src0 \[ .swizzle\] |
|------------------------------------------------------------------------------|



 



| Element                                                                                                                       | Beschreibung                                                   |
|----------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="dst0"></span><span id="DST0"></span>*dst0*<br/>                                                            | \[in \] Die Adresse des Ergebnisses des Vorgangs.<br/> |
| <span id="srcByteOffset"></span><span id="srcbyteoffset"></span><span id="SRCBYTEOFFSET"></span>*srcByteOffset*<br/> | \[in \] Gibt den Offset an, aus dem gelesen werden soll.<br/>          |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                                            | \[in \] Die zu lesende Komponente. <br/>                     |



 

## <a name="remarks"></a>Hinweise

*src0* muss:

-   Beliebige Shaderstufe: SRV (t \# )ld st
-   Compute-Shader oder Pixel-Shader: UAV (u \# )
-   Compute-Shader: freigegebener Threadgruppenspeicher (g \# )

*srcByteOffset* gibt den 32-Bit-Basiswert im Arbeitsspeicher für ein Fenster mit 4 sequenziellen 32-Bit-Werten an, in dem Daten gelesen werden können, je nach Swizzle und Maske für andere Parameter.

Die aus dem Rohdatenpuffer gelesenen Daten entsprechen dem folgenden Pseudocode: hier sind offset, address, zeiger auf den Pufferinhalt, stride der Quelle und die daten linear gespeichert.

``` syntax
                    BYTE *BufferContents;         // from src0
                    UINT srcByteOffset;           // from srcRegister
                    BYTE *ReadLocation;           // value to calculate
                    ReadLocation = BufferContents 
                                + srcByteOffset;

                    UINT32 Temp[4];  // used to make code shorter

                    // apply the source resource swizzle on source data
                    Temp = read_and_swizzle(ReadLocation, srcSwizzle);

                    // write the components to the output based on mask
                    ApplyWriteMask(dstRegister, dstWriteMask, Temp);
```

Die Adressierung von "out of bounds" für u /t einer bestimmten \# \# 32-Bit-Komponente gibt 0 für diese Komponente zurück.

Die Adressierung für g (die Grenzen dieses bestimmten g im Gegensatz zum freigegebenen Speicher) für eine bestimmte \# 32-Bit-Komponente gibt ein nicht definiertes \# Ergebnis zurück.

cs \_ 4 \_ 0 und cs \_ 4 \_ 1 unterstützen diese Anweisung für UAV und SRV.

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



 

cs \_ 4 \_ 0 und cs \_ 4 \_ 1 unterstützen diese Anweisung für UAV und SRV.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shader Model 5-Assembly (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





