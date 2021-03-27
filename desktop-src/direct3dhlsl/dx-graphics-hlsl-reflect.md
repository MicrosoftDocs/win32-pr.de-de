---
title: widerzuspiegeln
description: Gibt einen Reflektionsvektor mit einem incidentray und einem Oberflächen normalen zurück.
ms.assetid: e321b399-f382-4585-83a6-a7da1f7b2327
keywords:
- HLSL reflektieren
topic_type:
- apiref
api_name:
- reflect
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 46c981f636a797ecc4e0dd341ce44ed886c202cb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729928"
---
# <a name="reflect"></a>widerzuspiegeln

Gibt einen Reflektionsvektor mit einem incidentray und einem Oberflächen normalen zurück.



| *ret* reflektieren (*i*, *n*) |
|-------------------------|



 

## <a name="parameters"></a>Parameter



| Element                                                   | BESCHREIBUNG                                          |
|--------------------------------------------------------|------------------------------------------------------|
| <span id="i"></span><span id="I"></span>*Ich*<br/> | \[in \] einem Gleit Komma-und incidentvektor.<br/> |
| <span id="n"></span><span id="N"></span>*Nr*<br/> | \[in \] einem Gleit Komma-, normal-Vektor.<br/>   |



 

## <a name="return-value"></a>Rückgabewert

Ein Gleit Komma Wert, reflektionvektor.

## <a name="remarks"></a>Bemerkungen

Diese Funktion berechnet den Reflektionsvektor mithilfe der folgenden Formel: v = i-2 \* n \* Punkt (i n).

## <a name="type-description"></a>Typbeschreibung



| Name  | [**Vorlagentyp**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Komponententyp**](dx-graphics-hlsl-intrinsic-functions.md) | Size                           |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *i*   | [**ve**](dx-graphics-hlsl-intrinsic-functions.md) | [**Hafen**](/windows/desktop/WinProg/windows-data-types)                        | any                            |
| *n*   | [**ve**](dx-graphics-hlsl-intrinsic-functions.md) | [**Hafen**](/windows/desktop/WinProg/windows-data-types)                        | gleiche Dimension (n) wie Eingabe *i* |
| *TZI* | [**ve**](dx-graphics-hlsl-intrinsic-functions.md) | [**Hafen**](/windows/desktop/WinProg/windows-data-types)                        | gleiche Dimension (n) wie Eingabe *i* |



 

## <a name="minimum-shader-model"></a>Minimaler Shader-Modell

Diese Funktion wird in den folgenden shadermodellen unterstützt.



| Shadermodell                                                                       | Unterstützt |
|------------------------------------------------------------------------------------|-----------|
| [Shader Model 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) und höhere Shader-Modelle | ja       |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Intrinsische Funktionen (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

