---
title: Clip
description: Verwirft das aktuelle Pixel, wenn der angegebene Wert kleiner als 0 (null) ist.
ms.assetid: c9f84a27-5572-45aa-a12f-4446614b7be5
keywords:
- HLSL-Clip
topic_type:
- apiref
api_name:
- clip
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 92a75f2839dbbb605d976e07fffa5c2f9b27fd86
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104976720"
---
# <a name="clip"></a>Clip

Verwirft das aktuelle Pixel, wenn der angegebene Wert kleiner als 0 (null) ist.



| Clip (*x*) |
|-----------|



 

## <a name="parameters"></a>Parameter



| Element                                                   | BESCHREIBUNG                            |
|--------------------------------------------------------|----------------------------------------|
| <span id="x"></span><span id="X"></span>*Stuben*<br/> | \[im \] angegebenen Wert.<br/> |



 

## <a name="return-value"></a>Rückgabewert

Keine.

## <a name="remarks"></a>Hinweise

Verwenden Sie die intrinsische Funktion **Clip** HLSL, um Clippingebenen zu simulieren, wenn jede Komponente des *x* -Parameters den Abstand von einer Ebene darstellt.

Verwenden Sie außerdem die **Clip** -Funktion, um das Alpha-Verhalten zu testen, wie im folgenden Beispiel gezeigt:


```
clip( Input.Color.A < 0.1f ? -1:1 );
```



## <a name="type-description"></a>Typbeschreibung



| Name | [**Vorlagentyp**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Komponententyp**](dx-graphics-hlsl-intrinsic-functions.md) | Size |
|------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| *x*  | [**Skalar**](dx-graphics-hlsl-intrinsic-functions.md), **Vektor** oder **Matrix** | [**Hafen**](/windows/desktop/WinProg/windows-data-types)                        | any  |



 

## <a name="minimum-shader-model"></a>Minimaler Shader-Modell

Diese Funktion wird in den folgenden shadermodellen unterstützt.



| Shadermodell                                              | Unterstützt               |
|-----------------------------------------------------------|-------------------------|
| [Shadermodell 4](dx-graphics-hlsl-sm4.md)                | Ja (nur Pixel-Shader) |
| [Shader-Modell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | Ja (nur Pixel-Shader) |
| [Shader-Modell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | Ja (nur Pixel-Shader) |
| [Shader-Modell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | Ja (nur Pixel-Shader) |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Intrinsische Funktionen (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

