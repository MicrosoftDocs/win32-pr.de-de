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
# <a name="to-load-a-system-profile"></a>So laden Sie ein System Profil

Wenn Sie Änderungen an einem Systemprofil vornehmen möchten, müssen Sie es in ein Profil Objekt laden. Der Profil-Manager bietet zwei Optionen zum Laden von Systemprofilen: nach Bezeichner und nach Index.

Ein Systemprofil Bezeichner ist ein GUID-Wert, der dem Systemprofil beim Erstellen zugewiesen wurde. Eine Liste der GUID-Konstanten, die den Systemprofilen der Version 8 zugeordnet sind, finden Sie unter [Systemprofile](system-profiles.md). Die GUID-Konstanten für frühere Versionen finden Sie in der Header Datei "wmsysprf. h". Weitere Informationen zu diesem und anderen Header Dateien, die im Windows Media Format SDK enthalten sind, finden Sie unter [Bibliotheksdateien und Compilereinstellungen](library-files-and-compiler-settings.md).

Im folgenden Beispielcode wird veranschaulicht, wie ein Systemprofil mithilfe des Systemprofil Bezeichners geladen wird. Damit dieser Code funktioniert, müssen Sie "wmsysprf. h" und "stdio. h" einschließen. Weitere Informationen zur Verwendung dieses Codes finden Sie unter [Verwenden der Codebeispiele](using-the-code-examples.md).


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



Wenn Sie nicht wissen, welches Profil Sie verwenden möchten, können Sie alle Systemprofile einer bestimmten Version durchlaufen, indem Sie die [**getsystemprofilecount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-getsystemprofilecount) -Methode und die [**loadsystemprofile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-loadsystemprofile) -Methode der [**iwmprofilemanager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) -Schnittstelle verwenden. Diese Methoden behandeln nur eine Version der Systemprofile gleichzeitig. Weitere Informationen zum Ändern der Systemprofil Version finden [Sie unter So ändern Sie Systemprofil Versionen](to-change-system-profile-versions.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Verwenden von System Profilen**](using-system-profiles.md)
</dt> </dl>

 

 




