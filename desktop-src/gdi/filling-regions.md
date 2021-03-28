---
description: Eine Anwendung füllt das Innere eines Bereichs durch Aufrufen der fillrgn-Funktion und Bereitstellen eines Handles, das einen bestimmten Pinsel identifiziert.
ms.assetid: 6174b2ea-836a-4538-a0ad-e123c88fc6f6
title: Auffüllen von Regionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62709869f5f25a6cde11812844efdab6162b1e9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041968"
---
# <a name="filling-regions"></a>Auffüllen von Regionen

Eine Anwendung füllt das Innere eines Bereichs durch Aufrufen der [**fillrgn**](/windows/desktop/api/Wingdi/nf-wingdi-fillrgn) -Funktion und Bereitstellen eines Handles, das einen bestimmten Pinsel identifiziert. Wenn eine Anwendung fillrgn aufruft, füllt das System den Bereich mit dem Pinsel, indem der aktuelle Füll Modus für den angegebenen Gerätekontext verwendet wird. Es gibt zwei Füll Modi: "Alternative" und "Winding". Die Anwendung kann den Füll Modus für einen Gerätekontext durch Aufrufen der [**setpolyfillmode**](/windows/desktop/api/Wingdi/nf-wingdi-setpolyfillmode) -Funktion festlegen. Die Anwendung kann den aktuellen Füllmodus für einen Gerätekontext abrufen, indem die [**getpolyfillmode**](/windows/desktop/api/Wingdi/nf-wingdi-getpolyfillmode) -Funktion aufgerufen wird.

In der folgenden Abbildung sind zwei identische Bereiche dargestellt: eine mit dem alternativen Modus und die andere mit dem Auffüllmodus.

![Abbildung mit 2 5-Spitzen Sternen: eine, die nur in den Punkten gefüllt ist, die andere vollständig ausgefüllt](images/csrgn-03.png)

## <a name="alternate-mode"></a>Alternativer Modus

Führen Sie den folgenden Test aus, um zu bestimmen, welche Pixel das System hervorhebt, wenn der Alternative Modus angegeben ist:

1.  Wählen Sie ein Pixel im Inneren des Bereichs aus.
2.  Zeichnen Sie ein imaginäres Strahl in der positiven x-Richtung von diesem Pixel bis unendlich.
3.  Jedes Mal, wenn das Strahl eine Begrenzungs Linie schneidet, erhöhen Sie einen Count-Wert.

Das System hebt das Pixel hervor, wenn der Count-Wert eine ungerade Zahl ist.

## <a name="winding-mode"></a>Lademodus

Führen Sie den folgenden Test aus, um zu bestimmen, welche Pixel das System hervorhebt, wenn der Wickel Modus angegeben ist:

1.  Bestimmen Sie die Richtung, in der die einzelnen Begrenzungs Linien gezeichnet werden.
2.  Wählen Sie ein Pixel im Inneren des Bereichs aus.
3.  Zeichnen Sie ein imaginäres Ray, das in der positiven x-Richtung verläuft, vom Pixel bis zum unendlich.
4.  Jedes Mal, wenn das Strahl eine Begrenzungs Linie mit einer positiven y-Komponente schneidet, erhöhen Sie einen Count-Wert. Jedes Mal, wenn das Strahl eine Begrenzungs Linie mit einer negativen y-Komponente schneidet, wird der Count-Wert verringert.

Das System hebt das Pixel hervor, wenn der Count-Wert ungleich 0 (null) ist.

 

 



