---
title: store_structured (sm5 – asm)
description: Schreiben von 1-4 32-Bit-Komponenten mit wahlfreiem Zugriff in eine strukturierte, ungeordnete Pufferzugriffsansicht (UAV).
ms.assetid: 8080B2CA-5BDA-4F01-8B2B-B85BDD58C5AF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a220fca330ba4198669245f0336b363c448067613e3f21fce44c9af9325bd9e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118285755"
---
# <a name="store_structured-sm5---asm"></a>store \_ structured (sm5 – asm)

Schreiben von 1-4 32-Bit-Komponenten mit wahlfreiem Zugriff in eine strukturierte, ungeordnete Pufferzugriffsansicht (UAV).



| store \_ structured dst0 \[ .write mask , \_ \] dstAddress \[ .select component , \_ \] dstByteOffset \[ .select component , \_ \] src0 \[ .swizzle\] |
|---------------------------------------------------------------------------------------------------------------------------------|



 



| Element                                                                                                                       | Beschreibung                                                    |
|----------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dst0"></span><span id="DST0"></span>*dst0*<br/>                                                            | \[in \] Die Adresse der Ergebnisse des Vorgangs.<br/> |
| <span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*<br/>             | \[in \] Die Adresse, an der geschrieben werden soll.<br/>               |
| <span id="dstByteOffset"></span><span id="dstbyteoffset"></span><span id="DSTBYTEOFFSET"></span>*dstByteOffset*<br/> | \[in \] Der Index der zu schreibende Struktur.<br/>         |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                                            | \[in \] Die zu schreibende Komponenten.<br/>                     |



 

## <a name="remarks"></a>Hinweise

Diese Anweisung führt \* 32-Bit-Komponenten mit 1 bis 4 Komponenten aus, die von *src0* in *dst0* an der Adresse in *dstAddress* und *dstByteOffset* geschrieben wurden. Keine Formatkonvertierung.

*dst0* muss ein UAV (u \# ) sein. Im Compute-Shader kann es sich auch um freigegebenen Speicher der Threadgruppe \# (g) befinden.

*dstAddress* gibt den Index der zu schreibenden Struktur an.

Die Position der geschriebenen Daten entspricht dem folgenden Pseudocode, der den Offset, die Adresse, den Zeiger auf den Pufferinhalt, den Schritt der Quelle und die linear gespeicherten Daten anzeigt.

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

Dieser Pseudocode zeigt, wie der Vorgang funktioniert, aber die tatsächlichen Daten müssen nicht linear gespeichert werden. Wenn die Daten nicht linear gespeichert werden, muss der tatsächliche Vorgang der Anweisung mit dem Verhalten des obigen Vorgangs übereinstimmen.

*dst0* kann nur über eine Schreibmaske verfügen, die eine der folgenden Ist: .x, .xy, .xyz, .xyzw. Die Schreibmaske bestimmt die Anzahl der 32-Bit-Komponenten, die ohne Lücken geschrieben werden sollen.

Die Adressierung außerhalb der Grenzen für u \# casued by *dstAddress* bedeutet, dass nichts in den Arbeitsspeicher außerhalb der Grenzen geschrieben wird.

Wenn *dstByteOffset*, einschließlich *dstWriteMask,* den Zugriff außerhalb der Grenzen auf Sie \# verursacht, wird der gesamte Inhalt des UAV nicht definiert.

Die Adressierung außerhalb der Grenzen von g \# (die Begrenzungen dieses bestimmten g \# im Gegensatz zum gesamten freigegebenen Arbeitsspeicher) für eine bestimmte 32-Bit-Komponente bewirkt, dass der gesamte Inhalt des gesamten freigegebenen Speichers nicht definiert wird.

*dstByteOffset* ist ein separates Argument von *dstAddress,* da es sich häufig um ein Literal handelt. Diese Parametertrennung wurde für Atomaren im strukturierten Speicher nicht durchgeführt.

cs \_ 4 \_ 0 und cs \_ 4 \_ 1 unterstützen diese Anweisung für UAV und TGSM.

Diese Anweisung gilt für die folgenden Shaderstufen:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | X     | X       |



 

Da UAVs in allen Shaderstufen für Direct3D 11.1 verfügbar sind, gilt diese Anweisung für alle Shaderstufen für die Direct3D 11.1-Runtime, die ab Windows 8 verfügbar ist.



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Shader-Mindestmodell

Diese Anweisung wird in den folgenden Shadermodellen unterstützt:



| Shadermodell                                              | Unterstützt |
|-----------------------------------------------------------|-----------|
| [Shadermodell 5](d3d11-graphics-reference-sm5.md)        | ja       |
| [Shadermodell 4.1](dx-graphics-hlsl-sm4.md)              | nein        |
| [Shadermodell 4](dx-graphics-hlsl-sm4.md)                | nein        |
| [Shadermodell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | nein        |
| [Shadermodell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | nein        |
| [Shadermodell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | nein        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shadermodell 5-Assembly (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





