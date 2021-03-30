---
title: alle
description: Bestimmt, ob alle Komponenten des angegebenen-Werts ungleich 0 (null) sind.
ms.assetid: 9ee079ff-cd2c-41f5-98cd-ea1f4215e7d5
keywords:
- Alle HLSL
topic_type:
- apiref
api_name:
- all
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 59d59e18655aab10d13af998f4e2aa94da3fa08b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104976849"
---
# <a name="all"></a>alle

Bestimmt, ob alle Komponenten des angegebenen-Werts ungleich 0 (null) sind.



| *ret* all (*x*) |
|----------------|



 

## <a name="parameters"></a>Parameter



| Element                                                   | BESCHREIBUNG                            |
|--------------------------------------------------------|----------------------------------------|
| <span id="x"></span><span id="X"></span>*Stuben*<br/> | \[im \] angegebenen Wert.<br/> |



 

## <a name="return-value"></a>Rückgabewert

**True** , wenn alle Komponenten des *x* -Parameters ungleich NULL sind. andernfalls **false**.

## <a name="remarks"></a>Bemerkungen

Diese Funktion [**ähnelt der**](dx-graphics-hlsl-any.md) intrinsischen HLSL-Funktion. Die **any** -Funktion bestimmt, ob Komponenten des angegebenen-Werts ungleich 0 (null) sind, während die **all** -Funktion bestimmt, ob alle Komponenten des angegebenen Werts ungleich 0 (null) sind.

## <a name="type-description"></a>Typbeschreibung



| Name  | [**Vorlagentyp**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Komponententyp**](dx-graphics-hlsl-intrinsic-functions.md)                                                         | Size |
|-------|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|------|
| *x*   | [**Skalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vektor** oder **Matrix** | [**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types), [**bool**](/windows/desktop/WinProg/windows-data-types) | any  |
| *TZI* | [**Skalar**](dx-graphics-hlsl-intrinsic-functions.md)                            | [**bool**](/windows/desktop/WinProg/windows-data-types)                                                                                 | 1    |



 

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

 

