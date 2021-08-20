---
description: Stellt einen Shellordner dar. Dieses Objekt enthält Eigenschaften und Methoden, mit denen Sie Informationen zum Ordner abrufen können.
ms.assetid: f1e82c61-205e-47c8-bc7c-6a52410a672e
title: Folder-Objekt (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Folder
api_type:
- COM
api_location:
- Shldisp.h
ms.openlocfilehash: baf180149419178b489f3ba00042c561268b36e7b7ed7b0e2afab54b68f78466
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032618"
---
# <a name="folder-object"></a>Ordnerobjekt

Stellt einen Shellordner dar. Dieses Objekt enthält Eigenschaften und Methoden, mit denen Sie Informationen zum Ordner abrufen können.

## <a name="members"></a>Member

Das **Folder-Objekt** weist diese Typen von Membern auf:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **Folder-Objekt** verfügt über diese Methoden.



| Methode                                      | Beschreibung                                                                                                                |
|:--------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------|
| [**CopyHere**](folder-copyhere.md)         | Kopiert ein Element oder Elemente in einen Ordner.<br/>                                                                            |
| [**GetDetailsOf**](folder-getdetailsof.md) | Ruft Details zu einem Element in einem Ordner ab. Beispiel: Größe, Typ oder Zeitpunkt der letzten Änderung.<br/> |
| [**Items**](folder-items.md)               | Ruft ein [**FolderItems-Objekt**](folderitems.md) ab, das die Auflistung der Elemente im Ordner darstellt.<br/>    |
| [**MoveHere**](folder-movehere.md)         | Verschiebt ein Element oder Elemente in diesen Ordner.<br/>                                                                          |
| [**NewFolder**](folder-newfolder.md)       | Erstellt einen neuen Ordner.<br/>                                                                                           |
| [**ParseName**](folder-parsename.md)       | Erstellt ein [**FolderItem-Objekt,**](folderitem.md) das ein angegebenes Element darstellt, und gibt es zurück.<br/>                 |



 

### <a name="properties"></a>Eigenschaften

Das **Folder-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                               | Zugriffstyp          | Beschreibung                                          |
|:-------------------------------------------------------|:---------------------|:-----------------------------------------------------|
| [**Application**](folder-application.md)<br/>   | Schreibgeschützt<br/> | Enthält das Anwendungsobjekt des Ordners.<br/> |
| [**Parent**](folder-parent.md)<br/>             | Schreibgeschützt<br/> | Nicht implementiert.<br/>                          |
| [**ParentFolder**](folder-parentfolder.md)<br/> | Schreibgeschützt<br/> | Enthält das übergeordnete **Folder-Objekt.**<br/>    |
| [**Titel**](folder-title.md)<br/>               | Schreibgeschützt<br/> | Enthält den Titel des Ordners.<br/>         |



 

## <a name="remarks"></a>Hinweise

> [!Note]  
> Nicht alle Methoden werden für alle Ordner implementiert. Beispielsweise wird die [**ParseName-Methode**](folder-parsename.md) nicht für den ordner Systemsteuerung (CSIDL \_ CONTROLS) implementiert. Wenn Sie versuchen, eine nicht implementierte Methode aufzurufen, wird ein 0x800A01BD (Dezimalzahl 445) ausgelöst.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]<br/>                 |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl> |



 

 




