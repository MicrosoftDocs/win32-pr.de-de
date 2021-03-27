---
description: In diesem Abschnitt werden die Windows Shell-Rückruf Funktionen beschrieben.
title: Shellrückruf Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 617a73d9-e3e6-4def-a5b2-557faa7b03c0
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 4f6ae93437caa740c8c1349690b7e1452a032491
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393450"
---
# <a name="shell-callback-functions"></a>Shellrückruf Funktionen

In diesem Abschnitt werden die Windows Shell-Rückruf Funktionen beschrieben.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                     | BESCHREIBUNG                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Bffcallback**](/previous-versions/windows/desktop/legacy/bb762598(v=vs.85))<br/>                      | Gibt eine Anwendungs definierte Rückruffunktion an, die zum Senden von Nachrichten an und zum Verarbeiten von Nachrichten aus einem **Durchsuchen** -Dialogfeld verwendet wird, das als Reaktion auf einen Aufrufen von [**shbrowseforfolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera)angezeigt wird.<br/> |
| [*"F"*](fmextensionproc.md)<br/>                       | Gibt eine Anwendungs definierte Rückruffunktion an, die vom Datei-Manager für die Kommunikation mit einer Datei-Manager-Erweiterung aufgerufen wird.<br/>                                                                                            |
| [*Mrucmpproc*](mrucmpproc.md)<br/>                                 | Wird verwendet, um zu bestimmen, ob ein Element in einer zuletzt verwendeten (MRU-) Liste vorhanden ist.<br/>                                                                                                                                   |
| [**pappstate- \_ Änderungs \_ Routine**](/windows/desktop/api/appnotify/nc-appnotify-pappstate_change_routine)<br/> | Gibt eine APP-definierte Rückruffunktion an, die die APP benachrichtigt, wenn die app in den Status "angehalten" versetzt wird.<br/>                                                                                            |
| [**Subclassproc**](/windows/win32/api/commctrl/nc-commctrl-subclassproc)<br/>                  | Definiert den Prototyp der von [**removewindowsubclass**](/windows/desktop/api/Commctrl/nf-commctrl-removewindowsubclass) und [**setwindowsubclass**](/windows/desktop/api/Commctrl/nf-commctrl-setwindowsubclass)verwendeten Rückruffunktion.<br/>                                                   |
| [**FM- \_ Lösch \_ Vorgang**](undeletefile.md)<br/>                     | Gibt eine Anwendungs definierte Rückruffunktion an, die vom Datei-Manager aufgerufen wird, wenn der Benutzer den Befehl " **Undelete** " aus dem Menü **Datei** auswählt.<br/>                                                                   |



 

 

 
