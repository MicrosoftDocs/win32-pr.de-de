---
description: In diesem Thema wird beschrieben, wie benutzerdefinierte Pipelineobjekte variable Wiedergaberaten unterstützen können, einschließlich umgekehrter Wiedergabe. Informationen zur Verwendung der Ratensteuerung aus einer Anwendung finden Sie unter Ratensteuerung.
ms.assetid: 077678db-ca5a-423b-9430-93497113d639
title: Implementieren der Ratensteuerung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a3ff90e7b1748efd4cfcff41244164d1d6a997b6208d3e46afa0cdae9aa6bba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120114270"
---
# <a name="implementing-rate-control"></a>Implementieren der Ratensteuerung

In diesem Thema wird beschrieben, wie benutzerdefinierte Pipelineobjekte variable Wiedergaberaten unterstützen können, einschließlich umgekehrter Wiedergabe. Informationen zur Verwendung der Ratensteuerung aus einer Anwendung finden Sie unter [Ratensteuerung.](rate-control.md)

Dieses Thema enthält folgende Abschnitte:

-   [Medienquellen](#media-sources)
-   [Media Foundation Transformationen](#media-foundation-transforms)
    -   [Umgekehrte Wiedergabe](#reverse-playback)
-   [Mediensenken](#media-sinks)
-   [Zugehörige Themen](#related-topics)

Wenn Sie ein Microsoft Media Foundation Pipelineobjekt (Eine Medienquelle, Transformation oder Mediensenke) schreiben, müssen Sie möglicherweise variable Wiedergaberaten unterstützen. Implementieren Sie dazu die folgenden Schnittstellen:

1.  Implementieren Sie die [**INTERFACESGetService-Schnittstelle.**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
2.  Unterstützen Sie den **DIENST MF RATE CONTROL \_ \_ \_ SERVICE.** (Siehe [Dienstschnittstellen](service-interfaces.md).)
3.  Implementieren Sie die [**INTERFACESRateSupport-Schnittstelle,**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) die die vom -Objekt unterstützten Wiedergaberaten erhält.
4.  Implementieren Sie die [**INTERFACESRateControl-Schnittstelle,**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) die die Wiedergaberate abgibt oder festlegt.

## <a name="media-sources"></a>Medienquellen

Wenn eine Medienquelle die Ratensteuerung unterstützt, sollte sie sowohl [**DIE AuslastungssteuerungSunterstützung als**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) auch [**DIE VONSTRATEControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)implementieren. Andernfalls meldet die Mediensitzung, dass die minimale und maximale Wiedergaberate 1,0 beträgt, unabhängig davon, welche anderen Komponenten sich in der Pipeline befinden.

Die Wiedergaberate wirkt sich nicht auf die Präsentationszeiten der Beispiele aus, sodass die Medienquelle ihre Zeitstempel nicht anpassen sollte. Stattdessen wird die Präsentationsuhr schneller oder langsamer ausgeführt. Für die umgekehrte Wiedergabe liefert die Quelle Stichproben in umgekehrter Reihenfolge mit abnehmenden Zeitstempeln.

Der *fThin-Parameter* der [**PARAMETERSRATEControl::SetRate-Methode**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate) gibt an, ob die Medienquelle den Inhalt *ausdehnen* soll. Thinning gilt in erster Linie für Videostreams. Im schlanken Modus löscht die Quelle Deltaframes und liefert nur Keyframes. Bei sehr hohen Wiedergaberaten überspringt die Quelle möglicherweise einige Keyframes (z. B. alle anderen Keyframes).

Die Quelle muss keine Audiobeispiele im schlanken Modus löschen. Bei sehr hohen Wiedergaberaten ist die Quelle jedoch möglicherweise nicht in der Lage, Daten schnell zu lesen, um die Beispielanforderungen der Pipeline zu erfüllen. In diesem Fall muss die Quelle möglicherweise einige Audiodaten löschen. In diesem Falle sollte versucht werden, Audiobeispiele zu übermitteln, die sich in der Nähe der Videobeispiele befinden (vorausgesetzt, die Quelle verfügt über beide Arten von Streams).

Wenn ein Stream zwischen dem modus "thinned" und "non-thinned" übergibt, sendet er ein [MEStreamThinMode-Ereignis.](mestreamthinmode.md)

Wenn die Medienquelle einen Aufruf von [**SetRate**](/windows/desktop/api/mfidl/nf-mfidl-imfratecontrol-setrate)abschließt, sendet sie das [MESourceRateChanged-Ereignis.](mesourceratechanged.md)

Während der umgekehrten Wiedergabe:

-   Die Medienquelle übermittelt Stichproben in umgekehrter Reihenfolge, ohne die Zeitstempel anzupassen.
-   Zeitstempel innerhalb eines Streams sollten monoton verringert werden.
-   Der Anfang des Inhalts wird als Ende des Streams betrachtet. Nachdem jeder Medienstream das erste Beispiel im Stream übermittelt hat (d. h. präsentationszeit = 0), sendet er das [MEEndOfStream-Ereignis.](meendofstream.md)

## <a name="media-foundation-transforms"></a>Media Foundation Transformationen

Im Allgemeinen benötigt eine Media Foundation-Transformation (MFT) keine explizite Unterstützung für die Ratensteuerung, es sei denn, der MFT implementiert eine nicht schlanke umgekehrte Wiedergabe.

Wenn ein MFT die [**INTERFACESRateSupport-Schnittstelle**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) nicht implementiert, geht die Mediensitzung von Folgendem aus:

-   Der MFT unterstützt Arbitary-Wiedergaberaten für die Vorwärtswiedergabe, sowohl schlanke als auch nicht schlanke Wiedergabe.
-   Der MFT unterstützt die verfeinerte umgekehrte Wiedergabe, aber keine nicht schlanke umgekehrte Wiedergabe.

Wenn eine dieser Bedingungen nicht zutrifft, sollte der MFT DIE BEDINGUNGEN FÜR DIE Implementierung von [**"THICKNESSRateSupport"**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) und [**"THICKNESSRateControl"**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)implementieren.

### <a name="reverse-playback"></a>Umgekehrte Wiedergabe

Die Mediensitzung kann auch dann umgekehrt wiedergegeben werden, wenn eine oder mehrere Transformationen in der Pipeline die umgekehrte Wiedergabe nicht explizit unterstützen.

Wenn ein MFT die [**INTERFACESRateSupport-Schnittstelle**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) nicht verfügbar macht, verwendet die Mediensitzung für die umgekehrte Wiedergabe *die Ausdrückung* wie folgt:

-   Die Mediensitzung sendet Keyframes auf die übliche Weise an den MFT, indem [**SIE ÜBERTRANSFORM::P rocessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput)aufrufen.

-   Die Mediensitzung löscht Deltaframes und ersetzt sie durch [MEStreamTick-Ereignisse.](mestreamtick.md)

-   Zwischen jedem Beispiel leert die Mediensitzung den MFT, um Fehler zu vermeiden, die durch die Tatsache verursacht werden, dass die Zeitstempel abnehmen.

Ein Beispiel gilt als Keyframe, wenn das [MFSampleExtension \_ CleanPoint-Attribut](mfsampleextension-cleanpoint-attribute.md) auf **TRUE** festgelegt ist, und als Deltaframe, wenn dieses Attribut **FALSE** ist oder nicht festgelegt ist.

Wenn die [**MFT-Schnittstelle DIE Übergreifende**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)Unterstützung implementiert, verwendet die Mediensitzung diese Schnittstelle, um zu ermitteln, ob der MFT die nicht schlanke umgekehrte Wiedergabe unterstützt. Wenn der MFT die nicht schlanke umgekehrte Wiedergabe unterstützt, übermittelt die Mediensitzung alle Samplings in umgekehrter Reihenfolge, ohne Samplings zu löschen oder den MFT zu leeren.

Wenn ein MFT die nicht ausgediente umgekehrte Wiedergabe unterstützt, sollte er die [**INTERFACESRateControl-Schnittstelle**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) implementieren. Die Mediensitzung verwendet diese Schnittstelle, um den MFT zu benachrichtigen, wenn eine umgekehrte Wiedergabe erfolgt. An diesem Punkt muss der MFT darauf vorbereitet sein, dass die Zeitstempel verringert werden und Deltaframes in umgekehrter Reihenfolge eintreffen. Ein Decoder muss in der Regel Stichproben puffern, bis er eine ganze Gruppe von Bildern (GOP) empfangen hat. Anschließend wird der gesamte GOP decodiert und die decodierten Frames in der richtigen (umgekehrten) Reihenfolge ausgegeben.

## <a name="media-sinks"></a>Mediensenken

Wenn eine Mediensenke *ratenlos* ist, geht die Mediensitzung davon aus, dass die Mediensenke jede Wiedergaberate verarbeiten kann. Die Mediensenke muss [**NICHT DIE IMPLEMENTRATESupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)implementieren. (Eine ratenlose Mediensenke gibt MEDIASINK \_ zurück. RATELESS-Flag aus der [**NSSink::GetCharacteristics-Methode.)**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getcharacteristics)

Andernfalls sollte eine Mediensenke [**DIE UNTERSTÜTZUNG VONRATESupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport) implementieren, wenn sie andere Wiedergaberaten als 1.0 verarbeiten kann.

Mediensenken sollten [**NICHT DIE IMPLEMENTRATEControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)-Datei implementieren. Wenn sich die Wiedergaberate ändert, ruft die Präsentationsuhr die [**ENClockStateSink::OnClockSetRate-Methode**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclocksetrate) der Mediensenke auf.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ratensteuerung](rate-control.md)
</dt> <dt>

[Suchen, Vorlauf und Umgekehrtes Wiedergeben](seeking--fast-forward--and-reverse-play.md)
</dt> </dl>

 

 



