---
title: atomic_xor (sm5 – asm)
description: Atomarer bitweiser XOR in den Arbeitsspeicher.
ms.assetid: DC284647-FBB4-419B-A555-8076C5716F0A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 785b8483de724e17a08d2d79101ba8f5dc10a91b38583ad62944edad8c26772b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118794831"
---
# <a name="atomic_xor-sm5---asm"></a>atomic \_ xor (sm5 – asm)

Atomarer bitweiser XOR in den Arbeitsspeicher.



| atomic \_ xor dst, dstAddress \[ .swizzle \] , src0 \[ .select \_ component\] |
|---------------------------------------------------------------------|



 



| Element                                                                                                           | BESCHREIBUNG                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="dst"></span><span id="DST"></span>*Dst*<br/>                                                   | \[in \] Die Komponenten zu XOR mit *src0*. Bei diesem Wert muss es sich um eine ungeordnete Zugriffsansicht (UAV) \# (u) handelt. Im Compute-Shader kann es sich auch um freigegebenen Speicher der Threadgruppe \# (g) befinden. <br/> |
| <span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*<br/> | \[in \] Die Speicheradresse.<br/>                                                                                                                                                 |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                                | \[in \] Die Komponenten zu XOR mit *dst*.<br/>                                                                                                                                   |



 

## <a name="remarks"></a>Hinweise

Diese Anweisung führt eine einzelne 32-Bit-Bit-XOR-Komponente des Operanden *src0* in *dst* bei 32-Bit pro Komponentenadresse *dstAddress* aus, die atomar ausgeführt wird.

Die Anzahl der Von der Adresse entnommenen Komponenten wird durch die Dimensionalität von *dst* u \# oder g \# bestimmt.

Wenn *dst* ein u \# ist, kann er als roh, typisiert oder strukturiert deklariert werden. Wenn sie typisiert ist, muss sie als UINT/SINT deklariert werden, wobei das gebundene Ressourcenformat R32 \_ \_ UINT/SINT ist.

Wenn *dst* g \# ist, muss er als roh oder strukturiert deklariert werden.

An den Shader wird nichts zurückgegeben.

Wenn der Shaderaufruf inaktiv ist, z. B. wenn das Pixel zuvor bei seiner Ausführung verworfen wurde oder ein Pixel-/Beispielaufruf nur als Hilfselement für ein echtes Pixel/Sample für Ableitungen vorhanden ist, ändert diese Anweisung den *dst-Speicher* überhaupt nicht (im Hintergrund).

Die Adressierung außerhalb der Grenzen für u bewirkt, dass nichts in \# den Arbeitsspeicher geschrieben wird, außer wenn das u strukturiert ist und der \# Byteoffset in die Struktur (zweite Komponente der Adresse) den Zugriff außerhalb der Grenzen verursacht, dann wird der gesamte Inhalt des UAV nicht definiert.

Die Adressierung außerhalb der Grenzen von g \# (die Begrenzungen dieses bestimmten g im \# Gegensatz zum gesamten freigegebenen Arbeitsspeicher) bewirkt, dass der gesamte Inhalt des gesamten freigegebenen Speichers nicht definiert wird.

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

 

 





