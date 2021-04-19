---
description: Winlogon sendet Nachrichten an die Gina, während Dialogfelder angezeigt werden. Diese Nachrichten werden wie folgt in der SAS-Nachricht der wlx-WM gekapselt \_ \_ .
ms.assetid: 3da1c3d2-5116-47c3-98e4-f29b33693c69
title: Senden von Nachrichten an die Gina
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d2f7b5b0d8fbecafad0bcc36c84cf395813f767
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353437"
---
# <a name="sending-messages-to-the-gina"></a><span data-ttu-id="7bad9-104">Senden von Nachrichten an die Gina</span><span class="sxs-lookup"><span data-stu-id="7bad9-104">Sending Messages to the GINA</span></span>

<span data-ttu-id="7bad9-105">[*Winlogon*](../secgloss/w-gly.md) sendet Nachrichten an die [*Gina*](../secgloss/g-gly.md) , während Dialogfelder angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="7bad9-105">[*Winlogon*](../secgloss/w-gly.md) sends messages to the [*GINA*](../secgloss/g-gly.md) while dialog boxes are displayed.</span></span> <span data-ttu-id="7bad9-106">Diese Nachrichten werden wie folgt in der SAS-Nachricht der wlx-WM gekapselt \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="7bad9-106">These messages are all encapsulated in the WLX\_WM\_SAS message as follows.</span></span>



| <span data-ttu-id="7bad9-107">Typ der sicheren Aufmerksamkeit in den wParam-Parameter</span><span class="sxs-lookup"><span data-stu-id="7bad9-107">Secure attention sequence type in wParam parameter</span></span> | <span data-ttu-id="7bad9-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7bad9-108">Description</span></span>                                                                                                                                   |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7bad9-109">wlx \_ SAS \_ Type \_ STRG \_ alt \_ del</span><span class="sxs-lookup"><span data-stu-id="7bad9-109">WLX\_SAS\_TYPE\_CTRL\_ALT\_DEL</span></span>                     | <span data-ttu-id="7bad9-110">Gibt an, dass eine Tastenkombination STRG + ALT + ENTF empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="7bad9-110">Indicates that a CTRL+ALT+DEL key sequence was received.</span></span>                                                                                      |
| <span data-ttu-id="7bad9-111">wlx \_ SAS \_ Type \_ SC \_ Insert</span><span class="sxs-lookup"><span data-stu-id="7bad9-111">WLX\_SAS\_TYPE\_SC\_INSERT</span></span>                         | <span data-ttu-id="7bad9-112">Gibt an, dass eine [*Smartcard*](../secgloss/s-gly.md) in ein kompatibles Gerät eingefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="7bad9-112">Indicates that a [*smart card*](../secgloss/s-gly.md) has been inserted into a compatible device.</span></span> |
| <span data-ttu-id="7bad9-113">wlx \_ SAS \_ Type \_ SC \_ Remove</span><span class="sxs-lookup"><span data-stu-id="7bad9-113">WLX\_SAS\_TYPE\_SC\_REMOVE</span></span>                         | <span data-ttu-id="7bad9-114">Gibt an, dass eine Smartcard von einem kompatiblen Gerät entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="7bad9-114">Indicates that a smart card has been removed from a compatible device.</span></span>                                                                        |
| <span data-ttu-id="7bad9-115">Benutzer Abmeldung zum wlx- \_ SAS- \_ Typ \_ \_</span><span class="sxs-lookup"><span data-stu-id="7bad9-115">WLX\_SAS\_TYPE\_USER\_LOGOFF</span></span>                       | <span data-ttu-id="7bad9-116">Gibt an, dass ein Benutzer eine Abmeldung angefordert hat.</span><span class="sxs-lookup"><span data-stu-id="7bad9-116">Indicates that a user requested logoff.</span></span>                                                                                                       |
| <span data-ttu-id="7bad9-117">\_ \_ \_ scrnsvr-Timeout für wlx-SAS-Typ \_</span><span class="sxs-lookup"><span data-stu-id="7bad9-117">WLX\_SAS\_TYPE\_SCRNSVR\_TIMEOUT</span></span>                   | <span data-ttu-id="7bad9-118">Gibt an, dass der Bildschirmschoner aufgrund fehlender Benutzereingaben ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7bad9-118">Indicates that the screen saver should be run due to lack of user input.</span></span>                                                                      |
| <span data-ttu-id="7bad9-119">Timeout für wlx- \_ SAS- \_ Typ \_</span><span class="sxs-lookup"><span data-stu-id="7bad9-119">WLX\_SAS\_TYPE\_TIMEOUT</span></span>                            | <span data-ttu-id="7bad9-120">Gibt an, dass innerhalb des angegebenen Timeout Zeitraums keine Benutzereingaben empfangen wurden.</span><span class="sxs-lookup"><span data-stu-id="7bad9-120">Indicates that no user input was received within the specified time-out period.</span></span>                                                               |



 

<span data-ttu-id="7bad9-121">Bei Timeouts und Abmelde Vorgängen schließt Winlogon das Dialogfeld, nachdem die Nachricht gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="7bad9-121">For time-outs and logoffs, Winlogon will close the dialog box after the message has been sent.</span></span> <span data-ttu-id="7bad9-122">Diese Meldung wird gesendet, sodass der Dialogfeld Vorgang auf nützliche Weise reagieren kann (z. b. durch Schließen des Abmelde Vorgangs, wenn eine Abmeldung aufgetreten ist).</span><span class="sxs-lookup"><span data-stu-id="7bad9-122">This message is sent so the dialog box operation can respond in a useful manner (for example, by closing itself down if a logoff has occurred).</span></span>

<span data-ttu-id="7bad9-123">Bei Eingabe Timeouts wird das Dialogfeld mit dem Code wlx \_ DLG \_ input \_ Timeout geschlossen.</span><span class="sxs-lookup"><span data-stu-id="7bad9-123">For input time-outs, the dialog box is closed with the code WLX\_DLG\_INPUT\_TIMEOUT.</span></span>

<span data-ttu-id="7bad9-124">Für Bildschirmschoner-Timeouts wird das Dialogfeld mit dem Code wlx \_ DLG \_ Screen \_ Saver Timeout geschlossen \_ .</span><span class="sxs-lookup"><span data-stu-id="7bad9-124">For screen saver time-outs, the dialog box is closed with the code WLX\_DLG\_SCREEN\_SAVER\_TIMEOUT.</span></span>

<span data-ttu-id="7bad9-125">Bei Abmelde Vorgängen wird der Dialogfeld Vorgang mit dem Code wlx DLG-Benutzer Abmeldung geschlossen \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="7bad9-125">For logoffs, the dialog box operation is closed with the code WLX\_DLG\_USER\_LOGOFF.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7bad9-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7bad9-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7bad9-127">Winlogon wird initialisiert.</span><span class="sxs-lookup"><span data-stu-id="7bad9-127">Initializing Winlogon</span></span>](initializing-winlogon.md)
</dt> <dt>

[<span data-ttu-id="7bad9-128">Winlogon-Zustände</span><span class="sxs-lookup"><span data-stu-id="7bad9-128">Winlogon States</span></span>](winlogon-states.md)
</dt> <dt>

[<span data-ttu-id="7bad9-129">Unterstützte Dialog Feld Dienstnutzungsdauer-out-Vorgänge</span><span class="sxs-lookup"><span data-stu-id="7bad9-129">Supported Dialog Box Service Time-out Operations</span></span>](supported-dialog-box-service-time-out-operations.md)
</dt> <dt>

[<span data-ttu-id="7bad9-130">Winlogon-Unterstützungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="7bad9-130">Winlogon Support Functions</span></span>](authentication-functions.md)
</dt> </dl>

 

 
