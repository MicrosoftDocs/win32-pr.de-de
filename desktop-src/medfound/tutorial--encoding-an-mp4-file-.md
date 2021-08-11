---
description: In diesem Tutorial wird gezeigt, wie Sie die Transcode-API verwenden, um eine MP4-Datei mit H.264 für den Videostream und AAC für den Audiostream zu codieren.
ms.assetid: 60873aa6-46ec-4a73-94b9-0d8ac602f850
title: 'Tutorial: Codieren einer MP4-Datei'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 242777f04015f5444be5e0d8424ca06fc4b95cd84ca88c2b997d7b7466c734af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118237623"
---
# <a name="tutorial-encoding-an-mp4-file"></a>Tutorial: Codieren einer MP4-Datei

In diesem Tutorial wird gezeigt, wie Sie die [Transcode-API](transcode-api.md) verwenden, um eine MP4-Datei mit H.264 für den Videostream und AAC für den Audiostream zu codieren.

-   [Header und Bibliotheksdateien](#headers-and-library-files)
-   [Definieren der Codierungsprofile](#define-the-encoding-profiles)
-   [Schreiben der wmain-Funktion](#write-the-wmain-function)
-   [Codieren der Datei](#encode-the-file)
    -   [Erstellen der Medienquelle](#create-the-media-source)
    -   [Abrufen der Quelldauer](#get-the-source-duration)
    -   [Erstellen des Transcodierungsprofils](#create-the-transcode-profile)
    -   [Ausführen der Codierungssitzung](#run-the-encoding-session)
-   [Media Session Helper](#media-session-helper)
-   [Zugehörige Themen](#related-topics)

## <a name="headers-and-library-files"></a>Header und Bibliotheksdateien

Schließen Sie die folgenden Headerdateien ein.


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



## <a name="define-the-encoding-profiles"></a>Definieren der Codierungsprofile

Ein Ansatz für die Codierung besteht darin, eine Liste von Zielcodierungsprofilen zu definieren, die im Voraus bekannt sind. In diesem Tutorial verwenden wir einen relativ einfachen Ansatz und speichern eine Liste der Codierungsformate für H.264-Video- und AAC-Audio.

Für H.264 sind die wichtigsten Formatattribute das H.264-Profil, die Bildfrequenz, die Framegröße und die codierte Bitrate. Das folgende Array enthält eine Liste der H.264-Codierungsformate.


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



H.264-Profile werden mithilfe der [**eAVEncH264VProfile-Enumeration**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vprofile) angegeben. Sie können auch die H.264-Ebene angeben, aber der Microsoft Media Foundation [**H.264 Video Encoder**](h-264-video-encoder.md) kann die richtige Ebene für einen bestimmten Videostream ableiten. Daher wird empfohlen, die ausgewählte Ebene des Encoders nicht zu überschreiben. Für Interlacinginhalte würden Sie auch den Interlacemodus angeben (siehe [Video interlacing](video-interlacing.md)).

Bei AAC-Audiodaten sind die wichtigsten Formatattribute die Audioabtastrate, die Anzahl der Kanäle, die Anzahl der Bits pro Stichprobe und die codierte Bitrate. Optional können Sie die AAC-Audioprofilebenenanzeige festlegen. Weitere Informationen finden Sie unter [**AAC Encoder**](aac-encoder.md). Das folgende Array enthält eine Liste der AAC-Codierungsformate.


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
> Die `H264ProfileInfo` `AACProfileInfo` hier definierten Strukturen und sind nicht Teil der Media Foundation-API.

 

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



Die `wmain` Funktion führt folgende Schritte aus:

1.  Ruft die [**CoInitializeEx-Funktion**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializeex) auf, um die COM-Bibliothek zu initialisieren.
2.  Ruft die [**MFStartup-Funktion**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) auf, um Media Foundation zu initialisieren.
3.  Ruft die anwendungsdefinierte `EncodeFile` Funktion auf. Diese Funktion transcodiert die Eingabedatei in die Ausgabedatei und wird im nächsten Abschnitt angezeigt.
4.  Ruft die [**MFShutdown-Funktion**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) auf, um Media Foundation herunterzufahren.
5.  Rufen Sie die [**CoUninitialize-Funktion**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize) auf, um die Initialisierung der COM-Bibliothek zu aufheben.

## <a name="encode-the-file"></a>Codieren der Datei

Der folgende Code zeigt `EncodeFile` die -Funktion, die die Transcodierung ausführt. Diese Funktion besteht hauptsächlich aus Aufrufen anderer anwendungsdefinierter Funktionen, die weiter unten in diesem Thema gezeigt werden.


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



Die `EncodeFile` Funktion führt die folgenden Schritte aus.

1.  Erstellt eine Medienquelle für die Eingabedatei unter Verwendung der URL oder des Dateipfads der Eingabedatei. (Siehe [Erstellen der Medienquelle](#create-the-media-source).)
2.  Ruft die Dauer der Eingabedatei ab. (Siehe [Abrufen der Quelldauer](#get-the-source-duration).)
3.  Erstellen Sie das Transcodierungsprofil. (Weitere Informationen finden Sie unter [Erstellen des Transcodeprofils.)](#create-the-transcode-profile)
4.  Rufen Sie [**MFCreateTranscodeTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodetopology) auf, um die partielle Transcodierungstopologie zu erstellen.
5.  Erstellen Sie ein Hilfsobjekt, das die Mediensitzung verwaltet. (Weitere Informationen finden Sie unter Media Session Helper.)
6.  Führen Sie die Codierungssitzung aus, und warten Sie, bis sie abgeschlossen ist. (Siehe [Ausführen der Codierungssitzung](#run-the-encoding-session).)
7.  Rufen Sie [**ÜBERMEDIASOURCE::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) auf, um die Medienquelle herunterzufahren.
8.  Gibt Schnittstellenzeiger frei. Dieser Code verwendet die [SafeRelease-Funktion,](saferelease.md) um Schnittstellenzeiger freizugeben. Eine weitere Option ist die Verwendung einer intelligenten COM-Zeigerklasse, z. **B. CComPtr.**

### <a name="create-the-media-source"></a>Erstellen der Medienquelle

Die Medienquelle ist das Objekt, das die Eingabedatei liest und analysiert. Um die Medienquelle zu erstellen, übergeben Sie die URL der Eingabedatei an den [Quell resolver](source-resolver.md). Dies wird im folgenden Code veranschaulicht.


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



Weitere Informationen finden Sie unter [Verwenden des Quelllösers.](using-the-source-resolver.md)

### <a name="get-the-source-duration"></a>Abrufen der Quelldauer

Obwohl dies nicht erforderlich ist, ist es nützlich, die Medienquelle für die Dauer der Eingabedatei abzufragen. Dieser Wert kann verwendet werden, um den Codierungsfortschritt nachzuverfolgen. Die Dauer wird im [**MF \_ PD \_ DURATION-Attribut**](mf-pd-duration-attribute.md) des Präsentationsdeskriptors gespeichert. Rufen Sie den Präsentationsdeskriptor ab, indem Sie [**DENMEDIASource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor)aufrufen.


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



### <a name="create-the-transcode-profile"></a>Erstellen des Transcodierungsprofils

Das Transcodierungsprofil beschreibt die Codierungsparameter. Weitere Informationen zum Erstellen eines Transcodierungsprofils finden Sie unter [Verwenden der Transcodierungs-API.](fast-transcode-objects.md) Führen Sie die folgenden Schritte aus, um das Profil zu erstellen.

1.  Rufen Sie [**MFCreateTranscodeProfile**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodeprofile) auf, um das leere Profil zu erstellen.
2.  Erstellen Sie einen Medientyp für den AAC-Audiostream. Fügen Sie es dem Profil hinzu, indem Sie [**DIE DATEI ÜBERTRANSCODEProfile::SetAudioAttributes aufrufen.**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes)
3.  Erstellen Sie einen Medientyp für den H.264-Videostream. Fügen Sie es dem Profil hinzu, indem Sie [**ÜBERTRANSCODEProfile::SetVideoAttributes aufrufen.**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes)
4.  Rufen Sie [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) auf, um einen Attributspeicher für die Attribute auf Containerebene zu erstellen.
5.  Legen Sie das [MF \_ TRANSCODE \_ CONTAINERTYPE-Attribut](mf-transcode-containertype.md) fest. Dies ist das einzige erforderliche Attribut auf Containerebene. Legen Sie für die MP4-Dateiausgabe dieses Attribut auf **MFTranscodeContainerType \_ MPEG4** fest.
6.  Rufen Sie [**ÜBERTRANSCODEProfile::SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes) auf, um die Attribute auf Containerebene festzulegen.

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



Um die Attribute für den H.264-Videostream anzugeben, erstellen Sie einen Attributspeicher, und legen Sie die folgenden Attribute fest:



| attribute                                                       | Beschreibung                      |
|-----------------------------------------------------------------|---------------------------------|
| [**MF \_ \_ MT-UNTERTYP**](mf-mt-subtype-attribute.md)              | Legen Sie auf **MFVideoFormat \_ H264** fest. |
| [**MF \_ MT \_ \_ MPEG2-PROFIL**](mf-mt-mpeg2-profile-attribute.md) | H.264-Profil.                  |
| [**MF \_ MT \_ FRAME \_ SIZE**](mf-mt-frame-size-attribute.md)       | Framegröße.                     |
| [**MF \_ MT \_ FRAME \_ RATE**](mf-mt-frame-rate-attribute.md)       | Bildrate.                     |
| [**MF \_ MT \_ AVG \_ BITRATE**](mf-mt-avg-bitrate-attribute.md)     | Codierte Bitrate.               |



 

Um die Attribute für den AAC-Audiostream anzugeben, erstellen Sie einen Attributspeicher, und legen Sie die folgenden Attribute fest:



| attribute                                                                                      | Beschreibung                               |
|------------------------------------------------------------------------------------------------|------------------------------------------|
| [**MF \_ \_ MT-UNTERTYP**](mf-mt-subtype-attribute.md)                                             | Legen Sie auf **MFAudioFormat \_ AAC fest.**            |
| [**MF \_ \_ MT-AUDIOBEISPIELE \_ \_ PRO \_ SEKUNDE**](mf-mt-audio-samples-per-second-attribute.md)        | Rate der Audiostichproben.                       |
| [**MF \_ \_ MT-AUDIOBITS \_ \_ PRO \_ BEISPIEL**](mf-mt-audio-bits-per-sample-attribute.md)              | Bits pro Audiobeispiel.                   |
| [**MF \_ MT \_ AUDIO \_ NUM \_ CHANNELS**](mf-mt-audio-num-channels-attribute.md)                     | Anzahl der Audiokanäle.                |
| [**MF \_ MT \_ AUDIO \_ AVG \_ BYTES \_ PER \_ SECOND**](mf-mt-audio-avg-bytes-per-second-attribute.md)   | Codierte Bitrate.                        |
| [**MF MT AUDIO BLOCK ALIGNMENT (MF \_ \_ MT-AUDIOBLOCKAUSRICHTUNG) \_ \_**](mf-mt-audio-block-alignment-attribute.md)               | Auf 1 festlegen.                                |
| [MF \_ MT \_ AAC \_ AUDIO \_ PROFILE \_ LEVEL \_ INDICATION](mf-mt-aac-audio-profile-level-indication.md) | AAC-Profilebenenanzeige (optional). |



 

Der folgende Code erstellt die Videostreamattribute.


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



Der folgende Code erstellt die Audiostreamattribute.


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



Beachten Sie, dass die Transcodierungs-API keinen echten Medientyp erfordert, obwohl sie Medientypattribute verwendet. Insbesondere das [**MF \_ MT \_ MAJOR \_ TYPE-Attribut**](mf-mt-major-type-attribute.md) ist nicht erforderlich, da die [**Methoden SetVideoAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setvideoattributes) und [**SetAudioAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes) den Haupttyp implizieren. Es ist jedoch auch gültig, einen tatsächlichen Medientyp an diese Methoden zu übergeben. (Die [**BESCHRIFTUNGMediaType-Schnittstelle**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) [**erbt DIE ATTRIBUTE.)**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)

### <a name="run-the-encoding-session"></a>Ausführen der Codierungssitzung

Der folgende Code führt die Codierungssitzung aus. Es wird die Media Session-Hilfsklasse verwendet, die im nächsten Abschnitt gezeigt wird.


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



## <a name="media-session-helper"></a>Mediensitzungs-Hilfe

Die [Mediensitzung](media-session.md) wird im Abschnitt Media Foundation [Architektur](media-foundation-architecture.md) dieser Dokumentation genauer beschrieben. Die Mediensitzung verwendet ein asynchrones Ereignismodell. In einer GUI-Anwendung sollten Sie auf Sitzungsereignisse reagieren, ohne zu blockieren, dass der UI-Thread auf das nächste Ereignis wartet. Das Tutorial How to Play Unprotected Media Files (Wiedergeben von [ungeschützten Mediendateien)](how-to-play-unprotected-media-files.md) zeigt, wie Sie dies in einer Wiedergabeanwendung tun. Für die Codierung ist das Prinzip identisch, aber es sind weniger Ereignisse relevant:



| Ereignis                                  | Beschreibung                                                                                                                                                       |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [MESessionEnded](mesessionended.md)   | Wird ausgelöst, wenn die Codierung abgeschlossen ist.                                                                                                                            |
| [MESessionClosed](mesessionclosed.md) | Wird ausgelöst, [**wenn die METHODE FÜR DIE 100:000-000000000001**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) abgeschlossen ist. Nachdem dieses Ereignis ausgelöst wurde, ist es sicher, die Mediensitzung herunterfahren. |



 

Für eine Konsolenanwendung ist es sinnvoll, Ereignisse zu blockieren und auf diese zu warten. Je nach Quelldatei und Codierungseinstellungen kann es einige Zeit dauern, bis die Codierung abgeschlossen ist. Sie können Statusupdates wie folgt erhalten:

1.  Rufen [**Sie DIEMEDIASession::GetClock auf,**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-getclock) um die Präsentationsuhr zu erhalten.
2.  Fragen Sie die Uhr für die [**BENUTZEROBERFLÄCHEPresentationClock-Schnittstelle**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationclock) ab.
3.  Rufen [**Sie VORZEIGERDarstellungClock::GetTime auf,**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationclock-gettime) um die aktuelle Position zu erhalten.
4.  Die Position wird in Zeiteinheiten angegeben. Verwenden Sie den Wert , um den prozentsatz abgeschlossenen Wert zu `(100 * position) / duration` erhalten.

Hier ist die Deklaration der `CSession` -Klasse.


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



Der folgende Code zeigt die vollständige Implementierung der `CSession` -Klasse.


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

[**H.264 Video Encoder**](h-264-video-encoder.md)
</dt> <dt>

[Mediensitzung](media-session.md)
</dt> <dt>

[Medientypen](media-types.md)
</dt> <dt>

[Transcodierungs-API](transcode-api.md)
</dt> </dl>

 

 
