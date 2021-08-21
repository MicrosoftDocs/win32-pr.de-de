---
title: tex3Dproj
description: Samples a 3D texture using a projective divide; (Stichproben einer 3D-Textur mithilfe einer projektiven Division) Die Texturkoordinate wird durch t.w geteilt, bevor die Suche erfolgt.
ms.assetid: c7062ef0-3169-4cbe-b47b-4efc80944963
keywords:
- tex3Dproj HLSL
topic_type:
- apiref
api_name:
- tex3Dproj
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1a82c53b0871719f113f6f077234345d5af1a4e65d936c6de6c5d73f77acc3b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119489630"
---
# <a name="tex3dproj"></a>tex3Dproj

Samples a 3D texture using a projective divide; (Stichproben einer 3D-Textur mithilfe einer projektiven Division) Die Texturkoordinate wird durch t.w geteilt, bevor die Suche erfolgt.



| ret tex3Dproj(s, t) |
|---------------------|



 

## <a name="parameters"></a>Parameter



| Element                                                   | Beschreibung                               |
|--------------------------------------------------------|-------------------------------------------|
| <span id="s"></span><span id="S"></span>*s*<br/> | \[im \] Zustand "Sampler".<br/>      |
| <span id="t"></span><span id="T"></span>*T*<br/> | \[in \] Die Texturkoordinate.<br/> |



 

## <a name="return-value"></a>Rückgabewert

Der Wert der Texturdaten.

## <a name="type-description"></a>Typbeschreibung



| Name | Ein/Aus | [**Vorlagentyp**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Komponententyp**](dx-graphics-hlsl-intrinsic-functions.md) | Size |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| s    | in     | [**Objekt (object)**](dx-graphics-hlsl-intrinsic-functions.md) | [sampler3D](dx-graphics-hlsl-sampler.md)                      | 1    |
| t    | in     | [**Vektor**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 4    |
| Ret  | out    | [**Vektor**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 4    |



 

## <a name="minimum-shader-model"></a>Minimales Shadermodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                              | Unterstützt               |
|-----------------------------------------------------------|-------------------------|
| [Shadermodell 4](dx-graphics-hlsl-sm4.md)                | Ja (nur Pixel-Shader) |
| [Shadermodell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | Ja (nur Pixel-Shader) |
| [Shadermodell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | Ja (nur Pixel-Shader) |
| [Shadermodell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | Nein                      |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Systeminterne Funktionen (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

