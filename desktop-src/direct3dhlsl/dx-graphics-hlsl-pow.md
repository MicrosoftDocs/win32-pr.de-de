---
title: pow
description: Gibt den angegebenen Wert zurück, der mit der angegebenen Leistung ausgelöst wird.
ms.assetid: 1d64452c-81c7-4ef5-a332-13e0263c2cd1
keywords:
- pow HLSL
topic_type:
- apiref
api_name:
- pow
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a9d26e150d611df12f2e042d2e20c06ab82172bbc3d2f241ee1ce3a4725f1193
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119120074"
---
# <a name="pow"></a>pow

Gibt den angegebenen Wert zurück, der mit der angegebenen Leistung ausgelöst wird.



| *ret* pow(*x*, *y*) |
|---------------------|



 

## <a name="parameters"></a>Parameter



| Element                                                   | Beschreibung                            |
|--------------------------------------------------------|----------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/> | \[in \] Der angegebene Wert.<br/> |
| <span id="y"></span><span id="Y"></span>*Y*<br/> | \[in \] Die angegebene Energie.<br/> |



 

## <a name="return-value"></a>Rückgabewert

Der  x-Parameter, der mit dem *y-Parameter ausgelöst* wird.

## <a name="remarks"></a>Hinweise

Die **systeminterne** FUNKTION pow HLSL berechnet *x*<sup>y.</sup>



| X      | Y      | Ergebnis                                                                      |
|--------|--------|-----------------------------------------------------------------------------|
| < 0 | any    | NAN                                                                         |
| > 0 | == 0   | 1                                                                           |
| == 0   | > 0 | 0                                                                           |
| == 0   | < 0 | Inf                                                                         |
| > 0 | < 0 | 1/X<sup>-Y</sup>                                                            |
| == 0   | == 0   | Abhängig vom jeweiligen Grafikprozessor<br/> 0, 1 oder NAN<br/> |



 

## <a name="type-description"></a>Typbeschreibung



| Name  | [**Vorlagentyp**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Komponententyp**](dx-graphics-hlsl-intrinsic-functions.md) | Size                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *x*   | [**Skalar,**](dx-graphics-hlsl-intrinsic-functions.md) **Vektor** oder **Matrix** | [**schweben**](/windows/desktop/WinProg/windows-data-types)                        | any                            |
| *y*   | identisch mit Eingabe *x*                                                                                              | [**schweben**](/windows/desktop/WinProg/windows-data-types)                        | Gleiche Dimension(n) wie Eingabe *x* |
| *Ret* | identisch mit Eingabe *x*                                                                                              | [**schweben**](/windows/desktop/WinProg/windows-data-types)                        | Gleiche Dimension(n) wie Eingabe *x* |



 

## <a name="minimum-shader-model"></a>Minimales Shadermodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                                                       | Unterstützt           |
|------------------------------------------------------------------------------------|---------------------|
| [Shadermodell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) und höhere Shadermodelle | Ja                 |
| [Shadermodell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | Ja (nur \_ im Vergleich \_ zu 1 1) |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Systeminterne Funktionen (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

