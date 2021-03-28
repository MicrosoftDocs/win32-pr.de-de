---
title: store_raw (SM5-ASM)
description: Zufälliger Zugriff auf Schreibvorgänge von 1-4 32-Bit-Komponenten in typlosen Arbeitsspeicher.
ms.assetid: D166116A-CF4E-4020-9F6A-F9CEEFCDAB21
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c44b4d22a576853fb8b7d2c43fcb6a2d7fc9a448
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104389582"
---
# <a name="store_raw-sm5---asm"></a>\_rohspeicher (SM5-ASM)

Zufälliger Zugriff auf Schreibvorgänge von 1-4 32-Bit-Komponenten in typlosen Arbeitsspeicher.



| \_Rohdaten speichern dst0 \[ . Write \_ mask \] , dstbyteoffset \[ . Select \_ Component \] , src0 \[ . Swizzle\] |
|----------------------------------------------------------------------------------------|



 



| Element                                                                                                                       | BESCHREIBUNG                                |
|----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------|
| <span id="dst0"></span><span id="DST0"></span>*dst0*<br/>                                                            | \[in \] der Speicheradresse.<br/>      |
| <span id="dstByteOffset"></span><span id="dstbyteoffset"></span><span id="DSTBYTEOFFSET"></span>*dstbyteoffset*<br/> | \[im \] Offset.<br/>              |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                                            | \[in \] den zu schreibende Komponenten.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Diese Anweisung führt 1-4 \* -Komponente 32-Bit-Komponenten aus, die am Offset in *dstbyteoffset* von *src0* in *dst0* geschrieben wurden. Es gibt keine Formatkonvertierung.

*dst0* muss ein UAV (u \# ) sein, oder im COMPUTE-Shader kann es sich auch um einen Thread Gruppen-Shared Memory (g \# ) handeln.

*dstbyteoffset* gibt den 32-Bit-Basis Wert im Arbeitsspeicher für ein Fenster von 4 sequenziellen 32-Bit-Werten an, in dem Daten geschrieben werden können, abhängig von der Striche-und Maske für andere Parameter.

Der Speicherort der geschriebenen Daten entspricht dem folgenden Pseudo Code, der die Adresse, den Zeiger auf den Pufferinhalt und die Daten, die linear gespeichert werden, anzeigt.

``` syntax
                    BYTE *BufferContents;          // from src0
                    UINT dstByteOffset;            // source register
                    BYTE *WriteLocation;           // value to calculate

                    // calculate writing location
                    WriteLocation = BufferContents 
                                + dstByteOffset;

                    // calculate the number of components to write
                    switch (dstWriteMask)
                    {
                        x:    WriteComponents = 1; break;
                        xy:   WriteComponents = 2; break;
                        xyz:  WriteComponents = 3; break;
                        xyzw: WriteComponents = 4; break;
                        default:  // only these masks are valid                              
                    }

                    // copy the data from the source register with
                    //    the swizzle applied
                    memcpy(WriteLocation, swizzle(src0, src0.swizzle), 
                             WriteComponents * sizeof(UINT32));
```

Dieser Pseudo Code zeigt, wie der Vorgang funktioniert, aber die tatsächlichen Daten müssen nicht linear gespeichert werden. *dst0* kann nur eine Schreib Maske aufweisen, die eine der folgenden ist:. x,. XY,. XYZ,. xyzw. Die Schreib Maske bestimmt, wie viele 32-Bit-Komponenten ohne Lücken geschrieben werden.

Die Adressierung von u \# bedeutet, dass nichts in den Speicher außerhalb des gültigen Bereichs geschrieben wird. alle Teile, die sich in den Grenzen befinden, werden ordnungsgemäß geschrieben.

Die Adressierung auf g \# (die Begrenzungen dieses bestimmten g \# , im Gegensatz zum gesamten freigegebenen Speicher) für eine bestimmte 32-Bit-Komponente bewirkt, dass der gesamte Inhalt des gesamten freigegebenen Speichers undefiniert wird.

CS \_ 4 \_ 0 und CS \_ 4 \_ 1 unterstützen diese Anweisung für UAV.

Diese Anweisung gilt für die folgenden Shader-Phasen:



| Scheitelpunkt | Hülle | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | X     | X       |



 

Da UAVs in allen Shader-Phasen für Direct3D 11,1 verfügbar sind, gilt diese Anweisung für alle Shader-Phasen für die Direct3D 11,1-Laufzeit, die ab Windows 8 verfügbar ist.



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

 

 





