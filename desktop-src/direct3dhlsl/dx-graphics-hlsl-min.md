---
title: Min
description: Wählt den kleineren von x und y aus.
ms.assetid: 4e10cfc2-d680-4d7f-81b2-fa52024f902d
keywords:
- Min. HLSL
topic_type:
- apiref
api_name:
- min
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 129c5cb641c2d69b6c1365d8221663e264060532
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104474100"
---
# <a name="min"></a>Min

Wählt den kleineren von x und y aus.



| Ret min (x, y) |
|---------------|



 

## <a name="parameters"></a>Parameter



| Element                                                   | BESCHREIBUNG                          |
|--------------------------------------------------------|--------------------------------------|
| <span id="x"></span><span id="X"></span>*Stuben*<br/> | \[im \] x-Eingabe Wert.<br/> |
| <span id="y"></span><span id="Y"></span>*Teenie*<br/> | \[im \] y-Eingabe Wert.<br/> |



 

## <a name="return-value"></a>Rückgabewert

Der *x* -oder *y* -Parameter, je nachdem, welcher Wert der kleinste Wert ist.


## <a name="remarks"></a>Bemerkungen

Denormals werden wie folgt behandelt:

| src0 Quelle1-> | -inf | F             | +inf | NAN  |
|-------------|------|---------------|------|------|
| -inf        | -inf | -inf          | -inf | -inf |
| F           | -inf | src0 oder Quelle1  | src0 | src0 |
| +inf        | -inf | src1          | +inf | +inf |
| NaN         | -inf | src1          | +inf | NaN  |

F bedeutet eine endliche reelle Zahl.


## <a name="type-description"></a>Typbeschreibung

| Name | Ein/Aus      | [**Vorlagentyp**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Komponententyp**](dx-graphics-hlsl-intrinsic-functions.md)                 | Size                         |
|------|-------------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|------------------------------|
| x    | in          | [**Skalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vektor** oder **Matrix** | [**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types) | any                          |
| y    | in          | identisch mit Eingabe x                                                                                                | [**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types) | gleiche Dimension (n) wie Eingabe x |
| TZI  | Rückgabetyp | identisch mit Eingabe x                                                                                                | [**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types) | gleiche Dimension (n) wie Eingabe x |



 

## <a name="minimum-shader-model"></a>Minimaler Shader-Modell

Diese Funktion wird in den folgenden shadermodellen unterstützt.



| Shadermodell                                                                       | Unterstützt                   |
|------------------------------------------------------------------------------------|-----------------------------|
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) und höhere Shader-Modelle | ja                         |
| [Shader-Modell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | Ja (vs \_ 1 \_ 1 und PS \_ 1 \_ 4) |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Intrinsische Funktionen (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

[**DirectX-Funktionsspezifikation**](https://microsoft.github.io/DirectX-Specs/d3d/archive/D3D11_3_FunctionalSpec.htm#inst_MIN)