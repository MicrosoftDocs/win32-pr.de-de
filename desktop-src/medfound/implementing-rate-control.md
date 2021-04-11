---
description: In diesem Thema wird beschrieben, wie benutzerdefinierte Pipeline Objekte Variablen Wiedergabe Raten unterstützen können, einschließlich umgekehrter Wiedergabe. Informationen zur Verwendung der Raten Steuerung in einer Anwendung finden Sie unter Raten Steuerung.
ms.assetid: 077678db-ca5a-423b-9430-93497113d639
title: Implementieren der Raten Steuerung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5fd78cbbb95316a0d4ed12a50c9d3aa8954fe8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042646"
---
# <a name="implementing-rate-control"></a>Implementieren der Raten Steuerung

In diesem Thema wird beschrieben, wie benutzerdefinierte Pipeline Objekte Variablen Wiedergabe Raten unterstützen können, einschließlich umgekehrter Wiedergabe. Informationen zur Verwendung der Raten Steuerung in einer Anwendung finden Sie unter [Raten Steuerung](rate-control.md).

Dieses Thema enthält folgende Abschnitte:

-   [Medienquellen](#media-sources)
-   [Media Foundation Transformationen](#media-foundation-transforms)
    -   [Umgekehrte Wiedergabe](#reverse-playback)
-   [Medien senken](#media-sinks)
-   [Zugehörige Themen](#related-topics)

Wenn Sie ein Microsoft Media Foundation Pipeline Objekt (eine Medienquelle, eine Transformation oder eine Medien Senke) schreiben, müssen Sie möglicherweise Variablen Wiedergabe Raten unterstützen. Implementieren Sie zu diesem Zweck die folgenden Schnittstellen:

1.  Implementieren Sie die [**IMF GetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) -Schnittstelle.
2.  Unterstützung des MF-Dienst Dienstanbieter Dienst. **\_ \_ \_** (Siehe [Dienst Schnittstellen](service-interfaces.md).)
3.  Implementieren Sie die [**imfratesupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) -Schnittstelle, die die vom-Objekt unterstützten Wiedergabe Raten abruft.
4.  Implementieren Sie die [**imfratecontrol**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) -Schnittstelle, mit der die Wiedergabe Rate abgerufen oder festgelegt wird.

## <a name="media-sources"></a>Medienquellen

Wenn eine Medienquelle die Raten Steuerung unterstützt, sollte sowohl [**imfratesupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) als auch [**imfratecontrol**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)implementiert werden. Andernfalls meldet die Medien Sitzung, dass die minimale und die maximale Wiedergabe Rate 1,0 ist, unabhängig davon, welche anderen Komponenten in der Pipeline sind.

Die Wiedergabe Rate wirkt sich nicht auf die Präsentations Zeiten der Beispiele aus, sodass die Medienquelle ihre Zeitstempel nicht anpassen sollte. Stattdessen wird die Präsentations Uhr schneller oder langsamer ausgeführt. Bei umgekehrter Wiedergabe stellt die Quelle Beispiele in umgekehrter Reihenfolge bereit, wobei Zeitstempel verringert werden.

Der *Parameter "* Parameter" der [**imfratecontrol:: ltrate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) -Methode gibt an, ob der Inhalt von der Medienquelle *schlank* sein soll. Die Verdünnung bezieht sich hauptsächlich auf Videostreams. Im dünnen Modus löscht die Quelle Delta Frames und stellt nur Keyframes bereit. Bei sehr hohen Wiedergabe Raten kann die Quelle einige Keyframes überspringen (z. b. jeden anderen Keyframe übermitteln).

Die Quelle muss keine Audiobeispiele im dünnen Modus ablegen. Bei sehr hohen Wiedergabe Raten ist die Quelle jedoch möglicherweise nicht in der Lage, Daten schnell zu lesen, um die Beispiel Anforderungen der Pipeline auszufüllen. In diesem Fall muss die Quelle eventuell einige Audiodaten löschen. Wenn dies der Fall ist, sollten Sie versuchen, Audiobeispiele zu übermitteln, die sich in der Zeit der Videobeispiele nähern (vorausgesetzt, dass die Quelle beide Arten von Datenstrom aufweist).

Wenn ein Stream zwischen dem dünnen und dem nicht dünnen Modus übergeht, sendet er ein [mestreamthinmode](mestreamthinmode.md) -Ereignis.

Wenn die Medienquelle einen aufzurufenden aufrufsvorgang abschließt [**, sendet**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate)Sie das [mesourceratechanged](mesourceratechanged.md) -Ereignis.

Bei umgekehrter Wiedergabe:

-   Die Medienquelle stellt Beispiele in umgekehrter Reihenfolge bereit, ohne dass die Zeitstempel angepasst werden.
-   Zeitstempel in einem Stream sollten sich monoton verringern.
-   Der Anfang des Inhalts wird als Ende des Streams betrachtet. Nachdem jeder Mediendaten Strom das erste Beispiel im Stream übermittelt hat (d. h. Präsentationszeit = 0), sendet er das [meendof Stream](meendofstream.md) -Ereignis.

## <a name="media-foundation-transforms"></a>Media Foundation Transformationen

Im allgemeinen benötigt eine Media Foundation Transformation (MFT) keine explizite Unterstützung für die Raten Steuerung, es sei denn, der MFT implementiert eine nicht schlanke umgekehrte Wiedergabe.

Wenn eine MFT die [**imfratesupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) -Schnittstelle nicht implementiert, wird von der Medien Sitzung Folgendes vorausgesetzt:

-   Der MFT unterstützt die beliebiges-Wiedergabe Raten für die vorwärts Wiedergabe, sowohl für schlank als auch für nicht-dünn.
-   Der MFT unterstützt die schlanke rückgängigwiedergabe, unterstützt jedoch nicht die nicht schlanke umgekehrte Wiedergabe.

Wenn eine dieser Bedingungen nicht zutrifft, sollte der MFT [**imfratesupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) und [**imfratecontrol**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)implementieren.

### <a name="reverse-playback"></a>Umgekehrte Wiedergabe

Die Medien Sitzung kann in umgekehrter Reihenfolge wiedergegeben werden, auch wenn eine oder mehrere Transformationen in der Pipeline die umgekehrte Wiedergabe nicht explizit unterstützen.

Wenn eine MFT die [**imfratesupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) -Schnittstelle nicht verfügbar macht, verwendet die Medien Sitzung die *Verdünnung* für die umgekehrte Wiedergabe wie folgt:

-   Die Medien Sitzung sendet Keyframes auf die übliche Weise an die MFT, indem [**imftransform::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput)aufgerufen wird.

-   Die Medien Sitzung löscht Delta Frames und ersetzt Sie durch [mestreamtick](mestreamtick.md) -Ereignisse.

-   Zwischen den einzelnen Beispielen leert die Medien Sitzung die MFT, um Fehler zu vermeiden, die durch die Tatsache verursacht werden, dass die Zeitstempel abnimmt.

Ein Beispiel wird als Keyframe betrachtet, wenn das " [mfsampleextension"- \_ Cleanpoint](mfsampleextension-cleanpoint-attribute.md) -Attribut auf " **true**" festgelegt ist, und wird als Delta Frame betrachtet, wenn dieses Attribut " **false** " oder nicht festgelegt ist.

Wenn der MFT [**imfratesupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)implementiert, verwendet die Medien Sitzung diese Schnittstelle, um zu ermitteln, ob die MFT eine nicht schlanke umgekehrte Wiedergabe unterstützt. Wenn die MFT eine nicht schlanke umgekehrte Wiedergabe unterstützt, werden alle Beispiele in umgekehrter Reihenfolge von der Medien Sitzung übermittelt, ohne dass Beispiele gelöscht oder die MFT geleert werden muss.

Wenn eine MFT eine nicht schlanke umgekehrte Wiedergabe unterstützt, sollte Sie die [**imfratecontrol**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) -Schnittstelle implementieren. Die Medien Sitzung verwendet diese Schnittstelle, um die MFT zu benachrichtigen, wenn die umgekehrte Wiedergabe erfolgt. An diesem Punkt muss die MFT vorbereitet werden, damit die Zeitstempel abnimmt und Delta Frames in umgekehrter Reihenfolge eintreffen. Ein Decoder muss in der Regel Stichproben Puffern, bis er eine ganze Gruppe von Bildern (GOP) empfangen hat. Anschließend wird der gesamte GOP decodiert und die decodierten Frames in der korrekten (umgekehrten) Reihenfolge ausgegeben.

## <a name="media-sinks"></a>Medien senken

Wenn eine Medien Senke nicht mehr vorhanden ist, geht die Medien Sitzung davon *aus, dass* die Medien Senke jede Wiedergabe Rate verarbeiten kann. Die Medien Senke muss [**imfratesupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)nicht implementieren. (Eine ratlose Medien Senke gibt den mediasink \_ zurück. Gebühren Loses Flag von der [**imfmediasink:: getcharacteristics**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getcharacteristics) -Methode.)

Andernfalls sollte eine Medien Senke [**imfratesupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) implementieren, wenn Sie andere Wiedergabe Raten als 1,0 verarbeiten kann.

Für Medien senken sollte [**imfratecontrol**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)nicht implementiert werden. Wenn sich die Wiedergabe Rate ändert, ruft die Präsentationszeit die Methode [**IMF clockstaatink:: onclocksetrate**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) der Medien Senke auf.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Raten Steuerung](rate-control.md)
</dt> <dt>

[Suchen, schnelles vorwärts und umgekehrtes spielen](seeking--fast-forward--and-reverse-play.md)
</dt> </dl>

 

 



