---
description: Jedes Mal, wenn eine Anwendung einen Domänen Controller erstellt und sofort mit dem Aufrufen von GDI-Zeichnungs-oder-Ausgabefunktionen beginnt, nutzt Sie den standardmäßigen Seiten Raum für den Geräteraum und die Transformationen für den Geräte Speicherplatz auf dem Client Bereich.
ms.assetid: 64465eb4-d23a-44e7-ad0d-060b195d37b3
title: Standard Transformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab5f13c764a92c005fad36c9f2599b99a654284f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978688"
---
# <a name="default-transformations"></a>Standard Transformationen

Jedes Mal, wenn eine Anwendung einen Domänen Controller erstellt und sofort mit dem Aufrufen von GDI-Zeichnungs-oder-Ausgabefunktionen beginnt, nutzt Sie den standardmäßigen Seiten Raum für den Geräteraum und die Transformationen für den Geräte Speicherplatz auf dem Client Bereich. Eine Transformation für Welt-zu-Seite-Speicherplatz kann erst auftreten, wenn die Anwendung die [**setgraphicsmode**](/windows/desktop/api/Wingdi/nf-wingdi-setgraphicsmode) -Funktion aufruft, um den Modus auf "GM Advanced" festzulegen, \_ und dann die Funktion " [**setworldtransform**](/windows/desktop/api/Wingdi/nf-wingdi-setworldtransform) " aufruft.

Die Verwendung von mm \_ -Text (die standardmäßige Transformation für den Seiten Raum für den Geräteraum) führt zu einer eins-zu-Eins-Zuordnung, d. h. ein angegebener Punkt im Seiten Raum wird dem gleichen Punkt im Geräteraum zugeordnet. Wie bereits erwähnt, wird diese Transformation nicht durch eine Matrix angegeben. Stattdessen wird Sie durch Aufteilen der Breite des Viewports durch die Breite des Fensters und durch die Höhe des Viewports um die Höhe des Fensters erreicht. Im Standardfall sind die Viewport-Dimensionen 1 Pixel und 1 Pixel, und die Fenster Dimensionen sind 1-Seiten-Einheit um 1-Seiteneinheit.

Die Transformation für den Geräte Speicherplatz zu physischem Gerät (Client Bereich, Desktop oder Drucker) führt immer zu einer eins-zu-Eins-Zuordnung. Das heißt, eine Einheit im Gerätebereich entspricht immer einer Einheit im Client Bereich, auf dem Desktop oder auf einer Seite. Der einzige Zweck dieser Transformation ist die Übersetzung. Dadurch wird sichergestellt, dass die Ausgabe ordnungsgemäß im Fenster einer Anwendung angezeigt wird, unabhängig davon, wo das Fenster auf dem Desktop verschoben wird.

Der einzige eindeutige Aspekt von mm \_ -Text ist die Ausrichtung der y-Achse im Seitenbereich. In mm \_ -Text wird die positive y-Achse nach unten erweitert, und die negative y-Achse wird aufwärts erweitert.

 

 



