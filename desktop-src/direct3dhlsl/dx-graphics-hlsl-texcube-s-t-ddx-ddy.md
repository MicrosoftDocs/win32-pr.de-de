---
title: 'texCUBE (HLSL-Referenz): Wählen Sie die MIP-Ebene aus.'
description: Stichproben einer Würfeltextur mithilfe eines Farbverlaufs, um die Mipebene auszuwählen. | texCUBE (HLSL-Referenz)
ms.assetid: 5615f48b-eb0a-4de7-a441-51ec3cecf6fd
keywords:
- texCUBE HLSL
topic_type:
- apiref
api_name:
- texCUBE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4e236a17359f94adcb8b54d3af8b67df37b1fcb6aaf7e75e6f4dba298eaae7aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117725658"
---
# <a name="texcube-hlsl-reference---select-the-mip-level"></a>texCUBE (HLSL-Referenz): Wählen Sie die MIP-Ebene aus.

Stichproben einer Würfeltextur mithilfe eines Farbverlaufs, um die Mipebene auszuwählen.



| ret texCUBE(s, t, ddx, ddy) |
|-----------------------------|



 

## <a name="parameters"></a>Parameter



| Element                                                         | Beschreibung                                                                  |
|--------------------------------------------------------------|------------------------------------------------------------------------------|
| <span id="s"></span><span id="S"></span>*s*<br/>       | \[im \] Zustand "Sampler".<br/>                                         |
| <span id="t"></span><span id="T"></span>*T*<br/>       | \[in \] Die Texturkoordinate.<br/>                                    |
| <span id="ddx"></span><span id="DDX"></span>*Ddx*<br/> | \[in \] Änderungsrate der Oberflächengeometrie in x-Richtung.<br/> |
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



 

## <a name="minimum-shader-model"></a>Minimales Shadermodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                              | Unterstützt                |
|-----------------------------------------------------------|--------------------------|
| [Shadermodell 4](dx-graphics-hlsl-sm4.md)                | Ja (nur Pixel-Shader)  |
| [Shadermodell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | Ja (nur Pixel-Shader) |
| [Shadermodell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | Ja (nur Pixel-Shader) |
| [Shadermodell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | Nein                       |



 

1.  Eine erhebliche Code-Neuanordnung erfolgt, um Gradientenberechnungen außerhalb der Flusssteuerung zu verschieben.
2.  Wenn die D3DPSHADERCAPS2 0-Obergrenze mit \_ D3DD3DPSHADERCAPS2 \_ 0 GRADIENTINSTRUCTIONS festgelegt ist, ordnet der Compiler diese Funktion \_ texldd zu.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Systeminterne Funktionen (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

