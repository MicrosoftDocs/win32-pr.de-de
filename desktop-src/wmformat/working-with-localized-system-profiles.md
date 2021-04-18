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
# <a name="working-with-localized-system-profiles"></a><span data-ttu-id="817c5-108">Arbeiten mit lokalisierten System Profilen</span><span class="sxs-lookup"><span data-stu-id="817c5-108">Working with Localized System Profiles</span></span>

<span data-ttu-id="817c5-109">Das Windows Media-Format-SDK umfasst Systemprofile mit Namen und Beschreibungen in verschiedenen Sprachen.</span><span class="sxs-lookup"><span data-stu-id="817c5-109">The Windows Media Format SDK includes system profiles with names and descriptions in several languages.</span></span> <span data-ttu-id="817c5-110">Die lokalisierten Systemprofile. PRX-Dateien werden im \[ Ordner SDKRoot \] \\ wmsdk \\ WMFSDK9 \\ localizedprofiles installiert.</span><span class="sxs-lookup"><span data-stu-id="817c5-110">The localized system profile .prx files are installed into the \[SDKRoot\]\\WMSDK\\WMFSDK9\\LocalizedProfiles folder.</span></span> <span data-ttu-id="817c5-111">Wenn Sie mit den **iwmprofilemanagerlanguage** -Methoden auf eine bestimmte Datei zugreifen möchten, müssen Sie sie zusammen mit den anderen Systemprofil Dateien in das Stammverzeichnis des Systems verschieben.</span><span class="sxs-lookup"><span data-stu-id="817c5-111">To access a particular file with the **IWMProfileManagerLanguage** methods, you must move it into the system root directory along with the other system profile files.</span></span> <span data-ttu-id="817c5-112">Eine Liste der lokalisierten Systemprofil Dateien finden Sie unter [lokalisierte Systemprofile](localized-system-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="817c5-112">For a list of the localized system profile files, see [Localized System Profiles](localized-system-profiles.md).</span></span>

<span data-ttu-id="817c5-113">Sie können die Systemprofil Sprache mithilfe der Methoden der [**iwmprofilemanagerlanguage**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanagerlanguage) -Schnittstelle festlegen oder abrufen.</span><span class="sxs-lookup"><span data-stu-id="817c5-113">You can set or retrieve the system profile language using the methods of the [**IWMProfileManagerLanguage**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanagerlanguage) interface.</span></span> <span data-ttu-id="817c5-114">Die Sprache wird als langid-Wert angegeben, der aus einer primären und einer sekundären sprach Kennung besteht.</span><span class="sxs-lookup"><span data-stu-id="817c5-114">The language is specified as a LANGID value, which consists of a primary language identifier and a secondary language identifier.</span></span> <span data-ttu-id="817c5-115">Der folgende Code veranschaulicht, wie die aktuelle Sprache abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="817c5-115">The following code demonstrates how to retrieve the current language.</span></span> <span data-ttu-id="817c5-116">Die Standardsprache ist US-Englisch (0x409).</span><span class="sxs-lookup"><span data-stu-id="817c5-116">The default language is U.S. English (0x409).</span></span> <span data-ttu-id="817c5-117">Weitere Informationen zur Verwendung dieses Codes finden Sie unter [Verwenden der Codebeispiele](using-the-code-examples.md).</span><span class="sxs-lookup"><span data-stu-id="817c5-117">For more information about using this code, see [Using the Code Examples](using-the-code-examples.md).</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="817c5-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="817c5-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="817c5-119">**Verwenden von System Profilen**</span><span class="sxs-lookup"><span data-stu-id="817c5-119">**Using System Profiles**</span></span>](using-system-profiles.md)
</dt> </dl>

 

 




