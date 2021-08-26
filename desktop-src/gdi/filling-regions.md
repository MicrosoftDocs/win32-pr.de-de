---
description: Eine Anwendung füllt das Innere eines Bereiches aus, indem sie die FillRgn-Funktion aufruft und ein Handle an die Hand gibt, das einen bestimmten Pinsel identifiziert.
ms.assetid: 6174b2ea-836a-4538-a0ad-e123c88fc6f6
title: Füllen von Regionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d909643155b027f72b4235db366e640d7e53dacd4825b85090f9958aec1c94c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120015400"
---
# <a name="filling-regions"></a>Füllen von Regionen

Eine Anwendung füllt das Innere eines Bereiches aus, indem sie die [**FillRgn-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-fillrgn) aufruft und ein Handle an die Hand gibt, das einen bestimmten Pinsel identifiziert. Wenn eine Anwendung FillRgn aufruft, füllt das System den Bereich mit dem Pinsel aus, indem der aktuelle Füllmodus für den angegebenen Gerätekontext verwendet wird. Es gibt zwei Füllmodi: Alternative und Füllung. Die Anwendung kann den Füllmodus für einen Gerätekontext festlegen, indem sie die [**Funktion SetPolyFillMode**](/windows/desktop/api/Wingdi/nf-wingdi-setpolyfillmode) aufruft. Die Anwendung kann den aktuellen Füllmodus für einen Gerätekontext abrufen, indem sie die [**GetPolyFillMode-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-getpolyfillmode) aufruft.

Die folgende Abbildung zeigt zwei identische Bereiche: eine mit einem alternativen Modus gefüllt und die andere mit dem Wickelmodus.

![Abbildung mit zwei fünf punktenden Sternen: einer nur mit den Punkten gefüllt, der andere vollständig ausgefüllt](images/csrgn-03.png)

## <a name="alternate-mode"></a>Alternativer Modus

Führen Sie den folgenden Test aus, um zu bestimmen, welche Pixel das System bei Angabe des alternativen Modus hebt:

1.  Wählen Sie ein Pixel im inneren Bereich aus.
2.  Zeichnen Sie einen imaginären Strahl in der positiven X-Richtung von diesem Pixel in Richtung Unendlichkeit.
3.  Jedes Mal, wenn der Strahl eine Begrenzungslinie überschneidet, erhöhen Sie einen Count-Wert.

Das System hebt das Pixel hervor, wenn der Count-Wert eine ungerade Zahl ist.

## <a name="winding-mode"></a>Wickelmodus

Führen Sie den folgenden Test aus, um zu bestimmen, welche Pixel das System bei Angabe des Wickelmodus hebt:

1.  Bestimmen Sie die Richtung, in der jede Begrenzungslinie gezeichnet wird.
2.  Wählen Sie ein Pixel im inneren Bereich aus.
3.  Zeichnen Sie einen imaginären Strahl in der positiven X-Richtung vom Pixel in Richtung Unendlichkeit.
4.  Jedes Mal, wenn der Strahl eine Begrenzungslinie mit einer positiven y-Komponente überschneidet, erhöhen Sie einen Count-Wert. Jedes Mal, wenn der Strahl eine Begrenzungslinie mit einer negativen y-Komponente überschneidet, dekrementiert den Count-Wert.

Das System hebt das Pixel hervor, wenn der Count-Wert ungleich 0 (null) ist.

 

 



