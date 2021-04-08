---
title: Die onSearch-Methode
description: Die onSearch-Methode
ms.assetid: 709bb428-1a5e-4b8d-8622-5fcc816f0a1a
keywords:
- Windows Media Player-Plug-ins, onSearch-Methode
- Plug-ins, onSearch-Methode
- Benutzeroberflächen-Plug-ins, onSearch-Methode
- UI-Plug-ins, onSearch-Methode
- OnSearch-Methode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de5c33af434028e6ee72c757c8d71def0d4109fd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037071"
---
# <a name="the-onsearch-method"></a><span data-ttu-id="9b02b-108">Die onSearch-Methode</span><span class="sxs-lookup"><span data-stu-id="9b02b-108">The OnSearch Method</span></span>

<span data-ttu-id="9b02b-109">Die onSearch-Methode wird von Windows Media Player aufgerufen, wenn auf die **Such** Schaltfläche geklickt wird.</span><span class="sxs-lookup"><span data-stu-id="9b02b-109">The OnSearch method is called by Windows Media Player when the **Search** button is clicked.</span></span> <span data-ttu-id="9b02b-110">Diese Methode ruft das aktuelle **Medien** Objekt ab und übergibt es an die LaunchPage-Methode.</span><span class="sxs-lookup"><span data-stu-id="9b02b-110">This method retrieves the current **Media** object and passes it to the LaunchPage method.</span></span>

<span data-ttu-id="9b02b-111">Der folgende Code wird verwendet, um diese Methode zu implementieren:</span><span class="sxs-lookup"><span data-stu-id="9b02b-111">The following code is used to implement this method:</span></span>


```C++
LRESULT OnSearch(WORD wNotifyCode, WORD wID, HWND hwndCtl, BOOL& fHandled)
{
    HRESULT hr;
    CComPtr<IWMPMedia> spMedia;

    if( m_pPlugin && m_pPlugin->m_spCore )
    {
        // Get a pointer to the current media item.
        hr = m_pPlugin->m_spCore->get_currentMedia(&spMedia);
        if (SUCCEEDED(hr) && spMedia)
        {
            LaunchPage(spMedia);
        }
    else
        {
            MessageBox(_T("There is no media loaded."), _T("Warn"), MB_OK | MB_ICONWARNING);
        }
    }
    return 0;
}

```



## <a name="related-topics"></a><span data-ttu-id="9b02b-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9b02b-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b02b-113">**Implementieren von cpluginwindow**</span><span class="sxs-lookup"><span data-stu-id="9b02b-113">**Implementing CPluginWindow**</span></span>](implementing-cpluginwindow.md)
</dt> </dl>

 

 




