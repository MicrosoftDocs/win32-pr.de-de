---
title: tziger
description: Gibt die partielle Ableitung des angegebenen-Werts in Bezug auf die y-Koordinate des Bildschirm Raums zurück.
ms.assetid: 1c88804f-a13f-4714-a3ef-466307afbc1b
keywords:
- ddY HLSL
topic_type:
- apiref
api_name:
- ddy
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d27e48a6d9ae237e4e58d1fd30afbac3b2b40d3d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390508"
---
# <a name="ddy"></a>tziger

Gibt die partielle Ableitung des angegebenen-Werts in Bezug auf die y-Koordinate des Bildschirm Raums zurück.



| *ret* (*x*) |
|----------------|



 

Diese Funktion berechnet die partielle Ableitung in Bezug auf die y-Koordinate für den Bildschirmbereich. Verwenden Sie die [**DDX**](dx-graphics-hlsl-ddx.md) -Funktion, um die partielle Ableitung in Bezug auf die x-Koordinate des Bildschirm Raums zu berechnen.

Diese Funktion wird nur in Pixel-Shadern unterstützt.

## <a name="parameters"></a>Parameter



| Element                                                   | BESCHREIBUNG                            |
|--------------------------------------------------------|----------------------------------------|
| <span id="x"></span><span id="X"></span>*Stuben*<br/> | \[im \] angegebenen Wert.<br/> |



 

## <a name="return-value"></a>Rückgabewert

Die partielle Ableitung des *x* -Parameters.

## <a name="type-description"></a>Typbeschreibung



| Name  | [**Vorlagentyp**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Komponententyp**](dx-graphics-hlsl-intrinsic-functions.md) | Size                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *x*   | [**Skalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vektor** oder **Matrix** | [**Hafen**](/windows/desktop/WinProg/windows-data-types)                        | any                            |
| *TZI* | identisch mit Eingabe *x*                                                                                              | [**Hafen**](/windows/desktop/WinProg/windows-data-types)                        | gleiche Dimension (n) wie Eingabe *x* |



 

## <a name="minimum-shader-model"></a>Minimaler Shader-Modell

Diese Funktion wird in den folgenden shadermodellen unterstützt.



| Shadermodell                                                                | Unterstützt                                 |
|-----------------------------------------------------------------------------|-------------------------------------------|
| [Shader Model 5](d3d11-graphics-reference-sm5.md) und höhere shadermodelle | ja                                       |
| [Shadermodell 4](dx-graphics-hlsl-sm4.md)                                  | ja                                       |
| [Shader-Modell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md)                   | ja                                       |
| [Shader-Modell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md)                   | ja in PS \_ 2 \_ x; wird in PS 2 0 nicht unterstützt \_ \_ . |
| [Shader-Modell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                   | nein                                        |



 

Diese Funktion wird in den folgenden Typen von Shadern unterstützt:



| Scheitelpunkt | Hülle | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | x     |         |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Intrinsische Funktionen (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

