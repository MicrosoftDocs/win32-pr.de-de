---
title: imm_atomic_or (sm5 – asm)
description: Sofortiges atomares bitweises OR im Arbeitsspeicher. Gibt den Wert im Arbeitsspeicher vor dem OR zurück.
ms.assetid: 0ACE977D-5D0E-4E9C-A49F-B81D789B0D43
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e4188e8b79cdf4d782ebc926645a4279d08c9682fd0ae254c2ce37c5fbcf46a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982100"
---
# <a name="imm_atomic_or-sm5---asm"></a>imm \_ atomic \_ oder (sm5 - asm)

Sofortiges atomares bitweises OR im Arbeitsspeicher. Gibt den Wert im Arbeitsspeicher vor dem OR zurück.



| imm \_ atomic \_ oder dst0 \[ .single component mask , \_ \_ \] dst1, dstAddress \[ .swizzle \] , src0 \[ .select \_ component\] |
|------------------------------------------------------------------------------------------------------------|



 



| Element                                                                                                           | BESCHREIBUNG                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span id="dst0"></span><span id="DST0"></span>*dst0*<br/>                                                | \[in \] Enthält den Wert von *dst1* vor dem OR.<br/>                                                                   |
| <span id="dst1"></span><span id="DST1"></span>*dst1*<br/>                                                | \[in \] Einer ungeordneten Zugriffsansicht (UAV) (u \# ). Im Compute-Shader kann es sich auch um freigegebenen Threadgruppenspeicher \# (g) handelt. <br/> |
| <span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*<br/> | \[in \] Die Speicheradresse.<br/>                                                                                             |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                                | Der Wert für OR mit *dst1*.<br/>                                                                                           |



 

## <a name="remarks"></a>Hinweise

Diese Anweisung führt eine einzelne 32-Bit-Bit-BIT-OR-Komponente des Operanden *src0* mit *dst1* bei 32-Bit pro Komponentenadresse *dstAddress* aus.

Wenn *dst1* ein u \# ist, wurde er möglicherweise als roh, typisiert oder strukturiert deklariert. Wenn sie typisiert ist, muss sie als UINT/SINT deklariert werden, wobei das gebundene Ressourcenformat R32 \_ \_ UINT/SINT ist.

Wenn *dst1* g \# ist, muss es als roh oder strukturiert deklariert werden.

Der Wert im *dst1-Speicher,* bevor or an *dst0* zurückgegeben wird.

Der gesamte Vorgang wird atomar ausgeführt.

Die Anzahl der Komponenten, die von der Adresse stammen, wird durch die Dimensionalität der Ressource bestimmt, die bei *dst1* deklariert wurde.

Wenn der Shaderaufruf inaktiv ist, z. B. wenn das Pixel zuvor bei der Ausführung verworfen wurde, oder ein Pixel-/Beispielaufruf nur als Hilfselement für ein echtes Pixel/Sample für Ableitungen vorhanden ist, ändert diese Anweisung den *dst1-Speicher* überhaupt nicht, und der zurückgegebene Wert ist nicht definiert.

Die Adressierung außerhalb der Grenzen für u bewirkt, dass nichts in \# den Arbeitsspeicher geschrieben wird, außer wenn das u strukturiert ist und der \# Byteoffset in die Struktur (zweite Komponente der Adresse) den Zugriff außerhalb der Grenzen verursacht, dann wird der gesamte Inhalt des UAV nicht definiert.

Die Adressierung außerhalb der Grenzen für u \# oder g \# bewirkt, dass ein nicht definiertes Ergebnis an den Shader in *dst0* zurückgegeben wird.

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

 

 





