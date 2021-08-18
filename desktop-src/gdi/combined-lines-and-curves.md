---
description: Zusätzlich zum Zeichnen von Linien oder Kurven können Anwendungen Kombinationen aus Linien- und Kurvenausgaben zeichnen, indem sie eine einzelne Funktion aufrufen. Beispielsweise kann eine Anwendung die Kontur eines Kreisdiagramms zeichnen, indem sie die AngleArc-Funktion aufruft.
ms.assetid: 0abcc20c-ba89-4eb4-bbd1-7ea27d367fb8
title: Kombinierte Linien und Kurven
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1939b863bfacf2176f15c950b48c8b7c91cc43e7b6b4d4c58ac08e1760c4cee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105719"
---
# <a name="combined-lines-and-curves"></a>Kombinierte Linien und Kurven

Zusätzlich zum Zeichnen von Linien oder Kurven können Anwendungen Kombinationen aus Linien- und Kurvenausgaben zeichnen, indem sie eine einzelne Funktion aufrufen. Beispielsweise kann eine Anwendung die Kontur eines Kreisdiagramms zeichnen, indem sie die [**AngleArc-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-anglearc) aufruft.

Die [**AngleArc-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-anglearc) zeichnet einen Bogen entlang des Umkreises eines Kreises und zeichnet eine Linie, die den Ausgangspunkt des Bogens mit dem Mittelpunkt des Kreises verbindet. Zusätzlich zur Verwendung der **AngleArc-Funktion** kann eine Anwendung auch die Ausgabe von Linien- und unregelmäßigen Kurven mithilfe der [**PolyDraw-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-polydraw) kombinieren.

 

 



