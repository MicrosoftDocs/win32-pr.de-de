---
title: Lesen von Dateien mit dem synchronen Reader
description: Lesen von Dateien mit dem synchronen Reader
ms.assetid: 18c6c0cd-478f-4325-b23e-571c33779a96
keywords:
- Windows Medienformat-SDK, Lesen von Dateien
- Windows Medienformat-SDK, synchrone Reader
- Advanced Systems Format (ASF), synchrone Reader
- ASF (Advanced Systems Format), synchrone Reader
- Advanced Systems Format (ASF), Lesen von Dateien
- ASF (Advanced Systems Format), Lesen von Dateien
- Synchrone Reader,IWMReaderCallback-Schnittstelle
- IWMReaderCallback, synchrone Reader
- Synchrone Reader,Lesen von Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c30ed2f9af78c9643f269adb24f740f2fe9227bc2e5b8a36d5c9d29606564176
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118197472"
---
# <a name="reading-files-with-the-synchronous-reader"></a>Lesen von Dateien mit dem synchronen Reader

Sie können den synchronen Reader verwenden, um eine ASF-Datei mit synchronen Aufrufen anstelle der asynchronen Methoden im Readerobjekt zu lesen. Die Verwendung synchroner Aufrufe reduziert die Anzahl der Threads, die zum Lesen einer Datei erforderlich sind. Der asynchrone Reader verwendet mehrere Threads für die Verarbeitung von Datenströmen. Bei Dateien mit mehreren Streams kann die Anzahl der verwendeten Threads sehr groß werden. Der synchrone Reader verwendet nur einen Thread.

Der synchrone Reader wurde entwickelt, um die Anforderungen der Inhaltserstellungs- und Dateibearbeitungsanwendungen zu erfüllen. Sie können den synchronen Reader für andere Anwendungen verwenden, seine Funktionalität ist jedoch eingeschränkt.

Der synchrone Reader kann dateien öffnen, die lokal sind, oder Dateien in einem Netzwerk mithilfe des UNC-Pfadnamens (z.B. \\ \\ "someshare \\ \\ somedirectory somefile.wmv"). Sie können keine Dateien an den synchronen Reader streamen oder Dateien von einem Internetspeicherort aus öffnen. Der synchrone Reader bietet auch Unterstützung für die Verwendung der **IStream** COM-Schnittstelle als Quelle.

Der synchrone Reader bietet mehr Flexibilität beim Abrufen von Beispielen aus einer ASF-Datei als der asynchrone Reader. Der synchrone Reader kann Stichproben nach Streamnummer und Ausgabe liefern. Beispiele, die nach Streamnummer übermittelt werden, können komprimiert oder unkomprimiert werden. Der synchrone Reader kann auch während der Wiedergabe zwischen komprimierter und nicht komprimierter Übermittlung wechseln. dieses Feature wird als "schnelle Bearbeitung" bezeichnet. Mit diesem Feature kann eine Bearbeitungsanwendung medienbasierten Windows lesen und direkt an den Writer übergeben, bis ein gewünschter Frame erreicht ist. An diesem Punkt kann die Anwendung dem Leser mitteilen, dass er damit beginnen soll, unkomprimierten Inhalt zu liefern, den die Anwendung dann ändern und zur Erneutkomprimierung an den Writer übergeben kann. Wenn die Anwendung die Änderung der angegebenen Frames abgeschlossen hat, kann sie den Reader anraten, mit der Bereitstellung komprimierter Frames erneut zu beginnen.

Die grundlegendsten Funktionen des synchronen Readerobjekts können in die folgenden Schritte aufgeschlüsselt werden. In diesen Schritten bezieht sich "die Anwendung" auf das Programm, das Sie mit dem Windows Media Format SDK schreiben.

1.  Die Anwendung übergibt den Namen einer zu lesenden Datei an den synchronen Reader. Wenn der synchrone Reader die Datei öffnet, weist er jedem Stream eine Ausgabenummer zu. Wenn die Datei gegenseitigen Ausschluss verwendet, weist der Reader eine einzelne Ausgabe für alle sich gegenseitig ausschließenden Streams zu.
2.  Die Anwendung ruft Informationen zur Konfiguration der verschiedenen Ausgaben vom Reader ab. Die gesammelten Informationen ermöglichen der Anwendung das ordnungsgemäße Rendern von Medienbeispielen.
3.  Die Anwendung beginnt mit dem Anfordern von Stichproben nach dem anderen vom synchronen Reader. Der synchrone Reader stellt jedes Beispiel in einem Pufferobjekt bereit, für das er die [**INSSBuffer-Schnittstelle**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer) übergibt.
4.  Die Anwendung ist für das Rendern von Daten verantwortlich, nachdem sie vom Reader übermittelt wurden. Das Windows Media Format SDK stellt keine Renderingroutinen bereit. In der Regel verwenden Anwendungen andere SDKs zum Rendern von Daten, z. B. das Microsoft Direct X SDK oder die Multimediafunktionen des Microsoft Windows Platform SDK.

Diese Schritte werden in der WMSyncReader-Beispielanwendung veranschaulicht. Weitere Informationen finden Sie unter [Beispielanwendungen](sample-applications.md).

Der synchrone Reader unterstützt auch erweiterte Funktionen. Der synchrone Reader ermöglicht Folgendes:

-   Geben Sie einen Bereich von Stichproben an, der nach Zeit oder Framenummer abgerufen werden soll.
-   Steuern der Streamauswahl für sich gegenseitig ausschließende Streams.
-   Öffnen Sie eine Datei mithilfe der COM-Standardschnittstelle **IStream**.
-   Liest Profildaten aus dem Dateiheader.
-   Liest Metadaten aus dem Dateiheader.
-   Wechseln Sie während der Wiedergabe zwischen Stream- und Ausgabebeispielen.
-   Wechseln zwischen komprimierten und unkomprimierten Streambeispielen während der Wiedergabe.

In den folgenden Abschnitten wird die Verwendung des synchronen Readerobjekts ausführlich beschrieben.

-   [So erstellen Sie einen synchronen Reader und öffnen eine Datei](to-create-a-synchronous-reader-and-open-a-file.md)
-   [So suchen Sie Datenstromnummern und Ausgabenummern](to-find-stream-numbers-and-output-numbers.md)
-   [So rufen Sie Medienbeispiele mit dem synchronen Reader ab](to-retrieve-media-samples-with-the-synchronous-reader.md)
-   [So suchen Sie nach Zeit mithilfe des synchronen Readers](to-seek-by-time-using-the-synchronous-reader.md)
-   [So suchen Sie nach Framenummer mithilfe des synchronen Readers](to-seek-by-frame-number-using-the-synchronous-reader.md)
-   [So suchen Sie mithilfe des synchronen Readers nach SMPTE-Zeitcode](to-seek-by-smpte-time-code-using-the-synchronous-reader.md)
-   [So rufen Sie Streambeispiele mit dem synchronen Reader ab](to-retrieve-stream-samples-with-the-synchronous-reader.md)
-   [So rufen Sie komprimierte Beispiele mit dem synchronen Reader ab](to-retrieve-compressed-samples-with-the-synchronous-reader.md)

**Beispielcode**

Der folgende Beispielcode zeigt, wie Sie Beispiele aus einer ASF-Datei mit dem synchronen Reader lesen. Er gibt nach Framenummer einen Bereich von Beispielen an, die zu liefern sind.


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

[**IWMSyncReader-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[**Lesen von ASF-Dateien**](reading-asf-files.md)
</dt> <dt>

[**Synchrones Reader-Objekt**](synchronous-reader-object.md)
</dt> </dl>

 

 




