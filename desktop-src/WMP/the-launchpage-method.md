---
title: Die LaunchPage-Methode
description: Die LaunchPage-Methode
ms.assetid: f0f93535-5afc-4777-9188-5bbac63ddc6b
keywords:
- Windows Media Player-Plug-ins, LaunchPage-Methode
- Plug-ins, LaunchPage-Methode
- Benutzerschnittstellen-Plug-ins, LaunchPage-Methode
- UI-Plug-ins, LaunchPage-Methode
- LaunchPage-Methode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f04974eba1ba5c86300de44acd2ba6e2920954f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037173"
---
# <a name="the-launchpage-method"></a><span data-ttu-id="f9ea4-108">Die LaunchPage-Methode</span><span class="sxs-lookup"><span data-stu-id="f9ea4-108">The LaunchPage Method</span></span>

<span data-ttu-id="f9ea4-109">Die LaunchPage-Methode stellt die primäre Funktionalität des Plug-Ins bereit, d. h., es wird eine Suchseite mit Informationen über den Künstler des Medien Elements gestartet, das an die-Methode übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="f9ea4-109">The LaunchPage method provides the primary functionality of the plug-in, which is to launch a search page containing information about the artist of the media item passed to the method.</span></span>

<span data-ttu-id="f9ea4-110">Diese Methode wird von der onSearch-Methode mit dem aktuellen **Medien** Objekt aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="f9ea4-110">This method is called by the OnSearch method using the current **Media** object.</span></span>

<span data-ttu-id="f9ea4-111">Der folgende Code wird verwendet, um diese Methode zu implementieren:</span><span class="sxs-lookup"><span data-stu-id="f9ea4-111">The following code is used to implement this method:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="f9ea4-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f9ea4-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f9ea4-113">**Implementieren von cpluginwindow**</span><span class="sxs-lookup"><span data-stu-id="f9ea4-113">**Implementing CPluginWindow**</span></span>](implementing-cpluginwindow.md)
</dt> </dl>

 

 




