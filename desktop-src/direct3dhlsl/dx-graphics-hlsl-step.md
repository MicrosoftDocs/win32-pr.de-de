---
title: Schritt
description: Vergleicht zwei Werte und gibt 0 oder 1 basierend darauf zurück, welcher Wert größer ist.
ms.assetid: 1c1c4ec4-ae97-42ce-99af-71903e0b5edf
keywords:
- Schritt HLSL
topic_type:
- apiref
api_name:
- step
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 27fe6985a4dfb4e77f1052b421a6c46c617395f46b4484f046b33919a935613f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119276510"
---
# <a name="step"></a>Schritt

Vergleicht zwei Werte und gibt 0 oder 1 basierend darauf zurück, welcher Wert größer ist.



| *ret* step(*y*, *x*) |
|----------------------|



 

## <a name="parameters"></a>Parameter



| Element                                                   | BESCHREIBUNG                                                   |
|--------------------------------------------------------|---------------------------------------------------------------|
| <span id="y"></span><span id="Y"></span>*Y*<br/> | \[in \] Der erste zu vergleichende Gleitkommawert.<br/>  |
| <span id="x"></span><span id="X"></span>*X*<br/> | \[in \] Der zweite zu vergleichende Gleitkommawert.<br/> |



 

## <a name="return-value"></a>Rückgabewert

1, wenn der *x-Parameter* größer oder gleich dem *y-Parameter* ist; andernfalls 0.

## <a name="remarks"></a>Hinweise

Diese Funktion verwendet die folgende Formel: (*x*  >=  *y*) ? 1 : 0. Die Funktion gibt entweder 0 oder 1 zurück, je nachdem, ob der *x-Parameter* größer als der *y-Parameter* ist. Um eine reibungslose Interpolation zwischen 0 und 1 zu berechnen, verwenden Sie die intrinsische HLSL-Funktion [**smoothstep.**](dx-graphics-hlsl-smoothstep.md)

## <a name="type-description"></a>Typbeschreibung



| Name  | [**Vorlagentyp**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Komponententyp**](dx-graphics-hlsl-intrinsic-functions.md) | Size                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *y*   | [**Skalar,**](dx-graphics-hlsl-intrinsic-functions.md) **Vektor** oder **Matrix** | [**schweben**](/windows/desktop/WinProg/windows-data-types)                        | any                            |
| *x*   | entspricht der Eingabe *y*                                                                                              | [**schweben**](/windows/desktop/WinProg/windows-data-types)                        | gleiche Dimension(en) wie eingabe *y* |
| *Ret* | entspricht der Eingabe *y*                                                                                              | [**schweben**](/windows/desktop/WinProg/windows-data-types)                        | gleiche Dimension(en) wie eingabe *y* |



 

## <a name="minimum-shader-model"></a>Shader-Mindestmodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                                                       | Unterstützt                   |
|------------------------------------------------------------------------------------|-----------------------------|
| [Shadermodell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) und höhere Shadermodelle | ja                         |
| [Shadermodell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | Ja (im Vergleich zu \_ \_ 1 1 und PS \_ 1 \_ 4) |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Systeminterne Funktionen (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

