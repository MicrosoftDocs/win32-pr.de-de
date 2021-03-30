---
title: asuint
description: Interpretiert das Bitmuster von x als ganze Zahl ohne Vorzeichen.
ms.assetid: 8401001d-f9ee-43da-9756-f311e9f2bb20
keywords:
- asuint HLSL
topic_type:
- apiref
api_name:
- asuint
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1a2d351eb36c6910790e2dceb94e3a97951ad850
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104976800"
---
# <a name="asuint"></a>asuint

Interpretiert das Bitmuster von *x* als ganze Zahl ohne Vorzeichen.



| Ret-Taste (*x*) |
|-----------------|



 

## <a name="parameters"></a>Parameter



| Element                                                   | BESCHREIBUNG                        |
|--------------------------------------------------------|------------------------------------|
| <span id="x"></span><span id="X"></span>*Stuben*<br/> | \[im \] Eingabe Wert.<br/> |



 

## <a name="return-value"></a>Rückgabewert

Die Eingabe, die als ganze Zahl ohne Vorzeichen interpretiert wird.

## <a name="type-description"></a>Typbeschreibung



| Name  | [**Vorlagentyp**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Komponententyp**](dx-graphics-hlsl-intrinsic-functions.md)                 | Size                           |
|-------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|--------------------------------|
| *x*   | [**Skalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vektor** oder **Matrix** | [**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types) | any                            |
| *TZI* | identisch mit Eingabe *x*                                                                                              | [**uint**](/windows/desktop/WinProg/windows-data-types)                                         | gleiche Dimension (n) wie Eingabe *x* |



 

## <a name="minimum-shader-model"></a>Minimaler Shader-Modell

Diese Funktion wird in den folgenden shadermodellen unterstützt.



| Shadermodell                                                        | Unterstützt |
|---------------------------------------------------------------------|-----------|
| [Shader Model 4](dx-graphics-hlsl-sm4.md) und höhere shadermodelle | ja       |
| [Shader-Modell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md)           | nein        |
| [Shader-Modell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md)           | nein        |
| [Shader-Modell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)           | Nein        |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Intrinsische Funktionen (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

