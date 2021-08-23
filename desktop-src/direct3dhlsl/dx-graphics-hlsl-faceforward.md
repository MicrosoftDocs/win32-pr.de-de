---
title: faceforward
description: Flips the surface-normal (if needed) to face in a direction opposite to i; gibt das Ergebnis in n zurück.
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
ms.openlocfilehash: 253d581ef5ea2eddac55c63245039f1ccda6c0e73032468d1598fb919e850a18
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950380"
---
# <a name="faceforward"></a>faceforward

Flips the surface-normal (if needed) to face in a direction opposite to i; gibt das Ergebnis in n zurück.



| *ret* faceforward(*n*, *i*, *ng*) |
|-----------------------------------|



 

Diese Funktion verwendet die folgende Formel: -*n*  sign(dot(*i*, *ng*)).

## <a name="parameters"></a>Parameter



| Element                                                      | BESCHREIBUNG                                                                                                     |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span id="n"></span><span id="N"></span>*N*<br/>    | \[in \] Der resultierende Gleitkommaoberflächen-Normalvektor.<br/>                                           |
| <span id="i"></span><span id="I"></span>*Ich*<br/>    | \[in \] Ein Gleitkomma-Incidentvektor, der von der Ansichtsposition auf die Schattierungsposition zeigt.<br/> |
| <span id="ng"></span><span id="NG"></span>*Ng*<br/> | \[in \] Einem Gleitkommaoberflächen-Normalvektor.<br/>                                                       |



 

## <a name="return-value"></a>Rückgabewert

Ein normaler Gleitkommavektor für die Oberfläche, der auf die Ansichtsrichtung ausgerichtet ist.

## <a name="type-description"></a>Typbeschreibung



| Name  | [**Vorlagentyp**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Komponententyp**](dx-graphics-hlsl-intrinsic-functions.md) | Size                           |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *n*   | [**Vektor**](dx-graphics-hlsl-intrinsic-functions.md) | [**schweben**](/windows/desktop/WinProg/windows-data-types)                        | any                            |
| *i*   | [**Vektor**](dx-graphics-hlsl-intrinsic-functions.md) | [**schweben**](/windows/desktop/WinProg/windows-data-types)                        | gleiche Dimension(n) wie die *Eingabe n* |
| *Ng*  | [**Vektor**](dx-graphics-hlsl-intrinsic-functions.md) | [**schweben**](/windows/desktop/WinProg/windows-data-types)                        | Gleiche Dimensionen wie Eingabe *n*   |
| *Ret* | [**Vektor**](dx-graphics-hlsl-intrinsic-functions.md) | [**schweben**](/windows/desktop/WinProg/windows-data-types)                        | Gleiche Dimensionen wie Eingabe *n*   |



 

## <a name="minimum-shader-model"></a>Minimales Shadermodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                                                       | Unterstützt             |
|------------------------------------------------------------------------------------|-----------------------|
| [Shadermodell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) und höhere Shadermodelle | Ja                   |
| [Shadermodell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | vs \_ 1 \_ 1 und ps \_ 1 \_ 4 |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Systeminterne Funktionen (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

