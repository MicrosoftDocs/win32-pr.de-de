---
description: Verwenden der Fenstermediencodecs in DirectShow
ms.assetid: 5b930447-6bf2-4bb3-8dfb-05f4c1e7cd64
title: Verwenden der Fenstermediencodecs in DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 495a2675335474351da80b9845fba67f9e967d637d7c9d9c749ffc2f12ce3ea4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012180"
---
# <a name="using-the-window-media-codecs-in-directshow"></a>Verwenden der Fenstermediencodecs in DirectShow

Die Windows Medienaudio- und Videoencoderobjekte wurden ursprünglich für die Arbeit mit dem ASF-Dateicontainerformat und dem Windows Media Format SDK entworfen und optimiert. Die Codecobjekte funktionieren in DirectShow für bestimmte Szenarien gut, nämlich für 1-Pass-CBR und qualitätsbasierte VBR-Codierung von Videostreams. Wenn Sie jedoch erwägen, die Codecobjekte direkt in DirectShow mit anderen Dateicontainern als ASF zu verwenden, gibt es bestimmte Verhaltensweisen und Probleme, die Sie im Voraus kennen sollten.

> [!Note]  
> Wenn Sie eigenständige Codecs mit DirectShow verwenden möchten, sollten Sie sie wahrscheinlich nur als DMOs verwenden. Anders ausgedrückt: Sie verwenden die [**IMediaObject-Schnittstelle**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject) anstelle von [**DURCHSICHTTransform.**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

 

## <a name="wm-audio-in-avi-files"></a>WM-Audio in AVI-Dateien

Sie können DirectShow verwenden, um WMA-Streams in ein beliebiges Dateicontainerformat zu codieren, für das Sie über einen Multiplexerfilter verfügen. Die Codecschnittstellen Windows Media Audio und Video unterstützen WMA in AVI-Dateien jedoch nicht, da es mithilfe der standardmäßigen DirectShow AVI-Wiedergabefilter nicht möglich ist, die Audiovideosynchronisierung in einer AVI-Datei mit einem WMA-Stream zu verwalten. Weitere Informationen finden Sie unter [Speichern komprimierter Medien in AVI-Dateien.](storingcompressedmediainavifiles.md)

Der Audioencoder DMO Stichproben mit unterschiedlicher Dauer aus, selbst wenn er sich im Modus "Konstante Bitrate" befindet. Es funktioniert daher am besten mit Dateicontainerformaten, die Zeitstempel verwenden. AVI-Dateien stellen keinen Zeitstempel für jedes Audiobeispiel oder jede Gruppe von Beispielen zur Verfügung. In DirectShow stellt der AVI-Splitterfilter Zeitstempel für jede Gruppe von Stichproben (jeden Audioframe) basierend auf dem **nAvgBytesPerSec-Wert** in der [**WAVEFORMATEX-Struktur**](/previous-versions/dd757713(v=vs.85)) im AVI-Streamheader zusammen.

Die Annahme, die dieser Berechnung zugrunde liegt, ist, dass alle Audiobeispiele im Stream eine gleiche Dauer haben. Die Stichproben, die vom DMO ausgegeben werden, sind jedoch nicht gleich lange, sodass die vom AVI-Splitter angewendeten Zeitstempel nicht genau sind. Daher ist es nicht möglich, ohne den AVI-Splitter oder den Audiodecoder DMO zu ändern, eine directShow-basierte Anwendung zu verwenden, um AVI-Dateien mit synchronen Audio- und Videostreams wieder zu wieder geben. Der Windows Media Audio 9 Voice-Codec funktioniert in einigen Fällen, aber auch dieser Vorgang verliert nach jedem Suchvorgang die Synchronisierung, sodass er nicht wirklich als praktikable Lösung angesehen werden kann.

Wenn Sie über einen MP3-Encoder verfügen, können Sie AVI-Dateien mit WMV und MP3 für den Audiostream erstellen. Solche Dateien werden in Windows Media Player und anderen DirectShow-basierten Anwendungen ordnungsgemäß abspielt und suchen, da der AVI-Splitter speziellen Behandlungscode für MP3-Streams enthält. Eine weitere Möglichkeit ist die Verwendung von unkomprimiertem PCM-Audio, obwohl die resultierende Dateigröße deutlich größer ist als bei einem komprimierten Audiostream. Da die DirectShow-Beispielanwendung AVI-Dateien erstellt, wird die Verwendung des Audioencoder-DMO.

## <a name="one-pass-encoding"></a>One-Pass-Codierung

Der Videoencoder DMO funktioniert problemlos in DirectShow für zwei Codierungsmodi: CBR und qualitätsbasierte VBR. Solange Sie beim Erstellen des Filterdiagramms die richtige Reihenfolge der Vorgänge befolgen, wie in der Beispielanwendung gezeigt, ist es relativ einfach, WMV-Inhalte mithilfe des AVI-Multiplexers und des File Writer in eine AVI-Datei zu platzieren.

## <a name="two-pass-encoding"></a>Codierung mit zwei Durchgangen

Die Codierungsmodi mit zwei Durchgang erfordern einen komplexeren Ansatz zum Erstellen und Streamen von Diagrammen, um zu verhindern, dass DMO den Inhalt des ersten Durchgangs leert, bevor der zweite Durchgang beginnt. Bei der Codierung mit zwei Durchlaufs ist es erforderlich, den Graphen einmal ausführen, damit die DMO ihre Vorverarbeitungsanalyse der Dateidaten ausführen kann. Anschließend wird das Diagramm zurückgelädt und erneut ausgeführt, damit die DMO die eigentliche Codierung durchführen kann.

Wenn das Diagramm für den zweiten Durchlauf in einen Ausführungszustand übergeht, legt der DMO-Wrapper das DISCONTINUITY-Flag für das erste Beispiel fest, da der Zeitstempel nicht sequenziell mit dem letzten Zeitstempel des ersten Durchlaufs ist. Wenn der DMO, der auf diese Weise nicht in DirectShow funktioniert, das FLAG DISCONTINUITY empfängt, führt er eine Leerung durch und verliert die vom ersten Durchlauf gespeicherten Daten. Um dieses Problem zu beheben, besteht die beste Lösung wahrscheinlich im Schreiben eines benutzerdefinierten DMO-Wrapperfilters, der das DISCONTINUITY-Flag nicht festgelegt, wenn das Diagramm nach dem ersten Durchlauf durchgesuchet wird. Das Video for Windows (VfW)-Beispiel in diesem SDK veranschaulicht, wie die Codierung mit zwei Durchgangen funktioniert.

## <a name="interlaced-content"></a>Interlaced Content

Der WMV-Encoder DMO in der Lage, interlaced-Inhalte zu codieren, während das Interlacing beibehalten wird. Dies ist nützlich für Inhalte, die von einem TV erfasst werden und möglicherweise auch auf einem TV-Gerät wiedergeknendet werden. Es ist jedoch nicht möglich, interlacing mithilfe des standardmäßigen DMO Wrappers zu erhalten, da dieser Filter [**INSSBuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer) für seine Eingabebeispiele nicht unterstützt.

Die DMO verwendet diese Schnittstelle, um die Interlaced-Einstellungen für jedes empfangene Beispiel zu erhalten. Wenn die Schnittstelle nicht gefunden wird, wie dies beim DMO Wrapper der Fall ist, behandelt der DMO die Eingabebeispiele einfach als nicht geschachtelt. Für die Interlacingcodierung in DirectShow gibt es mehrere Alternativen. Der einfachste Ansatz ist wahrscheinlich die Verwendung des Windows Media Format 9 Series SDK entweder direkt oder mithilfe des WM ASF Writer DirectShow-Filters, um eine ASF-Datei mit Interlacing zu erstellen. Sie können diese Datei dann in ein anderes Format transcodieren. Wenn Sie in AVI transcodieren, verfügen Sie über eine Interlaced-Datei, aber die standardmäßigen DirectShow AVI-Wiedergabefilter erkennen sie nicht als solche, da sie [**VIDEOINFOHEADER2 nicht unterstützen.**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) Ein anderer Ansatz ist das Schreiben eines eigenen DMO Wrapperfilters, der die [**INSSBuffer-Schnittstelle**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer) unterstützt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Arbeiten mit Codec-DMOs](workingwithcodecdmos.md)
</dt> </dl>

 

 
