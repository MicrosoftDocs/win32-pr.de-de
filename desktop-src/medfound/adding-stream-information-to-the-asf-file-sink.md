---
description: Erfahren Sie mehr über das Hinzufügen von Streaminformationen zur ASF-Dateisenke, die eine Anwendung zum Archivieren von ASF-Mediendaten in einer Datei verwenden kann.
ms.assetid: 21cbde27-a2ca-4298-9197-43bcaf05588d
title: Hinzufügen von Streaminformationen zur ASF-Dateisenke
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de8202de8da5cb8e17534c334e3d39dddb3c4f99
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404357"
---
# <a name="adding-stream-information-to-the-asf-file-sink"></a>Hinzufügen von Streaminformationen zur ASF-Dateisenke

Die ASF-Dateisenke ist eine Implementierung von [**DURCHFMediaSink Media Foundation**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink) die eine Anwendung zum Archivieren von ASF-Mediendaten in einer Datei verwenden kann. Informationen zum Objektmodell und zur allgemeinen Verwendung von ASF-Mediensenken finden Sie unter [ASF-Mediensenken.](asf-media-sinks.md)

Nach dem Instanziieren der Dateisenke muss sie vor dem Erstellen der Topologie konfiguriert werden. Die Dateisenke muss die Datenströme in der Ausgabedatei, die Informationen zum Codierungsmodus und die Metadaten kennen. In diesem Thema wird der Prozess zum Hinzufügen eines Streams in der Dateisenke beschrieben.

-   [Hinzufügen von Streams in der ASF-Dateisenke](#adding-streams-in-the-asf-file-sink)
-   [Aufzählen von Streamsenken](#enumerating-stream-sinks)
-   [Verwandte Themen](#related-topics)

## <a name="adding-streams-in-the-asf-file-sink"></a>Hinzufügen von Streams in der ASF-Dateisenke

Die Dateisenke muss die Ausgabestreams und ihre Eigenschaften kennen, damit sie Ausgabebeispiele entsprechend generieren und der ASF-Ausgabedatei hinzufügen kann. Diese Einstellungen werden in das endgültige ASF-Headerobjekt geschrieben.

Um Streaminformationen festlegen zu können, müssen Sie über einen Verweis auf das ASF ContentInfo-Objekt der Dateisenke verfügen. Weitere Informationen finden Sie unter [Erstellen der ASF-Dateisenke.](creating-the-asf-file-sink.md)

Im folgenden Verfahren werden die allgemeinen Schritte zum Konfigurieren des Streams mithilfe des ASF-Profilobjekts zusammengefasst.

**So konfigurieren Sie Streaminformationen in der ASF-Dateisenke**

1.  Erstellen Sie ein ASF-Profilobjekt, indem [**Sie MFCreateASFProfile aufrufen.**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile)
2.  Erstellen Sie für jeden Stream in der Ausgabedatei einen Medientyp für den Zielstream, der der Dateisenke hinzugefügt werden soll. Der Medientyp muss mit den Ausgabetypen kompatibel sein, die von den Windows Media Encodern unterstützt werden.

    Informationen zum Hinzufügen von Audiostreams zum Profil finden Sie unter Erstellen von Audiostreams für die ASF-Codierung.

    Informationen zum Hinzufügen von Videostreams zum Profil finden Sie unter Erstellen von Videostreams für die ASF-Codierung.

3.  Erstellen Sie Streams basierend auf den Medientypen, die in Schritt 2 erstellt wurden, indem [**Sie IMFASFProfile::CreateStream aufrufen.**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createstream)
4.  Weisen Sie dem neu erstellten Stream eine Streamnummer zu, indem Sie den in Schritt 3 empfangenen [**IMFASFStreamConfig-Schnittstellenzeiger**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) aufrufen.
5.  Konfigurieren Sie optional den Stream mit den folgenden Informationen:
    -   Leaky bucket parameters by setting the attributes: [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) or [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md)
    -   Nutzlasterweiterung, gegenseitiger Ausschluss durch Aufrufen von [**IMFASFStreamConfig-Methoden.**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig)
6.  Legen Sie optional die Datenpaketgröße für das Profil fest, indem Sie die [**Attribute MF \_ ASFPROFILE \_ MINPACKETSIZE**](mf-asfprofile-minpacketsize-attribute.md) und [**MF \_ ASFPROFILE \_ MAXPACKETSIZE**](mf-asfprofile-maxpacketsize-attribute.md) festlegen. Das ASF-Profil macht die [**BEFIAttributes-Schnittstelle**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) verfügbar, auf die eine Anwendung verweisen kann, indem **sie IMFASFProfile::QueryInterface aufruft.**
7.  Legen Sie die Codierungsinformationen für den Stream in der Dateisenke fest. Dies wird unter [Festlegen von Eigenschaften in der Dateisenke erläutert.](setting-properties-in-the-file-sink.md)
8.  Fügen Sie den Stream dem Profil hinzu, indem Sie [**IMFASFProfile::SetStream aufrufen.**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-setstream)
9.  Ordnen Sie das Profil dem ContentInfo-Objekt zu, indem [**Sie IMFASFContentInfo::SetProfile aufrufen.**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-setprofile)

Um einen vorhandenen Stream zu ändern, kann die Anwendung einen Verweis auf die [**IMFASFStreamConfig-Schnittstelle**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) des Streams erhalten und gemäß den Anforderungen neu konfigurieren. Zum Hinzufügen oder Entfernen von Streams muss die Anwendung [**IMFASFProfile::RemoveStream aufrufen.**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-removestream) Um diese Änderungen zu übernehmen, Änderungen zu streamen oder zu entfernen, müssen Sie das Profil erneut im ContentInfo-Objekt festlegen. Dadurch wird das vorhandene Profil überschrieben, das dem ContentInfo-Objekt bereits zugeordnet ist.


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



## <a name="enumerating-stream-sinks"></a>Aufzählen von Streamsenken

Für jeden Stream im Profil, den das ContentInfo-Objekt kennt, erstellt die ASF-Dateisenke eine Streamsenke, die alle Eigenschaften des codierten Streams enthält, und fügt sie hinzu. Die ASF-Dateisenke ist für feste Streams konzipiert. Dies bedeutet, dass Sie keine Streams hinzufügen oder entfernen können, indem Sie [**DENKMediaSink::AddStreamSink**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-addstreamsink) oder [**DENKMediaSink::RemoveStreamSink aufrufen.**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-removestreamsink) Bei diesen Aufrufen für die Dateisenke tritt ein Fehler mit dem Fehlercode "MF \_ E \_ STREAMSINKS \_ FIXED" auf. Beim Hinzufügen oder Entfernen von Streams im Profil werden die Streamsenken in der Dateisenke nicht automatisch hinzugefügt oder entfernt. Sie müssen die vorhandene Instanz der Datei verwerfen und mit neuen Datenstrominformationen neu erstellen, wenn sich Ihre Streams im Profil geändert haben.

Im folgenden Verfahren werden die allgemeinen Schritte zum Aufzählen von Streamsenken in der ASF-Dateisenke zusammengefasst.

**So enumerieren Sie Streamsenken**

1.  Rufen [**Sie VORZEICHENMedienSink::GetStreamSinkCount**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkcount) auf, um die Gesamtzahl der Streamsenken in der ASF-Dateisenke zu erhalten.
2.  Eine Schleife durch die Streamsenken ang erhalten einen Verweis auf die [**GetStreamSinkByIndex-Schnittstelle**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyindex) der Streamsenke.

    Oder

    Rufen [**Sie durch Angabe der Datenstromnummer DEN NAMEN DESINKMEDIASink::GetStreamSinkById-Werts**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-getstreamsinkbyid) auf, um die Streamsenke zu erhalten. Jede Streamsenke wird mit der Streamnummer identifiziert, die Sie beim Erstellen des Streams im Profil festgelegt haben.

Wenn Sie eine Teiltopologie zum Codieren einer Mediendatei erstellen, müssen Sie der Topologie die Dateisenke als Ausgabetopologieknoten hinzufügen. Dazu können Sie entweder jede Streamsenke in der Dateisenke angeben oder das Aktivierungsobjekt der Dateisenke und die Bezeichner der Streamsenke festlegen. Weitere Informationen und Codebeispiele finden Sie unter [Erstellen von Ausgabeknoten.](creating-output-nodes.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ASF-Mediensenken](asf-media-sinks.md)
</dt> <dt>

[ASF-Unterstützung in Media Foundation](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



