---
description: Ein Rechteck ist ein vierseitiges Polygon, dessen Gegenseite parallel und gleich lang sind.
ms.assetid: 77d29981-032e-45ba-a06b-c9c992236803
title: Zeichen Rechtecke
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec1c5908ff989f7534536b3a6e84bad2095c096e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863651"
---
# <a name="drawing-rectangles"></a>Zeichen Rechtecke

Ein Rechteck ist ein vierseitiges Polygon, dessen Gegenseite parallel und gleich lang sind. Obwohl eine Anwendung ein Rechteck durch Aufrufen der [**Polygon**](/windows/desktop/api/Wingdi/nf-wingdi-polygon) Funktion zeichnen kann, um die Koordinaten der einzelnen Ecken anzugeben, bietet die [**Rechteck**](/windows/desktop/api/Wingdi/nf-wingdi-rectangle) Funktion eine einfachere Methode. Diese Funktion erfordert nur die Koordinaten für die obere linke Ecke und die unteren rechten Ecke. Wenn eine Anwendung die [**Rechteck**](/windows/win32/api/wingdi/nf-wingdi-rectangle) Funktion aufruft, zeichnet das System das Rechteck mit Ausnahme der rechten und unteren Seite, wenn für den angegebenen Gerätekontext keine globale Transformation festgelegt ist.

Wenn eine globale Transformation mithilfe der Funktion [**setworldtransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) oder [**modifyworldtransform**](/windows/desktop/api/Wingdi/nf-wingdi-modifyworldtransform) festgelegt wurde, enthält das System den rechten und unteren Rand.

Zusätzlich zum Zeichnen eines herkömmlichen Rechtecks können Sie Rechtecke mit abgerundeten Ecken zeichnen. Die [**roundRect**](/windows/desktop/api/Wingdi/nf-wingdi-roundrect) -Funktion erfordert, dass die Anwendung die Koordinaten der unteren linken und oberen rechten Ecke sowie die Breite und Höhe der Ellipse bereitstellt, die zum Runden der einzelnen Ecken verwendet wird.

Anwendungen können die folgenden Funktionen verwenden, um Rechtecke zu bearbeiten.



| Funktion                         | BESCHREIBUNG                                                        |
|----------------------------------|--------------------------------------------------------------------|
| [**FillRect**](/windows/desktop/api/Winuser/nf-winuser-fillrect)     | Zeichnet das Innere eines Rechtecks.                              |
| [**FrameRect**](/windows/desktop/api/Winuser/nf-winuser-framerect)   | Zeichnet die Seiten eines Rechtecks neu.                                  |
| [**Invertrect**](/windows/desktop/api/Winuser/nf-winuser-invertrect) | Kehrt die Farben um, die innerhalb des Inneren eines Rechtecks angezeigt werden. |



 

 

 
