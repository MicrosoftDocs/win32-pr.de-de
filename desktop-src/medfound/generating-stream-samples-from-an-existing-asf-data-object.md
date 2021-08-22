---
description: Generieren von Streambeispielen aus einem vorhandenen ASF-Datenobjekt
ms.assetid: eb27f122-d958-495d-98ea-8befd105a9a8
title: Generieren von Streambeispielen aus einem vorhandenen ASF-Datenobjekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97fb99440c3fc4721851f183b3bfc7aefafd3f652d0436b29e9cea1209ba59b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974449"
---
# <a name="generating-stream-samples-from-an-existing-asf-data-object"></a>Generieren von Streambeispielen aus einem vorhandenen ASF-Datenobjekt

Das *ASF-Splitterobjekt* ist eine WMContainer-Ebenenkomponente, die das ASF-Datenobjekt einer ASF-Datei (Advanced Systems Format) analysiert.

Vor der Übergabe von Datenpaketen an den Splitter muss die Anwendung Streams auf dem Splitter initialisieren, konfigurieren und auswählen, um sie für den Analyseprozess vorzubereiten. Weitere Informationen finden Sie unter [Erstellen des ASF-Splitterobjekts](creating-the-asf-splitter-object.md) und [Konfigurieren des ASF-Splitterobjekts.](configuring-the-asf-splitter-object.md)

Für die Analyse des ASF-Datenobjekts sind folgende Methoden erforderlich:

-   [**IMFASFSplitter::P arseData,**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-parsedata) die den Analyseprozess startet, indem der Puffer mit Datenpaketen per Push an den Splitter übertragen wird.
-   [**IMFASFSplitter::GetNextSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getnextsample) zum Sammeln von Streambeispielen, die aus dem an den Splitter übergebenen Puffer generiert wurden.

## <a name="finding-the-data-offset"></a>Suchen des Datenoffsets

Vor dem Starten des Analyseprozesses muss die Anwendung das Datenobjekt in der ASF-Datei suchen. Es gibt zwei Möglichkeiten, den Offset des Datenobjekts vom Anfang der Datei abzurufen:

-   Bevor Sie das ContentInfo-Objekt initialisiert haben, können Sie die [**IMFASFContentInfo::GetHeaderSize-Methode**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getheadersize) aufrufen. Diese Methode erfordert einen Puffer, der die ersten 30 Bytes des ASF-Headers enthält. Sie gibt die Größe des gesamten Headers zurück, der den Offset zum ersten Datenpaket angibt. Dieser Wert enthält auch die Datenobjektheadergröße von 50 Bytes.
-   Nachdem Sie das ContentInfo-Objekt initialisiert haben, können Sie den Präsentationsdeskriptor abrufen, indem Sie [**IMFASFContentInfo::GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor)aufrufen und dann den Präsentationsdeskriptor für das [**MF PD \_ \_ ASF DATA START \_ \_ \_ OFFSET-Attribut**](mf-pd-asf-data-start-offset-attribute.md) abfragen. Der Wert dieses Attributs ist die Headergröße.
    > [!Note]  
    > Das [**MF \_ PD \_ ASF DATA \_ \_ LENGTH-Attribut**](mf-pd-asf-data-length-attribute.md) im Präsentationsdeskriptor gibt die Länge des ASF-Datenobjekts an.

     

In beiden Fällen entspricht der zurückgegebene Wert der Größe des Headerobjekts plus der Größe des Headerabschnitts des Datenobjekts. Daher ist der resultierende Wert der Offset zum Anfang der Datenpakete im ASF-Datenobjekt. Wenn Sie mit dem Senden von Daten an den Splitter beginnen, müssen die Daten bei diesem Offset ab dem Anfang der ASF-Datei beginnen.

Der Offsetwert wird als Parameter an **ParseData** übergeben, der den Analyseprozess startet.

Das Datenobjekt ist in Datenpakete unterteilt. Jedes Datenpaket enthält einen Datenpaketheader, der Paketparsinginformationen und die Nutzlastdaten – die eigentlichen digitalen Mediendaten – bereitstellt. In einem Suchszenario möchte die Anwendung möglicherweise, dass der Splitter mit der Analyse eines bestimmten Datenpakets beginnt. Hierzu können Sie den ASF-Indexer verwenden, um den Offset abzurufen. Der Indexer gibt einen Offsetwert zurück, der an der Paketgrenze beginnt. Wenn Sie den Indexer nicht verwenden, stellen Sie sicher, dass der Offset am Anfang des Datenpaketheaders beginnt. Wenn ein ungültiger Offset an den Splitter übergeben wird, z. B. der Wert nicht auf die Paketgrenze verweist, sind **ParseHeader-** und **GetNextSample-Aufrufe** erfolgreich, aber **GetNextSample** ruft keine Stichproben ab, und **NULL** wird im *pSample-Parameter* empfangen.

Wenn der Splitter für die Analyse in umgekehrter Richtung konfiguriert ist, beginnt der Splitter immer mit der Analyse am Ende des Medienpuffers, der an **ParseData** übergeben wird. Übergeben Sie daher für die umgekehrte Analyse im Aufruf von **ParseData** den Offset im *cbLength-Parameter,* der die Länge der Daten angibt, und legen *Sie cbBufferOffset* auf 0 (null) fest.

## <a name="generating-samples-for-asf-data-packets"></a>Generieren von Beispielen für ASF-Datenpakete

Eine Anwendung startet den Analyseprozess, indem die Datenpakete an den Splitter übergeben werden. Die Eingabe für den Splitter ist eine Reihe von Medienpuffern, die das gesamte Datenobjekt oder Fragmente des Datenobjekts enthalten. Die Ausgabe des Splitters ist eine Reihe von Medienbeispielen, die die Paketdaten enthalten.

Um Eingabedaten an den Splitter zu übergeben, erstellen Sie einen Medienpuffer, und füllen Sie ihn mit Daten aus dem Abschnitt Datenobjekt der ASF-Datei aus. (Weitere Informationen zu Medienpuffern finden Sie unter [Medienpuffer](media-buffers.md).) Übergeben Sie dann den Medienpuffer an die [**IMFASFSplitter::P arseData-Methode.**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-parsedata) Sie können auch Folgendes angeben:

-   Der Offset in den Puffer, in dem der Splitter mit der Analyse beginnen soll. Wenn der Offset 0 (null) ist, beginnt die Analyse am Anfang des Puffers. Informationen zum Festlegen des Datenoffsets finden Sie im Abschnitt "Suchen des Datenoffsets" in diesem Thema.
-   Die Zu analysierende Datenmenge. Wenn dieser Wert 0 (null) ist, wird der Splitter analysiert, bis er das Ende des Puffers erreicht, wie von [**derENMEDIABuffer::GetCurrentLength-Methode**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediabuffer-getcurrentlength) angegeben.

Der Splitter generiert Medienbeispiele, indem er auf die Daten in den Medienpuffern verweist. Der Client kann die Ausgabebeispiele abrufen, indem [**er IMFASFSplitter::GetNextSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-getnextsample) in einer Schleife aufruft, bis keine weiteren Zu analysierenden Daten vorhanden sind. Wenn **GetNextSample** das \_ ASF STATUSFLAGS \_ INCOMPLETE-Flag im *pdwStatusFlags-Parameter* zurückgibt, bedeutet dies, dass weitere Beispiele abgerufen werden müssen, und die Anwendung kann **GetNextSample** erneut aufrufen. Rufen Sie andernfalls **ParseData** auf, um weitere Daten an den Splitter zu übergeben. Für die generierten Beispiele legt der Splitter die folgenden Informationen fest:

-   Der Splitter legt einen Zeitstempel für alle generierten Stichproben fest. Die Beispielzeit stellt die Präsentationszeit dar und enthält nicht die Vorrollzeit. Die Anwendung kann [**DIE PRÄSENTATIONszeit**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-getsampletime) in Einheiten von 100 Nanosekunden abrufen.
-   Wenn während der Stichprobengenerierung ein Break auftritt, legt der Splitter das [**MFSampleExtension-Discontinuity-Attribut \_**](mfsampleextension-discontinuity-attribute.md) für das erste Beispiel nach der Diskontinuität fest. Diskontinuitäten werden in der Regel durch verworfene Pakete in einer Netzwerkverbindung, beschädigte Dateidaten oder den Splitterwechsel von einem Quelldatenstrom zu einem anderen verursacht.
-   Für Videos überprüft der Splitter, ob das Beispiel einen Keyframe enthält. In diesem Falle legt der Splitter das [**\_ CLEANPoint-Attribut MFSampleExtension**](mfsampleextension-cleanpoint-attribute.md) für das Beispiel fest.

Wenn der Splitter Datenpakete verarbeitet, die von einem Medienserver empfangen werden, ist es möglich, dass die Paketlänge variabel ist. In diesem Fall muss der Client **ParseData** für jedes Paket aufrufen und das [**MFASFSPLITTER \_ PACKET \_ BOUNDARY-Attribut**](mfasfsplitter-packet-boundary-attribute.md) für jeden Puffer festlegen, der an den Splitter gesendet wird. Dieses Attribut gibt dem Splitter an, ob der Medienpuffer den Anfang eines ASF-Pakets enthält. Legen Sie das Attribut auf **TRUE** fest, wenn der Puffer den Anfang eines neuen Pakets enthält. Wenn der Puffer eine Fortsetzung des vorherigen Pakets enthält, legen Sie das -Attribut auf **FALSE** fest. Die Puffer können sich nicht über mehrere Pakete erstrecken.

Bevor neue Medienpuffer an den Splitter übergeben werden, muss die Anwendung [**IMFASFSplitter::Flush**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfsplitter-flush)aufrufen. Diese Methode setzt den Splitter zurück und löscht alle Teilrahmen, die auf den Abschluss warten. Dies ist nützlich in einem Suchszenario, in dem sich der Offset an einer anderen Position befindet.

### <a name="example"></a>Beispiel

Das folgende Codebeispiel zeigt, wie Datenpakete analysiert werden. Dieses Beispiel analysiert vom Anfang des Datenobjekts bis zum Ende des Streams und zeigt Informationen zu den Beispielen an, die Keyframes enthalten. Ein vollständiges Beispiel, das diesen Code verwendet, finden Sie unter [Tutorial: Lesen einer ASF-Datei.](tutorial--reading-an-asf-file.md)


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

 

 



