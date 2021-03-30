---
title: abs
description: Gibt den absoluten Wert des angegebenen-Werts zurück.
ms.assetid: 8c4cfd8f-8aac-4db3-8247-ce2bbf501e80
keywords:
- ABS HLSL
topic_type:
- apiref
api_name:
- abs
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1acd1903e1a65a38f5af7549ab52577bc6cba51c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104976793"
---
# <a name="abs"></a>abs

Gibt den absoluten Wert des angegebenen-Werts zurück.



| Ret Abs (*x*) |
|--------------|



 

## <a name="parameters"></a>Parameter



| Element                                                   | BESCHREIBUNG                            |
|--------------------------------------------------------|----------------------------------------|
| <span id="x"></span><span id="X"></span>*Stuben*<br/> | \[im \] angegebenen Wert.<br/> |



 

## <a name="return-value"></a>Rückgabewert

Der absolute Wert des *x* -Parameters.

## <a name="type-description"></a>Typbeschreibung



| Name  | [**Vorlagentyp**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Komponententyp**](dx-graphics-hlsl-intrinsic-functions.md)                 | Size                           |
|-------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|--------------------------------|
| *x*   | [**Skalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vektor** oder **Matrix** | [**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types) | any                            |
| *TZI* | identisch mit Eingabe *x*                                                                                              | identisch mit Eingabe *x*                                                              | gleiche Dimension (n) wie Eingabe *x* |



 

## <a name="minimum-shader-model"></a>Minimaler Shader-Modell

Diese Funktion wird in den folgenden shadermodellen unterstützt.



| Shadermodell                                                                       | Unterstützt             |
|------------------------------------------------------------------------------------|-----------------------|
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) und höhere Shader-Modelle | ja                   |
| [Shader-Modell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | vs \_ 1 \_ 1 und PS \_ 1 \_ 4 |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Intrinsische Funktionen (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

