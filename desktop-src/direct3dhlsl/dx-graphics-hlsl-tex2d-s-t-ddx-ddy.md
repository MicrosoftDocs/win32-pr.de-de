---
title: 'tex2D (HLSL-Referenz): Wählen Sie die MIP-Ebene aus.'
description: Stichproben einer 2D-Textur mithilfe eines Farbverlaufs, um die MIP-Ebene auszuwählen. | tex2D (HLSL-Referenz)
ms.assetid: 0e8c32ed-d174-4045-9cbf-6c04586ea5bb
keywords:
- tex2D HLSL
topic_type:
- apiref
api_name:
- tex2D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 43e6d60505964beb47eb14bb797a60a3c78089371c9e1fd67463586ba1e5db0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118513153"
---
# <a name="tex2d-hlsl-reference---select-the-mip-level"></a>tex2D (HLSL-Referenz): Wählen Sie die MIP-Ebene aus.

Stichproben einer 2D-Textur mithilfe eines Farbverlaufs, um die MIP-Ebene auszuwählen.



| ret tex2D(s, t, ddx, ddy) |
|---------------------------|



 

## <a name="parameters"></a>Parameter



| Element                                                         | BESCHREIBUNG                                                                  |
|--------------------------------------------------------------|------------------------------------------------------------------------------|
| <span id="s"></span><span id="S"></span>*s*<br/>       | \[im \] Zustand "Sampler".<br/>                                         |
| <span id="t"></span><span id="T"></span>*T*<br/>       | \[in \] Die Texturkoordinaten.<br/>                                   |
| <span id="ddx"></span><span id="DDX"></span>*Ddx*<br/> | \[in \] Änderungsrate der Oberflächengeometrie in x-Richtung.<br/> |
| <span id="ddy"></span><span id="DDY"></span>*ddy*<br/> | \[in \] Änderungsrate der Oberflächengeometrie in y-Richtung.<br/> |



 

## <a name="return-value"></a>Rückgabewert

Der Wert der Texturdaten.

## <a name="type-description"></a>Typbeschreibung



| Name | Ein/Aus | [**Vorlagentyp**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Komponententyp**](dx-graphics-hlsl-intrinsic-functions.md) | Size |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| s    | in     | [**Objekt (object)**](dx-graphics-hlsl-intrinsic-functions.md) | [sampler2D](dx-graphics-hlsl-sampler.md)                      | 1    |
| t    | in     | [**Vektor**](dx-graphics-hlsl-intrinsic-functions.md) | [**schweben**](/windows/desktop/WinProg/windows-data-types)                        | 2    |
| Ddx  | in     | [**Vektor**](dx-graphics-hlsl-intrinsic-functions.md) | [**schweben**](/windows/desktop/WinProg/windows-data-types)                        | 2    |
| ddy  | in     | [**Vektor**](dx-graphics-hlsl-intrinsic-functions.md) | [**schweben**](/windows/desktop/WinProg/windows-data-types)                        | 2    |
| Ret  | out    | [**Vektor**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 4    |



 

## <a name="minimum-shader-model"></a>Minimales Shadermodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                              | Unterstützt                |
|-----------------------------------------------------------|--------------------------|
| [Shadermodell 4](dx-graphics-hlsl-sm4.md)                | Ja (nur Pixel-Shader)  |
| [Shadermodell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | Ja (nur Pixel-Shader) |
| [Shadermodell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | Ja (nur Pixel-Shader) |
| [Shadermodell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | nein                       |



 

1.  Eine erhebliche Code-Neuanordnung erfolgt, um Gradientenberechnungen außerhalb der Flusssteuerung zu verschieben.
2.  Wenn die D3DPSHADERCAPS2 0-Obergrenze mit \_ D3DD3DPSHADERCAPS2 \_ 0 GRADIENTINSTRUCTIONS festgelegt ist, ordnet der Compiler diese Funktion \_ texldd zu.

## <a name="remarks"></a>Hinweise

Wenn die Flusssteuerung in einem Shader vorhanden ist, ist das Ergebnis einer farbverlaufsberechnung, die innerhalb eines bestimmten Verzweigungspfads angefordert wird, mehrdeutig, wenn angrenzende Pixel separate Flusssteuerungspfade heruntergefahren werden können. Daher wird die Verwendung von Pixel-Shader-Vorgangen, bei denen eine Farbverlaufsberechnung an einer Position innerhalb eines Flusssteuerungskonstrukts durchgeführt werden soll, als unzulässig eingestuft, die für einen bestimmten Primitiven, der rastert wird, pixelübergreifend variieren kann. Wenn eine der Seiten einer **if-Anweisung** mit dem Branchattribut eine Gradient-Funktion verwendet, kann ein Compilerfehler generiert werden. Siehe [if-Anweisung (DirectX HLSL).](dx-graphics-hlsl-if.md)

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Systeminterne Funktionen (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

