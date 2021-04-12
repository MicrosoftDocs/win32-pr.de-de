---
title: VML-Attribut "Dashboard"
description: VML-Attribut "Dashboard"
ms.assetid: 7d6c7cbf-9ccc-4117-af0a-ca8f36684f88
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4651af9ade605166121c7225925e3bf1ed8264ec
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315315"
---
# <a name="vml-dashstyle-attribute"></a>VML-Attribut "Dashboard"

In diesem Thema wird VML beschrieben, eine Funktion, die ab Windows Internet Explorer 9 veraltet ist. Webseiten und Anwendungen, die auf VML basieren, sollten zu SVG oder anderen allgemein unterstützten Standards migriert werden.

> [!Note]  
> Ab Dezember 2011 wurde dieses Thema archiviert. Daher wird er nicht mehr aktiv verwaltet. Weitere Informationen finden Sie unter [archivierte Inhalte](/previous-versions/windows/internet-explorer/ie-developer/). Informationen, Empfehlungen und Anleitungen zur aktuellen Version von Windows Internet Explorer finden Sie im [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Gibt den Punkt und das Bindestrich Muster für einen Strich an. Lese-/Schreibzugriff. **Vglinedashstyle**.

**Gilt für**

[Stellung](msdn-online-vml-stroke-element.md)

**Tagsyntax**

<v: *Element* DashStyle = " *Expression* " >

**Skript Syntax**

*Element* . DashStyle = "*Ausdruck*"

*Ausdruck* = *Element*. DashStyle

**Anmerkungen**

Mögliche Werte:

-   Solid (Standard)
-   Shortdash
-   Kurzpunkt
-   Shortdashdot
-   Shortdashdotdot
-   Punkt
-   Strich
-   Longdash
-   DashDot
-   Longdashdot
-   Longdashdotdot

Mit **dem Attribut "** Dashboard" kann der Benutzer ein benutzerdefiniertes Bindestrich Muster angeben. Dies erfolgt mithilfe einer Reihe von Zahlen. Dash-Stile werden in Bezug auf die Länge des Bindestrichs (der gezeichnete Teil des Strichs) und die Länge des leer Zeichens zwischen den Bindestrichen definiert. Die Längen sind relativ zur Linienstärke: eine Länge von "1" ist gleich der Linienstärke. Der **EndCap** -Stil wird auf jeden Bindestrich angewendet, der Pfeil Stil ist nicht. Die Zeichenfolge definiert zuerst die Länge des Bindestrichs und dann die Länge des Leerraums. Dies wird möglicherweise wiederholt, um komplexe Dash-Stile zu bilden. Die Zeichenfolge sollte immer ein Zahlenpaar enthalten. Wenn Sie eine ungerade Anzahl von Zahlen enthält, werden die letzten möglicherweise ignoriert.

In der folgenden Tabelle sind einige typische Werte und eine Beschreibung des beabsichtigten Effekts aufgeführt. "0" impliziert einen Punkt, der vierfache symmetrisch sein sollte (mit Round-End-Caps sollte er ein Kreis sein). Wenn die Linien Ende-Obergrenze "Flat" ist, sollte ein Viewer, soweit möglich, einen integrierten Betriebssystem-Dash auswählen (anders ausgedrückt: etwas, das schnell gezeichnet werden kann.) In der folgenden Tabelle sind einige Beispiele aufgeführt.



| DashStyle     | BESCHREIBUNG                                                                                          |
|---------------|------------------------------------------------------------------------------------------------------|
| "2 2"         | Kurzbinde Striche. Jeder Bindestrich und der Leerraum dazwischen sind doppelt so breit wie die Linie.                        |
| "0 2"         | Punkten. Der zwischen Raum zwischen und ist doppelt so breit wie die Linie.                                                  |
| "2 2 0 2"     | Kurzer Bindestrich Punkt.                                                                                      |
| "2 2 0 2 0 2" | Kurzer Bindestrich Punkt Punkt.                                                                                  |
| "1 2"         | Gewinn. Jeder Bindestrich ist die Breite der Linie, während jedes Leerzeichen doppelt so breit ist wie die Linie.            |
| "4 2"         | Streifens. Jeder Bindestrich ist viermal so breit wie die Breite der Linie, während jeder Leerraum doppelt so breit ist wie die Linie. |
| "8 2"         | Langer Bindestrich.                                                                                           |
| "4 2 1 2"     | Bindestrich Punkt.                                                                                            |
| "8 2 1 2"     | Long Dash-Punkt.                                                                                       |
| "8 2 1 2 1 2" | Langer Bindestrich Punkt Punkt.                                                                                   |



 

*VML-Standard Attribut*

**Beispiel**

Die Form hat einen Bindestrich mit abwechselnden Bindestrichen und Punkten.


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200,200,200, 200,1 x e">
   <v:stroke dashstyle="dashdot"/>
   </v:shape>
```



 

 