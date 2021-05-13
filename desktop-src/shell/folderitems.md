---
description: Stellt die Auflistung von Elementen in einem Shellordner dar. Dieses Objekt enthält Eigenschaften und Methoden, mit denen Sie Informationen über die Auflistung abrufen können.
title: FolderItems-Objekt (Shldisp.h)
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
ms.openlocfilehash: 2b6e9506d6c2354018a41ae7a15ca6e8e1900857
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840651"
---
# <a name="folderitems-object"></a>FolderItems-Objekt

Stellt die Auflistung von Elementen in einem Shellordner dar. Dieses Objekt enthält Eigenschaften und Methoden, mit denen Sie Informationen über die Auflistung abrufen können.

## <a name="members"></a>Member

Das **FolderItems-Objekt** verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **FolderItems-Objekt** verfügt über diese Methoden.



| Methode                                    | BESCHREIBUNG                                                                                              |
|:------------------------------------------|:---------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](folderitems--newenum.md) | Nicht implementiert.<br/>                                                                              |
| [**Element**](folderitems-item.md)          | Ruft das [**FolderItem-Objekt**](folderitem.md) für ein angegebenes Element in der Auflistung ab.<br/> |



 

### <a name="properties"></a>Eigenschaften

Das **FolderItems-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                                  | Zugriffstyp          | BESCHREIBUNG                                                                                                   |
|:----------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------|
| [**Application**](folderitems-application.md)<br/> | Schreibgeschützt<br/> | Enthält das [**Application-Objekt**](folderitems-application.md) der Ordnerelementeauflistung.<br/> |
| [**Count**](folderitems-count.md)<br/>             | Schreibgeschützt<br/> | Enthält die Anzahl der Elemente in der Auflistung.<br/>                                                    |
| [**Parent**](folderitems-parent.md)<br/>           | Schreibgeschützt<br/> | Nicht implementiert.<br/>                                                                                   |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                           |
| Header<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 4.71 oder höher)</dt> </dl> |



 

 




