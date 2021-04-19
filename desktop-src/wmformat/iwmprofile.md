---
title: IWMProfile-Schnittstelle
description: Die iwmprofile-Schnittstelle ist die primäre Schnittstelle für ein Profil Objekt.
ms.assetid: 00f28d6b-d27d-4268-960e-c8ea25e5359e
keywords:
- Iwmprofile-Schnittstelle Windows Media-Format
- Iwmprofile-Schnittstelle Windows Media-Format, beschrieben
topic_type:
- apiref
api_name:
- IWMProfile
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location:
- wmsdkidl.h
ms.openlocfilehash: f814df820bd50a36abf2ee8e453549f46c9c5c9e
ms.sourcegitcommit: 52d79b29f3b9933c8bef43207ff80c668a81cb73
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2020
ms.locfileid: "106342387"
---
# <a name="iwmprofile-interface"></a>IWMProfile-Schnittstelle

Die **iwmprofile** -Schnittstelle ist die primäre Schnittstelle für ein [*Profil*](wmformat-glossary.md) Objekt. Ein Profil Objekt wird verwendet, um benutzerdefinierte Profile zu konfigurieren. Sie können **iwmprofile** verwenden, um streamingkonfigurationsobjekte und gegenseitige Ausschluss Objekte zu erstellen, zu löschen oder zu ändern. Sie können auch allgemeine Informationen zum Profil festlegen und abrufen. Für den Zugriff auf alle Funktionen des profile-Objekts sollten Sie [**IWMProfile3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3)verwenden, das von **iwmprofile** und [**IWMProfile2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile2)erbt.

Auf **iwmprofile** kann auch über das Reader-Objekt zugegriffen werden, in dem Sie Informationen zu den Datenströmen einer Datei, die im Reader geladen ist, erhalten. Beim Zugriff auf **iwmprofile** vom Reader aus können Sie Änderungen am Profil vornehmen, aber keine der Änderungen kann in der Datei gespeichert werden. Häufig ist es praktisch, das Profil einer vorhandenen Datei als Grundlage für ein neues Profil zu verwenden. Der synchrone Reader unterstützt **iwmprofile** auf die gleiche Weise wie der Reader.

Die Profilinformationen, die über den Reader oder den synchronen Reader abgerufen werden, stammen nicht aus einer PRX-Datei. Der Reader verwendet die Informationen in der ASF-Datei, um die streamkonfigurationen zusammenzustellen. Folglich sind bestimmte Profilinformationen, wie der Name und die Beschreibung, nicht über den Reader verfügbar.

Es gibt mehrere Möglichkeiten, einen Zeiger auf eine **iwmprofile** -Schnittstelle zu erhalten. Der Profil-Manager verfügt über Methoden zum Erstellen eines neuen Profils und zum Zugreifen auf vorhandene Profile. Alle diese Methoden legen einen **iwmprofile** -Zeiger fest. Beim Lesen einer Datei kann ein Zeiger auf **iwmprofile** durch Aufrufen der **QueryInterface** -Methode jeder beliebigen Lese Schnittstelle abgerufen werden. Ebenso kann jede Schnittstelle des synchronen Reader-Objekts einen Zeiger mit einem aufzurufenden **QueryInterface**-[**IWMProfile3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3)abrufen.

## <a name="members"></a>Member

Die **iwmprofile** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Iwmprofile** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **iwmprofile** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                  | BESCHREIBUNG                                                                                 |
|:------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [**Addmutualexclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addmutualexclusion)             | Fügt dem Profil ein gegenseitiges Ausschluss Objekt hinzu.<br/>                                   |
| [**Addstream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addstream)                               | Fügt dem Profil einen Stream hinzu.<br/>                                                    |
| [**"Kreatenewmutualexandclusion"**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewmutualexclusion) | Erstellt ein gegenseitiges Ausschluss Objekt für das Profil.<br/>                               |
| [**"Kreatenewstream"**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewstream)                   | Erstellt ein streamkonfigurationsobjekt für das Profil.<br/>                           |
| [**GetDescription**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getdescription)                     | Ruft die Beschreibung des Profils ab.<br/>                                        |
| [**Getmutualexclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getmutualexclusion)             | Ruft ein gegenseitiges Ausschluss Objekt aus dem Profil ab.<br/>                            |
| [**Getmutualexclusioncount**](/windows/win32/api/wmcontainer/nf-wmcontainer-imfasfprofile-getmutualexclusioncount)   | Ruft die Anzahl der gegenseitigen Ausschluss Objekte im Profil ab.<br/>                 |
| [**GetName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getname)                                   | Ruft den Namen des Profils ab.<br/>                                               |
| [**GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream)                               | Ruft einen Stream unter Verwendung einer Indexnummer aus dem Profil ab.<br/>                     |
| [**Getstreambynumber**](/windows/win32/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreambynumber)               | Ruft einen Datenstrom ab, wobei die Nummer des Streams aus dem Profil verwendet wird.<br/>            |
| [**Getstreamcount**](/windows/win32/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreamcount)                     | Ruft die Anzahl der Streams im Profil ab.<br/>                                  |
| [**GetVersion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getversion)                             | Ruft die Versionsnummer von Microsoft Windows Media Services im Profil ab.<br/> |
| [**"Reconfigstream"**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream)                     | Ermöglicht das Einschließen von Änderungen, die an einer Datenstrom Konfiguration vorgenommen werden, in das Profil.<br/>    |
| [**Removemutualexclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-removemutualexclusion)       | Entfernt ein gegenseitiges Ausschluss Objekt aus dem Profil.<br/>                              |
| [**Removestream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-removestream)                         | Entfernt einen Stream aus dem Profil.<br/>                                               |
| [**Removestreambynumber**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-removestreambynumber)         | Entfernt einen Stream aus dem Profil.<br/>                                               |
| [**SetDescription**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-setdescription)                     | Gibt die Beschreibung des Profils an.<br/>                                        |
| [**SetName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-setname)                                   | Gibt den Namen des Profils an.<br/>                                               |



 

Informationen darüber, welche Schnittstellen mithilfe der QueryInterface-Methode dieser Schnittstelle abgerufen werden können, finden Sie im Thema für das Objekt, für das diese Schnittstelle implementiert ist.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Schnittstellen**](interfaces.md)
</dt> <dt>

[**Iwmprofilemanager-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager)
</dt> <dt>

[**Profil-Manager-Objekt**](profile-manager-object.md)
</dt> <dt>

[**Reader-Objekt**](reader-object.md)
</dt> <dt>

[**Synchrones Reader-Objekt**](synchronous-reader-object.md)
</dt> <dt>

[**Arbeiten mit Profilen**](working-with-profiles.md)
</dt> </dl>

 

