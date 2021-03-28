---
title: Getsampleposition (DirectX HLSL-Textur Objekt)
description: Ruft die Position des angegebenen Beispiels ab.
ms.assetid: 4e622b85-82d6-4339-b03a-becbe5f9aa57
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 062bf08064faf112fdc1efe5b371fcad72efeeea
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104389496"
---
# <a name="getsampleposition-directx-hlsl-texture-object"></a>Getsampleposition (DirectX HLSL-Textur Objekt)

Ruft die Position des angegebenen Beispiels ab.



|                                        |
|----------------------------------------|
| Ret Object. getsampleposition (int s); |



 

## <a name="parameters"></a>Parameter



| Element                                                                                           | BESCHREIBUNG                                                                                         |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Objekt*<br/> | Ein Texture2DMS-oder Texture2DMSArray [-Textur-Objekttyp](dx-graphics-hlsl-to-type.md) .<br/> |
| <span id="s"></span><span id="S"></span>*Hymnen*<br/>                                         | \[im \] NULL basierten Beispiel Index.<br/>                                                      |



 

## <a name="return-value"></a>Rückgabewert

Gibt die Beispiel Position (x, y), einen Gleit Komma Vektor mit zwei Komponenten, zurück.

## <a name="minimum-shader-model"></a>Minimaler Shader-Modell

Diese Funktion wird in den folgenden shadermodellen unterstützt.



| vs \_ 4 \_ 0 | vs \_ 4 \_ 1  | PS \_ 4 \_ 0 | PS \_ 4 \_ 1  | GS \_ 4 \_ 0 | GS \_ 4 \_ 1  |
|----------|-----------|----------|-----------|----------|-----------|
|          | x         |          | x         |          | x         |



 

-   Das Shader-Modell 4,1 ist in Direct3D 10,1 oder höher verfügbar.

## <a name="remarks"></a>Bemerkungen

Ein Pixelshader kann bei der Stichproben Häufigkeit (Ausführen eines Pixelshaders einmal pro Stichprobe) oder bei Pixel Häufigkeit (Ausführen eines Pixel-Shader einmal pro Pixel) ausgewertet werden. Fügen Sie die \_ Semantik "SV sampleindex" an eine Pixel-Shadereingabe an, um einen PixelShader bei der Stichproben Häufigkeit aufzurufen. der Eingabe Wert wird dann als Beispiel Index verwendet, wenn das Rendern des Renderziels

Sie können eine Pixel-Shadereingabe auf verschiedene Weise interpolieren. So interpolieren Sie an:

-   Ein Pixel Center verwendet keine Semantik.
-   Beispiel: Verwenden Sie die \_ Semantik "SV samplindex".
-   Einen Schwerpunkt Speicherort verwenden Sie den [ \_ Schwerpunkt](dx-graphics-hlsl-struct.md) -Modifizierer.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Texture-Objekt](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 





