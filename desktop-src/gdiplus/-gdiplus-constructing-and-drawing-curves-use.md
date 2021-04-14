---
description: 'GDI+ unterstützt verschiedene Arten von Kurven: Ellipsen, Arcs, kardinale Splines und B&\# 233; Zier-Splines.'
ms.assetid: 97a1342c-4edb-4671-b36d-b6992efad498
title: Erstellen und Zeichnen von Kurven
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f61c1aa12e3152ed65cca2da6911d2d53def81b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104994310"
---
# <a name="constructing-and-drawing-curves"></a>Erstellen und Zeichnen von Kurven

GDI+ unterstützt verschiedene Arten von Kurven: Ellipsen, Arcs, kardinale Splines und Bézier-Splines. Eine Ellipse wird durch das umgebende Rechteck definiert. ein Bogen ist ein Teil einer Ellipse, die durch einen Anfangs Winkel und einen Pfeil Winkel definiert wird. Ein kardinalspline wird durch ein Array von Punkten und einen Spannungs Parameter definiert – die Kurve verläuft nahtlos durch jeden Punkt im Array, und der Tension-Parameter wirkt sich auf die Art und Weise der Kurve aus. Eine Bézier-Spline wird von zwei Endpunkten und zwei Kontrollpunkten definiert – die Kurve übergibt nicht die Steuerungs Punkte, aber die Steuerungs Punkte beeinflussen die Richtung und die Kurve, wenn die Kurve von einem Endpunkt zum anderen wechselt.

In den folgenden Themen werden die wichtigsten Splines und die Bézier-Splines ausführlicher behandelt:

-   [Zeichnen von kardinalen Splines](-gdiplus-drawing-cardinal-splines-use.md)
-   [Zeichnen von Bézier-Splines](-gdiplus-drawing-bezier-splines-use.md)

 

 



