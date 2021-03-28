---
title: smoothstep
description: Gibt eine Smooth Hermite-interpolung zwischen 0 und 1 zurück, wenn x im Bereich \ min, Max \ liegt.
ms.assetid: 6a879d82-f5ab-4e9b-bc9c-8988cbe6aa82
keywords:
- smoothstep HLSL
topic_type:
- apiref
api_name:
- smoothstep
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 64e828b52a4d4517e53ba1f1aaf0f687255ad02b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104976672"
---
# <a name="smoothstep"></a>smoothstep

Gibt eine Smooth Hermite Interpolations zwischen 0 und 1 zurück, wenn *x* im Bereich \[ *Min*, *Max* liegt \] .



| *ret* -glättstep (*Min*, *Max*, *x*) |
|-------------------------------------|



 

## <a name="parameters"></a>Parameter



| Element                                                         | BESCHREIBUNG                                               |
|--------------------------------------------------------------|-----------------------------------------------------------|
| <span id="min"></span><span id="MIN"></span>*man*<br/> | \[im \] Minimal Bereich des *x* -Parameters.<br/> |
| <span id="max"></span><span id="MAX"></span>*Max*<br/> | \[im \] maximalen Bereich des *x* -Parameters.<br/> |
| <span id="x"></span><span id="X"></span>*Stuben*<br/>       | \[im \] angegebenen Wert, der interpoliert werden soll.<br/> |



 

## <a name="return-value"></a>Rückgabewert

Gibt 0 zurück, wenn *x* kleiner als *Min* ist. 1, wenn *x* größer als der *Maximale* Wert ist. andernfalls ein Wert zwischen 0 und 1, wenn *x* im Bereich \[ *Min*, Max liegt  \] .

## <a name="remarks"></a>Bemerkungen

Verwenden Sie die systeminterne Funktion " **smoothstep** HLSL", um einen reibungslosen Übergang zwischen zwei Werten zu erstellen. Beispielsweise können Sie diese Funktion verwenden, um zwei Farben reibungslos zu kombinieren.

## <a name="type-description"></a>Typbeschreibung



| Name  | [**Vorlagentyp**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Komponententyp**](dx-graphics-hlsl-intrinsic-functions.md) | Size                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *x*   | [**Skalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vektor** oder **Matrix** | [**Hafen**](/windows/desktop/WinProg/windows-data-types)                        | any                            |
| *min* | identisch mit Eingabe *x*                                                                                              | [**Hafen**](/windows/desktop/WinProg/windows-data-types)                        | gleiche Dimension (n) wie Eingabe *x* |
| *max* | identisch mit Eingabe *x*                                                                                              | [**Hafen**](/windows/desktop/WinProg/windows-data-types)                        | gleiche Dimension (n) wie Eingabe *x* |
| *TZI* | identisch mit Eingabe *x*                                                                                              | [**Hafen**](/windows/desktop/WinProg/windows-data-types)                        | gleiche Dimension (n) wie Eingabe *x* |



 

## <a name="minimum-shader-model"></a>Minimaler Shader-Modell

Diese Funktion wird in den folgenden shadermodellen unterstützt.



| Shadermodell                                                                       | Unterstützt           |
|------------------------------------------------------------------------------------|---------------------|
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) und höhere Shader-Modelle | ja                 |
| [Shader-Modell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | Ja ( \_ nur vs 1 \_ 1) |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Intrinsische Funktionen (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

