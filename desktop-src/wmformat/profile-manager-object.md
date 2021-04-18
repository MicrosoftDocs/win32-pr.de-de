---
title: Profil-Manager-Objekt
description: Profil-Manager-Objekt
ms.assetid: 8d174243-334e-418e-a1c8-77486b940de7
keywords:
- Windows Media-Format-SDK, Profil-Manager-Objekte
- Advanced Systems Format (ASF), Profil-Manager-Objekte
- ASF (Advanced Systems Format), Profil-Manager-Objekte
- Objekte, Profil-Manager-Objekte
- Profile, Objekte
- Profile, Profil-Manager-Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ce3d77598f52e43a840c1b6b3ef58baa47f77bd
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "106340891"
---
# <a name="profile-manager-object"></a>Profil-Manager-Objekt

Ein Profil ist ein Satz von Medien Parametern, die zum Erstellen einer ASF-Datei verwendet werden. Das Profil-Manager-Objekt erstellt Profil Objekte zur Bearbeitung. Profil Objekte können ohne Daten erstellt oder aus vorhandenen Profildaten erstellt werden. Das Profil-Manager-Objekt stellt auch Methoden zum Auflisten unterstützter Codecs und zum Abfragen dieser Codecs für Informationen bereit.

Das Profil-Manager-Objekt wird von der [**wmkreateprofilemanager**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateprofilemanager) -Funktion erstellt, mit der ein Zeiger auf eine [**iwmprofilemanager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager) -Schnittstelle festgelegt wird. Die anderen Schnittstellen des Profil-Manager-Objekts können durch Aufrufen der **QueryInterface** -Methode abgerufen werden.

Die folgenden Schnittstellen werden vom Profil-Manager-Objekt unterstützt.



| Schnittstelle                                                      | BESCHREIBUNG                                                                                                                                  |
|----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [**Iwmcodecinfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo)                           | Ruft Informationen zu unterstützten Codecs und deren Formaten ab.                                                                              |
| [**IWMCodecInfo2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo2)                         | Ruft die Namen der unterstützten Codecs und die Beschreibungen ihrer Formate ab. Erbt alle Methoden von **iwmcodecinfo**.          |
| [**IWMCodecInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcodecinfo3)                         | Ruft Codec-Eigenschaften und-Abfragen für unterstützte Funktionen ab. Erbt alle Methoden von **iwmcodecinfo** und **IWMCodecInfo2**. |
| [**Iwmprofilemanager**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager)                 | Erstellt neue Profile, lädt vorhandene Profile und speichert benutzerdefinierte Profile.                                                                    |
| [**IWMProfileManager2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager2)               | Steuert die Version der Systemprofile, die vom Profil-Manager aufgelistet werden. Erbt alle Methoden von **iwmprofilemanager**.             |
| [**Iwmprofilemanagerlanguage**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanagerlanguage) | Steuert die Sprache der vom Profil-Manager analysierten Systemprofile.                                                                  |



 

## <a name="remarks"></a>Bemerkungen

Wenn ein Profil-Manager-Objekt erstellt wird, werden alle Systemprofile analysiert, was einige Sekunden dauern kann. Wenn Sie einen Profil-Manager bei jeder Verwendung verwenden, wirkt sich dies negativ auf die Leistung aus. Sie sollten einen Profil-Manager einmal in der Anwendung erstellen und nur dann freigeben, wenn Sie ihn nicht mehr verwenden müssen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Objekte**](objects.md)
</dt> <dt>

[**Profil Objekt**](profile-object.md)
</dt> <dt>

[**Profiles**](profiles.md)
</dt> </dl>

 

 




