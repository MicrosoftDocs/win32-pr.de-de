---
title: texm3x2depth-PS
description: Berechnen Sie den Tiefen Wert, der für den tiefen Test für dieses Pixel verwendet werden soll.
ms.assetid: bacdd471-a6ee-4998-badd-93ffd4fd61d4
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 26d2c3efd1a31681520828b18d606d618d8c900a
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104976385"
---
# <a name="texm3x2depth---ps"></a>texm3x2depth-PS

Berechnen Sie den Tiefen Wert, der für den tiefen Test für dieses Pixel verwendet werden soll.

## <a name="syntax"></a>Syntax



| texm3x2depth DST, src |
|-----------------------|



 

where

-   DST ist das Ziel Register.
-   src ist ein Quell Register.

## <a name="remarks"></a>Bemerkungen



| Pixel-Shader-Versionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texm3x2depth          |      |      | x    |      |      |      |       |      |       |



 

Diese Anweisung muss mit der [texm3x2pad-PS-](texm3x2pad---ps.md) Anweisung verwendet werden.

Bei Verwendung dieser beiden Anweisungen müssen Textur Register die folgende Sequenz verwenden.


```
 
tex t(n)                     // Define tn as a standard 3-vector.(tn must be 
                             // defined in some way before it is used
texm3x2pad   t(m),   t(n)    // Where m > n
                             // Calculate z value
texm3x2depth t(m+1), t(n)    // Calculate w value; use both z and w to
                             // find depth
```



Die tiefen Berechnung erfolgt nach dem Verwenden eines Punktprodukt Vorgangs, um z und w zu suchen. Im folgenden finden Sie weitere Details dazu, wie die tiefen Berechnung durchgeführt wird.

Die texm3x2pad-Anweisung berechnet z.

z = TextureCoordinates (Stufe m)<sub>UVW</sub> \* t (n)<sub>RGB</sub>

Die texm3x2depth-Anweisung berechnet w.

w = TextureCoordinates (Phase m + 1)<sub>UVW</sub> \* t (n)<sub>RGB</sub>

Berechnen Sie die Tiefe, und speichern Sie das Ergebnis in t (m + 1).


```
 
if (w == 0)
  t(m+1) = 1.0
else
  t(m+1) = z/w
```



Die berechnete Tiefe wird so gekennzeichnet, dass Sie im tiefen Test für das Pixel verwendet wird, wobei der vorhandene tiefen Testwert für das Pixel ersetzt wird.

Stellen Sie sicher, dass z/w im Bereich von (0-1) liegt. Wenn z/w außerhalb dieses Bereichs liegt, wird das im tiefen Puffer gespeicherte Ergebnis nicht definiert.

Nach dem Ausführen von texm3x2depth steht Register t (m + 1) nicht mehr zur Verwendung im Shader zur Verfügung.

Wenn Sie mit dieser Anweisung eine Multisampling-Anweisung verwenden, entfällt der größte Vorteil des tiefen Puffers höherer Auflösung. Da der Pixelshader einmal pro Pixel ausgeführt wird, wird der einzelne tiefen Wert, der von texm3x2depth oder [textiefe-PS](texdepth---ps.md) ausgegeben wird, für jeden Vergleichstest des Subpixels-tiefen Werts verwendet.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixelshaderanweisungen](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




