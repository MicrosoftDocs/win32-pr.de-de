---
title: imm_atomic_cmp_exch (sm5 – asm)
description: Sofortiger Vergleich und Austausch mit dem Arbeitsspeicher.
ms.assetid: 317A69E1-0E0A-45C8-8E0A-B88659ADBECC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba1014d338687a0798675ed407c0db844c80491833b45628020249bf94b6061b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119562406"
---
# <a name="imm_atomic_cmp_exch-sm5---asm"></a>imm \_ atomic \_ cmp \_ exch (sm5 – asm)

Sofortiger Vergleich und Austausch mit dem Arbeitsspeicher.



| imm \_ atomic \_ cmp \_ exch dst0 \[ .single component mask , \_ \_ \] dst1, dstAddress \[ .swizzle \] , src0 \[ .select component , \_ \] src1 \[ .select \_ component\] |
|-----------------------------------------------------------------------------------------------------------------------------------------------|



 



| Element                                                                                                           | Beschreibung                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span id="dst0"></span><span id="DST0"></span>*dst0*<br/>                                                | \[out \] Enthält *dst1* vor dem Schreibvorgang.<br/>                                                                              |
| <span id="dst1"></span><span id="DST1"></span>*dst1*<br/>                                                | \[in \] Einer ungeordneten Zugriffsansicht (UAV) (u \# ). Im Compute-Shader kann es sich auch um freigegebenen Threadgruppenspeicher \# (g) handelt. <br/> |
| <span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*<br/> | \[in \] Der Zielspeicher.<br/>                                                                                         |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                                | \[in \] Der Wert, der mit *dst1* verglichen werden soll.<br/>                                                                                 |
| <span id="scr1"></span><span id="SCR1"></span>*scr1*<br/>                                                | \[in \] Der Wert, der in den Zielspeicher geschrieben wird, wenn die verglichenen Werte identisch sind.<br/>                               |



 

Diese Anweisung führt einen 32-Bit-Wertvergleich der einzelnen Komponente des Operanden *src0* mit *dst1* bei 32-Bit pro Komponentenadresse *dstAddress* durch.

Wenn *dst1* ein u \# ist, wurde er möglicherweise als roh, typisiert oder strukturiert deklariert. Wenn sie typisiert ist, muss sie als UINT/SINT deklariert werden, wobei das gebundene Ressourcenformat R32 \_ \_ UINT/SINT ist.

Wenn *dst1* g \# ist, muss es als roh oder strukturiert deklariert werden.

Wenn die verglichenen Werte identisch sind, wird der 32-Bit-Einzelkomponentenwert in *src1* in den Zielspeicher geschrieben. Andernfalls wird der Zielspeicher nicht geändert.

Der ursprüngliche 32-Bit-Wert im Zielspeicher wird immer in *dst0* geschrieben.

Der gesamte Vorgang wird atomar ausgeführt.

Wenn der Shaderaufruf inaktiv ist, z. B. wenn das Pixel zuvor bei der Ausführung verworfen wurde, oder ein Pixel-/Beispielaufruf nur als Hilfselement für ein echtes Pixel/Sample für Ableitungen vorhanden ist, ändert diese Anweisung den *dst1-Speicher* überhaupt nicht, und der zurückgegebene Wert ist nicht definiert.

Die Adressierung außerhalb der Grenzen für u bewirkt, dass nichts in \# den Arbeitsspeicher geschrieben wird, außer wenn das u strukturiert ist und der \# Byteoffset in die Struktur (zweite Komponente der Adresse) den Zugriff außerhalb der Grenzen verursacht, dann wird der gesamte Inhalt des UAV nicht definiert.

Die Adressierung außerhalb der Grenzen für u \# oder g \# bewirkt, dass ein nicht definiertes Ergebnis an den Shader in *dst0* zurückgegeben wird.

Diese Anweisung gilt für die folgenden Shaderstufen:



| Scheitelpunkt | Rumpf | Domäne | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | X     | X       |



 

Da UAVs in allen Shaderstufen für Direct3D 11.1 verfügbar sind, gilt diese Anweisung für alle Shaderstufen für die Direct3D 11.1-Runtime, die ab Windows 8 verfügbar ist.



| Scheitelpunkt | Rumpf | Domäne | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Shader-Mindestmodell

Diese Anweisung wird in den folgenden Shadermodellen unterstützt:



| Shadermodell                                              | Unterstützt |
|-----------------------------------------------------------|-----------|
| [Shadermodell 5](d3d11-graphics-reference-sm5.md)        | Ja       |
| [Shadermodell 4.1](dx-graphics-hlsl-sm4.md)              | Nein        |
| [Shadermodell 4](dx-graphics-hlsl-sm4.md)                | Nein        |
| [Shadermodell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | Nein        |
| [Shadermodell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | Nein        |
| [Shadermodell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | Nein        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shadermodell 5-Assembly (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





