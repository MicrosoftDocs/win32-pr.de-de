---
title: Umsetzung
description: Transponiert die angegebene Eingabematrix.
ms.assetid: 2a2ff2fb-73f0-4bb8-af83-38fe0567d122
keywords:
- Transponieren von HLSL
topic_type:
- apiref
api_name:
- transpose
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e6e545e657e6d9eaded92affba5bbb52a22222db2bf87acd5dddb72335a17ab0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119754"
---
# <a name="transpose"></a>Umsetzung

Transponiert die angegebene Eingabematrix.



| ret transponieren(*x*) |
|--------------------|



 

## <a name="parameters"></a>Parameter



| Element                                                   | Beschreibung                             |
|--------------------------------------------------------|-----------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/> | \[in \] Die angegebene Matrix.<br/> |



 

## <a name="return-value"></a>Rückgabewert

Der transponierte Wert des *x-Parameters.*

## <a name="remarks"></a>Hinweise

Wenn die Dimensionen der Quellmatrix *Zeilenspalten* *sind,* ist die resultierende Matrix *Spaltenzeilen.* 

## <a name="type-description"></a>Typbeschreibung



| Name | [**Vorlagentyp**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Komponententyp**](dx-graphics-hlsl-intrinsic-functions.md)                                                         | Size                                                                                   |
|------|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| *x*  | [**Matrix**](dx-graphics-hlsl-intrinsic-functions.md) | [**float,**](/windows/desktop/WinProg/windows-data-types) [**int,**](/windows/desktop/WinProg/windows-data-types) [**bool**](/windows/desktop/WinProg/windows-data-types) | any                                                                                    |
| Ret  | [**Matrix**](dx-graphics-hlsl-intrinsic-functions.md) | [**float,**](/windows/desktop/WinProg/windows-data-types) [**int,**](/windows/desktop/WinProg/windows-data-types) [**bool**](/windows/desktop/WinProg/windows-data-types) | rows = gleiche Anzahl von Spalten wie Eingabe *x,* Spalten = gleiche Anzahl von Zeilen wie Eingabe *x* |



 

## <a name="minimum-shader-model"></a>Minimales Shadermodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                                                       | Unterstützt |
|------------------------------------------------------------------------------------|-----------|
| [Shadermodell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) und höhere Shadermodelle | Ja       |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Systeminterne Funktionen (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

