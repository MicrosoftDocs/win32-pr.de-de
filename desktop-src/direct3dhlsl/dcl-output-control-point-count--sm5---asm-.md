---
title: dcl_output_control_point_count (SM5-ASM)
description: Deklariert die Anzahl der Ausgabe Kontrollpunkte des Hull-Shader.
ms.assetid: 51E8117F-1802-413B-9820-04D5CEBE2DB6
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 147f8f7021252f07cdb6dd0f225555ff0f23d54b
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104038372"
---
# <a name="dcl_output_control_point_count-sm5---asm"></a>Anzahl der DCL \_ \_ -Ausgabe Kontroll \_ Punkte \_ (SM5-ASM)

Deklariert die Anzahl der Ausgabe Kontrollpunkte des Hull-Shader.



| DCL \_ - \_ Ausgabe \_ Kontrollpunkt- \_ Anzahl N |
|--------------------------------------|



 



| Element                                                   | BESCHREIBUNG                                                                                    |
|--------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="N"></span><span id="n"></span>*Nr*<br/> | \[in \] einem ganzzahligen Wert von 0 bis 32, der die Anzahl von Ausgabe Kontrollpunkten angibt.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Der Hull-Shader kann 0-Kontrollpunkte ausgeben, wenn Sie nicht benötigt werden.

Diese Anweisung gilt für die folgenden Shader-Phasen:



| Scheitelpunkt | Hülle                 | Domain | Geometrie | Pixel | Compute |
|--------|----------------------|--------|----------|-------|---------|
|        | Deklarations Abschnitt |        |          |       |         |



 

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

 

 





