---
title: IWMProfile-Schnittstelle
description: Die IWMProfile-Schnittstelle ist die primäre Schnittstelle für ein Profilobjekt.
ms.assetid: 00f28d6b-d27d-4268-960e-c8ea25e5359e
keywords:
- IWMProfile-Schnittstelle windows Media Format
- IWMProfile-Schnittstelle windows Media Format , beschrieben
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
ms.openlocfilehash: 525cdee41be011e373c65e508e91087082c17f2ec279195e2a9ab285b391fd54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119084717"
---
# <a name="iwmprofile-interface"></a>IWMProfile-Schnittstelle

Die **IWMProfile-Schnittstelle** ist die primäre Schnittstelle für ein [*Profilobjekt.*](wmformat-glossary.md) Ein Profilobjekt wird verwendet, um benutzerdefinierte Profile zu konfigurieren. Sie können **IWMProfile** verwenden, um Streamkonfigurationsobjekte und gegenseitige Ausschlussobjekte zu erstellen, zu löschen oder zu ändern. Sie können auch allgemeine Informationen zum Profil festlegen und abrufen. Um auf alle Funktionen des Profilobjekts zuzugreifen, sollten Sie [**IWMProfile3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3)verwenden, das von **IWMProfile** und [**IWMProfile2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile2)erbt.

**Auf IWMProfile** kann auch über das Readerobjekt zugegriffen werden. Dort können Sie es verwenden, um Informationen zu den Datenströmen einer Datei abzurufen, die im Reader geladen wird. Wenn Sie über den Reader auf **IWMProfile** zugreifen, können Sie Änderungen am Profil vornehmen, aber keine der Änderungen kann in der Datei gespeichert werden. Es ist oft praktisch, das Profil einer vorhandenen Datei als Grundlage eines neuen Profils zu verwenden. Der synchrone Reader unterstützt **IWMProfile** auf die gleiche Weise wie der Reader.

Die profilinformationen, die über den Reader oder den synchronen Reader abgerufen werden, stammen nicht aus einer PRX-Datei. Der Reader verwendet die Informationen in der ASF-Datei, um die Streamkonfigurationen zusammenzustellen. Daher sind bestimmte Profilinformationen wie Name und Beschreibung nicht über den Reader verfügbar.

Es gibt mehrere Möglichkeiten, einen Zeiger auf eine **IWMProfile-Schnittstelle** abzurufen. Der Profil-Manager verfügt über Methoden zum Erstellen eines neuen Profils und zum Zugreifen auf vorhandene Profile. Alle diese Methoden legen einen **IWMProfile-Zeiger** fest. Beim Lesen einer Datei kann ein Zeiger auf **IWMProfile** abgerufen werden, indem die **QueryInterface-Methode** einer beliebigen Readerschnittstelle aufgerufen wird. Ebenso kann jede Schnittstelle des synchronen Readerobjekts einen Zeiger mit einem Aufruf von **QueryInterface**[**IWMProfile3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofile3)abrufen.

## <a name="members"></a>Member

Die **IWMProfile-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IWMProfile** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IWMProfile-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                  | BESCHREIBUNG                                                                                 |
|:------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [**AddMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addmutualexclusion)             | Fügt dem Profil ein objekt für gegenseitigen Ausschluss hinzu.<br/>                                   |
| [**AddStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-addstream)                               | Fügt dem Profil einen Stream hinzu.<br/>                                                    |
| [**CreateNewMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewmutualexclusion) | Erstellt ein objekt für gegenseitigen Ausschluss für das Profil.<br/>                               |
| [**CreateNewStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-createnewstream)                   | Erstellt ein Streamkonfigurationsobjekt für das Profil.<br/>                           |
| [**GetDescription**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getdescription)                     | Ruft die Beschreibung des Profils ab.<br/>                                        |
| [**GetMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getmutualexclusion)             | Ruft ein gegenseitiges Ausschlussobjekt aus dem Profil ab.<br/>                            |
| [**GetMutualExclusionCount**](/windows/win32/api/wmcontainer/nf-wmcontainer-imfasfprofile-getmutualexclusioncount)   | Ruft die Anzahl der gegenseitigen Ausschlussobjekte im Profil ab.<br/>                 |
| [**GetName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getname)                                   | Ruft den Namen des Profils ab.<br/>                                               |
| [**Getstream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream)                               | Ruft einen Stream unter Verwendung einer Indexnummer aus dem Profil ab.<br/>                     |
| [**GetStreamByNumber**](/windows/win32/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreambynumber)               | Ruft einen Stream unter Verwendung der Nummer des Streams aus dem Profil ab.<br/>            |
| [**GetStreamCount**](/windows/win32/api/wmcontainer/nf-wmcontainer-imfasfprofile-getstreamcount)                     | Ruft die Anzahl der Datenströme im Profil ab.<br/>                                  |
| [**Getversion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getversion)                             | Ruft die Versionsnummer von Microsoft Windows Media-Dienste im Profil ab.<br/> |
| [**ReconfigStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-reconfigstream)                     | Ermöglicht die Aufnahme von Änderungen an einer Streamkonfiguration in das Profil.<br/>    |
| [**RemoveMutualExclusion**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-removemutualexclusion)       | Entfernt ein gegenseitiges Ausschlussobjekt aus dem Profil.<br/>                              |
| [**RemoveStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-removestream)                         | Entfernt einen Stream aus dem Profil.<br/>                                               |
| [**RemoveStreamByNumber**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-removestreambynumber)         | Entfernt einen Stream aus dem Profil.<br/>                                               |
| [**SetDescription**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-setdescription)                     | Gibt die Beschreibung des Profils an.<br/>                                        |
| [**SetName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-setname)                                   | Gibt den Namen des Profils an.<br/>                                               |



 

Informationen dazu, welche Schnittstellen mithilfe der QueryInterface-Methode dieser Schnittstelle abgerufen werden können, finden Sie im Thema zu dem Objekt, für das diese Schnittstelle implementiert wird.

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Schnittstellen**](interfaces.md)
</dt> <dt>

[**IWMProfileManager-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmprofilemanager)
</dt> <dt>

[**Profil-Manager-Objekt**](profile-manager-object.md)
</dt> <dt>

[**Reader-Objekt**](reader-object.md)
</dt> <dt>

[**Synchrones Reader-Objekt**](synchronous-reader-object.md)
</dt> <dt>

[**Arbeiten mit Profilen**](working-with-profiles.md)
</dt> </dl>

 

