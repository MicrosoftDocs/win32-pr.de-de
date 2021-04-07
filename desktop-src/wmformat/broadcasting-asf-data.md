---
title: Übertragungen von ASF-Daten
description: Übertragungen von ASF-Daten
ms.assetid: 1b04f361-8147-4f6a-8c9d-d8eeed28550a
keywords:
- Windows Media-Format-SDK, Senden von ASF-Daten
- Advanced Systems Format (ASF), Broadcast von Daten
- ASF (Advanced Systems Format), Broadcasting Data
- Windows Media-Format-SDK, Senden von ASF-Daten
- Advanced Systems Format (ASF), Senden von Daten
- ASF (Advanced Systems Format), Senden von Daten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42339b4a3e60666c1ea0cb69a07dfdc836b19409
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/21/2020
ms.locfileid: "104038665"
---
# <a name="broadcasting-asf-data"></a>Übertragungen von ASF-Daten

In diesem Thema wird beschrieben, wie Sie mit dem HTTP-Protokoll ASF-Daten über ein Netzwerk senden. Zum Senden von Dateien über ein Netzwerk ist die Verwendung des Writer-Objekts erforderlich. Daher sollten Sie vor dem Lesen dieses Themas über ein allgemeines Verständnis dieses Objekts verfügen. Weitere Informationen finden Sie unter [Schreiben von ASF-Dateien](writing-asf-files.md).

Wenn Sie mit nicht komprimierten Daten beginnen, gehen Sie folgendermaßen vor:

1.  Erstellen Sie das Writer-Objekt, indem Sie die [**wmcreatewriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) -Funktion aufrufen. Diese Funktion gibt einen **iwmwriter** -Zeiger zurück.
    ```C++
    IWMWriter *pWriter;
    hr = WMCreateWriter(NULL, &pWriter);
    ```

    

2.  Erstellen Sie das netzwerksink-Objekt, indem Sie die [**wmcreateschreiternetworksink**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriternetworksink) -Funktion aufrufen, die einen **iwmschreiternetworksink** -Zeiger zurückgibt.
    ```C++
    IWMWriterNetworkSink *pNetSink;
    hr = WMCreateWriterNetworkSink(&pNetSink);
    ```

    

3.  Nennen Sie [**iwmschreiternetworksink:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-open) in der Netzwerk Senke, und geben Sie die Portnummer an, die geöffnet werden soll. Beispiel: 8080. Zum Abrufen der URL des Hosts können Sie optional [**iwmschreiternetworksink:: gethosturl**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-gethosturl) aufrufen. Clients greifen über diese URL auf den Inhalt zu. Sie können auch [**iwmschreiternetworksink:: setmaximumclients**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-setmaximumclients) aufrufen, um die Anzahl der Clients einzuschränken.
    ```C++
    DWORD dwPortNum = 8080;
    hr = pNetSink->Open( &dwPortNum)
    ```

    

4.  Fügen Sie die Netzwerk Senke an den Writer an, indem Sie [**iwmschreiteradvanced:: addsink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-addsink) für den Writer aufrufen, mit einem Zeiger auf die **iwmschreiternetworksink** -Schnittstelle der Netzwerk Senke.
    ```C++
    IWMWriterAdvanced *pWriterAdvanced;
    hr = pWriter->QueryInterface(IID_IWMWriterAdvanced, ( void** ) pWriterAdvanced );
    if (SUCCEEDED(hr))
    {
        pWriterAdvanced->AddSink(pNetSink);
    }
    ```

    

5.  Legen Sie das ASF-Profil fest, indem Sie die [**iwmwriter:: setprofile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) -Methode für das Writer-Objekt mit einem [**iwmprofile**](iwmprofile.md) -Zeiger aufrufen. Weitere Informationen zum Erstellen eines Profils finden Sie unter [Arbeiten mit Profilen](working-with-profiles.md).
6.  Optional können Sie Metadaten mithilfe der [**iwmheaderinfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) -Schnittstelle für den Writer angeben.
7.  Nennen Sie [**iwmwriter:: BeginWrite**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting) für den Writer.
    ```C++
    hr = pWriter->BeginWriting();
    ```

    

8.  Für jedes Beispiel wird die [**iwmwriter:: schreitesample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) -Methode aufgerufen. Geben Sie die Datenstrom Nummer, die Präsentationszeit, die Dauer der Stichprobe und einen Zeiger auf den Beispiel Puffer an. Die Methode " **Write tesample** " komprimiert die Beispiele.
9.  Wenn Sie den Vorgang abgeschlossen haben, nennen Sie [**iwmwriter:: endwriting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-endwriting) für den Writer.
    ```C++
    hr = pWriter->EndWriting();
    ```

    

10. Nennen Sie [**iwmschreiteradvanced:: removesink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-removesink) auf dem Writer, um das netzwerksink-Objekt zu trennen.
    ```C++
    hr = pWriterAdvanced->RemoveSink(pNetSink);
    ```

    

11. Nennen Sie [**iwmschreiternetworksink:: Close**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-close) in der Netzwerk Senke, um den Port freizugeben.
    ```C++
    hr = pNetSink->Close();
    ```

    

Eine weitere Möglichkeit zum Streamen von ASF-Inhalten über ein Netzwerk besteht darin, Sie aus einer vorhandenen ASF-Datei zu lesen. Das im SDK bereitgestellte wmvnetwrite-Beispiel veranschaulicht diese Vorgehensweise. Führen Sie zusätzlich zu den zuvor aufgeführten Schritten folgende Schritte aus:

1.  Erstellen Sie ein Reader-Objekt, und rufen Sie die **Open** -Methode mit dem Namen der Datei auf.
2.  Aufrufen von [**iwmreaderadvanced:: setmanualstreamselection**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setmanualstreamselection) für das Reader-Objekt mit dem Wert " **true**". Dadurch kann die Anwendung jeden Stream in der Datei lesen, einschließlich Streams mit gegenseitigem Ausschluss.
3.  Fragen Sie den Reader nach der [**iwmprofile**](iwmprofile.md) -Schnittstelle ab. Verwenden Sie diesen Zeiger, wenn Sie [**iwmwriter:: setprofile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) für das Writer-Objekt aufrufen (Schritt 5 in der vorherigen Prozedur).
4.  Für jeden Stream, der im Profil definiert ist, können Sie [**iwmprofile:: GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream) aufrufen, um die streamnummer abzurufen. Übergeben Sie diese streamnummer an die [**iwmreaderadvanced:: setreceivestreamsamples**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setreceivestreamsamples) -Methode des Readers. Diese Methode teilt dem Reader mit, komprimierte Beispiele zu liefern, anstatt Sie zu decodieren. Die Beispiele werden mithilfe der [**iwmreadercallbackadvanced:: onstreamsample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-onstreamsample) -Rückruf Methode der Anwendung an die Anwendung übermittelt.

    Sie müssen die Codec-Informationen für jeden Datenstrom abrufen, den Sie unkomprimiert gelesen haben, und ihn vor der Übertragung dem Header hinzufügen. Rufen Sie zum Abrufen der Codec-Informationen [**IWMHeaderInfo2:: getcodecinfocount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfocount) und [**IWMHeaderInfo2:: getcodecinfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfo) auf, um die Codecs aufzulisten, die der Datei im Reader zugeordnet sind. Wählen Sie die Codec-Informationen aus, die der Datenstrom Konfiguration entsprechen. Legen Sie dann die Codec-Informationen im Writer durch Aufrufen von [**IWMHeaderInfo3:: addcodecinfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addcodecinfo)fest, und übergeben Sie dabei die Informationen, die vom Reader abgerufen werden.

5.  Nachdem Sie das Profil für den Writer festgelegt haben, können Sie [**iwmwriter:: getinputcount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputcount) für den Writer aufrufen, um die Anzahl der Eingaben zu erhalten. Geben Sie für jede Eingabe den Wert " [**iwmwriter::**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops) " mit dem Wert **null** an. Dadurch wird dem Writer-Objekt angezeigt, dass die Anwendung komprimierte Beispiele bereitstellt, sodass der Writer keine Codecs zum Komprimieren der Daten verwenden muss. Stellen Sie sicher, dass Sie vor dem Aufrufen von **beginwriting**"" vor **dem Aufruf von** "
6.  Kopieren Sie optional die Metadatenattribute vom Reader in den Writer.
7.  Da die Beispiele des Readers bereits komprimiert sind, verwenden Sie die Methode [**iwmschreiteradvanced:: schreitestreamsample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-writestreamsample) , um die Beispiele anstelle der **beschreitesample** -Methode zu schreiben. Die " **Write-streamsample** "-Methode umgeht die üblichen Komprimierungs Prozeduren des Writer-Objekts.
8.  Wenn der Reader das Ende der Datei erreicht, sendet er eine WMT- \_ Benachrichtigungs Benachrichtigung an die Anwendung.

Außerdem sollte die Anwendung die Uhr auf dem Reader-Objekt steuern, damit der Reader so schnell wie möglich Daten aus der Datei abruft. Rufen Sie hierzu die [**iwmreaderadvanced:: setuserprovidedclock**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setuserprovidedclock) -Methode für den Reader mit dem Wert " **true**" auf. Nachdem der Reader die WMT \_ Started-Benachrichtigung gesendet hat, rufen Sie [**iwmreaderadvanced::D elivertime**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-delivertime) auf, und geben Sie das Zeitintervall an, das der Reader übermitteln soll. Nachdem der Reader das Zeitintervall gelesen hat, ruft er die [**iwmreadercallbackadvanced:: OnTime**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-ontime) -Rückruf Methode der Anwendung auf. Die Anwendung sollte **delivertime** erneut abrufen, um das nächste Zeitintervall zu lesen. So können Sie z. b. in Intervallen von einer Sekunde aus der Datei lesen:


```C++
// Initial call to DeliverTime.
QWORD m_qwTime = 10000000; // 1 second.
hr = m_pReaderAdvanced->DeliverTime(m_qwTime);

// In the callback:
HRESULT CNetWrite::OnTime(QWORD cnsCurrentTime, void *pvContext)
{
    HRESULT hr = S_OK;
    // Continue calling DeliverTime until the end of the file.
    if(!m_bEOF)
    {
        m_qwTime += 10000000; // 1 second.
        hr = m_pReaderAdvanced->DeliverTime(m_qwTime);
    }
    return S_OK;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Senden von ASF-Daten über ein Netzwerk**](sending-asf-data-over-a-network.md)
</dt> <dt>

[**Arbeiten mit Writer-senken**](working-with-writer-sinks.md)
</dt> </dl>

 

 




