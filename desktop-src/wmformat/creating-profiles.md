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
# <a name="creating-profiles"></a>Erstellen von Profilen

In vielen Fällen empfiehlt es sich, ein leeres Profil zu erstellen, das für Ihre Anforderungen konfiguriert werden kann. In anderen Fällen ist es einfacher, ein vorhandenes Profil zu bearbeiten, wie z. b. ein Systemprofil. Weitere Informationen zum Verwenden von Systemprofilen finden Sie unter [Verwenden von Systemprofilen](using-system-profiles.md).

Wenn Sie ein leeres Profil erstellen, das Sie für die Konfiguration bereit haben, ist ein Profil-Manager-Objekt erforderlich. Um die [**iwmprofilemanager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) -Schnittstelle eines Profil-Manager-Objekts abzurufen, müssen Sie die [**wmkreateprofilemanager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) -Funktion aufrufen.

Um ein leeres Profil zu erstellen, rufen Sie [**iwmprofilemanager:: kreateemptyprofile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofilemanager-createemptyprofile)auf. Wenn Sie ein leeres Profil erstellen, ist das einzige, was Sie angeben, die Version des Windows Media-Format-SDKs, dem das Profil entspricht. Sie sollten immer die neueste Version verwenden, es sei denn, Sie müssen eine frühere Version verwenden. Die-Version bestimmt die Struktur des Profils. in früheren Versionen wurden einige Eigenschaften nicht unterstützt.

Der folgende Beispielcode zeigt, wie Sie ein neues Profil erstellen. Um diesen Code in der Anwendung zu kompilieren, fügen Sie stdio. h ein. Weitere Informationen zur Verwendung dieses Codes finden Sie unter [Verwenden der Codebeispiele](using-the-code-examples.md).


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Iwmprofile-Schnittstelle**](iwmprofile.md)
</dt> <dt>

[**Iwmprofilemanager-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager)
</dt> <dt>

[**Arbeiten mit Profilen**](working-with-profiles.md)
</dt> </dl>

 

 




