---
title: Verwenden des gegenseitigen Ausschlusses der Mehrfachbitrate
description: Verwenden des gegenseitigen Ausschlusses der Mehrfachbitrate
ms.assetid: 69898b4d-fe10-422e-9ed2-87b65aa7bdb3
keywords:
- Multiple Bit Rate (MBR), gegenseitigen Ausschluss
- MBR (Multiple Bit Rate), gegenseitiger Ausschluss
- Gegenseitiger Ausschluss,Multiple-Bit-Rate (MBR)
- Profile,Multiple Bit Rate (MBR)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c31c7954f6aa5098f6cc221a7a761428ff15fd6a4c2c0a6e5c8cea2b6622a84b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119446970"
---
# <a name="using-multiple-bit-rate-mutual-exclusion"></a>Verwenden des gegenseitigen Ausschlusses der Mehrfachbitrate

Der gegenseitige Ausschluss mit mehrfacher Bitrate (Multiple Bit Rate, MBR) ist nützlich, wenn Sie Inhalte für eine Vielzahl von Wiedergabeszenarien codieren möchten. Eine MBR-Videoausgabe besteht aus einer einzelnen Eingabe, die mehrmals codiert ist und die jeweils unterschiedliche Einstellungen für die Bitrate haben. Wenn eine Datei mit MBR-Codierung gelesen wird, bestimmt der Reader basierend auf der verfügbaren Bandbreite, welcher Stream verwendet werden soll.

Das Windows Media Format SDK unterstützt die MBR-Codierung für Video- und Audiostreams. Darüber hinaus können Sie einen speziellen MbR-Codierungstyp erstellen, der MBR-Codierung mit mehreren Videogrößen genannt wird. MBR-Videofunktionen mit mehreren Videogrößen funktionieren identisch mit normalem MBR-Video, mit der Ausnahme, dass Sie unterschiedliche Bildgrößen für die Videostreams beim gegenseitigen Ausschluss angeben können.

Im folgenden Beispiel wird veranschaulicht, wie Sie ein Profil für MBR-Videos mit mehreren Videogrößen einrichten. Es erstellt ein neues Profil mit drei Videostreams mit unterschiedlichen Bitraten und Größen und schließt sie in ein Objekt für gegenseitigen Ausschluss ein.


```C++
IWMProfileManager*  pProfileMgr = NULL;
IWMProfile*         pProfile    = NULL;
IWMMutualExclusion* pMutex      = NULL;
IWMStreamConfig*    pStream     = NULL;
IWMMediaProps*      pMediaProps = NULL;

WM_MEDIA_TYPE*      pMediaType  = NULL;
DWORD               cbMediaType = 0;

HRESULT hr = S_OK;

// Initialize COM.
hr = CoInitialize(NULL);

// Create a profile manager object.
hr = WMCreateProfileManager(&pProfileMgr);

// Create an empty profile.
hr = pProfileMgr->CreateEmptyProfile(WMT_VER_9_0, &pProfile);

// Give the new profile a name and description.
hr = pProfile->SetName(L"MBR_Video_3_Stream_test");
hr = pProfile->SetDescription(L"Only for use with example code.");

// Create the first stream.
hr = pProfile->CreateNewStream(WMMEDIATYPE_Video, &pStream);

// Get the media properties interface for the new stream.
hr = pStream->QueryInterface(IID_IWMMediaProps, (void**)&pMediaProps);

// Get the media-type structure.
// First, get the size of the media-type structure.
hr = pMediaProps->GetMediaType(NULL, &cbMediaType);

// Allocate memory for the structure based on the retrieved size.
pMediaType = (WM_MEDIA_TYPE*) new BYTE[cbMediaType];

// Retrieve the media-type structure.
hr = pMediaProps->GetMediaType(pMediaType, &cbMediaType);

// Change the video size to 640 x 480.
pMediaType->pbFormat->bmiHeader.biWidth  = 640;
pMediaType->pbFormat->bmiHeader.biHeight = 480;

// Replace the WM_MEDIA_TYPE in the profile with the one just changed.
hr = pMediaProps->SetMediaType(pMediaType);

// Release the media properties interface and delete the structure.
pMediaProps->Release();
pMediaProps = NULL;
delete[] pMediaType;
pMediaType = NULL;

// Set the bit rate to 200.
hr = pStream->SetBitrate(200000);

// Set the stream number.
hr = pStream->SetStreamNumber(1);

// Include the new stream in the profile.
hr = pProfile->AddStream(pStream);

// Release the stream configuration interface.
pStream->Release();
pStream = NULL;

// For the remaining two streams, leave the video at its default size of
// 320 x 240 <entity type="ndash"/>- just change the bit rates.

// Repeat for a 100K stream.
hr = pProfile->CreateNewStream(WMMEDIATYPE_Video, &pStream);
hr = pStream->SetBitrate(100000);
hr = pStream->SetStreamNumber(2);
hr = pProfile->AddStream(pStream);
pStream->Release();
pStream = NULL;

// Repeat for a 56K stream.
hr = pProfile->CreateNewStream(WMMEDIATYPE_Video, &pStream);
hr = pStream->SetBitrate(56000);
hr = pStream->SetStreamNumber(3);
hr = pProfile->AddStream(pStream);
pStream->Release();
pStream = NULL;

// Now that we have three streams, create a mutual exclusion object.
hr = pProfile->CreateNewMutualExclusion(&pMutex);

// Add the three streams to the mutual exclusion.
hr = pMutex->AddStream(1);
hr = pMutex->AddStream(2);
hr = pMutex->AddStream(3);

// Configure the mutual exclusion for MBR video.
hr = pMutex->SetType(CLSID_WMMUTEX_Bitrate);

// Add the mutual exclusion to the profile.
hr = pProfile->AddMutualExclusion(pMutex);

// Release the mutual exclusion object.
pMutex->Release();
pMutex = NULL;

// TODO: Save the profile to a string, and save the string to a file.
// For more information, see To Save a Custom Profile.

// Release remaining interfaces.
pProfile->Release();
pProfile = NULL;

pProfileMgr->Release();
pProfileMgr = NULL;
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IWMMediaProps-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)
</dt> <dt>

[**IWMMutualExclusion-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion)
</dt> <dt>

[**IWMProfile-Schnittstelle**](iwmprofile.md)
</dt> <dt>

[**IWMStreamConfig-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig)
</dt> <dt>

[**Verwenden des gegenseitigen Ausschlusses**](using-mutual-exclusion.md)
</dt> <dt>

[**\_ \_ WM-MEDIENTYP**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type)
</dt> </dl>

 

 




