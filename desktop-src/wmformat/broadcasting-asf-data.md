---
title: Übertragungen von ASF-Daten
description: Übertragungen von ASF-Daten
ms.assetid: 1b04f361-8147-4f6a-8c9d-d8eeed28550a
keywords:
- Windows Medienformat-SDK, Übertragen von ASF-Daten
- Advanced Systems Format (ASF), Übertragen von Daten
- ASF (Advanced Systems Format), Broadcasting data
- Windows Medienformat-SDK, Senden von ASF-Daten
- Advanced Systems Format (ASF), Senden von Daten
- ASF (Advanced Systems Format), Senden von Daten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a44fc9ea0515822c765b0cb3af457254341a64f08e64d566aa9e226a48758e7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118434464"
---
# <a name="broadcasting-asf-data"></a>Übertragungen von ASF-Daten

In diesem Thema wird beschrieben, wie ASF-Daten über ein Netzwerk mithilfe des HTTP-Protokolls gesendet werden. Das Senden von Dateien über ein Netzwerk erfordert die Verwendung des Writer-Objekts. Daher sollten Sie dieses Objekt vor dem Lesen dieses Themas allgemein verstehen. Weitere Informationen finden Sie unter [Schreiben von ASF-Dateien.](writing-asf-files.md)

Wenn Sie mit unkomprimierten Daten beginnen, gehen Sie wie folgt vor:

1.  Erstellen Sie das Writer-Objekt, indem Sie die [**WMCreateWriter-Funktion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) aufrufen. Diese Funktion gibt einen **IWMWriter-Zeiger** zurück.
    ```C++
    IWMWriter *pWriter;
    hr = WMCreateWriter(NULL, &pWriter);
    ```

    

2.  Erstellen Sie das Netzwerksenkenobjekt, indem Sie die [**WMCreateWriterNetworkSink-Funktion**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-wmcreatewriternetworksink) aufrufen, die einen **IWMWriterNetworkSink-Zeiger** zurückgibt.
    ```C++
    IWMWriterNetworkSink *pNetSink;
    hr = WMCreateWriterNetworkSink(&pNetSink);
    ```

    

3.  Rufen [**Sie IWMWriterNetworkSink::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-open) in der Netzwerksenke auf, und geben Sie die zu öffnende Portnummer an. Beispiel: 8080. Rufen Sie optional [**IWMWriterNetworkSink::GetHostURL**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-gethosturl) auf, um die URL des Hosts zu erhalten. Clients greifen über diese URL auf den Inhalt zu. Sie können auch [**IWMWriterNetworkSink::SetMaximumClients**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-setmaximumclients) aufrufen, um die Anzahl der Clients einzuschränken.
    ```C++
    DWORD dwPortNum = 8080;
    hr = pNetSink->Open( &dwPortNum)
    ```

    

4.  Fügen Sie die Netzwerksenke an den Writer an, indem Sie [**IWMWriterAdvanced::AddSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-addsink) für den Writer mit einem Zeiger auf die **IWMWriterNetworkSink-Schnittstelle** der Netzwerksenke aufrufen.
    ```C++
    IWMWriterAdvanced *pWriterAdvanced;
    hr = pWriter->QueryInterface(IID_IWMWriterAdvanced, ( void** ) pWriterAdvanced );
    if (SUCCEEDED(hr))
    {
        pWriterAdvanced->AddSink(pNetSink);
    }
    ```

    

5.  Legen Sie das ASF-Profil fest, indem Sie die [**IWMWriter::SetProfile-Methode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) für das Writer-Objekt mit einem [**IWMProfile-Zeiger**](iwmprofile.md) aufrufen. Informationen zum Erstellen eines Profils finden Sie unter [Arbeiten mit Profilen.](working-with-profiles.md)
6.  Geben Sie optional Metadaten mithilfe der [**IWMHeaderInfo-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) für den Writer an.
7.  Rufen [**Sie IWMWriter::BeginWriting für**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-beginwriting) den Writer auf.
    ```C++
    hr = pWriter->BeginWriting();
    ```

    

8.  Rufen Sie für jedes Beispiel die [**IWMWriter::WriteSample-Methode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample) auf. Geben Sie die Streamnummer, die Präsentationszeit, die Dauer des Beispiels und einen Zeiger auf den Beispielpuffer an. Die **WriteSample-Methode** komprimiert die Beispiele.
9.  Wenn Sie fertig sind, rufen Sie [**IWMWriter::EndWriting für**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-endwriting) den Writer auf.
    ```C++
    hr = pWriter->EndWriting();
    ```

    

10. Rufen [**Sie IWMWriterAdvanced::RemoveSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-removesink) für den Writer auf, um das Netzwerksenkenobjekt zu trennen.
    ```C++
    hr = pWriterAdvanced->RemoveSink(pNetSink);
    ```

    

11. Rufen [**Sie IWMWriterNetworkSink::Close**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriternetworksink-close) in der Netzwerksenke auf, um den Port frei zu geben.
    ```C++
    hr = pNetSink->Close();
    ```

    

Eine weitere Möglichkeit zum Streamen von ASF-Inhalten über ein Netzwerk ist das Lesen aus einer vorhandenen ASF-Datei. Das im SDK bereitgestellte WMVNetWrite-Beispiel veranschaulicht diesen Ansatz. Führen Sie zusätzlich zu den oben aufgeführten Schritten die folgenden Schritte aus:

1.  Erstellen Sie ein Readerobjekt, und rufen Sie die **Open-Methode** mit dem Namen der Datei auf.
2.  Rufen [**Sie IWMReaderAdvanced::SetManualStreamSelection**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setmanualstreamselection) für das Readerobjekt mit dem Wert **TRUE auf.** Dadurch kann die Anwendung jeden Datenstrom in der Datei lesen, einschließlich Streams mit gegenseitigem Ausschluss.
3.  Fragen Sie den Reader nach der [**IWMProfile-Schnittstelle**](iwmprofile.md) ab. Verwenden Sie diesen Zeiger, wenn Sie [**IWMWriter::SetProfile für**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) das Writer-Objekt aufrufen (Schritt 5 in der vorherigen Prozedur).
4.  Rufen Sie für jeden im Profil definierten Stream [**IWMProfile::GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream) auf, um die Streamnummer zu erhalten. Übergeben Sie diese Streamnummer an die [**IWMReaderAdvanced::SetReceiveStreamSamples-Methode des Readers.**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setreceivestreamsamples) Diese Methode informiert den Leser, komprimierte Stichproben zu liefern, anstatt sie zu decodieren. Die Beispiele werden über die [**RÜCKRUFMReaderCallbackAdvanced::OnStreamSample-Rückrufmethode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-onstreamsample) der Anwendung an die Anwendung übermittelt.

    Sie müssen Codecinformationen für jeden Stream abrufen, den Sie unkomprimiert lesen, und sie dem Header vor der Übertragung hinzufügen. Um die Codecinformationen zu erhalten, rufen Sie [**IWMHeaderInfo2::GetCodecInfoCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfocount) und [**IWMHeaderInfo2::GetCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo2-getcodecinfo) auf, um die Codecs zu aufzählen, die der Datei im Reader zugeordnet sind. Wählen Sie die Codecinformationen aus, die der Streamkonfiguration entspricht. Legen Sie dann die Codecinformationen im Writer fest, indem [**Sie IWMHeaderInfo3::AddCodecInfo**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addcodecinfo)aufrufen und die vom Reader erhaltenen Informationen übergeben.

5.  Nachdem Sie das Profil für den Writer festgelegt haben, rufen Sie [**IWMWriter::GetInputCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputcount) für den Writer auf, um die Anzahl der Eingaben zu erhalten. Rufen Sie für jede Eingabe [**IWMWriter::SetInputProps mit**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops) dem Wert **NULL auf.** Dies gibt dem Writerobjekt an, dass die Anwendung komprimierte Stichproben liefert, sodass der Writer keine Codecs verwenden muss, um die Daten zu komprimieren. Stellen Sie sicher, dass **Sie SetInputProps aufrufen,** bevor **Sie BeginWriting aufrufen.**
6.  Kopieren Sie optional die Metadatenattribute aus dem Reader in den Writer.
7.  Da die Beispiele aus dem Reader bereits komprimiert sind, verwenden Sie anstelle der **WriteSample-Methode** die [**IWMWriterAdvanced::WriteStreamSample-Methode,**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-writestreamsample) um die Beispiele zu schreiben. Die **WriteStreamSample-Methode** umgeht die üblichen Komprimierungsvorgänge des Writerobjekts.
8.  Wenn der Reader das Ende der Datei erreicht, sendet er eine WMT \_ EOF-Benachrichtigung an die Anwendung.

Darüber hinaus sollte die Anwendung die Uhr für das Readerobjekt verwenden, damit der Reader Daten so schnell wie möglich aus der Datei pullt. Rufen Sie hierzu die [**IWMReaderAdvanced::SetUserProvidedClock-Methode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setuserprovidedclock) auf dem Reader mit dem Wert **TRUE auf.** Nachdem der Reader die WMT STARTED-Benachrichtigung sendet, rufen Sie \_ [**IWMReaderAdvanced::D eliverTime**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-delivertime) auf, und geben Sie das Zeitintervall an, das der Reader liefern soll. Nachdem der Reader dieses Zeitintervall gelesen hat, ruft er die [**IWMReaderCallbackAdvanced::OnTime-Rückrufmethode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallbackadvanced-ontime) der Anwendung auf. Die Anwendung sollte **DeliverTime erneut aufrufen,** um das nächste Zeitintervall zu lesen. Um beispielsweise in Intervallen von einer Sekunde aus der Datei zu lesen:


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

[**Arbeiten mit Writer-Senken**](working-with-writer-sinks.md)
</dt> </dl>

 

 




