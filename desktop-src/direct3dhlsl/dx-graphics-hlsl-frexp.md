---
title: frexp (Corecrt \_ math.h)
description: Gibt die Mantisse und den Exponenten des angegebenen Gleitkommawerts zurück.
ms.assetid: 9252feff-da85-4b3e-97db-1fcddd786695
keywords:
- frexp HLSL
topic_type:
- apiref
api_name:
- frexp
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f77ab30f525c37fcb2243bb6f634722420836f3893a4550edbb6604c8769773
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119276620"
---
# <a name="frexp"></a>frexp

Gibt die Mantisse und den Exponenten des angegebenen Gleitkommawerts zurück.



| *ret* frexp(*x*, *exp*) |
|-------------------------|



 

Der Rückgabewert ist die Mantisse, und der vom *exp-Parameter* zurückgegebene Wert ist der Exponent.

## <a name="parameters"></a>Parameter



| Element                                                         | BESCHREIBUNG                                                                                                                                      |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/>       | \[in \] Der angegebene Gleitkommawert. Wenn der *x-Parameter* 0 ist, gibt diese Funktion sowohl für die Mantisse als auch für den Exponenten 0 zurück.<br/> |
| <span id="exp"></span><span id="EXP"></span>*Exp*<br/> | \[out \] Der zurückgegebene Exponent des *x-Parameters.*<br/>                                                                                   |



 

## <a name="return-value"></a>Rückgabewert

Die Mantisse  des x-Parameters.

## <a name="type-description"></a>Typbeschreibung



| Name  | [**Vorlagentyp**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Komponententyp**](dx-graphics-hlsl-intrinsic-functions.md) | Size                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *x*   | [**Skalar,**](dx-graphics-hlsl-intrinsic-functions.md) **Vektor** oder **Matrix** | [**schweben**](/windows/desktop/WinProg/windows-data-types)                        | any                            |
| *exp* | identisch mit eingabe *x*                                                                                              | [**schweben**](/windows/desktop/WinProg/windows-data-types)                        | Gleiche Dimension(en) wie eingabe *x* |
| *Ret* | identisch mit eingabe *x*                                                                                              | [**schweben**](/windows/desktop/WinProg/windows-data-types)                        | Gleiche Dimension(en) wie eingabe *x* |



 

## <a name="minimum-shader-model"></a>Shader-Mindestmodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                                                       | Unterstützt           |
|------------------------------------------------------------------------------------|---------------------|
| [Shadermodell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) und höhere Shadermodelle | ja                 |
| [Shadermodell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md)                          | ja (nur ps \_ 2 \_ x) |
| [Shadermodell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | nein                  |



 

## <a name="remarks"></a>Bemerkungen

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------|--------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Corecrt \_ math.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Systeminterne Funktionen (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

