---
description: Eine Anwendung ruft die Dimensionen des umgebundenen Rechtecks einer Region ab, indem sie die GetRgnBox-Funktion aufruft.
ms.assetid: 3851d0f4-33ec-44db-9cb8-c2afb03ffc25
title: Abrufen eines umgebundenen Rechtecks
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9b7182d7c8f48fa8629855849710a601db9f93fd7e9180f9024d798b5ce2ebe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117886146"
---
# <a name="retrieving-a-bounding-rectangle"></a>Abrufen eines umgebundenen Rechtecks

Eine Anwendung ruft die Dimensionen des umgebundenen Rechtecks einer Region ab, indem sie die [**GetRgnBox-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-getrgnbox) aufruft. Wenn der Bereich rechteckig ist, **gibt GetRgnBox** die Dimensionen des Bereichs zurück. Wenn der Bereich elliptisch ist, gibt die Funktion die Dimensionen des kleinsten Rechtecks zurück, das um die Ellipse gezeichnet werden kann. Die langen Seiten des Rechtecks haben die gleiche Länge wie die Hauptachse der Ellipse, und die kurzen Seiten des Rechtecks haben die gleiche Länge wie die Nebenachse der Ellipse. Wenn der Bereich polygonal ist, **gibt GetRgnBox** die Dimensionen des kleinsten Rechtecks zurück, das um das gesamte Polygon gezeichnet werden kann.

 

 



