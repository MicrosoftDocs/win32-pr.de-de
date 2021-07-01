---
title: GetSamplePosition (DirectX HLSL-Texturobjekt)
description: Ruft die Position des angegebenen Beispiels ab.
ms.assetid: 4e622b85-82d6-4339-b03a-becbe5f9aa57
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9a1e5f4dc71d5af2e7973ef180c919a49e65ef81
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118585"
---
# <a name="getsampleposition-directx-hlsl-texture-object"></a>GetSamplePosition (DirectX HLSL-Texturobjekt)

Ruft die Position des angegebenen Beispiels ab.

ret Object.GetSamplePosition( int s );



 

## <a name="parameters"></a>Parameter



| Element                                                                                           | Beschreibung                                                                                         |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Objekt*<br/> | Ein Texture2DMS- oder ein Texture2DMSArray-Texturobjekttyp. [](dx-graphics-hlsl-to-type.md)<br/> |
| <span id="s"></span><span id="S"></span>*s*<br/>                                         | \[in \] Der nullbasierte Beispielindex.<br/>                                                      |



 

## <a name="return-value"></a>Rückgabewert

Gibt die (x,y)-Beispielposition zurück, einen Gleitkommavektor mit zwei Komponenten.

## <a name="minimum-shader-model"></a>Minimales Shadermodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| vs \_ 4 \_ 0 | vs \_ 4 \_ 1  | ps \_ 4 \_ 0 | ps \_ 4 \_ 1  | gs \_ 4 \_ 0 | gs \_ 4 \_ 1  |
|----------|-----------|----------|-----------|----------|-----------|
|          | x         |          | x         |          | x         |



 

-   ShaderModell 4.1 ist in Direct3D 10.1 oder höher verfügbar.

## <a name="remarks"></a>Bemerkungen

Ein Pixel-Shader kann mit der Abtastfrequenz (einmal pro Beispiel einen Pixels shader ausführen) oder mit Pixelfrequenz (einmal pro Pixel ausführen) ausgewertet werden. Fügen Sie die SV SampleIndex-Semantik an eine Pixel-Shadereingabe an, um einen Pixel-Shader mit Samplinghäufigkeit aufzurufen. Der Eingabewert wird dann als Beispielindex verwendet, wenn das Renderziel samplingt \_ wird.

Sie können eine Pixel-Shadereingabe auf verschiedene Weise interpolieren. So interpolieren Sie unter:

-   Ein Pixelzentriert, verwenden Sie keine Semantik.
-   Ein Beispiel: Verwenden Sie die SV \_ SampleIndex-Semantik.
-   Verwenden Sie als Schwerpunktposition den [ \_ Modifizierer "schwerpunkt".](dx-graphics-hlsl-struct.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Texture-Object](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 





