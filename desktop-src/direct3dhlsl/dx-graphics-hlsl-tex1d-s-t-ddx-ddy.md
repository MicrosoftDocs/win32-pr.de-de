---
title: 'tex1D (HLSL-Referenz): Wählen Sie die MIP-Ebene aus.'
description: Probieren Sie eine 1D-Textur mithilfe eines Farbverlaufs aus, um die Mipebene auszuwählen. | tex1D (HLSL-Referenz)
ms.assetid: 1fa01f39-1c01-4a2e-9f7d-ca8e887b00bb
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
ms.openlocfilehash: c9700f3e70c57a8ccd96d0a88d12a88bdfcbbcabb85a79d65f2b658b35d40552
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119489660"
---
# <a name="tex1d-hlsl-reference---select-the-mip-level"></a>tex1D (HLSL-Referenz): Wählen Sie die MIP-Ebene aus.

Probieren Sie eine 1D-Textur mithilfe eines Farbverlaufs aus, um die Mipebene auszuwählen.



| ret tex1D(s, t, ddx, ddy) |
|---------------------------|



 

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
| s    | in     | [**Objekt (object)**](dx-graphics-hlsl-intrinsic-functions.md) | [sampler1D](dx-graphics-hlsl-sampler.md)                      | 1    |
| t    | in     | [**Vektor**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 1    |
| Ddx  | in     | [**Vektor**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 1    |
| ddy  | in     | [**Vektor**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 1    |
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

## <a name="remarks"></a>Hinweise

Wenn die Flusssteuerung in einem Shader vorhanden ist, ist das Ergebnis einer Gradientenberechnung, die innerhalb eines bestimmten Verzweigungspfads angefordert wird, mehrdeutig, wenn benachbarte Pixel separate Flusssteuerungspfade durchlaufen können. Daher wird es als unzulässig angesehen, einen Pixelshadervorgang zu verwenden, der anfordert, dass eine Farbverlaufsberechnung an einer Position innerhalb eines Flusssteuerungskonstrukts durchgeführt wird, die für ein bestimmtes Primitive, das gerastert wird, pixelübergreifend variieren kann. Wenn auf beiden Seiten einer **if-Anweisung** mit dem Branchattribut eine Farbverlaufsfunktion verwendet wird, kann ein Compilerfehler generiert werden. Siehe [if-Anweisung (DirectX HLSL)](dx-graphics-hlsl-if.md).

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Systeminterne Funktionen (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

