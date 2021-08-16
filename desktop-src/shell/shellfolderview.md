---
description: Stellt die -Objekte in einer Sicht dar und stellt Eigenschaften und Methoden bereit, die zum Abrufen von Informationen über den Inhalt der Sicht verwendet werden.
ms.assetid: 3b866266-fee0-42f7-a1e0-9adb6cc2e23f
title: ShellFolderView-Objekt (Shldisp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShellFolderView
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: a95d57edb7992c9511e34480190580d34ad42da23c64c4297f5e4ebb75a95e73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118452127"
---
# <a name="shellfolderview-object"></a>ShellFolderView-Objekt

Stellt die -Objekte in einer Sicht dar und stellt Eigenschaften und Methoden bereit, die zum Abrufen von Informationen über den Inhalt der Sicht verwendet werden.

## <a name="members"></a>Member

Das **ShellFolderView-Objekt** verfügt über diese Typen von Membern:

-   [Ereignisse](#events)
-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="events"></a>Ereignisse

Das **ShellFolderView-Objekt** verfügt über diese Ereignisse.



| Ereignis                                                        | BESCHREIBUNG                                                                              |
|:-------------------------------------------------------------|:-----------------------------------------------------------------------------------------|
| [**SelectionChanged**](shellfolderview-selectionchanged.md) | Tritt ein, wenn sich der Auswahlzustand eines Elements oder eines Elements in der Ansicht geändert hat.<br/> |



 

### <a name="methods"></a>Methoden

Das **ShellFolderView-Objekt** verfügt über diese Methoden.



| Methode                                                 | BESCHREIBUNG                                                                                                        |
|:-------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------|
| [**PopupItemMenu**](shellfolderview-popupitemmenu.md) | Erstellt ein Kontextmenü für das angegebene Element und gibt die ausgewählte Befehlszeichenfolge zurück.<br/>                 |
| [**SelectedItems**](shellfolderview-selecteditems.md) | Ruft ein [**FolderItems-Objekt**](folderitems.md) ab, das alle ausgewählten Elemente in der Ansicht darstellt.<br/> |
| [**SelectItem**](shellfolderview-selectitem.md)       | Legt den Auswahlzustand eines Elements in der Ansicht fest.<br/>                                                        |



 

### <a name="properties"></a>Eigenschaften

Das **ShellFolderView-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                                      | Zugriffstyp          | BESCHREIBUNG                                                                                                  |
|:--------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------------------------------------|
| [**Application**](shellfolderview-application.md)<br/> | Schreibgeschützt<br/> | Enthält das Application-Objekt des Objekts.<br/>                                                         |
| [**FocusedItem**](shellfolderview-focuseditem.md)<br/> | Schreibgeschützt<br/> | Ruft ein [**FolderItem-Objekt**](folderitem.md) ab, das das Element mit dem Eingabefokus darstellt.<br/> |
| [**Ordner**](shellfolderview-folder.md)<br/>           | Schreibgeschützt<br/> | Ruft ein [**Folder-Objekt**](folder.md) ab, das die Sicht darstellt.<br/>                                  |
| [**Parent**](shellfolderview-parent.md)<br/>           | Schreibgeschützt<br/> | Nicht implementiert.<br/>                                                                                  |
| [**Skript**](shellfolderview-script.md)<br/>           | Schreibgeschützt<br/> | Veraltet.<br/>                                                                                       |
| [**ViewOptions**](shellfolderview-viewoptions.md)<br/> | Schreibgeschützt<br/> | Ruft einen Satz von Flags ab, die die aktuellen Optionen der Ansicht angeben.<br/>                                |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, nur Windows \[ XP-Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                           |
| Header<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 4.71 oder höher)</dt> </dl> |
| IID<br/>                      | CLSID \_ ShellFolderView<br/>                                                                              |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ShellFolderViewOptions-Flags**](/windows/desktop/api/Shldisp/ne-shldisp-shellfolderviewoptions)
</dt> </dl>

 

 




