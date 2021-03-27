---
title: DDX
description: Gibt die partielle Ableitung des angegebenen-Werts in Bezug auf die x-Koordinate des Bildschirm Raums zurück.
ms.assetid: a21c2d2a-7c62-4dc6-8521-273690be1104
keywords:
- DDX HLSL
topic_type:
- apiref
api_name:
- ddx
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dc82f41e8968ccfadaf5d87a8058d332f04ce3a7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390509"
---
# <a name="ddx"></a>DDX

Gibt die partielle Ableitung des angegebenen-Werts in Bezug auf die x-Koordinate des Bildschirm Raums zurück.



| *ret* DDX (*x*) |
|----------------|



 

Diese Funktion berechnet die partielle Ableitung in Bezug auf die x-Koordinate des Bildschirm Raums. Um die partielle Ableitung in Bezug auf die y-Koordinate des Bildschirm Raums zu berechnen, verwenden Sie die Funktion [**ddY**](dx-graphics-hlsl-ddy.md) .

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

 

