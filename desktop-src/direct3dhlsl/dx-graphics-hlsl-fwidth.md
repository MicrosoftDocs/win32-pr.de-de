---
title: Breite
description: Gibt den absoluten Wert der partiellen Ableitungen des angegebenen-Werts zurück.
ms.assetid: 7184c3b4-1720-4176-a494-7f73322a918e
keywords:
- Breite von HLSL
topic_type:
- apiref
api_name:
- fwidth
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cf2d5a34e1f387aadb3b044ddd1264616a61109b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104102046"
---
# <a name="fwidth"></a>Breite

Gibt den absoluten Wert der partiellen Ableitungen des angegebenen-Werts zurück.



| *ret* -Breite (*x*) |
|-------------------|



 

Diese Funktion berechnet Folgendes: [**ABS**](dx-graphics-hlsl-abs.md)([**DDX**](dx-graphics-hlsl-ddx.md)(*x*)) + [**ABS**](dx-graphics-hlsl-abs.md)([**ddY**](dx-graphics-hlsl-ddy.md)(*x*)).

Diese Funktion wird nur in Pixel-Shadern unterstützt.

## <a name="parameters"></a>Parameter



| Element                                                   | BESCHREIBUNG                            |
|--------------------------------------------------------|----------------------------------------|
| <span id="x"></span><span id="X"></span>*Stuben*<br/> | \[im \] angegebenen Wert.<br/> |



 

## <a name="return-value"></a>Rückgabewert

Der absolute Wert der partiellen Ableitungen des *x* -Parameters.

## <a name="type-description"></a>Typbeschreibung



| Name  | [**Vorlagentyp**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Komponententyp**](dx-graphics-hlsl-intrinsic-functions.md) | Size                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *x*   | [**Skalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vektor** oder **Matrix** | [**Hafen**](/windows/desktop/WinProg/windows-data-types)                        | any                            |
| *TZI* | identisch mit Eingabe *x*                                                                                              | [**Hafen**](/windows/desktop/WinProg/windows-data-types)                        | gleiche Dimension (n) wie Eingabe *x* |



 

## <a name="minimum-shader-model"></a>Minimaler Shader-Modell

Diese Funktion wird in den folgenden shadermodellen unterstützt.



| Shadermodell                                                                       | Unterstützt           |
|------------------------------------------------------------------------------------|---------------------|
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) und höhere Shader-Modelle | ja                 |
| [Shader-Modell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md)                          | Ja ( \_ nur PS 2 \_ x) |
| [Shader-Modell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | Nein                  |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Intrinsische Funktionen (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

