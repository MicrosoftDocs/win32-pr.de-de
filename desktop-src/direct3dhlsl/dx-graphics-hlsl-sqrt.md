---
title: sqrt
description: Gibt die Quadratwurzel des angegebenen Gleitkommawerts pro Komponente zurück.
ms.assetid: e8debc60-1441-4974-9ab3-6d1c2217caaf
keywords:
- sqrt HLSL
topic_type:
- apiref
api_name:
- sqrt
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6550906c50c44dba5ab28b6327c86a6bb94560e7ad3d9921b6e9d37eb35236de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117725840"
---
# <a name="sqrt"></a>sqrt

Gibt die Quadratwurzel des angegebenen Gleitkommawerts pro Komponente zurück.



| *ret* sqrt(*x*) |
|-----------------|



 

## <a name="parameters"></a>Parameter



| Element                                                   | Beschreibung                                           |
|--------------------------------------------------------|-------------------------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/> | \[in \] Der angegebene Gleitkommawert.<br/> |



 

## <a name="return-value"></a>Rückgabewert

Die Quadratwurzel des *x-Parameters* pro Komponente.

## <a name="type-description"></a>Typbeschreibung



| Name  | [**Vorlagentyp**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Komponententyp**](dx-graphics-hlsl-intrinsic-functions.md) | Size                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *x*   | [**Skalar,**](dx-graphics-hlsl-intrinsic-functions.md) **Vektor** oder **Matrix** | [**schweben**](/windows/desktop/WinProg/windows-data-types)                        | any                            |
| *Ret* | identisch mit eingabe *x*                                                                                              | [**schweben**](/windows/desktop/WinProg/windows-data-types)                        | Gleiche Dimension(en) wie eingabe *x* |



 

## <a name="minimum-shader-model"></a>Shader-Mindestmodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                                                       | Unterstützt           |
|------------------------------------------------------------------------------------|---------------------|
| [Shadermodell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) und höhere Shadermodelle | Ja                 |
| [Shadermodell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | ja (im Vergleich \_ \_ zu nur 1 1) |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Systeminterne Funktionen (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

