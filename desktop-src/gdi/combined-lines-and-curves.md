---
description: Zusätzlich zum Zeichnen von Linien oder Kurven können Anwendungen Kombinationen aus Zeilen-und Kurven Ausgabe zeichnen, indem Sie eine einzelne Funktion aufrufen. Beispielsweise kann eine Anwendung die Gliederung eines Kreis Diagramms zeichnen, indem die anglearc-Funktion aufgerufen wird.
ms.assetid: 0abcc20c-ba89-4eb4-bbd1-7ea27d367fb8
title: Kombinierte Linien und Kurven
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2ee6aaa3e7a1be580e36c01fb44c81296e894d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978736"
---
# <a name="combined-lines-and-curves"></a>Kombinierte Linien und Kurven

Zusätzlich zum Zeichnen von Linien oder Kurven können Anwendungen Kombinationen aus Zeilen-und Kurven Ausgabe zeichnen, indem Sie eine einzelne Funktion aufrufen. Beispielsweise kann eine Anwendung die Gliederung eines Kreis Diagramms zeichnen, indem die [**anglearc**](/windows/desktop/api/Wingdi/nf-wingdi-anglearc) -Funktion aufgerufen wird.

Die [**anglearc**](/windows/desktop/api/Wingdi/nf-wingdi-anglearc) -Funktion zeichnet einen Bogen entlang des Umkreis Bereichs eines Kreises und zeichnet eine Linie, die den Anfangspunkt des Bogens mit der Mitte des Kreises verbindet. Zusätzlich zur Verwendung der **anglearc** -Funktion kann eine Anwendung auch die Zeilen-und unregelmäßige Kurven Ausgabe mithilfe der [**polydraw**](/windows/desktop/api/Wingdi/nf-wingdi-polydraw) -Funktion kombinieren.

 

 



