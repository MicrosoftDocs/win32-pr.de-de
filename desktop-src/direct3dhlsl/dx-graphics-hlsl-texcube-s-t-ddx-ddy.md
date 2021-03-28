---
title: 'Texcube (HLSL-Referenz): Wählen Sie die MIP-Ebene aus.'
description: Verwendet einen Farbverlauf, um die MIP-Ebene auszuwählen. | Texcube (HLSL-Referenz)
ms.assetid: 5615f48b-eb0a-4de7-a441-51ec3cecf6fd
keywords:
- Texcube HLSL
topic_type:
- apiref
api_name:
- texCUBE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6286b4fedb94b9fd5c84c76171e9478f06e16ce4
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "104982676"
---
# <a name="texcube-hlsl-reference---select-the-mip-level"></a>Texcube (HLSL-Referenz): Wählen Sie die MIP-Ebene aus.

Verwendet einen Farbverlauf, um die MIP-Ebene auszuwählen.



| Ret Texcube (s, t, DDX, ddY) |
|-----------------------------|



 

## <a name="parameters"></a>Parameter



| Element                                                         | BESCHREIBUNG                                                                  |
|--------------------------------------------------------------|------------------------------------------------------------------------------|
| <span id="s"></span><span id="S"></span>*Hymnen*<br/>       | \[im \] samplerzustand.<br/>                                         |
| <span id="t"></span><span id="T"></span>*Bund*<br/>       | \[in \] der Textur Koordinate.<br/>                                    |
| <span id="ddx"></span><span id="DDX"></span>*DDX*<br/> | \[\]die Änderungs Rate der Oberflächengeometrie in der x-Richtung.<br/> |
| <span id="ddy"></span><span id="DDY"></span>*tziger*<br/> | \[\]die Änderungs Rate der Oberflächengeometrie in der y-Richtung.<br/> |



 

## <a name="return-value"></a>Rückgabewert

Der Wert der Textur Daten.

## <a name="type-description"></a>Typbeschreibung



| Name | Ein/Aus | [**Vorlagentyp**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Komponententyp**](dx-graphics-hlsl-intrinsic-functions.md) | Size |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| s    | in     | [**Objekt**](dx-graphics-hlsl-intrinsic-functions.md) | [samplercube](dx-graphics-hlsl-sampler.md)                    | 1    |
| t    | in     | [**ve**](dx-graphics-hlsl-intrinsic-functions.md) | [**Hafen**](/windows/desktop/WinProg/windows-data-types)                        | 3    |
| DDX  | in     | [**ve**](dx-graphics-hlsl-intrinsic-functions.md) | [**Hafen**](/windows/desktop/WinProg/windows-data-types)                        | 3    |
| tziger  | in     | [**ve**](dx-graphics-hlsl-intrinsic-functions.md) | [**Hafen**](/windows/desktop/WinProg/windows-data-types)                        | 3    |
| TZI  | out    | [**ve**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 4    |



 

## <a name="minimum-shader-model"></a>Minimaler Shader-Modell

Diese Funktion wird in den folgenden shadermodellen unterstützt.



| Shadermodell                                              | Unterstützt                |
|-----------------------------------------------------------|--------------------------|
| [Shadermodell 4](dx-graphics-hlsl-sm4.md)                | Ja (nur Pixel-Shader)  |
| [Shader-Modell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | Ja (nur Pixel-Shader) |
| [Shader-Modell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | Ja (nur Pixel-Shader) |
| [Shader-Modell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | nein                       |



 

1.  Eine bedeutende Code Neuanordnung erfolgt, um Farbverlaufs Berechnungen außerhalb der Fluss Steuerung zu verschieben.
2.  Wenn die D3DPSHADERCAPS2 \_ 0-Obergrenze mit D3DD3DPSHADERCAPS2 \_ 0 \_ gradientinstructions festgelegt ist, ordnet der Compiler diese Funktion texldd zu.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Intrinsische Funktionen (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

