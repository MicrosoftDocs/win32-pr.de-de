---
title: Löschen
description: Gibt einen rückbrechungs Vektor mithilfe eines eintretende Strahl, eines Oberflächen normalen und eines abbrechungs Indexes zurück.
ms.assetid: 9f9467d7-dd9b-472a-bbdc-752394d382c6
keywords:
- HLSL Abbrechen
topic_type:
- apiref
api_name:
- refract
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9e499d078a020ade1ff9ff2566c3fd15b2a820d2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104993567"
---
# <a name="refract"></a>Löschen

Gibt einen rückbrechungs Vektor mithilfe eines eintretende Strahl, eines Oberflächen normalen und eines abbrechungs Indexes zurück.



| *ret* Refract (*i*, *n*,?) |
|----------------------------|



 

## <a name="parameters"></a>Parameter



| Element                                                   | BESCHREIBUNG                                                  |
|--------------------------------------------------------|--------------------------------------------------------------|
| <span id="i"></span><span id="I"></span>*Ich*<br/> | \[in \] einem Gleit Komma-Richtungsvektor.<br/>    |
| <span id="n"></span><span id="N"></span>*Nr*<br/> | \[in \] einem Gleit Komma-, Oberflächen normalen Vektor.<br/>   |
| *?*<br/>                                         | \[brechen Sie in \] einem Gleit Komma den Index Skalarwert ab.<br/> |



 

## <a name="return-value"></a>Rückgabewert

Ein Gleit Komma Trennzeichen. Wenn der Winkel zwischen dem eingaberay i und dem Oberflächen normalen n zu groß für einen bestimmten abbrechungs Index ist, ist der Rückgabewert (0, 0,0).

## <a name="type-description"></a>Typbeschreibung



| Name              | [**Vorlagentyp**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Komponententyp**](dx-graphics-hlsl-intrinsic-functions.md) | Size                           |
|-------------------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *i*               | [**ve**](dx-graphics-hlsl-intrinsic-functions.md) | [**Hafen**](/windows/desktop/WinProg/windows-data-types)                        | any                            |
| *n*               | [**ve**](dx-graphics-hlsl-intrinsic-functions.md) | [**Hafen**](/windows/desktop/WinProg/windows-data-types)                        | gleiche Dimension (n) wie Eingabe *i* |
| ?                 | [**Skalar**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 1                              |
| Brechungs Vektor | [**ve**](dx-graphics-hlsl-intrinsic-functions.md) | [**Hafen**](/windows/desktop/WinProg/windows-data-types)                        | gleiche Dimension (n) wie Eingabe *i* |



 

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

 

