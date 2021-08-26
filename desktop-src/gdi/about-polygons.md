---
description: Ein Polygon ist eine gefüllte Form mit geraden Seiten.
ms.assetid: 2259855f-4bad-4513-a021-b48c73eb7841
title: Informationen zu Polygonen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f0d28bd915237991294f6579448ca08785481f374814f0ed5840f77ee9f813c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966440"
---
# <a name="about-polygons"></a>Informationen zu Polygonen

Ein *Polygon* ist eine gefüllte Form mit geraden Seiten. Die Seiten eines Polygons werden mit dem aktuellen Stift gezeichnet. Wenn das System ein Polygon ausfüllt, verwendet es den aktuellen Pinsel und den aktuellen Polygonfüllmodus. Die beiden Füllmodi Alternative (Standard) und Windung bestimmen, ob Bereiche innerhalb eines komplexen Polygons gefüllt oder nicht bezahlt bleiben. Eine Anwendung kann einen der beiden Modi auswählen, indem sie die [**SetPolyFillMode-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-setpolyfillmode) aufruft. Weitere Informationen zu Polygonfüllmodi finden Sie unter [Regionen.](regions.md)

Die folgende Abbildung zeigt ein Polygon, das [**mit**](/windows/desktop/api/Wingdi/nf-wingdi-polygon)polygon gezeichnet wurde.

![Abbildung eines Polygons in Form eines fünfzackigen Sterns](images/csfsh-04.png)

Zusätzlich zum Zeichnen eines einzelnen Polygons mithilfe von [**Polygon**](/windows/win32/api/wingdi/nf-wingdi-polygon)kann eine Anwendung mithilfe der [**PolyPolygon-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-polypolygon) mehrere Polygone zeichnen.

 

 
