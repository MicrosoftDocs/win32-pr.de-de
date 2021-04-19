---
description: Informationen zur Raten Kontrolle
ms.assetid: 509b2cc8-6017-41a9-ae80-9af21dce9367
title: Informationen zur Raten Kontrolle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3757e4d1d8a374061ff0c0e7fe02ba3c62243c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346306"
---
# <a name="about-rate-control"></a>Informationen zur Raten Kontrolle

In Media Foundation wird die *Wiedergabe Rate* als Verhältnis zwischen der aktuellen Wiedergabe Rate und der normalen Wiedergabe Rate ausgedrückt. Beispielsweise ist die Rate 2,0 doppelt so hoch, dass 0,5 eine halbe normale Geschwindigkeit ist. Negative Werte geben die umgekehrte Wiedergabe an. Die Wiedergabe Rate von-2,0 wird mit der doppelten Geschwindigkeit der normalen Geschwindigkeit rückwärts durchlaufen. Eine Rate von NULL bewirkt, dass ein Frame gerendert wird. Danach wird die Präsentationszeit nicht Fortschritt. Um einen weiteren Frame mit der Rate 0 zu erhalten, muss die Anwendung an einer neuen Position suchen.

Anwendungen verwenden die folgenden Schnittstellen zum Steuern der Wiedergabe Rate.

-   [**Imfratesupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport). Wird verwendet, um die schnellsten und langsamsten Wiedergabe Raten zu ermitteln, die möglich sind.
-   [**Imfratecontrol**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol). Wird verwendet, um die Wiedergabe Rate zu ändern.

Um diese beiden Schnittstellen abzurufen, nennen Sie [**imfgetservice:: GetService**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) für die Medien Sitzung. Der Dienst Bezeichner ist der MF- \_ Raten \_ Steuerungs \_ Dienst.

Mithilfe des Raten Steuerungs Dienstanbieter kann eine Anwendung die schnelle Vorwärts-und Rückwärts Wiedergabe implementieren.

## <a name="thinning"></a>Wird dünner

Die *Verdünnung* ist ein beliebiger Prozess, bei dem die Anzahl der Stichproben in einem Stream verringert wird, um die allgemeine Bitrate zu verringern. Bei Video wird die Verdünnung in der Regel durch Löschen der Delta Frames und Bereitstellung der Keyframes erreicht. Häufig kann die Pipeline schnellere Wiedergabe Raten mithilfe der dünnen Wiedergabe unterstützen, da die Datenrate geringer ist, da Delta Frames nicht decodiert werden.

Beim dünken werden die Zeitstempel oder die Dauer der Stichproben nicht geändert. Wenn die nominale Rate des Videodaten Stroms z. b. 25 Frames pro Sekunde beträgt, wird die Dauer jedes Frames weiterhin als 40 Millisekunden gekennzeichnet, auch wenn die Medienquelle alle Delta Frames löscht. Dies bedeutet, dass zwischen dem Ende eines Frames und dem Beginn der nächsten ein Zeitunterschied besteht.

## <a name="scrubbing"></a>Scrubbing (Bereinigung)

*Scrubbing* ist der Prozess der sofortigen Suche nach bestimmten Punkten im Stream durch Interaktion mit einer Scrollleiste, einer Zeitachse oder einer anderen visuellen Darstellung der Zeit. Die Bezeichnung ergibt sich aus dem Zeitpunkt der Band-zu-Band-bandspieler, wenn eine Bewegung hin und her herumrollt, um zu ermitteln, ob der Wiedergabe Kopf mit dem Band bereinigt wurde.

Das Scrubbing wird in Media Foundation implementiert, indem die Wiedergabe Rate auf NULL festgelegt wird. Weitere Informationen finden Sie unter Vorgehens [Weise beim Ausführen von Scrubbing](how-to-perform-scrubbing.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Raten Steuerung](rate-control.md)
</dt> <dt>

[Suchen, schnelles vorwärts und umgekehrtes spielen](seeking--fast-forward--and-reverse-play.md)
</dt> <dt>

[Dienst Schnittstellen](service-interfaces.md)
</dt> </dl>

 

 



