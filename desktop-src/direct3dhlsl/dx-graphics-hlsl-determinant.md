---
title: Determinante
description: Gibt die Determinante der angegebenen quadratischen Gleitkommamatrix zurück.
ms.assetid: 9062b6f1-8518-4ee4-8d57-5aa9e2176d05
keywords:
- Determinante HLSL
topic_type:
- apiref
api_name:
- determinant
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 75b17982560d70cf00cfb13832de9605b910f169d1461692f4c6a97274709e52
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119120305"
---
# <a name="determinant"></a>Determinante

Gibt die Determinante der angegebenen quadratischen Gleitkommamatrix zurück.



| *ret* determinant(*m*) |
|------------------------|



 

## <a name="parameters"></a>Parameter



| Element                                                   | Beschreibung                            |
|--------------------------------------------------------|----------------------------------------|
| <span id="m"></span><span id="M"></span>*M*<br/> | \[in \] Der angegebene Wert.<br/> |



 

## <a name="return-value"></a>Rückgabewert

Der Gleitkomma- und Skalarwert, der die Determinante des *m-Parameters* darstellt.

## <a name="type-description"></a>Typbeschreibung



| Name  | [**Vorlagentyp**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Komponententyp**](dx-graphics-hlsl-intrinsic-functions.md) | Size                                     |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------------------------------------------|
| *m*   | [**Matrix**](dx-graphics-hlsl-intrinsic-functions.md) | [**schweben**](/windows/desktop/WinProg/windows-data-types)                        | any (Anzahl der Zeilen = Anzahl der Spalten) |
| *Ret* | [**Skalare**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 1                                        |



 

## <a name="minimum-shader-model"></a>Minimales Shadermodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                                                       | Unterstützt             |
|------------------------------------------------------------------------------------|-----------------------|
| [Shadermodell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) und höhere Shadermodelle | Ja                   |
| [Shadermodell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | vs \_ 1 \_ 1 und ps \_ 1 \_ 4 |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Systeminterne Funktionen (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

