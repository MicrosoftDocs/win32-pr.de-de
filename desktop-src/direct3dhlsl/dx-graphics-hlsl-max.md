---
title: max
description: Wählt die größer als x und y aus.
ms.assetid: 08e17a0c-6d44-49ea-b613-bd262534522c
keywords:
- Max. HLSL
topic_type:
- apiref
api_name:
- max
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e81eca4f5cabea57f36aa66b722fedb3e1176c3c189db9cdcfd610e4e26047c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118791471"
---
# <a name="max"></a>max

Wählt die größer als x und y aus.



| ret max(x, y) |
|---------------|



 

## <a name="parameters"></a>Parameter



| Element                                                   | BESCHREIBUNG                          |
|--------------------------------------------------------|--------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/> | \[in \] Der x-Eingabewert.<br/> |
| <span id="y"></span><span id="Y"></span>*Y*<br/> | \[in \] Der y-Eingabewert.<br/> |



 

## <a name="return-value"></a>Rückgabewert

Der *x-* *oder y-Parameter,* der der größte Wert ist.


## <a name="remarks"></a>Hinweise

Denormale werden wie folgt behandelt:

| src0 src1-> | -inf | F             | +inf | NAN  |
|-------------|------|---------------|------|------|
| -inf        | -inf | src1          | +inf | -inf |
| F           | src0 | src0 oder src1  | +inf | src0 |
| +inf        | +inf | +inf          | +inf | +inf |
| NaN         | -inf | src1          | +inf | NaN  |

F bedeutet endliche reale Zahl.


## <a name="type-description"></a>Typbeschreibung

| Name | Ein/Aus      | [**Vorlagentyp**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Komponententyp**](dx-graphics-hlsl-intrinsic-functions.md)                 | Size                         |
|------|-------------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|------------------------------|
| x    | in          | [**Skalar,**](dx-graphics-hlsl-intrinsic-functions.md) **Vektor** oder **Matrix** | [**float,**](/windows/desktop/WinProg/windows-data-types) [ **int**](/windows/desktop/WinProg/windows-data-types) | any                          |
| y    | in          | identisch mit Eingabe x                                                                                                | [**float,**](/windows/desktop/WinProg/windows-data-types) [ **int**](/windows/desktop/WinProg/windows-data-types) | Gleiche Dimension(n) wie Eingabe x |
| Ret  | Rückgabetyp | identisch mit Eingabe x                                                                                                | [**float,**](/windows/desktop/WinProg/windows-data-types) [ **int**](/windows/desktop/WinProg/windows-data-types) | Gleiche Dimension(n) wie Eingabe x |



 

## <a name="minimum-shader-model"></a>Minimales Shadermodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                                                       | Unterstützt                   |
|------------------------------------------------------------------------------------|-----------------------------|
| [Shadermodell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) und höhere Shadermodelle | Ja                         |
| [Shadermodell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | Ja (im Vergleich \_ zu 1 \_ 1 und Ps \_ 1 \_ 4) |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Systeminterne Funktionen (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

[**DirectX-Funktionsspezifikation**](https://microsoft.github.io/DirectX-Specs/d3d/archive/D3D11_3_FunctionalSpec.htm#inst_MAX) 
</dt> </dl>
 
