---
title: fwidth
description: Gibt den absoluten Wert der partiellen Ableitungen des angegebenen Werts zurück.
ms.assetid: 7184c3b4-1720-4176-a494-7f73322a918e
keywords:
- fwidth HLSL
topic_type:
- apiref
api_name:
- fwidth
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: feee9a017664e71c9c96f19fda5106870c04b947dc2b668e67f376626f7ea38a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119120174"
---
# <a name="fwidth"></a>fwidth

Gibt den absoluten Wert der partiellen Ableitungen des angegebenen Werts zurück.



| *ret* fwidth(*x*) |
|-------------------|



 

Diese Funktion berechnet Folgendes: [**abs**](dx-graphics-hlsl-abs.md)([**ddx**](dx-graphics-hlsl-ddx.md)(*x*)) + [**abs**](dx-graphics-hlsl-abs.md)([**ddy**](dx-graphics-hlsl-ddy.md)(*x*)).

Diese Funktion wird nur in Pixel-Shadern unterstützt.

## <a name="parameters"></a>Parameter



| Element                                                   | Beschreibung                            |
|--------------------------------------------------------|----------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/> | \[in \] Der angegebene Wert.<br/> |



 

## <a name="return-value"></a>Rückgabewert

Der absolute Wert der partiellen Ableitungen des *x-Parameters.*

## <a name="type-description"></a>Typbeschreibung



| Name  | [**Vorlagentyp**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Komponententyp**](dx-graphics-hlsl-intrinsic-functions.md) | Size                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *x*   | [**Skalar,**](dx-graphics-hlsl-intrinsic-functions.md) **Vektor** oder **Matrix** | [**schweben**](/windows/desktop/WinProg/windows-data-types)                        | any                            |
| *Ret* | identisch mit Eingabe *x*                                                                                              | [**schweben**](/windows/desktop/WinProg/windows-data-types)                        | Gleiche Dimension(n) wie Eingabe *x* |



 

## <a name="minimum-shader-model"></a>Minimales Shadermodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                                                       | Unterstützt           |
|------------------------------------------------------------------------------------|---------------------|
| [Shadermodell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) und höhere Shadermodelle | Ja                 |
| [Shadermodell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md)                          | Ja (nur ps \_ 2 \_ x) |
| [Shadermodell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | Nein                  |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Systeminterne Funktionen (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

