---
title: ftou (SM4-ASM)
description: Gleit Komma Wert Konvertierung ohne Vorzeichen.
ms.assetid: 0E3E090B-72C0-4CED-AFA5-2DDCF67D7263
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4a5e65e4bb9d4e71e4a2000f00861cf63e7c181
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104313644"
---
# <a name="ftou-sm4---asm"></a>ftou (SM4-ASM)

Gleit Komma Wert Konvertierung ohne Vorzeichen.



| ftou dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle\] |
|----------------------------------------------------|



 



| f: dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle\] |
|----------------------------------------------------|



 



| Element                                                            | BESCHREIBUNG                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[in \] der Adresse des Vorgangs Ergebnisses. <br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] dem zu konvertierenden Wert.<br/>                        |



 

## <a name="remarks"></a>Bemerkungen

Die Konvertierung erfolgt pro Komponente. Die Rundung erfolgt immer in Richtung 0 (null) und folgt der C-Konvention für Umwandlungen von float in int.

Anwendungen, die eine andere Rundungs Semantik erfordern, können die **runden** Anweisungen vor dem umwandeln in eine ganze Zahl aufrufen.

Eingaben werden an den Bereich \[ 0,0 f... 4294967295.999 f \] vor der Konvertierung, und Eingabe-NaN-Werte führen zu einem Ergebnis von NULL.

Optionale Modifizierer Negation und absolute Werte werden vor der Konvertierung auf die Quell Werte angewendet.

Diese Anweisung gilt für die folgenden Shader-Phasen:



| Vertexshader | Geometrie-Shader | Pixelshader |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Minimaler Shader-Modell

Diese Funktion wird in den folgenden shadermodellen unterstützt.



| Shadermodell                                              | Unterstützt |
|-----------------------------------------------------------|-----------|
| [Shader-Modell 5](d3d11-graphics-reference-sm5.md)        | ja       |
| [Shadermodell 4,1](dx-graphics-hlsl-sm4.md)              | ja       |
| [Shadermodell 4](dx-graphics-hlsl-sm4.md)                | ja       |
| [Shader-Modell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | nein        |
| [Shader-Modell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | nein        |
| [Shader-Modell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | nein        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shader Model 4-Assembly (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





