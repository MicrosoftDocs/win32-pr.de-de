---
description: Ein Kreis ist ein Bereich, der durch die Schnittmenge einer Ellipse und zwei Radials begrenzt ist. Die folgende Abbildung zeigt einen Kreis, der mithilfe der Kreis Funktion gezeichnet wurde.
ms.assetid: 9ba7834e-02d2-4335-94c3-ab2f5c355619
title: Informationen zu Torten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a2184276fc208827ddac82fd7f4cacec3ddb20f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041982"
---
# <a name="about-pies"></a>Informationen zu Torten

Ein *Kreis ist ein* Bereich, der durch die Schnittmenge einer Ellipse und zwei Radials begrenzt ist. Die folgende Abbildung zeigt einen Kreis, der mithilfe der [**Kreis Funktion gezeichnet**](/windows/desktop/api/Wingdi/nf-wingdi-pie) wurde.

![Abbildung, die eine Ellipse mit schattiertem Kreis zeigt](images/csfsh-03.png)

Beim Aufrufen von " [**Pie**](/windows/win32/api/wingdi/nf-wingdi-pie)" stellt eine Anwendung die Koordinaten der oberen linken und der unteren rechten Ecke des umgebenden Rechtecks der Ellipse sowie die Koordinaten von zwei Punkten bereit, die zwei radiale definieren.

Wenn das System den gekrümmten Teil des Kreises zeichnet, wird die aktuelle Bogen Richtung für den angegebenen Gerätekontext verwendet. Die Standard-Bogen Richtung ist gegen den Uhrzeigersinn. Eine Anwendung kann die Richtung des Bogens zurücksetzen, indem die [**setarcdirection**](/windows/desktop/api/Wingdi/nf-wingdi-setarcdirection) -Funktion aufgerufen wird.

 

 
