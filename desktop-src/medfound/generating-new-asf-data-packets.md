---
description: Erstellen neuer ASF-Datenpakete
ms.assetid: 7afa9694-c965-40e2-8549-e32ff48def2a
title: Erstellen neuer ASF-Datenpakete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78f3432ecf34c58247a1533adb202b75f59d770c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484070"
---
# <a name="generating-new-asf-data-packets"></a>Erstellen neuer ASF-Datenpakete

Der ASF *Multiplexer* ist eine wmcontainer-Ebenenkomponente, die mit dem [ASF-Datenobjekt](asf-file-structure.md) zusammenarbeitet und einer Anwendung die Möglichkeit bietet, für einen Stream, der den im ContentInfo-Objekt definierten Anforderungen entspricht, ASF-Datenpakete zu generieren.

Der Multiplexer verfügt über eine Eingabe und eine Ausgabe. Er empfängt ein streambeispiel, das digitale Mediendaten enthält, und erstellt ein oder mehrere Datenpakete, die in einen ASF-Container geschrieben werden können.

In der folgenden Liste wird der Vorgang zum Erstellen von ASF-Datenpaketen zusammengefasst:

1.  Übergeben von Eingabedaten an den Multiplexer in [**imfasfmultiplexer::P rocesssample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample).
2.  Erfassen Sie die Datenpakete, indem Sie [**imfasfmultiplexer:: getnextpacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket) in einer Schleife aufrufen, bis alle vollständigen Pakete abgerufen wurden.
3.  Nachdem die Eingabedaten in komplette Pakete konvertiert wurden, sind möglicherweise einige ausstehende Daten im Multiplexer vorhanden, die nicht von [**getnextpacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket)abgerufen wurden. Rufen Sie [**imfasfmultiplexer:: Flush**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-flush) auf, um die ausstehenden Beispiele zu packeonieren, und erfassen Sie diese aus dem Multiplexer, indem Sie **getnextpacket** erneut aufrufen.
4.  Aktualisieren Sie die zugeordneten ASF-Header Objekte durch Aufrufen von [**imfasfmultiplexer:: End**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-end) , um Änderungen widerzuspiegeln, die von Multiplexer während der Generierung von Datenpaketen vorgenommen wurden

Das folgende Diagramm veranschaulicht die Generierung von Datenpaketen für eine ASF-Datei über den Multiplexer.

![Diagramm, das die Generierung von Datenpaketen für eine ASF-Datei anzeigt](images/packet.gif)

## <a name="asf-data-packet-creation"></a>Erstellung des ASF-Datenpakets

Nachdem Sie den Multiplexer erstellt und initialisiert haben, wie unter [Erstellen des Multiplexer-Objekts](creating-the-multiplexer-object.md)beschrieben, nennen Sie [**imfasfmultiplexer::P rocesssample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample) , um Eingabedaten für die Verarbeitung in Datenpakete an den Multiplexer zu übergeben. Die angegebene Eingabe muss ein Medien Beispiel ([**imfsample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) -Schnittstelle) sein, das einen oder mehrere Medien Puffer ([**imfmediabuffer**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediabuffer) -Schnittstelle) enthalten kann, die die Daten für einen Stream enthalten. Im Fall einer ASF-zu-ASF-Transcodierung kann das Eingabemedien Beispiel aus dem Splitter generiert werden, der packesierte streambeispiele erstellt. Weitere Informationen finden Sie unter [ASF-Splitter](asf-splitter.md).

Stellen Sie vor dem Aufrufen von [**processsample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample)sicher, dass der Zeitstempel des Eingabemedien Beispiels eine gültige Präsentationszeit ist. Andernfalls schlägt " **processsample** " fehl und gibt den "MF \_ E \_ No Sample"- \_ \_ Zeitstempel Code zurück.

Der Multiplexer kann Eingaben als komprimierte oder nicht komprimierte Medien Beispiele über [**processsample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample)akzeptieren. Der Multiplexer weist diesen Beispielen abhängig von der Bandbreitennutzung des Streams Sendezeiten zu. Während dieses Vorgangs überprüft der Multiplexer die Parameter für den Leaky-Bucket (Bitrate und Puffer Fenster Verwendung) und kann Beispiele ablehnen, die diese Werte nicht einhalten. Bei der Bandbreiten Prüfung kann für das Eingabemedien Beispiel aus einem der folgenden Gründe ein Fehler auftreten:

-   Wenn das Beispiel für ein Eingabe Medium zu spät eingetroffen ist, weil die zuletzt zugewiesene Sendezeit größer ist als der Zeitstempel in diesem Medien Beispiel. [**Processsample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample) schlägt fehl und gibt den Fehlercode für das **MF- \_ E- \_ Ende \_** zurück.
-   , Wenn der Zeitstempel für das Eingabemedien Beispiel vor der zugewiesenen Sendezeit liegt (Dies deutet auf einen Pufferüberlauf hin). Der Multiplexer kann diese Situation ignorieren, wenn er zur Anpassung der Bitrate konfiguriert ist, indem er während der Multiplexer-Initialisierung das Flag für die **\_ \_ Automatische Anpassung \_ von mfasf Multiplexer** festlegt. Weitere Informationen finden Sie unter "Multiplexer-Initialisierung und undichte Bucket-Einstellungen" unter [Erstellen des Multiplexer-Objekts](creating-the-multiplexer-object.md). Wenn dieses Flag nicht festgelegt ist und der Multiplexer einen Bandbreiten Überlauf feststellt, schlägt [**processsample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample) fehl und gibt den Fehlercode für die **MF-E- \_ \_ Bandbreite \_** zurück.

Nachdem der Multiplexer die Sendezeit zugewiesen hat, wird das Beispiel für Eingabemedien dem *Sendefenster* hinzugefügt – eine Liste mit Eingabemedien Beispielen, geordnet nach Sendezeiten und bereit für die Verarbeitung in Datenpakete. Während der Datenpaket Erstellung wird das Beispiel für Eingabemedien analysiert, und relevante Daten werden als Nutzlast in ein Datenpaket geschrieben. Ein umfassendes Datenpaket kann Daten aus einem oder mehreren Eingabemedien Beispielen enthalten.

Wenn neue Eingabemedien Beispiele im Sendefenster eintreffen, werden Sie zu einer Warteschlange hinzugefügt, bis ausreichend Medien Beispiele vorhanden sind, um ein umfassendes Paket zu bilden. Die Daten in Medien Puffern, die im Eingabemedien Beispiel enthalten sind, werden nicht in das generierte Datenpaket kopiert. Das Datenpaket enthält Verweise auf die Eingabemedien Puffer, bis das Eingabemedien Beispiel vollständig verpackt wurde und das vollständige Paket vom Multiplexer gesammelt wurde.

Wenn ein umfassendes Datenpaket verfügbar ist, kann es durch Aufrufen von [**imfasfmultiplexer:: getnextpacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket)abgerufen werden. Wenn Sie [**processsample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample) aufrufen, während fertige Pakete zum Abrufen bereit sind, tritt ein Fehler auf, und es wird der Fehlercode " **MF \_ E \_ notannahme** " zurückgegeben. Dies deutet darauf hin, dass der Multiplexer nicht mehr Eingaben akzeptieren kann, und Sie müssen **getnextpacket** aufrufen, um die wartenden Pakete abzurufen. Im Idealfall sollte jedem **processsample** -Aufruf mindestens ein **getnextpacket** -Aufruf folgen, um die gesamten Datenpakete abzurufen. Es kann mehr als ein Eingabemedien Beispiel dauern, um ein umfassendes Datenpaket zu erstellen. Im Gegensatz dazu können Daten in einem Eingabemedien Beispiel mehrere Pakete umfassen. Daher ergeben nicht alle Aufrufe von **processsample** Ausgabemedien Beispiele.

Wenn das Eingabemedien Beispiel einen Keyframe enthält, der durch das [**\_ Cleanpoint-Attribut "mfsampleextension**](mfsampleextension-cleanpoint-attribute.md) " angegeben wird, kopiert der Multiplexer das Attribut in das Paket.

## <a name="getting-asf-data-packets"></a>Erhalten von ASF-Datenpaketen

Um die Ausgabemedien Beispiele für ein vom Multiplexer generiertes, vom Multiplexer generiertes Datenpaket zu erfassen, müssen Sie [**imfasfmultiplexer:: getnextpacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket) in einer Schleife aufrufen, bis keine weiteren Ausgabemedien Beispiele für das Paket vorhanden sind. In der folgenden Liste sind die Erfolgsfälle aufgeführt:

-   Wenn ein vollständiges Datenpaket verfügbar ist, empfängt [**getnextpacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket) im *pdwstatusflags* -Parameter das Flag " **ASF-Status Kennzeichen \_ \_ \_ unvollständig** ". der *ppipacket* -Parameter empfängt einen Zeiger auf das erste Datenpaket. Diese Methode muss aufgerufen werden, solange Sie dieses Flag empfängt. Bei jeder iterierung verweist *ppipacket* auf das nächste Paket in der Warteschlange.
-   Wenn nur ein Datenpaket vorhanden ist, verweist *ppipacket* darauf, und das Flag für das **unvollständige ASF- \_ Statusflags \_ \_** wird in *pdwstatusflags* nicht empfangen.
-   [**Getnextpacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket) kann erfolgreich sein, ohne Datenpakete bereit zu lassen, wenn sich der Multiplexer noch im Prozess der packetisierung und dem Hinzufügen von Datenpaketen befindet. In diesem Fall verweist *ppipacket* auf **null**. Um den Vorgang fortzusetzen, müssen Sie dem Multiplexer weitere Eingabemedien Beispiele hinzugefügt werden, indem Sie [**processsample**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-processsample)aufrufen.

Der folgende Beispielcode zeigt eine Funktion, die Datenpakete mithilfe des Multiplexers generiert. Der generierte Datenpaket Inhalt wird in den vom Aufrufer zugeordneten Daten Byte Datenstrom geschrieben.


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



Die- `WriteBufferToByteStream` Funktion wird im Thema [**IMF Bytestream:: Write**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-write)angezeigt.

Eine komplette Anwendung, die dieses Codebeispiel verwendet, finden Sie unter [Tutorial: Kopieren von ASF-Streams aus einer Datei in eine andere](tutorial--copying-asf-streams-from-one-file-to-another.md).

## <a name="post-packet-generation-calls"></a>Post Packet-Generation-Aufrufe

Um sicherzustellen, dass im Multiplexer keine kompletten Datenpakete gewartet werden, wird [**imfasfmultiplexer:: Flush**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-flush)aufgerufen. Dadurch wird erzwungen, dass der Multiplexer alle ausgeführten Medien Beispiele packetisiert. Diese Pakete können von der Anwendung in Form von Medien Beispielen über **getnextpacket** in einer Schleife gesammelt werden, bis keine weiteren Pakete mehr abgerufen werden können.

Nachdem alle Medien Beispiele generiert wurden, wird [**imfasfmultiplexer:: End**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-end) aufgerufen, um das mit diesen Datenpaketen verknüpfte ASF-Header Objekt zu aktualisieren. Das Header Objekt wird durch Übergeben des ContentInfo-Objekts angegeben, das zum Initialisieren des Multiplexers verwendet wurde. Mit diesem Aufruf werden verschiedene Header Objekte aktualisiert, um Änderungen widerzuspiegeln, die während der Generierung des Datenpakets vom Multiplexer vorgenommen wurden Diese Informationen umfassen die Paket Anzahl, sende Dauer, Wiedergabedauer und streamnummern aller Streams. Die gesamte Header Größe wird ebenfalls aktualisiert.

Sie müssen sicherstellen, dass [**End**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-end) aufgerufen wird, nachdem alle Datenpakete abgerufen wurden. Wenn Pakete auf den Multiplexer warten, schlägt **End** fehl, und es wird der Fehlercode für den **MF \_ E \_ Flush \_** -Vorgang zurückgegeben. Rufen Sie in diesem Fall das wartende Paket ab, indem Sie " [**Flush**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-flush) " und " [**getnextpacket**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmultiplexer-getnextpacket) " in einer Schleife aufrufen.

> [!Note]  
> Bei der VBR-Codierung müssen Sie nach dem Aufrufen von **End** die Codierungs Statistik in den Codierungs Eigenschaften des ContentInfo-Objekts festlegen. Weitere Informationen zu diesem Prozess finden Sie unter "Konfigurieren des ContentInfo-Objekts mit Encodereinstellungen" unter [Festlegen von Eigenschaften im ContentInfo-Objekt](setting-properties-in-the-contentinfo-object.md). In der folgenden Liste sind die festzulegenden spezifischen Eigenschaften aufgeführt:
>
> -   [**Mfpkey \_ Ravg**](mfpkey-ravgproperty.md) ist die durchschnittliche Bitrate des VBR-Inhalts.
> -   [**Mfpkey \_ Bavg**](mfpkey-bavgproperty.md) ist das Puffer Fenster für die durchschnittliche Bitrate.
> -   [**Mfpkey \_ Rmax**](mfpkey-rmaxproperty.md) ist die Spitzen Bitrate der VBR-Inhalte.
> -   [**Mfpkey \_ Bmax**](mfpkey-bmaxproperty.md) ist das Hauptpuffer Fenster.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ASF Multiplexer](asf-multiplexer.md)
</dt> <dt>

[Tutorial: Kopieren von ASF-Streams aus einer Datei in eine andere](tutorial--copying-asf-streams-from-one-file-to-another.md)
</dt> <dt>

[Tutorial: Schreiben einer WMA-Datei mithilfe der CBR-Codierung](tutorial--writing-a-wma-file-by-using-cbr-encoding.md)
</dt> </dl>

 

 



