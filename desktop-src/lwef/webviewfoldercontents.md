---
title: WebViewFolderContents-Objekt (Shldisp.h)
description: Wird von der Shell für die Verwendung in einer WebView implementiert.
ms.assetid: c9c46e21-2721-43c9-a6f4-38fafbda3798
keywords:
- Webviewfoldercontents-Objekt Legacy Funktionen der Windows-Umgebung
- Webviewfoldercontents-Objekt, ältere Windows-Umgebungs Features, beschrieben
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
ms.openlocfilehash: a9ea2020e2d9baaffbc026692faafc702db14781
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339121"
---
# <a name="webviewfoldercontents-object"></a>Webviewfoldercontents-Objekt

Wird von der Shell für die Verwendung in einer *WebView* implementiert. **Webviewfoldercontents** wird automatisch mit dem aktuellen Ordner von WebView initialisiert. Es wird eine Shell-Ordneransicht erstellt, in der der Inhalt des Ordners in einem von fünf Formaten angezeigt wird: kleines Symbol, großes Symbol, Liste, Details und Miniaturansicht. Er ist außerhalb einer WebView ungültig.

Die von **webviewfoldercontents** verfügbar gemachten Methoden und Eigenschaften sind mit denen des [**shellfolderview**](/windows/desktop/shell/shellfolderview) -Objekts identisch.

## <a name="members"></a>Member

Das **webviewfoldercontents** -Objekt verfügt über folgende Typen von Membern:

-   [Ereignisse](#events)
-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="events"></a>Ereignisse

Das **webviewfoldercontents** -Objekt enthält diese Ereignisse.



| Ereignis                                                              | BESCHREIBUNG                                                                              |
|:-------------------------------------------------------------------|:-----------------------------------------------------------------------------------------|
| [**SelectionChanged**](webviewfoldercontents-selectionchanged.md) | Tritt auf, wenn sich der Auswahl Zustand eines Elements oder der Elemente in der Ansicht geändert hat.<br/> |



 

### <a name="methods"></a>Methoden

Das **webviewfoldercontents** -Objekt verfügt über diese Methoden.



| Methode                                                       | BESCHREIBUNG                                                                                                          |
|:-------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [**Popupitemmenu**](webviewfoldercontents-popupitemmenu.md) | Erstellt ein Kontextmenü für das angegebene Element und gibt die ausgewählte Befehls Zeichenfolge zurück.<br/>                   |
| [**SelectedItems**](webviewfoldercontents-selecteditems.md) | Ruft ein [**folderitems**](../shell/folderitems.md) -Objekt ab, das alle ausgewählten Elemente in der Ansicht darstellt.<br/> |
| [**SelectItem**](webviewfoldercontents-selectitem.md)       | Legt den Auswahl Zustand eines Elements in der Ansicht fest.<br/>                                                          |



 

### <a name="properties"></a>Eigenschaften

Das **webviewfoldercontents** -Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                                            | Zugriffstyp          | BESCHREIBUNG                                                                                                                              |
|:--------------------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------------------------------------------------------------|
| [**Application**](webviewfoldercontents-application.md)<br/> | Schreibgeschützt<br/> | Nicht implementiert.<br/>                                                                                                              |
| [**FocusedItem**](webviewfoldercontents-focuseditem.md)<br/> | Schreibgeschützt<br/> | Ruft ein [**folderItem**](../shell/folderitem.md) -Objekt ab, das das Element darstellt, das den Eingabefokus besitzt.<br/>                           |
| [**Ordner**](webviewfoldercontents-folder.md)<br/>           | Schreibgeschützt<br/> | Ruft ein [**Ordner**](../shell/folder.md) Objekt ab, das die Ansicht darstellt.<br/>                                                            |
| [**Parent**](webviewfoldercontents-parent.md)<br/>           | Schreibgeschützt<br/> | Nicht implementiert.<br/>                                                                                                              |
| [**Skript**](webviewfoldercontents-script.md)<br/>           | Schreibgeschützt<br/> | Ruft das Skript Objekt für die Ansicht ab.<br/>                                                                                       |
| [**Viewoptions**](webviewfoldercontents-viewoptions.md)<br/> | Schreibgeschützt<br/> | Ruft einen Satz von [**shellfolderviewoptions**](/windows/desktop/api/shldisp/ne-shldisp-shellfolderviewoptions) -Flags ab, die die aktuellen Optionen der Ansicht angeben.<br/> |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional, Windows XP \[ Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                           |
| Header<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 4,71 oder höher)</dt> </dl> |



 

