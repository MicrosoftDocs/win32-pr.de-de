---
title: trunc (corecrt \_ Math. h)
description: Kürzen eines Gleit Komma Werts in die ganzzahlige Komponente.
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
ms.openlocfilehash: 34493f60e60bc0dce35f5f9db50360265191c742
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104995944"
---
# <a name="trunc"></a>trunc

Kürzen eines Gleit Komma Werts in die ganzzahlige Komponente.



| Ret trunc (*x*) |
|----------------|



 

## <a name="parameters"></a>Parameter



| Element                                                   | BESCHREIBUNG                            |
|--------------------------------------------------------|----------------------------------------|
| <span id="x"></span><span id="X"></span>*Stuben*<br/> | \[in \] der angegebenen Eingabe.<br/> |



 

## <a name="return-value"></a>Rückgabewert

Der Eingabe Wert, der auf eine ganzzahlige Komponente gekürzt wird.

## <a name="remarks"></a>Bemerkungen

Diese Funktion verkürzt einen Gleit Komma Wert auf die ganzzahlige Komponente. Wenn ein Gleit Komma Wert von 1,6 ist, würde die trunc-Funktion 1,0 zurückgeben, wobei der Wert der Round-Funktion [**(DirectX HLSL)**](dx-graphics-hlsl-round.md) 2,0 zurückgeben würde.

## <a name="type-description"></a>Typbeschreibung



| Name | [**Vorlagentyp**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Komponententyp**](dx-graphics-hlsl-intrinsic-functions.md) | Size                         |
|------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|------------------------------|
| *x*  | [**Skalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vektor** oder **Matrix** | [**Hafen**](/windows/desktop/WinProg/windows-data-types)                        | any                          |
| TZI  | Gleicher Typ wie Eingabe x                                                                                           | [**Hafen**](/windows/desktop/WinProg/windows-data-types)                        | Gleiche Dimension (n) wie Eingabe x |



 

## <a name="minimum-shader-model"></a>Minimaler Shader-Modell

Diese Funktion wird in den folgenden shadermodellen unterstützt.



| Shadermodell                                                                       | Unterstützt |
|------------------------------------------------------------------------------------|-----------|
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) und höhere Shader-Modelle | ja       |



 

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------|--------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Corecrt \_ Math. h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Intrinsische Funktionen (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

