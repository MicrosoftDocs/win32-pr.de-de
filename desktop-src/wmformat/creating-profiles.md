---
title: Erstellen von Profilen
description: Erstellen von Profilen
ms.assetid: af4a8efe-d797-4d19-961d-b917e4c7c81a
keywords:
- Windows Media-Format-SDK, profile
- Profile, erstellen
- Profile, iwmprofilemanager-Schnittstelle
- Iwmprofilemanager, Erstellen von Profilen
- Profile, wmkreateprofilemanager-Funktion
- Wmkreateprofilemanager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45eeca9e99e09bd709b7e9fdf1aeffe8d35ca14a
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104038527"
---
# <a name="creating-profiles"></a><span data-ttu-id="28253-109">Erstellen von Profilen</span><span class="sxs-lookup"><span data-stu-id="28253-109">Creating Profiles</span></span>

<span data-ttu-id="28253-110">In vielen Fällen empfiehlt es sich, ein leeres Profil zu erstellen, das für Ihre Anforderungen konfiguriert werden kann.</span><span class="sxs-lookup"><span data-stu-id="28253-110">In many cases, you will want to create an empty profile to configure for your needs.</span></span> <span data-ttu-id="28253-111">In anderen Fällen ist es einfacher, ein vorhandenes Profil zu bearbeiten, wie z. b. ein Systemprofil.</span><span class="sxs-lookup"><span data-stu-id="28253-111">In other cases it is easier to edit an existing profile, like a system profile.</span></span> <span data-ttu-id="28253-112">Weitere Informationen zum Verwenden von Systemprofilen finden Sie unter [Verwenden von Systemprofilen](using-system-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="28253-112">For more information about using system profiles, see [Using System Profiles](using-system-profiles.md).</span></span>

<span data-ttu-id="28253-113">Wenn Sie ein leeres Profil erstellen, das Sie für die Konfiguration bereit haben, ist ein Profil-Manager-Objekt erforderlich.</span><span class="sxs-lookup"><span data-stu-id="28253-113">Creating an empty profile, ready for you to configure, requires a profile manager object.</span></span> <span data-ttu-id="28253-114">Um die [**iwmprofilemanager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) -Schnittstelle eines Profil-Manager-Objekts abzurufen, müssen Sie die [**wmkreateprofilemanager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="28253-114">To get the [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) interface of a profile manager object, call the [**WMCreateProfileManager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) function.</span></span>

<span data-ttu-id="28253-115">Um ein leeres Profil zu erstellen, rufen Sie [**iwmprofilemanager:: kreateemptyprofile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-createemptyprofile)auf.</span><span class="sxs-lookup"><span data-stu-id="28253-115">To create an empty profile, call [**IWMProfileManager::CreateEmptyProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-createemptyprofile).</span></span> <span data-ttu-id="28253-116">Wenn Sie ein leeres Profil erstellen, ist das einzige, was Sie angeben, die Version des Windows Media-Format-SDKs, dem das Profil entspricht.</span><span class="sxs-lookup"><span data-stu-id="28253-116">When you create an empty profile, the only thing you specify is the version of the Windows Media Format SDK with which the profile complies.</span></span> <span data-ttu-id="28253-117">Sie sollten immer die neueste Version verwenden, es sei denn, Sie müssen eine frühere Version verwenden.</span><span class="sxs-lookup"><span data-stu-id="28253-117">Unless you have a specific need to use a previous version, you should always use the latest version.</span></span> <span data-ttu-id="28253-118">Die-Version bestimmt die Struktur des Profils. in früheren Versionen wurden einige Eigenschaften nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="28253-118">The version dictates the structure of the profile; previous versions did not support some properties.</span></span>

<span data-ttu-id="28253-119">Der folgende Beispielcode zeigt, wie Sie ein neues Profil erstellen.</span><span class="sxs-lookup"><span data-stu-id="28253-119">The following example code shows how to create a new profile.</span></span> <span data-ttu-id="28253-120">Um diesen Code in der Anwendung zu kompilieren, fügen Sie stdio. h ein.</span><span class="sxs-lookup"><span data-stu-id="28253-120">To compile this code in your application, include stdio.h.</span></span> <span data-ttu-id="28253-121">Weitere Informationen zur Verwendung dieses Codes finden Sie unter [Verwenden der Codebeispiele](using-the-code-examples.md).</span><span class="sxs-lookup"><span data-stu-id="28253-121">For more information about using this code, see [Using the Code Examples](using-the-code-examples.md).</span></span>


```C++
HRESULT CreateProfile(IWMProfileManager* pProfileMgr, IWMProfile** ppProfile)
{
    HRESULT hr = S_OK;

    // Create the empty profile.
    hr = pProfileMgr->CreateEmptyProfile(WMT_VER_9_0, ppProfile);
    if(FAILED(hr))
    {
        printf("Could not create the profile.\n");
        return hr;
    }

    return S_OK;
}
```



## <a name="related-topics"></a><span data-ttu-id="28253-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="28253-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28253-123">**Iwmprofile-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="28253-123">**IWMProfile Interface**</span></span>](iwmprofile.md)
</dt> <dt>

[<span data-ttu-id="28253-124">**Iwmprofilemanager-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="28253-124">**IWMProfileManager Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager)
</dt> <dt>

[<span data-ttu-id="28253-125">**Arbeiten mit Profilen**</span><span class="sxs-lookup"><span data-stu-id="28253-125">**Working with Profiles**</span></span>](working-with-profiles.md)
</dt> </dl>

 

 




