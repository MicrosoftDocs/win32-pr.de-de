---
title: alle
description: Bestimmt, ob alle Komponenten des angegebenen Werts nicht 0 (null) sind.
ms.assetid: 9ee079ff-cd2c-41f5-98cd-ea1f4215e7d5
keywords:
- alle HLSL
topic_type:
- apiref
api_name:
- all
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9ddc9dd6177021500a84fb5fd8feba166b42ef671dfd96af3536615a068bfce1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119673600"
---
# <a name="all"></a>alle

Bestimmt, ob alle Komponenten des angegebenen Werts nicht 0 (null) sind.



| *ret* all(*x*) |
|----------------|



 

## <a name="parameters"></a>Parameter



| Element                                                   | BESCHREIBUNG                            |
|--------------------------------------------------------|----------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/> | \[in \] Der angegebene Wert.<br/> |



 

## <a name="return-value"></a>Rückgabewert

**TRUE,** wenn alle Komponenten des *x-Parameters* nicht 0 (null) sind; andernfalls **FALSE.**

## <a name="remarks"></a>Hinweise

Diese Funktion ähnelt der [**systeminternen**](dx-graphics-hlsl-any.md) HLSL-Funktion. Die **any-Funktion** bestimmt, ob Komponenten des angegebenen Werts nicht 0 (null) sind, während die **all-Funktion** bestimmt, ob alle Komponenten des angegebenen Werts nicht 0 (null) sind.

## <a name="type-description"></a>Typbeschreibung



| Name  | [**Vorlagentyp**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Komponententyp**](dx-graphics-hlsl-intrinsic-functions.md)                                                         | Size |
|-------|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|------|
| *x*   | [**Skalar,**](dx-graphics-hlsl-intrinsic-functions.md) **Vektor** oder **Matrix** | [**float,**](/windows/desktop/WinProg/windows-data-types) [**int,**](/windows/desktop/WinProg/windows-data-types) [**bool**](/windows/desktop/WinProg/windows-data-types) | any  |
| *Ret* | [**Skalare**](dx-graphics-hlsl-intrinsic-functions.md)                            | [**bool**](/windows/desktop/WinProg/windows-data-types)                                                                                 | 1    |



 

## <a name="minimum-shader-model"></a>Minimales Shadermodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                                                       | Unterstützt             |
|------------------------------------------------------------------------------------|-----------------------|
| [Shadermodell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) und höhere Shadermodelle | ja                   |
| [Shadermodell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | vs \_ 1 \_ 1 und ps \_ 1 \_ 4 |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Systeminterne Funktionen (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

