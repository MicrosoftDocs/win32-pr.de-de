---
title: distance
description: Gibt einen skalaren Abstand zwischen zwei Vektoren zurück.
ms.assetid: dda8dc39-fd72-4e92-bf9d-e700db0ede9e
keywords:
- entfernunghlsl
topic_type:
- apiref
api_name:
- distance
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c0f3a64778666ac8f7de16b91eed202e36e90ed1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315585"
---
# <a name="distance"></a>distance

Gibt einen skalaren Abstand zwischen zwei Vektoren zurück.



| *ret* -Distanz (*x*, *y*) |
|--------------------------|



 

## <a name="parameters"></a>Parameter



| Element                                                   | BESCHREIBUNG                                                    |
|--------------------------------------------------------|----------------------------------------------------------------|
| <span id="x"></span><span id="X"></span>*Stuben*<br/> | \[im \] ersten zu vergleichenden Gleit Komma Vektor.<br/>  |
| <span id="y"></span><span id="Y"></span>*Teenie*<br/> | \[im \] zweiten zu vergleichenden Gleit Komma Vektor.<br/> |



 

## <a name="return-value"></a>Rückgabewert

Ein Gleit Komma-Skalarwert, der den Abstand zwischen dem *x* -Parameter und dem *y* -Parameter darstellt.

## <a name="type-description"></a>Typbeschreibung



| Name  | [**Vorlagentyp**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Komponententyp**](dx-graphics-hlsl-intrinsic-functions.md) | Size                           |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *x*   | [**ve**](dx-graphics-hlsl-intrinsic-functions.md) | [**Hafen**](/windows/desktop/WinProg/windows-data-types)                        | any                            |
| *y*   | [**ve**](dx-graphics-hlsl-intrinsic-functions.md) | [**Hafen**](/windows/desktop/WinProg/windows-data-types)                        | gleiche Dimension (n) wie Eingabe *x* |
| *TZI* | [**Skalar**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 1                              |



 

## <a name="minimum-shader-model"></a>Minimaler Shader-Modell

Diese Funktion wird in den folgenden shadermodellen unterstützt.



| Shadermodell                                                                       | Unterstützt |
|------------------------------------------------------------------------------------|-----------|
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) und höhere Shader-Modelle | ja       |
| [Shader-Modell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | vs \_ 1 \_ 1  |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Intrinsische Funktionen (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

