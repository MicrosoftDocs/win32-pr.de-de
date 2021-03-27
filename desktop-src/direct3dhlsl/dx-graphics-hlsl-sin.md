---
title: sin
description: Gibt den Sinus des angegebenen-Werts zurück.
ms.assetid: e1c3ead8-73dd-4798-8553-1a42dbaefe8e
keywords:
- Sin HLSL
topic_type:
- apiref
api_name:
- sin
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d48332d35052a893dcb348a70e4d464a6bbfe0c9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390861"
---
# <a name="sin"></a>sin

Gibt den Sinus des angegebenen-Werts zurück.



| *ret* Sin (*x*) |
|----------------|



 

## <a name="parameters"></a>Parameter



| Element                                                   | BESCHREIBUNG                                        |
|--------------------------------------------------------|----------------------------------------------------|
| <span id="x"></span><span id="X"></span>*Stuben*<br/> | \[im \] angegebenen Wert im Bogenmaße.<br/> |



 

## <a name="return-value"></a>Rückgabewert

Der Sinus des *x* -Parameters.

## <a name="type-description"></a>Typbeschreibung



| Name  | [**Vorlagentyp**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Komponententyp**](dx-graphics-hlsl-intrinsic-functions.md) | Size                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *x*   | [**Skalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vektor** oder **Matrix** | [**Hafen**](/windows/desktop/WinProg/windows-data-types)                        | any                            |
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

 

