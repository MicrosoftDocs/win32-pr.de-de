---
description: Schattenvolumes werden zum Zeichnen von Schatten mit dem Schablonen Puffer verwendet.
ms.assetid: 8b71d871-ee66-47c4-8190-5c75419b28b2
title: Two-Sided Schablone (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b238c4b778b9894029764032e76b60c476a891a9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106346833"
---
# <a name="two-sided-stencil-direct3d-9"></a>Two-Sided Schablone (Direct3D 9)

Schattenvolumes werden zum Zeichnen von Schatten mit dem Schablonen Puffer verwendet. Die Anwendung berechnet die schattenvolumes, die durch die Schattierung von Geometrie umgewandelt werden, indem die Silhouette-Kanten berechnet und vom Licht in eine Gruppe von 3D-Volumes aufgeteilt werden. Diese Volumes werden dann zweimal im Schablonen Puffer gerendert.

Das erste Rendering zeichnet nach vorne gerichtete Polygone und erhöht die Schablonen Puffer Werte. Das zweite Rendering zeichnet die rückwärts gerichteten Polygone des Schatten Volumens und Dekremente die Schablonen Puffer Werte. Normalerweise brechen alle inkrementierten und dekrementierten Werte einander ab. Die Szene wurde jedoch bereits mit normaler Geometrie gerendert, sodass einige Pixel den z-Puffer-Test nicht bestanden haben, während das Schatten Volume gerendert wird. Werte, die im Schablonen Puffer verbleiben, entsprechen den im Schatten entsprechenden Pixeln. Diese verbleibenden Schablone-Puffer Inhalte werden als Maske verwendet, um einen großen, umfassenden, vier Vierfache in die Szene zu mischen. Wenn der Schablone-Puffer als Maske fungiert, besteht das Ergebnis darin, die Pixel in den Schatten zu verbergen.

Dies bedeutet, dass die Schatten Geometrie zweimal pro Lichtquelle gezeichnet wird und somit den Scheitelpunkt Durchsatz der GPU erhöht. Das zweiseitige Schablonen Feature wurde entwickelt, um diese Situation zu mindern. Bei dieser Vorgehensweise gibt es zwei Sätze von Schablone State (unten genannt), jeweils eine Menge für die Vorder-und die andere für die mit der Rückseite gerichteten Dreiecke. Auf diese Weise wird nur ein einzelner Durchlauf pro Schatten Volume pro Licht gezeichnet.

Die API-Änderungen sind auf einen neuen Satz von Rendering-Zuständen beschränkt. Der neue renderzustand D3DRS der \_ zwei \_ seitige \_ Schablonen Modus kann auf " **true** " oder " **false**" festgelegt werden. Der Standardwert ist **false** . Dies bedeutet das aktuelle Verhalten (DirectX 8). Wenn diese auf **true** festgelegt ist (dies funktioniert nur, wenn D3DSTENCILCAPS \_ twoseitigem festgelegt ist), gelten die folgenden Rendering-Zustände nur für die Front-on-Dreiecke (im Uhrzeigersinn).



| Rendering-Zustand        | BESCHREIBUNG                                                                              |
|---------------------|------------------------------------------------------------------------------------------|
| D3DRS \_ stencilfail  | D3DSTENCILOP, wenn der Schablone-Test fehlschlägt.                                                |
| D3DRS \_ stencilzfail | D3DSTENCILOP, wenn der Schablone-Test erfolgreich verläuft und z-Test fehlschlägt.                              |
| D3DRS \_ stencilpass  | D3DSTENCILOP, wenn sowohl Schablone als auch z-Tests bestanden werden.                                     |
| D3DRS \_ stencilfunc  | D3DCMPFUNC Fn. Der Schablone-Test wird durchlaufen, wenn ((Ref & Mask) stencilfn (Schablone & Mask)) "true" ist. |



 

Ein neuer Satz von Rendering-Zuständen gilt für die nach hinten gerichteten Dreiecke (gegen den Uhrzeigersinn).



| Rendering-Zustand             | BESCHREIBUNG                                                                                    |
|--------------------------|------------------------------------------------------------------------------------------------|
| D3DRS \_ CCW \_ stencilfail  | D3DSTENCILOP, wenn der Schablone-Test fehlschlägt.                                                      |
| D3DRS \_ CCW \_ stencilzfail | D3DSTENCILOP, wenn der Schablone-Test erfolgreich verläuft und z-Test fehlschlägt.                                    |
| D3DRS \_ CCW \_ stencilpass  | D3DSTENCILOP, wenn sowohl Schablone als auch z-Tests bestanden werden.                                           |
| D3DRS \_ CCW \_ stencilfunc  | D3DCMPFUNC-Funktion. Der Schablone-Test wird durchlaufen, wenn ((Ref & Mask) stencilfn (Schablone & Mask)) "true" ist. |



 

Die verbleibenden Schablone-Rendering-Zustände gelten immer für den Uhrzeigersinn und gegen den Uhrzeigersinn.

D3DRS \_ \_ der zweiseitige \_ Schablonen Modus wird für Linien und Punkt Sprites ignoriert, was bedeutet, dass das Verhalten von DirectX 8 unverändert bleibt. Die D3DRS \_ CCW- \_ Schablonen- \* Rendering-Zustände werden ignoriert.

Ein neues Cap-Bit gibt an, ob das Gerät dieses Feature unterstützt. Treiber, die dieses Feature nicht unterstützen, werden davon ausgehen, dass diese neuen Rendering-Zustände ignoriert werden. Alle anderen Schablone-deckbits gelten für beide Modi der Schablonen Pufferung. Da zwei \_ seitige \_ Schablonen die Fähigkeit zum Zeichnen mit D3DCULLMODE None impliziert \_ , muss die entsprechende Obergrenze vom Treiber festgelegt werden, wenn Sie diesen neuen Schablone-Modus unterstützt. Microsoft Windows Hardware Quality Labs (WHQL) sollte dies erzwingen.

Neue Rendering-Zustände:


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

[Techniken für Schablonen Puffer](stencil-buffer-techniques.md)
</dt> <dt>

[**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)
</dt> </dl>

 

 
