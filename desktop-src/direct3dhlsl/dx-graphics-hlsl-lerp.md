---
title: Lerp
description: Führt eine lineare interpolung aus.
ms.assetid: e369f182-b5bd-4b7f-aa77-9cfe11033bc4
keywords:
- Lerp HLSL
topic_type:
- apiref
api_name:
- lerp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7c7a5251aaf410d7224b87b9ee9a8f0e8a0c947e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104993431"
---
# <a name="lerp"></a>Lerp

Führt eine lineare interpolung aus.



| *ret* Lerp (*x*, *y*, *s*) |
|---------------------------|



 

## <a name="parameters"></a>Parameter



| Element                                                   | BESCHREIBUNG                                                                                           |
|--------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span id="x"></span><span id="X"></span>*Stuben*<br/> | \[im \] ersten Gleit Komma Wert.<br/>                                                     |
| <span id="y"></span><span id="Y"></span>*Teenie*<br/> | \[im \] zweiten Gleit Komma Wert.<br/>                                                    |
| <span id="s"></span><span id="S"></span>*Hymnen*<br/> | \[in \] einem Wert, der linear zwischen dem *x* -Parameter und dem *y* -Parameter interpoliert.<br/> |



 

## <a name="return-value"></a>Rückgabewert

Das Ergebnis der linearen interpolung.

## <a name="type-description"></a>Typbeschreibung



| Name  | [**Vorlagentyp**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Komponententyp**](dx-graphics-hlsl-intrinsic-functions.md) | Size                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *x*   | [**Skalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vektor** oder **Matrix** | [**Hafen**](/windows/desktop/WinProg/windows-data-types)                        | any                            |
| *y*   | identisch mit Eingabe *x*                                                                                              | [**Hafen**](/windows/desktop/WinProg/windows-data-types)                        | gleiche Dimension (n) wie Eingabe *x* |
| *s*   | identisch mit Eingabe *x*                                                                                              | [**Hafen**](/windows/desktop/WinProg/windows-data-types)                        | gleiche Dimension (n) wie Eingabe *x* |
| *TZI* | identisch mit Eingabe *x*                                                                                              | [**Hafen**](/windows/desktop/WinProg/windows-data-types)                        | gleiche Dimension (n) wie Eingabe *x* |



 

## <a name="remarks"></a>Bemerkungen

Die lineare interpolung basiert auf der folgenden Formel: x \* (1-s) + y \* s, die gleichwertig als x + s (y-x) geschrieben werden können.

## <a name="minimum-shader-model"></a>Minimaler Shader-Modell

Diese Funktion wird in den folgenden shadermodellen unterstützt.



| Shadermodell                                                                       | Unterstützt                   |
|------------------------------------------------------------------------------------|-----------------------------|
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) und höhere Shader-Modelle | ja                         |
| [Shader-Modell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | Ja (vs \_ 1 \_ 1 und PS \_ 1 \_ 1) |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Intrinsische Funktionen (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

