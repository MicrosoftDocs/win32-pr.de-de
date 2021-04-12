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
# <a name="saving-profiles"></a>Speichern von Profilen

Sie können die [**iwmprofilemanager:: saveprofile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-saveprofile) -Methode verwenden, um den Inhalt eines Profil Objekts in einer mit XML formatierten Zeichenfolge zu speichern. Es werden keine Methoden bereitgestellt, um die Profil Zeichenfolge in einer Datei zu speichern. Sie können die Datei-e/a-Routinen Ihrer Wahl verwenden.

> [!Note]  
> Sie sollten die in eine Datei geschriebene Profil Zeichenfolge niemals ändern. Alle Änderungen, die Sie an einem Profil vornehmen möchten, sollten Programm gesteuert erfolgen. Das Ändern von Werten in einer PRX-Datei kann zu unvorhersehbaren Ergebnissen führen.

 

Das folgende Beispiel ist eine Funktion, mit der ein Profil in einer Datei unter Verwendung der standardmäßigen Datei-e/a im C-Stil gespeichert wird. Um eine Anwendung zu kompilieren, die dieses Beispiel verwendet, müssen Sie "stdio. h" in Ihr Projekt einschließen.


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Arbeiten mit Profilen**](working-with-profiles.md)
</dt> </dl>

 

 




