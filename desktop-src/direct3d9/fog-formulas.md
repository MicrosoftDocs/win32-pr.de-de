---
description: C++-Anwendungen können steuern, wie sich der Nebel auf die Farbe von Objekten in einer Szene auswirkt, indem Sie ändern, wie Microsoft Direct3D Nebeleffekte über die Distanz berechnet.
ms.assetid: b7148ae8-45c7-4dbe-8295-0335c7fdeff0
title: Nebel Formeln (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75150a00d491f1e3fc1ea1444209449c1c2a825d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860195"
---
# <a name="fog-formulas-direct3d-9"></a>Nebel Formeln (Direct3D 9)

C++-Anwendungen können steuern, wie sich der Nebel auf die Farbe von Objekten in einer Szene auswirkt, indem Sie ändern, wie Microsoft Direct3D Nebeleffekte über die Distanz berechnet. Der [**D3DFOGMODE**](./d3dfogmode.md) -Enumerationstyp enthält Elemente, die die drei Nebel Formeln bezeichnen. Alle Formeln berechnen einen Nebel Faktor als eine Funktion der Entfernung, wobei die Parameter angegeben werden, die von der Anwendung festgelegt werden.

## <a name="linear-fog"></a>Linearer Nebel

Dies wird mit der folgenden D3DFOG \_ linearen Gleichung festgelegt.

![Gleichung von Direct3D linear Nebel](images/fogliner.png)

where

-   Start ist der Abstand, bei dem die Nebeleffekte beginnen.
-   "End" ist die Entfernung, bei der die Auswirkungen von Nebel nicht mehr zunehmen.
-   d stellt die Tiefe oder die Entfernung vom Standpunkt dar. Bei Bereichs basiertem Nebel ist der Wert für d der Abstand zwischen der Kameraposition und einem Scheitelpunkt. Bei einem nicht Bereichs basierten Nebel ist der Wert für d der absolute Wert der Z-Koordinate im Kamerabereich.

## <a name="exponential-fog"></a>Exponentieller Nebel

Lineare und exponentielle Formeln werden sowohl für Pixel Nebel als auch für Scheitelpunkt Nebel unterstützt.

Dies wird mit der folgenden D3DFOG \_ Exp-Gleichung festgelegt.

![Gleichung des exponentiellen Direct3D-Nebel Werts](images/fogexp.png)

where

-   e ist die Basis des natürlichen Logarithmus (ungefähr 2,71828).
-   die Dichte ist eine beliebige Nebeldichte, die zwischen 0,0 und 1,0 liegen kann.
-   d stellt die Tiefe oder die Entfernung vom Standpunkt dar, wie bereits erwähnt.

Dies wird mit der folgenden D3DFOG \_ exp2 Gleichung festgelegt.

![Gleichung von Direct3D exponentiellem 2-Nebel](images/fogexp2.png)

where

-   e ist die Basis des natürlichen Logarithmus, wie oben angegeben.
-   die Dichte ist eine beliebige Nebeldichte, die wie oben angegeben zwischen 0,0 und 1,0 reichen kann.
-   d stellt die Tiefe oder die Entfernung vom Standpunkt dar, wie oben angegeben.

> [!Note]  
> Das System speichert den Nebel Faktor in der Alpha Komponente der Glanz Farbe eines Scheitel Punkts. Wenn Ihre Anwendung ihre eigene Transformation und Beleuchtung durchführt, können Sie die Werte für den Nebel Faktor manuell einfügen, damit Sie vom System während des Renderings angewendet werden.

 

Das folgende Diagramm zeigt diese Formeln, wobei allgemeine Werte als in den Formel Parametern verwendet werden.

![Diagramm der Nebel Formeln in der Entfernung und der Farbmenge](images/foggraph.png)

D3DFOG \_ linear ist 1,0 am Anfang und 0,0 am Ende. Es wird nicht in Bezug auf die Near-oder Far-Plane gemessen.

Wenn Direct3D Nebeleffekte berechnet, wird der Nebel Faktor aus einer der vorangehenden Gleichungen in der folgenden Mischungs Gleichung verwendet.

![Gleichung von Nebeleffekten für Direct3D](images/fogcalc.png)

Mit dieser Formel wird die Farbe des aktuellen Polygons c durch den Nebel Faktor f effektiv skaliert, und das Produkt wird der Nebelfarbe C hinzugefügt, die durch die bitweise Umkehrung des Nebel Faktors skaliert wird. Der resultierende Farbwert ist eine Mischung aus der Nebelfarbe und der ursprünglichen Farbe als Faktor der Entfernung. Die Formel gilt für alle Geräte, die in Microsoft DirectX 7,0 und höher unterstützt werden. Bei der Legacy-Anlauf Vorrichtung skaliert der Nebel Faktor die diffusen und Glanz Farben, die auf den Bereich von 0,0 und 1,0 (einschließlich) zugeschnitten sind. Der Nebel Faktor beginnt in der Regel bei 1,0 für die nahe Ebene und sinkt auf der äußersten Ebene auf 0,0.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Nebel Typen](fog-types.md)
</dt> </dl>

 

 
