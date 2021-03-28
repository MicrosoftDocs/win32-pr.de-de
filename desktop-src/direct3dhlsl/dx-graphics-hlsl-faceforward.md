---
title: faceforward
description: Flippt die Oberfläche-normal (falls erforderlich) in eine Richtung vor i. Gibt das Ergebnis in n zurück.
ms.assetid: 6530a928-d221-49e4-ab68-6285c3db370f
keywords:
- faceforward HLSL
topic_type:
- apiref
api_name:
- faceforward
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c6a3f035ed4f0d16b500864f941bc4fe5413ff54
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101823"
---
# <a name="faceforward"></a>faceforward

Flippt die Oberfläche-normal (falls erforderlich) in eine Richtung vor i. Gibt das Ergebnis in n zurück.



| *ret* faceforward (*n*, *i*, *ng*) |
|-----------------------------------|



 

Diese Funktion verwendet die folgende Formel:-*n*  Sign (Punkt (*i*, *ng*)).

## <a name="parameters"></a>Parameter



| Element                                                      | BESCHREIBUNG                                                                                                     |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span id="n"></span><span id="N"></span>*Nr*<br/>    | \[im \] resultierenden Gleit Komma Oberflächen-normal Vektor.<br/>                                           |
| <span id="i"></span><span id="I"></span>*Ich*<br/>    | \[in \] einem Gleit Komma-Incident-Vektor, der von der Ansichts Position auf die Schattierungs Position zeigt.<br/> |
| <span id="ng"></span><span id="NG"></span>*1968*<br/> | \[in \] einem Gleit Komma Oberflächen-normal Vektor.<br/>                                                       |



 

## <a name="return-value"></a>Rückgabewert

Ein Gleit Komma Wert, Oberflächen normaler Vektor, der der Ansichts Richtung entspricht.

## <a name="type-description"></a>Typbeschreibung



| Name  | [**Vorlagentyp**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Komponententyp**](dx-graphics-hlsl-intrinsic-functions.md) | Size                           |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *n*   | [**ve**](dx-graphics-hlsl-intrinsic-functions.md) | [**Hafen**](/windows/desktop/WinProg/windows-data-types)                        | any                            |
| *i*   | [**ve**](dx-graphics-hlsl-intrinsic-functions.md) | [**Hafen**](/windows/desktop/WinProg/windows-data-types)                        | gleiche Dimension (n) wie Eingabe *n* |
| *ng*  | [**ve**](dx-graphics-hlsl-intrinsic-functions.md) | [**Hafen**](/windows/desktop/WinProg/windows-data-types)                        | gleiche Dimensionen wie Eingabe *n*   |
| *TZI* | [**ve**](dx-graphics-hlsl-intrinsic-functions.md) | [**Hafen**](/windows/desktop/WinProg/windows-data-types)                        | gleiche Dimensionen wie Eingabe *n*   |



 

## <a name="minimum-shader-model"></a>Minimaler Shader-Modell

Diese Funktion wird in den folgenden shadermodellen unterstützt.



| Shadermodell                                                                       | Unterstützt             |
|------------------------------------------------------------------------------------|-----------------------|
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) und höhere Shader-Modelle | ja                   |
| [Shader-Modell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | vs \_ 1 \_ 1 und PS \_ 1 \_ 4 |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Intrinsische Funktionen (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

