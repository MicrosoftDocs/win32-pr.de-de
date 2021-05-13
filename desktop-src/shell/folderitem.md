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
ms.openlocfilehash: a8b9309e7bd1c8cbcc05360c076db085d0f8b991
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840981"
---
# <a name="folderitem-object"></a>FolderItem-Objekt

Stellt ein Element in einem Shellordner dar. Dieses Objekt enthält Eigenschaften und Methoden, mit denen Sie Informationen zum Element abrufen können.

## <a name="members"></a>Member

Das **FolderItem-Objekt** verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **FolderItem-Objekt** verfügt über diese Methoden.



| Methode                                      | BESCHREIBUNG                                                                                                                                                 |
|:--------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**InvokeVerb**](folderitem-invokeverb.md) | Führt ein Verb für das Element aus.<br/>                                                                                                                     |
| [**Verben**](folderitem-verbs.md)           | Ruft das [**FolderItemVerbs-Objekt**](folderitemverbs.md) des Elements ab. Dieses Objekt ist die Auflistung von Verben, die für das Element ausgeführt werden können.<br/> |



 

### <a name="properties"></a>Eigenschaften

Das **FolderItem-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                                   | Zugriffstyp           | BESCHREIBUNG                                                                                                                                                                                                        |
|:-----------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Application**](folderitem-application.md)<br/>   | Schreibgeschützt<br/>  | Enthält das [**Application-Objekt**](folderitem-application.md) des Ordnerelements.<br/>                                                                                                                   |
| [**GetFolder**](folderitem-getfolder.md)<br/>       | Schreibgeschützt<br/>  | Enthält das [**Folder-Objekt**](folder.md) des Elements, wenn das Element ein Ordner ist.<br/>                                                                                                                           |
| [**GetLink**](folderitem-getlink.md)<br/>           | Schreibgeschützt<br/>  | Enthält das [**ShellLinkObject-Objekt**](shelllinkobject-object.md) des Elements, wenn das Element eine Verknüpfung ist.<br/>                                                                                                |
| [**IsBrowsable**](folderitem-isbrowsable.md)<br/>   | Schreibgeschützt<br/>  | Gibt an, ob das Element in einem Browser oder in einem Windows-Explorer werden kann.<br/>                                                                                                                         |
| [**IsFileSystem**](folderitem-isfilesystem.md)<br/> | Schreibgeschützt<br/>  | Gibt an, ob das Element Teil des Dateisystems ist.<br/>                                                                                                                                                       |
| [**IsFolder**](folderitem-isfolder.md)<br/>         | Schreibgeschützt<br/>  | Gibt an, ob das Element ein Ordner ist.<br/>                                                                                                                                                                      |
| [**Islink**](folderitem-islink.md)<br/>             | Schreibgeschützt<br/>  | Gibt an, ob das Element eine Verknüpfung ist.<br/>                                                                                                                                                               |
| [**ModifyDate**](folderitem-modifydate.md)<br/>     | Lesen/Schreiben<br/> | Legt das Datum und die Uhrzeit der letzten Änderung einer Datei fest oder ruft sie ab. [**ModifyDate kann**](folderitem-modifydate.md) verwendet werden, um das Datum und die Uhrzeit der letzten Änderung eines Ordners abzurufen, kann aber nicht festgelegt werden.<br/> |
| [**Name**](folderitem-name.md)<br/>                 | Lesen/Schreiben<br/> | Legt den Namen des Elements fest oder ruft diesen ab.<br/>                                                                                                                                                                           |
| [**Parent**](folderitem-parent.md)<br/>             | Schreibgeschützt<br/>  | Ruft ein -Objekt ab, das das übergeordnete Element des Elements darstellt.<br/>                                                                                                                                                  |
| [**Pfad**](folderitem-path.md)<br/>                 | Schreibgeschützt<br/>  | Enthält den vollständigen Pfad und Namen des Elements.<br/>                                                                                                                                                                 |
| [**Size**](folderitem-size.md)<br/>                 | Schreibgeschützt<br/>  | Enthält die Größe des Elements.<br/>                                                                                                                                                                               |
| [**type**](folderitem-type.md)<br/>                 | Schreibgeschützt<br/>  | Enthält eine Zeichenfolgendarstellung des Elementtyps.<br/>                                                                                                                                                    |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 2000 Professional- und Windows \[ XP-Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                           |
| Header<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 4.71 oder höher)</dt> </dl> |



 

 




