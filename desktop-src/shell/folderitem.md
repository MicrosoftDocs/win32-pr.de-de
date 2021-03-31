---
description: Stellt ein Element in einem Shellordner dar. Dieses Objekt enthält Eigenschaften und Methoden, mit denen Sie Informationen über das Element abrufen können.
title: FolderItem-Objekt (Shldisp. h)
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
ms.openlocfilehash: a1c66c594a60682ad359ffbcdcd0bf045601051d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484027"
---
# <a name="folderitem-object"></a>FolderItem-Objekt

Stellt ein Element in einem Shellordner dar. Dieses Objekt enthält Eigenschaften und Methoden, mit denen Sie Informationen über das Element abrufen können.

## <a name="members"></a>Member

Das **folderItem** -Objekt verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **folderItem** -Objekt verfügt über diese Methoden.



| Methode                                      | BESCHREIBUNG                                                                                                                                                 |
|:--------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Invokeverb**](folderitem-invokeverb.md) | Führt ein Verb für das Element aus.<br/>                                                                                                                     |
| [**Verben**](folderitem-verbs.md)           | Ruft das [**folderitemverbs**](folderitemverbs.md) -Objekt des Elements ab. Bei diesem Objekt handelt es sich um eine Auflistung von Verben, die für das Element ausgeführt werden können.<br/> |



 

### <a name="properties"></a>Eigenschaften

Das **folderItem** -Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                                   | Zugriffstyp           | BESCHREIBUNG                                                                                                                                                                                                        |
|:-----------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Application**](folderitem-application.md)<br/>   | Schreibgeschützt<br/>  | Enthält das [**Anwendungs**](folderitem-application.md) Objekt des Ordner Elements.<br/>                                                                                                                   |
| [**GetFolder**](folderitem-getfolder.md)<br/>       | Schreibgeschützt<br/>  | Enthält das [**Ordner**](folder.md) Objekt des Elements, wenn es sich bei dem Element um einen Ordner handelt.<br/>                                                                                                                           |
| [**Getlink**](folderitem-getlink.md)<br/>           | Schreibgeschützt<br/>  | Enthält das [**shelllinkobject**](shelllinkobject-object.md) -Objekt des Elements, wenn das Element eine Verknüpfung ist.<br/>                                                                                                |
| [**Isbrowsefähig**](folderitem-isbrowsable.md)<br/>   | Schreibgeschützt<br/>  | Gibt an, ob das Element in einem Browser-oder Windows-Explorer-Frame gehostet werden kann.<br/>                                                                                                                         |
| [**IsFile System**](folderitem-isfilesystem.md)<br/> | Schreibgeschützt<br/>  | Gibt an, ob das Element Teil des Dateisystems ist.<br/>                                                                                                                                                       |
| [**IsFolder**](folderitem-isfolder.md)<br/>         | Schreibgeschützt<br/>  | Gibt an, ob das Element ein Ordner ist.<br/>                                                                                                                                                                      |
| [**IsLink**](folderitem-islink.md)<br/>             | Schreibgeschützt<br/>  | Gibt an, ob das Element eine Verknüpfung ist.<br/>                                                                                                                                                               |
| [**ModifyDate**](folderitem-modifydate.md)<br/>     | Lesen/Schreiben<br/> | Ruft das Datum und die Uhrzeit der letzten Änderung einer Datei ab oder legt diese fest. Mit " [**ModifyDate**](folderitem-modifydate.md) " können das Datum und die Uhrzeit der letzten Änderung eines Ordners abgerufen, jedoch nicht festgelegt werden.<br/> |
| [**Name**](folderitem-name.md)<br/>                 | Lesen/Schreiben<br/> | Legt den Namen des Elements fest oder ruft diesen ab.<br/>                                                                                                                                                                           |
| [**Parent**](folderitem-parent.md)<br/>             | Schreibgeschützt<br/>  | Ruft ein-Objekt ab, das das übergeordnete Element des Elements darstellt.<br/>                                                                                                                                                  |
| [**`Path`**](folderitem-path.md)<br/>                 | Schreibgeschützt<br/>  | Enthält den vollständigen Pfad und den Namen des Elements.<br/>                                                                                                                                                                 |
| [**Size**](folderitem-size.md)<br/>                 | Schreibgeschützt<br/>  | Enthält die Größe des Elements.<br/>                                                                                                                                                                               |
| [**Sorte**](folderitem-type.md)<br/>                 | Schreibgeschützt<br/>  | Enthält eine Zeichen folgen Darstellung des Elementtyps.<br/>                                                                                                                                                    |



 

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, Windows XP \[ Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                           |
| Header<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 4,71 oder höher)</dt> </dl> |



 

 




