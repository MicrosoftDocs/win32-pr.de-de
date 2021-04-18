---
title: Arbeiten mit lokalisierten System Profilen
description: Arbeiten mit lokalisierten System Profilen
ms.assetid: d911baf6-0731-4f02-9001-d04464a03f56
keywords:
- Profile, System
- Systemprofile, lokalisiert
- Systemprofile, iwmprofilemanagerlanguage-Schnittstelle
- lokalisierte Systemprofile, Informationen zu
- Iwmprofilemanagerlanguage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd8c040d9804cd822b17e7caad8a8cfb5e5854c4
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "106341287"
---
# <a name="working-with-localized-system-profiles"></a>Arbeiten mit lokalisierten System Profilen

Das Windows Media-Format-SDK umfasst Systemprofile mit Namen und Beschreibungen in verschiedenen Sprachen. Die lokalisierten Systemprofile. PRX-Dateien werden im \[ Ordner SDKRoot \] \\ wmsdk \\ WMFSDK9 \\ localizedprofiles installiert. Wenn Sie mit den **iwmprofilemanagerlanguage** -Methoden auf eine bestimmte Datei zugreifen möchten, müssen Sie sie zusammen mit den anderen Systemprofil Dateien in das Stammverzeichnis des Systems verschieben. Eine Liste der lokalisierten Systemprofil Dateien finden Sie unter [lokalisierte Systemprofile](localized-system-profiles.md).

Sie können die Systemprofil Sprache mithilfe der Methoden der [**iwmprofilemanagerlanguage**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanagerlanguage) -Schnittstelle festlegen oder abrufen. Die Sprache wird als langid-Wert angegeben, der aus einer primären und einer sekundären sprach Kennung besteht. Der folgende Code veranschaulicht, wie die aktuelle Sprache abgerufen wird. Die Standardsprache ist US-Englisch (0x409). Weitere Informationen zur Verwendung dieses Codes finden Sie unter [Verwenden der Codebeispiele](using-the-code-examples.md).


```C++
HRESULT GetCurrentSystemProfileLanguage(IMWProfilManager* pProfileMgr)
{
    HRESULT hr = S_OK;

    IWMProfileManagerLanguage* pProfileMgrLang = NULL;

    // Get the profile manager language interface.
    hr = pProfileMgr->QueryInterface(IID_IWMProfileManagerLanguage,
                                     (void **) &pProfileMgrLang);
    if(FAILED(hr))
    {
        printf("Couldn't get IWMProfileManagerLanguage.\n");
        SAFE_RELEASE(pProfileMgrLang);
        return hr;
    }

    // Retrieve the current language (as a LANGID value)
    WORD wLangID = 0;
    hr = pProfileMgrLang->GetUserLanguageID(&wLangID);
    if(FAILED(hr))
    {
        printf("Could not get the current language.\n");
        SAFE_RELEASE(pProfileMgrLang);
        return hr;
    }

    printf("The current language ID is 0x%X\n", wLangID);

    SAFE_RELEASE(pProfileMgrLang);
    return S_OK;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Verwenden von System Profilen**](using-system-profiles.md)
</dt> </dl>

 

 




