---
title: modf (Corecrt \_ math.h)
description: Teilt den Wert x in Bruch- und Ganzzahlteile auf, die jeweils das gleiche Vorzeichen wie x haben.
ms.assetid: 0cac1cf3-f0da-4b0a-ba30-4af5d65b04b2
keywords:
- modf HLSL
topic_type:
- apiref
api_name:
- modf
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7c09af44cb95f35854d4366c05d238423fcecaff7c9a10c3c55fadf6b51dd7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118513811"
---
# <a name="modf"></a>modf

Teilt den Wert x in Bruch- und Ganzzahlteile auf, die jeweils das gleiche Vorzeichen wie x haben.



| ret modf(x, out ip) |
|---------------------|



 

## <a name="parameters"></a>Parameter



| Element                                                      | Beschreibung                                    |
|-----------------------------------------------------------|------------------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/>    | \[in \] Der x-Eingabewert.<br/>           |
| <span id="ip"></span><span id="IP"></span>*Ip*<br/> | \[out \] Der ganzzahlige Teil von *x*.<br/> |



 

## <a name="return-value"></a>Rückgabewert

Der Teil x mit Vorzeichen und Bruchteil.

## <a name="type-description"></a>Typbeschreibung



| Name | Ein/Aus | [**Vorlagentyp**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Komponententyp**](dx-graphics-hlsl-intrinsic-functions.md)                 | Size                         |
|------|--------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|------------------------------|
| x    | in     | [**Skalar,**](dx-graphics-hlsl-intrinsic-functions.md) **Vektor** oder **Matrix** | [**float,**](/windows/desktop/WinProg/windows-data-types) [ **int**](/windows/desktop/WinProg/windows-data-types) | any                          |
| ip   | out    | identisch mit Eingabe x                                                                                                | [**float,**](/windows/desktop/WinProg/windows-data-types) [ **int**](/windows/desktop/WinProg/windows-data-types) | Gleiche Dimension(n) wie Eingabe x |
| Ret  | out    | identisch mit Eingabe x                                                                                                | [**float,**](/windows/desktop/WinProg/windows-data-types) [ **int**](/windows/desktop/WinProg/windows-data-types) | Gleiche Dimension(n) wie Eingabe x |



 

## <a name="minimum-shader-model"></a>Minimales Shadermodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                                                       | Unterstützt           |
|------------------------------------------------------------------------------------|---------------------|
| [Shadermodell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) und höhere Shadermodelle | Ja                 |
| [Shadermodell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | Ja (nur \_ im Vergleich \_ zu 1 1) |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|--------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Corecrt \_ math.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Systeminterne Funktionen (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

