---
title: asfloat
description: Interpretiert das Bitmuster von x als Gleitkommazahl.
ms.assetid: 48e1e0cb-8578-4e6d-8c46-2b8b201906c1
keywords:
- asfloat HLSL
topic_type:
- apiref
api_name:
- asfloat
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d85f6010a8c82f8ae66d5fa56a979a9e946316a5e2737fe2c7257570499055d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119043848"
---
# <a name="asfloat"></a>asfloat

Interpretiert das Bitmuster von *x* als Gleitkommazahl.



| ret asfloat(*x*) |
|------------------|



 

## <a name="parameters"></a>Parameter



| Element                                                   | Beschreibung                        |
|--------------------------------------------------------|------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/> | \[in \] Der Eingabewert.<br/> |



 

## <a name="return-value"></a>Rückgabewert

Die Als Gleitkommazahl interpretierte Eingabe.

## <a name="type-description"></a>Typbeschreibung



| Name  | [**Vorlagentyp**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Komponententyp**](dx-graphics-hlsl-intrinsic-functions.md)                                                         | Size                           |
|-------|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| *x*   | [**Skalar,**](dx-graphics-hlsl-intrinsic-functions.md) **Vektor** oder **Matrix** | [**float,**](/windows/desktop/WinProg/windows-data-types) [**int,**](/windows/desktop/WinProg/windows-data-types) [**uint**](/windows/desktop/WinProg/windows-data-types) | any                            |
| *Ret* | identisch mit eingabe *x*                                                                                              | [**schweben**](/windows/desktop/WinProg/windows-data-types)                                                                                | Gleiche Dimension(en) wie eingabe *x* |



 

## <a name="function-overloads"></a>Funktionsüberladungen

<dl> 'float <x> asfloat(float <x> value); `  
` float <x> asfloat(int <x> value); `  
` float <x> asfloat(uint <x> value);'
</dl>

## <a name="minimum-shader-model"></a>Shader-Mindestmodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                                        | Unterstützt |
|---------------------------------------------------------------------|-----------|
| [Shadermodell 4](dx-graphics-hlsl-sm4.md) und höhere Shadermodelle | Ja       |
| [Shadermodell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md)           | Nein        |
| [Shadermodell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md)           | Nein        |
| [Shadermodell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)           | Nein        |



 

## <a name="remarks"></a>Hinweise

Ältere Compiler haben fälschlicherweise `asfloat(bool)` zugelassen, aber beachten Sie, dass bool-Eingaben nicht unterstützt werden.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Systeminterne Funktionen (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

