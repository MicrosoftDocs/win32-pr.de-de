---
title: tex2Dlod
description: Stichproben eine 2D-Textur mit Mipmaps. Die Mipmap-LOD wird in t.w. angegeben.
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
ms.openlocfilehash: f63a922fe86dc10d984369a1a872f84089b4db34
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104976648"
---
# <a name="tex2dlod"></a>tex2Dlod

Stichproben eine 2D-Textur mit Mipmaps. Die Mipmap-LOD wird in t.w. angegeben.



| Ret tex2Dlod (s, t) |
|--------------------|



 

## <a name="parameters"></a>Parameter



| Element                                                   | BESCHREIBUNG                               |
|--------------------------------------------------------|-------------------------------------------|
| <span id="s"></span><span id="S"></span>*Hymnen*<br/> | \[im \] samplerzustand.<br/>      |
| <span id="t"></span><span id="T"></span>*Bund*<br/> | \[in \] der Textur Koordinate.<br/> |



 

## <a name="return-value"></a>Rückgabewert

Der Wert der Textur Daten.

## <a name="type-description"></a>Typbeschreibung



| Name | Ein/Aus | [**Vorlagentyp**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Komponententyp**](dx-graphics-hlsl-intrinsic-functions.md) | Size |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| s    | in     | [**Objekt**](dx-graphics-hlsl-intrinsic-functions.md) | [sampler2D](dx-graphics-hlsl-sampler.md)                      | 1    |
| t    | in     | [**ve**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 4    |
| TZI  | out    | [**ve**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 4    |



 

## <a name="minimum-shader-model"></a>Minimaler Shader-Modell

Diese Funktion wird in den folgenden shadermodellen unterstützt.



| Shadermodell                                                                       | Unterstützt |
|------------------------------------------------------------------------------------|-----------|
| [Shader Model 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) und höhere Shader-Modelle | ja       |
| [Shader-Modell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md)                          | nein        |
| [Shader-Modell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | nein        |



 

## <a name="remarks"></a>Bemerkungen

Ab Direct3D 10 können Sie die neue HLSL-Syntax verwenden, um auf Texturen und andere Ressourcen zuzugreifen. Sie können systemeigene Textur Suchfunktionen, wie z. b. **tex2Dlod**, durch einen stärker objektorientierten Stil ersetzen. In diesem objektorientierten Stil sind Texturen von Samplern entkoppelt und verfügen über Methoden zum Laden und Sampling.

Beispiel für eine 2D-Textur, anstatt **tex2Dlod** wie in diesem Code zu verwenden:


```
sampler S;
...
color = tex2Dlod(S, Location);
```



Verwenden Sie die [samplelevel](dx-graphics-hlsl-to-samplelevel.md) -Methode eines [**Textur Objekts**](dx-graphics-hlsl-to-type.md) wie in diesem Code:


```
Texture2D MyTexture;
SamplerState MySampler;
...
color = MyTexture.SampleLevel(MySampler, Location, LOD);
```



Um die Funktionen für die Textur Suche im systeminternen Stil, wie z. b. **tex2Dlod**, mit [Shader Model 4](dx-graphics-hlsl-sm4.md) und höher zu verwenden, verwenden Sie [**D3DCOMPILE \_ enable abwärts \_ \_ Compatibility**](d3dcompile-constants.md) to compile. Wenn Sie jedoch Shader Model 4 und höher (auch [ \* \_ 4 \_ 0 \_ Ebene \_ 9 \_ \* ](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro)) mit neueren, objektorientierten Stil Code als Ziel haben möchten, migrieren Sie zur neueren HLSL-Syntax.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Intrinsische Funktionen (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

