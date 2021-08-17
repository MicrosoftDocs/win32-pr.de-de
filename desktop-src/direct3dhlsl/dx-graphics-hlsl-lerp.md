---
title: lerp
description: Führt eine lineare Interpolation aus.
ms.assetid: e369f182-b5bd-4b7f-aa77-9cfe11033bc4
keywords:
- lerp HLSL
topic_type:
- apiref
api_name:
- lerp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6981ef4134bbce17cbc7fa1e17de4d55de198572716ac39cbdd44b5e552e7f99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118791636"
---
# <a name="lerp"></a>lerp

Führt eine lineare Interpolation aus.



| *ret* lerp(*x*, *y*, *s*) |
|---------------------------|



 

## <a name="parameters"></a>Parameter



| Element                                                   | Beschreibung                                                                                           |
|--------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/> | \[in \] Der Wert des ersten Gleitkommawerts.<br/>                                                     |
| <span id="y"></span><span id="Y"></span>*Y*<br/> | \[in \] Der Wert des zweiten Gleitkommawerts.<br/>                                                    |
| <span id="s"></span><span id="S"></span>*s*<br/> | \[in \] Ein -Wert, der linear zwischen dem *x-Parameter* und dem *y-Parameter interpoliert.*<br/> |



 

## <a name="return-value"></a>Rückgabewert

Das Ergebnis der linearen Interpolation.

## <a name="type-description"></a>Typbeschreibung



| Name  | [**Vorlagentyp**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Komponententyp**](dx-graphics-hlsl-intrinsic-functions.md) | Size                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *x*   | [**Skalar,**](dx-graphics-hlsl-intrinsic-functions.md) **Vektor** oder **Matrix** | [**schweben**](/windows/desktop/WinProg/windows-data-types)                        | any                            |
| *y*   | identisch mit Eingabe *x*                                                                                              | [**schweben**](/windows/desktop/WinProg/windows-data-types)                        | Gleiche Dimension(n) wie Eingabe *x* |
| *s*   | identisch mit Eingabe *x*                                                                                              | [**schweben**](/windows/desktop/WinProg/windows-data-types)                        | Gleiche Dimension(n) wie Eingabe *x* |
| *Ret* | identisch mit Eingabe *x*                                                                                              | [**schweben**](/windows/desktop/WinProg/windows-data-types)                        | Gleiche Dimension(n) wie Eingabe *x* |



 

## <a name="remarks"></a>Hinweise

Die lineare Interpolation basiert auf der folgenden Formel: x (1 s) + y s, die entsprechend als \* \* x + s(y-x) geschrieben werden können.

## <a name="minimum-shader-model"></a>Minimales Shadermodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                                                       | Unterstützt                   |
|------------------------------------------------------------------------------------|-----------------------------|
| [Shadermodell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) und höhere Shadermodelle | Ja                         |
| [Shadermodell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | Ja (im Vergleich \_ zu 1 \_ 1 und ps \_ 1 \_ 1) |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Systeminterne Funktionen (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

