---
title: Ddx
description: Gibt die partielle Ableitung des angegebenen Werts in Bezug auf die x-Koordinate des Bildschirmbereichs zurück.
ms.assetid: a21c2d2a-7c62-4dc6-8521-273690be1104
keywords:
- ddx HLSL
topic_type:
- apiref
api_name:
- ddx
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a60f2376af13e291ff0c59966bd50261cf2fd29ceb10d8ea26f621e257956ce0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119043818"
---
# <a name="ddx"></a>Ddx

Gibt die partielle Ableitung des angegebenen Werts in Bezug auf die x-Koordinate des Bildschirmbereichs zurück.



| *ret* ddx(*x*) |
|----------------|



 

Diese Funktion berechnet die partielle Ableitung in Bezug auf die Bildschirmraum-X-Koordinate. Um die partielle Ableitung in Bezug auf die Bildschirmraum-y-Koordinate zu berechnen, verwenden Sie die [**ddy-Funktion.**](dx-graphics-hlsl-ddy.md)

Diese Funktion wird nur in Pixel-Shadern unterstützt.

## <a name="parameters"></a>Parameter



| Element                                                   | Beschreibung                            |
|--------------------------------------------------------|----------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/> | \[in \] Der angegebene Wert.<br/> |



 

## <a name="return-value"></a>Rückgabewert

Die partielle  Ableitung des x-Parameters.

## <a name="type-description"></a>Typbeschreibung



| Name  | [**Vorlagentyp**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Komponententyp**](dx-graphics-hlsl-intrinsic-functions.md) | Size                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *x*   | [**Skalar,**](dx-graphics-hlsl-intrinsic-functions.md) **Vektor** oder **Matrix** | [**schweben**](/windows/desktop/WinProg/windows-data-types)                        | any                            |
| *Ret* | identisch mit eingabe *x*                                                                                              | [**schweben**](/windows/desktop/WinProg/windows-data-types)                        | Gleiche Dimension(en) wie eingabe *x* |



 

## <a name="minimum-shader-model"></a>Shader-Mindestmodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                                                | Unterstützt                                 |
|-----------------------------------------------------------------------------|-------------------------------------------|
| [Shadermodell 5](d3d11-graphics-reference-sm5.md) und höhere Shadermodelle | Ja                                       |
| [Shadermodell 4](dx-graphics-hlsl-sm4.md)                                  | Ja                                       |
| [Shadermodell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md)                   | Ja                                       |
| [Shadermodell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md)                   | yes in ps \_ 2 \_ x; nicht unterstützt in ps \_ 2 \_ 0. |
| [Shadermodell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                   | Nein                                        |



 

Diese Funktion wird in den folgenden Shadertypen unterstützt:



| Scheitelpunkt | Rumpf | Domäne | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     |         |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Systeminterne Funktionen (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

