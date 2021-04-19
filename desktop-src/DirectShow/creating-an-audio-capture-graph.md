---
description: Erstellen eines audioerfassungs Diagramms
ms.assetid: 2302bb40-a5db-473a-afeb-71905ac41f47
title: Erstellen eines audioerfassungs Diagramms
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bd3c731a7dc498fcb7180bc56ae6a7f94dbec6d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106346419"
---
# <a name="creating-an-audio-capture-graph"></a>Erstellen eines audioerfassungs Diagramms

Der erste Schritt für eine audioerfassungs Anwendung ist die Erstellung eines Filter Diagramms. Die Konfiguration des Diagramms hängt von dem Typ der Datei ab, die Sie erstellen möchten.

-   Reine Audiodatei: audioerfassungs Filter nach [AVI MUX](avi-mux-filter.md) -Filter und AVI MUX in [File Writer](file-writer-filter.md) Filter.
-   WAV-Datei: audioerfassungs Filter für [wavdest Filter Sample](wavdest-filter-sample.md) to File Writer Filter
-   Windows Media Audio Datei (. WMA): audioerfassungs Filter für den [WM-ASF-Writer](wm-asf-writer-filter.md) -Filter.

Der wavdest-Filter wird als SDK-Beispiel bereitgestellt. Um es zu verwenden, müssen Sie den Filter erstellen und registrieren.

Wenn Sie den ASF-Writer-Filter verwenden möchten, müssen Sie das Windows Media SDK installieren und einen Software Schlüssel abrufen, um den Filter zu entsperren. Weitere Informationen finden Sie unter [Verwenden von Windows Media in DirectShow](using-windows-media-in-directshow.md).

Sie können das Filter Diagramm mit dem [Erfassungs Diagramm](capture-graph-builder.md) -Generator-Objekt erstellen, oder Sie können das Diagramm manuell erstellen. Das heißt, dass die Anwendung jeden Filterprogramm gesteuert hinzufügen und verbinden kann. In diesem Artikel wird die manuelle Vorgehensweise beschrieben. Weitere Informationen zur Verwendung des Erfassungs Diagramm-Generators finden Sie unter [Video Aufzeichnung](video-capture.md). Ein Großteil der Informationen in diesem Artikel gilt für reine audiodiagramme.

Hinzufügen des audioerfassungs Geräts

Da der audioerfassungs Filter mit einem bestimmten Hardware Gerät kommuniziert, können Sie nicht einfach **cokreateinstance** aufrufen, um den Filter zu erstellen. Verwenden Sie stattdessen den [Enumerator "System Geräte](system-device-enumerator.md) ", um alle Geräte in der Kategorie "audioerfassungs Quellen" aufzulisten, die durch den Klassen Bezeichner CLSID \_ audioinputdevicecategory gekennzeichnet wird.

Der Enumerator für System Geräte gibt eine Liste der Moniker für die Geräte zurück. der Anzeige Name jedes Monikers entspricht dem Namen des Geräts. Wählen Sie einen der zurückgegebenen Moniker aus, und verwenden Sie ihn zum Erstellen einer Instanz des audioerfassungs Filters für dieses Gerät. Fügen Sie den Filter dem Filter Diagramm hinzu. Das bevorzugte audioaufzeichnungs Gerät des Benutzers wird zuerst in der monikerliste angezeigt. (Der Benutzer wählt ein bevorzugtes Gerät aus, indem er in der Systemsteuerung auf Sounds und Multimedia klickt.)

Weitere Informationen finden Sie unter [using the System Device Enumerator](using-the-system-device-enumerator.md).

Zum Angeben der Eingabe, die von erfasst werden soll, rufen Sie die [**IAMAudioInputMixer**](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer) -Schnittstelle aus dem audioerfassungs Filter ab und rufen die **Put \_ enable** -Methode auf, um die Eingabe anzugeben. Eine Einschränkung dieser Methode besteht jedoch darin, dass unterschiedliche Hardware Geräte verschiedene Zeichen folgen verwenden können, um Ihre Eingaben zu identifizieren. Beispielsweise kann eine Karte "Mikrofon" verwenden, um die Mikrofon Eingabe zu identifizieren, und eine andere Karte kann "MIC" verwenden. Um den Zeichen folgen Bezeichner für eine bestimmte Eingabe zu ermitteln, verwenden Sie die Windows Multimedia Functions [**WaveOutOpen**](/previous-versions//dd743866(v=vs.85)), [**mixeropen**](/previous-versions//dd757308(v=vs.85))und [**mixergetlineinfo**](/previous-versions//dd757303(v=vs.85)). Weitere Informationen finden Sie im MSDN-Thema [Mixer Geräte Abfragen](/windows/desktop/Multimedia/mixer-device-queries) .

Hinzufügen von Multiplexer und dateiwriter

Ein audioerfassungs Diagramm muss einen Multiplexer und einen dateiwriter enthalten.

Ein *Multiplexer* ist ein Filter, der einen oder mehrere Streams in einem einzigen Stream mit einem bestimmten Format kombiniert. Der AVI MUX-Filter kombiniert z. b. Audio-und Videostreams in einem verschachtelten AVI-Stream. Für die Audioerfassung gibt es in der Regel nur einen einzigen Audiostream, aber die Audiodaten müssen immer noch in ein Format gepackt werden, das auf dem Datenträger gespeichert werden kann. hierfür ist ein Multiplexer erforderlich. Die Auswahl von Multiplexer ist vom Zielformat abhängig:

-   AVI: AVI Multiplexer
-   WAV: wavdest
-   WMA: ASF-Writer

Ein *dateiwriter* ist ein Filter, der eingehende Daten in eine Datei schreibt. Verwenden Sie für AVI-oder WAV-Dateien den [dateiwriter-Filter](file-writer-filter.md). Bei WMA-Dateien fungiert der ASF-Writer sowohl als Multiplexer als auch als dateiwriter.

Nachdem Sie die Filter erstellt und dem Diagramm hinzugefügt haben, verbinden Sie die Ausgabe-PIN des audioerfassungs Filters mit der Eingabe-PIN des Multiplexers, und verbinden Sie die Ausgabe-PIN des Multiplexers mit der Eingabe-PIN des filterwriters (angenommen, dies sind separate Filter). Um den Dateinamen anzugeben, Fragen Sie den dateiwriter nach der [**ifilesinkfilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) -Schnittstelle ab, und nennen Sie die [**ifilesinkfilter:: setFileName**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter-setfilename) -Methode.

### <a name="example-code"></a>Beispielcode

Im folgenden Beispiel wird gezeigt, wie ein audioerfassungs Diagramm mit dem wavdest-Filter erstellt wird. Die gleichen Prinzipien gelten für die anderen Dateitypen.


```C++
IBaseFilter *pSrc = NULL, *pWaveDest = NULL, *pWriter = NULL;
IFileSinkFilter *pSink= NULL;
IGraphBuilder *pGraph;

// Create the Filter Graph Manager.
hr = CoCreateInstance(CLSID_FilterGraph, NULL, CLSCTX_INPROC_SERVER,
    IID_IGraphBuilder, (void**)&pGraph);

// This example omits error handling.

// Not shown: Use the System Device Enumerator to create the 
// audio capture filter.

// Add the audio capture filter to the filter graph. 
hr = pGraph->AddFilter(pSrc, L"Capture");

// Add the WavDest and the File Writer.
hr = AddFilterByCLSID(pGraph, CLSID_WavDest, L"WavDest", &pWaveDest);
hr = AddFilterByCLSID(pGraph, CLSID_FileWriter, L"File Writer", &pWriter);

// Set the file name.
hr = pWriter->QueryInterface(IID_IFileSinkFilter, (void**)&pSink);
hr = pSink->SetFileName(L"C:\\MyWavFile.wav", NULL);

// Connect the filters.
hr = ConnectFilters(pGraph, pSrc, pWaveDest);
hr = ConnectFilters(pGraph, pWaveDest, pWriter);

// Not shown: Release interface pointers.

```



In diesem Beispiel `AddFilterByCLSID` wird die unter [Hinzufügen eines Filters nach CLSID](add-a-filter-by-clsid.md)beschriebene Funktion und die `ConnectFilters` in Verbinden von [zwei Filtern](connect-two-filters.md)beschriebene Funktion verwendet. Keines dieser APIs ist eine DirectShow-API.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Audioerfassung](audio-capture.md)
</dt> </dl>

 

 
