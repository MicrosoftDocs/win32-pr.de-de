---
title: dcl_input_control_point_count (SM5-ASM)
description: Deklarieren Sie die Eingabe Steuerungspunkt-Anzahl von Hull-Shader im Abschnitt "Hull Shader Declaration".
ms.assetid: 2E524BF0-3DD0-446A-8437-0CF17B348D83
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f0a674a05bfd66b4c1d94da73958dc68f00fe21
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104389602"
---
# <a name="dcl_input_control_point_count-sm5---asm"></a>Anzahl der DCL \_ \_ -Eingabe Kontroll \_ Punkte \_ (SM5-ASM)

Deklarieren Sie die Eingabe Steuerungspunkt-Anzahl von Hull-Shader im Abschnitt "Hull Shader Declaration".



| DCL- \_ Eingabe \_ Steuerungspunkt- \_ \_ Anzahl {1.. 32} |
|-------------------------------------------|



 



| Element                                                   | BESCHREIBUNG                                      |
|--------------------------------------------------------|--------------------------------------------------|
| <span id="N"></span><span id="n"></span>*Nr*<br/> | \[in \] der Eingabe Steuerungspunkt-Anzahl.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Mindestens ein Eingabe Steuerungspunkt ist erforderlich. Sie kann leer sein, wenn Sie nicht benötigt wird.

Diese Anweisung gilt für die folgenden Shader-Phasen:



| Scheitelpunkt | Hülle | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        | X    |        |          |       |         |



 

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

 

 





