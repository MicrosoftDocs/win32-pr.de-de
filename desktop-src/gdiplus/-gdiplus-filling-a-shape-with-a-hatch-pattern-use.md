---
description: 'Ein Schraffurmuster wird aus zwei Farben erstellt: eine für den Hintergrund und eine für die Linien, die das Muster über den Hintergrund bilden.'
ms.assetid: 7c2bfe54-3259-40d6-9eb4-1a8ad3dda477
title: Auffüllen einer Form mit einem Schraffurmuster
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c37f06c93a6ac66a4a6066874c99b88652a0819
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988085"
---
# <a name="filling-a-shape-with-a-hatch-pattern"></a>Auffüllen einer Form mit einem Schraffurmuster

Ein Schraffurmuster wird aus zwei Farben erstellt: eine für den Hintergrund und eine für die Linien, die das Muster über den Hintergrund bilden. Um eine geschlossene Form mit einem Schraffurmuster auszufüllen, verwenden Sie ein [**HatchBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush) -Objekt. Im folgenden Beispiel wird veranschaulicht, wie Sie eine Ellipse mit einem Schraffurmuster ausfüllen:


```
HatchBrush hBrush(HatchStyleHorizontal, Color(255, 255, 0, 0),
   Color(255, 128, 255, 255));
stat = graphics.FillEllipse(&hBrush, 0, 0, 100, 60);
```



Die folgende Abbildung zeigt die gefüllte Ellipse.

![Abbildung einer Ellipse, die mit einem Schraffurmuster von horizontalen Linien über einem voll Bild Hintergrund gefüllt ist](images/hatch1.png)

Der [**HatchBrush**](/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush) -Konstruktor benötigt drei Argumente: die Schraffurart, die Farbe der schraffurzeile und die Farbe des Hintergrunds. Das schraffurargumentgument kann ein beliebiges Element der [**HatchStyle**](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-hatchstyle) -Enumeration sein. In der **HatchStyle** -Enumeration sind mehr als 50 Elemente vorhanden. Einige dieser Elemente sind in der folgenden Liste aufgeführt:

-   **HatchStyleHorizontal**
-   **Hatchstylevertical**
-   **Hatchstyleforwarddiagonal**
-   **Hatchstylebackwarddiagonal**
-   **Hatchstylecross**
-   **Hatchstylediagonalcross**

 

 



