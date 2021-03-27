---
title: Lautstärke
description: Generiert einen zufälligen Wert mithilfe des Perlin-Rausch-Algorithmus.
ms.assetid: 0188a7f3-9955-4e1c-9370-ef1d8aff3765
keywords:
- Füll-HLSL
topic_type:
- apiref
api_name:
- noise
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6a4dc01eaeb8276527d5d78b07a250d2a6fb1ab9
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104391248"
---
# <a name="noise"></a>Lautstärke

Generiert einen zufälligen Wert mithilfe des Perlin-Rausch-Algorithmus.




| *ret* -Rauschen (*x*) |
|------------------|



 

## <a name="parameters"></a>Parameter



| Element                                                   | BESCHREIBUNG                                                                    |
|--------------------------------------------------------|--------------------------------------------------------------------------------|
| <span id="x"></span><span id="X"></span>*Stuben*<br/> | \[in \] einem Gleit Komma Vektor, von dem Perlin-Rauschen generiert werden sollen.<br/> |



 

## <a name="return-value"></a>Rückgabewert

Der Perlin-Rausch Wert innerhalb eines Bereichs zwischen-1 und 1.

## <a name="remarks"></a>Bemerkungen

Perlin-Rauschwerte ändern sich reibungslos von einem Punkt zu einem anderen als einem Leerzeichen und erstellen dabei natürliche, nach dem Zufallsprinzip generierte Werte. Sie können Perlin-Rauschen verwenden, um prozedurale Texturen für Effekte wie Rauch und Feuer zu generieren.

## <a name="type-description"></a>Typbeschreibung



| Name  | [**Vorlagentyp**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Komponententyp**](dx-graphics-hlsl-intrinsic-functions.md) | Size |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| *x*   | [**ve**](dx-graphics-hlsl-intrinsic-functions.md) | [**Hafen**](/windows/desktop/WinProg/windows-data-types)                        | any  |
| *TZI* | [**Skalar**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 1    |



 

## <a name="minimum-shader-model"></a>Minimaler Shader-Modell

Diese Funktion wird in den folgenden shadermodellen unterstützt.



| Shadermodell                                                                       | Unterstützt           |
|------------------------------------------------------------------------------------|---------------------|
| [Shader Model 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) und höhere Shader-Modelle | nein                  |
| [Shader-Modell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | Ja ( \_ nur TX 1 \_ 0) |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Intrinsische Funktionen (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

