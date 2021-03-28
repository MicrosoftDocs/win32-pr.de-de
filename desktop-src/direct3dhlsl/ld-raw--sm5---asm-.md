---
title: ld_raw (SM5-ASM)
description: Zufälliger Zugriffs Lesevorgang von 1-4 32-Bit-Komponenten aus einem RAW-Puffer.
ms.assetid: F7DBA80D-4DD5-4271-B571-24FB6188ABFE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd4a9480ef60098b394e0eff2b06043fd9a32e45
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104976400"
---
# <a name="ld_raw-sm5---asm"></a>LD \_ RAW (SM5-ASM)

Zufälliger Zugriffs Lesevorgang von 1-4 32-Bit-Komponenten aus einem RAW-Puffer.



| LD \_ RAW dst0 \[ . mask \] , srcbyteoffset \[ . Select \_ Component \] , src0 \[ . Swizzle\] |
|------------------------------------------------------------------------------|



 



| Element                                                                                                                       | BESCHREIBUNG                                                   |
|----------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="dst0"></span><span id="DST0"></span>*dst0*<br/>                                                            | \[in \] der Adresse des Vorgangs Ergebnisses.<br/> |
| <span id="srcByteOffset"></span><span id="srcbyteoffset"></span><span id="SRCBYTEOFFSET"></span>*srcbyteoffset*<br/> | \[in \] gibt den Offset an, aus dem gelesen werden soll.<br/>          |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                                            | \[in \] der zu lesenden Komponente. <br/>                     |



 

## <a name="remarks"></a>Bemerkungen

*src0* muss Folgendes sein:

-   Beliebige Shader-Stufe: SRV (t \# ) LD St
-   Compute-Shader oder Pixel-Shader: UAV (u \# )
-   Compute-Shader: Thread Gruppe Shared Memory (g \# )

*srcbyteoffset* gibt den 32-Bit-Basis Wert im Arbeitsspeicher für ein Fenster von 4 sequenziellen 32-Bit-Werten an, in denen Daten möglicherweise gelesen werden, je nach dem flüchtigen und der Maske anderer Parameter.

Die aus dem RAW-Puffer gelesenen Daten entsprechen dem folgenden Pseudo Code:, wobei der Offset, die Adresse, der Zeiger auf den Pufferinhalt, der Stride der Quelle und die Daten linear gespeichert werden.

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

Die Out-of-Bounds-Adressierung für u \# /t \# einer bestimmten 32-Bit-Komponente gibt 0 für diese Komponente zurück.

Die Adressierung auf g \# (die Begrenzungen dieses bestimmten g \# , im Gegensatz zum gesamten Shared Memory) für eine bestimmte 32-Bit-Komponente gibt ein nicht definiertes Ergebnis zurück.

CS \_ 4 \_ 0 und CS \_ 4 \_ 1 unterstützen diese Anweisung für UAV und SRV.

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



 

CS \_ 4 \_ 0 und CS \_ 4 \_ 1 unterstützen diese Anweisung für UAV und SRV.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shader Model 5-Assembly (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





