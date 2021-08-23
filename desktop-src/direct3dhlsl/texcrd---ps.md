---
title: texcrd – ps
description: Kopiert Texturkoordinatendaten aus dem Iteratorregister der Quelltexturkoordinate als Farbdaten im Zielregister.
ms.assetid: b3330d70-6e18-4494-a01c-51f0a282e305
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 795dacbec01abdfa49527e36fefc9194a6168a99c1d9ab425b30f987e5445096
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118506426"
---
# <a name="texcrd---ps"></a>texcrd – ps

Kopiert Texturkoordinatendaten aus dem Iteratorregister der Quelltexturkoordinate als Farbdaten im Zielregister.

## <a name="syntax"></a>Syntax



| texcrd dst, src |
|-----------------|



 

where

-   dst ist das Zielregister.
-   src ist ein Quellregister.

## <a name="remarks"></a>Hinweise



| Pixel-Shaderversionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texcrd                |      |      |      | x    |      |      |       |      |       |



 

Diese Anweisung interpretiert Koordinatendaten als Farbdaten (RGBA).

Von dieser Anweisung wird keine Textur entnommen. Nur Texturkoordinaten, die in dieser Texturphase festgelegt sind, sind relevant.

Beachten Sie bei verwendung von texcrd die folgenden Details dazu, wie Daten aus dem Quellregister in das Zielregister kopiert werden. Das Quelltexturkoordinatenregister (t) enthält Daten im Bereich \# \[ -D3DCAPS9. MaxTextureRepeat, D3DCAPS9. MaxTextureRepeat , während das Zielregister (r ) Daten nur im (wahrscheinlich kleineren) Bereich \] \# \[ –D3DCAPS9 halten kann. PixelShader1xMaxValue, D3DCAPS9. PixelShader1xMaxValue \] . Beachten Sie, dass für Pixel-Shader, Version 1 \_ 4, D3DCAPS9. PixelShader1xMaxValue muss mindestens acht sein. Die texcrd-Anweisung verhält sich bei der Klammer von Quelldaten, die sich nicht im Zielregister befindet, auf unterschiedlicher Hardware wahrscheinlich anders. Die erste Pixel-Shader-Hardware der Version 1 4 auf dem Markt führt eine spezielle Klammer für Werte außerhalb \_ des Bereichs aus. Diese Klammer wurde entwickelt, um eine Zahl zu erzeugen, die in das Zielregister passen kann, aber auch, um das Textur adressierungsverhalten für Daten zu erhalten, die nicht im Bereich liegen (siehe [**D3DTEXTUREADDRESS),**](/windows/desktop/direct3d9/d3dtextureaddress)wenn die Daten anschließend für texturbasierte Stichprobenentnahme verwendet werden sollen. Neue Hardware von verschiedenen Herstellern weist dieses Verhalten jedoch möglicherweise nicht auf und drosselt möglicherweise nur Daten, um den Zielregisterbereich zu erreichen. Daher ist die sicherste Methode bei Der Verwendung von Pixel-Shader Version 1 4 texcrd besteht in der Bereitstellung von Texturkoordinatendaten nur in dem Pixel-Shader, der sich bereits im Bereich \_ \[ -8,8 befindet, sodass Sie sich nicht auf die Art der Hardware-Klammern \] verlassen.

Im Gegensatz zu texcoord \_ klammert texcrd keine Werte zwischen 0 und 1.

Regeln für die Verwendung von texcrd:

1.  Der gleiche Modifizierer ".xyz" oder ".xyw" muss auf jeden Leses eines einzelnen t(n)-Registers innerhalb einer texcrd- oder texld-Anweisung angewendet werden.
2.  Das vierte Kanalergebnis von texcrd ist in allen Fällen nicht festgelegt/nicht definiert.
3.  Der dritte Kanal ist für den Fall xyw dw nicht \_ festgelegt/nicht definiert.

## <a name="examples"></a>Beispiele

Der vollständige Satz zulässiger Syntax für texcrd unter Berücksichtigung aller gültigen Kombinationen aus Quellmodifizierer/-selektor und Ziel-Schreibmaske ist unten dargestellt. Beachten Sie, dass die RGBA- und XYZW-Notation austauschbar verwendet werden können.

Kopiert die ersten drei Kanäle des Texturkoordinaten-Iteratorregisters t(n) in r(m). Der vierte Kanal von r(m) ist nicht initialisiert.


```
texcrd  r(m).rgb, t(n).xyz  

// Produces the same result as the previous instruction
texcrd  r(m).rgb, t(n)
```



Legt die erste, zweite und vierte Komponente von t(n) in die ersten drei Kanäle von r(m) ein. Der vierte Kanal von r(m) ist nicht initialisiert.


```
texcrd  r(m).rgb, t(n).xyw
```



Hier ist ein beispiel für eine projektive Division mit dem \_ dw-Modifizierer.

In diesem Beispiel werden x/w und y/w aus t(n) in die ersten beiden Kanäle von r(m) kopiert. Der dritte und vierte Kanal von r(m) sind nicht initialisiert. Alle Daten, die zuvor in den dritten Kanal von r(m) geschrieben wurden, gehen verloren. Daten im vierten Kanal von r(m) gehen aufgrund des Phasenmarkers verloren. Für Version 1 \_ 4 wird das D3DTTFF \_ PROJECTED-Flag ignoriert.


```
texcrd  r(m).rg,  t(n)_dw.xyw
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anweisungen für Pixel-Shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 