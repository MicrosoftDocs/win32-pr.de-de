---
title: store_uav_typed (SM5-ASM)
description: Zufälliger Zugriff auf das Schreiben eines Elements in eine typisierte, unsortierter Zugriffs Ansicht (UAV).
ms.assetid: AD8E035B-DACD-4241-A05B-7D6DC8E3222C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6243e6fbb2092bac699dbbce04cb3c3478880866
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104038322"
---
# <a name="store_uav_typed-sm5---asm"></a>Store- \_ UAV \_ -typisiert (SM5-ASM)

Zufälliger Zugriff auf das Schreiben eines Elements in eine typisierte, unsortierter Zugriffs Ansicht (UAV).



| Store \_ UAV \_ typisiertes dstuav. xyzw, dstaddress \[ . Swizzle \] , src0 \[ . Swizzle\] |
|-------------------------------------------------------------------------|



 



| Element                                                                                                           | BESCHREIBUNG                                             |
|----------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstuav*<br/>                 | \[in \] enthält das Ergebnis des Vorgangs.<br/> |
| <span id="dstAddress"></span><span id="dstaddress"></span><span id="DSTADDRESS"></span>*dstaddress*<br/> | \[in \] der Adresse, an der geschrieben werden soll.<br/>        |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                                | \[in \] den zu schreibende Komponenten.<br/>              |



 

## <a name="remarks"></a>Bemerkungen

Diese Anweisung führt ein 4 \* -Bit-32-Bit-Element aus, das von *src0* auf *dstuav* an der Adresse in *dstaddress* geschrieben wurde. *dstuav* ist ein typisiertes UAV (u \# ).

Das Format der UAV bestimmt die Formatkonvertierung.

Die Anzahl der Komponenten, die von der Adresse aus der 32-Bit-Ganzzahl ohne Vorzeichen entnommen werden, hängt von der Dimensionalität der in *dstuav* deklarierten Ressource ab. Diese Adresse befindet sich in-Elementen.

Die Adressierung außerhalb der Grenzen bedeutet, dass nichts in den Speicher geschrieben wird.

*dstuav* hat immer eine. xyzw-Schreib Maske. Alle Komponenten müssen geschrieben werden.

Es ist ungültig und nicht definiert, diese Anweisung für eine UAV zu verwenden, die nicht als typisiert deklariert ist. Das heißt, dass dies auf einer strukturierten oder typlosen UAV durchgeführt werden kann.

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

 

 





