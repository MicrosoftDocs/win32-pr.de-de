---
description: In diesem Tutorial wird gezeigt, wie Sie die transcode-API verwenden, um eine Windows Media Audio-Datei (WMA) zu codieren.
ms.assetid: 2397ca78-edb5-4756-bd07-00529db28f76
title: 'Tutorial: Codieren einer WMA-Datei'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f491a9d460771dae91a49ab42982fbe97b24c42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106358813"
---
# <a name="tutorial-encoding-a-wma-file"></a>Tutorial: Codieren einer WMA-Datei

In diesem Tutorial wird gezeigt, wie Sie die [transcode-API](transcode-api.md) verwenden, um eine Windows Media Audio-Datei (WMA) zu codieren.

In diesem Tutorial wird der größte Teil des Codes aus dem Tutorial zum [Codieren einer MP4-Datei](tutorial--encoding-an-mp4-file-.md)wieder verwendet. Daher sollten Sie dieses Tutorial zuerst lesen. Der einzige Code, der sich unterscheidet, ist die-Funktion `CreateTranscodeProfile` , die das transcodieren-Profil erstellt.

## <a name="create-the-transcode-profile"></a>Erstellen des transcode-Profils

Ein *transcodieren-Profil* beschreibt die Codierungs Parameter und den Datei Container. Bei WMA handelt es sich bei dem Datei Container um eine ASF-Datei (Advanced Streaming Format). Die ASF-Datei enthält einen Audiostream, der mit dem [**Windows Media Audio Encoder**](windowsmediaaudioencoder.md)codiert wird.

Um die transcodieren-Topologie zu erstellen, erstellen Sie das transcodieren-Profil, und geben Sie die Parameter für den Audiodatenstrom und den Container an. Erstellen Sie dann die Topologie, indem Sie die Eingabe Quelle, die Ausgabe-URL und das transcodieren-Profil angeben.

Führen Sie die folgenden Schritte aus, um das Profil zu erstellen.

1.  Rufen Sie die Funktion [**mfkreatetranscodeprofile**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodeprofile) auf, um ein leeres transcodieren-Profil zu erstellen.
2.  Aufrufen von [**mftranscodegetaudiooutputavailabletypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes) zum Abrufen einer Liste von audiomedientyp aus dem Encoder. Diese Funktion gibt einen [**IMF Collection**](/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection) -Zeiger zurück, der eine Auflistung von [**IMF MediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) -Zeigern darstellt.
3.  Wählen Sie den audiomedientyp aus, der Ihren Transcodierungs Anforderungen entspricht, und kopieren Sie die Attribute in einen Attribut Speicher. In diesem Tutorial wird der erste Medientyp in der Liste verwendet.
    -   Wenn Sie [**imfcollection:: getElements**](/windows/desktop/api/mfobjects/nf-mfobjects-imfcollection-getelement) aufrufen, wählen Sie einen audiomedientyp aus der Liste aus.
    -   Fragen Sie den Medientyp ab, um einen Zeiger auf die [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Schnittstelle des Attribut Speicher des Medientyps zu erhalten.
    -   Aufrufen von [**imfattributes:: GetCount**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getcount) , um die Anzahl der Attribute zu erhalten, die im Medientyp enthalten sind.
    -   Rufen Sie [**mfkreateattributs**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) auf, um einen neuen Attribut Speicher zu erstellen.
    -   Nennen Sie [**imfattributes:: copyallitems**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-copyallitems) , um die Attribute aus dem Medientyp in den neuen Attribut Speicher zu kopieren.
4.  Wenn Sie [**imftranscodeprofile:: setaudioattribute**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes) aufrufen, legen Sie die Attribute für den Audiodatenstrom fest.
5.  Rufen Sie [**mfkreateattributs**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) auf, um einen Attribut Speicher für die Attribute auf Container Ebene zu erstellen.
6.  Legen Sie das Attribut [MF \_ transcode \_ ContainerType](mf-transcode-containertype.md) auf **mftranscodecontainertype \_ ASF** fest, das einen ASF-Datei Container angibt.
7.  Wenn Sie [**imftranscodeprofile:: setcontainerattribute**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes) aufrufen, legen Sie die Attribute auf Container Ebene für das Profil fest.


```C++
template <class Q>
HRESULT GetCollectionObject(IMFCollection *pCollection, DWORD index, Q **ppObj)
{
    IUnknown *pUnk;
    HRESULT hr = pCollection->GetElement(index, &pUnk);
    if (SUCCEEDED(hr))
    {
        hr = pUnk->QueryInterface(IID_PPV_ARGS(ppObj));
        pUnk->Release();
    }
    return hr;
}

HRESULT CreateTranscodeProfile(IMFTranscodeProfile **ppProfile)
{
    IMFTranscodeProfile *pProfile = NULL;     // Transcode profile.
    IMFCollection   *pAvailableTypes = NULL;  // List of audio media types.
    IMFMediaType    *pAudioType = NULL;       // Audio media type.
    IMFAttributes   *pAudioAttrs = NULL;      // Copy of the audio media type.
    IMFAttributes   *pContainer = NULL;       // Container attributes.

    DWORD dwMTCount = 0;
    
    // Create an empty transcode profile.
    HRESULT hr = MFCreateTranscodeProfile(&pProfile);
    if (FAILED(hr))
    {
        goto done;
    }

    // Get output media types for the Windows Media audio encoder.

    // Enumerate all codecs except for codecs with field-of-use restrictions.
    // Sort the results.

    DWORD dwFlags = 
        (MFT_ENUM_FLAG_ALL & (~MFT_ENUM_FLAG_FIELDOFUSE)) | 
        MFT_ENUM_FLAG_SORTANDFILTER;

    hr = MFTranscodeGetAudioOutputAvailableTypes(MFAudioFormat_WMAudioV9, 
        dwFlags, NULL, &pAvailableTypes);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pAvailableTypes->GetElementCount(&dwMTCount);
    if (FAILED(hr))
    {
        goto done;
    }
    if (dwMTCount == 0)
    {
        hr = E_FAIL;
        goto done;
    }

    // Get the first audio type in the collection and make a copy.
    hr = GetCollectionObject(pAvailableTypes, 0, &pAudioType);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = MFCreateAttributes(&pAudioAttrs, 0);       
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pAudioType->CopyAllItems(pAudioAttrs);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the audio attributes on the profile.
    hr = pProfile->SetAudioAttributes(pAudioAttrs);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the container attributes.
    hr = MFCreateAttributes(&pContainer, 1);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pContainer->SetGUID(MF_TRANSCODE_CONTAINERTYPE, MFTranscodeContainerType_ASF);
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
    SafeRelease(&pAvailableTypes);
    SafeRelease(&pAudioType);
    SafeRelease(&pAudioAttrs);
    SafeRelease(&pContainer);
    return hr;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Transcode-API](transcode-api.md)
</dt> </dl>

 

 



