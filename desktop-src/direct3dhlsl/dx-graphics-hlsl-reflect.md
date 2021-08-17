---
title: Spiegeln
description: Gibt einen Reflektionsvektor mit einem Incidentstrahl und einer Oberflächennormnorm zurück.
ms.assetid: e321b399-f382-4585-83a6-a7da1f7b2327
keywords:
- hlsl reflektieren
topic_type:
- apiref
api_name:
- reflect
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2abc7100eae846fc3d2f21b013676aa3dbc64574a7e8cdb8a14dc492ceb33f75
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117725944"
---
# <a name="reflect"></a>Spiegeln

Gibt einen Reflektionsvektor mit einem Incidentstrahl und einer Oberflächennormnorm zurück.



| *ret* reflect(*i*, *n*) |
|-------------------------|



 

## <a name="parameters"></a>Parameter



| Element                                                   | Beschreibung                                          |
|--------------------------------------------------------|------------------------------------------------------|
| <span id="i"></span><span id="I"></span>*Ich*<br/> | \[in \] Einem Gleitkomma- und Incidentvektor.<br/> |
| <span id="n"></span><span id="N"></span>*N*<br/> | \[in \] einem Gleitkomma, normaler Vektor.<br/>   |



 

## <a name="return-value"></a>Rückgabewert

Ein Gleitkomma-Reflektionsvektor.

## <a name="remarks"></a>Hinweise

Diese Funktion berechnet den Reflektionsvektor mit der folgenden Formel: v = i - 2 \* n \* Punkt(i n) .

## <a name="type-description"></a>Typbeschreibung



| Name  | [**Vorlagentyp**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Komponententyp**](dx-graphics-hlsl-intrinsic-functions.md) | Size                           |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *i*   | [**Vektor**](dx-graphics-hlsl-intrinsic-functions.md) | [**schweben**](/windows/desktop/WinProg/windows-data-types)                        | any                            |
| *n*   | [**Vektor**](dx-graphics-hlsl-intrinsic-functions.md) | [**schweben**](/windows/desktop/WinProg/windows-data-types)                        | Gleiche Dimension(n) wie eingabe *i* |
| *Ret* | [**Vektor**](dx-graphics-hlsl-intrinsic-functions.md) | [**schweben**](/windows/desktop/WinProg/windows-data-types)                        | Gleiche Dimension(n) wie eingabe *i* |



 

## <a name="minimum-shader-model"></a>Minimales Shadermodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                                                       | Unterstützt |
|------------------------------------------------------------------------------------|-----------|
| [Shadermodell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) und höhere Shadermodelle | Ja       |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Systeminterne Funktionen (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

