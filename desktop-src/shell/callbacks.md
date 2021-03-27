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
# <a name="shell-callback-functions"></a><span data-ttu-id="9fd5c-103">Shellrückruf Funktionen</span><span class="sxs-lookup"><span data-stu-id="9fd5c-103">Shell Callback Functions</span></span>

<span data-ttu-id="9fd5c-104">In diesem Abschnitt werden die Windows Shell-Rückruf Funktionen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="9fd5c-104">This section describes the Windows Shell callback functions.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="9fd5c-105">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="9fd5c-105">In this section</span></span>



| <span data-ttu-id="9fd5c-106">Thema</span><span class="sxs-lookup"><span data-stu-id="9fd5c-106">Topic</span></span>                                                                     | <span data-ttu-id="9fd5c-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9fd5c-107">Description</span></span>                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9fd5c-108">[**Bffcallback**](/previous-versions/windows/desktop/legacy/bb762598(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9fd5c-108">[**BFFCALLBACK**](/previous-versions/windows/desktop/legacy/bb762598(v=vs.85))</span></span><br/>                      | <span data-ttu-id="9fd5c-109">Gibt eine Anwendungs definierte Rückruffunktion an, die zum Senden von Nachrichten an und zum Verarbeiten von Nachrichten aus einem **Durchsuchen** -Dialogfeld verwendet wird, das als Reaktion auf einen Aufrufen von [**shbrowseforfolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera)angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="9fd5c-109">Specifies an application-defined callback function used to send messages to, and process messages from, a **Browse** dialog box displayed in response to a call to [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera).</span></span><br/> |
| [<span data-ttu-id="9fd5c-110">*"F"*</span><span class="sxs-lookup"><span data-stu-id="9fd5c-110">*FMExtensionProc*</span></span>](fmextensionproc.md)<br/>                       | <span data-ttu-id="9fd5c-111">Gibt eine Anwendungs definierte Rückruffunktion an, die vom Datei-Manager für die Kommunikation mit einer Datei-Manager-Erweiterung aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="9fd5c-111">Specifies an application-defined callback function called by File Manager to communicate with a File Manager extension.</span></span><br/>                                                                                            |
| [<span data-ttu-id="9fd5c-112">*Mrucmpproc*</span><span class="sxs-lookup"><span data-stu-id="9fd5c-112">*MRUCMPPROC*</span></span>](mrucmpproc.md)<br/>                                 | <span data-ttu-id="9fd5c-113">Wird verwendet, um zu bestimmen, ob ein Element in einer zuletzt verwendeten (MRU-) Liste vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="9fd5c-113">Used to determine whether an item is present in a most recently used (MRU) list.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="9fd5c-114">**pappstate- \_ Änderungs \_ Routine**</span><span class="sxs-lookup"><span data-stu-id="9fd5c-114">**PAPPSTATE\_CHANGE\_ROUTINE**</span></span>](/windows/desktop/api/appnotify/nc-appnotify-pappstate_change_routine)<br/> | <span data-ttu-id="9fd5c-115">Gibt eine APP-definierte Rückruffunktion an, die die APP benachrichtigt, wenn die app in den Status "angehalten" versetzt wird.</span><span class="sxs-lookup"><span data-stu-id="9fd5c-115">Specifies an app-defined callback function that notifies the app when the app is entering or leaving a suspended state.</span></span><br/>                                                                                            |
| [<span data-ttu-id="9fd5c-116">**Subclassproc**</span><span class="sxs-lookup"><span data-stu-id="9fd5c-116">**SUBCLASSPROC**</span></span>](/windows/win32/api/commctrl/nc-commctrl-subclassproc)<br/>                  | <span data-ttu-id="9fd5c-117">Definiert den Prototyp der von [**removewindowsubclass**](/windows/desktop/api/Commctrl/nf-commctrl-removewindowsubclass) und [**setwindowsubclass**](/windows/desktop/api/Commctrl/nf-commctrl-setwindowsubclass)verwendeten Rückruffunktion.</span><span class="sxs-lookup"><span data-stu-id="9fd5c-117">Defines the prototype for the callback function used by [**RemoveWindowSubclass**](/windows/desktop/api/Commctrl/nf-commctrl-removewindowsubclass) and [**SetWindowSubclass**](/windows/desktop/api/Commctrl/nf-commctrl-setwindowsubclass).</span></span><br/>                                                   |
| [<span data-ttu-id="9fd5c-118">**FM- \_ Lösch \_ Vorgang**</span><span class="sxs-lookup"><span data-stu-id="9fd5c-118">**FM\_UNDELETE\_PROC**</span></span>](undeletefile.md)<br/>                     | <span data-ttu-id="9fd5c-119">Gibt eine Anwendungs definierte Rückruffunktion an, die vom Datei-Manager aufgerufen wird, wenn der Benutzer den Befehl " **Undelete** " aus dem Menü **Datei** auswählt.</span><span class="sxs-lookup"><span data-stu-id="9fd5c-119">Specifies an application-defined callback function called by File Manager when the user chooses the **Undelete** command from the **File** menu.</span></span><br/>                                                                   |



 

 

 
