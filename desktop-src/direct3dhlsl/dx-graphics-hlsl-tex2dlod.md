---
title: tex2Dlod
description: Stichproben einer 2D-Textur mit Mipmaps. Die Mipmap-LOD wird in t.w angegeben.
ms.assetid: 689eff39-f6ac-4c25-8b92-ca68707ae8ad
keywords:
- tex2Dlod HLSL
topic_type:
- apiref
api_name:
- tex2Dlod
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f9581418eb2a3d8736fcd0e125eaafec11494e6b6d5471cef33f9592475d5ec0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117725678"
---
# <a name="tex2dlod"></a>tex2Dlod

Stichproben einer 2D-Textur mit Mipmaps. Die Mipmap-LOD wird in t.w angegeben.



| ret tex2Dlod(s, t) |
|--------------------|



 

## <a name="parameters"></a>Parameter



| Element                                                   | Beschreibung                               |
|--------------------------------------------------------|-------------------------------------------|
| <span id="s"></span><span id="S"></span>*s*<br/> | \[im \] Zustand "Sampler".<br/>      |
| <span id="t"></span><span id="T"></span>*T*<br/> | \[in \] Die Texturkoordinate.<br/> |



 

## <a name="return-value"></a>Rückgabewert

Der Wert der Texturdaten.

## <a name="type-description"></a>Typbeschreibung



| Name | Ein/Aus | [**Vorlagentyp**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Komponententyp**](dx-graphics-hlsl-intrinsic-functions.md) | Size |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| s    | in     | [**Objekt (object)**](dx-graphics-hlsl-intrinsic-functions.md) | [sampler2D](dx-graphics-hlsl-sampler.md)                      | 1    |
| t    | in     | [**Vektor**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 4    |
| Ret  | out    | [**Vektor**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 4    |



 

## <a name="minimum-shader-model"></a>Minimales Shadermodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                                                       | Unterstützt |
|------------------------------------------------------------------------------------|-----------|
| [Shadermodell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) und höhere Shadermodelle | Ja       |
| [Shadermodell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md)                          | Nein        |
| [Shadermodell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | Nein        |



 

## <a name="remarks"></a>Hinweise

Ab Direct3D 10 können Sie mithilfe der neuen HLSL-Syntax auf Texturen und andere Ressourcen zugreifen. Sie können Textursyntitäts-Lookupfunktionen wie **tex2Dlod** durch einen objektorientierteren Stil ersetzen. In diesem objektorientierten Stil werden Texturen von Samplern entkoppelt und verfügen über Methoden zum Laden und Sampling.

Beispiel für eine 2D-Textur anstelle von **tex2Dlod** wie in diesem Code:


```
sampler S;
...
color = tex2Dlod(S, Location);
```



Verwenden Sie [die SampleLevel-Methode](dx-graphics-hlsl-to-samplelevel.md) eines [**Texturobjekts**](dx-graphics-hlsl-to-type.md) wie in diesem Code:


```
Texture2D MyTexture;
SamplerState MySampler;
...
color = MyTexture.SampleLevel(MySampler, Location, LOD);
```



Verwenden Sie [**D3DCOMPILE \_ ENABLE \_ BACKWARDS \_ COMPATIBILITY**](d3dcompile-constants.md) zum Kompilieren, um die Funktionen für die Textursuche im systeminternen Stil wie **tex2Dlod** mit [Shadermodell 4](dx-graphics-hlsl-sm4.md) und höher zu verwenden. Wenn Sie jedoch Shadermodell 4 und höher (sogar [ \* \_ 4 0 Ebene \_ \_ \_ 9) \_ \* ](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro)mit neueren objektorientiertem Stilcode als Ziel verwenden möchten, migrieren Sie zur neueren HLSL-Syntax.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Systeminterne Funktionen (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

