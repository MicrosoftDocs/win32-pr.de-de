---
description: Stellt ein Element in einem Shellordner dar. Dieses Objekt enthält Eigenschaften und Methoden, mit denen Sie Informationen über das Element abrufen können.
title: FolderItem-Objekt (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItem
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 38c0e049-2f9f-43bc-8bf2-1b7becf16e66
ms.openlocfilehash: f6744441c051d65bd24f2db888f9bc8d71e66cedcf50c097094beee8ae5a96a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119715370"
---
# <a name="folderitem-object"></a>FolderItem-Objekt

Stellt ein Element in einem Shellordner dar. Dieses Objekt enthält Eigenschaften und Methoden, mit denen Sie Informationen über das Element abrufen können.

## <a name="members"></a>Member

Das **FolderItem-Objekt** verfügt über folgende Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **FolderItem-Objekt** verfügt über diese Methoden.



| Methode                                      | Beschreibung                                                                                                                                                 |
|:--------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**InvokeVerb**](folderitem-invokeverb.md) | Führt ein Verb für das Element aus.<br/>                                                                                                                     |
| [**Verben**](folderitem-verbs.md)           | Ruft das [**FolderItemVerbs-Objekt**](folderitemverbs.md) des Elements ab. Dieses Objekt ist die Auflistung von Verben, die für das Element ausgeführt werden können.<br/> |



 

### <a name="properties"></a>Eigenschaften

Das **FolderItem-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                                   | Zugriffstyp           | Beschreibung                                                                                                                                                                                                        |
|:-----------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Application**](folderitem-application.md)<br/>   | Schreibgeschützt<br/>  | Enthält das [**Application-Objekt**](folderitem-application.md) des Ordnerelements.<br/>                                                                                                                   |
| [**GetFolder**](folderitem-getfolder.md)<br/>       | Schreibgeschützt<br/>  | Enthält das [**Folder-Objekt**](folder.md) des Elements, wenn das Element ein Ordner ist.<br/>                                                                                                                           |
| [**GetLink**](folderitem-getlink.md)<br/>           | Schreibgeschützt<br/>  | Enthält das [**ShellLinkObject-Objekt**](shelllinkobject-object.md) des Elements, wenn das Element eine Verknüpfung ist.<br/>                                                                                                |
| [**IsBrowsable**](folderitem-isbrowsable.md)<br/>   | Schreibgeschützt<br/>  | Gibt an, ob das Element in einem Browser oder Windows Explorer-Frame gehostet werden kann.<br/>                                                                                                                         |
| [**IsFileSystem**](folderitem-isfilesystem.md)<br/> | Schreibgeschützt<br/>  | Gibt an, ob das Element Teil des Dateisystems ist.<br/>                                                                                                                                                       |
| [**IsFolder**](folderitem-isfolder.md)<br/>         | Schreibgeschützt<br/>  | Gibt an, ob das Element ein Ordner ist.<br/>                                                                                                                                                                      |
| [**Islink**](folderitem-islink.md)<br/>             | Schreibgeschützt<br/>  | Gibt an, ob das Element eine Verknüpfung ist.<br/>                                                                                                                                                               |
| [**ModifyDate**](folderitem-modifydate.md)<br/>     | Lesen/Schreiben<br/> | Legt das Datum und die Uhrzeit der letzten Änderung einer Datei fest oder ruft sie ab. [**ModifyDate**](folderitem-modifydate.md) kann verwendet werden, um das Datum und die Uhrzeit der letzten Änderung eines Ordners abzurufen, aber nicht festzulegen.<br/> |
| [**Name**](folderitem-name.md)<br/>                 | Lesen/Schreiben<br/> | Legt den Namen des Elements fest oder ruft diesen ab.<br/>                                                                                                                                                                           |
| [**Parent**](folderitem-parent.md)<br/>             | Schreibgeschützt<br/>  | Ruft ein -Objekt ab, das das übergeordnete Element des Elements darstellt.<br/>                                                                                                                                                  |
| [**Pfad**](folderitem-path.md)<br/>                 | Schreibgeschützt<br/>  | Enthält den vollständigen Pfad und Namen des Elements.<br/>                                                                                                                                                                 |
| [**Größe**](folderitem-size.md)<br/>                 | Schreibgeschützt<br/>  | Enthält die Größe des Elements.<br/>                                                                                                                                                                               |
| [**Typ**](folderitem-type.md)<br/>                 | Schreibgeschützt<br/>  | Enthält eine Zeichenfolgendarstellung des Elementtyps.<br/>                                                                                                                                                    |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                           |
| Header<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 4.71 oder höher)</dt> </dl> |



 

 




