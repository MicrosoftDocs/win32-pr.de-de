---
title: atan2 (Corecrt \_ math.h)
description: Gibt den Arangens von zwei Werten (x,y) zurück.
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
ms.openlocfilehash: 2932f82cf6d9e8b2071446b63f84e60727aff2da2213461d3c1194b2811fe1a9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854970"
---
# <a name="atan2"></a>atan2

Gibt den Arangens von zwei Werten (x,y) zurück.



| *ret* atan2(*y*, *x*) |
|-----------------------|



 

## <a name="parameters"></a>Parameter



| Element                                                   | Beschreibung                    |
|--------------------------------------------------------|--------------------------------|
| <span id="y"></span><span id="Y"></span>*Y*<br/> | \[in \] Der y-Wert.<br/> |
| <span id="x"></span><span id="X"></span>*X*<br/> | \[in \] Der x-Wert.<br/> |



 

## <a name="return-value"></a>Rückgabewert

Der Arangens von (y,x).

## <a name="remarks"></a>Hinweise

Die Vorzeichen der *x-* und *y-Parameter* werden verwendet, um den Quadranten der Rückgabewerte im Bereich von -π zu π zu bestimmen. Die systeminterne **ATAN2** HLSL-Funktion ist für jeden anderen Punkt als den Ursprung gut definiert, auch wenn *y* gleich 0 und *x* nicht gleich 0 ist.

## <a name="type-description"></a>Typbeschreibung



| Name  | [**Vorlagentyp**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Komponententyp**](dx-graphics-hlsl-intrinsic-functions.md) | Size                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *y*   | identisch mit eingabe *x*                                                                                              | [**schweben**](/windows/desktop/WinProg/windows-data-types)                        | Gleiche Dimension(en) wie eingabe *x* |
| *x*   | [**Skalar,**](dx-graphics-hlsl-intrinsic-functions.md) **Vektor** oder **Matrix** | [**schweben**](/windows/desktop/WinProg/windows-data-types)                        | any                            |
| *Ret* | identisch mit eingabe *x*                                                                                              | [**schweben**](/windows/desktop/WinProg/windows-data-types)                        | Gleiche Dimension(en) wie eingabe *x* |



 

## <a name="minimum-shader-model"></a>Shader-Mindestmodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                                                       | Unterstützt |
|------------------------------------------------------------------------------------|-----------|
| [Shadermodell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) und höhere Shadermodelle | Ja       |
| [Shadermodell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | Vs \_ 1 \_ 1  |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|--------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Corecrt \_ math.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Systeminterne Funktionen (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

