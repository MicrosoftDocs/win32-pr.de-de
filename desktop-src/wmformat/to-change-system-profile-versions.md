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
# <a name="to-change-system-profile-versions"></a>So ändern Sie System Profil Versionen

Wenn Sie ein Profil-Manager-Objekt erstellen, werden die Systemprofile analysiert. Sie können die Systemprofile mithilfe der [**iwmprofilemanager:: getsystemprofilecount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-getsystemprofilecount) -Methode und der [**iwmprofilemanager:: loadsystemprofile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadsystemprofile) -Methode durchlaufen, aber der Profil-Manager zählt und listet nur die Profile einer einzelnen Version gleichzeitig auf. Wenn Sie diese Methode für die Suche nach Systemprofilen verwenden möchten, müssen Sie sicherstellen, dass der Profil-Manager die gewünschte Version behandelt. Verwenden Sie die Methoden der [**IWMProfileManager2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager2) -Schnittstelle, um die vom Profil-Manager verwendete Systemprofil Version festzulegen und abzurufen.

Versionen werden mithilfe der Member des Enumerationstyps der [**WMT- \_ Version**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_version) angegeben. Wenn Sie die Systemprofil Version auf WMT \_ ver \_ 9 0 festlegen \_ , wird der-Vorgang erfolgreich ausgeführt, aber die Anzahl der Systemprofile ist 0 (null). Dies liegt daran, dass keine vordefinierten Systemprofile die Codecs Windows Media Audio und der Video 9-Serie verwenden. Weitere Informationen zum Aktualisieren von Profilen für die Verwendung der neuesten Codecs finden Sie unter [wieder verwenden von streamkonfigurationen](reusing-stream-configurations.md).

Wenn Sie ein Systemprofil mit dem GUID-Bezeichner laden, spielt es keine Rolle, welche Systemprofil Version der Profil-Manager verwendet. Weitere Informationen zum Laden von Systemprofilen finden [Sie unter So laden Sie ein Systemprofil](to-load-a-system-profile.md).

Der folgende Beispielcode zeigt, wie die Systemprofil Version festgelegt und abgerufen wird. In diesem Beispiel wird printf für die Konsolenausgabe verwendet, und es muss "stdio. h" eingeschlossen werden. Weitere Informationen zur Verwendung dieses Codes finden Sie unter [Verwenden der Codebeispiele](using-the-code-examples.md).


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

[**Verwenden von System Profilen**](using-system-profiles.md)
</dt> </dl>

 

 




