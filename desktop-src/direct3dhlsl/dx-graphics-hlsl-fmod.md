---
title: "\"f\" (corecrt \\_ Math. h)"
description: Gibt den Gleit Komma Rest von x/y zurück.
ms.assetid: bb940548-c4c5-4109-a488-4ea7295c7213
keywords:
- f/a-HLSL
topic_type:
- apiref
api_name:
- fmod
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9dc4367e3aa80484098e88926567953fc8e9a90
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354737"
---
# <a name="fmod"></a>fmod

Gibt den Gleit Komma Rest von x/y zurück.



| *ret* f (*x*, *y*) |
|----------------------|



 

## <a name="parameters"></a>Parameter



| Element                                                   | BESCHREIBUNG                                    |
|--------------------------------------------------------|------------------------------------------------|
| <span id="x"></span><span id="X"></span>*Stuben*<br/> | \[in \] der Gleit Komma-Dividende.<br/> |
| <span id="y"></span><span id="Y"></span>*Teenie*<br/> | \[im Gleit \] Komma Trennzeichen.<br/>  |



 

## <a name="return-value"></a>Rückgabewert

Der Gleit Komma Rest des *x* -Parameters, dividiert durch den *y* -Parameter.

## <a name="remarks"></a>Bemerkungen

Der Gleit Komma Rest wird so berechnet, dass x = i \* y + f, wobei es sich um eine ganze Zahl handelt, f dasselbe Vorzeichen wie x hat und der absolute Wert von f kleiner ist als der absolute Wert von y.

## <a name="type-description"></a>Typbeschreibung



| Name  | [**Vorlagentyp**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Komponententyp**](dx-graphics-hlsl-intrinsic-functions.md) | Size                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *x*   | [**Skalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vektor** oder **Matrix** | [**Hafen**](/windows/desktop/WinProg/windows-data-types)                        | any                            |
| *y*   | identisch mit Eingabe *x*                                                                                              | [**Hafen**](/windows/desktop/WinProg/windows-data-types)                        | gleiche Dimension (n) wie Eingabe *x* |
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

 

