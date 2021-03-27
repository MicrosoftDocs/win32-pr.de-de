---
description: Stellt die Objekte in einer Ansicht dar und stellt Eigenschaften und Methoden bereit, die zum Abrufen von Informationen über den Inhalt der Ansicht verwendet werden.
ms.assetid: 3b866266-fee0-42f7-a1e0-9adb6cc2e23f
title: Shellfolderview-Objekt (Shldisp. h)
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
ms.openlocfilehash: 79eb172641cbd96e2ed0fa6631bc18718340628f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104994998"
---
# <a name="shellfolderview-object"></a>Shellfolderview-Objekt

Stellt die Objekte in einer Ansicht dar und stellt Eigenschaften und Methoden bereit, die zum Abrufen von Informationen über den Inhalt der Ansicht verwendet werden.

## <a name="members"></a>Member

Das **shellfolderview** -Objekt verfügt über diese Typen von Membern:

-   [Ereignisse](#events)
-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="events"></a>Ereignisse

Das **shellfolderview** -Objekt enthält diese Ereignisse.



| Ereignis                                                        | BESCHREIBUNG                                                                              |
|:-------------------------------------------------------------|:-----------------------------------------------------------------------------------------|
| [**SelectionChanged**](shellfolderview-selectionchanged.md) | Tritt auf, wenn sich der Auswahl Zustand eines Elements oder der Elemente in der Ansicht geändert hat.<br/> |



 

### <a name="methods"></a>Methoden

Das **shellfolderview** -Objekt verfügt über diese Methoden.



| Methode                                                 | BESCHREIBUNG                                                                                                        |
|:-------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------|
| [**Popupitemmenu**](shellfolderview-popupitemmenu.md) | Erstellt ein Kontextmenü für das angegebene Element und gibt die ausgewählte Befehls Zeichenfolge zurück.<br/>                 |
| [**SelectedItems**](shellfolderview-selecteditems.md) | Ruft ein [**folderitems**](folderitems.md) -Objekt ab, das alle ausgewählten Elemente in der Ansicht darstellt.<br/> |
| [**SelectItem**](shellfolderview-selectitem.md)       | Legt den Auswahl Zustand eines Elements in der Ansicht fest.<br/>                                                        |



 

### <a name="properties"></a>Eigenschaften

Das **shellfolderview** -Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                                      | Zugriffstyp          | BESCHREIBUNG                                                                                                  |
|:--------------------------------------------------------------|:---------------------|:-------------------------------------------------------------------------------------------------------------|
| [**Application**](shellfolderview-application.md)<br/> | Schreibgeschützt<br/> | Enthält das Anwendungs Objekt des-Objekts.<br/>                                                         |
| [**FocusedItem**](shellfolderview-focuseditem.md)<br/> | Schreibgeschützt<br/> | Ruft ein [**folderItem**](folderitem.md) -Objekt ab, das das Element darstellt, das den Eingabefokus besitzt.<br/> |
| [**Ordner**](shellfolderview-folder.md)<br/>           | Schreibgeschützt<br/> | Ruft ein [**Ordner**](folder.md) Objekt ab, das die Ansicht darstellt.<br/>                                  |
| [**Parent**](shellfolderview-parent.md)<br/>           | Schreibgeschützt<br/> | Nicht implementiert.<br/>                                                                                  |
| [**Skript**](shellfolderview-script.md)<br/>           | Schreibgeschützt<br/> | Veraltet.<br/>                                                                                       |
| [**Viewoptions**](shellfolderview-viewoptions.md)<br/> | Schreibgeschützt<br/> | Ruft einen Satz von Flags ab, die die aktuellen Optionen der Ansicht angeben.<br/>                                |



 

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, Windows XP \[ Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                           |
| Header<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 4,71 oder höher)</dt> </dl> |
| IID<br/>                      | CLSID \_ shellfolderview<br/>                                                                              |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Shellfolderviewoptions-Flags**](/windows/desktop/api/Shldisp/ne-shldisp-shellfolderviewoptions)
</dt> </dl>

 

 




