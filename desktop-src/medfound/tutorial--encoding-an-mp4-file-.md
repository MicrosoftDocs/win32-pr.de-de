---
description: In diesem Tutorial wird gezeigt, wie Sie die transcode-API verwenden, um eine MP4-Datei mit H. 264 für den Videostream und AAC für den Audiostream zu codieren.
ms.assetid: 60873aa6-46ec-4a73-94b9-0d8ac602f850
title: 'Tutorial: Codieren einer MP4-Datei'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae895ef321b35f080bf946384ee32d83c2c539fd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215409"
---
# <a name="tutorial-encoding-an-mp4-file"></a>Tutorial: Codieren einer MP4-Datei

In diesem Tutorial wird gezeigt, wie Sie die [transcode-API](transcode-api.md) verwenden, um eine MP4-Datei mit H. 264 für den Videostream und AAC für den Audiostream zu codieren.

-   [Header und Bibliotheksdateien](#headers-and-library-files)
-   [Definieren der Codierungs profile](#define-the-encoding-profiles)
-   [Schreiben der wmain-Funktion](#write-the-wmain-function)
-   [Codieren der Datei](#encode-the-file)
    -   [Erstellen der Medienquelle](#create-the-media-source)
    -   [Quell Dauer erhalten](#get-the-source-duration)
    -   [Erstellen des transcode-Profils](#create-the-transcode-profile)
    -   [Ausführen der Codierungs Sitzung](#run-the-encoding-session)
-   [Hilfsprogramm für Medien Sitzung](#media-session-helper)
-   [Zugehörige Themen](#related-topics)

## <a name="headers-and-library-files"></a>Header und Bibliotheksdateien

Fügen Sie die folgenden Header Dateien ein.


```C++
#include <new>
#include <iostream>
#include <windows.h>
#include <mfapi.h>
#include <Mfidl.h>
#include <shlwapi.h>
```



Verknüpfen Sie die folgenden Bibliotheksdateien.


```C++
#pragma comment(lib, "mfplat")
#pragma comment(lib, "mf")
#pragma comment(lib, "mfuuid")
#pragma comment(lib, "shlwapi")
```



## <a name="define-the-encoding-profiles"></a>Definieren der Codierungs profile

Ein Codierungs Ansatz besteht darin, eine Liste von Ziel Codierungs Profilen zu definieren, die im Voraus bekannt sind. Für dieses Tutorial verwenden wir einen relativ einfachen Ansatz und speichern eine Liste von Codierungs Formaten für H. 264-Video und AAC-Audiodaten.

Bei h. 264 sind die wichtigsten Format Attribute das H. 264-Profil, die Framerate, die Frame Größe und die codierte Bitrate. Das folgende Array enthält eine Liste mit H. 264-Codierungs Formaten.


```C++
struct H264ProfileInfo
{
    UINT32  profile;
    MFRatio fps;
    MFRatio frame_size;
    UINT32  bitrate;
};

H264ProfileInfo h264_profiles[] = 
{
    { eAVEncH264VProfile_Base, { 15, 1 },       { 176, 144 },   128000 },
    { eAVEncH264VProfile_Base, { 15, 1 },       { 352, 288 },   384000 },
    { eAVEncH264VProfile_Base, { 30, 1 },       { 352, 288 },   384000 },
    { eAVEncH264VProfile_Base, { 29970, 1000 }, { 320, 240 },   528560 },
    { eAVEncH264VProfile_Base, { 15, 1 },       { 720, 576 },  4000000 },
    { eAVEncH264VProfile_Main, { 25, 1 },       { 720, 576 }, 10000000 },
    { eAVEncH264VProfile_Main, { 30, 1 },       { 352, 288 }, 10000000 },
};
```



H. 264-Profile werden mithilfe der [**eAVEncH264VProfile**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vprofile) -Enumeration angegeben. Sie können auch die H. 264-Ebene angeben, aber der Microsoft Media Foundation [**h. 264-Video Encoder**](h-264-video-encoder.md) kann die richtige Ebene für einen bestimmten Videostream ableiten. Daher wird empfohlen, die ausgewählte Ebene des Encoders nicht zu überschreiben. Beim Zeilen Sprung Inhalt würden Sie auch den damit-Modus angeben (siehe [Video-Interlacing](video-interlacing.md)).

Bei AAC-Audiodaten sind die wichtigsten Format Attribute die audiobeispielrate, die Anzahl der Kanäle, die Anzahl der Bits pro Sample und die codierte Bitrate. Optional können Sie die Anzeige der AAC-audioprofilebene festlegen. Weitere Informationen finden Sie unter [**AAC-Encoder**](aac-encoder.md). Das folgende Array enthält eine Liste mit AAC-Codierungs Formaten.


```C++
struct AACProfileInfo
{
    UINT32  samplesPerSec;
    UINT32  numChannels;
    UINT32  bitsPerSample;
    UINT32  bytesPerSec;
    UINT32  aacProfile;
};

AACProfileInfo aac_profiles[] = 
{
    { 96000, 2, 16, 24000, 0x29}, 
    { 48000, 2, 16, 24000, 0x29}, 
    { 44100, 2, 16, 16000, 0x29}, 
    { 44100, 2, 16, 12000, 0x29}, 
};
```



> [!Note]  
> Die `H264ProfileInfo` hier definierten-und- `AACProfileInfo` Strukturen sind nicht Teil der Media Foundation-API.

 

## <a name="write-the-wmain-function"></a>Schreiben der wmain-Funktion

Der folgende Code zeigt den Einstiegspunkt für die Konsolenanwendung.


```C++
int video_profile = 0;
int audio_profile = 0;

int wmain(int argc, wchar_t* argv[])
{
    HeapSetInformation(NULL, HeapEnableTerminationOnCorruption, NULL, 0);

    if (argc < 3 || argc > 5)
    {
        std::cout << "Usage:" << std::endl;
        std::cout << "input output [ audio_profile video_profile ]" << std::endl;
        return 1;
    }

    if (argc > 3)
    {
        audio_profile = _wtoi(argv[3]);
    }
    if (argc > 4)
    {
        video_profile = _wtoi(argv[4]);
    }

    HRESULT hr = CoInitializeEx(NULL, COINIT_APARTMENTTHREADED);
    if (SUCCEEDED(hr))
    {
        hr = MFStartup(MF_VERSION);
        if (SUCCEEDED(hr))
        {
            hr = EncodeFile(argv[1], argv[2]);
            MFShutdown();
        }
        CoUninitialize();
    }

    if (SUCCEEDED(hr))
    {
        std::cout << "Done." << std::endl;
    }
    else
    {
        std::cout << "Error: " << std::hex << hr << std::endl;
    }

    return 0;
}
```



Die `wmain` Funktion führt Folgendes aus:

1.  Ruft die [**CoInitializeEx**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) -Funktion auf, um die com-Bibliothek zu initialisieren.
2.  Ruft die [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) -Funktion auf, um Media Foundation zu initialisieren.
3.  Ruft die Anwendungs definierte `EncodeFile` Funktion auf. Diese Funktion versieht die Eingabedatei in die Ausgabedatei und wird im nächsten Abschnitt angezeigt.
4.  Ruft die [**mfshutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) -Funktion auf, um Media Foundation herunterzufahren.
5.  Um die Initialisierung der com-Bibliothek aufzurufen, können Sie die Funktion " [**count Initialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) "

## <a name="encode-the-file"></a>Codieren der Datei

Der folgende Code zeigt die- `EncodeFile` Funktion, die die Transcodierung ausführt. Diese Funktion besteht größtenteils aus Aufrufen von anderen Anwendungs definierten Funktionen, die weiter unten in diesem Thema angezeigt werden.


```C++
HRESULT EncodeFile(PCWSTR pszInput, PCWSTR pszOutput)
{
    IMFTranscodeProfile *pProfile = NULL;
    IMFMediaSource *pSource = NULL;
    IMFTopology *pTopology = NULL;
    CSession *pSession = NULL;

    MFTIME duration = 0;

    HRESULT hr = CreateMediaSource(pszInput, &pSource);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = GetSourceDuration(pSource, &duration);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = CreateTranscodeProfile(&pProfile);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = MFCreateTranscodeTopology(pSource, pszOutput, pProfile, &pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = CSession::Create(&pSession);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSession->StartEncodingSession(pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = RunEncodingSession(pSession, duration);

done:            
    if (pSource)
    {
        pSource->Shutdown();
    }

    SafeRelease(&pSession);
    SafeRelease(&pProfile);
    SafeRelease(&pSource);
    SafeRelease(&pTopology);
    return hr;
}
```



Die- `EncodeFile` Funktion führt die folgenden Schritte aus.

1.  Erstellt eine Medienquelle für die Eingabedatei, wobei die URL oder der Dateipfad der Eingabedatei verwendet wird. (Informationen hierzu finden Sie [unter Erstellen der Medienquelle](#create-the-media-source).)
2.  Ruft die Dauer der Eingabedatei ab. (Weitere Informationen finden [Sie unter Ermitteln der Quell Dauer](#get-the-source-duration).)
3.  Erstellen Sie das transcodieren-Profil. (Weitere Informationen finden Sie [unter Erstellen des transcode-Profils](#create-the-transcode-profile).)
4.  Rufen Sie [**mfkreatetranscodetopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodetopology) auf, um die partielle transcodetopologie zu erstellen.
5.  Erstellen Sie ein Hilfsobjekt, das die Medien Sitzung verwaltet. (Weitere Informationen finden Sie unter Media Session Helper).
6.  Führen Sie die Codierungs Sitzung aus, und warten Sie, bis Sie beendet ist (Siehe [Ausführen der Codierungs Sitzung](#run-the-encoding-session).)
7.  Wenden Sie [**imfmediasource:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) an, um die Medienquelle zu schließen.
8.  Releaseschnittstellenzeiger. Dieser Code verwendet die [saferelease](saferelease.md) -Funktion zum Freigeben von Schnittstellen Zeigern. Eine andere Möglichkeit ist die Verwendung einer intelligenten com-Zeiger Klasse, z. b. **CComPtr**.

### <a name="create-the-media-source"></a>Erstellen der Medienquelle

Die Medienquelle ist das Objekt, das die Eingabedatei liest und analysiert. Um die Medienquelle zu erstellen, übergeben Sie die URL der Eingabedatei an den [quellresolver](source-resolver.md). Dies wird im folgenden Code veranschaulicht.


```C++
HRESULT CreateMediaSource(PCWSTR pszURL, IMFMediaSource **ppSource)
{
    MF_OBJECT_TYPE ObjectType = MF_OBJECT_INVALID;

    IMFSourceResolver* pResolver = NULL;
    IUnknown* pSource = NULL;

    // Create the source resolver.
    HRESULT hr = MFCreateSourceResolver(&pResolver);
    if (FAILED(hr))
    {
        goto done;
    }

    // Use the source resolver to create the media source
    hr = pResolver->CreateObjectFromURL(pszURL, MF_RESOLUTION_MEDIASOURCE, 
        NULL, &ObjectType, &pSource);
    if (FAILED(hr))
    {
        goto done;
    }

    // Get the IMFMediaSource interface from the media source.
    hr = pSource->QueryInterface(IID_PPV_ARGS(ppSource));

done:
    SafeRelease(&pResolver);
    SafeRelease(&pSource);
    return hr;
}
```



Weitere Informationen finden Sie unter [using the Source Resolver](using-the-source-resolver.md).

### <a name="get-the-source-duration"></a>Quell Dauer erhalten

Obwohl es nicht erforderlich ist, ist es hilfreich, die Medienquelle für die Dauer der Eingabedatei abzufragen. Dieser Wert kann zum Nachverfolgen des Codierungs Fortschritts verwendet werden. Die Dauer wird im [**MF \_ PD \_ Duration**](mf-pd-duration-attribute.md) -Attribut des Präsentations Deskriptors gespeichert. Rufen Sie den Präsentations Deskriptor ab, indem Sie [**imfmediasource:: createpresentationdescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor)aufrufen.


```C++
HRESULT GetSourceDuration(IMFMediaSource *pSource, MFTIME *pDuration)
{
    *pDuration = 0;

    IMFPresentationDescriptor *pPD = NULL;

    HRESULT hr = pSource->CreatePresentationDescriptor(&pPD);
    if (SUCCEEDED(hr))
    {
        hr = pPD->GetUINT64(MF_PD_DURATION, (UINT64*)pDuration);
        pPD->Release();
    }
    return hr;
}
```



### <a name="create-the-transcode-profile"></a>Erstellen des transcode-Profils

Im transcodieren-Profil werden die Codierungs Parameter beschrieben. Weitere Informationen zum Erstellen eines transcodieren-Profils finden [Sie unter Verwenden der transcodieren-API](fast-transcode-objects.md). Führen Sie die folgenden Schritte aus, um das Profil zu erstellen.

1.  Rufen Sie [**mfkreatetranscodeprofile**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodeprofile) auf, um das leere Profil zu erstellen.
2.  Erstellen Sie einen Medientyp für den AAC-Audiodatenstrom. Fügen Sie Sie dem Profil hinzu, indem Sie [**imftranscodeprofile:: setaudioattribute**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes)aufrufen.
3.  Erstellen Sie einen Medientyp für den H. 264-Videostream. Fügen Sie Sie dem Profil hinzu, indem Sie [**imftranscodeprofile:: setvideoattribute**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes)aufrufen.
4.  Rufen Sie [**mfkreateattributs**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) auf, um einen Attribut Speicher für die Attribute auf Container Ebene zu erstellen.
5.  Legen Sie das Attribut " [MF \_ transcode \_ ContainerType](mf-transcode-containertype.md) " fest. Dies ist das einzige erforderliche Attribut auf Container Ebene. Legen Sie für die Ausgabe von MP4-Dateien dieses Attribut auf **mftranscodecontainertype \_ MPEG4** fest.
6.  Wenn Sie [**imftranscodeprofile:: setcontainerattribute**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes) aufrufen, legen Sie die Attribute auf Container Ebene fest.

Der folgende Code zeigt diese Schritte.


```C++
HRESULT CreateTranscodeProfile(IMFTranscodeProfile **ppProfile)
{
    IMFTranscodeProfile *pProfile = NULL;
    IMFAttributes *pAudio = NULL;
    IMFAttributes *pVideo = NULL;
    IMFAttributes *pContainer = NULL;

    HRESULT hr = MFCreateTranscodeProfile(&pProfile);
    if (FAILED(hr)) 
    {
        goto done;
    }

    // Audio attributes.
    hr = CreateAACProfile(audio_profile, &pAudio);
    if (FAILED(hr)) 
    {
        goto done;
    }

    hr = pProfile->SetAudioAttributes(pAudio);
    if (FAILED(hr)) 
    {
        goto done;
    }

    // Video attributes.
    hr = CreateH264Profile(video_profile, &pVideo);
    if (FAILED(hr)) 
    {
        goto done;
    }

    hr = pProfile->SetVideoAttributes(pVideo);
    if (FAILED(hr)) 
    {
        goto done;
    }

    // Container attributes.
    hr = MFCreateAttributes(&pContainer, 1);
    if (FAILED(hr)) 
    {
        goto done;
    }

    hr = pContainer->SetGUID(MF_TRANSCODE_CONTAINERTYPE, MFTranscodeContainerType_MPEG4);
    if (FAILED(hr)) 
    {
        goto done;
    }

    hr = pProfile->SetContainerAttributes(pContainer);
    if (FAILED(hr)) 
    {
        goto done;
    }

    *ppProfile = pProfile;
    (*ppProfile)->AddRef();

done:
    SafeRelease(&pProfile);
    SafeRelease(&pAudio);
    SafeRelease(&pVideo);
    SafeRelease(&pContainer);
    return hr;
}
```



Um die Attribute für den H. 264-Videostream anzugeben, erstellen Sie einen Attribut Speicher und legen die folgenden Attribute fest:



| Attribut                                                       | Beschreibung                      |
|-----------------------------------------------------------------|---------------------------------|
| [**MF- \_ MT- \_ Untertyp**](mf-mt-subtype-attribute.md)              | Legen Sie auf **mfvideoformat \_ H264** fest. |
| [**MF- \_ MT- \_ MPEG2- \_ Profil**](mf-mt-mpeg2-profile-attribute.md) | H. 264-Profil.                  |
| [**MF- \_ MT- \_ Frame \_ Größe**](mf-mt-frame-size-attribute.md)       | Frame Größe.                     |
| [**MF- \_ MT- \_ Frame \_ Rate**](mf-mt-frame-rate-attribute.md)       | Die Framerate.                     |
| [**MF-mittlere mittlere \_ \_ \_ Bitrate**](mf-mt-avg-bitrate-attribute.md)     | Codierte Bitrate.               |



 

Um die Attribute für den AAC-Audiostream anzugeben, erstellen Sie einen Attribut Speicher und legen die folgenden Attribute fest:



| Attribut                                                                                      | Beschreibung                               |
|------------------------------------------------------------------------------------------------|------------------------------------------|
| [**MF- \_ MT- \_ Untertyp**](mf-mt-subtype-attribute.md)                                             | Auf **mfaudioformat- \_ AAC** festlegen            |
| [**MF \_ \_ -MT- \_ Audiobeispiele \_ pro \_ Sekunde**](mf-mt-audio-samples-per-second-attribute.md)        | Audiobeispielrate.                       |
| [**MF \_ \_ -MT- \_ audiobits \_ pro \_ Beispiel**](mf-mt-audio-bits-per-sample-attribute.md)              | Bits pro Audiobeispiel.                   |
| [**MF \_ \_ -MT- \_ audionum- \_ Kanäle**](mf-mt-audio-num-channels-attribute.md)                     | Anzahl der Audiokanäle.                |
| [**MF \_ \_ -MT-audiodurchschn. \_ \_ Byte \_ pro \_ Sekunde**](mf-mt-audio-avg-bytes-per-second-attribute.md)   | Codierte Bitrate.                        |
| [**MF \_ \_ -MT- \_ Audioblock \_ Ausrichtung**](mf-mt-audio-block-alignment-attribute.md)               | Auf 1 festlegen.                                |
| [Anzeige der MF \_ \_ \_ -AAC- \_ \_ audioprofilebene \_](mf-mt-aac-audio-profile-level-indication.md) | Anzeige der AAC-Profil Ebene (optional). |



 

Mit dem folgenden Code werden die Videodaten Strom Attribute erstellt.


```C++
HRESULT CreateH264Profile(DWORD index, IMFAttributes **ppAttributes)
{
    if (index >= ARRAYSIZE(h264_profiles))
    {
        return E_INVALIDARG;
    }

    IMFAttributes *pAttributes = NULL;

    const H264ProfileInfo& profile = h264_profiles[index];

    HRESULT hr = MFCreateAttributes(&pAttributes, 5);
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetGUID(MF_MT_SUBTYPE, MFVideoFormat_H264);
    }
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(MF_MT_MPEG2_PROFILE, profile.profile);
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeSize(
            pAttributes, MF_MT_FRAME_SIZE, 
            profile.frame_size.Numerator, profile.frame_size.Numerator);
    }
    if (SUCCEEDED(hr))
    {
        hr = MFSetAttributeRatio(
            pAttributes, MF_MT_FRAME_RATE, 
            profile.fps.Numerator, profile.fps.Denominator);
    }
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(MF_MT_AVG_BITRATE, profile.bitrate);
    }
    if (SUCCEEDED(hr))
    {
        *ppAttributes = pAttributes;
        (*ppAttributes)->AddRef();
    }
    SafeRelease(&pAttributes);
    return hr;
}
```



Mit dem folgenden Code werden die audiostreamattribute erstellt.


```C++
HRESULT CreateAACProfile(DWORD index, IMFAttributes **ppAttributes)
{
    if (index >= ARRAYSIZE(h264_profiles))
    {
        return E_INVALIDARG;
    }

    const AACProfileInfo& profile = aac_profiles[index];

    IMFAttributes *pAttributes = NULL;

    HRESULT hr = MFCreateAttributes(&pAttributes, 7);
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetGUID(MF_MT_SUBTYPE, MFAudioFormat_AAC);
    }
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(
            MF_MT_AUDIO_BITS_PER_SAMPLE, profile.bitsPerSample);
    }
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(
            MF_MT_AUDIO_SAMPLES_PER_SECOND, profile.samplesPerSec);
    }
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(
            MF_MT_AUDIO_NUM_CHANNELS, profile.numChannels);
    }
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(
            MF_MT_AUDIO_AVG_BYTES_PER_SECOND, profile.bytesPerSec);
    }
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(MF_MT_AUDIO_BLOCK_ALIGNMENT, 1);
    }
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(
            MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION, profile.aacProfile);
    }
    if (SUCCEEDED(hr))
    {
        *ppAttributes = pAttributes;
        (*ppAttributes)->AddRef();
    }
    SafeRelease(&pAttributes);
    return hr;
}
```



Beachten Sie, dass die transcodieren-API keinen echten Medientyp erfordert, obwohl Sie Medientyp Attribute verwendet. Insbesondere das [**MF MT- \_ \_ \_ Haupttyp**](mf-mt-major-type-attribute.md) Attribut ist nicht erforderlich, da die [**setvideoattribute**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes) -Methode und die [**setaudioattribute**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes) -Methode den Haupttyp implizieren. Es ist jedoch auch gültig, einen tatsächlichen Medientyp an diese Methoden zu übergeben. (Die [**IMF MediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) -Schnittstelle erbt [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes).)

### <a name="run-the-encoding-session"></a>Ausführen der Codierungs Sitzung

Der folgende Code führt die Codierungs Sitzung aus. Dabei wird die Hilfsprogrammklasse für Medien Sitzungen verwendet, die im nächsten Abschnitt angezeigt wird.


```C++
HRESULT RunEncodingSession(CSession *pSession, MFTIME duration)
{
    const DWORD WAIT_PERIOD = 500;
    const int   UPDATE_INCR = 5;

    HRESULT hr = S_OK;
    MFTIME pos;
    LONGLONG prev = 0;
    while (1)
    {
        hr = pSession->Wait(WAIT_PERIOD);
        if (hr == E_PENDING)
        {
            hr = pSession->GetEncodingPosition(&pos);

            LONGLONG percent = (100 * pos) / duration ;
            if (percent >= prev + UPDATE_INCR)
            {
                std::cout << percent << "% .. ";  
                prev = percent;
            }
        }
        else
        {
            std::cout << std::endl;
            break;
        }
    }
    return hr;
}
```



## <a name="media-session-helper"></a>Hilfsprogramm für Medien Sitzung

Die [Medien Sitzung](media-session.md) wird vollständig im Abschnitt [Media Foundation-Architektur](media-foundation-architecture.md) dieser Dokumentation beschrieben. Die Medien Sitzung verwendet ein asynchrones Ereignis Modell. In einer GUI-Anwendung sollten Sie auf Sitzungs Ereignisse reagieren, ohne den UI-Thread zu blockieren, um auf das nächste Ereignis zu warten. Im Tutorial zum Wiedergeben [ungeschützter Mediendateien](how-to-play-unprotected-media-files.md) wird gezeigt, wie dies in einer Wiedergabe Anwendung durchzuführen ist. Bei der Codierung ist das Prinzip identisch, aber es sind weniger Ereignisse relevant:



| Ereignis                                  | Beschreibung                                                                                                                                                       |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Mesessionend](mesessionended.md)   | Wird ausgelöst, wenn die Codierung beendet ist.                                                                                                                            |
| [Mesessionclosed](mesessionclosed.md) | Wird ausgelöst, wenn die [**imfmediasession:: Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) -Methode abgeschlossen wird. Nachdem dieses Ereignis ausgelöst wurde, kann die Medien Sitzung sicher heruntergefahren werden. |



 

Bei einer Konsolenanwendung ist es sinnvoll, Ereignisse zu blockieren und auf Ereignisse zu warten. Abhängig von der Quelldatei und den Codierungs Einstellungen kann es eine Weile dauern, bis die Codierung beendet ist. Statusaktualisierungen können wie folgt angezeigt werden:

1.  Aufrufen von [**imfmediasession:: getclock**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getclock) zum Abrufen der Präsentations Uhr.
2.  Fragen Sie die Uhr nach der [**IMF presentationclock**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationclock) -Schnittstelle ab.
3.  [**Imfpresentationclock:: getTime**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-gettime) aufrufen, um die aktuelle Position zu erhalten.
4.  Die Position wird in Zeiteinheiten angegeben. Verwenden Sie den Wert, um den Prozentsatz der abgeschlossenen Werte zu erhalten `(100 * position) / duration` .

Hier ist die Deklaration der- `CSession` Klasse.


```C++
class CSession  : public IMFAsyncCallback 
{
public:
    static HRESULT Create(CSession **ppSession);

    // IUnknown methods
    STDMETHODIMP QueryInterface(REFIID riid, void** ppv);
    STDMETHODIMP_(ULONG) AddRef();
    STDMETHODIMP_(ULONG) Release();

    // IMFAsyncCallback methods
    STDMETHODIMP GetParameters(DWORD* pdwFlags, DWORD* pdwQueue)
    {
        // Implementation of this method is optional.
        return E_NOTIMPL;
    }
    STDMETHODIMP Invoke(IMFAsyncResult *pResult);

    // Other methods
    HRESULT StartEncodingSession(IMFTopology *pTopology);
    HRESULT GetEncodingPosition(MFTIME *pTime);
    HRESULT Wait(DWORD dwMsec);

private:
    CSession() : m_cRef(1), m_pSession(NULL), m_pClock(NULL), m_hrStatus(S_OK), m_hWaitEvent(NULL)
    {
    }
    virtual ~CSession()
    {
        if (m_pSession)
        {
            m_pSession->Shutdown();
        }

        SafeRelease(&m_pClock);
        SafeRelease(&m_pSession);
        CloseHandle(m_hWaitEvent);
    }

    HRESULT Initialize();

private:
    IMFMediaSession      *m_pSession;
    IMFPresentationClock *m_pClock;
    HRESULT m_hrStatus;
    HANDLE  m_hWaitEvent;
    long    m_cRef;
};
```



Der folgende Code zeigt die komplette Implementierung der- `CSession` Klasse.


```C++
HRESULT CSession::Create(CSession **ppSession)
{
    *ppSession = NULL;

    CSession *pSession = new (std::nothrow) CSession();
    if (pSession == NULL)
    {
        return E_OUTOFMEMORY;
    }

    HRESULT hr = pSession->Initialize();
    if (FAILED(hr))
    {
        pSession->Release();
        return hr;
    }
    *ppSession = pSession;
    return S_OK;
}

STDMETHODIMP CSession::QueryInterface(REFIID riid, void** ppv)
{
    static const QITAB qit[] = 
    {
        QITABENT(CSession, IMFAsyncCallback),
        { 0 }
    };
    return QISearch(this, qit, riid, ppv);
}

STDMETHODIMP_(ULONG) CSession::AddRef()
{
    return InterlockedIncrement(&m_cRef);
}

STDMETHODIMP_(ULONG) CSession::Release()
{
    long cRef = InterlockedDecrement(&m_cRef);
    if (cRef == 0)
    {
        delete this;
    }
    return cRef;
}

HRESULT CSession::Initialize()
{
    IMFClock *pClock = NULL;

    HRESULT hr = MFCreateMediaSession(NULL, &m_pSession);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = m_pSession->GetClock(&pClock);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pClock->QueryInterface(IID_PPV_ARGS(&m_pClock));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = m_pSession->BeginGetEvent(this, NULL);
    if (FAILED(hr))
    {
        goto done;
    }

    m_hWaitEvent = CreateEvent(NULL, FALSE, FALSE, NULL);  
    if (m_hWaitEvent == NULL)
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
    }
done:
    SafeRelease(&pClock);
    return hr;
}

// Implements IMFAsyncCallback::Invoke
STDMETHODIMP CSession::Invoke(IMFAsyncResult *pResult)
{
    IMFMediaEvent* pEvent = NULL;
    MediaEventType meType = MEUnknown;
    HRESULT hrStatus = S_OK;

    HRESULT hr = m_pSession->EndGetEvent(pResult, &pEvent);
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

    switch (meType)
    {
    case MESessionEnded:
        hr = m_pSession->Close();
        if (FAILED(hr))
        {
            goto done;
        }
        break;

    case MESessionClosed:
        SetEvent(m_hWaitEvent);
        break;
    }

    if (meType != MESessionClosed)
    {
        hr = m_pSession->BeginGetEvent(this, NULL);
    }

done:
    if (FAILED(hr))
    {
        m_hrStatus = hr;
        m_pSession->Close();
    }

    SafeRelease(&pEvent);
    return hr;
}

HRESULT CSession::StartEncodingSession(IMFTopology *pTopology)
{
    HRESULT hr = m_pSession->SetTopology(0, pTopology);
    if (SUCCEEDED(hr))
    {
        PROPVARIANT varStart;
        PropVariantClear(&varStart);
        hr = m_pSession->Start(&GUID_NULL, &varStart);
    }
    return hr;
}

HRESULT CSession::GetEncodingPosition(MFTIME *pTime)
{
    return m_pClock->GetTime(pTime);
}

HRESULT CSession::Wait(DWORD dwMsec)
{
    HRESULT hr = S_OK;

    DWORD dwTimeoutStatus = WaitForSingleObject(m_hWaitEvent, dwMsec);
    if (dwTimeoutStatus != WAIT_OBJECT_0)
    {
        hr = E_PENDING;
    }
    else
    {
        hr = m_hrStatus;
    }
    return hr;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**AAC-Encoder**](aac-encoder.md)
</dt> <dt>

[**H. 264-Video Encoder**](h-264-video-encoder.md)
</dt> <dt>

[Medien Sitzung](media-session.md)
</dt> <dt>

[Medientypen](media-types.md)
</dt> <dt>

[Transcode-API](transcode-api.md)
</dt> </dl>

 

 
