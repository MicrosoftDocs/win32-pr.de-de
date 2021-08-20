---
description: In diesem Abschnitt werden die Windows Shell-Rückruffunktionen beschrieben.
title: Shell-Rückruffunktionen
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 617a73d9-e3e6-4def-a5b2-557faa7b03c0
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: d3fd334dd49d2b9cec3322630866fde4a99ccad0b5f253dd7253e551264737a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118460843"
---
# <a name="shell-callback-functions"></a>Shell-Rückruffunktionen

In diesem Abschnitt werden die Windows Shell-Rückruffunktionen beschrieben.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                     | Beschreibung                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**BFFCALLBACK**](/previous-versions/windows/desktop/legacy/bb762598(v=vs.85))<br/>                      | Gibt eine anwendungsdefinierte Rückruffunktion an, die verwendet wird,  um Nachrichten an ein Dialogfeld Durchsuchen zu senden und zu verarbeiten, das als Reaktion auf einen Aufruf von [**SHBrowseForFolder angezeigt wird.**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera)<br/> |
| [*FMExtensionProc*](fmextensionproc.md)<br/>                       | Gibt eine anwendungsdefinierte Rückruffunktion an, die vom Datei-Manager aufgerufen wird, um mit einer Datei-Manager-Erweiterung zu kommunizieren.<br/>                                                                                            |
| [*MRUCMPPROC*](mrucmpproc.md)<br/>                                 | Wird verwendet, um zu bestimmen, ob ein Element in einer LISTE der zuletzt verwendeten Elemente (MRU) vorhanden ist.<br/>                                                                                                                                   |
| [**\_PAPPSTATE-ÄNDERUNGSROUTINE \_**](/windows/desktop/api/appnotify/nc-appnotify-pappstate_change_routine)<br/> | Gibt eine von der App definierte Rückruffunktion an, die die App benachrichtigt, wenn die App in einen angehaltenen Zustand eintritt oder diesen verlässt.<br/>                                                                                            |
| [**UNTERKLASSEPROC**](/windows/win32/api/commctrl/nc-commctrl-subclassproc)<br/>                  | Definiert den Prototyp für die Rückruffunktion, die von [**RemoveWindowSubclass und**](/windows/desktop/api/Commctrl/nf-commctrl-removewindowsubclass) [**SetWindowSubclass verwendet wird.**](/windows/desktop/api/Commctrl/nf-commctrl-setwindowsubclass)<br/>                                                   |
| [**FM \_ UNDELETE \_ PROC**](undeletefile.md)<br/>                     | Gibt eine anwendungsdefinierte Rückruffunktion an, die vom Datei-Manager aufgerufen wird, wenn der Benutzer im Menü Datei den Befehl **Undelete** **(Elete) auswählt.**<br/>                                                                   |



 

 

 
