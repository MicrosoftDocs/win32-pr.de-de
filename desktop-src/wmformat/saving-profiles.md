---
title: Speichern von Profilen
description: Speichern von Profilen
ms.assetid: 07c1ef16-6696-4314-aed8-58cda464b0db
keywords:
- Windows Medienformat-SDK, Speichern von Profilen
- Windows Medienformat-SDK, Speichern von Profilen
- Profile,Speichern
- profiles,IWMProfileManager-Schnittstelle
- IWMProfileManager, Speichern von Profilen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6befb09d7e0d628462bdd22e1e905c351be58dc077959089883ce3707dc493d3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119547040"
---
# <a name="saving-profiles"></a>Speichern von Profilen

Sie können die [**IWMProfileManager::SaveProfile-Methode**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-saveprofile) verwenden, um den Inhalt eines Profilobjekts in einer mit XML formatierten Zeichenfolge zu speichern. Es werden keine Methoden bereitgestellt, um die Profilzeichenfolge in einer Datei zu speichern. Sie können die Datei-E/A-Routinen Ihrer Wahl verwenden.

> [!Note]  
> Sie sollten die in eine Datei geschriebene Profilzeichenfolge nie ändern. Alle Änderungen, die Sie an einem Profil vornehmen möchten, sollten programmgesteuert vorgenommen werden. Das Ändern von Werten in einer PRX-Datei kann zu unvorhersehbaren Ergebnissen führen.

 

Das folgende Beispiel ist eine Funktion zum Speichern eines Profils in einer Datei mithilfe von Datei-E/A im C-Standardformat. Um eine Anwendung zu kompilieren, die dieses Beispiel verwendet, müssen Sie stdio.h in Das Projekt verwenden.


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

 

 




