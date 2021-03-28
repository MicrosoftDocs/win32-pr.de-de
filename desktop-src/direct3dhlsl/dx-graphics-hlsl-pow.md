---
title: pow
description: Gibt den angegebenen Wert in der angegebenen Potenz zurück.
ms.assetid: 1d64452c-81c7-4ef5-a332-13e0263c2cd1
keywords:
- Pow HLSL
topic_type:
- apiref
api_name:
- pow
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f190c374b6c0ac42d41862eb918f0c0482b6d785
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104474093"
---
# <a name="pow"></a>pow

Gibt den angegebenen Wert in der angegebenen Potenz zurück.



| *ret* Pow (*x*, *y*) |
|---------------------|



 

## <a name="parameters"></a>Parameter



| Element                                                   | BESCHREIBUNG                            |
|--------------------------------------------------------|----------------------------------------|
| <span id="x"></span><span id="X"></span>*Stuben*<br/> | \[im \] angegebenen Wert.<br/> |
| <span id="y"></span><span id="Y"></span>*Teenie*<br/> | \[in \] der angegebenen Potenz.<br/> |



 

## <a name="return-value"></a>Rückgabewert

Der *x* -Parameter, der für den *y* -Parameter ausgelöst wird.

## <a name="remarks"></a>Bemerkungen

Die intrinsische Funktion " **Pow** HLSL" berechnet *x*<sup>y</sup>.



| X      | Y      | Ergebnis                                                                      |
|--------|--------|-----------------------------------------------------------------------------|
| < 0 | any    | NAN                                                                         |
| > 0 | = = 0   | 1                                                                           |
| = = 0   | > 0 | 0                                                                           |
| = = 0   | < 0 | INF                                                                         |
| > 0 | < 0 | 1/X<sup>-Y</sup>                                                            |
| = = 0   | = = 0   | Hängt vom jeweiligen Grafikprozessor ab.<br/> 0, oder 1 oder NaN<br/> |



 

## <a name="type-description"></a>Typbeschreibung



| Name  | [**Vorlagentyp**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Komponententyp**](dx-graphics-hlsl-intrinsic-functions.md) | Size                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *x*   | [**Skalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vektor** oder **Matrix** | [**Hafen**](/windows/desktop/WinProg/windows-data-types)                        | any                            |
| *y*   | identisch mit Eingabe *x*                                                                                              | [**Hafen**](/windows/desktop/WinProg/windows-data-types)                        | gleiche Dimension (n) wie Eingabe *x* |
| *TZI* | identisch mit Eingabe *x*                                                                                              | [**Hafen**](/windows/desktop/WinProg/windows-data-types)                        | gleiche Dimension (n) wie Eingabe *x* |



 

## <a name="minimum-shader-model"></a>Minimaler Shader-Modell

Diese Funktion wird in den folgenden shadermodellen unterstützt.



| Shadermodell                                                                       | Unterstützt           |
|------------------------------------------------------------------------------------|---------------------|
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) und höhere Shader-Modelle | ja                 |
| [Shader-Modell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | Ja ( \_ nur vs 1 \_ 1) |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Intrinsische Funktionen (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

