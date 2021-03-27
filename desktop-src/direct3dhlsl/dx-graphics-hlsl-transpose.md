---
title: austauschen
description: Vertauscht die angegebene Eingabe Matrix.
ms.assetid: 2a2ff2fb-73f0-4bb8-af83-38fe0567d122
keywords:
- HLSL austauschen
topic_type:
- apiref
api_name:
- transpose
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 44f129a87edaff260de87136954be7598ee3acb6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390427"
---
# <a name="transpose"></a>austauschen

Vertauscht die angegebene Eingabe Matrix.



| Ret-austauschen (*x*) |
|--------------------|



 

## <a name="parameters"></a>Parameter



| Element                                                   | BESCHREIBUNG                             |
|--------------------------------------------------------|-----------------------------------------|
| <span id="x"></span><span id="X"></span>*Stuben*<br/> | \[in \] der angegebenen Matrix.<br/> |



 

## <a name="return-value"></a>Rückgabewert

Der übersetzte Wert des *x* -Parameters.

## <a name="remarks"></a>Bemerkungen

Wenn die Dimensionen der Quell Matrix *Zeilen* *Spalten* sind, handelt es sich bei der resultierenden Matrix um *Spalten* *Zeilen*.

## <a name="type-description"></a>Typbeschreibung



| Name | [**Vorlagentyp**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Komponententyp**](dx-graphics-hlsl-intrinsic-functions.md)                                                         | Size                                                                                   |
|------|-------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| *x*  | [**Matrix**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types), [**bool**](/windows/desktop/WinProg/windows-data-types) | any                                                                                    |
| TZI  | [**Matrix**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types), [**bool**](/windows/desktop/WinProg/windows-data-types) | Rows = gleiche Anzahl von Spalten wie Eingabe *x*, Spalten = gleiche Anzahl von Zeilen als Eingabe *x* |



 

## <a name="minimum-shader-model"></a>Minimaler Shader-Modell

Diese Funktion wird in den folgenden shadermodellen unterstützt.



| Shadermodell                                                                       | Unterstützt |
|------------------------------------------------------------------------------------|-----------|
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) und höhere Shader-Modelle | ja       |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Intrinsische Funktionen (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

