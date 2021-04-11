---
description: Erstellen von streambeispielen aus einem vorhandenen ASF-Datenobjekt
ms.assetid: eb27f122-d958-495d-98ea-8befd105a9a8
title: Erstellen von streambeispielen aus einem vorhandenen ASF-Datenobjekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee612c9352e3295d6b4957922e385de40a9a1fa3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127884"
---
# <a name="generating-stream-samples-from-an-existing-asf-data-object"></a>Erstellen von streambeispielen aus einem vorhandenen ASF-Datenobjekt

Das ASF- *Splitter* Objekt ist eine wmcontainer-Ebenenkomponente, die das ASF-Datenobjekt einer ASF-Datei (Advanced Systems Format) analysiert.

Vor dem übergeben von Datenpaketen an den Splitter muss die Anwendung Streams für den Splitter initialisieren, konfigurieren und auswählen, damit Sie für den Prozess vorbereitet werden kann. Weitere Informationen finden Sie unter [Erstellen des ASF-Splitter Objekts](creating-the-asf-splitter-object.md) und [Konfigurieren des ASF-Splitter Objekts](configuring-the-asf-splitter-object.md).

Die für das Ausführen des ASF-Datenobjekts erforderlichen Methoden sind:

-   [**Imfasfsplitter::P arenddata**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-parsedata) , der den Analyseprozess startet, indem der Puffer mit den Datenpaketen an den Splitter gepusht wird.
-   [**Imfasfsplitter:: getnextsample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getnextsample) , das streambeispiele sammelt, die aus dem an Splitter über gebenden Puffer generiert wurden.

## <a name="finding-the-data-offset"></a>Suchen des Daten Offsets

Vor dem Starten des Prozesses muss die Anwendung das Datenobjekt innerhalb der ASF-Datei finden. Es gibt zwei Möglichkeiten, den Offset des Datenobjekts vom Anfang der Datei zu erhalten:

-   Bevor Sie das ContentInfo-Objekt initialisiert haben, können Sie die [**imfasfcontentinfo:: gethadersize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getheadersize) -Methode aufrufen. Diese Methode erfordert einen Puffer, der die ersten 30 Bytes des ASF-Headers enthält. Sie gibt die Größe des gesamten Headers zurück, der den Offset zum ersten Datenpaket angibt. Dieser Wert enthält auch die Datenobjekt-Header Größe von 50 Bytes.
-   Nachdem Sie das ContentInfo-Objekt initialisiert haben, können Sie den Präsentations Deskriptor abrufen, indem Sie [**imfasfcontentinfo:: generatepresentationdescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor)aufrufen und dann den Präsentations Deskriptor für das MF PD-Attribut für den [**ASF- \_ \_ \_ Daten \_ Start \_ Offset**](mf-pd-asf-data-start-offset-attribute.md) Abfragen. Der Wert dieses Attributs ist die Header Größe.
    > [!Note]  
    > Das MF PD-Attribut für die [**\_ ASF- \_ \_ Daten \_ Länge**](mf-pd-asf-data-length-attribute.md) im Präsentations Deskriptor gibt die Länge des ASF-Datenobjekts an.

     

In beiden Fällen ist der zurückgegebene Wert die Größe des Header Objekts zuzüglich der Größe des Header Abschnitts des Datenobjekts. Daher ist der resultierende Wert der Offset bis zum Anfang der Datenpakete im ASF-Datenobjekt. Wenn Sie mit dem Senden von Daten an den Splitter beginnen, müssen die Daten an diesem Offset ab dem Anfang der ASF-Datei beginnen.

Der Offset Wert wird als Parameter an die **Analysedaten** übergeben, die den Analyseprozess startet.

Das Datenobjekt wird in Datenpakete aufgeteilt. Jedes Datenpaket enthält einen datenpaketheader, der Informationen zur Paketverarbeitung und die Nutzlastdaten bereitstellt – die eigentlichen digitalen Mediendaten. In einem Such Szenario möchte die Anwendung möglicherweise, dass der Splitter mit der Analyse bei einem bestimmten Datenpaket beginnt. Zu diesem Zweck können Sie den-ASF-Indexer zum Abrufen des Offsets verwenden. Der Indexer gibt einen Offset-Wert zurück, der an der Paket Grenze beginnt. Wenn Sie nicht den Indexer verwenden, stellen Sie sicher, dass der Offset am Anfang des Datenpaket Headers beginnt. Wenn ein ungültiger Offset an den Splitter übergeben wird, z. b. wenn der Wert nicht auf die Paket Grenze zeigt, werden die Parameter " **Parser Header** " und " **getnextsample** " erfolgreich ausgeführt, aber " **getnextsample** " ruft keine Stichproben ab, und **null** wird im *psample* -Parameter empfangen.

Wenn der Splitter zum Analysieren in umgekehrter Richtung konfiguriert ist, beginnt der Splitter immer am Ende des Medien Puffers, der an " **bisedata**" weitergeleitet wird. Daher wird für die umgekehrte Analyse im Aufrufen von "- **Daten**" der Offset im *cblength* -Parameter übergeben, der die Länge der Daten angibt und *cbbufferoffset* auf 0 (null) festlegt.

## <a name="generating-samples-for-asf-data-packets"></a>Erstellen von Beispielen für ASF-Datenpakete

Eine Anwendung startet den Prozess, indem Sie die Datenpakete an den Splitter übergibt. Die Eingabe für den Splitter ist eine Reihe von Medien Puffern, die die gesamten-oder-Fragmente des Datenobjekts enthalten. Die Ausgabe des Splitters ist eine Reihe von Medien Beispielen, die die Paketdaten enthalten.

Wenn Sie Eingabedaten an den Splitter übergeben möchten, erstellen Sie einen Medien Puffer, und füllen Sie ihn mit Daten aus dem Datenobjekt Abschnitt der ASF-Datei. (Weitere Informationen zu Medien Puffern finden Sie unter [Medien Puffer](media-buffers.md).) Übergeben Sie dann den Medien Puffer an die [**imfasfsplitter::P areldata**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-parsedata) -Methode. Sie können auch Folgendes angeben:

-   Der Offset im Puffer, an dem der Splitter mit der Verarbeitung beginnen soll. Wenn der Offset 0 (null) ist, beginnt die Verarbeitung am Anfang des Puffers. Weitere Informationen zum Festlegen des Daten Offsets finden Sie im Abschnitt "Suchen des Daten Offsets" in diesem Thema.
-   Die zu testenden Datenmenge. Wenn dieser Wert 0 (null) ist, wird der Splitter so lange analysiert, bis das Ende des Puffers erreicht wird, wie durch die [**imfmediabuffer:: getcurrentlength**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-getcurrentlength) -Methode angegeben.

Der Splitter generiert Medien Beispiele durch Verweisen auf die Daten in den Medien Puffern. Der Client kann die Ausgabe Beispiele abrufen, indem er [**imfasfsplitter:: getnextsample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getnextsample) in einer Schleife aufruft, bis keine weiteren Daten zum Analysieren vorhanden sind. Wenn **getnextsample** das "ASF \_ Statusflags \_ unvollständig"-Flag im *pdwstatusflags* -Parameter zurückgibt, bedeutet dies, dass weitere abzurufende Beispiele vorhanden sind, und die Anwendung kann **getnextsample** erneut aufrufen. Anderenfalls können Sie " **Parser Data** " zum Übergeben von mehr Daten an den Splitter angleichen. Für die generierten Beispiele legt der Splitter die folgenden Informationen fest:

-   Der Splitter legt einen Zeitstempel für alle generierten Beispiele fest. Die Beispiel Zeit stellt die Präsentationszeit dar und umfasst nicht die Vorabversion. Die Anwendung kann [**imfsample:: getsampletime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampletime) aufrufen, um die Präsentationszeit in 100-Nanosecond-Einheiten zu erhalten.
-   Wenn während der Beispiel Generierung eine Unterbrechung auftritt, legt der Splitter das Attribut " [**\_ discontinuity" der MF SampleExtension**](mfsampleextension-discontinuity-attribute.md) -Eigenschaft auf das erste Beispiel nach der Diskontinuität fest. Diskontinuitäten werden normalerweise durch gelöschte Pakete in einer Netzwerkverbindung, beschädigte Datei Daten oder den Splitter des Splitters von einem Quelldaten Strom zu einem anderen verursacht.
-   Bei einem Video prüft der Splitter, ob das Beispiel einen Keyframe enthält. Wenn dies der Fall ist, legt der Splitter das [**MF SampleExtension- \_ cleanpointattribut**](mfsampleextension-cleanpoint-attribute.md) für das Beispiel fest.

Wenn der Splitter Datenpakete verarbeitet, die von einem Medienserver empfangen werden, ist es möglich, dass die Paketlänge variabel ist. In diesem Fall muss der Client für jedes Paket " **Parser Data** " und für jeden Puffer, der an den Splitter gesendet wird, das Attribut " [**mfasfsplitter \_ Packet \_ Boundary**](mfasfsplitter-packet-boundary-attribute.md) " festlegen. Dieses Attribut gibt dem Splitter an, ob der Medien Puffer den Anfang eines ASF-Pakets enthält. Legen Sie das-Attribut auf **true** fest, wenn der Puffer den Anfang eines neuen Pakets enthält. Wenn der Puffer eine Fortsetzung des vorherigen Pakets enthält, legen Sie das-Attribut auf " **false**" fest. Die Puffer können nicht mehrere Pakete umfassen.

Bevor neue Medien Puffer an den Splitter übergeben werden, muss die Anwendung [**imfasfsplitter:: Flush**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-flush)aufgerufen werden. Diese Methode setzt den Splitter zurück und löscht jeden partiellen Frame, der auf den Abschluss wartet. Dies ist in einem Such Szenario nützlich, bei dem sich der Offset an einem anderen Speicherort befindet.

### <a name="example"></a>Beispiel

Im folgenden Codebeispiel wird gezeigt, wie Datenpakete analysiert werden. Dieses Beispiel analysiert vom Anfang des Datenobjekts bis zum Ende des Streams und zeigt Informationen über die Beispiele an, die Keyframes enthalten. Ein umfassendes Beispiel, in dem dieser Code verwendet wird, finden Sie unter [Tutorial: Lesen einer ASF-Datei](tutorial--reading-an-asf-file.md).


```C++
// Parse the video stream and display information about the video samples.
//
// The current read position of the byte stream must be at the start of the ASF
// Data Object.

HRESULT DisplayKeyFrames(IMFByteStream *pStream, IMFASFSplitter *pSplitter)
{
    const DWORD cbReadSize = 2048;  // Read size (arbitrary value)

    IMFMediaBuffer *pBuffer = NULL;
    IMFSample *pSample = NULL;

    HRESULT hr = S_OK;
    while (SUCCEEDED(hr))
    {
        // The parser must get a newly allocated buffer each time.
        hr = MFCreateMemoryBuffer(cbReadSize, &pBuffer);
        if (FAILED(hr))
        {
            break;
        }

        // Read data into the buffer.
        hr = ReadFromByteStream(pStream, pBuffer, cbReadSize);
        if (FAILED(hr)) 
        {
            break; 
        }

        // Get the amound of data that was read.
        DWORD cbData;
        hr = pBuffer->GetCurrentLength(&cbData);
        if (FAILED(hr)) 
        { 
            break; 
        }

        if (cbData == 0)
        {
            break; // End of file.
        }

        // Send the data to the ASF splitter.
        hr = pSplitter->ParseData(pBuffer, 0, 0);
        SafeRelease(&pBuffer);
        if (FAILED(hr)) 
        { 
            break; 
        }

        // Pull samples from the splitter.
        DWORD parsingStatus = 0;
        do
        {
            WORD streamID;
            hr = pSplitter->GetNextSample(&parsingStatus, &streamID, &pSample);
            if (FAILED(hr)) 
            { 
                break; 
            }
            if (pSample == NULL)
            {
                // No samples yet. Parse more data.
                break;
            }
            if (IsRandomAccessPoint(pSample))
            {
                DisplayKeyFrame(pSample);
            }
            SafeRelease(&pSample);
            
        } while (parsingStatus & ASF_STATUSFLAGS_INCOMPLETE);
    }
    SafeRelease(&pSample);
    SafeRelease(&pBuffer);
    return hr;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ASF-Splitter](asf-splitter.md)
</dt> </dl>

 

 



