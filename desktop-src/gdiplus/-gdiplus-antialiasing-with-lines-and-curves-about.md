---
description: Wenn Sie Windows GDI+ verwenden, um eine Linie zu zeichnen, geben Sie den Ausgangspunkt und den Endpunkt der Linie an. Sie müssen jedoch keine Informationen zu den einzelnen Pixeln auf der Linie bereitstellen.
ms.assetid: 7c4869c1-76ff-42d1-abf1-387121943b2a
title: Antialiasing bei Linien und Kurven
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6d6fd1df9c8dca6bb600c723fa61cf14b99e53a51670768a7323ca33e12b9b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117697109"
---
# <a name="antialiasing-with-lines-and-curves"></a>Antialiasing bei Linien und Kurven

Wenn Sie Windows GDI+ verwenden, um eine Linie zu zeichnen, geben Sie den Ausgangspunkt und den Endpunkt der Linie an. Sie müssen jedoch keine Informationen zu den einzelnen Pixeln auf der Linie bereitstellen. GDI+ in Verbindung mit der Anzeigetreibersoftware, um zu bestimmen, welche Pixel eingeschaltet werden, um die Linie auf einem bestimmten Anzeigegerät anzuzeigen.

Stellen Sie sich eine gerade rote Linie vor, die vom Punkt (4, 2) bis zum Punkt (16, 10) reicht. Angenommen, das Koordinatensystem hat seinen Ursprung in der oberen linken Ecke, und die Maßeinheit ist das Pixel. Gehen Sie außerdem davon aus, dass die X-Achse nach rechts und die y-Achse nach unten zeigt. Die folgende Abbildung zeigt eine vergrößerte Ansicht der roten Linie, die auf einem mehrfarbigen Hintergrund gezeichnet wird.

![Abbildung mit vollfarbigen roten Pixeln auf einem mehrfarbigen Hintergrund](images/aboutgdip02-art33.png)

Beachten Sie, dass die roten Pixel, die zum Rendern der Linie verwendet werden, nicht transparent sind. An der Anzeige der Linie sind keine teilweise transparenten Pixel beteiligt. Diese Art von Linienrendering gibt der Linie ein verstrichenes Aussehen, und die Linie sieht ein wenig wie eine Striche aus. Diese Technik der Darstellung einer Linie mit einem Strich wird als Aliasing bezeichnet. ist ein Alias für die theoretische Linie.

Ein komplexeres Verfahren zum Rendern einer Linie umfasst die Verwendung teilweise transparenter Pixel zusammen mit rein roten Pixeln. Pixel werden auf reines Rot oder eine Mischung aus Rot und der Hintergrundfarbe festgelegt, je nachdem, wie nah sie sich an der Linie befinden. Diese Art von Rendering wird als Antialiasing bezeichnet und führt zu einer Linie, die das menschliche Auge als reibungsloser annimmt. Die folgende Abbildung zeigt, wie bestimmte Pixel mit dem Hintergrund kombiniert werden, um eine Antialiasinglinie zu erzeugen.

![Abbildung, die Pixel zeigt, bei denen es sich um Rotschattierungen auf demselben Hintergrund handelt](images/aboutgdip02-art34.png)

Antialiasing (Glättung) kann auch auf Kurven angewendet werden. Die folgende Abbildung zeigt eine vergrößerte Ansicht einer geglätteten Ellipse.

![Abbildung einer Ellipse, die aus verschiedenen Schattierungen von blauen Pixeln auf einem weißen Hintergrund besteht](images/aboutgdip02-art35.png)

Die folgende Abbildung zeigt die gleiche Ellipse in ihrer tatsächlichen Größe, einmal ohne Antialiasing und einmal mit Antialiasing.

![Screenshot von zwei Ausellipsen: Die mit Antialiasing erscheint auf verständliche Weise reibungsloser.](images/aboutgdip02-art36.png)

Erstellen Sie zum Zeichnen von Linien und Kurven, die Antialiasing verwenden, ein [**Graphics-Objekt,**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) und übergeben Sie *SmoothingModeAntiAlias an* die [**Graphics::SetSmoothingMode-Methode.**](/windows/desktop/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-setsmoothingmode) Rufen Sie dann eine der Zeichnungsmethoden desselben **Grafikobjekts** auf.


```
myGraphics.SetSmoothingMode(SmoothingModeAntiAlias);
myGraphics.DrawLine(&myPen, 0, 0, 12, 8);
```



**SmoothingModeAntiAlias** ist ein Element der [**SmoothingMode-Enumeration.**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-smoothingmode)

 

 



