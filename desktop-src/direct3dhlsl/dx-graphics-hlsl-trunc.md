---
title: trunc (Corecrt \_ math.h)
description: Schneidt einen Gleitkommawert auf die ganzzahlige Komponente ab.
ms.assetid: a0978fa2-71f8-4257-8c90-96224c2ec953
keywords:
- trunc HLSL
topic_type:
- apiref
api_name:
- trunc
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0845e619e8674d729735da1b639802df256d9c210615d71578a4e1effd777e39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119845770"
---
# <a name="trunc"></a>trunc

Schneidt einen Gleitkommawert auf die ganzzahlige Komponente ab.



| ret trunc(*x*) |
|----------------|



 

## <a name="parameters"></a>Parameter



| Element                                                   | BESCHREIBUNG                            |
|--------------------------------------------------------|----------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/> | \[in \] Die angegebene Eingabe.<br/> |



 

## <a name="return-value"></a>Rückgabewert

Der Eingabewert, der auf eine ganzzahlige Komponente gekürzt wurde.

## <a name="remarks"></a>Hinweise

Diese Funktion schneide einen Gleitkommawert auf die ganzzahlige Komponente ab. Bei einem Gleitkommawert von 1,6 würde die trunc-Funktion 1,0 zurückgeben, wobei die [**round-Funktion (DirectX HLSL)**](dx-graphics-hlsl-round.md) 2,0 zurückgeben würde.

## <a name="type-description"></a>Typbeschreibung



| Name | [**Vorlagentyp**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Komponententyp**](dx-graphics-hlsl-intrinsic-functions.md) | Size                         |
|------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|------------------------------|
| *x*  | [**Skalar,**](dx-graphics-hlsl-intrinsic-functions.md) **Vektor** oder **Matrix** | [**schweben**](/windows/desktop/WinProg/windows-data-types)                        | any                          |
| Ret  | Identischer Typ wie Eingabe x                                                                                           | [**schweben**](/windows/desktop/WinProg/windows-data-types)                        | Gleiche Dimension(n) wie Eingabe x |



 

## <a name="minimum-shader-model"></a>Minimales Shadermodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                                                       | Unterstützt |
|------------------------------------------------------------------------------------|-----------|
| [Shadermodell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) und höhere Shadermodelle | Ja       |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|--------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Corecrt \_ math.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Systeminterne Funktionen (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

