---
title: Texcube (HLSL-Referenz)
description: Abtastungen einer Cube-Textur.
ms.assetid: 77943eb9-86e8-4ae4-8975-8f925e084ce4
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
ms.openlocfilehash: 524ed44028372eeabf176c30da8b3a31a8ee7988
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039122"
---
# <a name="texcube-hlsl-reference"></a>Texcube (HLSL-Referenz)

Abtastungen einer Cube-Textur.



| Ret Texcube (s, t) |
|-------------------|



 

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
| t    | in     | [**ve**](dx-graphics-hlsl-intrinsic-functions.md) | [**Hafen**](/windows/desktop/WinProg/windows-data-types)                        | 3    |
| TZI  | out    | [**ve**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 4    |



 

## <a name="minimum-shader-model"></a>Minimaler Shader-Modell

Diese Funktion wird in den folgenden shadermodellen unterstützt.



| Shadermodell                                              | Unterstützt               |
|-----------------------------------------------------------|-------------------------|
| [Shadermodell 4](dx-graphics-hlsl-sm4.md)                | Ja (nur Pixel-Shader) |
| [Shader-Modell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | Ja (nur Pixel-Shader) |
| [Shader-Modell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | Ja (nur Pixel-Shader) |
| [Shader-Modell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | Ja (nur Pixel-Shader) |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Intrinsische Funktionen (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

