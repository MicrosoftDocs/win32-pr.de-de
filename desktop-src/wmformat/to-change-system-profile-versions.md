---
title: So ändern Sie System Profil Versionen
description: So ändern Sie System Profil Versionen
ms.assetid: 66bf4041-47b5-41b4-abb4-eb08d05e3b28
keywords:
- Profile, System
- Systemprofile, Versionen
- Systemprofile, Ändern von Versionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 824e2b1cf4a43cef0e87daa461c6510a6672472d
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104314303"
---
# <a name="to-change-system-profile-versions"></a><span data-ttu-id="2b838-106">So ändern Sie System Profil Versionen</span><span class="sxs-lookup"><span data-stu-id="2b838-106">To Change System Profile Versions</span></span>

<span data-ttu-id="2b838-107">Wenn Sie ein Profil-Manager-Objekt erstellen, werden die Systemprofile analysiert.</span><span class="sxs-lookup"><span data-stu-id="2b838-107">Whenever you create a profile manager object, it parses the system profiles.</span></span> <span data-ttu-id="2b838-108">Sie können die Systemprofile mithilfe der [**iwmprofilemanager:: getsystemprofilecount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-getsystemprofilecount) -Methode und der [**iwmprofilemanager:: loadsystemprofile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadsystemprofile) -Methode durchlaufen, aber der Profil-Manager zählt und listet nur die Profile einer einzelnen Version gleichzeitig auf.</span><span class="sxs-lookup"><span data-stu-id="2b838-108">You can iterate through the system profiles using the [**IWMProfileManager::GetSystemProfileCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-getsystemprofilecount) and [**IWMProfileManager::LoadSystemProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadsystemprofile) methods, but the profile manager will count and list only the profiles of a single version at a time.</span></span> <span data-ttu-id="2b838-109">Wenn Sie diese Methode für die Suche nach Systemprofilen verwenden möchten, müssen Sie sicherstellen, dass der Profil-Manager die gewünschte Version behandelt.</span><span class="sxs-lookup"><span data-stu-id="2b838-109">If you want to use this method of finding system profiles, you need to ensure that the profile manger deals with the version you want.</span></span> <span data-ttu-id="2b838-110">Verwenden Sie die Methoden der [**IWMProfileManager2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager2) -Schnittstelle, um die vom Profil-Manager verwendete Systemprofil Version festzulegen und abzurufen.</span><span class="sxs-lookup"><span data-stu-id="2b838-110">Use the methods of the [**IWMProfileManager2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager2) interface to set and retrieve the system profile version used by the profile manager.</span></span>

<span data-ttu-id="2b838-111">Versionen werden mithilfe der Member des Enumerationstyps der [**WMT- \_ Version**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_version) angegeben.</span><span class="sxs-lookup"><span data-stu-id="2b838-111">Versions are specified using the members of the [**WMT\_VERSION**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_version) enumeration type.</span></span> <span data-ttu-id="2b838-112">Wenn Sie die Systemprofil Version auf WMT \_ ver \_ 9 0 festlegen \_ , wird der-Vorgang erfolgreich ausgeführt, aber die Anzahl der Systemprofile ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="2b838-112">If you set the system profile version to WMT\_VER\_9\_0, the call will succeed, but the system profile count will be zero.</span></span> <span data-ttu-id="2b838-113">Dies liegt daran, dass keine vordefinierten Systemprofile die Codecs Windows Media Audio und der Video 9-Serie verwenden.</span><span class="sxs-lookup"><span data-stu-id="2b838-113">This is because no predefined system profiles use the Windows Media Audio and Video 9 Series codecs.</span></span> <span data-ttu-id="2b838-114">Weitere Informationen zum Aktualisieren von Profilen für die Verwendung der neuesten Codecs finden Sie unter [wieder verwenden von streamkonfigurationen](reusing-stream-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="2b838-114">For more information about updating profiles to use the newest codecs, see [Reusing Stream Configurations](reusing-stream-configurations.md).</span></span>

<span data-ttu-id="2b838-115">Wenn Sie ein Systemprofil mit dem GUID-Bezeichner laden, spielt es keine Rolle, welche Systemprofil Version der Profil-Manager verwendet.</span><span class="sxs-lookup"><span data-stu-id="2b838-115">If you load a system profile by its GUID identifier, it does not matter which system profile version the profile manager is using.</span></span> <span data-ttu-id="2b838-116">Weitere Informationen zum Laden von Systemprofilen finden [Sie unter So laden Sie ein Systemprofil](to-load-a-system-profile.md).</span><span class="sxs-lookup"><span data-stu-id="2b838-116">For more information about loading system profiles, see [To Load a System Profile](to-load-a-system-profile.md).</span></span>

<span data-ttu-id="2b838-117">Der folgende Beispielcode zeigt, wie die Systemprofil Version festgelegt und abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="2b838-117">The following example code shows how to set and retrieve the system profile version.</span></span> <span data-ttu-id="2b838-118">In diesem Beispiel wird printf für die Konsolenausgabe verwendet, und es muss "stdio. h" eingeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="2b838-118">This example uses printf for console output and requires stdio.h to be included.</span></span> <span data-ttu-id="2b838-119">Weitere Informationen zur Verwendung dieses Codes finden Sie unter [Verwenden der Codebeispiele](using-the-code-examples.md).</span><span class="sxs-lookup"><span data-stu-id="2b838-119">For more information about using this code, see [Using the Code Examples](using-the-code-examples.md).</span></span>


```C++
int main(void)
{
    HRESULT hr = S_OK;

    IWMProfileManager*  pProfileMgr  = NULL;
    IWMProfileManager2* pProfileMgr2 = NULL;

    WMT_VERSION         profileVersion;

    // Initialize COM.
    hr = CoInitialize(NULL);
    if(FAILED(hr))
    {
        printf("Could not initialize COM.");
        return 0;
    }

    // Create a profile manager object.
    hr = WMCreateProfileManager(&pProfileMgr);
    if(FAILED(hr))
    {
        printf("Could not create a profile manager object.");
        return 0;
    }

    // Get the IWMProfileManager2 interface.
    hr = pProfileMgr->QueryInterface(IID_IWMProfileManager2, 
                                     (void**) &pProfileMgr2);
    if(FAILED(hr))
    {
        printf("Could not get the IWMProfileManager2 interface.");
        SAFE_RELEASE(pProfileMgr);
        return 0;
    }

    // Release the old interface.
    SAFE_RELEASE(pProfileMgr);

    // Get the current system profile version.
    hr = pProfileMgr2->GetSystemProfileVersion(&profileVersion);
    if(FAILED(hr))
    {
        printf("Could not retrieve profile version.");
        printf("\nError code: 0x%X\n", hr);
        SAFE_RELEASE(pProfileMgr2);
        return 0;
    }
    
    // Display the current version.
    printf("Current version: ");
    switch(profileVersion)
    {
    case WMT_VER_4_0:
        printf("WMT_VER_4_0\n");
        break;
    case WMT_VER_7_0:
        printf("WMT_VER_7_0\n");
        break;
    case WMT_VER_8_0:
        printf("WMT_VER_8_0\n");
        break;
    case WMT_VER_9_0:
        printf("WMT_VER_9_0\n");
        break;
    }

    // Set the system profile version to 8.
    profileVersion = WMT_VER_8_0;

    hr = pProfileMgr2->SetSystemProfileVersion(profileVersion);
    if(FAILED(hr))
    {
        printf("Could not change profile version.");
        printf("\nError code: 0x%X\n", hr);
        SAFE_RELEASE(pProfileMgr2);
        return 0;
    }

    // Print verification.
    printf("Successfully set version to ");
    switch(profileVersion)
    {
    case WMT_VER_4_0:
        printf("WMT_VER_4_0\n");
        break;
    case WMT_VER_7_0:
        printf("WMT_VER_7_0\n");
        break;
    case WMT_VER_8_0:
        printf("WMT_VER_8_0\n");
        break;
    case WMT_VER_9_0:
        printf("WMT_VER_9_0\n");
        break;
    }

    // Clean up.
    SAFE_RELEASE(pProfileMgr2);
}
```



## <a name="related-topics"></a><span data-ttu-id="2b838-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2b838-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2b838-121">**Verwenden von System Profilen**</span><span class="sxs-lookup"><span data-stu-id="2b838-121">**Using System Profiles**</span></span>](using-system-profiles.md)
</dt> </dl>

 

 




