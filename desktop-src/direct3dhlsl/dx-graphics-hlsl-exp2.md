---
title: exp2 (corecrt \_ Math. h)
description: Gibt den Exponentialwert 2 oder den 2X-Wert des angegebenen-Werts zurück.
ms.assetid: 68b0057c-864d-440b-84f6-781d5fa3b019
keywords:
- exp2 HLSL
topic_type:
- apiref
api_name:
- exp2
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63aaf5ee7c29da49ca2e7b21d80af6967721058d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982186"
---
# <a name="exp2"></a>exp2

Gibt den Exponentialwert 2 oder 2<sup>x</sup>des angegebenen-Werts zurück.



| *ret* exp2 (*x*) |
|-----------------|



 

## <a name="parameters"></a>Parameter



| Element                                                   | BESCHREIBUNG                                           |
|--------------------------------------------------------|-------------------------------------------------------|
| <span id="x"></span><span id="X"></span>*Stuben*<br/> | \[im \] angegebenen Gleit Komma Wert.<br/> |



 

## <a name="return-value"></a>Rückgabewert

Die exponentialbasis 2 des *x* -Parameters.

## <a name="type-description"></a>Typbeschreibung



| Name  | [**Vorlagentyp**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Komponententyp**](dx-graphics-hlsl-intrinsic-functions.md) | Size                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
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

 

