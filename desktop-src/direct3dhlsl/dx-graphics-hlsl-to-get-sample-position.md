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
ms.openlocfilehash: 95be6d9b6c4cbf70aed059399af0892a3c75f0a3462b6ef2b0732e8180f4e123
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068110"
---
# <a name="getsampleposition-directx-hlsl-texture-object"></a>GetSamplePosition (DirectX HLSL-Texturobjekt)

Ruft die Position des angegebenen Beispiels ab.

ret Object.GetSamplePosition( int s );



 

## <a name="parameters"></a>Parameter



| Element                                                                                           | BESCHREIBUNG                                                                                         |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span id="Object"></span><span id="object"></span><span id="OBJECT"></span>*Objekt*<br/> | Ein Texture2DMS- oder Texture2DMSArray-Texturobjekttyp. [](dx-graphics-hlsl-to-type.md)<br/> |
| <span id="s"></span><span id="S"></span>*s*<br/>                                         | \[in \] Der nullbasierte Beispielindex.<br/>                                                      |



 

## <a name="return-value"></a>Rückgabewert

Gibt die (x,y)-Beispielposition zurück, einen Gleitkommavektor mit zwei Komponenten.

## <a name="minimum-shader-model"></a>Shader-Mindestmodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| Vs \_ 4 \_ 0 | Vs \_ 4 \_ 1  | ps \_ 4 \_ 0 | ps \_ 4 \_ 1  | gs \_ 4 \_ 0 | gs \_ 4 \_ 1  |
|----------|-----------|----------|-----------|----------|-----------|
|          | x         |          | x         |          | x         |



 

-   Shadermodell 4.1 ist in Direct3D 10.1 oder höher verfügbar.

## <a name="remarks"></a>Hinweise

Ein Pixel-Shader kann mit abtastender Frequenz ausgewertet werden (einmal pro Stichprobe einen Pixel-Shader ausführen) oder mit Pixelfrequenz (einmal pro Pixel einen Pixelshader ausführen). Fügen Sie die \_ SEmantik SV SampleIndex an eine Pixel-Shadereingabe an, um einen Pixelshader bei der Stichprobenhäufigkeit aufzurufen. Der Eingabewert wird dann als Beispielindex beim Sampling des Renderziels verwendet.

Sie können eine Pixel-Shadereingabe auf verschiedene Weise interpolieren. So interpolieren Sie unter:

-   Ein Pixelmittelpunkt, verwenden Sie keine Semantik.
-   In einem Beispiel wird die \_ SEmantik SV SampleIndex verwendet.
-   Verwenden Sie den [ \_ Schwerpunktmodifizierer](dx-graphics-hlsl-struct.md) als Schwerpunktspeicherort.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Texturobjekt](dx-graphics-hlsl-to-type.md)
</dt> </dl>

 

 





