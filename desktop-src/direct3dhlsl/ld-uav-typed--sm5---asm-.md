---
title: ld_uav_typed (sm5 – asm)
description: Zufälliger Zugriff auf ein Element aus einer typisierten ungeordneten Zugriffsansicht (UAV).
ms.assetid: E5E03311-3596-4497-9271-FE6445DBFC62
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc9685341f4a3a2e6b22bbbcc4b36f6ecccc153f17c67f38c390e6beeef94358
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982070"
---
# <a name="ld_uav_typed-sm5---asm"></a>ld \_ uav \_ typed (sm5 - asm)

Zufälliger Zugriff auf ein Element aus einer typisierten ungeordneten Zugriffsansicht (UAV).



| ld \_ uav \_ typed dst0 \[ .mask \] , srcAddress \[ .swizzle \] , srcUAV \[ .swizzle\] |
|--------------------------------------------------------------------------|



 



| Element                                                                                                           | Beschreibung                                                    |
|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dst0"></span><span id="DST0"></span>*dst0*<br/>                                                | \[in \] Die Adresse der Ergebnisse des Vorgangs.<br/> |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/> | \[in \] Gibt die Adresse an, aus der gelesen werden soll.<br/>          |
| <span id="srcUAV"></span><span id="srcuav"></span><span id="SRCUAV"></span>*srcUAV*<br/>                 | \[in \] Die Quelle, aus der gelesen werden soll. <br/>                    |



 

## <a name="remarks"></a>Hinweise

Diese Anweisung führt ein aus *srcUAV* gelesenes 4-Komponenten-Element an der Ganzzahladresse ohne Vorzeichen in *srcAddress* aus, das basierend auf dem Format in 32 Bit pro Komponente konvertiert und dann im Shader in *dst0* geschrieben wird.

*srcUAV* ist ein UAV (u \# ), der als typisiert deklariert ist. Der Typ der gebundenen Ressource muss jedoch R32 \_ UINT/SINT/FLOAT sein.

Die Anzahl der 32-Bit-Komponenten für ganzzahlige Zahlen ohne Vorzeichen aus der Adresse wird durch die Dimensionalität der Ressource bestimmt, die unter *srcUAV* deklariert ist. Die Adressierung entspricht der [ld-Anweisung.](ld--sm4---asm-.md)

Die Adressierung außerhalb der Grenzen  entspricht der ld-Anweisung.

Das Verhalten dieser Anweisung ist  identisch mit der ld-Anweisung, wenn sie als **ld dst0 \[ .mask \] , srcAddress \[ .swizzle, \] srcUAV \[ .swizzle \]** aufgerufen wird.

Es ist ungültig und nicht definiert, diese Anweisung für eine UAV zu verwenden, die nicht als typisiert deklariert ist. Dies bei einem strukturierten oder typlosen UAV ist ungültig.

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



 

cs \_ 4 \_ 0 und cs \_ 4 \_ 1 unterstützen diese Anweisung für UAV, SRV und TGSM.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shadermodell 5-Assembly (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





