---
description: C++-Anwendungen können steuern, wie sich Beeinträchtigungen auf die Farbe von Objekten in einer Szene auswirken, indem sie ändern, wie Microsoft Direct3D Effekte im Lauf der Entfernung berechnet.
ms.assetid: b7148ae8-45c7-4dbe-8295-0335c7fdeff0
title: Formeln für Formeln (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac92b6d00ff5f4d4ec03dbe7bb40365917f8b835fd121cdc934c470c45c38814
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120026998"
---
# <a name="fog-formulas-direct3d-9"></a>Formeln für Formeln (Direct3D 9)

C++-Anwendungen können steuern, wie sich Beeinträchtigungen auf die Farbe von Objekten in einer Szene auswirken, indem sie ändern, wie Microsoft Direct3D Effekte im Lauf der Entfernung berechnet. Der [**D3DFOGMODE-Enumerationstyp**](./d3dfogmode.md) enthält Member, die die drei Formeln identifizieren. Alle Formeln berechnen einen Faktor für die Auslastung als Funktion des Abstands, vorausgesetzt, die Parameter werden von Ihrer Anwendung festgelegt.

## <a name="linear-fog"></a>Lineare Linienlinie

Dies wird mit der folgenden D3DFOG \_ LINEAR-Gleichung festgelegt.

![Gleichung des linearen Direct3d-Gleichungsrades](images/fogliner.png)

where

-   start ist der Abstand, ab dem Die Effekte beginnen.
-   end ist der Abstand, bei dem sich die Effekte nicht mehr erhöhen.
-   d stellt die Tiefe oder den Abstand vom Blickpunkt dar. Bei bereichsbasiertem Licht ist der Wert für d der Abstand zwischen der Kameraposition und einem Scheitelpunkt. Bei nicht bereichsbasierten Abmessungen ist der Wert für d der absolute Wert der Z-Koordinate im Kameraraum.

## <a name="exponential-fog"></a>Exponentielles Gleiten

Lineare und exponentielle Formeln werden sowohl für Pixel- als auch für Scheitelpunktkurven unterstützt.

Dies wird mit der folgenden D3DFOG \_ EXP-Gleichung festgelegt.

![Gleichung des exponentiellen Direct3d-Gleitens](images/fogexp.png)

where

-   e ist die Basis natürlicher Logarithmen (ca. 2,71828).
-   density ist eine beliebige Dichte von 0,0 bis 1,0.
-   d stellt die Tiefe oder den Abstand vom Standpunkt dar, wie zuvor erwähnt.

Dies wird mit der folgenden D3DFOG \_ EXP2-Gleichung festgelegt.

![Gleichung von direct3d exponential 2-2-Gleichung](images/fogexp2.png)

where

-   e ist die Basis der natürlichen Logarithmen, wie oben beschrieben.
-   density ist eine beliebige Dichte von 0,0 bis 1,0, wie oben beschrieben.
-   d stellt die Tiefe oder den Abstand vom Standpunkt dar, wie oben angegeben.

> [!Note]  
> Das System speichert den Knotenfaktor in der Alphakomponente der Glanzfarbe für einen Scheitelpunkt. Wenn Ihre Anwendung eine eigene Transformation und Beleuchtung ausführt, können Sie manuell Werte für den Faktor "Factor Factor" einfügen, die während des Renderings vom System angewendet werden.

 

Das folgende Diagramm zeigt diese Formeln mit allgemeinen Werten wie in den Formelparametern.

![Diagramm der Formeln für Die Formeln über Abstand und Farbmenge](images/foggraph.png)

D3DFOG \_ LINEAR ist 1,0 am Anfang und 0,0 am Ende. Sie wird nicht relativ zur nah- oder fernen Ebene gemessen.

Wenn Direct3D Die Effekte von Effekten berechnet, verwendet es den Faktor des Füllfaktors aus einer der vorangehenden Gleichungen in der folgenden Mischungsgleichung.

![Gleichung von Effekten für direct3d](images/fogcalc.png)

Diese Formel skaliert effektiv die Farbe des aktuellen Polygons C um den Faktor f und fügt das Produkt der Farbfarbe C hinzu, skaliert durch die bitweise Umkehrung des Faktors der Striche. Der resultierende Farbwert ist eine Mischung aus der Farbfarbe und der ursprünglichen Farbe als Abstandsfaktor. Die Formel gilt für alle Geräte, die in Microsoft DirectX 7.0 und höher unterstützt werden. Für das Legacy-Rampengerät skaliert der Faktor für die Streufarbe die diffusen und specellarischen Farbkomponenten, die an den Bereich von 0,0 und 1,0 (einschließlich) klammern. Der Verformungsfaktor beginnt in der Regel bei 1,0 für die nahe Ebene und verringert sich auf der fernen Ebene auf 0,0.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Typen von Typen](fog-types.md)
</dt> </dl>

 

 
