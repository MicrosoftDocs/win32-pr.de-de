---
description: Wenn eine Anwendung einen DC erstellt und sofort mit dem Aufrufen von GDI-Zeichnungs- oder -Ausgabefunktionen beginnt, nutzt sie den Standardseitenbereich für Gerätebereich und Gerätebereich zu Clientbereichstransformationen.
ms.assetid: 64465eb4-d23a-44e7-ad0d-060b195d37b3
title: Standardtransformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ba34effd9d6d43ab3b0abc740250c58788a8ce2f1556e89c92b78af823e58c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119469680"
---
# <a name="default-transformations"></a>Standardtransformationen

Wenn eine Anwendung einen DC erstellt und sofort mit dem Aufrufen von GDI-Zeichnungs- oder -Ausgabefunktionen beginnt, nutzt sie den Standardseitenbereich für Gerätebereich und Gerätebereich zu Clientbereichstransformationen. Eine World-to-Page-Raumtransformation kann erst durchgeführt werden, wenn die Anwendung zuerst die [**SetGraphicsMode-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-setgraphicsmode) aufruft, um den Modus auf GM ADVANCED und dann die \_ [**SetWorldTransform-Funktion**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) aufruft.

Die Verwendung von MM TEXT (die Standardtransformation von Seitenbereich zu Gerätebereich) führt zu einer 1:1-Zuordnung, d. h., ein angegebener Punkt im Seitenbereich wird dem gleichen Punkt im Gerätebereich \_ angezeigt. Wie bereits erwähnt, wird diese Transformation nicht durch eine Matrix angegeben. Stattdessen wird die Breite des Viewports durch die Breite des Fensters und die Höhe des Viewports durch die Höhe des Fensters dividieren. Im Standardfall sind die Viewportdimensionen 1 Pixel by 1 Pixel und die Fensterdimensionen 1-Seiten-Einheit nach 1-Seiten-Einheit.

Die Transformation zwischen Gerätebereich und physischem Gerät (Clientbereich, Desktop oder Druckerdruck) führt immer zu einer 1:1-Zuordnung. Das heißt, eine Einheit im Gerätebereich entspricht immer einer Einheit im Clientbereich, auf dem Desktop oder auf einer Seite. Der einzige Zweck dieser Transformation ist die Übersetzung. es stellt sicher, dass die Ausgabe im Fenster einer Anwendung ordnungsgemäß angezeigt wird, unabhängig davon, wo dieses Fenster auf dem Desktop verschoben wird.

Der einzige eindeutige Aspekt von MM \_ TEXT ist die Ausrichtung der y-Achse im Seitenbereich. In MM \_ TEXT wird die positive y-Achse nach unten und die negative Y-Achse nach oben erweitert.

 

 



