---
description: Ein Polygon ist eine gefüllte Form mit geraden Seiten.
ms.assetid: 2259855f-4bad-4513-a021-b48c73eb7841
title: Informationen zu Polygonen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3efe99793aa0f8ae964583b4ca854340792751f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041981"
---
# <a name="about-polygons"></a>Informationen zu Polygonen

Ein *Polygon* ist eine gefüllte Form mit geraden Seiten. Die Seiten eines Polygons werden mithilfe des aktuellen Stifts gezeichnet. Wenn das System ein Polygon füllt, verwendet es den aktuellen Pinsel und den aktuellen Polygon Füll Modus. Die zwei Füll Modi, Alternate (Standard) und die Auffüllung, bestimmen, ob Bereiche innerhalb eines komplexen Polygons ausgefüllt oder nicht gezeichnet werden. Eine Anwendung kann einen der beiden Modi auswählen, indem Sie die Funktion [**setpolyfillmode**](/windows/desktop/api/Wingdi/nf-wingdi-setpolyfillmode) aufruft. Weitere Informationen zu den Polygon Füll Modi finden Sie unter [Regionen](regions.md).

Die folgende Abbildung zeigt ein Polygon, das mit [**Polygon**](/windows/desktop/api/Wingdi/nf-wingdi-polygon)gezeichnet wird.

![Abbildung eines Polygons in der Form eines fünf-Spitzen-Stern](images/csfsh-04.png)

Zusätzlich zum Zeichnen eines einzelnen Polygone [**mithilfe eines Polygone**](/windows/win32/api/wingdi/nf-wingdi-polygon)kann eine Anwendung mehrere Polygone mithilfe der [**polypolygon**](/windows/desktop/api/Wingdi/nf-wingdi-polypolygon) -Funktion zeichnen.

 

 
