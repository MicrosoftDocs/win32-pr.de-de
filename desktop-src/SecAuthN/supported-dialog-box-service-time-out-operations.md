---
description: Winlogon implementiert zwei Timeout Vorgänge, eine für sichere Dialogfelder und die andere für die Aktivierung und Beendigung des Bildschirmschoners.
ms.assetid: b1dfd7dc-cc00-4f1a-a157-c60b5d0f0b13
title: Unterstützte Dialog Feld Dienstnutzungsdauer-out-Vorgänge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 274950cadd45cd4e7e3be890da0e4350a4d0c5ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751665"
---
# <a name="supported-dialog-box-service-time-out-operations"></a><span data-ttu-id="5995e-103">Unterstützte Dialog Feld Dienstnutzungsdauer-out-Vorgänge</span><span class="sxs-lookup"><span data-stu-id="5995e-103">Supported Dialog Box Service Time-out Operations</span></span>

<span data-ttu-id="5995e-104">[*Winlogon*](../secgloss/w-gly.md) implementiert zwei Timeout Vorgänge, eine für sichere Dialogfelder und die andere für die Aktivierung und Beendigung des Bildschirmschoners.</span><span class="sxs-lookup"><span data-stu-id="5995e-104">[*Winlogon*](../secgloss/w-gly.md) implements two time-out operations, one for secure dialog boxes and the other for screen saver activation and termination.</span></span>

<span data-ttu-id="5995e-105">Beim Anzeigen eines sicheren Dialog Felds (z. b. Anmeldung oder Entsperren einer Arbeitsstation) kann Winlogon die Dialogfelder mit einem Timeout erreichen und einen geeigneten Ergebniscode an die Dialogfeld Prozedur zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="5995e-105">While displaying a secure dialog box, such as logon or unlocking a workstation, Winlogon can time-out the dialog boxes and return an appropriate result code to the dialog box procedure.</span></span> <span data-ttu-id="5995e-106">Winlogon stellt eine Reihe von Dialogfeld-Unterstützungsfunktionen für die [*Gina*](../secgloss/g-gly.md)bereit.</span><span class="sxs-lookup"><span data-stu-id="5995e-106">Winlogon provides a set of dialog box support functions for the [*GINA*](../secgloss/g-gly.md).</span></span> <span data-ttu-id="5995e-107">Die Gina muss diese Funktionen anstelle ihrer Windows-Entsprechungen verwenden, um sicherzustellen, dass die Gina und Winlogon die entsprechende Kontrolle über die Dialogfelder behalten.</span><span class="sxs-lookup"><span data-stu-id="5995e-107">The GINA must use these functions instead of their Windows counterparts to ensure that the GINA and Winlogon maintain appropriate control over the dialog boxes.</span></span> <span data-ttu-id="5995e-108">Wenn Sie die Winlogon-Versionen dieser Funktionen nicht verwenden, kann dies dazu führen, dass nicht autorisierte Benutzer Zugriff auf das System erhalten.</span><span class="sxs-lookup"><span data-stu-id="5995e-108">Failure to use the Winlogon versions of these functions could result in unauthorized users gaining access to the system.</span></span>

<span data-ttu-id="5995e-109">Die Dienste für das Winlogon-Dialogfeld werden von den folgenden Unterstützungsfunktionen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="5995e-109">Winlogon dialog box services are provided by the following support functions.</span></span>



| <span data-ttu-id="5995e-110">Support-Funktion</span><span class="sxs-lookup"><span data-stu-id="5995e-110">Support function</span></span>                                               | <span data-ttu-id="5995e-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5995e-111">Description</span></span>                                                                                      |
|----------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5995e-112">**Wlxmessagebox**</span><span class="sxs-lookup"><span data-stu-id="5995e-112">**WlxMessageBox**</span></span>](/windows/win32/api/winwlx/nc-winwlx-pwlx_message_box)                         | <span data-ttu-id="5995e-113">Ähnelt der [**MessageBox**](/windows/win32/api/winuser/nf-winuser-messagebox) -Funktion von Windows.</span><span class="sxs-lookup"><span data-stu-id="5995e-113">Similar to the Windows [**MessageBox**](/windows/win32/api/winuser/nf-winuser-messagebox) function.</span></span>                         |
| [<span data-ttu-id="5995e-114">**Wlxdialogbox**</span><span class="sxs-lookup"><span data-stu-id="5995e-114">**WlxDialogBox**</span></span>](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box)                           | <span data-ttu-id="5995e-115">Ähnelt der Windows [**Dialogbox**](/windows/win32/api/winuser/nf-winuser-dialogboxa) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="5995e-115">Similar to the Windows [**DialogBox**](/windows/win32/api/winuser/nf-winuser-dialogboxa) function.</span></span>                           |
| [<span data-ttu-id="5995e-116">**Wlxdialogboxindirekte**</span><span class="sxs-lookup"><span data-stu-id="5995e-116">**WlxDialogBoxIndirect**</span></span>](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_indirect)           | <span data-ttu-id="5995e-117">Ähnelt der Windows [**dialogboxindirekte**](/windows/win32/api/winuser/nf-winuser-dialogboxindirecta) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="5995e-117">Similar to the Windows [**DialogBoxIndirect**](/windows/win32/api/winuser/nf-winuser-dialogboxindirecta) function.</span></span>           |
| [<span data-ttu-id="5995e-118">**Wlxdialogboxparam**</span><span class="sxs-lookup"><span data-stu-id="5995e-118">**WlxDialogBoxParam**</span></span>](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_param)                 | <span data-ttu-id="5995e-119">Ähnelt der Windows [**DialogBoxParam**](/windows/win32/api/winuser/nf-winuser-dialogboxparama) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="5995e-119">Similar to the Windows [**DialogBoxParam**](/windows/win32/api/winuser/nf-winuser-dialogboxparama) function.</span></span>                 |
| [<span data-ttu-id="5995e-120">**Wlxdialogboxderederederetztparam**</span><span class="sxs-lookup"><span data-stu-id="5995e-120">**WlxDialogBoxIndirectParam**</span></span>](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_indirect_param) | <span data-ttu-id="5995e-121">Ähnelt der Windows [**dialogboxderetparam**](/windows/win32/api/winuser/nf-winuser-dialogboxindirectparama) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="5995e-121">Similar to the Windows [**DialogBoxIndirectParam**](/windows/win32/api/winuser/nf-winuser-dialogboxindirectparama) function.</span></span> |



 

<span data-ttu-id="5995e-122">Gina-DLLs können auch wlx- \_ WM- \_ SAS-Nachrichten von Winlogon empfangen.</span><span class="sxs-lookup"><span data-stu-id="5995e-122">GINA DLLs can also receive WLX\_WM\_SAS messages from Winlogon.</span></span> <span data-ttu-id="5995e-123">Diese Nachrichten werden an aktive Dialogfelder gesendet, wenn eine Sicherheits [*Sequenz (Secure Attention Sequence*](../secgloss/s-gly.md) , SAS) empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="5995e-123">These messages are sent to active dialog boxes if an [*secure attention sequence*](../secgloss/s-gly.md) (SAS) is received.</span></span> <span data-ttu-id="5995e-124">Dies ist hilfreich, wenn die Gina gerade aufgefordert wird, die passende PIN für eine [*Smartcard*](../secgloss/s-gly.md)einzugeben, und die Karte aus dem [*Smartcardleser*](../secgloss/r-gly.md)entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="5995e-124">This is useful if the GINA is in the process of prompting for the matching PIN for a [*smart card*](../secgloss/s-gly.md), and the card is removed from the smart card [*reader*](../secgloss/r-gly.md).</span></span> <span data-ttu-id="5995e-125">Winlogon verwendet wlx \_ DLG- \_ SAS als EndDialog-Ergebniscode, wenn ein SAS-Ereignis während eines Dialogfeld Vorgangs auftritt.</span><span class="sxs-lookup"><span data-stu-id="5995e-125">Winlogon uses WLX\_DLG\_SAS as the EndDialog result code when an SAS event occurs during a dialog box operation.</span></span>

<span data-ttu-id="5995e-126">Timeouts werden ebenfalls auf diese Weise übermittelt.</span><span class="sxs-lookup"><span data-stu-id="5995e-126">Time-outs are also delivered in this manner.</span></span> <span data-ttu-id="5995e-127">Eine wlx- \_ WM- \_ SAS-Nachricht wird mit dem wlx- \_ SAS- \_ Typ \_ scrnsvr- \_ Timeout oder dem wlx- \_ SAS- \_ \_ typtimeout gesendet.</span><span class="sxs-lookup"><span data-stu-id="5995e-127">A WLX\_WM\_SAS message is sent with WLX\_SAS\_TYPE\_SCRNSVR\_TIMEOUT or WLX\_SAS\_TYPE\_TIMEOUT.</span></span> <span data-ttu-id="5995e-128">Das Dialogfeld endet mit einem geeigneten Exitcode, damit Gina-Entwickler die Timeout Benachrichtigungen miteinander verbinden können.</span><span class="sxs-lookup"><span data-stu-id="5995e-128">The dialog box will end with an appropriate exit code to allow GINA developers to hook the time-out notifications.</span></span>

<span data-ttu-id="5995e-129">Die Gina-Dialogfelder können von Winlogon mithilfe des Codes wlx DLG-Benutzer Abmeldung beendet werden \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="5995e-129">GINA dialog boxes can be terminated by Winlogon by using the code WLX\_DLG\_USER\_LOGOFF.</span></span> <span data-ttu-id="5995e-130">Dies weist darauf hin, dass sich der Benutzer während der Ausführung des Dialog Felds abgemeldet hat (z. b. durch Aufrufen der [**ExitWindowsEx**](/windows/win32/api/winuser/nf-winuser-exitwindowsex) -Funktion von einem anderen Thread).</span><span class="sxs-lookup"><span data-stu-id="5995e-130">This indicates that the user has logged off during the running of the dialog box (for example, by calling the [**ExitWindowsEx**](/windows/win32/api/winuser/nf-winuser-exitwindowsex) function from another thread).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5995e-131">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5995e-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5995e-132">Winlogon wird initialisiert.</span><span class="sxs-lookup"><span data-stu-id="5995e-132">Initializing Winlogon</span></span>](initializing-winlogon.md)
</dt> <dt>

[<span data-ttu-id="5995e-133">Winlogon-Zustände</span><span class="sxs-lookup"><span data-stu-id="5995e-133">Winlogon States</span></span>](winlogon-states.md)
</dt> <dt>

[<span data-ttu-id="5995e-134">Senden von Nachrichten an die Gina</span><span class="sxs-lookup"><span data-stu-id="5995e-134">Sending Messages to the GINA</span></span>](sending-messages-to-the-gina.md)
</dt> <dt>

[<span data-ttu-id="5995e-135">Winlogon-Unterstützungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="5995e-135">Winlogon Support Functions</span></span>](authentication-functions.md)
</dt> </dl>

 

 
