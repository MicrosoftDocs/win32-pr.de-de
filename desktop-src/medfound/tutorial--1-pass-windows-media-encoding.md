---
description: 'Codierung bezieht sich auf den Prozess der Umstellung digitaler Medien von einem Format in ein anderes. Beispiel: das Umrechnen von MP3-Audiodaten in Windows Media Audio Format gemäß der Definition des Advanced Systems Format (ASF).'
ms.assetid: 4fe202d8-c8f5-4e9a-ad40-1aea8f767362
title: 'Tutorial: 1-Pass-Windows-Medien Codierung'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d670b107f315966a048a2f847183431f9a57bd4
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "103761460"
---
# <a name="tutorial-1-pass-windows-media-encoding"></a>Tutorial: 1-Pass-Windows-Medien Codierung

Codierung bezieht sich auf den Prozess der Umstellung digitaler Medien von einem Format in ein anderes. Beispiel: das Umrechnen von MP3-Audiodaten in Windows Media Audio Format gemäß der Definition des Advanced Systems Format (ASF).

**Hinweis**  Die ASF-Spezifikation definiert einen Containertyp für die Ausgabedatei (. WMA oder. wmv), die Mediendaten in einem beliebigen Format enthalten kann, komprimiert oder unkomprimiert. Beispielsweise kann ein ASF-Container, z. b. eine. WMA-Datei, Mediendaten im MP3-Format enthalten. Beim Codierungsprozess wird das tatsächliche Format der in der Datei enthaltenen Daten konvertiert.

In diesem Tutorial wird veranschaulicht, wie Sie die Eingabe Quelle für unverschlüsselte Inhalte (nicht DRM-geschützt) in Windows Media-Inhalt codieren und die Daten in einer neuen ASF-Datei (. WM \* ) mithilfe von ASF-Komponenten der Pipeline Schicht schreiben Diese Komponenten werden verwendet, um eine partielle Codierungs Topologie zu erstellen, die von einer Instanz der Medien Sitzung gesteuert wird.

In diesem Tutorial erstellen Sie eine Konsolenanwendung, die die Dateinamen für die Eingabe und Ausgabe und den Codierungs Modus als Argumente annimmt. Die Eingabedatei kann ein komprimiertes oder ein nicht komprimiertes Medienformat aufweisen. Gültige Codierungs Modi sind "CBR" (Konstante Bitrate) oder "VBR" (Variable Bitrate). Die Anwendung erstellt eine Medienquelle, die die durch den Eingabe Dateinamen angegebene Quelle darstellt, und die ASF-Datei-Senke, um den codierten Inhalt der Quelldatei in einer ASF-Datei zu archivieren. Damit das Szenario einfach implementiert werden kann, verfügt die Ausgabedatei nur über einen Audiostream und einen Videostream. Die Anwendung fügt den Windows Media Audio 9,1 Professional-Codec für die Audiostream-Formatkonvertierung und Windows Media Video 9-Codec für den Videostream ein.

Bei konstanter Bitrate-Codierung muss der Encoder vor Beginn der Codierungs Sitzung die Zielbitrate kennen, die er erreichen muss. In diesem Tutorial verwendet die Anwendung für den Modus "CBR" die Bitrate, die mit dem ersten Ausgabe Medientyp verfügbar ist, der vom Encoder während der Medientyp Aushandlung als Zielbitrate abgerufen wird. Für die variablenbitrate-Codierung veranschaulicht dieses Tutorial die Codierung mit variabler Bitrate durch Festlegen einer Qualitätsstufe. Die Audiodatenströme werden auf der Qualitätsstufe 98 und Videostreams auf der Qualitätsstufe 95 codiert.

Im folgenden Verfahren werden die Schritte zum Codieren von Windows Media-Inhalten in einem ASF-Container mithilfe eines 1-Pass-Codierungs Modus zusammengefasst.

1.  Erstellen Sie eine Medienquelle für die angegebene mithilfe des Quell Resolvers.
2.  Listet die Streams in der Medienquelle auf.
3.  Erstellen Sie die ASF-Medien Senke, und fügen Sie in Abhängigkeit von den Streams in der Medienquelle, die codiert werden müssen, streamsenken hinzu.
4.  Konfigurieren Sie die Medien Senke mit den erforderlichen Codierungs Eigenschaften.
5.  Erstellen Sie die Windows Media Encoder für die Streams in der Ausgabedatei.
6.  Konfigurieren Sie die Encoder mit den Eigenschaften, die für die Medien Senke festgelegt sind.
7.  Erstellen Sie eine partielle Codierungs Topologie.
8.  Instanziieren Sie die Medien Sitzung, und legen Sie die Topologie für die Medien Sitzung fest.
9.  Starten Sie die Codierungs Sitzung, indem Sie die Medien Sitzung Steuern und alle relevanten Ereignisse aus der Medien Sitzung erhalten.
10. Bei der VBR-Codierung werden die Codierungs Eigenschaftswerte aus dem Encoder und auf der Medien Senke festgelegt.
11. Schließen und beenden Sie die Codierungs Sitzung.

Dieses Tutorial enthält die folgenden Abschnitte:

-   [Voraussetzungen](#prerequisites)
-   [Einrichten des Projekts](#set-up-the-project)
-   [Erstellen der Medienquelle](#create-the-media-source)
-   [Erstellen der ASF-Datei-Senke](#create-the-asf-file-sink)
    -   [Erstellen des ASF-Profil Objekts](#create-the-asf-profile-object)
    -   [Erstellen eines komprimierten Audiomedien Typs](#create-a-compressed-audio-media-type)
    -   [Erstellen eines komprimierten Video Medientyps](#create-a-compressed-video-media-type)
    -   [Erstellen des ASF-ContentInfo-Objekts](#create-the-asf-contentinfo-object)
    -   [Erstellen der ASF-Datei-Senke](#create-the-asf-file-sink)
-   [Erstellen der partiellen Codierungs Topologie](#build-the-partial-encoding-topology)
    -   [Erstellen des Knotens "Quell Topologie" für die Medienquelle](#create-the-source-topology-node-for-the-media-source)
    -   [Instanziieren Sie die erforderlichen Encoder, und erstellen Sie die Transformations Knoten.](#instantiate-the-required-encoders-and-create-the-transform-nodes)
    -   [Erstellen der Knoten für die Ausgabe Topologie für die Datei Senke](#create-the-output-topology-nodes-for-the-file-sink)
    -   [Verbinden der Quell-, Transformations-und Senke Knoten](#connect-the-source-transform-and-sink-nodes)
-   [Verarbeiten der Codierungs Sitzung](#handling-the-encoding-session)
-   [Aktualisieren der Codierungs Eigenschaften in der Datei Senke](#update-encoding-properties-in-the-file-sink)
-   [Implementieren von Main](#implement-main)
-   [Testen der Ausgabedatei](#test-the-output-file)
-   [Allgemeine Fehler Codes und Tipps zum Debuggen](#common-error-codes-and-debugging-tips)
-   [Zugehörige Themen](#related-topics)

## <a name="prerequisites"></a>Voraussetzungen

In diesem Tutorial wird Folgendes vorausgesetzt:

-   Sie sind mit der [ASF-Dateistruktur](asf-file-structure.md)vertraut, die von Media Foundation bereitgestellten [ASF-Komponenten der Pipeline Schicht](pipeline-layer-asf-components.md) , um mit ASF-Objekten zu arbeiten. Zu diesen Komponenten gehören die folgenden Objekte:
    -   [Medienquellen](media-sources.md)

        **Hinweis**  Wenn Sie die transbewertung durchführen (das Umwandeln einer höheren Bitrate-Datei in eine Datei mit niedrigerer Bitrate ohne Änderung von Formaten), verwenden Sie die [ASF-Medienquelle](asf-media-source.md).

    -   [Windows Media Encoder](windows-media-encoders.md)
    -   [ASF-Medien senken](asf-media-sinks.md)
    -   [ASF-ContentInfo-Objekt](asf-contentinfo-object.md)
    -   [ASF-Profil](asf-profile.md)

-   Sie sind mit Windows Media Encoder und den verschiedenen Codierungs Typen vertraut, insbesondere [konstanter Bitraten Codierung](constant-bit-rate-encoding.md) und [Qualitäts basierter variablenbitrate-Codierung](quality-based-variable-bit-rate--vbr--encoding.md).
-   Sie sind mit MFT-Codierungs Vorgängen vertraut. Insbesondere das Erstellen einer Instanz des Encoders und das Festlegen von Eingabe-und Ausgabetypen für den Encoder.
-   Sie sind mit Topologieobjekten vertraut und erfahren, wie Sie eine Codierungs Topologie erstellen. Weitere Informationen zu Topologien und topologieknoten finden Sie unter [Erstellen von Topologien](creating-topologies.md).
-   Sie sind mit dem Ereignis Modell der [Medien Sitzung](media-session.md)und den Fluss Steuerungs Vorgängen vertraut. Weitere Informationen finden Sie unter [Medien Sitzungs Ereignisse](media-session-events.md).

## <a name="set-up-the-project"></a>Einrichten des Projekts

1.  Fügen Sie die folgenden Header in die Quelldatei ein:

    ```C++
    #include <new>
    #include <mfidl.h>            // Media Foundation interfaces
    #include <mfapi.h>            // Media Foundation platform APIs
    #include <mferror.h>        // Media Foundation error codes
    #include <wmcontainer.h>    // ASF-specific components
    #include <wmcodecdsp.h>        // Windows Media DSP interfaces
    #include <Dmo.h>            // DMO objects
    #include <uuids.h>            // Definition for FORMAT_VideoInfo
    #include <propvarutil.h>
    
    ```

    

2.  Verknüpfen Sie die folgenden Bibliotheksdateien:

    ```C++
    // The required link libraries 
    #pragma comment(lib, "mfplat")
    #pragma comment(lib, "mf")
    #pragma comment(lib, "mfuuid")
    #pragma comment(lib, "msdmo")
    #pragma comment(lib, "strmiids")
    #pragma comment(lib, "propsys")
    
    ```

    

3.  Deklarieren Sie die Funktion [saferelease](saferelease.md) .

    ```C++
    template <class T> void SafeRelease(T **ppT)
    {
        if (*ppT)
        {
            (*ppT)->Release();
            *ppT = NULL;
        }
    }
    ```

    

4.  Deklarieren Sie die Codierungs \_ Modus-Enumeration zum Definieren von CBR-und VBR-Codierungs Typen

    ```C++
    // Encoding mode
    typedef enum ENCODING_MODE {
      NONE  = 0x00000000,
      CBR   = 0x00000001,
      VBR   = 0x00000002,
    } ;
    
    ```

    

5.  Definiert eine Konstante für das Puffer Fenster für einen Videostream.

    ```C++
    // Video buffer window
    const INT32 VIDEO_WINDOW_MSEC = 3000;
    
    ```

    

## <a name="create-the-media-source"></a>Erstellen der Medienquelle

Erstellen Sie eine Medienquelle für die Eingabe Quelle. Media Foundation stellt integrierte Medienquellen für verschiedene Medienformate bereit: MP3, MP4/3GP, AVI/Wave. Informationen zu den von Media Foundation unterstützten Formaten finden Sie [unter Unterstützte Medienformate in Media Foundation](supported-media-formats-in-media-foundation.md).

Verwenden Sie zum Erstellen der Medienquelle den [quellresolver](source-resolver.md). Dieses Objekt analysiert die URL, die für die Quelldatei angegeben wurde, und erstellt die entsprechende Medienquelle.

Führen Sie die folgenden Aufrufe aus:

-   [**MF | atesourceresolver**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatesourceresolver)
-   [**IMF sourceresolver:: forateobjectfromurl**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl)

    Weitere Informationen zu diesen Aufrufen finden Sie unter [using the Source Resolver](using-the-source-resolver.md).

    Wenn die Eingabedatei im ASF-Format vorliegt und Sie Sie in eine andere Bitrate Datei konvertieren möchten, ohne Formate zu ändern, erstellt der Quell-Solver eine Instanz der [ASF-Medienquelle](asf-media-source.md).

Das folgende Codebeispiel zeigt eine Funktion, die für die angegebene Datei eine Medienquelle erstellt.


```C++
//  Create a media source from a URL.
HRESULT CreateMediaSource(PCWSTR sURL, IMFMediaSource **ppSource)
{
    MF_OBJECT_TYPE ObjectType = MF_OBJECT_INVALID;

    IMFSourceResolver* pSourceResolver = NULL;
    IUnknown* pSource = NULL;

    // Create the source resolver.
    HRESULT hr = MFCreateSourceResolver(&pSourceResolver);
    if (FAILED(hr))
    {
        goto done;
    }

    // Use the source resolver to create the media source.

    // Note: For simplicity this sample uses the synchronous method to create 
    // the media source. However, creating a media source can take a noticeable
    // amount of time, especially for a network source. For a more responsive 
    // UI, use the asynchronous BeginCreateObjectFromURL method.

    hr = pSourceResolver->CreateObjectFromURL(
        sURL,                       // URL of the source.
        MF_RESOLUTION_MEDIASOURCE,  // Create a source object.
        NULL,                       // Optional property store.
        &ObjectType,        // Receives the created object type. 
        &pSource            // Receives a pointer to the media source.
        );
    if (FAILED(hr))
    {
        goto done;
    }

    // Get the IMFMediaSource interface from the media source.
    hr = pSource->QueryInterface(IID_PPV_ARGS(ppSource));

done:
    SafeRelease(&pSourceResolver);
    SafeRelease(&pSource);
    return hr;
}
```



## <a name="create-the-asf-file-sink"></a>Erstellen der ASF-Datei-Senke

Erstellen Sie eine Instanz der ASF-Datei-Senke, die codierte Mediendaten in einer ASF-Datei am Ende der Codierungs Sitzung archiviert.

In diesem Tutorial erstellen Sie ein Aktivierungs Objekt für die ASF-Datei-Senke. Die dateisenke benötigt die folgenden Informationen, um die erforderlichen streamsenken zu erstellen.

-   Die Streams, die codiert und in die endgültige Datei geschrieben werden sollen.
-   Die Codierungs Eigenschaften, die zum Codieren des Medien Inhalts verwendet werden, z. b. Codierungstyp, Anzahl der Codierungs Durchläufen und die zugehörigen Eigenschaften.
-   Die globalen Dateieigenschaften, die für die Medien Senke angeben, ob die Parameter für die Leaky-Bucket (Bitrate und Puffergröße) automatisch angepasst werden sollen.

Die Datenstrom Informationen werden im ASF-Profil Objekt konfiguriert, und die Codierungs-und globalen Eigenschaften werden in einem Eigenschaften Speicher festgelegt, der vom ASF-ContentInfo-Objekt verwaltet wird.

Eine Übersicht über die ASF-Datei-Senke finden Sie unter [ASF-Medien senken](asf-media-sinks.md).

### <a name="create-the-asf-profile-object"></a>Erstellen des ASF-Profil Objekts

Damit die ASF-Datei-Senke codierte Mediendaten in eine ASF-Datei schreibt, muss die Senke die Anzahl der Streams und den Typ der Streams kennen, für die streamsenken erstellt werden. In diesem Tutorial extrahieren Sie diese Informationen aus der Medienquelle und erstellen entsprechende Ausgabedaten Ströme. Beschränken Sie die Ausgabestreams auf einen Audiostream und einen Videostream. Erstellen Sie für jeden ausgewählten Stream in der Quelle einen Zielstream, und fügen Sie ihn dem Profil hinzu.

Um diesen Schritt zu implementieren, benötigen Sie die folgenden Objekte.

-   [ASF-Profil](asf-profile.md)
-   Präsentations Deskriptor für die Medienquelle
-   Streamdeskriptoren für die ausgewählten Streams in der Medienquelle.
-   Medientypen für die ausgewählten Streams.

In den folgenden Schritten wird beschrieben, wie das ASF-Profil und die zielstreams erstellt werden.

**So erstellen Sie das ASF-Profil**

1.  Rufen Sie [**mfkreateasfprofile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile) auf, um ein leeres Profil Objekt zu erstellen.
2.  Rufen Sie [**imfmediasource:: foratepresentationdescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) auf, um den Präsentations Deskriptor für die Medienquelle zu erstellen, die Sie in diesem Tutorial im Abschnitt "Erstellen der Medienquelle" beschrieben haben.
3.  Aufrufen Sie [**imfpresentationdescriptor:: getstreamdescriptorcount**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorcount) , um die Anzahl der Streams in der Medienquelle abzurufen.
4.  Aufrufen von [**imfpresentationdescriptor:: getstreamdescriptorbyindex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) für jeden Stream in der Medienquelle Ruft den streamdeskriptor des Streams ab.
5.  Aufrufen von [**imfstreamdescriptor:: getmediatypeer Handler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) gefolgt von [**imfmediatypeer Handler:: getmediatypeer byindex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex) und Abrufen des ersten Medientyps für den Datenstrom.

    **Hinweis**   Um komplexe Aufrufe zu vermeiden, gehen Sie davon aus, dass nur ein Medientyp pro Stream vorhanden ist, und wählen Sie den ersten Medientyp des Streams aus. Bei komplexen Streams müssen Sie jeden Medientyp aus dem Medientyp Handler auflisten und den Medientyp auswählen, den Sie codieren möchten.

6.  Aufrufen von "I [**imfmediatype:: getmajortype**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getmajortype) " zum Abrufen des Haupttyps des Streams, um zu bestimmen, ob der Stream Audiodaten oder Videos enthält.
7.  Erstellen Sie, abhängig vom Haupttyp des Streams, Zielmedien Typen. Diese Medientypen enthalten Formatinformationen, die vom Encoder während der Codierungs Sitzung verwendet werden. In den folgenden Abschnitten dieses Lernprogramms wird der Prozess der Erstellung der Zielmedien Typen beschrieben.
    -   Erstellen eines komprimierten Audiomedien Typs
    -   Erstellen eines komprimierten Video Medientyps
8.  Erstellen Sie einen Datenstrom auf der Grundlage des Zielmedien Typs, konfigurieren Sie den Stream gemäß den Anforderungen der Anwendung, und fügen Sie den Stream zum Profil hinzu. Weitere Informationen finden Sie unter [Hinzufügen von Datenstrom Informationen zur-Senke der ASF-Datei](adding-stream-information-to-the-asf-file-sink.md).

    1.  Rufen Sie [**imfasfprofile:: foratestream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-createstream) auf, und übergeben Sie den Zielmedientyp, um den Ausgabedatenstrom zu erstellen. Die-Methode ruft die imfassstreamconfig-Schnittstelle des Stream-Objekts ab.
    2.  Konfigurieren Sie den Stream.
        -   Aufrufen von [**imfasfstreamconfig:: setstreamnumber**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-setstreamnumber) , um dem Stream eine Zahl zuzuweisen. Diese Einstellung ist obligatorisch.
        -   Konfigurieren Sie optional die Lecks-Bucket-Parameter, die Nutz Last Erweiterung und den gegenseitigen Ausschluss für jeden Stream, indem Sie [**imfasfstreamconfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) -Methoden und relevante Datenstrom-Konfigurations Attribute aufrufen
    3.  Fügen Sie die Codierungs Eigenschaften auf Streamebene mithilfe des ASF ContentInfo-Objekts hinzu. Weitere Informationen zu diesem Schritt finden Sie im Abschnitt "Erstellen des ASF-ContentInfo-Objekts" in diesem Tutorial.
    4.  Aufrufen von [**imfasfprofile:: setStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-setstream) , um den Stream zum Profil hinzuzufügen.

    Im folgenden Codebeispiel wird ein ausgabeaudiodatenstrom erstellt.

    ```C++
    //-------------------------------------------------------------------
    //  CreateAudioStream
    //  Create an audio stream and add it to the profile.
    //
    //  pProfile: A pointer to the ASF profile.
    //  wStreamNumber: Stream number to assign for the new stream.
    //-------------------------------------------------------------------

    HRESULT CreateAudioStream(IMFASFProfile* pProfile, WORD wStreamNumber)
    {
        if (!pProfile)
        {
            return E_INVALIDARG;
        }
        if (wStreamNumber < 1 || wStreamNumber > 127 )
        {
            return MF_E_INVALIDSTREAMNUMBER;
        }

        IMFMediaType* pAudioType = NULL;
        IMFASFStreamConfig* pAudioStream = NULL;
        
        //Create an output type from the encoder
        HRESULT hr = GetOutputTypeFromWMAEncoder(&pAudioType);
        if (FAILED(hr))
        {
            goto done;
        }
        
        //Create a new stream with the audio type
        hr = pProfile->CreateStream(pAudioType, &pAudioStream);
        if (FAILED(hr))
        {
            goto done;
        }

        //Set stream number
        hr = pAudioStream->SetStreamNumber(wStreamNumber);
        if (FAILED(hr))
        {
            goto done;
        }
        
        //Add the stream to the profile
        hr = pProfile->SetStream(pAudioStream);
        if (FAILED(hr))
        {
            goto done;
        }

        wprintf_s(L"Audio Stream created. Stream Number: %d.\n", wStreamNumber);

    done:
        SafeRelease(&pAudioStream);
        SafeRelease(&pAudioType);
        return hr;
    }
    ```

    

    Das folgende Codebeispiel erstellt einen ausgabevideostream.

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

    

Im folgenden Codebeispiel werden die Ausgabestreams abhängig von den Datenströmen in der Quelle erstellt.


```C++
    //For each stream in the source, add target stream information in the profile
    for (DWORD iStream = 0; iStream < dwSrcStream; iStream++)
    {
        hr = pPD->GetStreamDescriptorByIndex(
            iStream, &fSelected, &pStreamDesc);
        if (FAILED(hr))
        {
            goto done;
        }

        if (!fSelected)
        {
            continue;
        }

        //Get the media type handler
        hr = pStreamDesc->GetMediaTypeHandler(&pHandler);
        if (FAILED(hr))
        {
            goto done;
        }

        //Get the first media type 
        hr = pHandler->GetMediaTypeByIndex(0, &pMediaType);
        if (FAILED(hr))
        {
            goto done;
        }

        //Get the major type
        hr = pMediaType->GetMajorType(&guidMajor);
        if (FAILED(hr))
        {
            goto done;
        }

        // If this is a video stream, create the target video stream
        if (guidMajor == MFMediaType_Video)
        {
            //The stream level encoding properties will be set in this call
            hr = CreateVideoStream(pProfile, wStreamID, pMediaType);

            if (FAILED(hr))
            {
                goto done;
            }
        }
        
        // If this is an audio stream, create the target audio stream
        if (guidMajor == MFMediaType_Audio)
        {
            //The stream level encoding properties will be set in this call
            hr = CreateAudioStream(pProfile, wStreamID);

            if (FAILED(hr))
            {
                goto done;
            }
        }

        //Get stream's encoding property
        hr = pContentInfo->GetEncodingConfigurationPropertyStore(wStreamID, &pContentInfoProps);
        if (FAILED(hr))
        {
            goto done;
        }

        //Set the stream-level encoding properties
        hr = SetEncodingProperties(guidMajor, pContentInfoProps);       
        if (FAILED(hr))
        {
            goto done;
        }


        SafeRelease(&pMediaType);
        SafeRelease(&pStreamDesc);
        SafeRelease(&pContentInfoProps);
        wStreamID++;
    }
```



### <a name="create-a-compressed-audio-media-type"></a>Erstellen eines komprimierten Audiomedien Typs

Wenn Sie einen Audiostream in die Ausgabedatei einschließen möchten, erstellen Sie einen Audiotyp, indem Sie die Merkmale des codierten Typs angeben, indem Sie die erforderlichen Attribute festlegen. Um sicherzustellen, dass der Audiotyp mit dem Windows Media-Audioencoder kompatibel ist, instanziieren Sie den Encoder-MFT, legen Sie die Codierungs Eigenschaften fest, und rufen Sie einen Medientyp durch Aufrufen von [**imftransform:: getoutputavailabletype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype)ab. Sie können den erforderlichen Ausgabetyp durchlaufen, indem Sie alle verfügbaren Typen durchlaufen, die Attribute der einzelnen Medientypen erhalten und den Typ auswählen, der Ihren Anforderungen am ehesten entspricht. In diesem Tutorial können Sie den ersten verfügbaren Typ aus der Liste der vom Encoder unterstützten Ausgabemedien Typen erhalten.

**Hinweis**  Für Windows 7 stellt Media Foundation eine neue Funktion, [**mftranscodegetaudiooutputavailabletypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes) , bereit, mit der eine Liste der kompatiblen Audiotypen abgerufen wird. Diese Funktion ruft nur die Medientypen für die CBR-Codierung ab.

Für einen kompletten Audiotyp müssen die folgenden Attribute festgelegt sein:

-   [**Haupt-Typ des MF- \_ MT \_ \_**](mf-mt-major-type-attribute.md)
-   [**MF- \_ MT- \_ Untertyp**](mf-mt-subtype-attribute.md)
-   [**MF \_ \_ -MT- \_ audionum- \_ Kanäle**](mf-mt-audio-num-channels-attribute.md)
-   [**MF \_ \_ -MT- \_ Audiobeispiele \_ pro \_ Sekunde**](mf-mt-audio-samples-per-second-attribute.md)
-   [**MF \_ \_ -MT- \_ Audioblock \_ Ausrichtung**](mf-mt-audio-block-alignment-attribute.md)
-   [**MF \_ \_ -MT-audiodurchschn. \_ \_ Byte \_ pro \_ Sekunde**](mf-mt-audio-avg-bytes-per-second-attribute.md)
-   [**MF \_ \_ -MT- \_ audiobits \_ pro \_ Beispiel**](mf-mt-audio-bits-per-sample-attribute.md)

Im folgenden Codebeispiel wird ein komprimierter Audiotyp erstellt, indem ein kompatibler Typ aus dem Windows Media Audio Encoder erhalten wird. Die Implementierung von setencodingproperties wird im Abschnitt "Erstellen des ASF-ContentInfo-Objekts" in diesem Tutorial gezeigt.


```C++
//-------------------------------------------------------------------
//  GetOutputTypeFromWMAEncoder
//  Gets a compatible output type from the Windows Media audio encoder.
//
//  ppAudioType: Receives a pointer to the media type.
//-------------------------------------------------------------------

HRESULT GetOutputTypeFromWMAEncoder(IMFMediaType** ppAudioType)
{
    if (!ppAudioType)
    {
        return E_POINTER;
    }

    IMFTransform* pMFT = NULL;
    IMFMediaType* pType = NULL;
    IPropertyStore* pProps = NULL;

    //We need to find a suitable output media type
    //We need to create the encoder to get the available output types
    //and discard the instance.

    CLSID *pMFTCLSIDs = NULL;   // Pointer to an array of CLISDs. 
    UINT32 cCLSID = 0;            // Size of the array.

    MFT_REGISTER_TYPE_INFO tinfo;
    
    tinfo.guidMajorType = MFMediaType_Audio;
    tinfo.guidSubtype = MFAudioFormat_WMAudioV9;

    // Look for an encoder.
    HRESULT hr = MFTEnum(
        MFT_CATEGORY_AUDIO_ENCODER,
        0,                  // Reserved
        NULL,                // Input type to match. None.
        &tinfo,             // WMV encoded type.
        NULL,               // Attributes to match. (None.)
        &pMFTCLSIDs,        // Receives a pointer to an array of CLSIDs.
        &cCLSID             // Receives the size of the array.
        );
    if (FAILED(hr))
    {
        goto done;
    }

    // MFTEnum can return zero matches.
    if (cCLSID == 0)
    {
        hr = MF_E_TOPO_CODEC_NOT_FOUND;
        goto done;
    }
    else
    {
        // Create the MFT decoder
        hr = CoCreateInstance(pMFTCLSIDs[0], NULL,
            CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pMFT));

        if (FAILED(hr))
        {
            goto done;
        }

    }

    // Get the encoder's property store

    hr = pMFT->QueryInterface(IID_PPV_ARGS(&pProps));
    if (FAILED(hr))
    {
        goto done;
    }
    
    //Set encoding properties
    hr = SetEncodingProperties(MFMediaType_Audio, pProps);
    if (FAILED(hr))
    {
        goto done;
    }

    //Get the first output type
    //You can loop through the available output types to choose 
    //the one that meets your target requirements
    hr = pMFT->GetOutputAvailableType(0, 0, &pType);
    if (FAILED(hr))
    {
        goto done;
    }

    //Return to the caller
    *ppAudioType = pType;
    (*ppAudioType)->AddRef();
    
done:
    SafeRelease(&pProps);
    SafeRelease(&pType);
    SafeRelease(&pMFT);
    CoTaskMemFree(pMFTCLSIDs);
    return hr;
}
```



### <a name="create-a-compressed-video-media-type"></a>Erstellen eines komprimierten Video Medientyps

Wenn Sie einen Videostream in die Ausgabedatei einschließen möchten, erstellen Sie einen komplett codierten Videotyp. Der gesamte Medientyp muss die gewünschte Bitrate und die privaten Codec-Daten enthalten.

Es gibt zwei Möglichkeiten, einen gesamten Video Medientyp zu erstellen.

-   Erstellen Sie einen leeren Medientyp, kopieren Sie die Medientyp Attribute aus dem Quell Videotyp, und überschreiben Sie das Attribut " [**MF \_ MT \_ SubType**](mf-mt-subtype-attribute.md) " mit der GUID-Konstante "MF Videoformat \_ WMV3".

    Für einen kompletten Videotyp müssen die folgenden Attribute festgelegt sein:

    -   Haupt-Typ des MF- \_ MT \_ \_
    -   MF- \_ MT- \_ Untertyp
    -   MF- \_ MT- \_ Frame \_ Rate
    -   MF- \_ MT- \_ Frame \_ Größe
    -   MF- \_ MT- \_ Interlace- \_ Modus
    -   Verhältnis der MF- \_ MT- \_ Pixel \_ Seite \_
    -   MF-mittlere mittlere \_ \_ \_ Bitrate
    -   \_ \_ Benutzer \_ Daten für MF-MT

    Im folgenden Codebeispiel wird ein komprimierter Videotyp aus dem Videotyp der Quelle erstellt.

    ```C++
    //-------------------------------------------------------------------
    //  CreateCompressedVideoType
    //  Creates an output type from source's video media type.
    //
    //    pType: A pointer to the source's video media type.
    //  ppVideoType: Receives a pointer to the media type.
    //-------------------------------------------------------------------

    HRESULT CreateCompressedVideoType(
            IMFMediaType* pType, 
            IMFMediaType** ppVideoType)
    {
        if (!pType)
        {
            return E_INVALIDARG;
        }
        if (!ppVideoType)
        {
            return E_POINTER;
        }
        
        HRESULT hr = S_OK;
        MFRatio fps = { 0 };
        MFRatio par = { 0 };
        UINT32 width = 0, height = 0;
        UINT32 interlace = MFVideoInterlace_Unknown;
        UINT32 fSamplesIndependent = 0;
        UINT32 cBitrate = 0;

        IMFMediaType* pMediaType = NULL;

        GUID guidMajor = GUID_NULL;

        hr = pType->GetMajorType(&guidMajor);
        if (FAILED(hr))
        {
            goto done;
        }

        if (guidMajor != MFMediaType_Video )
        {
            hr = MF_E_INVALID_FORMAT;
            goto done;
        }

        hr = MFCreateMediaType(&pMediaType);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pType->CopyAllItems(pMediaType);
        if (FAILED(hr))
        {
            goto done;
        }

        //Fill the missing attributes
        //1. Frame rate
        hr = MFGetAttributeRatio(pMediaType, MF_MT_FRAME_RATE, (UINT32*)&fps.Numerator, (UINT32*)&fps.Denominator);
        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            fps.Numerator = 30000;
            fps.Denominator = 1001;

            hr = MFSetAttributeRatio(pMediaType, MF_MT_FRAME_RATE, fps.Numerator, fps.Denominator);
            if (FAILED(hr))
            {
                goto done;
            }
        }

        ////2. Frame size
        hr = MFGetAttributeSize(pMediaType, MF_MT_FRAME_SIZE, &width, &height);
        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            width = 1280;
            height = 720;
                
            hr = MFSetAttributeSize(pMediaType, MF_MT_FRAME_SIZE, width, height);
            if (FAILED(hr))
            {
                goto done;
            }
        }

        ////3. Interlace mode
        
        if (FAILED(pMediaType->GetUINT32(MF_MT_INTERLACE_MODE, &interlace)))
        {
            hr = pMediaType->SetUINT32(MF_MT_INTERLACE_MODE, MFVideoInterlace_Progressive);
            if (FAILED(hr))
            {
                goto done;
            }

        }

        ////4. Pixel aspect Ratio
        hr = MFGetAttributeRatio(pMediaType, MF_MT_PIXEL_ASPECT_RATIO, (UINT32*)&par.Numerator, (UINT32*)&par.Denominator);
        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            par.Numerator = par.Denominator = 1;
            hr = MFSetAttributeRatio(pMediaType, MF_MT_PIXEL_ASPECT_RATIO, (UINT32)par.Numerator, (UINT32)par.Denominator);
            if (FAILED(hr))
            {
                goto done;
            }

        }

        //6. bit rate
        if (FAILED(pMediaType->GetUINT32(MF_MT_AVG_BITRATE, &cBitrate)))
        {
            hr = pMediaType->SetUINT32(MF_MT_AVG_BITRATE, 1000000);
            if (FAILED(hr))
            {
                goto done;
            }

        }

        hr = pMediaType->SetGUID(MF_MT_SUBTYPE, MFVideoFormat_WMV3);
        if (FAILED(hr))
        {
            goto done;
        }

        // Return the pointer to the caller.
        *ppVideoType = pMediaType;
        (*ppVideoType)->AddRef();


    done:
        SafeRelease(&pMediaType);
        return hr;
    }
    
    ```

    

-   Abrufen eines kompatiblen Medientyps aus dem Windows Media-Video Encoder durch Festlegen der Codierungs Eigenschaften und anschließendes Aufrufen von [**imftransform:: getoutputavailabletype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype). Diese Methode gibt den partiellen Typ zurück. Stellen Sie sicher, dass Sie den partiellen Typ in einen vollständigen Typ konvertieren, indem Sie folgende Informationen hinzufügen:

    -   Legen Sie die Video [**Bitrate im MF \_ MT \_ AVG- \_ Bitrate**](mf-mt-avg-bitrate-attribute.md) -Attribut fest.
    -   Fügen Sie private Codec-Daten hinzu, indem Sie das [**MF \_ MT- \_ Benutzer \_ Daten**](mf-mt-user-data-attribute.md) Attribut festlegen. Ausführliche Anweisungen finden Sie unter "private Codec-Daten" unter [Konfigurieren eines WMV-Encoders](configuring-a-wmv-encoder.md).

    Da [**iwmcodecprivatedata:: getprivatedata**](../wmformat/iwmcodecprivatedata-getprivatedata.md) die Bitrate vor der Rückgabe der privaten Codec-Daten überprüft, stellen Sie sicher, dass Sie die Bitrate festlegen, bevor Sie die privaten Codec-Daten erhalten.

    Im folgenden Codebeispiel wird ein komprimierter Videotyp erstellt, indem ein kompatibler Typ aus dem Windows Media Video Encoder erhalten wird. Außerdem wird ein unkomprimierter Videotyp erstellt und als Eingabe des Encoders festgelegt. Dies wird in der Hilfsfunktion createuncompressedvideotype implementiert. Getoutputtypeer fromwmvencoder konvertiert den zurückgegebenen partiellen Typ durch Hinzufügen von privaten Codec-Daten in einen vollständigen Typ. Die Implementierung von setencodingproperties wird im Abschnitt "Erstellen des ASF-ContentInfo-Objekts" in diesem Tutorial gezeigt.

    ```C++
    //-------------------------------------------------------------------
    //  GetOutputTypeFromWMVEncoder
    //  Gets a compatible output type from the Windows Media video encoder.
    //
    //  pType: A pointer to the source video stream's media type.
    //  ppVideoType: Receives a pointer to the media type.
    //-------------------------------------------------------------------

    HRESULT GetOutputTypeFromWMVEncoder(IMFMediaType* pType, IMFMediaType** ppVideoType)
    {
        if (!ppVideoType)
        {
            return E_POINTER;
        }

        IMFTransform* pMFT = NULL;
        IPropertyStore* pProps = NULL;
        IMFMediaType* pInputType = NULL;
        IMFMediaType* pOutputType = NULL;
        
        UINT32 cBitrate = 0;

        //We need to find a suitable output media type
        //We need to create the encoder to get the available output types
        //and discard the instance.

        CLSID *pMFTCLSIDs = NULL;   // Pointer to an array of CLISDs. 
        UINT32 cCLSID = 0;          // Size of the array.

        MFT_REGISTER_TYPE_INFO tinfo;
        
        tinfo.guidMajorType = MFMediaType_Video;
        tinfo.guidSubtype = MFVideoFormat_WMV3;

        // Look for an encoder.
        HRESULT hr = MFTEnum(
            MFT_CATEGORY_VIDEO_ENCODER,
            0,                  // Reserved
            NULL,               // Input type to match. None.
            &tinfo,             // WMV encoded type.
            NULL,               // Attributes to match. (None.)
            &pMFTCLSIDs,        // Receives a pointer to an array of CLSIDs.
            &cCLSID             // Receives the size of the array.
            );
        if (FAILED(hr))
        {
            goto done;
        }

        // MFTEnum can return zero matches.
        if (cCLSID == 0)
        {
            hr = MF_E_TOPO_CODEC_NOT_FOUND;
            goto done;
        }
        else
        {
            //Create the MFT decoder
            hr = CoCreateInstance(pMFTCLSIDs[0], NULL,
                CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pMFT));
            if (FAILED(hr))
            {
                goto done;
            }

        }
        
        //Get the video encoder property store
        hr = pMFT->QueryInterface(IID_PPV_ARGS(&pProps));
        if (FAILED(hr))
        {
            goto done;
        }

        //Set encoding properties
        hr = SetEncodingProperties(MFMediaType_Video, pProps);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = CreateUncompressedVideoType(pType, &pInputType);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pMFT->SetInputType(0, pInputType, 0);

        //Get the first output type
        //You can loop through the available output types to choose 
        //the one that meets your target requirements
        hr =  pMFT->GetOutputAvailableType(0, 0, &pOutputType);
        if (FAILED(hr))
        {
            goto done;
        }
        
        hr = pType->GetUINT32(MF_MT_AVG_BITRATE, &cBitrate);
        if (FAILED(hr))
        {
            goto done;
        }

        //Now set the bit rate
        hr = pOutputType->SetUINT32(MF_MT_AVG_BITRATE, cBitrate);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = AddPrivateData(pMFT, pOutputType);
        if (FAILED(hr))
        {
            goto done;
        }

        //Return to the caller
        *ppVideoType = pOutputType;
        (*ppVideoType)->AddRef();
        
    done:
        SafeRelease(&pProps);
        SafeRelease(&pOutputType);
        SafeRelease(&pInputType);
        SafeRelease(&pMFT);
        CoTaskMemFree(pMFTCLSIDs);
        return hr;
    }
    ```

    

    Im folgenden Codebeispiel wird ein unkomprimierter Videotyp erstellt.

    ```C++
    //-------------------------------------------------------------------
    //  CreateUncompressedVideoType
    //  Creates an uncompressed video type.
    //
    //    pType: A pointer to the source's video media type.
    //  ppVideoType: Receives a pointer to the media type.
    //-------------------------------------------------------------------

    HRESULT CreateUncompressedVideoType(IMFMediaType* pType, IMFMediaType** ppMediaType)
    {
        if (!pType)
        {
            return E_INVALIDARG;
        }
        if (!ppMediaType)
        {
            return E_POINTER;
        }
        
        MFRatio fps = { 0 };
        MFRatio par = { 0 };
        UINT32 width = 0, height = 0;
        UINT32 interlace = MFVideoInterlace_Unknown;
        UINT32 cBitrate = 0;

        IMFMediaType* pMediaType = NULL;

        GUID guidMajor = GUID_NULL;

        HRESULT hr = pType->GetMajorType(&guidMajor);
        if (FAILED(hr))
        {
            goto done;
        }

        if (guidMajor != MFMediaType_Video )
        {
            hr = MF_E_INVALID_FORMAT;
            goto done;
        }

        hr = MFGetAttributeRatio(pType, MF_MT_FRAME_RATE, (UINT32*)&fps.Numerator, (UINT32*)&fps.Denominator);
        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            fps.Numerator = 30000;
            fps.Denominator = 1001;

        }
        hr = MFGetAttributeSize(pType, MF_MT_FRAME_SIZE, &width, &height);
        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            width = 1280;
            height = 720;

        }

        interlace = MFGetAttributeUINT32(pType, MF_MT_INTERLACE_MODE, MFVideoInterlace_Progressive);

        hr = MFGetAttributeRatio(pType, MF_MT_PIXEL_ASPECT_RATIO, (UINT32*)&par.Numerator, (UINT32*)&par.Denominator);
        if (FAILED(hr))
        {
            par.Numerator = par.Denominator = 1;
        }

        cBitrate = MFGetAttributeUINT32(pType, MF_MT_AVG_BITRATE, 1000000);

        hr = MFCreateMediaType(&pMediaType);
        if (FAILED(hr))
        {
            goto done;
        }
        hr = pMediaType->SetGUID(MF_MT_MAJOR_TYPE, guidMajor);
        if (FAILED(hr))
        {
            goto done;
        }
        hr = pMediaType->SetGUID(MF_MT_SUBTYPE, MFVideoFormat_RGB32);
        if (FAILED(hr))
        {
            goto done;
        }
        hr = MFSetAttributeRatio(pMediaType, MF_MT_FRAME_RATE, fps.Numerator, fps.Denominator);
        if (FAILED(hr))
        {
            goto done;
        }
        hr = MFSetAttributeSize(pMediaType, MF_MT_FRAME_SIZE, width, height);
        if (FAILED(hr))
        {
            goto done;
        }
        hr = pMediaType->SetUINT32(MF_MT_INTERLACE_MODE, 2);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pMediaType->SetUINT32(MF_MT_ALL_SAMPLES_INDEPENDENT, TRUE);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pMediaType->SetUINT32(MF_MT_AVG_BITRATE, cBitrate);
        if (FAILED(hr))
        {
            goto done;
        }

        // Return the pointer to the caller.
        *ppMediaType = pMediaType;
        (*ppMediaType)->AddRef();


    done:
        SafeRelease(&pMediaType);
        return hr;
    }
    ```

    

    Im folgenden Codebeispiel werden dem angegebenen Video Medientyp private Codec-Daten hinzugefügt.

    ```C++
    //
    // AddPrivateData
    // Appends the private codec data to a media type.
    //
    // pMFT: The video encoder
    // pTypeOut: A video type from the encoder's type list.
    //
    // The function modifies pTypeOut by adding the codec data.
    //

    HRESULT AddPrivateData(IMFTransform *pMFT, IMFMediaType *pTypeOut)
    {
        HRESULT hr = S_OK;
        ULONG cbData = 0;
        BYTE *pData = NULL;

        IWMCodecPrivateData *pPrivData = NULL;

        DMO_MEDIA_TYPE mtOut = { 0 };

        // Convert the type to a DMO type.
        hr = MFInitAMMediaTypeFromMFMediaType(
            pTypeOut, 
            FORMAT_VideoInfo, 
            (AM_MEDIA_TYPE*)&mtOut
            );
        
        if (SUCCEEDED(hr))
        {
            hr = pMFT->QueryInterface(IID_PPV_ARGS(&pPrivData));
        }

        if (SUCCEEDED(hr))
        {
            hr = pPrivData->SetPartialOutputType(&mtOut);
        }

        //
        // Get the private codec data
        //

        // First get the buffer size.
        if (SUCCEEDED(hr))
        {
            hr = pPrivData->GetPrivateData(NULL, &cbData);
        }

        if (SUCCEEDED(hr))
        {
            pData = new BYTE[cbData];

            if (pData == NULL)
            {
                hr = E_OUTOFMEMORY;
            }
        }

        // Now get the data.
        if (SUCCEEDED(hr))
        {
            hr = pPrivData->GetPrivateData(pData, &cbData);
        }

        // Add the data to the media type.
        if (SUCCEEDED(hr))
        {
            hr = pTypeOut->SetBlob(MF_MT_USER_DATA, pData, cbData);
        }

        delete [] pData;
        MoFreeMediaType(&mtOut);
        SafeRelease(&pPrivData);
        return hr;
    }
    ```

    

### <a name="create-the-asf-contentinfo-object"></a>Erstellen des ASF-ContentInfo-Objekts

Das Objekt "ASF ContentInfo" ist eine Komponente auf wmcontainerebene, die in erster Linie zum Speichern von Informationen über das ASF-Header Objekt dient Die ASF-Datei-Senke implementiert das ContentInfo-Objekt, um Informationen (in einem Eigenschaften Speicher) zu speichern, die zum Schreiben des ASF-Header Objekts der codierten Datei verwendet werden. Zu diesem Zweck müssen Sie vor dem Starten der Codierungs Sitzung den folgenden Satz von Informationen für das ContentInfo-Objekt erstellen und konfigurieren.

1.  Rufen Sie [**mfkreateasfcontentinfo**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfcontentinfo) auf, um ein leeres ContentInfo-Objekt zu erstellen.

    Im folgenden Codebeispiel wird ein leeres ContentInfo-Objekt erstellt.

    ```C++
        // Create an empty ContentInfo object
        hr = MFCreateASFContentInfo(&pContentInfo);
        if (FAILED(hr))
        {
            goto done;
        }
    
    ```

    

2.  Aufrufen von [**imfasfcontentinfo:: getencodingconfigurationpropertystore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) zum Abrufen des Eigenschafts Speichers auf Datenstrom Ebene der Datei Senke. In diesem Befehl müssen Sie die Datenstrom Nummer übergeben, die Sie beim Erstellen des ASF-Profils für den Stream zugewiesen haben.
3.  Legen Sie die [Codierungs Eigenschaften](configuring-the-encoder.md) auf Streamebene im Stream-Eigenschaften Speicher der Datei Senke fest. Weitere Informationen finden Sie unter "Stream Encoding Properties" unter [Setting Properties in the file Sink](setting-properties-in-the-file-sink.md).

    Im folgenden Codebeispiel werden die Eigenschaften der Streamebene im Eigenschaften Speicher der Datei Senke festgelegt.

    ```C++
            //Get stream's encoding property
            hr = pContentInfo->GetEncodingConfigurationPropertyStore(wStreamID, &pContentInfoProps);
            if (FAILED(hr))
            {
                goto done;
            }

            //Set the stream-level encoding properties
            hr = SetEncodingProperties(guidMajor, pContentInfoProps);       
            if (FAILED(hr))
            {
                goto done;
            }

    
    ```

    

    Im folgenden Codebeispiel wird die Implementierung von setencodingproperties veranschaulicht. Diese Funktion legt Codierungs Eigenschaften auf Streamebene für CBR und VBR fest.

    ```C++
    //-------------------------------------------------------------------
    //  SetEncodingProperties
    //  Create a media source from a URL.
    //
    //  guidMT:  Major type of the stream, audio or video
    //  pProps:  A pointer to the property store in which 
    //           to set the required encoding properties.
    //-------------------------------------------------------------------

    HRESULT SetEncodingProperties (const GUID guidMT, IPropertyStore* pProps)
    {
        if (!pProps)
        {
            return E_INVALIDARG;
        }

        if (EncodingMode == NONE)
        {
            return MF_E_NOT_INITIALIZED;
        }
       
        HRESULT hr = S_OK;

        PROPVARIANT var;

        switch (EncodingMode)
        {
            case CBR:
                // Set VBR to false.
                hr = InitPropVariantFromBoolean(FALSE, &var);
                if (FAILED(hr))
                {
                    goto done;
                }

                hr = pProps->SetValue(MFPKEY_VBRENABLED, var);
                if (FAILED(hr))
                {
                    goto done;
                }

                // Set the video buffer window.
                if (guidMT == MFMediaType_Video)
                {
                    hr = InitPropVariantFromInt32(VIDEO_WINDOW_MSEC, &var);
                    if (FAILED(hr))
                    {
                        goto done;
                    }

                    hr = pProps->SetValue(MFPKEY_VIDEOWINDOW, var);    
                    if (FAILED(hr))
                    {
                        goto done;
                    }
                }
                break;

            case VBR:
                //Set VBR to true.
                hr = InitPropVariantFromBoolean(TRUE, &var);
                if (FAILED(hr))
                {
                    goto done;
                }

                hr = pProps->SetValue(MFPKEY_VBRENABLED, var);
                if (FAILED(hr))
                {
                    goto done;
                }

                // Number of encoding passes is 1.

                hr = InitPropVariantFromInt32(1, &var);
                if (FAILED(hr))
                {
                    goto done;
                }

                hr = pProps->SetValue(MFPKEY_PASSESUSED, var);
                if (FAILED(hr))
                {
                    goto done;
                }

                // Set the quality level.

                if (guidMT == MFMediaType_Audio)
                {
                    hr = InitPropVariantFromUInt32(98, &var);
                    if (FAILED(hr))
                    {
                        goto done;
                    }

                    hr = pProps->SetValue(MFPKEY_DESIRED_VBRQUALITY, var);    
                    if (FAILED(hr))
                    {
                        goto done;
                    }
                }
                else if (guidMT == MFMediaType_Video)
                {
                    hr = InitPropVariantFromUInt32(95, &var);
                    if (FAILED(hr))
                    {
                        goto done;
                    }

                    hr = pProps->SetValue(MFPKEY_VBRQUALITY, var);    
                    if (FAILED(hr))
                    {
                        goto done;
                    }
                }
                break;

            default:
                hr = E_UNEXPECTED;
                break;
        }    

    done:
        PropVariantClear(&var);
        return hr;
    }
    ```

    

4.  Aufrufen von [**imfasfcontentinfo:: getencodingconfigurationpropertystore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore) zum Abrufen des globalen Eigenschafts Speichers der Datei Senke. In diesem Befehl müssen Sie 0 im ersten Parameter übergeben. Weitere Informationen finden Sie unter "globale dateisenke-Eigenschaften" unter [Festlegen von Eigenschaften in der Datei Senke](setting-properties-in-the-file-sink.md).
5.  Legen Sie [**mfpkey \_ asfmediasink \_ autoadjust \_ Bitrate**](mfpkey-asfmediasink-autoadjust-bitrate-property.md) auf Variant \_ true fest, um sicherzustellen, dass die Lecks-Bucket-Werte im ASF Multiplexer ordnungsgemäß angepasst werden. Weitere Informationen zu dieser Eigenschaft finden Sie unter "Multiplexer-Initialisierung und undichte Bucket-Einstellungen" unter [Erstellen des Multiplexer-Objekts](creating-the-multiplexer-object.md).

    Im folgenden Codebeispiel werden die Eigenschaften der Streamebene im Eigenschaften Speicher der Datei Senke festgelegt.

    ```C++
        //Now we need to set global properties that will be set on the media sink
        hr = pContentInfo->GetEncodingConfigurationPropertyStore(0, &pContentInfoProps);
        if (FAILED(hr))
        {
            goto done;
        }

        //Auto adjust Bitrate
        var.vt = VT_BOOL;
        var.boolVal = VARIANT_TRUE;

        hr = pContentInfoProps->SetValue(MFPKEY_ASFMEDIASINK_AUTOADJUST_BITRATE, var);
        
        //Initialize with the profile
        hr = pContentInfo->SetProfile(pProfile);
        if (FAILED(hr))
        {
            goto done;
        }
    ```

    

    > [!Note]  
    > Es gibt weitere Eigenschaften, die Sie auf der globalen Ebene für die Datei Senke festlegen können. Weitere Informationen finden Sie unter "Konfigurieren des ContentInfo-Objekts mit Encodereinstellungen" unter [Festlegen von Eigenschaften im ContentInfo-Objekt](setting-properties-in-the-contentinfo-object.md).

     

Verwenden Sie die konfigurierten ASF-ContentInfo, um ein Aktivierungs Objekt für die ASF-Datei-Senke zu erstellen (im nächsten Abschnitt beschrieben).

Wenn Sie eine Out-of-Process-Datei Senke ([**mfkreateasfmediasinkactivation**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate)) erstellen, die mit einem Aktivierungs Objekt verwendet wird, können Sie das konfigurierte ContentInfo-Objekt verwenden, um die ASF-Medien Senke zu instanziieren (im nächsten Abschnitt beschrieben). Wenn Sie eine in-Process-Datei Senke ([**mfcreateasfmediasink**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasink)) erstellen, anstatt das leere ContentInfo-Objekt wie in Schritt 1 beschrieben zu erstellen, rufen Sie einen Verweis auf die [**imfasfcontentinfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) -Schnittstelle ab, indem Sie **imfmediasink:: QueryInterface** für die Datei Senke aufrufen. Anschließend müssen Sie das ContentInfo-Objekt konfigurieren, wie in diesem Abschnitt beschrieben.

### <a name="create-the-asf-file-sink"></a>Erstellen der ASF-Datei-Senke

In diesem Schritt des Tutorials verwenden Sie die konfigurierte Datei "ASF ContentInfo", die Sie im vorherigen Schritt erstellt haben, um ein Aktivierungs Objekt für die ASF-Datei-Senke zu erstellen, indem Sie die [**mfcreateasfmediasinkaktivierungs**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfmediasinkactivate) -Funktion aufrufen. Weitere Informationen finden Sie unter [Erstellen der ASF-Datei-Senke](creating-the-asf-file-sink.md).

Im folgenden Codebeispiel wird das Aktivierungs Objekt für die dateisenke erstellt.


```C++
    //Create the activation object for the  file sink
    hr = MFCreateASFMediaSinkActivate(sURL, pContentInfo, &pActivate);
    if (FAILED(hr))
    {
        goto done;
    }

```



## <a name="build-the-partial-encoding-topology"></a>Erstellen der partiellen Codierungs Topologie

Als Nächstes erstellen Sie eine partielle Codierungs Topologie, indem Sie topologieknoten für die Medienquelle, die erforderlichen Windows Media Encoder und die ASF-Datei-Senke erstellen. Nachdem Sie die topologieknoten hinzugefügt haben, verbinden Sie die Quell-, Transformations-und Senke Knoten. Vor dem Hinzufügen von topologieknoten müssen Sie ein leeres Topologieobjekt erstellen, indem Sie [**mfcreatetopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology)aufrufen.

### <a name="create-the-source-topology-node-for-the-media-source"></a>Erstellen des Knotens "Quell Topologie" für die Medienquelle

In diesem Schritt erstellen Sie den quelltopologieknoten für die Medienquelle.

Um diesen Knoten zu erstellen, benötigen Sie die folgenden Verweise:

-   Ein Zeiger auf die Medienquelle, die Sie in dem Schritt erstellt haben, der im Abschnitt "Erstellen der Medienquelle" dieses Tutorials beschrieben wird.
-   Ein Zeiger auf den Präsentations Deskriptor für die Medienquelle. Sie können einen Verweis auf die imfpresentationdescriptor-Schnittstelle der Medienquelle abrufen, indem Sie [**imfmediasource:: createpresentationdescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor)aufrufen.
-   Ein Zeiger auf den Datenstrom Deskriptor für jeden Stream in der Medienquelle, für den Sie einen Zielstream in dem Schritt erstellt haben, den Sie im Abschnitt "Erstellen des ASF-Profil Objekts" dieses Tutorials beschrieben haben.

Weitere Informationen zum Erstellen von Quellknoten und Codebeispielen finden Sie unter [Erstellen von Quellknoten](creating-source-nodes.md).

Im folgenden Codebeispiel wird eine partielle Topologie erstellt, indem der Quellknoten und die erforderlichen Transformations Knoten hinzugefügt werden. Mit diesem Code werden die Hilfsfunktionen "addsourcenode" und "addtransformoutputnodes" aufgerufen. Diese Funktionen sind später in diesem Tutorial enthalten.


```C++
//-------------------------------------------------------------------
//  BuildPartialTopology
//  Create a partial encoding topology by adding the source and the sink.
//
//  pSource:  A pointer to the media source to enumerate the source streams.
//  pSinkActivate: A pointer to the activation object for ASF file sink.
//  ppTopology:  Receives a pointer to the topology.
//-------------------------------------------------------------------

HRESULT BuildPartialTopology(
       IMFMediaSource *pSource, 
       IMFActivate* pSinkActivate,
       IMFTopology** ppTopology)
{
    if (!pSource || !pSinkActivate)
    {
        return E_INVALIDARG;
    }
    if (!ppTopology)
    {
        return E_POINTER;
    }

    HRESULT hr = S_OK;

    IMFPresentationDescriptor* pPD = NULL;
    IMFStreamDescriptor *pStreamDesc = NULL;
    IMFMediaTypeHandler* pMediaTypeHandler = NULL;
    IMFMediaType* pSrcType = NULL;

    IMFTopology* pTopology = NULL;
    IMFTopologyNode* pSrcNode = NULL;
    IMFTopologyNode* pEncoderNode = NULL;
    IMFTopologyNode* pOutputNode = NULL;


    DWORD cElems = 0;
    DWORD dwSrcStream = 0;
    DWORD StreamID = 0;
    GUID guidMajor = GUID_NULL;
    BOOL fSelected = FALSE;


    //Create the topology that represents the encoding pipeline
    hr = MFCreateTopology (&pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

        
    hr = pSource->CreatePresentationDescriptor(&pPD);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pPD->GetStreamDescriptorCount(&dwSrcStream);
    if (FAILED(hr))
    {
        goto done;
    }

    for (DWORD iStream = 0; iStream < dwSrcStream; iStream++)
    {
        hr = pPD->GetStreamDescriptorByIndex(
            iStream, &fSelected, &pStreamDesc);
        if (FAILED(hr))
        {
            goto done;
        }

        if (!fSelected)
        {
            continue;
        }

        hr = AddSourceNode(pTopology, pSource, pPD, pStreamDesc, &pSrcNode);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pStreamDesc->GetMediaTypeHandler (&pMediaTypeHandler);
        if (FAILED(hr))
        {
            goto done;
        }
        
        hr = pStreamDesc->GetStreamIdentifier(&StreamID);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pMediaTypeHandler->GetMediaTypeByIndex(0, &pSrcType);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pSrcType->GetMajorType(&guidMajor);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = AddTransformOutputNodes(pTopology, pSinkActivate, pSrcType, &pEncoderNode);
        if (FAILED(hr))
        {
            goto done;
        }

        //now we have the transform node, connect it to the source node
        hr = pSrcNode->ConnectOutput(0, pEncoderNode, 0);
        if (FAILED(hr))
        {
            goto done;
        }
                

        SafeRelease(&pStreamDesc);
        SafeRelease(&pMediaTypeHandler);
        SafeRelease(&pSrcType);
        SafeRelease(&pEncoderNode);
        SafeRelease(&pOutputNode);
        guidMajor = GUID_NULL;
    }

    *ppTopology = pTopology;
   (*ppTopology)->AddRef();


    wprintf_s(L"Partial Topology Built.\n");

done:
    SafeRelease(&pStreamDesc);
    SafeRelease(&pMediaTypeHandler);
    SafeRelease(&pSrcType);
    SafeRelease(&pEncoderNode);
    SafeRelease(&pOutputNode);
    SafeRelease(&pTopology);

    return hr;
}
```



Im folgenden Codebeispiel wird der Codierungs Topologie erstellt und der Knoten der Quell Topologie hinzugefügt. Sie benötigt Zeiger auf ein zuvor Topologieobjekt, die Medienquelle zum Auflisten der Quelldaten Ströme, den Präsentations Deskriptor der Medienquelle und den Datenstrom Deskriptor der Medienquelle. Der Aufrufer erhält einen Zeiger auf den Knoten der Quell Topologie.


```C++
// Add a source node to a topology.
HRESULT AddSourceNode(
    IMFTopology *pTopology,           // Topology.
    IMFMediaSource *pSource,          // Media source.
    IMFPresentationDescriptor *pPD,   // Presentation descriptor.
    IMFStreamDescriptor *pSD,         // Stream descriptor.
    IMFTopologyNode **ppNode)         // Receives the node pointer.
{
    IMFTopologyNode *pNode = NULL;

    // Create the node.
    HRESULT hr = MFCreateTopologyNode(MF_TOPOLOGY_SOURCESTREAM_NODE, &pNode);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the attributes.
    hr = pNode->SetUnknown(MF_TOPONODE_SOURCE, pSource);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pNode->SetUnknown(MF_TOPONODE_PRESENTATION_DESCRIPTOR, pPD);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pNode->SetUnknown(MF_TOPONODE_STREAM_DESCRIPTOR, pSD);
    if (FAILED(hr))
    {
        goto done;
    }
    
    // Add the node to the topology.
    hr = pTopology->AddNode(pNode);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the pointer to the caller.
    *ppNode = pNode;
    (*ppNode)->AddRef();

done:
    SafeRelease(&pNode);
    return hr;
}
```



### <a name="instantiate-the-required-encoders-and-create-the-transform-nodes"></a>Instanziieren Sie die erforderlichen Encoder, und erstellen Sie die Transformations Knoten.

Die Media Foundation Pipeline fügt nicht automatisch die erforderlichen Windows Media Encoder für die Streams ein, die Sie codieren müssen. Die Anwendung muss die Encoder manuell hinzufügen. Auflisten Sie zu diesem Zweck die Streams im ASF-Profil, das Sie in dem Schritt im Abschnitt "Erstellen des ASF-Profil Objekts" in diesem Tutorial erstellt haben. Instanziieren Sie für jeden Stream in der Quelle und den entsprechenden Stream im Profil die erforderlichen Encoder. Für diesen Schritt benötigen Sie einen Zeiger auf das Aktivierungs Objekt für die Datei Senke, die Sie im Abschnitt "Erstellen der ASF-Datei-Senke" in diesem Tutorial erstellt haben.

Eine Übersicht über das Erstellen von Encodern über Aktivierungs Objekte finden [Sie unter Verwenden der Aktivierungs Objekte eines Encoder](using-an-encoder-s-activation-objects.md).

Im folgenden Verfahren werden die Schritte beschrieben, die erforderlich sind, um die erforderlichen Encoder zu instanziieren.

1.  Rufen Sie einen Verweis auf das ContentInfo-Objekt der Senke ab, indem Sie [**imfaktivate:: activateobject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) für die Datei Senke aktivieren und dann [**imfasfcontentinfo**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) aus der Datei Senke Abfragen, indem Sie **QueryInterface** aufrufen.
2.  Rufen Sie das mit dem ContentInfo-Objekt verknüpfte ASF-Profil durch Aufrufen von [**imfasfcontentinfo:: GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile)ab.
3.  Listet die Streams im Profil auf. Hierfür benötigen Sie die Anzahl der Datenströme und einen Verweis auf die [**imfasfstreamconfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig) -Schnittstelle jedes Streams.

    Wenden Sie die folgenden Methoden an:

    -   [**Imfasf profile:: getstreamcount**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreamcount)
    -   [**Imfasf profile:: GetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream)

4.  Für jeden Stream erhalten Sie den Haupttyp und die Codierungs Eigenschaften des Streams aus dem ContentInfo-Objekt.

    Wenden Sie die folgenden Methoden an:

    -   [**Imfasf streamconfig:: getmediatype**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getmediatype)
    -   [**IMF MediaType:: getmajortype**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getmajortype)
    -   [**Imfasbcontentinfo:: getencodingconfigurationpropertystore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore)

        Für diesen Befehl benötigen Sie die vom [**imfasfprofile:: GetStream**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstream) -Befehl abgerufene Datenstrom Nummer.

5.  Instanziieren Sie abhängig vom Typ des Streams, der Audiodatei oder des Videos das Aktivierungs Objekt für den Encoder, indem Sie [**mfcreatewmaencoderactivation**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) oder [**mfcreatewmvencoderactivation**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmvencoderactivate)aufrufen.

    Um diese Funktionen aufzurufen, benötigen Sie die folgenden Verweise:

    -   Ein Zeiger auf den Medientyp des Streams, der von [**imfasfstreamconfig:: getmediatype**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfstreamconfig-getmediatype) im vorherigen Schritt abgerufen wurde.
    -   Ein Zeiger auf den Codierungs Eigenschafts Speicher des Streams, der von [**imfasfcontentinfo:: getencodingconfigurationpropertystore**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getencodingconfigurationpropertystore)abgerufen wurde. Durch Übergeben eines Zeigers an den Eigenschaften Speicher werden die in der Datei-Senke festgelegten Stream-Eigenschaften auf die MFT des Encoders kopiert.

6.  Aktualisieren Sie den Parameter "Leaky Bucket" für den Audiodatenstrom.

    [**Mfkreatewmaencoderaktivierungs**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) legt den Ausgabetyp für den Windows Media-Audiocodec auf dem zugrunde liegenden Encoder-MFT fest. Nachdem der Typ des Ausgabe Mediums festgelegt wurde, ruft der Encoder die durchschnittliche Bitrate aus dem Ausgabe Medientyp ab, berechnet die drehbitrate des Puffer Fensters und legt die Lecks-Bucket-Werte fest, die während der Codierungs Sitzung verwendet werden. Sie können diese Werte in der Datei Senke aktualisieren, indem Sie entweder den Encoder Abfragen oder benutzerdefinierte Werte festlegen. Zum Aktualisieren von Werten benötigen Sie den folgenden Satz von Informationen:

    -   Durchschnittliche Bitrate: ermitteln Sie die durchschnittliche Bitrate aus dem für den Ausgabe Medientyp festgelegten Wert für " [**MF \_ MT \_ -audiodurchschn \_ \_ Bytes \_ pro \_ Sekunde**](mf-mt-audio-avg-bytes-per-second-attribute.md) ", der während der Medientyp Aushandlung ausgewählt wird.
    -   Puffer Fenster: Sie können es durch Aufrufen von [**iwmcodecleakybucket:: getbuffersizebits**](../wmformat/iwmcodecleakybucket-getbuffersizebits.md)abrufen.
    -   Anfängliche Puffergröße: wird auf 0 festgelegt.

    Erstellen Sie ein Array von DWords, und legen Sie den Wert in der Eigenschaft " [**mfpkey \_ asfstreamsink \_ korrigiert \_ leakybucket**](mfpkey-asfstreamsink-corrected-leakybucket-property.md) " der Audiodaten Strom-Senke fest. Wenn Sie die aktualisierten Werte nicht angeben, werden Sie von der Medien Sitzung entsprechend festgelegt.

    Weitere Informationen finden Sie unter unkomplizierter [Bucket-Puffer Modell](the-leaky-bucket-buffer-model.md).

Die in Schritt 5 erstellten Aktivierungs Objekte müssen der Topologie als Knoten für die Transformations Topologie hinzugefügt werden. Weitere Informationen und ein Codebeispiel finden Sie unter "Erstellen eines Transformations Knotens aus einem Aktivierungs Objekt" unter [Erstellen von Transformations Knoten](creating-transform-nodes.md).

Im folgenden Codebeispiel wird der erforderliche Encoder aktiviert und hinzugefügt. Sie benötigt Zeiger auf ein zuvor erstelltes Topologieobjekt, das Aktivierungs Objekt der Datei Senke und den Medientyp des Quelldaten Stroms. Außerdem wird addoutputnode aufgerufen (siehe nächstes Codebeispiel), mit dem der Senke-Knoten erstellt und der Codierungs Topologie hinzugefügt wird. Der Aufrufer erhält einen Zeiger auf den Knoten der Quell Topologie.


```C++
//-------------------------------------------------------------------
//  AddTransformOutputNodes
//  Creates and adds the sink node to the encoding topology.
//  Creates and adds the required encoder activates.

//  pTopology:  A pointer to the topology.
//  pSinkActivate:  A pointer to the file sink's activation object.
//  pSourceType: A pointer to the source stream's media type.
//  ppNode:  Receives a pointer to the topology node.
//-------------------------------------------------------------------

HRESULT AddTransformOutputNodes(
    IMFTopology* pTopology,
    IMFActivate* pSinkActivate,
    IMFMediaType* pSourceType,
    IMFTopologyNode **ppNode    // Receives the node pointer.
    )
{
    if (!pTopology || !pSinkActivate || !pSourceType)
    {
        return E_INVALIDARG;
    }

    IMFTopologyNode* pEncNode = NULL;
    IMFTopologyNode* pOutputNode = NULL;
    IMFASFContentInfo* pContentInfo = NULL;
    IMFASFProfile* pProfile = NULL;
    IMFASFStreamConfig* pStream = NULL;
    IMFMediaType* pMediaType = NULL;
    IPropertyStore* pProps = NULL;
    IMFActivate *pEncoderActivate = NULL;
    IMFMediaSink *pSink = NULL; 

    GUID guidMT = GUID_NULL;
    GUID guidMajor = GUID_NULL;

    DWORD cStreams = 0;
    WORD wStreamNumber = 0;

    HRESULT hr = S_OK;
        
    hr = pSourceType->GetMajorType(&guidMajor);
    if (FAILED(hr))
    {
        goto done;
    }

    // Create the node.
    hr = MFCreateTopologyNode(MF_TOPOLOGY_TRANSFORM_NODE, &pEncNode);
    if (FAILED(hr))
    {
        goto done;
    }
    
    //Activate the sink
    hr = pSinkActivate->ActivateObject(__uuidof(IMFMediaSink), (void**)&pSink);
    if (FAILED(hr))
    {
        goto done;
    }
    //find the media type in the sink
    //Get content info from the sink
    hr = pSink->QueryInterface(__uuidof(IMFASFContentInfo), (void**)&pContentInfo);
    if (FAILED(hr))
    {
        goto done;
    }
    

    hr = pContentInfo->GetProfile(&pProfile);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pProfile->GetStreamCount(&cStreams);
    if (FAILED(hr))
    {
        goto done;
    }

    for(DWORD index = 0; index < cStreams ; index++)
    {
        hr = pProfile->GetStream(index, &wStreamNumber, &pStream);
        if (FAILED(hr))
        {
            goto done;
        }
        hr = pStream->GetMediaType(&pMediaType);
        if (FAILED(hr))
        {
            goto done;
        }
        hr = pMediaType->GetMajorType(&guidMT);
        if (FAILED(hr))
        {
            goto done;
        }
        if (guidMT!=guidMajor)
        {
            SafeRelease(&pStream);
            SafeRelease(&pMediaType);
            guidMT = GUID_NULL;

            continue;
        }
        //We need to activate the encoder
        hr = pContentInfo->GetEncodingConfigurationPropertyStore(wStreamNumber, &pProps);
        if (FAILED(hr))
        {
            goto done;
        }

        if (guidMT == MFMediaType_Audio)
        {
             hr = MFCreateWMAEncoderActivate(pMediaType, pProps, &pEncoderActivate);
            if (FAILED(hr))
            {
                goto done;
            }
            wprintf_s(L"Audio Encoder created. Stream Number: %d .\n", wStreamNumber);

            break;
        }
        if (guidMT == MFMediaType_Video)
        {
            hr = MFCreateWMVEncoderActivate(pMediaType, pProps, &pEncoderActivate);
            if (FAILED(hr))
            {
                goto done;
            }
            wprintf_s(L"Video Encoder created. Stream Number: %d .\n", wStreamNumber);

            break;
        }
    }

    // Set the object pointer.
    hr = pEncNode->SetObject(pEncoderActivate);
    if (FAILED(hr))
    {
        goto done;
    }

    // Add the node to the topology.
    hr = pTopology->AddNode(pEncNode);
    if (FAILED(hr))
    {
        goto done;
    }

    //Add the output node to this node.
    hr = AddOutputNode(pTopology, pSinkActivate, wStreamNumber, &pOutputNode);
    if (FAILED(hr))
    {
        goto done;
    }

    //now we have the output node, connect it to the transform node
    hr = pEncNode->ConnectOutput(0, pOutputNode, 0);
    if (FAILED(hr))
    {
        goto done;
    }

   // Return the pointer to the caller.
    *ppNode = pEncNode;
    (*ppNode)->AddRef();


done:
    SafeRelease(&pEncNode);
    SafeRelease(&pOutputNode);
    SafeRelease(&pEncoderActivate);
    SafeRelease(&pMediaType);
    SafeRelease(&pProps);
    SafeRelease(&pStream);
    SafeRelease(&pProfile);
    SafeRelease(&pContentInfo);
    SafeRelease(&pSink);
    return hr;
}
```



### <a name="create-the-output-topology-nodes-for-the-file-sink"></a>Erstellen der Knoten für die Ausgabe Topologie für die Datei Senke

In diesem Schritt erstellen Sie den Knoten Ausgabe Topologie für die ASF-Datei-Senke.

Um diesen Knoten zu erstellen, benötigen Sie die folgenden Verweise:

-   Ein Zeiger auf das Aktivierungs Objekt, das Sie in dem Schritt erstellt haben, der im Abschnitt "Erstellen der ASF-Datei-Senke" dieses Tutorials beschrieben wird.
-   Die streamnummern zur Identifizierung der Stream-senken, die der Datei Senke hinzugefügt werden. Die streamnummern entsprechen der Datenstrom Kennung, die während der Datenstrom Erstellung festgelegt wurde.

Weitere Informationen zum Erstellen von Ausgabe Knoten und Codebeispielen finden Sie unter "Erstellen eines Ausgabe Knotens aus einem Aktivierungs Objekt" unter [Erstellen von Ausgabe Knoten](creating-output-nodes.md).

Wenn Sie kein Aktivierungs Objekt für die Datei-Senke verwenden, müssen Sie die streamsenken in der ASF-Datei-Senke auflisten und jede streamsenke als Ausgabe Knoten in der Topologie festlegen. Weitere Informationen zur Stream Sink-Enumeration finden Sie unter "Auflisten von streamsenken" unter [Hinzufügen von streaminformationen zur ASF-Datei-Senke](adding-stream-information-to-the-asf-file-sink.md).

Im folgenden Codebeispiel wird der Codierungs Knoten erstellt und der Codierungs Topologie hinzugefügt. Sie benötigt Zeiger auf ein zuvor erstelltes Topologieobjekt, das Aktivierungs Objekt der Datei Senke und die Identifikationsnummer des Streams. Der Aufrufer erhält einen Zeiger auf den Knoten der Quell Topologie.


```C++
// Add an output node to a topology.
HRESULT AddOutputNode(
    IMFTopology *pTopology,     // Topology.
    IMFActivate *pActivate,     // Media sink activation object.
    DWORD dwId,                 // Identifier of the stream sink.
    IMFTopologyNode **ppNode)   // Receives the node pointer.
{
    IMFTopologyNode *pNode = NULL;

    // Create the node.
    HRESULT hr = MFCreateTopologyNode(MF_TOPOLOGY_OUTPUT_NODE, &pNode);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the object pointer.
    hr = pNode->SetObject(pActivate);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the stream sink ID attribute.
    hr = pNode->SetUINT32(MF_TOPONODE_STREAMID, dwId);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pNode->SetUINT32(MF_TOPONODE_NOSHUTDOWN_ON_REMOVE, FALSE);
    if (FAILED(hr))
    {
        goto done;
    }

    // Add the node to the topology.
    hr = pTopology->AddNode(pNode);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the pointer to the caller.
    *ppNode = pNode;
    (*ppNode)->AddRef();

done:
    SafeRelease(&pNode);
    return hr;
}
```



Im folgenden Codebeispiel werden die streamsenken für eine angegebene Medien Senke aufgelistet.


```C++
//-------------------------------------------------------------------
//  EnumerateStreamSinks
//  Enumerates the stream sinks within the specified media sink.
//
//  pSink:  A pointer to the media sink.
//-------------------------------------------------------------------
HRESULT EnumerateStreamSinks (IMFMediaSink* pSink)
{
    if (!pSink)
    {
        return E_INVALIDARG;
    }
    
    IMFStreamSink* pStreamSink = NULL;
    DWORD cStreamSinks = 0;

    HRESULT hr = pSink->GetStreamSinkCount(&cStreamSinks);
    if (FAILED(hr))
    {
        goto done;
    }

    for(DWORD index = 0; index < cStreamSinks; index++)
    {
        hr = pSink->GetStreamSinkByIndex (index, &pStreamSink);
        if (FAILED(hr))
        {
            goto done;
        }

        //Use the stream sink
        //Not shown.
    }
done:
    SafeRelease(&pStreamSink);

    return hr;
}
```



### <a name="connect-the-source-transform-and-sink-nodes"></a>Verbinden der Quell-, Transformations-und Senke Knoten

In diesem Schritt verbinden Sie den Quellknoten mit dem Transformations Knoten, der auf die Codierungen verweist, die Sie in diesem Tutorial im Abschnitt "Instanziieren der erforderlichen Encoder und Erstellen der Transformations Knoten" beschrieben erstellt haben. Der Transformations Knoten wird mit dem Ausgabe Knoten verbunden, der das Aktivierungs Objekt für die Datei Senke enthält.

## <a name="handling-the-encoding-session"></a>Verarbeiten der Codierungs Sitzung

In diesem Schritt führen Sie die folgenden Schritte aus:

1.  Rufen Sie [**mfkreatemediasession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) auf, um eine Codierungs Sitzung zu erstellen.
2.  Greifen Sie auf [**imfmediasession:: settopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) zu, um die Codierungs Topologie für die Sitzung festzulegen. Wenn der-Befehl abgeschlossen ist, wertet die Medien Sitzung die topologieknoten aus und fügt zusätzliche Transformations Objekte ein, z. b. einen Decoder, der die angegebene komprimierte Quelle in nicht komprimierte Beispiele konvertiert, die als Eingabe an den Encoder übergeben werden
3.  Wenden Sie [**imfmediasession:: GetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-getevent) an, um die von der Medien Sitzung ausgelöbenen Ereignisse anzufordern.

    In der Ereignisschleife starten und schließen Sie die Codierungs Sitzung abhängig von den Ereignissen, die von der Medien Sitzung ausgelöst werden. Der [**imfmediasession:: settopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) -Befehl führt dazu, dass die Medien Sitzung das Ereignis [mesessiontopologystatus](mesessiontopologystatus.md) mit dem Wert für das MF- \_ topostatusready- \_ Flag aufruft. Alle Ereignisse werden asynchron generiert, und eine Anwendung kann diese Ereignisse synchron oder asynchron abrufen. Da es sich bei der Anwendung in diesem Tutorial um eine Konsolenanwendung handelt und blockierende Benutzeroberflächenthreads nicht von Bedeutung sind, werden die Ereignisse aus der Medien Sitzung synchron angezeigt.

    Um die Ereignisse asynchron zu erhalten, muss Ihre Anwendung die [**imfasynccallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) -Schnittstelle implementieren. Weitere Informationen und ein Beispiel für die Implementierung dieser Schnittstelle finden Sie unter "behandeln von Sitzungs Ereignissen" unter Wiedergeben von [Mediendateien mit Media Foundation](how-to-play-unprotected-media-files.md).

Warten Sie in der Ereignisschleife zum Übertragen von Medien Sitzungs Ereignissen auf das Ereignis [mesessiontopologystatus](mesessiontopologystatus.md) , das ausgelöst wird, wenn die [**imfmediasession:: settopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology) abgeschlossen und die Topologie aufgelöst wird. Starten Sie nach dem Abrufen des mesessiontopologystatus-Ereignisses die Codierungs Sitzung, indem Sie [**imfmediasession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start)aufrufen. Die Medien Sitzung generiert das [meendof Presentation](meendofpresentation.md) -Ereignis, wenn alle Codierungs Vorgänge vollständig sind. Dieses Ereignis muss für die VBR-Codierung behandelt werden und wird im nächsten Abschnitt "Aktualisieren der Codierungs Eigenschaften für die Datei-Senke für die VBR-Codierung" in diesem Tutorial erläutert.

Die Medien Sitzung generiert das ASF-Header Objekt und schließt die Datei ab, wenn die Codierungs Sitzung abgeschlossen ist, und löst dann das Ereignis [mesessionclosed](mesessionclosed.md) aus. Dieses Ereignis muss behandelt werden, indem für die Medien Sitzung ordnungsgemäße Herunterfahr Vorgänge durchgeführt werden. Um mit dem Herunterfahren zu beginnen, wenden Sie [**imfmediasession:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown)an. Nachdem die Codierungs Sitzung geschlossen wurde, können Sie keine andere Topologie für die Codierung auf derselben Medien Sitzungs Instanz festlegen. Um eine andere Datei zu codieren, muss die aktuelle Medien Sitzung geschlossen und freigegeben werden, und die neue Topologie muss für eine neu erstellte Medien Sitzung festgelegt werden. Im folgenden Codebeispiel wird die Medien Sitzung erstellt, die Codierungs Topologie festgelegt und die Ereignisse der Medien Sitzung behandelt.

Im folgenden Codebeispiel wird die Medien Sitzung erstellt, die Codierungs Topologie festgelegt und die Codierungs Sitzung gesteuert, indem Ereignisse aus der Medien Sitzung behandelt werden.


```C++
//-------------------------------------------------------------------
//  Encode
//  Controls the encoding session and handles events from the media session.
//
//  pTopology:  A pointer to the encoding topology.
//-------------------------------------------------------------------

HRESULT Encode(IMFTopology *pTopology)
{
    if (!pTopology)
    {
        return E_INVALIDARG;
    }
    
    IMFMediaSession *pSession = NULL;
    IMFMediaEvent* pEvent = NULL;
    IMFTopology* pFullTopology = NULL;
    IUnknown* pTopoUnk = NULL;


    MediaEventType meType = MEUnknown;  // Event type

    HRESULT hr = S_OK;
    HRESULT hrStatus = S_OK;            // Event status
                
    MF_TOPOSTATUS TopoStatus = MF_TOPOSTATUS_INVALID; // Used with MESessionTopologyStatus event.    
        

    hr = MFCreateMediaSession(NULL, &pSession);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSession->SetTopology(MFSESSION_SETTOPOLOGY_IMMEDIATE, pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

    //Get media session events synchronously
    while (1)
    {
        hr = pSession->GetEvent(0, &pEvent);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pEvent->GetType(&meType);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pEvent->GetStatus(&hrStatus);
        if (FAILED(hr))
        {
            goto done;
        }
        if (FAILED(hrStatus))
        {
            hr = hrStatus;
            goto done;
        }

       switch(meType)
        {
            case MESessionTopologyStatus:
                {
                    // Get the status code.
                    MF_TOPOSTATUS status = (MF_TOPOSTATUS)MFGetAttributeUINT32(
                                             pEvent, MF_EVENT_TOPOLOGY_STATUS, MF_TOPOSTATUS_INVALID);

                    if (status == MF_TOPOSTATUS_READY)
                    {
                        PROPVARIANT var;
                        PropVariantInit(&var);
                        wprintf_s(L"Topology resolved and set on the media session.\n");

                        hr = pSession->Start(NULL, &var);
                        if (FAILED(hr))
                        {
                            goto done;
                        }

                    }
                    if (status == MF_TOPOSTATUS_STARTED_SOURCE)
                    {
                        wprintf_s(L"Encoding started.\n");
                        break;
                    }
                    if (status == MF_TOPOSTATUS_ENDED)
                    {
                        wprintf_s(L"Encoding complete.\n");
                        hr = pSession->Close();
                        if (FAILED(hr))
                        {
                            goto done;
                        }

                        break;
                    }
                }
                break;


            case MESessionEnded:
                wprintf_s(L"Encoding complete.\n");
                hr = pSession->Close();
                if (FAILED(hr))
                {
                    goto done;
                }
                break;

            case MEEndOfPresentation:
                {
                    if (EncodingMode == VBR)
                    {
                        hr = pSession->GetFullTopology(MFSESSION_GETFULLTOPOLOGY_CURRENT, 0, &pFullTopology);
                        if (FAILED(hr))
                        {
                            goto done;
                        }
                        hr = PostEncodingUpdate(pFullTopology);
                        if (FAILED(hr))
                        {
                            goto done;
                        }
                        wprintf_s(L"Updated sinks for VBR. \n");
                    }
                }
                break;

            case MESessionClosed:
                wprintf_s(L"Encoding session closed.\n");

                hr = pSession->Shutdown();
                goto done;
        }
        if (FAILED(hr))
        {
            goto done;
        }

        SafeRelease(&pEvent);

    }
done:
    SafeRelease(&pEvent);
    SafeRelease(&pSession);
    SafeRelease(&pFullTopology);
    SafeRelease(&pTopoUnk);
    return hr;
}
```



## <a name="update-encoding-properties-in-the-file-sink"></a>Aktualisieren der Codierungs Eigenschaften in der Datei Senke

Bestimmte Codierungs Eigenschaften, wie z. b. die Codierungs Bitrate und die exakten Werte für den leckwert, werden erst nach Abschluss der Codierung bekannt, insbesondere bei der VBR-Codierung. Um die korrekten Werte zu erhalten, muss die Anwendung auf das [meendofpresentation](meendofpresentation.md) -Ereignis warten, das angibt, dass die Codierungs Sitzung beendet ist. Die Leaky-Bucket-Werte müssen in der Senke aktualisiert werden, damit das ASF-Header Objekt die exakten Werte widerspiegeln kann.

Im folgenden Verfahren werden die Schritte beschrieben, die zum Durchlaufen der Knoten in der Codierungs Topologie erforderlich sind, um den dateisenke-Knoten zu erhalten und die erforderlichen Eigenschaften für das Leaky

**So aktualisieren Sie die Eigenschaftswerte nach der Codierung in der ASF-Datei-Senke**

1.  Aufrufen von [**imftopology:: getoutputnodecollection**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-getoutputnodecollection) zum Abrufen der Ausgabe Knoten Sammlung aus der Codierungs Topologie.
2.  Rufen Sie für jeden Knoten einen Zeiger auf die streamsenke im Knoten durch Aufrufen von [**imftopologynode:: GetObject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getobject)ab. Fragen Sie die [**IMF streamsink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink) -Schnittstelle auf dem [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Zeiger ab, der von **imftopologynode:: GetObject** zurückgegeben wurde.
3.  Rufen Sie für jede streamsenke den downstreamknoten (Encoder) ab, indem Sie [**imftopologynode:: GetInput**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-getinput)aufrufen.
4.  Fragen Sie den Knoten ab, um den [**imftransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) -Zeiger vom encoderknoten zu erhalten.
5.  Fragen Sie den Encoder nach dem [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) -Zeiger ab, um den Codierungs Eigenschaften Speicher vom Encoder zu erhalten.
6.  Fragen Sie die streamsenke für den [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) -Zeiger ab, um den Eigenschaften Speicher der Stream-Senke zu erhalten.
7.  Rufen Sie [**IPropertyStore:: GetValue**](/windows/win32/api/propsys/nn-propsys-ipropertystore) auf, um die erforderlichen Eigenschaftswerte aus dem Eigenschaften Speicher des Encoders abzurufen und Sie durch Aufrufen von **IPropertyStore:: SetValue** in den Eigenschaften Speicher der Stream-Senke zu kopieren.

In der folgenden Tabelle sind die Eigenschaftswerte nach der Codierung aufgeführt, die für die streamsenke für den Videostream festgelegt werden müssen.



| Codierungstyp                                                                                  | Eigenschaftsname (GetValue)                                                                        | Eigenschaftsname (SetValue)                                                                                                |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [Konstante Bitrate-Codierung](constant-bit-rate-encoding.md)                                   | mfpkey \_ bavg<br/> mfpkey \_ Ravg<br/>                                                 | mfpkey \_ stat \_ bavg<br/> mfpkey \_ stat \_ Ravg<br/>                                                             |
| [Qualitäts basierte Variable Bitrate Codierung](quality-based-variable-bit-rate--vbr--encoding.md) | mfpkey \_ bavg<br/> mfpkey \_ Ravg<br/> mfpkey ( \_ bmax)<br/> mfpkey- \_ Rmax<br/> | mfpkey \_ stat \_ bavg<br/> mfpkey \_ stat \_ Ravg<br/> mfpkey \_ stat ( \_ bmax)<br/> mfpkey \_ stat \_ Rmax<br/> |



 

Im folgenden Codebeispiel werden die Eigenschaftswerte nach der Codierung festgelegt.


```C++
//-------------------------------------------------------------------
//  PostEncodingUpdate
//  Updates the file sink with encoding properties set on the encoder
//  during the encoding session.
    //1. Get the output nodes
    //2. For each node, get the downstream node
    //3. For the downstream node, get the MFT
    //4. Get the property store
    //5. Get the required values
    //6. Set them on the stream sink
//
//  pTopology: A pointer to the full topology retrieved from the media session.
//-------------------------------------------------------------------

HRESULT PostEncodingUpdate(IMFTopology *pTopology)
{
    if (!pTopology)
    {
        return E_INVALIDARG;
    }

    HRESULT hr = S_OK;

    IMFCollection* pOutputColl = NULL;
    IUnknown* pNodeUnk = NULL;
    IMFMediaType* pType = NULL;
    IMFTopologyNode* pNode = NULL;
    IUnknown* pSinkUnk = NULL;
    IMFStreamSink* pStreamSink = NULL;
    IMFTopologyNode* pEncoderNode = NULL;
    IUnknown* pEncoderUnk = NULL;
    IMFTransform* pEncoder = NULL;
    IPropertyStore* pStreamSinkProps = NULL;
    IPropertyStore* pEncoderProps = NULL;

    GUID guidMajorType = GUID_NULL;

    PROPVARIANT var;
    PropVariantInit( &var );

    DWORD cElements = 0;

    hr = pTopology->GetOutputNodeCollection( &pOutputColl);
    if (FAILED(hr))
    {
        goto done;
    }


    hr = pOutputColl->GetElementCount(&cElements);
    if (FAILED(hr))
    {
        goto done;
    }


    for(DWORD index = 0; index < cElements; index++)
    {
        hr = pOutputColl->GetElement(index, &pNodeUnk);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pNodeUnk->QueryInterface(IID_IMFTopologyNode, (void**)&pNode);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pNode->GetInputPrefType(0, &pType);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pType->GetMajorType( &guidMajorType );
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pNode->GetObject(&pSinkUnk);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pSinkUnk->QueryInterface(IID_IMFStreamSink, (void**)&pStreamSink);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pNode->GetInput( 0, &pEncoderNode, NULL );
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pEncoderNode->GetObject(&pEncoderUnk);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pEncoderUnk->QueryInterface(IID_IMFTransform, (void**)&pEncoder);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pStreamSink->QueryInterface(IID_IPropertyStore, (void**)&pStreamSinkProps);
        if (FAILED(hr))
        {
            goto done;
        }

        hr = pEncoder->QueryInterface(IID_IPropertyStore, (void**)&pEncoderProps);
        if (FAILED(hr))
        {
            goto done;
        }

        if( guidMajorType == MFMediaType_Video )
        {            
            hr = pEncoderProps->GetValue( MFPKEY_BAVG, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_BAVG, var );
            if (FAILED(hr))
            {
                goto done;
            }

            PropVariantClear( &var );
            hr = pEncoderProps->GetValue( MFPKEY_RAVG, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_RAVG, var);
            if (FAILED(hr))
            {
                goto done;
            }

            PropVariantClear( &var );
            hr = pEncoderProps->GetValue( MFPKEY_BMAX, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_BMAX, var);
            if (FAILED(hr))
            {
                goto done;
            }

            PropVariantClear( &var );
            hr = pEncoderProps->GetValue( MFPKEY_RMAX, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_RMAX, var);
            if (FAILED(hr))
            {
                goto done;
            }
        }
        else if( guidMajorType == MFMediaType_Audio )
        {      
            hr = pEncoderProps->GetValue( MFPKEY_STAT_BAVG, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_BAVG, var );
            if (FAILED(hr))
            {
                goto done;
            }
            
            PropVariantClear( &var );
            hr = pEncoderProps->GetValue( MFPKEY_STAT_RAVG, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_RAVG, var );
            if (FAILED(hr))
            {
                goto done;
            }
            
            PropVariantClear( &var );
            hr = pEncoderProps->GetValue( MFPKEY_STAT_BMAX, &var);
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_BMAX, var);
            if (FAILED(hr))
            {
                goto done;
            }

            PropVariantClear( &var );
            hr = pEncoderProps->GetValue( MFPKEY_STAT_RMAX, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_STAT_RMAX, var );         
            if (FAILED(hr))
            {
                goto done;
            }

            PropVariantClear( &var );
            hr = pEncoderProps->GetValue( MFPKEY_WMAENC_AVGBYTESPERSEC, &var );
            if (FAILED(hr))
            {
                goto done;
            }
            hr = pStreamSinkProps->SetValue( MFPKEY_WMAENC_AVGBYTESPERSEC, var );         
            if (FAILED(hr))
            {
                goto done;
            }
        } 
        PropVariantClear( &var ); 
   }
done:
    SafeRelease (&pOutputColl);
    SafeRelease (&pNodeUnk);
    SafeRelease (&pType);
    SafeRelease (&pNode);
    SafeRelease (&pSinkUnk);
    SafeRelease (&pStreamSink);
    SafeRelease (&pEncoderNode);
    SafeRelease (&pEncoderUnk);
    SafeRelease (&pEncoder);
    SafeRelease (&pStreamSinkProps);
    SafeRelease (&pEncoderProps);

    return hr;
   
}
```



## <a name="implement-main"></a>Implementieren von Main

Das folgende Codebeispiel zeigt die Hauptfunktion der Konsolenanwendung.


```C++
int wmain(int argc, wchar_t* argv[])
{
    HeapSetInformation(NULL, HeapEnableTerminationOnCorruption, NULL, 0);

    if (argc != 4)
    {
        wprintf_s(L"Usage: %s inputaudio.mp3, %s output.wm*, %Encoding Type: CBR, VBR\n");
        return 0;
    }


    HRESULT             hr = S_OK;

    IMFMediaSource* pSource = NULL;
    IMFTopology* pTopology = NULL;
    IMFActivate* pFileSinkActivate = NULL;

    hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED | COINIT_DISABLE_OLE1DDE);
    if (FAILED(hr))
    {
        goto done;
    }

    //Set the requested encoding mode
    if (wcscmp(argv[3], L"CBR")==0)
    {
        EncodingMode = CBR;
    }
    else if (wcscmp(argv[3], L"VBR")==0)
    {
        EncodingMode = VBR;
    }
    else
    {
        EncodingMode = CBR;
    }

    // Start up Media Foundation platform.
    hr = MFStartup(MF_VERSION);
    if (FAILED(hr))
    {
        goto done;
    }

    //Create the media source
    hr = CreateMediaSource(argv[1], &pSource);
    if (FAILED(hr))
    {
        goto done;
    }

    //Create the file sink activate
    hr = CreateMediaSink(argv[2], pSource, &pFileSinkActivate);
    if (FAILED(hr))
    {
        goto done;
    }

    //Build the encoding topology.
    hr = BuildPartialTopology(pSource, pFileSinkActivate, &pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

    //Instantiate the media session and start encoding
    hr = Encode(pTopology);
    if (FAILED(hr))
    {
        goto done;
    }


done:
    // Clean up.
    SafeRelease(&pSource);
    SafeRelease(&pTopology);
    SafeRelease(&pFileSinkActivate);

    MFShutdown();
    CoUninitialize();

    if (FAILED(hr))
    {
        wprintf_s(L"Could not create the output file due to 0x%X\n", hr);
    }
    return 0;
}
```



## <a name="test-the-output-file"></a>Testen der Ausgabedatei

In der folgenden Liste wird eine Checkliste zum Testen der codierten Datei beschrieben. Diese Werte können im Dialogfeld Dateieigenschaften aktiviert werden, das Sie anzeigen können, indem Sie mit der rechten Maustaste auf die codierte Datei klicken und im Kontextmenü **Eigenschaften** auswählen.

-   Der Pfad der codierten Datei ist richtig.
-   Die Größe der Datei beträgt mehr als 0 KB, und die Wiedergabedauer entspricht der Dauer der Quelldatei.
-   Überprüfen Sie für den Videostream die Rahmenbreite und-Höhe sowie die Framerate. Diese Werte sollten den Werten entsprechen, die Sie im ASF-Profil angegeben haben, das Sie in dem im Abschnitt "Erstellen des ASF-Profil Objekts" beschriebenen Schritt erstellt haben.
-   Für den Audiodatenstrom muss die Bitrate nahe dem Wert liegen, den Sie für den Ziel Medientyp angegeben haben.
-   Öffnen Sie die Datei in Windows Media Player, und überprüfen Sie die Qualität der Codierung.
-   Öffnen Sie die ASF-Datei in asfviewer, um die Struktur einer ASF-Datei anzuzeigen. Dieses Tool kann von dieser Microsoft- [Website](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=56de5ee4-51ca-46c6-903b-97390ad14fea)heruntergeladen werden.

## <a name="common-error-codes-and-debugging-tips"></a>Allgemeine Fehler Codes und Tipps zum Debuggen

In der folgenden Liste werden die allgemeinen Fehlercodes beschrieben, die möglicherweise von Ihrem empfangen werden.

-   Beim Aufrufen von [**imfsourceresolver:: forateobjectfromurl**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) wird die Anwendung angehalten.

    Stellen Sie sicher, dass Sie die Media Foundation-Plattform initialisiert haben, indem Sie [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup)aufrufen. Diese Funktion richtet die asynchrone Plattform ein, die von allen Methoden verwendet wird, die asynchrone Vorgänge starten, wie z. b. [**IMF sourceresolver:: forateobjectfromurl**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl), intern.

-   [**IMF sourceresolver:: forateobjectfromurl**](/windows/desktop/api/mfidl/nf-mfidl-imfsourceresolver-createobjectfromurl) gibt HRESULT 0x80070002 zurück. "das System kann die angegebene Datei nicht finden.

    Stellen Sie sicher, dass der vom Benutzer im ersten Argument angegebene Eingabe Dateiname vorhanden ist.

-   HRESULT 0x80070020 "der Prozess kann nicht auf die Datei zugreifen, da Sie von einem anderen Prozess verwendet wird. "

    Stellen Sie sicher, dass die Eingabe-und Ausgabedateien zurzeit nicht von einer anderen Ressource im System verwendet werden.

-   Aufrufe von [**imftransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) -Methoden geben MF \_ E \_ invalidmediatype zurück.

    Stellen Sie sicher, dass die folgenden Bedingungen erfüllt sind:

    -   Der Eingabetyp oder der Ausgabetyp, den Sie angegeben haben, ist mit den vom Encoder unterstützten Medientypen kompatibel.
    -   Die von Ihnen angegebenen Medientypen sind fertiggestellt. Weitere Informationen zu den Medientypen finden Sie im Abschnitt "Erstellen eines komprimierten audiomediums" und "Erstellen eines komprimierten Video Medientyps" in diesem Tutorial.
    -   Stellen Sie sicher, dass Sie die Zielbitrate für den partiellen Medientyp festgelegt haben, dem Sie die privaten Codec-Daten hinzufügen.

-   Die Medien Sitzung gibt den \_ \_ nicht unterstützten D3D-Typ von MF E \_ \_ im Ereignis Status zurück.

    Dieser Fehler wird zurückgegeben, wenn der Medientyp der Quelle einen gemischten damit-Modus angibt, der nicht von Windows Media Video Encoder unterstützt wird. Wenn Ihr komprimierter Video Medientyp für die Verwendung von progressivem Modus festgelegt ist, muss die Pipeline eine Deinterlacing-Transformation verwenden. Da die Pipeline keine Abgleich findet (Dies wird durch diesen Fehlercode angezeigt), müssen Sie manuell einen Deinterlacer (transcode-Videoprozessor) zwischen dem Decoder und den encoderknoten einfügen.

-   Die Medien Sitzung gibt E \_ invalidArg im Ereignis Status zurück.

    Dieser Fehler wird zurückgegeben, wenn die Medientyp Attribute der Quelle nicht mit den Attributen des auf dem Windows Media Encoder festgelegten Ausgabemedien Typs kompatibel sind.

-   [**Iwmcodecprivatedata:: getprivatedata**](../wmformat/iwmcodecprivatedata-getprivatedata.md) gibt HRESULT 0x80040203 "ein Syntax Fehler bei dem Versuch, eine Abfrage Zeichenfolge auszuwerten" zurück.

    Stellen Sie sicher, dass der Eingabetyp für den Encoder-MFT festgelegt ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Komponenten der Pipeline Schicht-ASF](pipeline-layer-asf-components.md)
</dt> </dl>

 

 
