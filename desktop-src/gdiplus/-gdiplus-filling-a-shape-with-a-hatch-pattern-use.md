---
description: 'Ein Schraffurmuster besteht aus zwei Farben: einer für den Hintergrund und eine für die Linien, die das Muster über dem Hintergrund bilden.'
ms.assetid: 7c2bfe54-3259-40d6-9eb4-1a8ad3dda477
title: Füllen einer Form mit einem Schraffurmuster
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b571ab09dc91c037e0cc89a2b107c2f8d253b832b593bb32a169bc970295d41
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015100"
---
# <a name="filling-a-shape-with-a-hatch-pattern"></a>Füllen einer Form mit einem Schraffurmuster

Ein Schraffurmuster besteht aus zwei Farben: einer für den Hintergrund und eine für die Linien, die das Muster über dem Hintergrund bilden. Um eine geschlossene Form mit einem Schraffurmuster zu füllen, verwenden Sie ein [**HatchBrush-Objekt.**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush) Im folgenden Beispiel wird veranschaulicht, wie eine Ellipse mit einem Schraffurmuster gefüllt wird:


```
HatchBrush hBrush(HatchStyleHorizontal, Color(255, 255, 0, 0),
   Color(255, 128, 255, 255));
stat = graphics.FillEllipse(&hBrush, 0, 0, 100, 60);
```



Die folgende Abbildung zeigt die ausgefüllte Ellipse.

![Abbildung einer mit Schraffurmustern gefüllten Ellipse mit horizontalen Linien über einem soliden Hintergrund](images/hatch1.png)

Der [**HatchBrush-Konstruktor**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush) verwendet drei Argumente: den Schraffurstil, die Farbe der Schraffurlinie und die Farbe des Hintergrunds. Das Schraffurstilargument kann ein beliebiges Element der [**HatchStyle-Enumeration**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-hatchstyle) sein. Die **HatchStyle-Enumeration** enthält mehr als 50 Elemente. Einige dieser Elemente werden in der folgenden Liste angezeigt:

-   **HatchStyleHorizontal**
-   **HatchStyleVertical**
-   **HatchStyleForwardDiagonal**
-   **HatchStyleBackwardDiagonal**
-   **HatchStyleCross**
-   **HatchStyleDiagonalCross**

 

 



