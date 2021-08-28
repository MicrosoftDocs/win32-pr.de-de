---
title: So laden Sie ein Systemprofil
description: So laden Sie ein Systemprofil
ms.assetid: 2398a44d-c5c7-4fa2-b0ed-1cfb75d8822c
keywords:
- Profile, System
- Systemprofile, Laden
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: becd98903921b81ce1eaf7d2317659c7760bb99c4e55e07efe336719d5d34ed4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807480"
---
# <a name="to-load-a-system-profile"></a>So laden Sie ein Systemprofil

Um Änderungen an einem Systemprofil vorzunehmen, müssen Sie es in ein Profilobjekt laden. Der Profil-Manager bietet zwei Optionen zum Laden von Systemprofilen: nach Bezeichner und nach Index.

Ein Systemprofilbezeichner ist ein GUID-Wert, der dem Systemprofil beim Erstellen zugewiesen wurde. Eine Liste der GUID-Konstanten, die den Systemprofilen der Version 8 zugeordnet sind, finden Sie unter [Systemprofile.](system-profiles.md) Die GUID-Konstanten für frühere Versionen finden Sie in der Headerdatei WMSysPrf.h. Weitere Informationen zu dieser und anderen Headerdateien, die im Windows Media Format SDK enthalten sind, finden Sie unter [Bibliotheksdateien und Compiler Einstellungen](library-files-and-compiler-settings.md).

Der folgende Beispielcode veranschaulicht das Laden eines Systemprofils mithilfe des Systemprofilbezeichners. Damit dieser Code funktioniert, müssen Sie WMSysPrf.h und stdio.h einschließen. Weitere Informationen zur Verwendung dieses Codes finden Sie unter [Verwenden der Codebeispiele.](using-the-code-examples.md)


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



Wenn Sie nicht wissen, welches Profil Sie verwenden möchten, können Sie mithilfe der Methoden [**GetSystemProfileCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-getsystemprofilecount) und [**LoadSystemProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadsystemprofile) der [**IWMProfileManager-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) alle Systemprofile einer bestimmten Version durchlaufen. Diese Methoden behandeln jeweils nur eine Version der Systemprofile. Weitere Informationen zum Ändern der Systemprofilversion finden Sie unter [So ändern Sie Systemprofilversionen.](to-change-system-profile-versions.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Verwenden von Systemprofilen**](using-system-profiles.md)
</dt> </dl>

 

 




