---
description: Erstellen eines Graph
ms.assetid: 2302bb40-a5db-473a-afeb-71905ac41f47
title: Erstellen eines Graph
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8ff89cff8662bb5da81860053221596b18e89ab2300134cf2ff8826ae99b787
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120108220"
---
# <a name="creating-an-audio-capture-graph"></a>Erstellen eines Graph

Der erste Schritt für eine Audioerfassungsanwendung ist das Erstellen eines Filterdiagramms. Die Konfiguration des Diagramms hängt vom Typ der Datei ab, die Sie erstellen möchten.

-   Rein audiobasierte AVI-Datei: Filter für Audioaufnahme nach [AVI Mux-Filter](avi-mux-filter.md) und AVI Mux zu [File Writer-Filter.](file-writer-filter.md)
-   WAV-Datei: Audio Capture Filter to [WavDest Filter Sample](wavdest-filter-sample.md) to File Writer Filter
-   Windows Medienaudiodatei (WMA): Audioaufnahmefilter für [WM ASF](wm-asf-writer-filter.md) Writer-Filter.

Der WavDest-Filter wird als SDK-Beispiel bereitgestellt. Um ihn zu verwenden, müssen Sie den Filter erstellen und registrieren.

Um den ASF Writer-Filter zu verwenden, müssen Sie das Windows Media SDK installieren und einen Softwareschlüssel abrufen, um den Filter zu entsperren. Weitere Informationen finden Sie unter [Verwenden von Windows Medien in DirectShow.](using-windows-media-in-directshow.md)

Sie können das Filterdiagramm mithilfe des [Capture Graph Builder-Objekts](capture-graph-builder.md) erstellen, oder Sie können das Diagramm "manuell" erstellen. Das heißt, die Anwendung muss jeden Filter programmgesteuert hinzufügen und verbinden. In diesem Artikel wird der manuelle Ansatz beschrieben. Weitere Informationen zur Verwendung von Capture Graph Builder finden Sie unter [Video capture](video-capture.md). Ein Großteil der Informationen in diesem Artikel gilt für rein audiobasierte Diagramme.

Hinzufügen des Audioaufnahmegeräts

Da der Audioaufnahmefilter mit einem bestimmten Hardwaregerät kommuniziert, können Sie **CoCreateInstance** nicht einfach aufrufen, um den Filter zu erstellen. Verwenden Sie stattdessen den [Systemgeräte-Enumerator,](system-device-enumerator.md) um alle Geräte in der Kategorie "Audioaufnahmequellen" aufzuzählen, die durch den Klassenbezeichner CLSID \_ AudioInputDeviceCategory identifiziert wird.

Der Systemgeräte-Enumerator gibt eine Liste von Monikern für die Geräte zurück. Der Anzeigename jedes Monikers entspricht dem Namen des Geräts. Wählen Sie einen der zurückgegebenen Moniker aus, und verwenden Sie ihn, um eine Instanz des Audioaufnahmefilters für dieses Gerät zu erstellen. Fügen Sie den Filter dem Filterdiagramm hinzu. Das bevorzugte Audioaufzeichnungsgerät des Benutzers wird zuerst in der Monikerliste angezeigt. (Der Benutzer wählt ein bevorzugtes Gerät aus, indem er in Systemsteuerung auf Sounds und Multimedia klickt.)

Weitere Informationen finden Sie unter [Verwenden des Systemgeräte-Enumerators](using-the-system-device-enumerator.md).

Rufen Sie zum Angeben der zu erfassenden Eingabe die [**IAMAudioInputMixer-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer) aus dem Audio capture-Filter ab, und rufen Sie die **\_ put Enable-Methode** auf, um die Eingabe anzugeben. Eine Einschränkung dieser Methode besteht jedoch darin, dass verschiedene Hardwaregeräte unterschiedliche Zeichenfolgen verwenden können, um ihre Eingaben zu identifizieren. Beispielsweise kann eine Karte "Mikrofon" verwenden, um die Mikrofoneingabe zu identifizieren, und eine andere Karte kann "Mikrofon" verwenden. Um den Zeichenfolgenbezeichner für eine bestimmte Eingabe zu bestimmen, verwenden Sie die Windows Multimediafunktionen [**waveOutOpen**](/previous-versions//dd743866(v=vs.85)), [**mixerOpen**](/previous-versions//dd757308(v=vs.85))und [**mixerGetLineInfo**](/previous-versions//dd757303(v=vs.85)). Weitere Informationen finden Sie im MSDN-Thema [Mixer Geräteabfragen.](/windows/desktop/Multimedia/mixer-device-queries)

Hinzufügen des Multiplexers und des Dateiwriters

Ein Audioaufnahmegraph muss einen Multiplexer und einen Dateiwriter enthalten.

Ein *Multiplexer* ist ein Filter, der einen oder mehrere Datenströme in einem einzelnen Stream mit einem bestimmten Format kombiniert. Beispielsweise kombiniert der AVI Mux-Filter Audio- und Videostreams in einem verschachtelten AVI-Stream. Für die Audioaufnahme gibt es in der Regel nur einen einzelnen Audiodatenstrom, aber die Audiodaten müssen weiterhin in einem Format gepackt werden, das auf dem Datenträger gespeichert werden kann, was einen Multiplexer erfordert. Die Wahl des Multiplexers hängt vom Zielformat ab:

-   AVI: AVI Multiplexer
-   WAV: WavDest
-   WMA: ASF Writer

Ein *Dateiwriter* ist ein Filter, der eingehende Daten in eine Datei schreibt. Verwenden Sie für AVI- oder WAV-Dateien den [Dateiwriterfilter](file-writer-filter.md). Bei WMA-Dateien fungiert der ASF Writer sowohl als Multiplexer als auch als Dateiwriter.

Nachdem Sie die Filter erstellt und dem Diagramm hinzugefügt haben, verbinden Sie den Ausgabepin des Audioaufnahmefilters mit dem Eingabepin des Multiplexers, und verbinden Sie den Ausgabepin des Multiplexers mit dem Eingabepin des Filterwriters (vorausgesetzt, es handelt sich dabei um separate Filter). Um den Dateinamen anzugeben, fragen Sie den Dateiwriter nach der [**IFileSinkFilter-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) ab, und rufen Sie die [**IFileSinkFilter::SetFileName-Methode**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter-setfilename) auf.

### <a name="example-code"></a>Beispielcode

Das folgende Beispiel zeigt, wie Sie mithilfe des WavDest-Filters ein Audioaufnahmediagramm erstellen. Die gleichen Prinzipien gelten für die anderen Dateitypen.


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



In diesem Beispiel werden die `AddFilterByCLSID` unter Hinzufügen eines Filters nach [CLSID](add-a-filter-by-clsid.md)beschriebene Funktion und die `ConnectFilters` in Verbinden Zwei [Filter](connect-two-filters.md)beschriebene Funktion verwendet. Keine dieser ApIs ist eine DirectShow-API.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Audioaufnahme](audio-capture.md)
</dt> </dl>

 

 
