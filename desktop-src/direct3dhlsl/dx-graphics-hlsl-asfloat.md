---
title: asfloat
description: Interpretiert das Bitmuster von x als Gleit Komma Zahl.
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
ms.openlocfilehash: 9a5701d959fb59519318dd7f2e91b6790f4c0b6e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104993534"
---
# <a name="asfloat"></a>asfloat

Interpretiert das Bitmuster von *x* als Gleit Komma Zahl.



| Ret asfloat (*x*) |
|------------------|



 

## <a name="parameters"></a>Parameter



| Element                                                   | BESCHREIBUNG                        |
|--------------------------------------------------------|------------------------------------|
| <span id="x"></span><span id="X"></span>*Stuben*<br/> | \[im \] Eingabe Wert.<br/> |



 

## <a name="return-value"></a>Rückgabewert

Die als Gleit Komma Zahl interpretierte Eingabe.

## <a name="type-description"></a>Typbeschreibung



| Name  | [**Vorlagentyp**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Komponententyp**](dx-graphics-hlsl-intrinsic-functions.md)                                                         | Size                           |
|-------|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| *x*   | [**Skalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vektor** oder **Matrix** | [**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types), [**uint**](/windows/desktop/WinProg/windows-data-types) | any                            |
| *TZI* | identisch mit Eingabe *x*                                                                                              | [**Hafen**](/windows/desktop/WinProg/windows-data-types)                                                                                | gleiche Dimension (n) wie Eingabe *x* |



 

## <a name="function-overloads"></a>Funktions Überladungen

<dl> ' float <x> asfloat (float- <x> Wert); `  
` float <x> asfloat (int- <x> Wert); `  
` float <x> asfloat (uint- <x> Wert); '
</dl>

## <a name="minimum-shader-model"></a>Minimaler Shader-Modell

Diese Funktion wird in den folgenden shadermodellen unterstützt.



| Shadermodell                                                        | Unterstützt |
|---------------------------------------------------------------------|-----------|
| [Shader Model 4](dx-graphics-hlsl-sm4.md) und höhere shadermodelle | ja       |
| [Shader-Modell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md)           | nein        |
| [Shader-Modell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md)           | nein        |
| [Shader-Modell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)           | nein        |



 

## <a name="remarks"></a>Bemerkungen

Ältere Compiler sind falsch zulässig `asfloat(bool)` , aber beachten Sie, dass keine booleschen Eingaben unterstützt werden.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Intrinsische Funktionen (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

