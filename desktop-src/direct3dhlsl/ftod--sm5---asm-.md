---
title: "\"f\" (SM5-ASM)"
description: Komponenten Weise Konvertierung von Gleit Komma Daten mit einfacher Genauigkeit in Gleit Komma Daten mit doppelter Genauigkeit.
ms.assetid: 95297556-41ED-4ED0-8F9A-16B7A440AF25
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6790735745805426d32aefcc5d5d771ade644e43
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104313704"
---
# <a name="ftod-sm5---asm"></a>"f" (SM5-ASM)

Komponenten Weise Konvertierung von Gleit Komma Daten mit einfacher Genauigkeit in Gleit Komma Daten mit doppelter Genauigkeit.



| f: dest \[ . mask \] , \[ - \] src \[ . Swizzle \] , |
|-------------------------------------------|



 



| Element                                                            | BESCHREIBUNG                                          |
|-----------------------------------------------------------------|------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[in \] der Adresse der konvertierten Daten.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] den zu konvertierenden Daten.<br/>          |



 

## <a name="remarks"></a>Bemerkungen

Jede Komponente der Quelle wird von der Darstellung mit einfacher Genauigkeit in die Darstellung mit doppelter Genauigkeit konvertiert.

Die gültigen *dest* -Masken sind. XY,. zw und. xyzw. . XY empfängt das Ergebnis der ersten Konvertierung, und. zw empfängt das Ergebnis der zweiten Konvertierung.

*dest* ist eine doppelte vec2 über (x 32lsb, y 32msb) und (z 32lsb, w 32msb).

*src* ist ein Gleit Komma vec2 über x und y (ZW wird ignoriert) (postswizzle).

Bei<->Double-Konvertierungen können Implementierungen entweder float32 denorms beachten oder Sie leeren.

Diese Anweisung gilt für die folgenden Shader-Phasen:



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

 

 





