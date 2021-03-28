---
title: atomic_or (SM5-ASM)
description: Atomarischer bitweiser or-Operator.
ms.assetid: 5AFB96AA-267B-454E-9526-BA61A876ED42
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 245f1b02edd74712471206b095f0c8a9040962b6
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104516502"
---
# <a name="atomic_or-sm5---asm"></a>Atomic \_ oder (SM5-ASM)

Atomarischer bitweiser or-Operator.



| Atomic \_ oder DST, dstaddress \[ . Swizzle \] , src0 \[ . Select- \_ Komponente\] |
|--------------------------------------------------------------------|



 



| Element                                                                                                           | BESCHREIBUNG                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="dst"></span><span id="DST"></span>*DST*<br/>                                                   | \[in \] den Komponenten zu oder mit *src0*. Dieser Wert muss eine ungeordnete Zugriffs Ansicht (UAV) sein \# . Im COMPUTE-Shader kann es sich auch um einen Thread Gruppen-Shared Memory (g \# ) handeln. <br/> |
| <span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstaddress*<br/> | \[in \] der Speicheradresse.<br/>                                                                                                                                                |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                                | \[in \] den Komponenten zu oder mit *DST*.<br/>                                                                                                                                   |



 

## <a name="remarks"></a>Bemerkungen

Diese Anweisung führt eine einzelne Komponente 32-Bit bitweise OR of Operand *src0* to *DST* at 32-Bit per Component Address *dstaddress* aus, die atomarisch ausgeführt wird.

Die Anzahl der Komponenten, die von der Adresse entnommen werden, hängt von der Dimensionalität der *DST* u \# oder g ab \# .

Wenn *DST* eine u ist \# , kann Sie als RAW, typisiert oder strukturiert deklariert werden. Wenn Sie eingegeben wird, muss Sie als uint/Sint mit dem gebundenen Ressourcen Format "R32 \_ uint/ \_ Sint" deklariert werden.

Wenn *DST* g ist \# , muss es als RAW oder strukturiert deklariert werden.

An den Shader wird nichts zurückgegeben.

Wenn der Shader-Aufruf inaktiv ist, z. b. wenn das Pixel bereits in seiner Ausführung verworfen wurde, oder wenn ein Pixel-/Beispielaufruf nur vorhanden ist, um als Hilfsobjekt für ein reales Pixel/Beispiel für Ableitungen zu dienen, ändert diese Anweisung den *DST* -Arbeitsspeicher überhaupt nicht (im Hintergrund).

Die Out-of-Bounds-Adressierung in u \# bewirkt, dass nichts in den Arbeitsspeicher geschrieben wird, es sei denn, die u \# ist strukturiert, und der Byte Offset in der Struktur (zweite Komponente der Adresse) verursacht den Zugriff außerhalb der Grenzen, und der gesamte Inhalt der UAV wird nicht definiert.

Die Begrenzung auf g \# (die Begrenzungen dieses bestimmten g im \# Gegensatz zum gesamten Shared Memory) bewirkt, dass der gesamte Inhalt des gesamten freigegebenen Speichers undefiniert wird.

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

 

 





