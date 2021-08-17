---
title: LOG10
description: Gibt den Logarithmus der Basis 10 des angegebenen Werts zurück.
ms.assetid: a94f8438-8153-4a31-bde3-98831edf99e5
keywords:
- log10 HLSL
topic_type:
- apiref
api_name:
- log10
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1a0a6aa00037fcf93df39dc40f694f0460878121c9c8f962e4cc28ba0b4a0a94
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118791545"
---
# <a name="log10"></a>LOG10

Gibt den Logarithmus der Basis 10 des angegebenen Werts zurück.



| *ret* log10(*x*) |
|------------------|



 

## <a name="parameters"></a>Parameter



| Element                                                   | BESCHREIBUNG                            |
|--------------------------------------------------------|----------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/> | \[in \] Der angegebene Wert.<br/> |



 

## <a name="return-value"></a>Rückgabewert

Der Logarithmus der Basis 10 des *x-Parameters.* Wenn der *x-Parameter* negativ ist, gibt diese Funktion einen unbestimmten Wert zurück. Wenn das *x* 0 ist, gibt diese Funktion -INF zurück.

## <a name="type-description"></a>Typbeschreibung



| Name  | [**Vorlagentyp**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Komponententyp**](dx-graphics-hlsl-intrinsic-functions.md) | Size                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *x*   | [**Skalar,**](dx-graphics-hlsl-intrinsic-functions.md) **Vektor** oder **Matrix** | [**schweben**](/windows/desktop/WinProg/windows-data-types)                        | any                            |
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

 

