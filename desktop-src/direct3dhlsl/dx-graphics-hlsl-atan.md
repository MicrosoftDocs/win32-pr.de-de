---
title: atan
description: Gibt den Arangens des angegebenen Werts zurück.
ms.assetid: e3ce3ac3-1012-414f-a193-102208083e39
keywords:
- atan HLSL
topic_type:
- apiref
api_name:
- atan
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 69c3b51381318627dd5c3ce7b64fe405968c669418bdf743b5c56eaae535b0a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117726400"
---
# <a name="atan"></a>atan

Gibt den Arangens des angegebenen Werts zurück.



| *ret* atan(*x*) |
|-----------------|



 

## <a name="parameters"></a>Parameter



| Element                                                   | Beschreibung                            |
|--------------------------------------------------------|----------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/> | \[in \] Der angegebene Wert.<br/> |



 

## <a name="return-value"></a>Rückgabewert

Der Arangens  des x-Parameters. Dieser Wert liegt im Bereich von -π/2 bis π/2.

## <a name="type-description"></a>Typbeschreibung



| Name  | [**Vorlagentyp**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Komponententyp**](dx-graphics-hlsl-intrinsic-functions.md) | Size                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *x*   | [**Skalar,**](dx-graphics-hlsl-intrinsic-functions.md) **Vektor** oder **Matrix** | [**schweben**](/windows/desktop/WinProg/windows-data-types)                        | any                            |
| *Ret* | identisch mit eingabe *x*                                                                                              | [**schweben**](/windows/desktop/WinProg/windows-data-types)                        | Gleiche Dimension(en) wie eingabe *x* |



 

## <a name="minimum-shader-model"></a>Shader-Mindestmodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                                                       | Unterstützt |
|------------------------------------------------------------------------------------|-----------|
| [Shadermodell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) und höhere Shadermodelle | Ja       |
| [Shadermodell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | Vs \_ 1 \_ 1  |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Systeminterne Funktionen (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

