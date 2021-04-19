---
description: Die ASF-Datei Senke ist eine Implementierung von imfmediasink, die von Media Foundation bereitgestellt wird, die eine Anwendung zum Archivieren von ASF-Mediendaten in einer Datei verwenden kann. Weitere Informationen zum Objektmodell der ASF-Medien senken und zur allgemeinen Verwendung finden Sie unter ASF-Medien senken.
ms.assetid: 21cbde27-a2ca-4298-9197-43bcaf05588d
title: Hinzufügen von streaminformationen zur ASF-Datei-Senke
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42e08c6997d9c77836f379d4ca7b75720ddea245
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345051"
---
# <a name="adding-stream-information-to-the-asf-file-sink"></a>Hinzufügen von streaminformationen zur ASF-Datei-Senke

Die ASF-Datei Senke ist eine Implementierung von [**imfmediasink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) , die von Media Foundation bereitgestellt wird, die eine Anwendung zum Archivieren von ASF-Mediendaten in einer Datei verwenden kann. Weitere Informationen zum Objektmodell und zur allgemeinen Verwendung von ASF Medien senken finden Sie unter [ASF-Medien senken](asf-media-sinks.md).

Nach dem Instanziieren der Datei Senke muss Sie vor dem Erstellen der Topologie konfiguriert werden. Die Datei Senke muss die Datenströme in der Ausgabedatei, die Codierungs Modus-Informationen und die Metadaten kennen. In diesem Thema wird der Vorgang zum Hinzufügen von Datenströmen in der Datei Senke beschrieben.

-   [Hinzufügen von Streams in der ASF-Datei-Senke](#adding-streams-in-the-asf-file-sink)
-   [Auflisten von streamsenken](#enumerating-stream-sinks)
-   [Zugehörige Themen](#related-topics)

## <a name="adding-streams-in-the-asf-file-sink"></a>Hinzufügen von Streams in der ASF-Datei-Senke

Die Datei Senke muss die Ausgabestreams und ihre Eigenschaften kennen, damit Sie Ausgabe Beispiele entsprechend generieren und der Ausgabe-ASF-Datei hinzufügen kann. Diese Einstellungen werden in das endgültige Objekt des ASF-Headers geschrieben.

Um streaminformationen festzulegen, müssen Sie über einen Verweis auf das ASF ContentInfo-Objekt der Datei Senke verfügen. Weitere Informationen finden Sie unter [Erstellen der ASF-Datei-Senke](creating-the-asf-file-sink.md).

Im folgenden Verfahren werden die allgemeinen Schritte zum Konfigurieren des Streams mithilfe des ASF-Profil Objekts zusammengefasst.

**So konfigurieren Sie streaminformationen in der ASF-Datei-Senke**

1.  Erstellen Sie ein ASF-Profil Objekt, indem Sie [**mfcreateasfprofile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile)aufrufen.
2.  Erstellen Sie für jeden Stream in der Ausgabedatei einen Medientyp für den Zielstream, der in der Datei Senke hinzugefügt werden soll. Der Medientyp muss mit den von den Windows Media Encoder unterstützten Ausgabetypen kompatibel sein.

    Weitere Informationen zum Hinzufügen von Audiodatenströmen zum Profil finden Sie unter Creating Audiostreams for ASF Encoding.

    Weitere Informationen zum Hinzufügen von Videostreams zum Profil finden Sie unter Erstellen von Videostreams für die ASF-Codierung.

3.  Erstellen Sie Streams basierend auf den in Schritt 2 erstellten Medientypen durch Aufrufen von [**imfasfprofile:: CreateStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createstream).
4.  Weisen Sie eine streamnummer für den neu erstellten Stream zu, indem Sie den in Schritt 3 empfangenen [**imfasfstreamconfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) -Schnittstellen Zeiger aufrufen.
5.  Konfigurieren Sie den Stream optional mit den folgenden Informationen:
    -   Lecks von Bucket-Parametern durch Festlegen der Attribute: [**MF \_ asfstreamconfig \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) oder [**MF \_ asfstreamconfig \_ LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md)
    -   Nutz Last Erweiterung, gegenseitiger Ausschluss durch Aufrufen von [**imfasfstreamconfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) -Methoden.
6.  Legen Sie optional die Größe des Datenpakets für das Profil fest, indem Sie die Eigenschaften " [**MF \_ asfprofile \_ MinPacketSize**](mf-asfprofile-minpacketsize-attribute.md) " und " [**MF \_ asfprofile \_ MaxPacketSize**](mf-asfprofile-maxpacketsize-attribute.md) " festlegen Das ASF-Profil macht die [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Schnittstelle verfügbar, auf die eine Anwendung durch Aufrufen von **imfasfprofile:: QueryInterface** verweisen kann.
7.  Legen Sie Codierungsinformationen für den Stream in der Datei Senke fest. Erläutert unter [Festlegen von Eigenschaften in der Datei Senke](setting-properties-in-the-file-sink.md).
8.  Fügen Sie den Stream zum Profil hinzu, indem Sie [**imfasfprofile:: setStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-setstream)aufrufen.
9.  Ordnen Sie das Profil dem ContentInfo-Objekt zu, indem Sie [**imfasfcontentinfo:: setprofile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile)aufrufen.

Um einen vorhandenen Stream zu ändern, kann die Anwendung einen Verweis auf die [**imfasfstreamconfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) -Schnittstelle des Streams erhalten und entsprechend den Anforderungen neu konfigurieren. Zum Hinzufügen oder Entfernen von Streams muss die Anwendung [**imfasfprofile:: removestream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-removestream)aufrufen. Um diese Änderungen, streamänderungen oder Entfernungs Änderungen zu übernehmen, müssen Sie das Profil erneut im ContentInfo-Objekt festlegen. Dies überschreibt das vorhandene Profil, das bereits mit dem ContentInfo-Objekt verknüpft ist.


```C++
//-------------------------------------------------------------------
//  CreateVideoStream
//  Create an video stream and add it to the profile.
//
//  pProfile: A pointer to the ASF profile.
//  wStreamNumber: Stream number to assign for the new stream.
//    pType: A pointer to the source's video media type.
//-------------------------------------------------------------------

HRESULT CreateVideoStream(IMFASFProfile* pProfile, WORD wStreamNumber, IMFMediaType* pType)
{
    if (!pProfile)
    {
        return E_INVALIDARG;
    }
    if (wStreamNumber < 1 || wStreamNumber > 127 )
    {
        return MF_E_INVALIDSTREAMNUMBER;
    }

    HRESULT hr = S_OK;

    
    IMFMediaType* pVideoType = NULL;
    IMFASFStreamConfig* pVideoStream = NULL;

    UINT32 dwBitRate = 0;
        
    //Create a new video type from the source type
    hr = CreateCompressedVideoType(pType, &pVideoType);
    if (FAILED(hr))
    {
        goto done;
    }

    //Create a new stream with the video type
    hr = pProfile->CreateStream(pVideoType, &pVideoStream);
    if (FAILED(hr))
    {
        goto done;
    }
    

    //Set a valid stream number
    hr = pVideoStream->SetStreamNumber(wStreamNumber);
    if (FAILED(hr))
    {
        goto done;
    }

    //Add the stream to the profile
    hr = pProfile->SetStream(pVideoStream);
    if (FAILED(hr))
    {
        goto done;
    }

    wprintf_s(L"Video Stream created. Stream Number: %d .\n", wStreamNumber);

done:

    SafeRelease(&pVideoStream);
    SafeRelease(&pVideoType);

    return hr;
}
```



## <a name="enumerating-stream-sinks"></a>Auflisten von streamsenken

Für jeden Datenstrom im Profil, den das ContentInfo-Objekt kennt, erstellt die ASF-Datei-Senke eine streamsenke, die alle Eigenschaften des codierten Streams enthält, und fügt Sie hinzu. Die ASF-Datei-Senke enthält fixierte Datenströme. Dies bedeutet, dass Sie Datenströme nicht hinzufügen oder entfernen können, indem Sie [**imfmediasink:: addstreamsink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-addstreamsink) oder [**imfmediasink:: removestreamsink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-removestreamsink)aufrufen. Diese Aufrufe für die Datei-Senke schlagen mit dem \_ Fehlercode "MF E \_ streamsinks Fixed" fehl \_ . Durch das Hinzufügen oder Entfernen von Streams im Profil werden die streamsenken in der Datei Senke nicht automatisch hinzugefügt oder entfernt. Wenn sich ihre Streams im Profil geändert haben, müssen Sie die vorhandene Instanz der Datei verwerfen und mit neuen Datenstrom Informationen neu erstellen.

Im folgenden Verfahren werden die allgemeinen Schritte zum Auflisten von streamsenken in der ASF-Datei-Senke zusammengefasst.

**So zählen Sie streamsenken auf**

1.  Aufrufen von [**imfmediasink:: getstreamsink count**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkcount) zum Abrufen der Gesamtanzahl von streamsenken in der ASF-Datei-Senke.
2.  Schleife durch die Stream-senken: erhalten Sie einen Verweis auf die [**getstreamsink byindex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyindex) -Schnittstelle der Stream-Senke.

    Oder

    Aufrufen von [**imfmediasink:: getstreamsinkbyid**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyid) zum Abrufen der streamsenke durch Angeben der streamnummer. Jede streamsenke wird durch die Datenstrom Nummer identifiziert, die Sie beim Erstellen des Streams im Profil festgelegt haben.

Wenn Sie eine partielle Topologie zum Codieren einer Mediendatei entwickeln, müssen Sie die Datei Senke der Topologie als Knoten für die Ausgabe Topologie hinzufügen. Sie können dazu entweder jede streamsenke in der Datei Senke angeben oder das Datei-senkenaktivierungs-und die Datenstrom-senkenbezeichner festlegen. Weitere Informationen und ein Codebeispiel finden Sie unter [Erstellen von Ausgabe Knoten](creating-output-nodes.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ASF-Medien senken](asf-media-sinks.md)
</dt> <dt>

[Unterstützung von ASF in Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



