---
title: Die LaunchPage-Methode
description: Die LaunchPage-Methode
ms.assetid: f0f93535-5afc-4777-9188-5bbac63ddc6b
keywords:
- Windows Media Player-Plug-Ins, LaunchPage-Methode
- Plug-Ins, LaunchPage-Methode
- Benutzeroberflächen-Plug-Ins, LaunchPage-Methode
- UI-Plug-Ins, LaunchPage-Methode
- LaunchPage-Methode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11a22e1f4b136711a6f4336fbe54d6d90e4bb18b24a88645587311a0b4046f6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119762720"
---
# <a name="the-launchpage-method"></a>Die LaunchPage-Methode

Die LaunchPage-Methode stellt die primäre Funktionalität des Plug-Ins bereit, nämlich das Starten einer Suchseite, die Informationen über den Interpreten des medienbezogenen Elements enthält, das an die -Methode übergeben wird.

Diese Methode wird von der OnSearch-Methode mit dem aktuellen **Media-Objekt** aufgerufen.

Der folgende Code wird verwendet, um diese Methode zu implementieren:


```C++
void LaunchPage(IWMPMedia *pMedia)
{
    USES_CONVERSION;

    HRESULT hr;
    CComBSTR bstrType;
    CComBSTR bstrArtist;

    // Get the name of the artist.
    bstrType = _T("artist");
    hr = pMedia->getItemInfo(bstrType, &bstrArtist);
    if (SUCCEEDED(hr)) 
    {
        // Create the search URL.
        TCHAR szSearch[MAX_PATH];
        _stprintf_s(szSearch, MAX_PATH, _T("https://search.msn.com/results.asp?q=%s"), OLE2T(bstrArtist));
        CComBSTR bstrURL = szSearch;

        // Launch the search page.
        m_pPlugin->m_spCore->launchURL(bstrURL);
    }
    else
    {
        MessageBox(_T("Failed to get artist information from media."), _T("Warn"), MB_OK | MB_ICONWARNING);
    }
}

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Implementieren von CPluginWindow**](implementing-cpluginwindow.md)
</dt> </dl>

 

 




