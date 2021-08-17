---
title: tanh
description: Gibt den hyperbolischen Tangens des angegebenen Werts zurück.
ms.assetid: e2d27aa0-5e03-4f2f-a29c-884711710c8d
keywords:
- tanh HLSL
topic_type:
- apiref
api_name:
- tanh
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7a680863cd8aa4c46a74dc4a4d332ce893dc8bbcb2b46589af3ad35acb15e172
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117725698"
---
# <a name="tanh"></a>tanh

Gibt den hyperbolischen Tangens des angegebenen Werts zurück.



| *ret* tanh(*x*) |
|-----------------|



 

## <a name="parameters"></a>Parameter



| Element                                                   | Beschreibung                                        |
|--------------------------------------------------------|----------------------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/> | \[in \] Der angegebene Wert im Bogenmaß.<br/> |



 

## <a name="return-value"></a>Rückgabewert

Der hyperbolische Tangens des *x-Parameters.*

## <a name="type-description"></a>Typbeschreibung



| Name  | [**Vorlagentyp**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Komponententyp**](dx-graphics-hlsl-intrinsic-functions.md) | Size                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *x*   | [**Skalar,**](dx-graphics-hlsl-intrinsic-functions.md) **Vektor** oder **Matrix** | [**schweben**](/windows/desktop/WinProg/windows-data-types)                        | any                            |
| *Ret* | identisch mit Eingabe *x*                                                                                              | [**schweben**](/windows/desktop/WinProg/windows-data-types)                        | Gleiche Dimension(n) wie Eingabe *x* |



 

## <a name="minimum-shader-model"></a>Minimales Shadermodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                                                       | Unterstützt           |
|------------------------------------------------------------------------------------|---------------------|
| [Shadermodell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) und höhere Shadermodelle | Ja                 |
| [Shadermodell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | Ja (nur \_ im Vergleich \_ zu 1 1) |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Systeminterne Funktionen (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

