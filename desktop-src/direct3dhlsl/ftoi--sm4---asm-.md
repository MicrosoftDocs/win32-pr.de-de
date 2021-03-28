---
title: 'ftoi (sm4 – asm) '
description: Gleit Komma Zahl Konvertierungen mit Vorzeichen.
ms.assetid: 580AB4A6-0C1C-409B-B2B9-BA1D37772F46
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c02ce1b506d112a59d3087f59d219557575b8def
ms.sourcegitcommit: 8c658e9872a2173e3dcec94195f9067fbcd85d3d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/17/2020
ms.locfileid: "104316670"
---
# <a name="ftoi-sm4---asm"></a>ftoi (sm4 – asm) 

Gleit Komma Zahl Konvertierungen mit Vorzeichen.

| f: dest \[ . mask \] , \[ - \] src0 \[ \_ ABS \] \[ . Swizzle\] |
|-|

| Element | BESCHREIBUNG |
|-|-|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[in \] der Adresse des Vorgangs Ergebnisses.<br/> *dest*  =  [Round \_ z](round-z--sm4---asm-.md)(*src0*)<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] der zu konvertierenden Komponente.<br/> |

## <a name="remarks"></a>Bemerkungen

Die Konvertierung erfolgt pro Komponente. Die Rundung erfolgt immer in Richtung 0 (null) und folgt der C-Konvention für Umwandlungen von float in int. Anwendungen, die eine andere Rundungs Semantik erfordern, können die **runden** Anweisungen vor dem umwandeln in eine ganze Zahl aufrufen.

Eingaben werden an den Bereich \[ 2147483648.999 f... 2147483647.999 f \] vor der Konvertierung, und Eingabe-NaN-Werte führen zu einem Ergebnis von NULL.

Optionale Modifizierer Negation und absolute Werte werden vor der Konvertierung auf die Quell Werte angewendet.

Diese Anweisung gilt für die folgenden Shader-Phasen:

| Vertexshader | Geometrie-Shader | Pixelshader |
|-|-|-|
| x | x | x |

## <a name="minimum-shader-model"></a>Minimaler Shader-Modell

Diese Funktion wird in den folgenden shadermodellen unterstützt.

| Shadermodell | Unterstützt |
|-|-|
| [Shader-Modell 5](d3d11-graphics-reference-sm5.md) | ja |
| [Shadermodell 4,1](dx-graphics-hlsl-sm4.md) | ja |
| [Shadermodell 4](dx-graphics-hlsl-sm4.md) | ja |
| [Shader-Modell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | nein |
| [Shader-Modell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | nein |
| [Shader-Modell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | nein |

## <a name="related-topics"></a>Zugehörige Themen

[Shader Model 4-Assembly (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
