---
title: atan2 (corecrt \_ Math. h)
description: Gibt den Arkus Tangens von zwei Werten (x, y) zurück.
ms.assetid: e7b53751-f321-4390-8f8f-ec1fa3aaa798
keywords:
- atan2 HLSL
topic_type:
- apiref
api_name:
- atan2
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52fbc6574d0fc0d53a165ae7da87c2627a295be4
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104219504"
---
# <a name="atan2"></a>atan2

Gibt den Arkus Tangens von zwei Werten (x, y) zurück.



| *ret* atan2 (*y*, *x*) |
|-----------------------|



 

## <a name="parameters"></a>Parameter



| Element                                                   | BESCHREIBUNG                    |
|--------------------------------------------------------|--------------------------------|
| <span id="y"></span><span id="Y"></span>*Teenie*<br/> | \[im \] y-Wert.<br/> |
| <span id="x"></span><span id="X"></span>*Stuben*<br/> | \[im \] x-Wert.<br/> |



 

## <a name="return-value"></a>Rückgabewert

Der Arkus Tangens von (y, x).

## <a name="remarks"></a>Bemerkungen

Die Vorzeichen der *x* -und *y* -Parameter werden verwendet, um den Quadranten der Rückgabewerte innerhalb des Bereichs von bis Adressierung zu bestimmen. Die intrinsische Funktion **atan2** HLSL ist für jeden anderen Punkt als den Ursprung klar definiert, auch wenn *y* gleich 0 und *x* nicht gleich 0 ist.

## <a name="type-description"></a>Typbeschreibung



| Name  | [**Vorlagentyp**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Komponententyp**](dx-graphics-hlsl-intrinsic-functions.md) | Size                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *y*   | identisch mit Eingabe *x*                                                                                              | [**Hafen**](/windows/desktop/WinProg/windows-data-types)                        | gleiche Dimension (n) wie Eingabe *x* |
| *x*   | [**Skalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vektor** oder **Matrix** | [**Hafen**](/windows/desktop/WinProg/windows-data-types)                        | any                            |
| *TZI* | identisch mit Eingabe *x*                                                                                              | [**Hafen**](/windows/desktop/WinProg/windows-data-types)                        | gleiche Dimension (n) wie Eingabe *x* |



 

## <a name="minimum-shader-model"></a>Minimaler Shader-Modell

Diese Funktion wird in den folgenden shadermodellen unterstützt.



| Shadermodell                                                                       | Unterstützt |
|------------------------------------------------------------------------------------|-----------|
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) und höhere Shader-Modelle | ja       |
| [Shader-Modell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | vs \_ 1 \_ 1  |



 

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------|--------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Corecrt \_ Math. h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Intrinsische Funktionen (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

