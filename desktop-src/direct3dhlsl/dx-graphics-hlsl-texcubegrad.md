---
title: texCUBEgrad
description: Probieren Sie eine Cubetextur mithilfe eines Farbverlaufs aus, um die Mipebene auszuwählen. | texCUBEgrad
ms.assetid: ebc5e38a-e314-43b0-9a00-7e4147e24bf0
keywords:
- texCUBEgrad HLSL
topic_type:
- apiref
api_name:
- texCUBEgrad
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 831cfafcdc970a785bb702cabeac5b7ef881526421ef5ada9cb05cd1b407ce6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119884"
---
# <a name="texcubegrad"></a>texCUBEgrad

Probieren Sie eine Cubetextur mithilfe eines Farbverlaufs aus, um die Mipebene auszuwählen.



| ret texCUBEgrad(s, t, ddx, ddy) |
|---------------------------------|



 

## <a name="parameters"></a>Parameter



| Element                                                         | Beschreibung                                                                  |
|--------------------------------------------------------------|------------------------------------------------------------------------------|
| <span id="s"></span><span id="S"></span>*s*<br/>       | \[im \] Samplerzustand.<br/>                                         |
| <span id="t"></span><span id="T"></span>*T*<br/>       | \[in \] Die Texturkoordinate.<br/>                                    |
| <span id="ddx"></span><span id="DDX"></span>*Ddx*<br/> | \[in \] Änderungsrate der Oberflächengeometrie in x Richtung.<br/> |
| <span id="ddy"></span><span id="DDY"></span>*ddy*<br/> | \[in \] Änderungsrate der Oberflächengeometrie in y-Richtung.<br/> |



 

## <a name="return-value"></a>Rückgabewert

Der Wert der Texturdaten.

## <a name="type-description"></a>Typbeschreibung



| Name | Ein/Aus | [**Vorlagentyp**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Komponententyp**](dx-graphics-hlsl-intrinsic-functions.md) | Size |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| s    | in     | [**Objekt (object)**](dx-graphics-hlsl-intrinsic-functions.md) | [samplerCUBE](dx-graphics-hlsl-sampler.md)                    | 1    |
| t    | in     | [**Vektor**](dx-graphics-hlsl-intrinsic-functions.md) | [**schweben**](/windows/desktop/WinProg/windows-data-types)                        | 3    |
| Ddx  | in     | [**Vektor**](dx-graphics-hlsl-intrinsic-functions.md) | [**schweben**](/windows/desktop/WinProg/windows-data-types)                        | 3    |
| ddy  | in     | [**Vektor**](dx-graphics-hlsl-intrinsic-functions.md) | [**schweben**](/windows/desktop/WinProg/windows-data-types)                        | 3    |
| Ret  | out    | [**Vektor**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 4    |



 

## <a name="minimum-shader-model"></a>Shader-Mindestmodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                              | Unterstützt                |
|-----------------------------------------------------------|--------------------------|
| [Shadermodell 4](dx-graphics-hlsl-sm4.md)                | ja (nur Pixelshader)  |
| [Shadermodell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | ja (nur Pixelshader) |
| [Shadermodell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | ja (nur Pixelshader) |
| [Shadermodell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | Nein                       |



 

1.  Umfangreiche Neuanordnung von Code erfolgt, um Gradientenberechnungen außerhalb der Flusssteuerung zu verschieben.
2.  Wenn die Obergrenze D3DPSHADERCAPS2 \_ 0 mit D3DD3DPSHADERCAPS2 \_ 0 \_ GRADIENTINSTRUCTIONS festgelegt ist, ordnet der Compiler diese Funktion texldd zu.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Systeminterne Funktionen (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

