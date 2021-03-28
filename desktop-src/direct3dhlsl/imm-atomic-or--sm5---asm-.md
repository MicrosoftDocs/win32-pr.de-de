---
title: imm_atomic_or (SM5-ASM)
description: Direkter atomarischer bitweiser or-Operator. Gibt den Wert im Arbeitsspeicher vor oder zurück.
ms.assetid: 0ACE977D-5D0E-4E9C-A49F-B81D789B0D43
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2bc3b9afd2ba9f4dc63a8fb5c5818c1121c7ec6
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104038352"
---
# <a name="imm_atomic_or-sm5---asm"></a>imm \_ Atomic \_ oder (SM5-ASM)

Direkter atomarischer bitweiser or-Operator. Gibt den Wert im Arbeitsspeicher vor oder zurück.



| imm \_ Atomic \_ oder dst0 \[ . Single \_ Component \_ mask \] , dST1, dstaddress \[ . Swizzle \] , src0 \[ . Select \_ Component\] |
|------------------------------------------------------------------------------------------------------------|



 



| Element                                                                                                           | BESCHREIBUNG                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span id="dst0"></span><span id="DST0"></span>*dst0*<br/>                                                | \[in \] enthält den Wert von *dST1* vor oder.<br/>                                                                   |
| <span id="dst1"></span><span id="DST1"></span>*dst1*<br/>                                                | \[in \] einer ungeordneten Zugriffs Ansicht (UAV) (u \# ). Im COMPUTE-Shader kann dies auch Thread Gruppe Shared Memory (g \# ) sein. <br/> |
| <span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstaddress*<br/> | \[in \] der Speicheradresse.<br/>                                                                                             |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                                | Der Wert für oder mit *dST1*.<br/>                                                                                           |



 

## <a name="remarks"></a>Bemerkungen

Diese Anweisung führt eine einzelne Komponente 32-Bit bitweises OR of Operand *src0* with *dST1* at 32-Bit pro Component Address *dstaddress* aus.

Wenn *dST1* eine u ist \# , wurde Sie möglicherweise als RAW, typisiert oder strukturiert deklariert. Wenn Sie eingegeben wird, muss Sie als uint/Sint mit dem gebundenen Ressourcen Format "R32 \_ uint/ \_ Sint" deklariert werden.

Wenn *dST1* den Wert g \# hat, muss er als RAW oder strukturiert deklariert werden.

Der Wert im *dST1* -Arbeitsspeicher, bevor oder an *dst0* zurückgegeben wird.

Der gesamte Vorgang wird atomisch ausgeführt.

Die Anzahl der Komponenten, die von der Adresse entnommen werden, hängt von der Dimensionalität der Ressource ab, die unter *dST1* deklariert ist.

Wenn der Shader-Aufruf inaktiv ist, z. b. wenn das Pixel zuvor in seiner Ausführung verworfen wurde oder ein Pixel-/Beispielaufruf nur vorhanden ist, um als Hilfsobjekt/Stichprobe für Ableitungen zu dienen, ändert diese Anweisung den *dST1* -Arbeitsspeicher nicht, und der zurückgegebene Wert ist nicht definiert.

Die Out-of-Bounds-Adressierung in u \# bewirkt, dass nichts in den Arbeitsspeicher geschrieben wird, außer wenn die u \# strukturiert ist und der Byte Offset in die Struktur (zweite Komponente der Adresse) den Zugriff außerhalb der Grenzen verursacht, dann wird der gesamte Inhalt der UAV nicht definiert.

Die Adressierung für "u" \# oder "g" bewirkt, \# dass ein nicht definiertes Ergebnis an den Shader in *dst0* zurückgegeben wird.

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

 

 





