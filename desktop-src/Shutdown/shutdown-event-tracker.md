---
description: Mit der Ereignisprotokollierung für das Herunterfahren kann der Benutzer oder die Anwendung den Grund für das Herunterfahren oder Neustarten des Systems dokumentieren.
ms.assetid: 860c014e-1fde-45d1-b366-c279bfcf4079
title: Ereignisprotokollierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4208914149bb84df34e67cca71b40cde66363211
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104345708"
---
# <a name="shutdown-event-tracker"></a><span data-ttu-id="aa971-103">Ereignisprotokollierung</span><span class="sxs-lookup"><span data-stu-id="aa971-103">Shutdown Event Tracker</span></span>

<span data-ttu-id="aa971-104">Mit der Ereignisprotokollierung für das *herunter* fahren kann der Benutzer oder die Anwendung den Grund für das Herunterfahren oder Neustarten des Systems dokumentieren.</span><span class="sxs-lookup"><span data-stu-id="aa971-104">The *Shutdown Event Tracker* enables the user or application to document the reason for shutting down or restarting the system.</span></span> <span data-ttu-id="aa971-105">Der Benutzer wird aufgefordert, Informationen einzugeben, wenn Sie im **Startmenü** **herunter** fahren oder Shutdown.exe verwenden.</span><span class="sxs-lookup"><span data-stu-id="aa971-105">The user is prompted to fill in information when selecting **Shut Down** from the **Start** menu, or when using Shutdown.exe.</span></span> <span data-ttu-id="aa971-106">Entwickler können einen Grund Code beim Aufrufen der Funktionen [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) und [**initiatesystemshutdownetx**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa) einschließen.</span><span class="sxs-lookup"><span data-stu-id="aa971-106">Developers can include a reason code when calling the [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) and [**InitiateSystemShutdownEx**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa) functions.</span></span> <span data-ttu-id="aa971-107">Die Informationen werden im Ereignisprotokoll gespeichert.</span><span class="sxs-lookup"><span data-stu-id="aa971-107">The information is stored in the event log.</span></span>

<span data-ttu-id="aa971-108">**Windows XP:** Diese Funktion ist zwar standardmäßig ab Windows Server 2003 aktiviert, aber Sie müssen Sie unter Windows XP aktivieren.</span><span class="sxs-lookup"><span data-stu-id="aa971-108">**Windows XP:** While this feature is enabled by default starting with Windows Server 2003, you must enable it on Windows XP.</span></span> <span data-ttu-id="aa971-109">Weitere Informationen finden Sie in der Dokumentation für das Herunterfahren der Ereignisprotokollierung, die im System oder auf TechNet enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="aa971-109">For more information, see the documentation for the Shutdown Event Tracker included in the system or on TechNet.</span></span>

<span data-ttu-id="aa971-110">Die Funktionen " [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) " und " [**initiatesystemshutdownetx**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa) " wurden aktualisiert, um die Ursache für das Herunterfahren im *dwReason* -Parameter zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="aa971-110">The [**ExitWindowsEx**](/windows/desktop/api/Winuser/nf-winuser-exitwindowsex) and [**InitiateSystemShutdownEx**](/windows/desktop/api/Winreg/nf-winreg-initiatesystemshutdownexa) functions have been updated to support shutdown reason codes in the *dwReason* parameter.</span></span> <span data-ttu-id="aa971-111">Verwenden Sie die Werte, die in Reason. h definiert sind, um den Grund für das Herunterfahren zu erstellen, oder definieren Sie einen benutzerdefinierten Grund</span><span class="sxs-lookup"><span data-stu-id="aa971-111">Use the values defined in Reason.h to construct a shutdown reason code, or define a custom reason code.</span></span> <span data-ttu-id="aa971-112">Der Grund für das Herunterfahren wird aus einem hauptflag, einem nebenflag und zwei optionalen Flags erstellt.</span><span class="sxs-lookup"><span data-stu-id="aa971-112">A shutdown reason code is constructed from a major flag, a minor flag, and two optional flags.</span></span> <span data-ttu-id="aa971-113">Weitere Informationen finden Sie unter [Grund Codes](system-shutdown-reason-codes.md)für das Herunterfahren des Systems.</span><span class="sxs-lookup"><span data-stu-id="aa971-113">For more information, see [System Shutdown Reason Codes](system-shutdown-reason-codes.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="aa971-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="aa971-114">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="aa971-115">[Ereignisprotokollierung für Herunterfahren (TechNet)](/previous-versions/windows/it-pro/windows-server-2003/cc783475(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="aa971-115">[Shutdown Event Tracker (TechNet)](/previous-versions/windows/it-pro/windows-server-2003/cc783475(v=ws.10))</span></span>
</dt> </dl>

 

 
