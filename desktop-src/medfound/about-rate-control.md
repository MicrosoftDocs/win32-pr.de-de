---
description: Informationen zur Rate Control
ms.assetid: 509b2cc8-6017-41a9-ae80-9af21dce9367
title: Informationen zur Rate Control
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61ae8ad5bcfaaf415c888418a7a6bd5d77f72434150e30fcac071d078b8ee6d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035658"
---
# <a name="about-rate-control"></a>Informationen zur Rate Control

In Media Foundation wird die *Wiedergaberate* als Verhältnis der aktuellen Wiedergaberate zur normalen Wiedergaberate ausgedrückt. Beispielsweise ist eine Rate von 2,0 doppelt normal und 0,5 halb normal. Negative Werte geben die umgekehrte Wiedergabe an. Eine Wiedergaberate von -2,0 wird mit doppelter Normalgeschwindigkeit rückwärts durch den Stream übertragen. Eine Rate von 0 (null) bewirkt, dass ein Frame gerendert wird. Danach wird die Präsentationsuhr nicht mehr voran. Um einen weiteren Frame mit der Rate von 0 (null) zu erhalten, muss die Anwendung eine neue Position suchen.

Anwendungen verwenden die folgenden Schnittstellen, um die Wiedergaberate zu steuern.

-   [**DURCHATTENRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport). Wird verwendet, um die schnellsten und langsamsten Wiedergaberaten zu finden, die möglich sind.
-   [**ATRATEControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol). Wird verwendet, um die Wiedergaberate zu ändern.

Um diese beiden Schnittstellen zu erhalten, rufen [**Sie INTGETService::GetService in**](/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice) der Mediensitzung auf. Der Dienstbezeichner ist MF \_ RATE \_ CONTROL \_ SERVICE.

Mithilfe des Rate Control-Diensts kann eine Anwendung eine schnelle Vorwärts- und Umgekehrtwiedergabe implementieren.

## <a name="thinning"></a>Ausdünnung

*Thinning ist* ein beliebiger Prozess, der die Anzahl der Stichproben in einem Stream reduziert, um die Bitrate insgesamt zu reduzieren. Bei Videos erfolgt die Verankerung in der Regel durch Löschen der Deltaframes und Bereitstellen nur der Keyframes. Häufig kann die Pipeline schnellere Wiedergaberaten mit schlanker Wiedergabe unterstützen, da die Datenrate niedriger ist, da Deltaframes nicht decodiert werden.

Die Verankerung ändert weder die Zeitstempel noch die Dauer der Stichproben. Wenn die Nominalrate des Videostreams beispielsweise 25 Frames pro Sekunde beträgt, wird die Dauer jedes Frames weiterhin als 40 Millisekunden markiert, auch wenn die Medienquelle alle Deltaframes verdrungen hat. Das bedeutet, dass zwischen dem Ende eines Frames und dem Anfang des nächsten Frames eine Zeitlücke besteht.

## <a name="scrubbing"></a>Scrubbing (Bereinigung)

*Bereinigung ist* der Prozess der sofortigen Suche nach bestimmten Punkten im Stream durch Interaktion mit einer Bildlaufleiste, Zeitachse oder einer anderen visuellen Darstellung der Zeit. Der Begriff stammt aus der Zeit von Bandplayern, die eine Rolle hin und her geschoben haben, um einen Abschnitt zu finden, wie das Bereinigung des Wiedergabekopfs mit dem Band.

Die Bereinigung wird in der Media Foundation, indem die Wiedergaberate auf 0 (null) gesetzt wird. Weitere Informationen finden Sie unter [How to Perform Scrubbing](how-to-perform-scrubbing.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Rate Control](rate-control.md)
</dt> <dt>

[Suchen, Vorlauf und Umgekehrtes Wiederkehren](seeking--fast-forward--and-reverse-play.md)
</dt> <dt>

[Dienstschnittstellen](service-interfaces.md)
</dt> </dl>

 

 



