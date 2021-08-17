---
title: tex1D (HLSL-Referenz)
description: Probieren Sie eine 1D-Textur aus.
ms.assetid: 587be0fd-af12-4bf0-862b-84988435e90e
keywords:
- tex1D HLSL
topic_type:
- apiref
api_name:
- tex1D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7fd7c8b02d9bbd904ae9205201203bbfdb06ad48d749048be7bc81cbfa83caca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117725688"
---
# <a name="tex1d-hlsl-reference"></a>tex1D (HLSL-Referenz)

Probieren Sie eine 1D-Textur aus.



| ret tex1D(s, t) |
|-----------------|



 

## <a name="parameters"></a>Parameter



| Element                                                   | Beschreibung                               |
|--------------------------------------------------------|-------------------------------------------|
| <span id="s"></span><span id="S"></span>*s*<br/> | \[im \] Samplerzustand.<br/>      |
| <span id="t"></span><span id="T"></span>*T*<br/> | \[in \] Die Texturkoordinate.<br/> |



 

## <a name="return-value"></a>Rückgabewert

Der Wert der Texturdaten.

## <a name="type-description"></a>Typbeschreibung



| Name | Ein/Aus | [**Vorlagentyp**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Komponententyp**](dx-graphics-hlsl-intrinsic-functions.md) | Size |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| s    | in     | [**Objekt (object)**](dx-graphics-hlsl-intrinsic-functions.md) | [sampler1D](dx-graphics-hlsl-sampler.md)                      | 1    |
| t    | in     | [**Skalare**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 1    |
| Ret  | out    | [**Vektor**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 4    |



 

## <a name="minimum-shader-model"></a>Shader-Mindestmodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                              | Unterstützt                                                                                                                         |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [Shadermodell 4](dx-graphics-hlsl-sm4.md)                | Ja (nur Pixelshader), aber Sie müssen beim Kompilieren die [Legacykompilierungsoption](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax) verwenden. |
| [Shadermodell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | ja (nur Pixelshader)                                                                                                           |
| [Shadermodell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | ja (nur Pixelshader)                                                                                                           |
| [Shadermodell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | ja (nur Pixelshader)                                                                                                           |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Systeminterne Funktionen (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

