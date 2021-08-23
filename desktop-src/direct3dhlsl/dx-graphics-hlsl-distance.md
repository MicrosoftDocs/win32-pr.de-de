---
title: distance
description: Gibt einen Abstandsskalar zwischen zwei Vektoren zurück.
ms.assetid: dda8dc39-fd72-4e92-bf9d-e700db0ede9e
keywords:
- Distance HLSL
topic_type:
- apiref
api_name:
- distance
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f51c5e9865b9dfc1c5a941beb43010dc8fad64e2d8ac8763998c22cb3e0dfbd5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726540"
---
# <a name="distance"></a>distance

Gibt einen Abstandsskalar zwischen zwei Vektoren zurück.



| *ret* distance(*x*, *y*) |
|--------------------------|



 

## <a name="parameters"></a>Parameter



| Element                                                   | Beschreibung                                                    |
|--------------------------------------------------------|----------------------------------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/> | \[in \] Der erste zu vergleichende Gleitkommavektor.<br/>  |
| <span id="y"></span><span id="Y"></span>*Y*<br/> | \[in \] Der zweite zu vergleichende Gleitkommavektor.<br/> |



 

## <a name="return-value"></a>Rückgabewert

Ein Gleitkomma- und Skalarwert, der den Abstand zwischen dem *x-Parameter* und dem *y-Parameter* darstellt.

## <a name="type-description"></a>Typbeschreibung



| Name  | [**Vorlagentyp**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Komponententyp**](dx-graphics-hlsl-intrinsic-functions.md) | Size                           |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *x*   | [**Vektor**](dx-graphics-hlsl-intrinsic-functions.md) | [**schweben**](/windows/desktop/WinProg/windows-data-types)                        | any                            |
| *y*   | [**Vektor**](dx-graphics-hlsl-intrinsic-functions.md) | [**schweben**](/windows/desktop/WinProg/windows-data-types)                        | Gleiche Dimension(en) wie eingabe *x* |
| *Ret* | [**Skalare**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 1                              |



 

## <a name="minimum-shader-model"></a>Shader-Mindestmodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                                                       | Unterstützt |
|------------------------------------------------------------------------------------|-----------|
| [Shadermodell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) und höhere Shadermodelle | Ja       |
| [Shadermodell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | Vs \_ 1 \_ 1  |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Systeminterne Funktionen (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

