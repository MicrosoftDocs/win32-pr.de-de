---
description: Ein Kreis ist ein Bereich, der durch die Schnittmenge einer Ellipsekurve und zweier radialer Kurve gebunden ist. Die folgende Abbildung zeigt einen Kreis, der mithilfe der Pie-Funktion gezeichnet wird.
ms.assetid: 9ba7834e-02d2-4335-94c3-ab2f5c355619
title: Informationen zu Kreisen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e447e313a3088bbf9a72c790115fb3bb25770017cf13ce7922685fd18ccfe671
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966460"
---
# <a name="about-pies"></a>Informationen zu Kreisen

Ein *Kreis* ist ein Bereich, der durch die Schnittmenge einer Ellipsekurve und zweier radialer Kurve gebunden ist. Die folgende Abbildung zeigt einen Kreis, der mithilfe der [**Pie-Funktion gezeichnet**](/windows/desktop/api/Wingdi/nf-wingdi-pie) wird.

![Abbildung, die eine Ellipse mit einem schattierten Kreis zeigt](images/csfsh-03.png)

Beim Aufrufen von [**Pie**](/windows/win32/api/wingdi/nf-wingdi-pie)stellt eine Anwendung die Koordinaten der oberen linken und unteren rechten Ecken des umgebundenen Rechtecks der Ellipse sowie die Koordinaten von zwei Punkten zur Definition von zwei radialen Punkten zur Auswahl.

Wenn das System den gekrümmten Teil des Kreiss zeichnet, verwendet es die aktuelle Bogenrichtung für den angegebenen Gerätekontext. Die Standard arc-Richtung ist gegen den Uhrzeigersinn. Eine Anwendung kann die Arcrichtung zurücksetzen, indem sie die [**SetArcDirection-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-setarcdirection) aufruft.

 

 
