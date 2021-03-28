---
title: Signieren
description: Gibt das Vorzeichen von x zurück.
ms.assetid: 3e2e04e8-0ffc-4721-a5d8-1ccfa6ca2a1a
keywords:
- HLSL Signieren
topic_type:
- apiref
api_name:
- sign
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fc177e72e116394ffd6241e0616b84c9066a68a7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104993566"
---
# <a name="sign"></a>Signieren

Gibt das Vorzeichen von *x* zurück.



| *ret* -Zeichen (*x*) |
|-----------------|



 

## <a name="parameters"></a>Parameter



| Element                                                   | BESCHREIBUNG                        |
|--------------------------------------------------------|------------------------------------|
| <span id="x"></span><span id="X"></span>*Stuben*<br/> | \[im \] Eingabe Wert.<br/> |



 

## <a name="return-value"></a>Rückgabewert

Gibt-1 zurück, wenn *x* kleiner als 0 (null) ist. 0, wenn *x* gleich NULL ist. und 1, wenn *x* größer als 0 (null) ist.

## <a name="type-description"></a>Typbeschreibung



| Name  | [**Vorlagentyp**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Komponententyp**](dx-graphics-hlsl-intrinsic-functions.md)                 | Size                           |
|-------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|--------------------------------|
| *x*   | [**Skalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vektor** oder **Matrix** | [**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types) | any                            |
| *TZI* | identisch mit Eingabe *x*                                                                                              | [**INT**](/windows/desktop/WinProg/windows-data-types)                                          | gleiche Dimension (n) wie Eingabe *x* |



 

## <a name="minimum-shader-model"></a>Minimaler Shader-Modell

Diese Funktion wird in den folgenden shadermodellen unterstützt.



| Shadermodell                                                                       | Unterstützt                   |
|------------------------------------------------------------------------------------|-----------------------------|
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) und höhere Shader-Modelle | ja                         |
| [Shader-Modell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | Ja (vs \_ 1 \_ 1 und PS \_ 1 \_ 4) |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Intrinsische Funktionen (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

