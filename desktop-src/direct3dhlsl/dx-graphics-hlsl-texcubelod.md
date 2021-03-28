---
title: texcubelod
description: Stichproben eine cubetextur mit Mipmaps. Die Mipmap-LOD wird in t.w. angegeben.
ms.assetid: fa7b236d-2c52-42bd-9123-919541f9e675
keywords:
- texcubelod HLSL
topic_type:
- apiref
api_name:
- texCUBElod
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 72635211263085f03b87c2e013ea57d1b6a21464
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104976840"
---
# <a name="texcubelod"></a>texcubelod

Stichproben eine cubetextur mit Mipmaps. Die Mipmap-LOD wird in t.w. angegeben.



| Ret texcubelod (s, t) |
|----------------------|



 

## <a name="parameters"></a>Parameter



| Element                                                   | BESCHREIBUNG                               |
|--------------------------------------------------------|-------------------------------------------|
| <span id="s"></span><span id="S"></span>*Hymnen*<br/> | \[im \] samplerzustand.<br/>      |
| <span id="t"></span><span id="T"></span>*Bund*<br/> | \[in \] der Textur Koordinate.<br/> |



 

## <a name="return-value"></a>Rückgabewert

Der Wert der Textur Daten.

## <a name="type-description"></a>Typbeschreibung



| Name | Ein/Aus | [**Vorlagentyp**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Komponententyp**](dx-graphics-hlsl-intrinsic-functions.md) | Size |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| s    | in     | [**Objekt**](dx-graphics-hlsl-intrinsic-functions.md) | [samplercube](dx-graphics-hlsl-sampler.md)                    | 1    |
| t    | in     | [**ve**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 4    |
| TZI  | out    | [**ve**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 4    |



 

## <a name="minimum-shader-model"></a>Minimaler Shader-Modell

Diese Funktion wird in den folgenden shadermodellen unterstützt.



| Shadermodell                                              | Unterstützt               |
|-----------------------------------------------------------|-------------------------|
| [Shadermodell 4](dx-graphics-hlsl-sm4.md)                | Ja (nur Pixel-Shader) |
| [Shader-Modell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | Ja (nur Pixel-Shader) |
| [Shader-Modell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | nein                      |
| [Shader-Modell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | Nein                      |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Intrinsische Funktionen (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

