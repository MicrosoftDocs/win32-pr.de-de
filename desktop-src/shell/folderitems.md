---
description: Stellt die Auflistung von Elementen in einem Shellordner dar. Dieses Objekt enthält Eigenschaften und Methoden, mit denen Sie Informationen über die Auflistung abrufen können.
title: Folderitems-Objekt (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItems
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: b99201b3-95e8-4ddd-b338-dee8d107d0a0
ms.openlocfilehash: 6f9a6fa978c64c788cbd224cf3a39454c644a57e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749153"
---
# <a name="folderitems-object"></a>Folderitems-Objekt

Stellt die Auflistung von Elementen in einem Shellordner dar. Dieses Objekt enthält Eigenschaften und Methoden, mit denen Sie Informationen über die Auflistung abrufen können.

## <a name="members"></a>Member

Das **folderitems** -Objekt verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **folderitems** -Objekt verfügt über diese Methoden.



| Methode                                    | BESCHREIBUNG                                                                                              |
|:------------------------------------------|:---------------------------------------------------------------------------------------------------------|
| [**\_"Netwenum"**](folderitems--newenum.md) | Nicht implementiert.<br/>                                                                              |
| [**Element**](folderitems-item.md)          | Ruft das [**folderItem**](folderitem.md) -Objekt für ein angegebenes Element in der Auflistung ab.<br/> |



 

### <a name="properties"></a>Eigenschaften

Das **folderitems** -Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                                  | Zugriffstyp          | BESCHREIBUNG                                                                                                   |
|:----------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------|
| [**Application**](folderitems-application.md)<br/> | Schreibgeschützt<br/> | Enthält das [**Anwendungs**](folderitems-application.md) Objekt der Auflistung der Ordner Elemente.<br/> |
| [**Anzahl**](folderitems-count.md)<br/>             | Schreibgeschützt<br/> | Enthält die Anzahl der Elemente in der Auflistung.<br/>                                                    |
| [**Parent**](folderitems-parent.md)<br/>           | Schreibgeschützt<br/> | Nicht implementiert.<br/>                                                                                   |



 

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, Windows XP \[ Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                           |
| Header<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 4,71 oder höher)</dt> </dl> |



 

 




