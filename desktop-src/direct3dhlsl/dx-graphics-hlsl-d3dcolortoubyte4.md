---
title: D3DCOLORtoUBYTE4
description: Konvertiert einen Gleit Komma-4D-Vektor, der durch ein D3DCOLOR-Element festgelegt ist, in einen UBYTE4.
ms.assetid: 20a7be00-1e36-41c3-bc98-933b3faa8f35
keywords:
- D3DCOLORtoUBYTE4 HLSL
topic_type:
- apiref
api_name:
- D3DCOLORtoUBYTE4
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c60f0934d6700ec7fbd9e6d9e6443cb6409ab15f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104517072"
---
# <a name="d3dcolortoubyte4"></a>D3DCOLORtoUBYTE4

Konvertiert einen Gleit Komma-4D-Vektor, der durch ein D3DCOLOR-Element festgelegt ist, in einen UBYTE4.



| *ret* D3DCOLORtoUBYTE4 (*x*) |
|-----------------------------|



 

Diese Funktion durch schwimmt und skaliert Komponenten des *x* -Parameters. Verwenden Sie diese Funktion, um den Mangel an UBYTE4-Unterstützung in gewisser Hardware auszugleichen.

## <a name="parameters"></a>Parameter



| Element                                                   | BESCHREIBUNG                                              |
|--------------------------------------------------------|----------------------------------------------------------|
| <span id="x"></span><span id="X"></span>*Stuben*<br/> | \[in \] der zu konvertierenden Gleit Komma Vector4.<br/> |



 

## <a name="return-value"></a>Rückgabewert

Die UBYTE4-Darstellung des *x* -Parameters.

## <a name="type-description"></a>Typbeschreibung



| Name  | [**Vorlagentyp**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Komponententyp**](dx-graphics-hlsl-intrinsic-functions.md) | Size |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| *x*   | [**ve**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 4    |
| *TZI* | [**ve**](dx-graphics-hlsl-intrinsic-functions.md) | [**Zah**](/windows/desktop/WinProg/windows-data-types)                      | 4    |



 

## <a name="minimum-shader-model"></a>Minimaler Shader-Modell

Diese Funktion wird in den folgenden shadermodellen unterstützt.



| Shadermodell                                                                       | Unterstützt |
|------------------------------------------------------------------------------------|-----------|
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) und höhere Shader-Modelle | ja       |
| [Shader-Modell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | vs \_ 1 \_ 1  |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Intrinsische Funktionen (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

