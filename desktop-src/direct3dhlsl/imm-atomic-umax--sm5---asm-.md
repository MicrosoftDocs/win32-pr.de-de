---
title: imm_atomic_umax (sm5 – asm)
description: Sofortige atomare maximale Größe ohne Vorzeichen im Arbeitsspeicher. Gibt den Wert im Arbeitsspeicher vor dem max-Vorgang zurück.
ms.assetid: 6C9D2CA3-1502-41E1-8535-C94DF31201E1
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 399142e182cbf33a8adea3ac8236fdc81e4f4b100e562e65bbb39057b6e6e192
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986510"
---
# <a name="imm_atomic_umax-sm5---asm"></a>imm \_ atomic \_ umax (sm5 - asm)

Sofortige atomare maximale Größe ohne Vorzeichen im Arbeitsspeicher. Gibt den Wert im Arbeitsspeicher vor dem max-Vorgang zurück.



| imm \_ atomic \_ umax dst0 \[ .single component mask , \_ \_ \] dst1, dstAddress \[ .swizzle \] , src0 \[ .select \_ component\] |
|--------------------------------------------------------------------------------------------------------------|



 



| Element                                                                                                           | Beschreibung                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span id="dst0"></span><span id="DST0"></span>*dst0*<br/>                                                | \[in \] Enthält den Wert aus *dst1* vor dieser Anweisung.<br/>                                                         |
| <span id="dst1"></span><span id="DST1"></span>*dst1*<br/>                                                | \[in \] Einer ungeordneten Zugriffsansicht (UAV) (u \# ). Im Compute-Shader kann es sich auch um freigegebenen Threadgruppenspeicher \# (g) handelt. <br/> |
| <span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*<br/> | \[in \] Die Speicheradresse.<br/>                                                                                             |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                                | \[in \] Der Wert, der mit *dst1* bei *dstAddress* verglichen werden soll.<br/>                                                                 |



 

## <a name="remarks"></a>Hinweise

Diese Anweisung führt einen 32-Bit-Maximalwert ohne Vorzeichen einer einzelnen Komponente des Operanden *src0* mit *dst1* bei 32 Bit pro Komponentenadresse *dstAddress* aus.

Wenn *dst1* ein u \# ist, wurde er möglicherweise als roh, typisiert oder strukturiert deklariert. Wenn sie typisiert ist, muss sie als UINT/SINT deklariert werden, wobei das gebundene Ressourcenformat R32 \_ \_ UINT/SINT ist.

Wenn *dst1* g \# ist, muss es als roh oder strukturiert deklariert werden.

Der Wert im *dst1-Arbeitsspeicher* vor max wird an *dst0* zurückgegeben.

Die Anzahl der Von der Adresse entnommenen Komponenten wird durch die Dimensionalität von *dst1* bestimmt.

Der gesamte Vorgang wird atomar ausgeführt.

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

 

 





