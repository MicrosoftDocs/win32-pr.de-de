---
title: So laden Sie ein System Profil
description: So laden Sie ein System Profil
ms.assetid: 2398a44d-c5c7-4fa2-b0ed-1cfb75d8822c
keywords:
- Profile, System
- Systemprofile, laden
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73e745cb2fed32d650a22febef827ed7662f4448
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104389877"
---
# <a name="to-load-a-system-profile"></a><span data-ttu-id="79fd4-105">So laden Sie ein System Profil</span><span class="sxs-lookup"><span data-stu-id="79fd4-105">To Load a System Profile</span></span>

<span data-ttu-id="79fd4-106">Wenn Sie Änderungen an einem Systemprofil vornehmen möchten, müssen Sie es in ein Profil Objekt laden.</span><span class="sxs-lookup"><span data-stu-id="79fd4-106">To make changes to a system profile, you must load it into a profile object.</span></span> <span data-ttu-id="79fd4-107">Der Profil-Manager bietet zwei Optionen zum Laden von Systemprofilen: nach Bezeichner und nach Index.</span><span class="sxs-lookup"><span data-stu-id="79fd4-107">The profile manager provides two options for loading system profiles: by identifier, and by index.</span></span>

<span data-ttu-id="79fd4-108">Ein Systemprofil Bezeichner ist ein GUID-Wert, der dem Systemprofil beim Erstellen zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="79fd4-108">A system profile identifier is a GUID value assigned to the system profile when it was created.</span></span> <span data-ttu-id="79fd4-109">Eine Liste der GUID-Konstanten, die den Systemprofilen der Version 8 zugeordnet sind, finden Sie unter [Systemprofile](system-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="79fd4-109">For a list of the GUID constants associated with the version 8 system profiles, see [System Profiles](system-profiles.md).</span></span> <span data-ttu-id="79fd4-110">Die GUID-Konstanten für frühere Versionen finden Sie in der Header Datei "wmsysprf. h".</span><span class="sxs-lookup"><span data-stu-id="79fd4-110">You can find the GUID constants for previous versions in the header file WMSysPrf.h.</span></span> <span data-ttu-id="79fd4-111">Weitere Informationen zu diesem und anderen Header Dateien, die im Windows Media Format SDK enthalten sind, finden Sie unter [Bibliotheksdateien und Compilereinstellungen](library-files-and-compiler-settings.md).</span><span class="sxs-lookup"><span data-stu-id="79fd4-111">For more information about this and other header files included with the Windows Media Format SDK, see [Library Files and Compiler Settings](library-files-and-compiler-settings.md).</span></span>

<span data-ttu-id="79fd4-112">Im folgenden Beispielcode wird veranschaulicht, wie ein Systemprofil mithilfe des Systemprofil Bezeichners geladen wird.</span><span class="sxs-lookup"><span data-stu-id="79fd4-112">The following example code demonstrates how to load a system profile using the system profile identifier.</span></span> <span data-ttu-id="79fd4-113">Damit dieser Code funktioniert, müssen Sie "wmsysprf. h" und "stdio. h" einschließen.</span><span class="sxs-lookup"><span data-stu-id="79fd4-113">For this code to work, you must include WMSysPrf.h and stdio.h.</span></span> <span data-ttu-id="79fd4-114">Weitere Informationen zur Verwendung dieses Codes finden Sie unter [Verwenden der Codebeispiele](using-the-code-examples.md).</span><span class="sxs-lookup"><span data-stu-id="79fd4-114">For more information about using this code, see [Using the Code Examples](using-the-code-examples.md).</span></span>


```C++
IWMProfileManager* pProfileMgr = NULL;
IWMProfile*        pProfile    = NULL;

HRESULT hr = S_OK;

// Initialize COM.
hr = CoInitialize(NULL);

// Create a profile manager.
hr = WMCreateProfileManager(&pProfileMgr);

// Retrieve the data for the general-purpose broadband video profile.
hr = pProfileMgr->LoadProfileByID(WMProfile_V80_100Video, &pProfile);

// TODO: Perform whatever customizations are needed. For details about
// editing profiles, see Using Custom Profiles.

// Clean up.
pProfile->Release();
pProfile = NULL;
pProfileMgr->Release();
pProfileMgr = NULL;
```



<span data-ttu-id="79fd4-115">Wenn Sie nicht wissen, welches Profil Sie verwenden möchten, können Sie alle Systemprofile einer bestimmten Version durchlaufen, indem Sie die [**getsystemprofilecount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-getsystemprofilecount) -Methode und die [**loadsystemprofile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadsystemprofile) -Methode der [**iwmprofilemanager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) -Schnittstelle verwenden.</span><span class="sxs-lookup"><span data-stu-id="79fd4-115">If you do not know which profile you want to use, you can iterate through all of the system profiles of a particular version using the [**GetSystemProfileCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-getsystemprofilecount) and [**LoadSystemProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadsystemprofile) methods of the [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) interface.</span></span> <span data-ttu-id="79fd4-116">Diese Methoden behandeln nur eine Version der Systemprofile gleichzeitig.</span><span class="sxs-lookup"><span data-stu-id="79fd4-116">These methods only deal with one version of the system profiles at a time.</span></span> <span data-ttu-id="79fd4-117">Weitere Informationen zum Ändern der Systemprofil Version finden [Sie unter So ändern Sie Systemprofil Versionen](to-change-system-profile-versions.md).</span><span class="sxs-lookup"><span data-stu-id="79fd4-117">For more information about changing the system profile version, see [To Change System Profile Versions](to-change-system-profile-versions.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="79fd4-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="79fd4-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="79fd4-119">**Verwenden von System Profilen**</span><span class="sxs-lookup"><span data-stu-id="79fd4-119">**Using System Profiles**</span></span>](using-system-profiles.md)
</dt> </dl>

 

 




