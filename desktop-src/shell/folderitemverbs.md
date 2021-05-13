---
description: Stellt die Auflistung von Verben für ein Element in einem Shellordner dar. Dieses Objekt enthält Eigenschaften und Methoden, mit denen Sie Informationen über die Auflistung abrufen können.
title: FolderItemVerbs-Objekt (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FolderItemVerbs
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 31badb4b-b89e-4294-9dd7-bda716e163b2
ms.openlocfilehash: 8206c2113e2fa60abef41e43e4739b6eefd77dd4
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840605"
---
# <a name="folderitemverbs-object"></a>FolderItemVerbs-Objekt

Stellt die Auflistung von Verben für ein Element in einem Shellordner dar. Dieses Objekt enthält Eigenschaften und Methoden, mit denen Sie Informationen über die Auflistung abrufen können.

## <a name="members"></a>Member

Das **FolderItemVerbs-Objekt** verfügt über die folgenden Membertypen:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **FolderItemVerbs-Objekt** verfügt über diese Methoden.



| Methode                                        | BESCHREIBUNG                                                                                                      |
|:----------------------------------------------|:-----------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](folderitemverbs--newenum.md) | Erstellt ein neues **FolderItemVerbs-Objekt,** das eine Kopie dieses FolderItemVerbs-Objekts ist, und gibt es zurück.<br/>   |
| [**Element**](folderitemverbs-item.md)          | Ruft das [**FolderItemVerb-Objekt**](folderitemverb.md) für ein angegebenes Element in der Auflistung ab.<br/> |



 

### <a name="properties"></a>Eigenschaften

Das **FolderItemVerbs-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                                      | Zugriffstyp          | BESCHREIBUNG                                                |
|:--------------------------------------------------------------|:---------------------|:-----------------------------------------------------------|
| [**Application**](folderitemverbs-application.md)<br/> | Schreibgeschützt<br/> | Nicht implementiert.<br/>                                |
| [**Count**](folderitemverbs-count.md)<br/>             | Schreibgeschützt<br/> | Enthält die Anzahl der Elemente in der Auflistung.<br/> |
| [**Parent**](folderitemverbs-parent.md)<br/>           | Schreibgeschützt<br/> | Nicht implementiert.<br/>                                |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 2000 Professional- und Windows \[ XP-Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                           |
| Header<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 4.71 oder höher)</dt> </dl> |



 

 




