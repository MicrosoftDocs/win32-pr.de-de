---
title: Profil-Manager-Objekt
description: Profil-Manager-Objekt
ms.assetid: 8d174243-334e-418e-a1c8-77486b940de7
keywords:
- Windows Medienformat-SDK, Profil-Manager-Objekte
- Advanced Systems Format (ASF), Profil-Manager-Objekte
- ASF (Advanced Systems Format), Profil-Manager-Objekte
- Objekte, Profil-Manager-Objekte
- Profile, Objekte
- Profile, Profil-Manager-Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ce272067e98f787d5136cacc0a2d02f474264f14f14aa785b28162945ef1b41
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119084647"
---
# <a name="profile-manager-object"></a>Profil-Manager-Objekt

Ein Profil ist ein Satz von Medienparametern, die zum Erstellen einer ASF-Datei verwendet werden. Das Profil-Manager-Objekt erstellt Profilobjekte zur Bearbeitung. Profilobjekte können ohne Daten erstellt oder aus vorhandenen Profildaten erstellt werden. Das Profil-Manager-Objekt stellt auch Methoden zum Aufzählen unterstützter Codecs und zum Abfragen dieser Codecs nach Informationen bereit.

Das Profil-Manager-Objekt wird von der [**WMCreateProfileManager-Funktion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) erstellt, die einen Zeiger auf eine [**IWMProfileManager-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) festlegt. Die anderen Schnittstellen des Profil-Manager-Objekts können durch Aufrufen der **QueryInterface-Methode** abgerufen werden.

Die folgenden Schnittstellen werden vom Profil-Manager-Objekt unterstützt.



| Schnittstelle                                                      | Beschreibung                                                                                                                                  |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [**IWMCodecInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo)                           | Ruft Informationen zu unterstützten Codecs und deren Formaten ab.                                                                              |
| [**IWMCodecInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo2)                         | Ruft die Namen der unterstützten Codecs und die Beschreibungen ihrer Formate ab. Erbt alle Methoden von **IWMCodecInfo.**          |
| [**IWMCodecInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3)                         | Ruft Codeceigenschaften ab und fragt Codecs für unterstützte Features ab. Erbt alle Methoden von **IWMCodecInfo** und **IWMCodecInfo2.** |
| [**IWMProfileManager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager)                 | Erstellt neue Profile, lädt vorhandene Profile und speichert benutzerdefinierte Profile.                                                                    |
| [**IWMProfileManager2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager2)               | Steuert die Version von Systemprofilen, die vom Profil-Manager aufzählt werden. Erbt alle Methoden von **IWMProfileManager.**             |
| [**IWMProfileManagerLanguage**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanagerlanguage) | Steuert die Sprache der vom Profil-Manager analysierten Systemprofile.                                                                  |



 

## <a name="remarks"></a>Hinweise

Wenn ein Profil-Manager-Objekt erstellt wird, werden alle Systemprofile analysiert, was mehrere Sekunden dauern kann. Das Erstellen und Freigeben eines Profil-Managers bei jeder Verwendung wirkt sich negativ auf die Leistung aus. Sie sollten einen Profil-Manager einmal in Ihrer Anwendung erstellen und nur dann freigeben, wenn Sie ihn nicht mehr verwenden müssen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Objekte**](objects.md)
</dt> <dt>

[**Profilobjekt**](profile-object.md)
</dt> <dt>

[**Profiles**](profiles.md)
</dt> </dl>

 

 




