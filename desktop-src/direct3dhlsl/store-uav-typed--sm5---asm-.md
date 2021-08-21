---
title: store_uav_typed (sm5 – asm)
description: Schreiben eines Elements mit wahlfreiem Zugriff in eine typisierte ungeordnete Zugriffsansicht (UAV).
ms.assetid: AD8E035B-DACD-4241-A05B-7D6DC8E3222C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc190662ebab4629c92bba8fafbe75fe23704f8543c7eb9ceba53b9ab02b1029
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118508240"
---
# <a name="store_uav_typed-sm5---asm"></a>store \_ uav \_ typed (sm5 - asm)

Schreiben eines Elements mit wahlfreiem Zugriff in eine typisierte ungeordnete Zugriffsansicht (UAV).



| store \_ uav \_ typed dstUAV.xyzw, dstAddress \[ .swizzle \] , src0 \[ .swizzle\] |
|-------------------------------------------------------------------------|



 



| Element                                                                                                           | Beschreibung                                             |
|----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*<br/>                 | \[in \] Enthält das Ergebnis des Vorgangs.<br/> |
| <span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstAddress*<br/> | \[in \] Die Adresse, an der geschrieben werden soll.<br/>        |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                                | \[in \] Die zu schreibende Komponenten.<br/>              |



 

## <a name="remarks"></a>Hinweise

Diese Anweisung führt ein \* 32-Bit-Element mit vier Komponenten aus, das von *src0* in *dstUAV* an der Adresse in *dstAddress* geschrieben wurde. *dstUAV* ist ein typisierter UAV (u \# ).

Das Format des UAV bestimmt die Formatkonvertierung.

Die Anzahl der 32-Bit-Komponenten ganzzahliger Zahlen ohne Vorzeichen, die von der Adresse übernommen werden, wird durch die Dimensionalität der Ressource bestimmt, die unter *dstUAV* deklariert ist. Diese Adresse befindet sich in -Elementen.

Die Adressierung außerhalb der Grenzen bedeutet, dass nichts in den Arbeitsspeicher geschrieben wird.

*dstUAV* verfügt immer über eine .xyzw-Schreibmaske. Alle Komponenten müssen geschrieben werden.

Es ist ungültig und nicht definiert, diese Anweisung für eine UAV zu verwenden, die nicht als typisiert deklariert ist. Das heißt, eine strukturierte oder typlose UAV ist ungültig.

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

 

 





