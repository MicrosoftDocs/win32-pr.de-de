---
title: tex3D (HLSL-Referenz)
description: Probieren Sie eine 3D-Textur aus.
ms.assetid: 713eec24-bdf5-456e-98da-30e2c9d7e808
keywords:
- tex3D HLSL
topic_type:
- apiref
api_name:
- tex3D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8f5f5ea1db13e2c7aea9ee27cb4035bc59b7ac2672e7cb7527f5bd749c8833e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119744800"
---
# <a name="tex3d-hlsl-reference"></a>tex3D (HLSL-Referenz)

Probieren Sie eine 3D-Textur aus.



| ret tex3D(s, t) |
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
| s    | in     | [**Objekt (object)**](dx-graphics-hlsl-intrinsic-functions.md) | [sampler3D](dx-graphics-hlsl-sampler.md)                      | 1    |
| t    | in     | [**Vektor**](dx-graphics-hlsl-intrinsic-functions.md) | [**schweben**](/windows/desktop/WinProg/windows-data-types)                        | 3    |
| Ret  | out    | [**Vektor**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 4    |



 

## <a name="minimum-shader-model"></a>Shader-Mindestmodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                              | Unterstützt                                                                                                                         |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [Shadermodell 4](dx-graphics-hlsl-sm4.md)                | Ja (nur Pixelshader), aber Sie müssen beim Kompilieren die [Legacykompilierungsoption](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax) verwenden. |
| [Shadermodell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | ja (nur Pixelshader)                                                                                                           |
| [Shadermodell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | ja (nur Pixelshader)                                                                                                           |
| [Shadermodell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | ja (nur Pixelshader)                                                                                                           |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Systeminterne Funktionen (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

