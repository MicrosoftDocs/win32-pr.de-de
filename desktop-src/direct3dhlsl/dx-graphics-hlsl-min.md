---
title: min
description: Wählt den kleineren von x und y aus.
ms.assetid: 4e10cfc2-d680-4d7f-81b2-fa52024f902d
keywords:
- min HLSL
topic_type:
- apiref
api_name:
- min
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8ba9474383af448c36c6bb1130470aa6706fd8bd06c2d21bef66eb1c4bbcda0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118513821"
---
# <a name="min"></a>min

Wählt den kleineren von x und y aus.



| ret min(x, y) |
|---------------|



 

## <a name="parameters"></a>Parameter



| Element                                                   | Beschreibung                          |
|--------------------------------------------------------|--------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/> | \[in \] Der x-Eingabewert.<br/> |
| <span id="y"></span><span id="Y"></span>*Y*<br/> | \[in \] Der y-Eingabewert.<br/> |



 

## <a name="return-value"></a>Rückgabewert

Der *x-* oder *y-Parameter,* je nachdem, welcher Wert am kleinsten ist.


## <a name="remarks"></a>Hinweise

Denormals werden wie folgt behandelt:

| src0 src1-> | -inf | F             | +inf | NAN  |
|-------------|------|---------------|------|------|
| -inf        | -inf | -inf          | -inf | -inf |
| F           | -inf | src0 oder src1  | src0 | src0 |
| +inf        | -inf | src1          | +inf | +inf |
| NaN         | -inf | src1          | +inf | NaN  |

F bedeutet endliche reelle Zahl.


## <a name="type-description"></a>Typbeschreibung

| Name | Ein/Aus      | [**Vorlagentyp**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Komponententyp**](dx-graphics-hlsl-intrinsic-functions.md)                 | Size                         |
|------|-------------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|------------------------------|
| x    | in          | [**Skalar,**](dx-graphics-hlsl-intrinsic-functions.md) **Vektor** oder **Matrix** | [**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types) | any                          |
| j    | in          | identisch mit eingabe x                                                                                                | [**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types) | Gleiche Dimension(en) wie eingabe x |
| Ret  | Rückgabetyp | identisch mit eingabe x                                                                                                | [**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types) | Gleiche Dimension(en) wie eingabe x |



 

## <a name="minimum-shader-model"></a>Shader-Mindestmodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                                                       | Unterstützt                   |
|------------------------------------------------------------------------------------|-----------------------------|
| [Shadermodell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) und höhere Shadermodelle | Ja                         |
| [Shadermodell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | Ja (im Vergleich zu \_ \_ 1 1 und PS \_ 1 \_ 4) |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Systeminterne Funktionen (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

[**DirectX-Funktionsspezifikation**](https://microsoft.github.io/DirectX-Specs/d3d/archive/D3D11_3_FunctionalSpec.htm#inst_MIN)