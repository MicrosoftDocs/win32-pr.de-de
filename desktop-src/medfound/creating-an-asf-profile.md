---
description: In diesem Thema wird beschrieben, wie Sie ein ASF-Profil in Microsoft Media Foundation.
ms.assetid: 9633bc88-12bd-404a-b779-878eb1ee5699
title: Erstellen eines ASF-Profils
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80a0225a6ff17f68c5443fce15f9bdc196901313ccaaebdde2f7f34c49860538
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118743247"
---
# <a name="creating-an-asf-profile"></a>Erstellen eines ASF-Profils

In diesem Thema wird beschrieben, wie Sie ein ASF-Profil in Microsoft Media Foundation.

-   [Erstellen eines neuen Profils](#create-a-new-profile)
-   [Das Profil aus dem ASF ContentInfo-Objekt](#get-the-profile-from-the-asf-contentinfo-object)
-   [Get the Profile from a Presentation Descriptor](#get-the-profile-from-a-presentation-descriptor)
-   [Zugehörige Themen](#related-topics)

## <a name="create-a-new-profile"></a>Erstellen eines neuen Profils

Um ein leeres ASF-Profil zu erstellen, rufen Sie die [**MFCreateASFProfile-Funktion**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofile) auf. Diese Funktion gibt einen Zeiger auf die [**IMFASFProfile-Schnittstelle**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile) zurück. Die Anwendung kann diese Schnittstelle verwenden, um dem Profil Streams hinzuzufügen und die einzelnen Streams zu konfigurieren. Weitere Informationen finden Sie unter [Erstellen und Konfigurieren von ASF-Streams](creating-and-configuring-asf-streams.md).

Optional kann die Anwendung zwei oder mehr Streams Objekte für gegenseitigen Ausschluss hinzufügen. Weitere Informationen [finden Sie unter Using Mutual Exclusion for ASF Streams](using-mutual-exclusion-for-asf-streams.md).

## <a name="get-the-profile-from-the-asf-contentinfo-object"></a>Das Profil aus dem ASF ContentInfo-Objekt

Eine Anwendung kann das ASF-Profil einer vorhandenen ASF-Datei aus dem [ASF ContentInfo-Objekt erhalten.](asf-contentinfo-object.md) Das Profil ist bereits konfiguriert und enthält Einstellungen für alle Streams in der Datei.

Initialisieren Sie das ContentInfo-Objekt durch Analyse des ASF-Headerobjekts der Datei. Dies erfolgt über die [**IMFASFContentInfo::P arseHeader-Methode.**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-parseheader) Nachdem alle Headerobjekte gelesen und die ASF-Bibliothek aufgefüllt wurde, wird das Profil für diese Datei generiert. Die Anwendung kann einen Zeiger auf dieses initialisierte Profil erhalten, indem [**sie IMFASFContentInfo::GetProfile aufruft.**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-getprofile)

## <a name="get-the-profile-from-a-presentation-descriptor"></a>Get the Profile from a Presentation Descriptor

Sie können das Profilobjekt einer vorhandenen ASF-Datei aus dem [Präsentationsdeskriptor](presentation-descriptors.md) für die Datei oder aus dem [ASF ContentInfo-Objekt](asf-contentinfo-object.md) erhalten. In diesem Fall ist das Profil bereits konfiguriert und enthält Einstellungen für alle Streams in der Datei. Dies kann nützlich sein, wenn Sie ein vorhandenes ASF-Profil ändern möchten. Beispielsweise können Sie eine Medienvideodatei mit einer niedrigeren Bitrate Windows codieren.

Rufen Sie [**MFCreateASFProfileFromPresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfprofilefrompresentationdescriptor)auf, um das Profil aus dem Präsentationsdeskriptor zu erhalten. Diese Funktion analysiert den Präsentationsdeskriptor und füllt ein ASF-Profil mit Informationen zur Mediendatei auf. Die Funktion gibt einen Zeiger auf die IMFASFProfile-Schnittstelle zurück. Sie können diese Schnittstelle dann verwenden, um das Profil zu ändern.

Rufen Sie eine der folgenden Methoden auf, um den Präsentationsdeskriptor zu erhalten:

-   Rufen Sie in der ASF-Medienquelle [**DEN AUFRUF VON DER MEDIENQUELLE::CreatePresentationDescriptor auf.**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor)
-   Rufen Sie [im ASF ContentInfo-Objekt](asf-contentinfo-object.md) [**IMFASFContentInfo::GeneratePresentationDescriptor auf.**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor) Stellen Sie vor dem Aufrufen dieser Methode sicher, dass das ContentInfo-Objekt zum Lesen initialisiert ist. Weitere Informationen finden Sie unter "Initialisieren des ContentInfo-Objekts aus einer vorhandenen ASF-Datei" unter Lesen des [ASF-Headerobjekts einer vorhandenen Datei.](reading-the-asf-header-object-of-an-existing-file.md) Wenn Sie jedoch bereits über ein initialisiertes ContentInfo-Objekt verfügen, können Sie das Profil direkt daraus erhalten. Dies wird weiter unten in diesem Thema unter "Abrufen des Profils aus dem ContentInfo-Objekt" beschrieben.

Das folgende Beispiel zeigt, wie Sie ein Profil aus einem Präsentationsdeskriptor erstellen. Die Funktion erstellt eine Medienquelle für die Datei, ruft den Präsentationsdeskriptor aus der Medienquelle ab und erstellt ein Profil. In diesem Beispiel wird davon ausgegangen, *dass pszFileName* die URL einer ASF-Datei angibt.


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



In diesem Beispiel wird [SafeRelease verwendet,](saferelease.md) um Schnittstellenzeigende frei zu geben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ASF-Profil](asf-profile.md)
</dt> </dl>

 

 



