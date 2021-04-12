---
title: Speichern von Profilen
description: Speichern von Profilen
ms.assetid: 07c1ef16-6696-4314-aed8-58cda464b0db
keywords:
- Windows Media-Format-SDK, Speichern von Profilen
- Windows Media-Format-SDK, Profil Speicherung
- Profile, speichern
- Profile, iwmprofilemanager-Schnittstelle
- Iwmprofilemanager, Speichern von Profilen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 276b002f0b7f98de2e84f2c27a4f52bde25726bb
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104389847"
---
# <a name="saving-profiles"></a><span data-ttu-id="7ec9f-108">Speichern von Profilen</span><span class="sxs-lookup"><span data-stu-id="7ec9f-108">Saving Profiles</span></span>

<span data-ttu-id="7ec9f-109">Sie können die [**iwmprofilemanager:: saveprofile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-saveprofile) -Methode verwenden, um den Inhalt eines Profil Objekts in einer mit XML formatierten Zeichenfolge zu speichern.</span><span class="sxs-lookup"><span data-stu-id="7ec9f-109">You can use the [**IWMProfileManager::SaveProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-saveprofile) method to save the contents of a profile object to a string formatted with XML.</span></span> <span data-ttu-id="7ec9f-110">Es werden keine Methoden bereitgestellt, um die Profil Zeichenfolge in einer Datei zu speichern. Sie können die Datei-e/a-Routinen Ihrer Wahl verwenden.</span><span class="sxs-lookup"><span data-stu-id="7ec9f-110">No methods are provided to store the profile string to a file; you can use the file I/O routines of your choice.</span></span>

> [!Note]  
> <span data-ttu-id="7ec9f-111">Sie sollten die in eine Datei geschriebene Profil Zeichenfolge niemals ändern.</span><span class="sxs-lookup"><span data-stu-id="7ec9f-111">You should never alter the profile string written to a file.</span></span> <span data-ttu-id="7ec9f-112">Alle Änderungen, die Sie an einem Profil vornehmen möchten, sollten Programm gesteuert erfolgen.</span><span class="sxs-lookup"><span data-stu-id="7ec9f-112">Any changes you want to make to a profile should be made programmatically.</span></span> <span data-ttu-id="7ec9f-113">Das Ändern von Werten in einer PRX-Datei kann zu unvorhersehbaren Ergebnissen führen.</span><span class="sxs-lookup"><span data-stu-id="7ec9f-113">Changing values in a .prx file can cause unpredictable results.</span></span>

 

<span data-ttu-id="7ec9f-114">Das folgende Beispiel ist eine Funktion, mit der ein Profil in einer Datei unter Verwendung der standardmäßigen Datei-e/a im C-Stil gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="7ec9f-114">The following example is a function to save a profile to a file using standard C-style file I/O.</span></span> <span data-ttu-id="7ec9f-115">Um eine Anwendung zu kompilieren, die dieses Beispiel verwendet, müssen Sie "stdio. h" in Ihr Projekt einschließen.</span><span class="sxs-lookup"><span data-stu-id="7ec9f-115">To compile an application that uses this example, you must include stdio.h in your project.</span></span>


```C++
HRESULT ProfileToFile(IWMProfileManager* pProfileMgr, 
                      IWMProfile* pProfile)
{
    HRESULT hr = S_OK;

    FILE*   pFile;
    
    WCHAR*  pwszProfileString = NULL;
    DWORD   cchProfileString = 0;

    // Save the profile to a string.
    // First, retrieve the size of the string required.
    hr = pProfileMgr->SaveProfile(pProfile, 
                                  NULL, 
                                  &cchProfileString);
    if(FAILED(hr))
    {
        printf("Could not get the profile string size.");
        return hr;
    }

    // Allocate memory to hold the string.
    pwszProfileString = new WCHAR[cchProfileString];

    if(pwszProfileString == NULL)
    {
        printf("Could not allocate memory for the profile string.");
        return E_OUTOFMEMORY;
    }

    // Retrieve the string.
    hr = pProfileMgr->SaveProfile(pProfile, 
                                  pwszProfileString, 
                                  &cchProfileString);
    if(FAILED(hr))
    {
        printf("Could not save the profile string.");
        return hr;
    }

    // Create the output file.
    pFile = fopen("MyProfile.prx", "w");

    // Write the profile string to the file.
    fprintf(pFile, "%S\n", pwszProfileString);

    // Close the file.
    fclose(pFile);

    delete[] pwszProfileString;

    return S_OK;
}
```



## <a name="related-topics"></a><span data-ttu-id="7ec9f-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7ec9f-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ec9f-117">**Arbeiten mit Profilen**</span><span class="sxs-lookup"><span data-stu-id="7ec9f-117">**Working with Profiles**</span></span>](working-with-profiles.md)
</dt> </dl>

 

 




