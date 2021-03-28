---
title: atomic_umin (SM5-ASM)
description: Atomare unsignierte Ganzzahl ohne Vorzeichen.
ms.assetid: 08822267-1A7F-4976-9402-601DD4B86E59
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8089dbed0e23443291176c47cda1a691202b164f
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104976409"
---
# <a name="atomic_umin-sm5---asm"></a>atomarische \_ Umschlag (SM5-ASM)

Atomare unsignierte Ganzzahl ohne Vorzeichen.



| Atomic- \_ in-DST, dstaddress \[ . Swizzle \] , src0 \[ . Select- \_ Komponente\] |
|----------------------------------------------------------------------|



 



| Element                                                                                                           | BESCHREIBUNG                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="dst"></span><span id="DST"></span>*DST*<br/>                                                   | \[in \] den Komponenten, die mit *src0* verglichen werden sollen. Dieser Wert muss eine ungeordnete Zugriffs Ansicht (UAV) sein \# . Im COMPUTE-Shader kann es sich auch um einen Thread Gruppen-Shared Memory (g \# ) handeln. <br/> |
| <span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstaddress*<br/> | \[in \] der Speicheradresse.<br/>                                                                                                                                                   |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                                | \[in \] den Komponenten, die mit *DST* verglichen werden sollen.<br/>                                                                                                                                   |



 

## <a name="remarks"></a>Bemerkungen

Diese Anweisung führt eine einzelne Komponente mit einer Länge von 32 Bit ohne Vorzeichen des Operanden *src0* in *DST* um 32 Bit pro Komponenten Adresse *dstaddress* aus, die atomisch ausgeführt wird.

Die Anzahl der Komponenten, die von der Adresse entnommen werden, hängt von der Dimensionalität der *DST* u \# oder g ab \# .

Wenn *DST* eine u ist \# , kann Sie als RAW, typisiert oder strukturiert deklariert werden. Wenn Sie eingegeben wird, muss Sie als uint/Sint mit dem gebundenen Ressourcen Format "R32 \_ uint/ \_ Sint" deklariert werden.

Wenn *DST* g ist \# , muss es als RAW oder strukturiert deklariert werden.

An den Shader wird nichts zurückgegeben.

Wenn der Shader-Aufruf inaktiv ist, z. b. wenn das Pixel bereits in seiner Ausführung verworfen wurde, oder wenn ein Pixel-/Beispielaufruf nur vorhanden ist, um als Hilfsobjekt für ein reales Pixel/Beispiel für Ableitungen zu dienen, ändert diese Anweisung den *DST* -Arbeitsspeicher überhaupt nicht (im Hintergrund).

Die Out-of-Bounds-Adressierung in u \# bewirkt, dass nichts in den Arbeitsspeicher geschrieben wird, außer wenn die u \# strukturiert ist und der Byte Offset in die Struktur (zweite Komponente der Adresse) den Zugriff außerhalb der Grenzen verursacht, dann wird der gesamte Inhalt der UAV nicht definiert.

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

 

 





