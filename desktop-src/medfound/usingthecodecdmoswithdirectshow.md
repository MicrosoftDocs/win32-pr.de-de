---
description: Verwenden der Fenster Medien Codecs in DirectShow
ms.assetid: 5b930447-6bf2-4bb3-8dfb-05f4c1e7cd64
title: Verwenden der Fenster Medien Codecs in DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb521c0e3897dc2415fbd613f97b755a146657d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343380"
---
# <a name="using-the-window-media-codecs-in-directshow"></a>Verwenden der Fenster Medien Codecs in DirectShow

Die Windows Media Audio-und Video Encoder-und Decoder-Objekte wurden ursprünglich entworfen und optimiert, um mit dem Datei Containerformat ASF und dem SDK für den Windows Media-Format arbeiten zu können. Die Codec-Objekte funktionieren in DirectShow für bestimmte Szenarien gut, d.... Dies gilt für CBR und eine qualitativ hochwertige VBR-Codierung von Videodaten strömen. Wenn Sie jedoch erwägen, die Codec-Objekte direkt in DirectShow mithilfe von Datei Containern als ASF zu verwenden, gibt es bestimmte Verhalten und Probleme, die Sie im Voraus beachten sollten.

> [!Note]  
> Wenn Sie eigenständige Codecs mit DirectShow verwenden möchten, sollten Sie Sie wahrscheinlich nur als DMOS verwenden. Anders ausgedrückt: Sie verwenden die [**imediaobject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) -Schnittstelle anstelle von [**IMF Transform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform).

 

## <a name="wm-audio-in-avi-files"></a>WM-Audiodatei in AVI-Dateien

Mithilfe von DirectShow können Sie WMA-Streams in ein beliebiges Datei Containerformat codieren, für das Sie einen Multiplexer-Filter verwenden. Die Windows Media Audio-und Video-Codec-Schnittstellen unterstützen WMA in AVI-Dateien jedoch nicht, da es nicht möglich ist, die standardmäßigen DirectShow-AVI-Wiedergabe Filter zu verwenden, um die audiovideosynchronisierung in einer AVI-Datei mit einem WMA-Stream aufrechtzuerhalten. Weitere Informationen finden Sie unter [Speichern von komprimierten Medien in AVI-Dateien](storingcompressedmediainavifiles.md).

Der Audioencoder-DMO gibt Stichproben unterschiedlicher Dauer aus, auch wenn der Modus "Konstante Bitrate" angezeigt wird. Dies funktioniert daher am besten mit Datei Containerformaten, die Zeitstempel verwenden. AVI-Dateien stellen keinen Zeitstempel für jedes Audiobeispiel oder jede Gruppe von Beispielen bereit. In DirectShow stellt der avi-Splitter Filter Zeitstempel für jede Gruppe von Stichproben (jeden audioframe) basierend auf dem **navgbytespersec** -Wert in der [**WaveFormatEx**](/previous-versions/dd757713(v=vs.85)) -Struktur im AVI-Streamheader her.

Die Annahme, dass diese Berechnung zugrunde liegt, besteht darin, dass alle Audiobeispiele im Stream die gleiche Dauer haben. die vom DMO ausgegebenen Beispiele sind jedoch nicht identisch, sodass die vom avi-Splitter angewendeten Zeitstempel nicht exakt sind. Aus diesem Grund ist es nicht möglich, den avi-Splitter oder den Audiodecoder-DMO zu ändern, um die Verwendung einer beliebigen DirectShow-basierten Anwendung für die Wiedergabe von AVI-Dateien mit Audiodaten und Videostreams synchron zu verwenden. In einigen Fällen funktioniert der Voice-Codec von Windows Media Audio 9, aber auch dies verliert nach jedem Suchvorgang die Synchronisierung, sodass er nicht als geeignete Lösung angesehen werden kann.

Wenn Sie über einen MP3-Encoder verfügen, können Sie AVI-Dateien mit WMV und MP3 für den Audiostream erstellen. Diese Dateien werden in Windows Media Player und anderen DirectShow-basierten Anwendungen ordnungsgemäß wiedergegeben, da der avi-Splitter einen speziellen Behandlungs Code für MP3-Streams enthält. Eine andere Möglichkeit ist die Verwendung von unkomprimierter PCM-Audiodaten, obwohl die resultierende Dateigröße deutlich größer als bei einem komprimierten Audiodatenstrom ist. Da die DirectShow-Beispielanwendung AVI-Dateien erstellt, wird die Verwendung des Audioencoders DMO nicht veranschaulicht.

## <a name="one-pass-encoding"></a>One-Pass-Codierung

Der Video Encoder DMO funktioniert problemlos in DirectShow für zwei Codierungs Modi: CBR und Qualitäts basiertes VBR. Solange Sie bei der Erstellung des Filter Diagramms auf die richtige Reihenfolge der Vorgänge folgen, wie in der Beispielanwendung veranschaulicht, ist es relativ einfach, WMV-Inhalte mithilfe von AVI Multiplexer und dem dateiwriter in eine AVI-Datei zu platzieren.

## <a name="two-pass-encoding"></a>Zwei-Pass-Codierung

Die zwei-Pass-Codierungs Modi erfordern einen komplexeren Ansatz zum entwickeln und Streamen von Diagrammen, um zu verhindern, dass der DMO seinen Inhalt vor dem zweiten Durchlauf aus dem ersten Durchlauf legt. Bei der Codierung mit zwei Durchgängen ist es erforderlich, das Diagramm einmal auszuführen, damit DMO seine Vorverarbeitungs Analyse der Datei Daten durchführen kann. Anschließend wird das Diagramm zurück gezeichnet und erneut ausgeführt, damit das DMO die tatsächliche Codierung durchführen kann.

Wenn das Diagramm für den zweiten Durchlauf in den Lauf Zustand wechselt, legt der DMO-Wrapper das discontinuity-Flag für das erste Beispiel fest, da der Zeitstempel nicht mit dem letzten Zeitstempel im ersten Durchlauf sequenziell ist. Wenn der DMO, der nicht für die Ausführung in DirectShow entworfen wurde, das discontinuity-Flag empfängt, führt er eine Leerung aus und verliert die vom ersten Durchlauf gespeicherten Daten. Um dieses Problem zu umgehen, besteht die beste Lösung wahrscheinlich darin, einen benutzerdefinierten DMO-Wrapper Filter zu schreiben, der das discontinuity-Flag nicht festgelegt, wenn das Diagramm nach dem ersten Durchlauf als Seeding festgelegt wird. Das Beispiel Video für Windows (Vfw) in diesem SDK veranschaulicht, wie die zwei-Pass-Codierung ausgeführt wird.

## <a name="interlaced-content"></a>Zeilen Sprung Inhalt

Der WMV Encoder DMO ist in der Lage, Zeilen Sprung Inhalte zu codieren, während die Überlappung beibehalten wird. Dies ist nützlich für Inhalte, die von einem Fernsehgerät aufgezeichnet werden und möglicherweise auch auf einem Fernsehgerät wiedergegeben werden. Es ist jedoch nicht möglich, die Überlappung mit dem standardmäßigen DMO-Wrapper beizubehalten, da dieser Filter [**inssbuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer) in den Eingabe Beispielen nicht unterstützt.

Der DMO verwendet diese Schnittstelle zum Abrufen der Zeilen Sprung Einstellungen für jedes empfangene Beispiel. Wenn die Schnittstelle nicht gefunden wird, wie es bei dem DMO-Wrapper der Fall ist, behandelt die DMO einfach die Eingabe Beispiele als nicht-Zeilen Sprung. Zum Ausführen von Zeilen Sprung Codierung in DirectShow gibt es mehrere Alternativen. Am einfachsten ist es, das Windows Media Format 9-Serien-SDK entweder direkt oder mithilfe des "WM ASF Writer DirectShow Filter" zu verwenden, um eine Zeilen Sprung-ASF-Datei zu erstellen. Anschließend können Sie diese Datei in ein anderes Format umwandeln. Wenn Sie in AVI umwandeln, verfügen Sie über eine Zeilen Sprung Datei, aber die standardmäßigen DirectShow AVI-Wiedergabe Filter erkennen Sie nicht als solche, da Sie [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2)nicht unterstützen. Ein anderer Ansatz besteht darin, einen eigenen DMO-Wrapper Filter zu schreiben, der die [**inssbuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer) -Schnittstelle unterstützt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Arbeiten mit Codec-DMOS](workingwithcodecdmos.md)
</dt> </dl>

 

 
