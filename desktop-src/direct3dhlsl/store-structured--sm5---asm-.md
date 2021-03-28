---
title: store_structured (SM5-ASM)
description: Zufälliger Zugriff auf Schreibvorgänge von 1-4 32-Bit-Komponenten in eine strukturierte Puffer-UAV (unsortierter Zugriffs Ansicht).
ms.assetid: 8080B2CA-5BDA-4F01-8B2B-B85BDD58C5AF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5890d30fac57923365f0bdea89fcce55f7922c7
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104038326"
---
# <a name="store_structured-sm5---asm"></a>\_strukturierte Geschäfte (SM5-ASM)

Zufälliger Zugriff auf Schreibvorgänge von 1-4 32-Bit-Komponenten in eine strukturierte Puffer-UAV (unsortierter Zugriffs Ansicht).



| Store \_ strukturiert dst0 \[ . Write \_ mask \] , dstaddress \[ . Select \_ Component \] , dstbyteoffset \[ . Select \_ Component \] , src0 \[ . Swizzle\] |
|---------------------------------------------------------------------------------------------------------------------------------|



 



| Element                                                                                                                       | BESCHREIBUNG                                                    |
|----------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dst0"></span><span id="DST0"></span>*dst0*<br/>                                                            | \[in \] der Adresse der Ergebnisse des Vorgangs.<br/> |
| <span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstaddress*<br/>             | \[in \] der Adresse, an der geschrieben werden soll.<br/>               |
| <span id="dstByteOffset"></span><span id="dstbyteoffset"></span><span id="DSTBYTEOFFSET"></span>*dstbyteoffset*<br/> | \[im \] Index der zu schreibenden-Struktur.<br/>         |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                                            | \[in \] den zu schreibende Komponenten.<br/>                     |



 

## <a name="remarks"></a>Bemerkungen

Diese Anweisung führt 1-4 \* -Komponente-32-Bit-Komponenten aus, die von *src0* auf *dst0* an der Adresse in *dstaddress* und *dstbyteoffset* geschrieben wurden. Keine Formatkonvertierung.

*dst0* muss eine UAV (u \# ) sein. Im COMPUTE-Shader kann es sich auch um einen Thread Gruppen-Shared Memory (g \# ) handeln.

*dstaddress* gibt den Index der zu schreibenden Struktur an.

Der Speicherort der geschriebenen Daten entspricht dem folgenden Pseudo Code, der den Offset, die Adresse, den Zeiger auf den Pufferinhalt, den Schritt der Quelle und die Daten, die linear gespeichert werden, anzeigt.

``` syntax
                    BYTE *BufferContents;             // from dst0
                    UINT BufferStride;                // from dst0
                    UINT dstAddress, dstByteOffset;   // source registers
                    BYTE *WriteLocation;              // value to calculate

                    // calculate writing location
                     WriteLocation = BufferContents 
                                + BufferStride * dstAddress 
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
                             WriteComponents * sizeof(INT32));
```

Dieser Pseudo Code zeigt, wie der Vorgang funktioniert, aber die tatsächlichen Daten müssen nicht linear gespeichert werden. Wenn die Daten nicht linear gespeichert werden, muss die tatsächliche Operation der Anweisung mit dem Verhalten des obigen Vorgangs identisch sein.

*dst0* kann nur eine Schreib Maske aufweisen, die eine der folgenden ist:. x,. XY,. XYZ,. xyzw. Die Schreib Maske bestimmt die Anzahl der 32-Bit-Komponenten, die ohne Lücken geschrieben werden sollen.

Wenn die Adressierung von " \# *dstaddress* " nicht mehr begrenzt ist, bedeutet dies, dass nichts in den Speicher außerhalb des gültigen Bereichs geschrieben wird.

Wenn *dstbyteoffset*, einschließlich *dstschreitemask*, den Zugriff für den Zugriff auf Sie verursacht, wird \# der gesamte Inhalt der UAV nicht definiert.

Die Adressierung auf g \# (die Begrenzungen dieses bestimmten g \# , im Gegensatz zum gesamten freigegebenen Speicher) für eine bestimmte 32-Bit-Komponente bewirkt, dass der gesamte Inhalt des gesamten freigegebenen Speichers undefiniert wird.

*dstbyteoffset* ist ein separates Argument von *dstaddress* , da es sich in der Regel um ein Literalelement handelt. Diese Parameter Trennung wurde nicht für Atomics in strukturiertem Arbeitsspeicher durchgeführt.

CS \_ 4 \_ 0 und CS \_ 4 \_ 1 unterstützen diese Anweisung für UAV und TGSM.

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

 

 





