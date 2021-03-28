---
title: frexp (corecrt \_ Math. h)
description: Gibt die Mantisse und den Exponenten des angegebenen Gleit Komma Werts zurück.
ms.assetid: 9252feff-da85-4b3e-97db-1fcddd786695
keywords:
- frexp HLSL
topic_type:
- apiref
api_name:
- frexp
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bddbcbbf9e97aff739bb06a0f0d0ddac12134463
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961596"
---
# <a name="frexp"></a>frexp

Gibt die Mantisse und den Exponenten des angegebenen Gleit Komma Werts zurück.



| *ret* frexp (*x*, *Exp*) |
|-------------------------|



 

Der Rückgabewert ist die Mantisse, und der vom *Exp* -Parameter zurückgegebene Wert ist der Exponent.

## <a name="parameters"></a>Parameter



| Element                                                         | BESCHREIBUNG                                                                                                                                      |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="x"></span><span id="X"></span>*Stuben*<br/>       | \[im \] angegebenen Gleit Komma Wert. Wenn der *x* -Parameter 0 (null) ist, gibt diese Funktion für die Mantisse und den Exponenten 0 zurück.<br/> |
| <span id="exp"></span><span id="EXP"></span>*Exp*<br/> | \[\]der zurückgegebene Exponent des *x* -Parameters.<br/>                                                                                   |



 

## <a name="return-value"></a>Rückgabewert

Die Mantisse des *x* -Parameters.

## <a name="type-description"></a>Typbeschreibung



| Name  | [**Vorlagentyp**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Komponententyp**](dx-graphics-hlsl-intrinsic-functions.md) | Size                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *x*   | [**Skalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vektor** oder **Matrix** | [**Hafen**](/windows/desktop/WinProg/windows-data-types)                        | any                            |
| *exp* | identisch mit Eingabe *x*                                                                                              | [**Hafen**](/windows/desktop/WinProg/windows-data-types)                        | gleiche Dimension (n) wie Eingabe *x* |
| *TZI* | identisch mit Eingabe *x*                                                                                              | [**Hafen**](/windows/desktop/WinProg/windows-data-types)                        | gleiche Dimension (n) wie Eingabe *x* |



 

## <a name="minimum-shader-model"></a>Minimaler Shader-Modell

Diese Funktion wird in den folgenden shadermodellen unterstützt.



| Shadermodell                                                                       | Unterstützt           |
|------------------------------------------------------------------------------------|---------------------|
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) und höhere Shader-Modelle | ja                 |
| [Shader-Modell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md)                          | Ja ( \_ nur PS 2 \_ x) |
| [Shader-Modell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | nein                  |



 

## <a name="remarks"></a>Bemerkungen

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------|--------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Corecrt \_ Math. h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Intrinsische Funktionen (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

