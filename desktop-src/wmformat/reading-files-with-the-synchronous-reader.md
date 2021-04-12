---
title: Lesen von Dateien mit dem synchronen Reader
description: Lesen von Dateien mit dem synchronen Reader
ms.assetid: 18c6c0cd-478f-4325-b23e-571c33779a96
keywords:
- Windows Media-Format-SDK, Lesen von Dateien
- SDK für den Windows Media-Format, synchrone Reader
- Advanced Systems Format (ASF), synchrone Reader
- ASF (Advanced Systems Format), synchrone Reader
- Advanced Systems Format (ASF), Lesen von Dateien
- ASF (Advanced Systems Format), Lesen von Dateien
- synchrone Reader, iwmreadercallback-Schnittstelle
- Iwmreadercallback, synchrone Reader
- synchrone Leser, Lesen von Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 893a1bd324cdc91968e423f2084bfdba5ef57c8e
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104389850"
---
# <a name="reading-files-with-the-synchronous-reader"></a>Lesen von Dateien mit dem synchronen Reader

Sie können den synchronen Reader verwenden, um eine ASF-Datei mit synchronen Aufrufen anstelle der asynchronen Methoden im Reader-Objekt zu lesen. Die Verwendung von synchronen Aufrufen reduziert die Anzahl der Threads, die zum Lesen einer Datei erforderlich sind. Der asynchrone Reader verwendet mehrere Threads, um Datenströme zu verarbeiten. Für Dateien mit mehreren Streams kann die Anzahl der verwendeten Threads sehr groß werden. Der synchrone Reader verwendet nur einen Thread.

Der synchrone Reader wurde entwickelt, um die Anforderungen der Inhaltserstellung und der Datei Bearbeitungsanwendungen zu erfüllen. Sie können den synchronen Reader für andere Anwendungen verwenden, seine Funktionalität ist jedoch begrenzt.

Der synchrone Reader kann lokale Dateien oder Dateien in einem Netzwerk mithilfe des UNC-Pfadnamens öffnen (z \\ \\ . b. "someshare \\ somedirectory \\ somefile. wmv"). Sie können keine Dateien an den synchronen Reader streamen oder Dateien von einem Internet Speicherort aus öffnen. Der synchrone Reader bietet auch Unterstützung für die Verwendung der **IStream** -com-Schnittstelle als Quelle.

Der synchrone Reader bietet mehr Flexibilität beim Abrufen von Beispielen aus einer ASF-Datei als der asynchrone Reader. Der synchrone Reader kann Beispiele nach streamnummer und Ausgabe bereitzustellen. Die von der Datenstrom Nummer übermittelten Beispiele können komprimiert oder dekomprimiert werden. Der synchrone Reader kann während der Wiedergabe auch zwischen komprimierter und nicht komprimierter Übermittlung wechseln. Diese Funktion wird als "schnelles bearbeiten" bezeichnet. Diese Funktion ermöglicht es einer Bearbeitungs Anwendung, Windows Media-basierte Inhalte zu lesen und direkt an den Writer weiterzuleiten, bis ein gewünschter Frame erreicht wird. An diesem Punkt kann die Anwendung den Reader anweisen, nicht komprimierte Inhalte bereitzustellen, die von der Anwendung dann geändert und zur erneuten Komprimierung an den Writer übergeben werden können. Wenn die Anwendung das Ändern der angegebenen Frames abgeschlossen hat, kann Sie den Reader anweisen, mit der Übermittlung von komprimierten Frames zu beginnen.

Die grundlegende Funktionalität des synchronen Reader-Objekts kann in die folgenden Schritte aufgeteilt werden. In den folgenden Schritten bezieht sich "die Anwendung" auf das Programm, das Sie mit dem Windows Media-Format-SDK schreiben.

1.  Die Anwendung übergibt dem synchronen Reader den Namen einer zu lesenden Datei. Wenn die Datei vom synchronen Reader geöffnet wird, wird jedem Stream eine Ausgabe Nummer zugewiesen. Wenn die Datei einen gegenseitigen Ausschluss verwendet, weist der Reader eine einzelne Ausgabe für alle sich gegenseitig ausschließenden Streams zu.
2.  Die Anwendung ruft Informationen zur Konfiguration der verschiedenen Ausgaben des Readers ab. Die gesammelten Informationen ermöglichen der Anwendung das ordnungsgemäße Rendering von Medien Beispielen.
3.  Die Anwendung beginnt, nacheinander Beispiele vom synchronen Reader anzufordern. Der synchrone Reader stellt jedes Beispiel in einem Puffer Objekt bereit, für das es die [**inssbuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer) -Schnittstelle übermittelt.
4.  Die Anwendung ist für das Rendern von Daten verantwortlich, nachdem Sie vom Reader zugestellt wurde. Das Windows Media-Format-SDK stellt keine renderingroutinen bereit. In der Regel verwenden Anwendungen andere SDKs zum Rendering von Daten, z. b. das Microsoft Direct X SDK, oder die Multimedia-Funktionen des Microsoft Windows Platform SDK.

Diese Schritte werden in der Beispielanwendung wmsynkreader veranschaulicht. Weitere Informationen finden Sie unter [Beispielanwendungen](sample-applications.md).

Der synchrone Reader unterstützt auch erweiterte Funktionen. Der synchrone Reader ermöglicht Ihnen Folgendes:

-   Geben Sie einen Bereich von Stichproben an, die nach Zeit oder nach Frame Nummer abgerufen werden sollen.
-   Steuern der Streamauswahl für sich gegenseitig ausschließende Streams.
-   Öffnen Sie eine Datei mit der Standard-COM-Schnittstelle **IStream**.
-   Liest Profildaten aus dem Dateiheader.
-   Lesen von Metadaten aus dem Dateiheader.
-   Wechsel zwischen Stream-und Ausgabe Beispielen während der Wiedergabe.
-   Zwischen komprimierten und unkomprimierten streambeispielen während der Wiedergabe wechseln.

In den folgenden Abschnitten wird die Verwendung des synchronen Reader-Objekts ausführlich beschrieben.

-   [So erstellen Sie einen synchronen Reader und öffnen eine Datei](to-create-a-synchronous-reader-and-open-a-file.md)
-   [So suchen Sie nach streamnummern und Ausgabe Nummern](to-find-stream-numbers-and-output-numbers.md)
-   [So rufen Sie Medien Beispiele mit dem synchronen Reader ab](to-retrieve-media-samples-with-the-synchronous-reader.md)
-   [So suchen Sie nach Zeit mithilfe des synchronen Readers](to-seek-by-time-using-the-synchronous-reader.md)
-   [So suchen Sie nach Frame Nummer mithilfe des synchronen Readers](to-seek-by-frame-number-using-the-synchronous-reader.md)
-   [So suchen Sie nach SMPTE-Zeit Code mithilfe des synchronen Readers](to-seek-by-smpte-time-code-using-the-synchronous-reader.md)
-   [So rufen Sie streambeispiele mit dem synchronen Reader ab](to-retrieve-stream-samples-with-the-synchronous-reader.md)
-   [So rufen Sie komprimierte Beispiele mit dem synchronen Reader ab](to-retrieve-compressed-samples-with-the-synchronous-reader.md)

**Beispiel Code**

Der folgende Beispielcode zeigt, wie Sie mit dem synchronen Reader Beispiele aus einer ASF-Datei lesen. Er gibt nach Frame Nummer einen Bereich von zu über liegende Stichproben an.


```C++
IWMSyncReader* pSyncReader = NULL;
INSSBuffer*    pMyBuffer   = NULL;

QWORD cnsSampleTime = 0;
QWORD cnsSampleDuration = 0;
DWORD dwFlags = 0;
DWORD dwOutputNumber;
HRESULT hr = S_OK;

// Initialize COM.
hr = CoInitialize(NULL);

// Create a synchronous reader.
hr = WMCreateSyncReader(NULL, WMT_RIGHT_PLAYBACK, &pSyncReader);

// Open an ASF file.
hr = pSyncReader->Open(L"c:\\somefile.wmv");

// TODO: Identify the properties for each output. This works 
// exactly as it does with the asynchronous reader.

// Specify a playback range from frame number 100 of the video 
// stream to the end of the file. Assume that the video stream 
// is stream number 2.
hr = pSyncReader->SetRangeByFrame(2, 100, 0);

// Loop through all the samples in the specified range.
do
{
   // Get the next sample, regardless of its stream number.
   hr = pSyncReader->GetNextSample(0,
                                   &pMyBuffer,
                                   &cnsSampleTime,
                                   &cnsSampleDuration,
                                   &dwFlags,
                                   &dwOutputNumber,
                                   NULL);

   if(SUCCEEDED(hr))
   {
      // TODO: Process the sample in whatever way is appropriate 
      // to your application. When finished, clean up.
      pMyBuffer->Release();
      pMyBuffer = NULL;
      cnsSampleTime     = 0;
      cnsSampleDuration = 0;
      dwFlags           = 0;
      dwOutputNumber    = 0;
   }
} 
while (SUCCEEDED(hr));

pSyncReader->Release();
pSyncReader = NULL;

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Iwmsynkreader-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[**Lesen von ASF-Dateien**](reading-asf-files.md)
</dt> <dt>

[**Synchrones Reader-Objekt**](synchronous-reader-object.md)
</dt> </dl>

 

 




