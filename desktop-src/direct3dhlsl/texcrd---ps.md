---
title: texcrd-PS
description: Kopiert Texturkoordinaten Daten aus dem Iterator der Quell Textur Koordinate als Farbdaten im Ziel Register.
ms.assetid: b3330d70-6e18-4494-a01c-51f0a282e305
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e1b7bda7ab06c4af43eaa40393d2c5d64b09d9f4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104993399"
---
# <a name="texcrd---ps"></a>texcrd-PS

Kopiert Texturkoordinaten Daten aus dem Iterator der Quell Textur Koordinate als Farbdaten im Ziel Register.

## <a name="syntax"></a>Syntax



| texcrd DST, src |
|-----------------|



 

where

-   DST ist das Ziel Register.
-   src ist ein Quell Register.

## <a name="remarks"></a>Bemerkungen



| Pixel-Shader-Versionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texcrd                |      |      |      | x    |      |      |       |      |       |



 

Diese Anweisung interpretiert Koordinatendaten als Farbdaten (RGBA).

Von dieser Anweisung wird keine Textur entnommen. Nur für diese Textur Stufe festgelegte Texturkoordinaten sind relevant.

Beachten Sie bei der Verwendung von texcrd die folgenden Details dazu, wie Daten aus dem Quell Register in das Ziel Register kopiert werden. Das Quell Textur-Koordinaten Register (t \# ) enthält Daten im Bereich \[ -D3DCAPS9. MaxTextureRepeat, D3DCAPS9. MaxTextureRepeat \] , während das Ziel Register (r \# ) nur Daten im (wahrscheinlichen kleineren) Bereich enthalten kann, \[ D3DCAPS9. PixelShader1xMaxValue, D3DCAPS9. PixelShader1xMaxValue \] . Beachten Sie, dass für Pixel Shader \_ , Version 1 4, D3DCAPS9. PixelShader1xMaxValue muss mindestens acht sein. Die texcrd-Anweisung bei der Klammer von Quelldaten, die sich außerhalb des Bereichs des Ziel Registers befinden, verhält sich wahrscheinlich auf unterschiedlicher Hardware anders. Die erste Pixel-Shader Version 1 \_ 4 Hardware auf dem Markt führt eine spezielle Klammer für Werte außerhalb des Bereichs aus. Diese Klemme ist darauf ausgelegt, eine Zahl zu schaffen, die in das Ziel Register passt, aber auch, um das Verhalten der Textur Adressierung für außerhalb des Gültigkeits Bereichs stehende Daten beizubehalten (siehe [**D3DTEXTUREADDRESS**](/windows/desktop/direct3d9/d3dtextureaddress)), wenn die Daten anschließend für die Textur Stichprobe verwendet werden sollen. Neue Hardware von unterschiedlichen Herstellern zeigt dieses Verhalten jedoch möglicherweise nicht an und kann nur Daten an den Ziel Registrierungsbereich anpassen. Daher besteht die sicherste Vorgehensweise bei der Verwendung von PixelShader Version 1 \_ 4 texcrd darin, Texturkoordinaten Daten nur in den Pixelshader anzugeben, der sich bereits im Bereich von \[ -8, 8 befindet, \] sodass Sie sich nicht auf die Art und Weise von Hardware Klammern verlassen können.

Anders als texcoord \_ gibt texcrd keine Werte zwischen 0 und 1 an.

Regeln für die Verwendung von texcrd:

1.  Derselbe. XYZ-oder. xyw-Modifizierer muss auf jeden Lesevorgang eines einzelnen t (n)-Registers innerhalb einer texcrd-oder texld-Anweisung angewendet werden.
2.  Das vierte kanalergebnis von texcrd ist in allen Fällen nicht festgelegt/nicht definiert.
3.  Der dritte Kanal ist für den xyw DW-Fall nicht festgelegt/nicht definiert \_ .

## <a name="examples"></a>Beispiele

Der vollständige Satz zulässiger Syntax für texcrd, wobei alle gültigen Kombinationen aus quellmodifizierer/Selektor und Ziel Schreib Maske berücksichtigt werden, ist unten dargestellt. Beachten Sie, dass die. RGBA-und. xyzw-Notation austauschbar verwendet werden kann.

Kopiert die ersten drei Kanäle von Texturkoordinaten iteratorregister, t (n), in r (m). Der vierte Kanal von r (m) ist nicht initialisiert.


```
texcrd  r(m).rgb, t(n).xyz  

// Produces the same result as the previous instruction
texcrd  r(m).rgb, t(n)
```



Legt die ersten, zweiten und vierten Komponenten von t (n) in die ersten drei Kanäle von r (m) ab. Der vierte Kanal von r (m) ist nicht initialisiert.


```
texcrd  r(m).rgb, t(n).xyw
```



Im folgenden finden Sie ein Beispiel für eine Projective Teilung mithilfe des \_ DW-Modifizierers.

In diesem Beispiel werden x/w und y/w aus t (n) in die ersten beiden Kanäle von r (m) kopiert. Der dritte und vierte Kanal von r (m) sind nicht initialisiert. Alle Daten, die zuvor in den dritten Kanal von r (m) geschrieben wurden, gehen verloren. Die Daten im vierten Kanal von r (m) gehen aufgrund des Phasen Markers verloren. Bei Version 1 \_ 4 \_ wird das Flag D3DTTFF projiziert ignoriert.


```
texcrd  r(m).rg,  t(n)_dw.xyw
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixelshaderanweisungen](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 