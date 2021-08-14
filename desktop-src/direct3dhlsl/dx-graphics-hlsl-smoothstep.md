---
title: smoothstep
description: Gibt eine reibungslose Ermite-Interpolation zwischen 0 und 1 zurück, wenn x sich im Bereich \min, max\ befindet.
ms.assetid: 6a879d82-f5ab-4e9b-bc9c-8988cbe6aa82
keywords:
- smoothstep HLSL
topic_type:
- apiref
api_name:
- smoothstep
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5416dab57fc77f7b664518afcb0f4623875fd2a660f7d1aff82ab42f2c297b22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118513795"
---
# <a name="smoothstep"></a>smoothstep

Gibt eine nahtlose Eremite-Interpolation zwischen 0 und 1 zurück, wenn *x* im Bereich \[ *min*, *max.* \] liegt.



| *ret* smoothstep(*min*, *max*, *x*) |
|-------------------------------------|



 

## <a name="parameters"></a>Parameter



| Element                                                         | BESCHREIBUNG                                               |
|--------------------------------------------------------------|-----------------------------------------------------------|
| <span id="min"></span><span id="MIN"></span>*Min*<br/> | \[in \] Der mindeste Bereich des *x-Parameters.*<br/> |
| <span id="max"></span><span id="MAX"></span>*Max*<br/> | \[in \] Der maximale Bereich des *x-Parameters.*<br/> |
| <span id="x"></span><span id="X"></span>*X*<br/>       | \[in \] Der angegebene Wert, der interpoliert werden soll.<br/> |



 

## <a name="return-value"></a>Rückgabewert

Gibt 0 zurück, wenn *x* kleiner als *min* ist. 1, wenn *x* größer als *max* ist; Andernfalls ein Wert zwischen 0 und 1, wenn *x* im Bereich \[ *min*, *max.* \] liegt.

## <a name="remarks"></a>Hinweise

Verwenden Sie die intrinsische HLSL-Funktion **smoothstep,** um einen reibungslosen Übergang zwischen zwei Werten zu erstellen. Beispielsweise können Sie diese Funktion verwenden, um zwei Farben reibungslos zu mischen.

## <a name="type-description"></a>Typbeschreibung



| Name  | [**Vorlagentyp**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Komponententyp**](dx-graphics-hlsl-intrinsic-functions.md) | Size                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *x*   | [**Skalar,**](dx-graphics-hlsl-intrinsic-functions.md) **Vektor** oder **Matrix** | [**schweben**](/windows/desktop/WinProg/windows-data-types)                        | any                            |
| *min* | identisch mit eingabe *x*                                                                                              | [**schweben**](/windows/desktop/WinProg/windows-data-types)                        | Gleiche Dimension(en) wie eingabe *x* |
| *max* | identisch mit eingabe *x*                                                                                              | [**schweben**](/windows/desktop/WinProg/windows-data-types)                        | Gleiche Dimension(en) wie eingabe *x* |
| *Ret* | identisch mit eingabe *x*                                                                                              | [**schweben**](/windows/desktop/WinProg/windows-data-types)                        | Gleiche Dimension(en) wie eingabe *x* |



 

## <a name="minimum-shader-model"></a>Shader-Mindestmodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                                                       | Unterstützt           |
|------------------------------------------------------------------------------------|---------------------|
| [Shadermodell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) und höhere Shadermodelle | ja                 |
| [Shadermodell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | ja (im Vergleich \_ \_ zu nur 1 1) |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Systeminterne Funktionen (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

