---
description: Schattenvolumes werden zum Zeichnen von Schatten mit dem Schablonenpuffer verwendet.
ms.assetid: 8b71d871-ee66-47c4-8190-5c75419b28b2
title: Two-Sided Schablone (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95bca0b960f96d1747b2b7ad51771276df2cfe1da1fa8ac9aa4d7c1ce8ea7c03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118290510"
---
# <a name="two-sided-stencil-direct3d-9"></a>Two-Sided Schablone (Direct3D 9)

Schattenvolumes werden zum Zeichnen von Schatten mit dem Schablonenpuffer verwendet. Die Anwendung berechnet die Schattenvolumen, die durch verdeckende Geometrie umgewandelt werden, indem die Kanten der Kanten berechnet und vom Licht weg in eine Reihe von 3D-Volumes zusammengestellt werden. Diese Volumes werden dann zweimal in den Schablonenpuffer gerendert.

Das erste Rendern zeichnet vorwärts gerichtete Polygone und erhöht die Schablonenpufferwerte. Das zweite Rendern zeichnet die rückwärts gerichteten Polygone des Schattenvolumens und dekrementiert die Schablonenpufferwerte. Normalerweise brechen sich alle inkrementierten und dekrementierten Werte gegenseitig ab. Die Szene wurde jedoch bereits mit normaler Geometrie gerendert, sodass einige Pixel beim Z-Puffertest fehlschlagen, wenn das Schattenvolumen gerendert wird. Die werte, die im Schablonenpuffer übrig bleiben, entsprechen den Pixeln im Schatten. Diese verbleibenden Schablonenpufferinhalte werden als Maske verwendet, um ein großes, allumfassendes schwarzes Quader alphanumerierend in die Szene einzublenden. Wenn der Schablonenpuffer als Maske fungiert, besteht das Ergebnis darin, Pixel in den Schatten zu dunkler zu machen.

Dies bedeutet, dass die Schattengeometrie zweimal pro Lichtquelle gezeichnet wird, was den Scheitelpunktdurchsatz der GPU unter Druck setzt. Die zweiseitige Schablonenfunktion wurde entwickelt, um diese Situation zu entschärfen. Bei diesem Ansatz gibt es zwei Sätze des Schablonenzustands (unten benannt), eine für die vorderen Dreiecke und die andere für die hinteren Dreiecke. Auf diese Weise wird nur ein einzelner Durchlauf pro Schattenvolumen pro Licht gezeichnet.

Die API-Änderungen sind auf einen neuen Satz von Renderzuständen beschränkt. Der neue Renderzustand D3DRS \_ Two \_ Sided \_ StencilMODE kann auf **TRUE** oder **FALSE** festgelegt werden. Standardmäßig ist **es FALSE,** d.h. das aktuelle Verhalten (DirectX 8). Wenn diese Einstellung auf **TRUE** festgelegt ist (dies funktioniert nur, wenn D3DSTENCILCAPS \_ TWOSIDED festgelegt ist), gelten die folgenden Renderzustände nur für die vorderen Dreiecke (im Uhrzeigersinn).



| Renderzustand        | Beschreibung                                                                              |
|---------------------|------------------------------------------------------------------------------------------|
| D3DRS \_ STENCILFAIL  | D3DSTENCILOP, wenn der Schablonentest fehlschlägt.                                                |
| D3DRS \_ STENCILZFAIL | D3DSTENCILOP, wenn der Schablonentest erfolgreich war und z-test fehlschlägt.                              |
| D3DRS \_ STENCILPASS  | D3DSTENCILOP, wenn Schablonen- und Z-Tests erfolgreich sind.                                     |
| D3DRS \_ STENCILFUNC  | D3DCMPFUNC fn. Der Schablonentest ist erfolgreich, wenn ((ref & mask) stencilfn (stencil & mask)) true ist. |



 

Ein neuer Satz von Renderzuständen gilt für die rückwärts gerichteten Dreiecke (gegen den Uhrzeigersinn).



| Renderzustand             | Beschreibung                                                                                    |
|--------------------------|------------------------------------------------------------------------------------------------|
| D3DRS \_ CCW \_ STENCILFAIL  | D3DSTENCILOP, wenn der Schablonentest fehlschlägt.                                                      |
| D3DRS \_ CCW \_ STENCILZFAIL | D3DSTENCILOP, wenn der Schablonentest erfolgreich war und z-test fehlschlägt.                                    |
| D3DRS \_ CCW \_ STENCILPASS  | D3DSTENCILOP, wenn Schablonen- und Z-Tests erfolgreich sind.                                           |
| D3DRS \_ CCW \_ STENCILFUNC  | D3DCMPFUNC-Funktion. Der Schablonentest ist erfolgreich, wenn ((ref & Mask) stencilfn (stencil & mask)) true ist. |



 

Die verbleibenden Schablonenrenderzustände gelten immer für Dreiecke im Uhrzeigersinn und gegen den Uhrzeigersinn.

D3DRS \_ Two \_ Sided \_ StencilMODE wird für Linien und Punkt-Sprites ignoriert, was bedeutet, dass das Verhalten von DirectX 8 nicht geändert wird. Die D3DRS \_ CCW \_ STENCIL-Renderzustände \* werden ignoriert.

Ein neues Cap-Bit gibt an, ob das Gerät dieses Feature unterstützt. Es wird erwartet, dass Treiber, die dieses Feature nicht unterstützen, diese neuen Renderzustände ignorieren. Alle anderen Schablonen-Cap-Bits gelten für beide Modi der Schablonenpufferung. Da Two \_ Sided \_ Stencil die Fähigkeit impliziert, mit D3DCULLMODE \_ NONE zu zeichnen, muss die entsprechende Obergrenze vom Treiber festgelegt werden, wenn dieser neue Schablonenmodus unterstützt wird. Microsoft Windows Hardware Quality Labs (WHQL) sollte dies erzwingen.

Neue Renderzustände:


```
D3DRS_Two_Sided_StencilMODE // BOOL (default is FALSE)
D3DRS_CCW_STENCILFAIL     // Same default as D3DRS_STENCILFAIL
D3DRS_CCW_STENCILZFAIL    // Same default as D3DRS_STENCILZFAIL
D3DRS_CCW_STENCILPASS     // Same default as D3DRS_STENCILPASS
D3DRS_CCW_STENCILFUNC     // Same default as D3DRS_STENCILFUNC
```



Neue Obergrenze:


```
D3DSTENCILCAPS_TWOSIDED // a flag on D3DCAPS9.StencilCaps
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Schablonenpuffertechniken](stencil-buffer-techniques.md)
</dt> <dt>

[**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)
</dt> </dl>

 

 
