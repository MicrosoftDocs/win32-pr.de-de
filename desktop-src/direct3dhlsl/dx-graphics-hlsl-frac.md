---
title: Frac
description: Gibt den Bruchteil (oder Dezimalteil) von x zurück. , die größer oder gleich 0 und kleiner als 1 ist.
ms.assetid: 4e85390f-2b1a-402b-b932-09b80097f7e6
keywords:
- frac HLSL
topic_type:
- apiref
api_name:
- frac
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: acc2553a59509ab6a8ad4c1ed5ec11df8c775763963a77f60c074bdf43d389f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117726258"
---
# <a name="frac"></a>Frac

Gibt den Bruchteil (oder Dezimalteil) von x zurück. , die größer oder gleich 0 und kleiner als 1 ist.

Siehe auch [trunc](./dx-graphics-hlsl-trunc.md).

| *ret* frac(*x*) |
|-----------------|



 

## <a name="parameters"></a>Parameter



| Element                                                   | Beschreibung                            |
|--------------------------------------------------------|----------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/> | \[in \] Der angegebene Wert.<br/> |



 

## <a name="return-value"></a>Rückgabewert

Der Bruchteil des *x-Parameters.*

## <a name="type-description"></a>Typbeschreibung



| Name  | [**Vorlagentyp**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Komponententyp**](dx-graphics-hlsl-intrinsic-functions.md) | Size                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *x*   | [**Skalar,**](dx-graphics-hlsl-intrinsic-functions.md) **Vektor** oder **Matrix** | [**schweben**](/windows/desktop/WinProg/windows-data-types)                        | any                            |
| *Ret* | identisch mit Eingabe *x*                                                                                              | [**schweben**](/windows/desktop/WinProg/windows-data-types)                        | Gleiche Dimension(n) wie Eingabe *x* |



 

## <a name="minimum-shader-model"></a>Minimales Shadermodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                                                       | Unterstützt |
|------------------------------------------------------------------------------------|-----------|
| [Shadermodell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) und höhere Shadermodelle | Ja       |
| [Shadermodell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | vs \_ 1 \_ 1  |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Systeminterne Funktionen (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

