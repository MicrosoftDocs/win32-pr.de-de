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
ms.openlocfilehash: ac8be8a81cca5c0ed7377475f2e3688a8c0c90c33fddcaab8c4de0f15f174eca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118514773"
---
# <a name="asuint"></a>asuint

Interpretiert das Bitmuster von *x* als ganze Zahl ohne Vorzeichen.



| ret asuint(*x*) |
|-----------------|



 

## <a name="parameters"></a>Parameter



| Element                                                   | BESCHREIBUNG                        |
|--------------------------------------------------------|------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/> | \[in \] Der Eingabewert.<br/> |



 

## <a name="return-value"></a>Rückgabewert

Die Eingabe, die als ganze Zahl ohne Vorzeichen interpretiert wird.

## <a name="type-description"></a>Typbeschreibung



| Name  | [**Vorlagentyp**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Komponententyp**](dx-graphics-hlsl-intrinsic-functions.md)                 | Size                           |
|-------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|--------------------------------|
| *x*   | [**Skalar,**](dx-graphics-hlsl-intrinsic-functions.md) **Vektor** oder **Matrix** | [**float,**](/windows/desktop/WinProg/windows-data-types) [ **int**](/windows/desktop/WinProg/windows-data-types) | any                            |
| *Ret* | identisch mit Eingabe *x*                                                                                              | [**uint**](/windows/desktop/WinProg/windows-data-types)                                         | Gleiche Dimension(n) wie Eingabe *x* |



 

## <a name="minimum-shader-model"></a>Minimales Shadermodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                                        | Unterstützt |
|---------------------------------------------------------------------|-----------|
| [Shadermodell 4](dx-graphics-hlsl-sm4.md) und höhere Shadermodelle | ja       |
| [Shadermodell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md)           | nein        |
| [Shadermodell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md)           | nein        |
| [Shadermodell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)           | Nein        |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Systeminterne Funktionen (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

