---
title: So ändern Sie Systemprofilversionen
description: So ändern Sie Systemprofilversionen
ms.assetid: 66bf4041-47b5-41b4-abb4-eb08d05e3b28
keywords:
- Profile, System
- Systemprofile, Versionen
- Systemprofile, Versionsänderungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c963a142c879242b5e2ae734dedb4073a120a57a9121c3f3f95e5838c15110a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119084270"
---
# <a name="to-change-system-profile-versions"></a>So ändern Sie Systemprofilversionen

Jedes Mal, wenn Sie ein Profil-Manager-Objekt erstellen, werden die Systemprofile analysiert. Sie können die Systemprofile mithilfe der Methoden [**IWMProfileManager::GetSystemProfileCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-getsystemprofilecount) und [**IWMProfileManager::LoadSystemProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadsystemprofile) durchlaufen, aber der Profil-Manager zählt und listet nur die Profile einer einzelnen Version auf. Wenn Sie diese Methode zum Suchen von Systemprofilen verwenden möchten, müssen Sie sicherstellen, dass der Profil-Manager die gewünschte Version verarbeitet. Verwenden Sie die Methoden der [**IWMProfileManager2-Schnittstelle,**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager2) um die vom Profil-Manager verwendete Systemprofilversion festzulegen und abzurufen.

Versionen werden mithilfe der Member des [**WMT \_ VERSION-Enumerationstyps**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_version) angegeben. Wenn Sie die Systemprofilversion auf WMT \_ VER \_ 9 \_ 0 festlegen, wird der Aufruf erfolgreich ausgeführt, aber die Anzahl der Systemprofile ist 0 (null). Dies liegt daran, dass keine vordefinierten Systemprofile die Codecs Windows Medienaudio- und Video 9-Serie verwenden. Weitere Informationen zum Aktualisieren von Profilen für die Verwendung der neuesten Codecs finden Sie unter [Wiederverwenden von Streamkonfigurationen.](reusing-stream-configurations.md)

Wenn Sie ein Systemprofil anhand seines GUID-Bezeichners laden, spielt es keine Rolle, welche Systemprofilversion der Profil-Manager verwendet. Weitere Informationen zum Laden von Systemprofilen finden Sie unter [So laden Sie ein Systemprofil.](to-load-a-system-profile.md)

Der folgende Beispielcode zeigt, wie die Systemprofilversion festgelegt und abgerufen wird. In diesem Beispiel wird printf für die Konsolenausgabe verwendet, und stdio.h muss eingeschlossen werden. Weitere Informationen zur Verwendung dieses Codes finden Sie unter [Verwenden der Codebeispiele.](using-the-code-examples.md)


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Verwenden von Systemprofilen**](using-system-profiles.md)
</dt> </dl>

 

 




