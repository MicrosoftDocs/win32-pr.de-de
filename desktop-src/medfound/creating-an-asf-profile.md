---
description: In diesem Thema wird beschrieben, wie Sie in Microsoft Media Foundation als ASF-Profil erstellen.
ms.assetid: 9633bc88-12bd-404a-b779-878eb1ee5699
title: Erstellen eines ASF-Profils
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08ed9553811645b8589de7fb1805f1a307c4bdef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344018"
---
# <a name="creating-an-asf-profile"></a>Erstellen eines ASF-Profils

In diesem Thema wird beschrieben, wie Sie in Microsoft Media Foundation als ASF-Profil erstellen.

-   [Erstellen eines neuen Profils](#create-a-new-profile)
-   [Profil aus dem Objekt "ASF ContentInfo" erhalten](#get-the-profile-from-the-asf-contentinfo-object)
-   [Profil aus einem Präsentations Deskriptor abgerufen](#get-the-profile-from-a-presentation-descriptor)
-   [Zugehörige Themen](#related-topics)

## <a name="create-a-new-profile"></a>Erstellen eines neuen Profils

Um ein leeres ASF-Profil zu erstellen, rufen Sie die Funktion [**mfkreateasfprofile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile) auf. Diese Funktion gibt einen Zeiger auf die [**imfasfprofile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) -Schnittstelle zurück. Die Anwendung kann diese Schnittstelle verwenden, um Datenströme zum Profil hinzuzufügen und die einzelnen Streams zu konfigurieren. Weitere Informationen finden Sie unter [Erstellen und Konfigurieren von ASF-Streams](creating-and-configuring-asf-streams.md).

Optional kann die Anwendung zwei oder mehr Streams Objekte mit gegenseitigem Ausschluss hinzufügen. Siehe [Verwenden des gegenseitigen Ausschlusses für ASF-Streams](using-mutual-exclusion-for-asf-streams.md).

## <a name="get-the-profile-from-the-asf-contentinfo-object"></a>Profil aus dem Objekt "ASF ContentInfo" erhalten

Eine Anwendung kann das ASF-Profil einer vorhandenen ASF-Datei aus dem [Objekt "ASF ContentInfo](asf-contentinfo-object.md)" erhalten. Das Profil ist bereits konfiguriert und enthält Einstellungen für alle Streams in der Datei.

Initialisieren Sie das ContentInfo-Objekt, indem Sie das ASF-Header Objekt der Datei übernehmen. Dies erfolgt über die [**imfasf ContentInfo::P arsheader**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) -Methode. Nachdem alle Header Objekte gelesen und die ASF-Bibliothek aufgefüllt wurde, wird das Profil für diese Datei generiert. Die Anwendung kann einen Zeiger auf dieses initialisierte Profil abrufen, indem [**imfasfcontentinfo:: GetProfile**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile)aufgerufen wird.

## <a name="get-the-profile-from-a-presentation-descriptor"></a>Profil aus einem Präsentations Deskriptor abgerufen

Sie können das Profil Objekt einer vorhandenen ASF-Datei aus dem [Präsentations Deskriptor](presentation-descriptors.md) für die Datei oder aus dem Objekt " [ASF ContentInfo](asf-contentinfo-object.md) " erhalten. In diesem Fall ist das Profil bereits konfiguriert und enthält Einstellungen für alle Streams in der Datei. Dies kann hilfreich sein, wenn Sie ein vorhandenes ASF-Profil ändern möchten. Beispielsweise möchten Sie möglicherweise eine Windows Media Video Datei mit einer niedrigeren Bitrate erneut codieren.

Um das Profil aus dem Präsentations Deskriptor abzurufen, müssen Sie [**mfkreateasfprofilefrompresentationdescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofilefrompresentationdescriptor)aufrufen. Diese Funktion analysiert den Präsentations Deskriptor und füllt ein ASF-Profil mit Informationen über die Mediendatei. Die-Funktion gibt einen Zeiger auf die imfasfprofile-Schnittstelle zurück. Anschließend können Sie diese Schnittstelle verwenden, um das Profil zu ändern.

Um den Präsentations Deskriptor abzurufen, wenden Sie eine der folgenden Methoden an:

-   Nennen Sie aus der ASF-Medienquelle [**imfmediasource:: foratepresentationdescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor).
-   Nennen Sie aus dem Objekt " [ASF ContentInfo](asf-contentinfo-object.md) " [**imfasfcontentinfo:: generatepresentationdescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor). Stellen Sie vor dem Aufrufen dieser Methode sicher, dass das ContentInfo-Objekt zum Lesen initialisiert wird. Weitere Informationen finden Sie unter "Initialisieren des ContentInfo-Objekts aus einer vorhandenen ASF-Datei" beim [Lesen des ASF-Header Objekts einer vorhandenen Datei](reading-the-asf-header-object-of-an-existing-file.md). Wenn Sie jedoch bereits über ein initialisiertes ContentInfo-Objekt verfügen, können Sie das Profil direkt aus dem Objekt erhalten. Dies wird weiter unten in diesem Thema unter "erhalten des Profils aus dem ContentInfo-Objekt" beschrieben.

Im folgenden Beispiel wird gezeigt, wie ein Profil aus einem Präsentations Deskriptor erstellt wird. Die-Funktion erstellt eine Medienquelle für die Datei, Ruft den Präsentations Deskriptor aus der Medienquelle ab und erstellt ein Profil. In diesem Beispiel wird davon ausgegangen, dass *pszFileName* die URL einer ASF-Datei angibt.


```C++
HRESULT GetASFProfile(PCWSTR pszFileName, IMFASFProfile** ppProfile)
{
    *ppProfile = NULL;

    IMFSourceResolver* pResolver = NULL;
    IUnknown* pSourceUnk = NULL;
    IMFMediaSource* pSource = NULL;
    IMFPresentationDescriptor* pPD = NULL;

    // Create the source resolver.
    HRESULT hr = MFCreateSourceResolver(&pResolver);

    // Use the source resolver to create the media source.
    if (SUCCEEDED(hr))
    {
        MF_OBJECT_TYPE ObjectType;

        hr = pResolver->CreateObjectFromURL(
                pszFileName,
                MF_RESOLUTION_MEDIASOURCE, 
                NULL,                      
                &ObjectType,               
                &pSourceUnk   
            );
    }

    // Get the IMFMediaSource interface from the media source.
    if (SUCCEEDED(hr))
    {
        hr = pSourceUnk->QueryInterface(IID_PPV_ARGS(&pSource));
    }

    // Get the presentation desccriptor.
    if (SUCCEEDED(hr))
    {
        hr = pSource->CreatePresentationDescriptor(&pPD);
    }

    // Get the profile from the presentation descriptor.
    if (SUCCEEDED(hr))
    {
        hr = MFCreateASFProfileFromPresentationDescriptor(pPD, ppProfile);
    }

    SafeRelease(&pResolver);
    SafeRelease(&pSourceUnk);
    SafeRelease(&pSource);
    SafeRelease(&pPD);
    return hr;
}
```



In diesem Beispiel wird [saferelease](saferelease.md) verwendet, um Schnittstellen Zeiger freizugeben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ASF-Profil](asf-profile.md)
</dt> </dl>

 

 



