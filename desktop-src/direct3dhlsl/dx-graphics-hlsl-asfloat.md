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
ms.openlocfilehash: 901b64099547060305bab6db43cbe75b3fdb8d9c
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886266"
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
| *Ret* | identisch mit eingabe *x*                                                                                              | [**float**](/windows/desktop/WinProg/windows-data-types)                                                                                | Gleiche Dimension(en) wie eingabe *x* |



 

## <a name="function-overloads"></a>Funktionsüberladungen

<dl> `float&lt;x&gt; asfloat(float&lt;x&gt; value);`  
`float&lt;x&gt; asfloat(int&lt;x&gt; value);`  
`float&lt;x&gt; asfloat(uint&lt;x&gt; value);`  
</dl>

## <a name="minimum-shader-model"></a>Shader-Mindestmodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                                        | Unterstützt |
|---------------------------------------------------------------------|-----------|
| [Shadermodell 4](dx-graphics-hlsl-sm4.md) und höhere Shadermodelle | ja       |
| [Shadermodell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md)           | Nein        |
| [Shadermodell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md)           | Nein        |
| [Shadermodell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)           | Nein        |



 

## <a name="remarks"></a>Hinweise

Ältere Compiler haben fälschlicherweise `asfloat(bool)` zugelassen, aber beachten Sie, dass bool-Eingaben nicht unterstützt werden.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Systeminterne Funktionen (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

