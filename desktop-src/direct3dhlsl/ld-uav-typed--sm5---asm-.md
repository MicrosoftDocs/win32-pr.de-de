---
title: ld_uav_typed (SM5-ASM)
description: Zufälliger Zugriffs Lesevorgang eines Elements aus einer typisierten nicht geordneten Zugriffs Ansicht (UAV).
ms.assetid: E5E03311-3596-4497-9271-FE6445DBFC62
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61b22392c802378c094b443c8ff2f2282909bd1f
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104313680"
---
# <a name="ld_uav_typed-sm5---asm"></a>LD \_ UAV \_ -typisiert (SM5-ASM)

Zufälliger Zugriffs Lesevorgang eines Elements aus einer typisierten nicht geordneten Zugriffs Ansicht (UAV).



| LD \_ UAV \_ typisiert dst0 \[ . mask \] , srcaddress \[ . Swizzle \] , srcuav \[ . Swizzle\] |
|--------------------------------------------------------------------------|



 



| Element                                                                                                           | BESCHREIBUNG                                                    |
|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dst0"></span><span id="DST0"></span>*dst0*<br/>                                                | \[in \] der Adresse der Ergebnisse des Vorgangs.<br/> |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcaddress*<br/> | \[in \] gibt die Adresse an, aus der gelesen werden soll.<br/>          |
| <span id="srcUAV"></span><span id="srcuav"></span><span id="SRCUAV"></span>*srcuav*<br/>                 | \[in \] der Quelle, aus der gelesen werden soll. <br/>                    |



 

## <a name="remarks"></a>Bemerkungen

Diese Anweisung führt ein aus *srcuav* gelesene 4-Component-Element an der ganzzahligen Adresse ohne Vorzeichen in *srcaddress* aus, die auf Grundlage des Formats in 32-Bit pro Komponente konvertiert und dann im Shader in *dst0* geschrieben wird.

*srcuav* ist ein UAV (u \# ), das als typisiert deklariert ist. Der Typ der gebundenen Ressource muss jedoch "R32 \_ uint/Sint/float" lauten.

Die Anzahl der Komponenten, die von der Adresse aus der 32-Bit-Ganzzahl ohne Vorzeichen entnommen werden, hängt von der Dimensionalität der in *srcuav* deklarierten Ressource ab. Adressierung ist mit der [LD](ld--sm4---asm-.md) -Anweisung identisch.

Die Adressierung außerhalb der Begrenzungen ist mit der **LD** -Anweisung identisch.

Das Verhalten dieser Anweisung ist mit der **LD** -Anweisung identisch, wenn Sie als **LD dst0 \[ . mask \] , srcaddress \[ . Swizzle \] , srcuav \[ . Swizzle \]** aufgerufen wird.

Es ist ungültig und nicht definiert, diese Anweisung für eine UAV zu verwenden, die nicht als typisiert deklariert ist. Eine strukturierte oder typlose UAV ist ungültig.

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



 

CS \_ 4 \_ 0 und CS \_ 4 \_ 1 unterstützen diese Anweisung für UAV, SRV und TGSM.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shader Model 5-Assembly (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





