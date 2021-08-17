---
title: Lautstärke
description: Generiert mithilfe des Perlin-Noise-Algorithmus einen zufallsbasierten Wert.
ms.assetid: 0188a7f3-9955-4e1c-9370-ef1d8aff3765
keywords:
- HlSL-Rauschen
topic_type:
- apiref
api_name:
- noise
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5eb93d32e7730b6840700bba9dc5a629bf3180f83673581f8589a254d467cff8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119120104"
---
# <a name="noise"></a>Lautstärke

Generiert mithilfe des Perlin-Noise-Algorithmus einen zufallsbasierten Wert.




| *ret* noise(*x*) |
|------------------|



 

## <a name="parameters"></a>Parameter



| Element                                                   | Beschreibung                                                                    |
|--------------------------------------------------------|--------------------------------------------------------------------------------|
| <span id="x"></span><span id="X"></span>*X*<br/> | \[in \] Einem Gleitkommavektor, aus dem Perlinrauschen generiert werden soll.<br/> |



 

## <a name="return-value"></a>Rückgabewert

Der Perlin-Rauschwert innerhalb eines Bereichs zwischen -1 und 1.

## <a name="remarks"></a>Hinweise

Perlin-Rauschwerte ändern sich nahtlos von einem Punkt zum anderen über einen Raum, wodurch natürlich aussehende, zufällig generierte Werte erstellt werden. Sie können Perlinrauschen verwenden, um prozedurale Texturen für Effekte wie Feuer und Feuer zu generieren.

## <a name="type-description"></a>Typbeschreibung



| Name  | [**Vorlagentyp**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Komponententyp**](dx-graphics-hlsl-intrinsic-functions.md) | Size |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| *x*   | [**Vektor**](dx-graphics-hlsl-intrinsic-functions.md) | [**schweben**](/windows/desktop/WinProg/windows-data-types)                        | any  |
| *Ret* | [**Skalare**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 1    |



 

## <a name="minimum-shader-model"></a>Shader-Mindestmodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                                                       | Unterstützt           |
|------------------------------------------------------------------------------------|---------------------|
| [Shadermodell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) und höhere Shadermodelle | Nein                  |
| [Shadermodell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | ja (nur tx \_ \_ 1 0) |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Systeminterne Funktionen (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

