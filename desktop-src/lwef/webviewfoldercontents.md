---
title: WebViewFolderContents-Objekt (Shldisp.h)
description: Wird von der Shell für die Verwendung in einer WebView implementiert.
ms.assetid: c9c46e21-2721-43c9-a6f4-38fafbda3798
keywords:
- WebViewFolderContents-Objekt Legacy Windows Umgebungsfeatures
- WebViewFolderContents-Objekt Legacy Windows Environment Features , beschrieben
topic_type:
- apiref
api_name:
- WebViewFolderContents
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 179fe0146f49d0e5172410ca119953a7b3f245af20c0e4c2d83ff78fa23b93e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035958"
---
# <a name="webviewfoldercontents-object"></a>WebViewFolderContents-Objekt

Wird von der Shell für die Verwendung in einer *WebView implementiert.* **WebViewFolderContents** initialisiert sich automatisch mit dem aktuellen Ordner von WebView. Es wird eine Shellordneransicht erstellt, die den Inhalt des Ordners in einem von fünf Formaten anzeigt: Kleines Symbol, großes Symbol, Liste, Details oder Miniaturansicht. Sie ist außerhalb einer WebView ungültig.

Die Methoden und Eigenschaften, die **von WebViewFolderContents verfügbar** gemacht werden, sind identisch mit denen des [**ShellFolderView-Objekts.**](/windows/desktop/shell/shellfolderview)

## <a name="members"></a>Member

Das **WebViewFolderContents-Objekt** verfügt über die folgenden Membertypen:

-   [Ereignisse](#events)
-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="events"></a>Ereignisse

Das **WebViewFolderContents-Objekt** verfügt über diese Ereignisse.



| Ereignis                                                              | Beschreibung                                                                              |
|:-------------------------------------------------------------------|:-----------------------------------------------------------------------------------------|
| [**SelectionChanged**](webviewfoldercontents-selectionchanged.md) | Tritt ein, wenn sich der Auswahlzustand eines Elements oder von Elementen in der Ansicht geändert hat.<br/> |



 

### <a name="methods"></a>Methoden

Das **WebViewFolderContents-Objekt** verfügt über diese Methoden.



| Methode                                                       | Beschreibung                                                                                                          |
|:-------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [**PopupItemMenu**](webviewfoldercontents-popupitemmenu.md) | Erstellt ein Kontextmenü für das angegebene Element und gibt die ausgewählte Befehlszeichenfolge zurück.<br/>                   |
| [**SelectedItems**](webviewfoldercontents-selecteditems.md) | Ruft ein [**FolderItems-Objekt**](../shell/folderitems.md) ab, das alle ausgewählten Elemente in der Ansicht darstellt.<br/> |
| [**SelectItem**](webviewfoldercontents-selectitem.md)       | Legt den Auswahlzustand eines Elements in der Ansicht fest.<br/>                                                          |



 

### <a name="properties"></a>Eigenschaften

Das **WebViewFolderContents-Objekt** verfügt über diese Eigenschaften.



| Eigenschaft                                                            | Zugriffstyp          | Beschreibung                                                                                                                              |
|:--------------------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [**Anwendung**](webviewfoldercontents-application.md)<br/> | Schreibgeschützt<br/> | Nicht implementiert.<br/>                                                                                                              |
| [**FocusedItem**](webviewfoldercontents-focuseditem.md)<br/> | Schreibgeschützt<br/> | Ruft ein [**FolderItem-Objekt**](../shell/folderitem.md) ab, das das Element mit dem Eingabefokus darstellt.<br/>                           |
| [**Ordner**](webviewfoldercontents-folder.md)<br/>           | Schreibgeschützt<br/> | Ruft ein [**Folder-Objekt**](../shell/folder.md) ab, das die Sicht darstellt.<br/>                                                            |
| [**Parent**](webviewfoldercontents-parent.md)<br/>           | Schreibgeschützt<br/> | Nicht implementiert.<br/>                                                                                                              |
| [**Skript**](webviewfoldercontents-script.md)<br/>           | Schreibgeschützt<br/> | Ruft das Skriptobjekt für die Sicht ab.<br/>                                                                                       |
| [**ViewOptions**](webviewfoldercontents-viewoptions.md)<br/> | Schreibgeschützt<br/> | Ruft einen Satz von [**ShellFolderViewOptions-Flags**](/windows/desktop/api/shldisp/ne-shldisp-shellfolderviewoptions) ab, die die aktuellen Optionen der Ansicht angeben.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional nur Windows \[ XP-Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                           |
| Header<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>                           |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 4.71 oder höher)</dt> </dl> |



 

