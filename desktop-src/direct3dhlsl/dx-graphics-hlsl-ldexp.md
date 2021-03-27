---
title: LDE XP (corecrt \_ Math. h)
description: Gibt das Ergebnis der Multiplikation des angegebenen Werts mit zwei Werten zurück, die auf die Potenz des angegebenen Exponenten zurückzuführen sind.
ms.assetid: 6d6fee96-f952-4058-a1ac-3abb98dbd540
keywords:
- LDE XP HLSL
topic_type:
- apiref
api_name:
- ldexp
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 731cb5cbf933ea3f8754a7d70b9ef0b7a54e783b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103870139"
---
# <a name="ldexp"></a>ldexp

Gibt das Ergebnis der Multiplikation des angegebenen Werts mit zwei Werten zurück, die auf die Potenz des angegebenen Exponenten zurückzuführen sind.



| *ret* LDE XP (*x*, *Exp*) |
|-------------------------|



 

Diese Funktion verwendet die folgende Formel: *x* \* 2 <sup>Exp</sup>

## <a name="parameters"></a>Parameter



| Element                                                         | BESCHREIBUNG                               |
|--------------------------------------------------------------|-------------------------------------------|
| <span id="x"></span><span id="X"></span>*Stuben*<br/>       | \[im \] angegebenen Wert.<br/>    |
| <span id="exp"></span><span id="EXP"></span>*Exp*<br/> | \[im \] angegebenen Exponenten.<br/> |



 

## <a name="return-value"></a>Rückgabewert

Das Ergebnis der Multiplikation des *x* -Parameters mit zwei Werten, die durch den *Exp* -Parameter ausgelöst werden.

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
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) und höhere Shader-Modelle | ja                 |
| [Shader-Modell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | Ja ( \_ nur vs 1 \_ 1) |



 

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------|--------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Corecrt \_ Math. h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Intrinsische Funktionen (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

