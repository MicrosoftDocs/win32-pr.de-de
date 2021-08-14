---
description: Generieren neuer ASF-Datenpakete
ms.assetid: 7afa9694-c965-40e2-8549-e32ff48def2a
title: Generieren neuer ASF-Datenpakete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9473037d656bd4fcc01b91a908103fcda3e364a36e8caaf42cfc0558381e5af8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118742074"
---
# <a name="generating-new-asf-data-packets"></a>Generieren neuer ASF-Datenpakete

Der *ASF-Multiplexer* ist eine WMContainer-Ebenenkomponente, die mit dem [ASF-Datenobjekt](asf-file-structure.md) funktioniert und einer Anwendung die Möglichkeit bietet, ASF-Datenpakete für einen Stream zu generieren, die den im ContentInfo-Objekt definierten Anforderungen entsprechen.

Der Multiplexer verfügt über eine Eingabe und eine Ausgabe. Es empfängt ein Streambeispiel, das digitale Mediendaten enthält, und erzeugt ein oder mehrere Datenpakete, die in einen ASF-Container geschrieben werden können.

In der folgenden Liste wird der Prozess zum Generieren von ASF-Datenpaketen zusammengefasst:

1.  Übergeben Sie Eingabedaten an den Multiplexer in [**IMFASFMultiplexer::P rocessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample).
2.  Sammeln Sie die Datenpakete, indem [**Sie IMFASFMultiplexer::GetNextPacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket) in einer Schleife aufrufen, bis alle vollständigen Pakete abgerufen wurden.
3.  Nachdem die Eingabedaten in vollständige Pakete konvertiert wurden, sind möglicherweise einige ausstehende Daten im Multiplexer vorhanden, die nicht von [**GetNextPacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket)abgerufen wurden. Rufen Sie [**IMFASFMultiplexer::Flush**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-flush) auf, um die ausstehenden Beispiele zu packen und sie vom Multiplexer zu sammeln, indem **Sie GetNextPacket** erneut aufrufen.
4.  Aktualisieren Sie die zugeordneten ASF-Headerobjekte, indem [**Sie IMFASFMultiplexer::End**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-end) aufrufen, um änderungen widerzuspiegeln, die vom Multiplexer während der Generierung von Datenpaketen vorgenommen wurden.

Das folgende Diagramm veranschaulicht die Generierung von Datenpaketen für eine ASF-Datei über den Multiplexer.

![Diagramm der Generierung von Datenpaketen für eine ASF-Datei](images/packet.gif)

## <a name="asf-data-packet-creation"></a>ASF-Datenpaketerstellung

Rufen Sie nach dem Erstellen und Initialisieren des Multiplexers wie unter [Erstellen des Multiplexer-Objekts](creating-the-multiplexer-object.md)beschrieben [**IMFASFMultiplexer::P rocessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample) auf, um Eingabedaten zur Verarbeitung in Datenpakete an den Multiplexer zu übergeben. Die angegebene Eingabe muss sich in einem Medienbeispiel [**(DIESSAMPLE-Schnittstelle)**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) mit einem oder mehreren Medienpuffern [**(DIESMEDIABUFFER-Schnittstelle)**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) mit den Daten für einen Stream enthalten. Bei der ASF-zu-ASF-Transcodierung kann das Eingabemedienbeispiel aus dem Splitter generiert werden, der paketisierte Streambeispiele erstellt. Weitere Informationen finden Sie unter [ASF-Splitter.](asf-splitter.md)

Stellen Sie vor dem Aufrufen von [**ProcessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample)sicher, dass der Zeitstempel des Eingabemedienbeispiels eine gültige Präsentationszeit ist. andernfalls schlägt **ProcessSample** fehl und gibt den MF \_ E NO SAMPLE \_ \_ \_ TIMESTAMP-Code zurück.

Der Multiplexer kann Eingaben als komprimierte oder unkomprimierte Medienbeispiele über [**ProcessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample)akzeptieren. Der Multiplexer weist diesen Stichproben Sendezeiten abhängig von der Bandbreitennutzung des Streams zu. Während dieses Vorgangs überprüft der Multiplexer die leaky-Bucketparameter (Bitrate und Pufferfensterauslastung) und kann Stichproben ablehnen, die diesen Werten nicht entsprechen. Das Beispiel für Eingabemedien kann die Bandbreitenüberprüfung aus einem der folgenden Gründe fehlschlagen:

-   Wenn das Eingabemedienbeispiel zu spät eingetroffen ist, weil die zuletzt zugewiesene Sendezeit größer ist als der Zeitstempel für dieses Medienbeispiel. [**ProcessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample) schlägt fehl und gibt den **MF E LATE \_ \_ \_ SAMPLE-Fehlercode** zurück.
-   Wenn der Zeitstempel im Eingabemedienbeispiel vor der zugewiesenen Sendezeit liegt (dies weist auf einen Pufferüberlauf hin). Der Multiplexer kann diese Situation ignorieren, wenn er so konfiguriert ist, dass er die Bitrate durch Festlegen des **MFASF \_ MULTIPLEXER \_ AUTOADJUST \_ BITRATE-Flags** während der Multiplexerinitialisierung anpasst. Weitere Informationen finden Sie unter "Multiplexer Initialization and Leaky Bucket Einstellungen" (Multiplexer-Initialisierung und Leaky Bucket Einstellungen) unter [Creating the Multiplexer Object (Erstellen des Multiplexer-Objekts).](creating-the-multiplexer-object.md) Wenn dieses Flag nicht festgelegt ist und für den Multiplexer ein Bandbreitenüberlauf auftritt, schlägt [**ProcessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample) fehl und gibt den **MF E BANDWIDTH \_ \_ \_ OVERRUN-Fehlercode** zurück.

Nachdem der Multiplexer die Sendezeit zugewiesen hat, wird das Eingabemedienbeispiel dem *Sendefenster* hinzugefügt – eine Liste der Eingabemedienbeispiele, sortiert nach Sendezeiten und bereit für die Verarbeitung in Datenpaketen. Während der Erstellung von Datenpaketen wird das Eingabemedienbeispiel analysiert, und relevante Daten werden als Nutzlast in ein Datenpaket geschrieben. Ein vollständiges Datenpaket kann Daten aus einem oder mehreren Eingabemedienbeispielen enthalten.

Wenn neue Eingabemedienbeispiele im Sendefenster eintreffen, werden sie einer Warteschlange hinzugefügt, bis genügend Medienbeispiele vorhanden sind, um ein vollständiges Paket zu bilden. Die Daten in Medienpuffern, die im Eingabemedienbeispiel enthalten sind, werden nicht in das generierte Datenpaket kopiert. Das Datenpaket enthält Verweise auf die Eingabemedienpuffer, bis das Eingabemedienbeispiel vollständig paketiert und das vollständige Paket vom Multiplexer erfasst wurde.

Wenn ein vollständiges Datenpaket verfügbar ist, kann es durch Aufrufen von [**IMFASFMultiplexer::GetNextPacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket)abgerufen werden. Wenn Sie [**ProcessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample) aufrufen, während vollständige Pakete zum Abrufen bereit sind, tritt ein Fehler auf, und der **MF E \_ \_ NOTACCEPTING-Fehlercode** wird zurückgegeben. Dies gibt an, dass der Multiplexer keine weiteren Eingaben akzeptieren kann und Sie **GetNextPacket** aufrufen müssen, um die wartenden Pakete abzurufen. Im Idealfall sollte auf jeden **ProcessSample-Aufruf** mindestens ein **GetNextPacket-Aufruf** folgen, um die vollständigen Datenpakete abzurufen. Es kann mehrere Eingabemedienbeispiele dauern, um ein vollständiges Datenpaket zu erstellen. Umgekehrt können daten in einem Eingabemedienbeispiel mehrere Pakete umfassen. Daher ergeben nicht alle Aufrufe von **ProcessSample** Ausgabemedienbeispiele.

Wenn das Eingabemedienbeispiel einen Keyframe enthält, der durch das [**MFSampleExtension \_ CleanPoint-Attribut**](mfsampleextension-cleanpoint-attribute.md) angegeben wird, kopiert der Multiplexer das Attribut in das Paket.

## <a name="getting-asf-data-packets"></a>Abrufen von ASF-Datenpaketen

Um die Ausgabemedienbeispiele für ein vollständiges Datenpaket zu erfassen, das vom Multiplexer generiert wird, rufen [**Sie IMFASFMultiplexer::GetNextPacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket) in einer Schleife auf, bis für das Paket keine Ausgabemedienbeispiele mehr vorhanden sind. Im Folgenden werden die Erfolgsfälle aufgeführt:

-   Wenn ein vollständiges Datenpaket verfügbar ist, [**empfängt GetNextPacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket) das **FLAG ASF \_ STATUS \_ FLAGS \_ INCOMPLETE** im *pdwStatusFlags-Parameter.* Der *ppIPacket-Parameter* empfängt einen Zeiger auf das erste Datenpaket. Sie müssen diese Methode aufrufen, solange sie dieses Flag empfängt. Bei jeder Iteration zeigt *ppIPacket* auf das nächste Paket in der Warteschlange.
-   Wenn nur ein Datenpaket vorhanden ist, zeigt *ppIPacket* darauf, und das **FLAG ASF \_ STATUS \_ FLAGS \_ INCOMPLETE** wird in *pdwStatusFlags* nicht empfangen.
-   [**GetNextPacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket) kann ohne Datenpakete erfolgreich ausgeführt werden, wenn der Multiplexer noch datenpakete packt und hinzufügt. In diesem Fall zeigt *ppIPacket* auf **NULL.** Um fortzufahren, müssen Sie dem Multiplexer weitere Eingabemedienbeispiele bereitstellen, indem [**Sie ProcessSample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample)aufrufen.

Der folgende Beispielcode zeigt eine Funktion, die Datenpakete mit dem Multiplexer generiert. Der generierte Datenpaketinhalt wird in den Vom Aufrufer zugeordneten Daten bytestream geschrieben.


```C++
//-------------------------------------------------------------------
// GenerateASFDataPackets
// 
// Gets data packets from the mux. This function is called after 
// calling IMFASFMultiplexer::ProcessSample. 
//-------------------------------------------------------------------

HRESULT GenerateASFDataPackets( 
    IMFASFMultiplexer *pMux, 
    IMFByteStream *pDataStream
    )
{
    HRESULT hr = S_OK;

    IMFSample *pOutputSample = NULL;
    IMFMediaBuffer *pDataPacketBuffer = NULL;

    DWORD dwMuxStatus = ASF_STATUSFLAGS_INCOMPLETE;

    while (dwMuxStatus & ASF_STATUSFLAGS_INCOMPLETE)
    {
        hr = pMux->GetNextPacket(&dwMuxStatus, &pOutputSample);

        if (FAILED(hr))
        {
            break;
        }

        if (pOutputSample)
        {
            //Convert to contiguous buffer
            hr = pOutputSample->ConvertToContiguousBuffer(&pDataPacketBuffer);
            
            if (FAILED(hr))
            {
                break;
            }

            //Write buffer to byte stream
            hr = WriteBufferToByteStream(pDataStream, pDataPacketBuffer, NULL);

            if (FAILED(hr))
            {
                break;
            }
        }

        SafeRelease(&pDataPacketBuffer);
        SafeRelease(&pOutputSample);
    }

    SafeRelease(&pOutputSample);
    SafeRelease(&pDataPacketBuffer);
    return hr;
}
```



Die `WriteBufferToByteStream` Funktion wird im Thema [**ÜBERBYTESTREAM::Write**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-write)gezeigt.

Eine vollständige Anwendung, die dieses Codebeispiel verwendet, finden Sie unter [Tutorial: Kopieren von ASF-Streams aus einer Datei in eine andere](tutorial--copying-asf-streams-from-one-file-to-another.md).

## <a name="post-packet-generation-calls"></a>Post-Packet-Generation-Aufrufe

Um sicherzustellen, dass im Multiplexer keine vollständigen Datenpakete warten, rufen Sie [**IMFASFMultiplexer::Flush**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-flush)auf. Dadurch wird der Multiplexer gezwungen, alle aktuell ausgeführten Medienbeispiele zu packen. Die Anwendung kann diese Pakete in Form von Medienbeispielen über **GetNextPacket** in einer Schleife sammeln, bis keine weiteren Pakete mehr abgerufen werden müssen.

Nachdem alle Medienbeispiele generiert wurden, rufen Sie [**IMFASFMultiplexer::End**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-end) auf, um das ASF-Headerobjekt zu aktualisieren, das diesen Datenpaketen zugeordnet ist. Das Header-Objekt wird durch Übergeben des ContentInfo-Objekts angegeben, das zum Initialisieren des Multiplexers verwendet wurde. Dieser Aufruf aktualisiert verschiedene Headerobjekte, um änderungen widerzuspiegeln, die vom Multiplexer während der Generierung von Datenpaketen vorgenommen wurden. Diese Informationen umfassen paketanzahl, Sendedauer, Wiedergabedauer und Streamnummern aller Streams. Die Gesamtheadergröße wird ebenfalls aktualisiert.

Sie müssen sicherstellen, dass [**End**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-end) aufgerufen wird, nachdem alle Datenpakete abgerufen wurden. Wenn Pakete im Multiplexer warten, schlägt **End** fehl und gibt den **MF E FLUSH \_ \_ \_ NEEDED-Fehlercode** zurück. Rufen Sie in diesem Fall das wartende Paket ab, indem [**Sie Flush**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-flush) und [**GetNextPacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket) in einer Schleife aufrufen.

> [!Note]  
> Für die VBR-Codierung müssen Sie nach dem Aufruf von **End** die Codierungsstatistiken in den Codierungseigenschaften des ContentInfo-Objekts festlegen. Informationen zu diesem Prozess finden Sie unter "Konfigurieren des ContentInfo-Objekts mit Encoder Einstellungen" unter [Festlegen von Eigenschaften im ContentInfo-Objekt.](setting-properties-in-the-contentinfo-object.md) Die folgende Liste zeigt die spezifischen Eigenschaften, die festgelegt werden sollen:
>
> -   [**MFPKEY \_ DIE durchschnittliche**](mfpkey-ravgproperty.md) Bitrate des VBR-Inhalts.
> -   [**MFPKEY \_ BAVG**](mfpkey-bavgproperty.md) ist das Pufferfenster für die durchschnittliche Bitrate.
> -   [**MFPKEY \_ RMAX**](mfpkey-rmaxproperty.md) ist die Spitzenbitrate des VBR-Inhalts.
> -   [**MFPKEY \_ BMAX**](mfpkey-bmaxproperty.md) ist das Spitzenpufferfenster.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ASF Multiplexer](asf-multiplexer.md)
</dt> <dt>

[Tutorial: Kopieren von ASF-Streams aus einer Datei in eine andere](tutorial--copying-asf-streams-from-one-file-to-another.md)
</dt> <dt>

[Tutorial: Schreiben einer WMA-Datei mithilfe der CBR-Codierung](tutorial--writing-a-wma-file-by-using-cbr-encoding.md)
</dt> </dl>

 

 



