---
description: In diesem Tutorial erfahren Sie, wie Sie mithilfe der Transcodierungs-API eine Windows WMA-Datei (Media Audio) codieren.
ms.assetid: 2397ca78-edb5-4756-bd07-00529db28f76
title: 'Tutorial: Codieren einer WMA-Datei'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86301f301bb4f39f6c9258ec3eacfdd1646af8e76791e2df37ae6bf7d8f89880
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972789"
---
# <a name="tutorial-encoding-a-wma-file"></a>Tutorial: Codieren einer WMA-Datei

In diesem Tutorial wird gezeigt, wie Sie die [Transcodierungs-API verwenden,](transcode-api.md) um eine Windows WMA-Datei (Media Audio) zu codieren.

In diesem Tutorial wird der größte Teil des Codes aus dem Tutorial Codieren einer [MP4-Datei](tutorial--encoding-an-mp4-file-.md)wiederverwendet, daher sollten Sie dieses Tutorial zuerst lesen. Der einzige Code, der sich unterscheidet, ist die Funktion `CreateTranscodeProfile` , die das Transcodierungsprofil erstellt.

## <a name="create-the-transcode-profile"></a>Erstellen des Transcodierungsprofils

Ein *Transcodierungsprofil* beschreibt die Codierungsparameter und den Dateicontainer. Für WMA ist der Dateicontainer eine ASF-Datei (Advanced Streaming Format). Die ASF-Datei enthält einen Audiostream, der mit dem Medienaudioencoder Windows [**codiert wird.**](windowsmediaaudioencoder.md)

Erstellen Sie zum Erstellen der Transcodierungstopologie das Transcodierungsprofil, und geben Sie die Parameter für den Audiostream und den Container an. Erstellen Sie dann die Topologie, indem Sie die Eingabequelle, die Ausgabe-URL und das Transcodierungsprofil angeben.

Führen Sie zum Erstellen des Profils die folgenden Schritte aus.

1.  Rufen Sie die [**MFCreateTranscodeProfile-Funktion auf,**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodeprofile) um ein leeres Transcodierungsprofil zu erstellen.
2.  Rufen [**Sie MFTranscodeGetAudioOutputAvailableTypes**](/windows/desktop/api/mfidl/nf-mfidl-mftranscodegetaudiooutputavailabletypes) auf, um eine Liste der Audiomedientypen vom Encoder zu erhalten. Diese Funktion gibt einen [**FALSECollection-Zeiger**](/windows/desktop/api/mfobjects/nn-mfobjects-imfcollection) zurück, der eine Auflistung von [**FALSEMediaType-Zeigern**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype) darstellt.
3.  Wählen Sie den Audiomedientyp aus, der Ihren Transcodierungsanforderungen entspricht, und kopieren Sie die Attribute in einen Attributspeicher. Für dieses Tutorial wird der erste Medientyp in der Liste verwendet.
    -   Rufen [**Sie DIE 1:0Collection::GetElement auf,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfcollection-getelement) um einen Audiomedientyp aus der Liste auszuwählen.
    -   Fragen Sie den Medientyp ab, um einen Zeiger auf die [**BENUTZERDEFINIERTEAttribute-Schnittstelle**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) des Attributspeichers des Medientyps zu erhalten.
    -   Rufen [**Sie DIE ATTRIBUTEs::GetCount auf,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getcount) um die Anzahl der Attribute im Medientyp zu erhalten.
    -   Rufen [**Sie MFCreateAttributes auf,**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) um einen neuen Attributspeicher zu erstellen.
    -   Rufen [**Sie DIE ATTRIBUTE::CopyAllItems**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-copyallitems) auf, um die Attribute aus dem Medientyp in den neuen Attributspeicher zu kopieren.
4.  Rufen [**Sie ZUM FESTLEGENTRANSCODEProfile::SetAudioAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setaudioattributes) auf, um die Attribute für den Audiostream fest.
5.  Rufen [**Sie MFCreateAttributes auf,**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) um einen Attributspeicher für die Attribute auf Containerebene zu erstellen.
6.  Legen Sie [das MF \_ TRANSCODE \_ CONTAINERTYPE-Attribut](mf-transcode-containertype.md) auf **MFTranscodeContainerType \_ ASF fest,** das einen ASF-Dateicontainer angibt.
7.  Rufen Sie ZUM Festlegen der Attribute auf Containerebene für das Profil [**DEN Wert FÜR DIETRANSCODEProfile::SetContainerAttributes**](/windows/desktop/api/mfidl/nf-mfidl-imftranscodeprofile-setcontainerattributes) auf.


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

[Transcodierungs-API](transcode-api.md)
</dt> </dl>

 

 



