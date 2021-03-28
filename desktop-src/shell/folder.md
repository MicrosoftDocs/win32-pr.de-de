---
description: Stellt einen Shellordner dar. Dieses Objekt enthält Eigenschaften und Methoden, mit denen Sie Informationen zum Ordner abrufen können.
ms.assetid: f1e82c61-205e-47c8-bc7c-6a52410a672e
title: Folder-Objekt (Shldisp. h)
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
ms.openlocfilehash: d37966b13a182161c1a6248c93eabaf5dfa3597c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524491"
---
# <a name="folder-object"></a>Folder-Objekt

Stellt einen Shellordner dar. Dieses Objekt enthält Eigenschaften und Methoden, mit denen Sie Informationen zum Ordner abrufen können.

## <a name="members"></a>Member

Das **Ordner** Objekt enthält die folgenden Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Das **Folder** -Objekt verfügt über diese Methoden.



| Methode                                      | BESCHREIBUNG                                                                                                                |
|:--------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------|
| [**Copyhere**](folder-copyhere.md)         | Kopiert ein Element oder Elemente in einen Ordner.<br/>                                                                            |
| [**GetDetailsOf**](folder-getdetailsof.md) | Ruft Details zu einem Element in einem Ordner ab. Beispielsweise Größe, Typ oder Zeitpunkt der letzten Änderung.<br/> |
| [**Items**](folder-items.md)               | Ruft ein [**folderitems**](folderitems.md) -Objekt ab, das die Auflistung der Elemente im Ordner darstellt.<br/>    |
| [**Muvehere**](folder-movehere.md)         | Verschiebt ein Element oder Elemente in diesen Ordner.<br/>                                                                          |
| [**NewFolder**](folder-newfolder.md)       | Erstellt einen neuen Ordner.<br/>                                                                                           |
| [**PARSENAME**](folder-parsename.md)       | Erstellt ein [**folderItem**](folderitem.md) -Objekt, das ein bestimmtes Element darstellt, und gibt es zurück.<br/>                 |



 

### <a name="properties"></a>Eigenschaften

Das **Ordner** Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                               | Zugriffstyp          | BESCHREIBUNG                                          |
|:-------------------------------------------------------|:---------------------|:-----------------------------------------------------|
| [**Application**](folder-application.md)<br/>   | Schreibgeschützt<br/> | Enthält das Anwendungs Objekt des Ordners.<br/> |
| [**Parent**](folder-parent.md)<br/>             | Schreibgeschützt<br/> | Nicht implementiert.<br/>                          |
| [**Ordner "Ordner"**](folder-parentfolder.md)<br/> | Schreibgeschützt<br/> | Enthält das übergeordnete **Ordner** Objekt.<br/>    |
| [**Titel**](folder-title.md)<br/>               | Schreibgeschützt<br/> | Enthält den Titel des Ordners.<br/>         |



 

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Nicht alle Methoden werden für alle Ordner implementiert. Beispielsweise ist die Methode " [**Parser Name**](folder-parsename.md) " nicht für den System Steuerungs Ordner (CSIDL-Steuer \_ Elemente) implementiert. Wenn Sie versuchen, eine nicht implementierte Methode aufzurufen, wird ein 0x800a01bd (Decimal 445)-Fehler ausgelöst.

 

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, Windows XP \[ Desktop-Apps\]<br/>                 |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl> |



 

 




