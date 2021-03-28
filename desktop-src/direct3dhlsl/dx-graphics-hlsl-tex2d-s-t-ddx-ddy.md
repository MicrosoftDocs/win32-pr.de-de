---
title: 'tex2D (HLSL-Referenz): Wählen Sie die MIP-Ebene aus.'
description: Stichproben eine 2D-Textur mit einem Farbverlauf, um die MIP-Ebene auszuwählen. | tex2D (HLSL-Referenz)
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
ms.openlocfilehash: 5a642a92756f3f0774e5719aa1fcf9ec302eecb5
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/16/2021
ms.locfileid: "104982693"
---
# <a name="tex2d-hlsl-reference---select-the-mip-level"></a>tex2D (HLSL-Referenz): Wählen Sie die MIP-Ebene aus.

Stichproben eine 2D-Textur mit einem Farbverlauf, um die MIP-Ebene auszuwählen.



| Ret tex2D (s, t, DDX, ddY) |
|---------------------------|



 

## <a name="parameters"></a>Parameter



| Element                                                         | BESCHREIBUNG                                                                  |
|--------------------------------------------------------------|------------------------------------------------------------------------------|
| <span id="s"></span><span id="S"></span>*Hymnen*<br/>       | \[im \] samplerzustand.<br/>                                         |
| <span id="t"></span><span id="T"></span>*Bund*<br/>       | \[in \] den Texturkoordinaten.<br/>                                   |
| <span id="ddx"></span><span id="DDX"></span>*DDX*<br/> | \[\]die Änderungs Rate der Oberflächengeometrie in der x-Richtung.<br/> |
| <span id="ddy"></span><span id="DDY"></span>*tziger*<br/> | \[\]die Änderungs Rate der Oberflächengeometrie in der y-Richtung.<br/> |



 

## <a name="return-value"></a>Rückgabewert

Der Wert der Textur Daten.

## <a name="type-description"></a>Typbeschreibung



| Name | Ein/Aus | [**Vorlagentyp**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Komponententyp**](dx-graphics-hlsl-intrinsic-functions.md) | Size |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| s    | in     | [**Objekt**](dx-graphics-hlsl-intrinsic-functions.md) | [sampler2D](dx-graphics-hlsl-sampler.md)                      | 1    |
| t    | in     | [**ve**](dx-graphics-hlsl-intrinsic-functions.md) | [**Hafen**](/windows/desktop/WinProg/windows-data-types)                        | 2    |
| DDX  | in     | [**ve**](dx-graphics-hlsl-intrinsic-functions.md) | [**Hafen**](/windows/desktop/WinProg/windows-data-types)                        | 2    |
| tziger  | in     | [**ve**](dx-graphics-hlsl-intrinsic-functions.md) | [**Hafen**](/windows/desktop/WinProg/windows-data-types)                        | 2    |
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

## <a name="remarks"></a>Bemerkungen

Wenn die Fluss Steuerung in einem Shader vorhanden ist, ist das Ergebnis einer in einem bestimmten Verzweigungs Pfad angeforderten gradientenberechnung mehrdeutig, wenn angrenzende Pixel getrennte Fluss Steuerungs Pfade nach unten durchlaufen können. Daher wird die Verwendung eines pixelshadervorgangs als unzulässig angesehen, der eine gradientenberechnung an einem Speicherort anfordert, der sich innerhalb eines Fluss Steuerungs Konstrukts befindet, das für ein bestimmtes primitiv, das gerengt wird, in Pixel variieren kann. Wenn eine Seite einer **if** -Anweisung mit dem Branch-Attribut eine Gradient-Funktion verwendet, kann ein Compilerfehler generiert werden. Siehe [if-Anweisung (DirectX HLSL)](dx-graphics-hlsl-if.md).

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Intrinsische Funktionen (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

