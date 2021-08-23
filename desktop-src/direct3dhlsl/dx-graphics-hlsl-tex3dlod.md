---
title: tex3Dlod
description: Probieren Sie eine 3D-Textur mit Mipmaps aus. Die Mipmap-LOD wird in t.w angegeben.
ms.assetid: 9bdd8fa1-8c02-4765-8f4d-61ceb532354e
keywords:
- tex3Dlod HLSL
topic_type:
- apiref
api_name:
- tex3Dlod
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 787a9d9fff3fd997fc56a7b5820a81b4b6ab004882f378745a1c044ab6156f26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119904"
---
# <a name="tex3dlod"></a>tex3Dlod

Probieren Sie eine 3D-Textur mit Mipmaps aus. Die Mipmap-LOD wird in t.w angegeben.



| ret tex3Dlod(s, t) |
|--------------------|



 

## <a name="parameters"></a>Parameter



| Element                                                   | Beschreibung                               |
|--------------------------------------------------------|-------------------------------------------|
| <span id="s"></span><span id="S"></span>*s*<br/> | \[im \] Samplerzustand.<br/>      |
| <span id="t"></span><span id="T"></span>*T*<br/> | \[in \] Die Texturkoordinate.<br/> |



 

## <a name="return-value"></a>Rückgabewert

Der Wert der Texturdaten.

## <a name="type-description"></a>Typbeschreibung



| Name | Ein/Aus | [**Vorlagentyp**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Komponententyp**](dx-graphics-hlsl-intrinsic-functions.md) | Size |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| s    | in     | [**Objekt (object)**](dx-graphics-hlsl-intrinsic-functions.md) | [sampler3D](dx-graphics-hlsl-sampler.md)                      | 1    |
| t    | in     | [**Vektor**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 4    |
| Ret  | out    | [**Vektor**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 4    |



 

## <a name="minimum-shader-model"></a>Shader-Mindestmodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                              | Unterstützt               |
|-----------------------------------------------------------|-------------------------|
| [Shadermodell 4](dx-graphics-hlsl-sm4.md)                | ja (nur Pixelshader) |
| [Shadermodell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | ja (nur Pixelshader) |
| [Shadermodell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | Nein                      |
| [Shadermodell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | Nein                      |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Systeminterne Funktionen (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

