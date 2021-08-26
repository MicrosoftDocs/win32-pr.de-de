---
description: 'GDI+ unterstützt verschiedene Arten von Kurven: Ellipsen, Bogen, Kardinalsplines und B&\# 233;zier-Splines.'
ms.assetid: 97a1342c-4edb-4671-b36d-b6992efad498
title: Erstellen und Zeichnen von Kurven
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b78ebd7ce81099d5b7f483939c0f4b238d1f124357bf6e1863b25fedb7e22f4c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015220"
---
# <a name="constructing-and-drawing-curves"></a>Erstellen und Zeichnen von Kurven

GDI+ unterstützt verschiedene Arten von Kurven: Ellipsen, Bogen, Kardinalsplines und Bézier-Splines. Eine Ellipse wird durch das umgebundene Rechteck definiert. Ein Bogen ist ein Teil einer Ellipse, der durch einen Startwinkel und einen Sweepwinkel definiert wird. Eine Kardinal-Spline wird durch ein Array von Punkten und einen Parameter für die Kurve definiert. Die Kurve durchläuft jeden Punkt im Array reibungslos, und der Parameter "parameters" beeinflusst die Art und Weise, wie die Kurve sich schwenniert. Ein Bézier-Spline wird durch zwei Endpunkte und zwei Kontrollpunkte definiert– die Kurve durchläuft nicht die Kontrollpunkte, aber die Kontrollpunkte beeinflussen die Richtung und die Kurve, während die Kurve von einem Endpunkt zum anderen übergeht.

In den folgenden Themen werden kardinale Splines und Bézier-Splines ausführlicher behandelt:

-   [Zeichnen von Kardinalsplines](-gdiplus-drawing-cardinal-splines-use.md)
-   [Zeichnen von Bézier-Splines](-gdiplus-drawing-bezier-splines-use.md)

 

 



