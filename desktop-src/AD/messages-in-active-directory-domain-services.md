---
title: Nachrichten in Active Directory Domain Services
description: Nachrichten in Active Directory Domain Services sind in Windows 2000 und Windows NT 4,0 mit Service Pack 6a (SP6a) und höher mit DSClient funktionsfähig.
ms.assetid: 32a4724b-3182-4521-975c-cef33afee0b2
ms.tgt_platform: multiple
keywords:
- Active Directory Meldungen anzeigen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6895aee711af04778318cf42920d0b0416725205
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340408"
---
# <a name="messages-in-active-directory-domain-services"></a><span data-ttu-id="ecfd0-104">Nachrichten in Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="ecfd0-104">Messages in Active Directory Domain Services</span></span>

<span data-ttu-id="ecfd0-105">Nachrichten in Active Directory Domain Services sind in Windows 2000 und Windows NT 4,0 mit Service Pack 6a (SP6a) und höher mit DSClient funktionsfähig.</span><span class="sxs-lookup"><span data-stu-id="ecfd0-105">Messages in Active Directory Domain Services are functional in Windows 2000 and Windows NT 4.0 with Service Pack 6a (SP6a) and later with DSClient.</span></span> <span data-ttu-id="ecfd0-106">Sie sind auch in Windows 98/95-Arbeitsstationen mit IE 4.01 und höher und DSClient funktionsfähig.</span><span class="sxs-lookup"><span data-stu-id="ecfd0-106">They are also functional in Windows 98/95 workstations with IE4.01 and later and DSClient.</span></span> <span data-ttu-id="ecfd0-107">Wenn jedoch Mehrfachauswahl-Eigenschaften Seiten von der Shell aus gestartet werden, sind die Fehlermeldung " [**WM \_ adsprop \_ Notify \_ Error**](wm-adsprop-notify-error.md) " und die zugehörigen Hilfsfunktionen " [**adspropsenderrormessage**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsenderrormessage) " und " [**adspropshowerrordialog**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog) " nicht funktionsfähig und werden nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ecfd0-107">However, if multiselect property pages are launched from the shell, then the [**WM\_ADSPROP\_NOTIFY\_ERROR**](wm-adsprop-notify-error.md) message and its corresponding helper functions, [**ADsPropSendErrorMessage**](/windows/desktop/api/Adsprop/nf-adsprop-adspropsenderrormessage) and [**ADsPropShowErrorDialog**](/windows/desktop/api/Adsprop/nf-adsprop-adspropshowerrordialog) are not functional and will not be displayed.</span></span> <span data-ttu-id="ecfd0-108">Wenn Mehrfachauswahl-Eigenschaften Seiten innerhalb eines Verwaltungs Tools (z. b. AD-Benutzer und-Computer) gestartet werden, sind alle Meldungen funktionsfähig und verfügbar, die auf den Mehrfachauswahl-Eigenschaften Seiten angezeigt werden können.</span><span class="sxs-lookup"><span data-stu-id="ecfd0-108">If multiselect property pages are launched within an admin tool, for example, AD Users and Computers, then all messages are functional and available to be displayed within the multiselect property pages.</span></span>

<span data-ttu-id="ecfd0-109">Active Directory Domain Services die folgenden Meldungen verwenden:</span><span class="sxs-lookup"><span data-stu-id="ecfd0-109">Active Directory Domain Services use the following messages:</span></span>

-   [<span data-ttu-id="ecfd0-110">**WM- \_ adsprop- \_ Benachrichtigung \_ anwenden**</span><span class="sxs-lookup"><span data-stu-id="ecfd0-110">**WM\_ADSPROP\_NOTIFY\_APPLY**</span></span>](wm-adsprop-notify-apply.md)
-   [<span data-ttu-id="ecfd0-111">**WM- \_ adsprop- \_ Benachrichtigungs \_ Änderung**</span><span class="sxs-lookup"><span data-stu-id="ecfd0-111">**WM\_ADSPROP\_NOTIFY\_CHANGE**</span></span>](wm-adsprop-notify-change.md)
-   [<span data-ttu-id="ecfd0-112">**WM- \_ adsprop- \_ Benachrichtigungs \_ Fehler**</span><span class="sxs-lookup"><span data-stu-id="ecfd0-112">**WM\_ADSPROP\_NOTIFY\_ERROR**</span></span>](wm-adsprop-notify-error.md)
-   [<span data-ttu-id="ecfd0-113">**WM- \_ adsprop \_ Benachrichtigen \_ Beenden**</span><span class="sxs-lookup"><span data-stu-id="ecfd0-113">**WM\_ADSPROP\_NOTIFY\_EXIT**</span></span>](wm-adsprop-notify-exit.md)
-   [<span data-ttu-id="ecfd0-114">**WM- \_ adsprop- \_ Benachrichtigungs \_ Vordergrund**</span><span class="sxs-lookup"><span data-stu-id="ecfd0-114">**WM\_ADSPROP\_NOTIFY\_FOREGROUND**</span></span>](wm-adsprop-notify-foreground.md)
-   [<span data-ttu-id="ecfd0-115">**WM \_ adsprop- \_ Benachrichtigungs \_ paar Benachrichtigen**</span><span class="sxs-lookup"><span data-stu-id="ecfd0-115">**WM\_ADSPROP\_NOTIFY\_PAGEHWND**</span></span>](wm-adsprop-notify-pagehwnd.md)
-   [<span data-ttu-id="ecfd0-116">**WM \_ adsprop \_ benachrichtigt \_ pageingeit**</span><span class="sxs-lookup"><span data-stu-id="ecfd0-116">**WM\_ADSPROP\_NOTIFY\_PAGEINIT**</span></span>](wm-adsprop-notify-pageinit.md)
-   [<span data-ttu-id="ecfd0-117">**WM \_ adsprop \_ Benachrichtigen von \_ SetFocus**</span><span class="sxs-lookup"><span data-stu-id="ecfd0-117">**WM\_ADSPROP\_NOTIFY\_SETFOCUS**</span></span>](wm-adsprop-notify-setfocus.md)
-   [<span data-ttu-id="ecfd0-118">**WM- \_ adsprop- \_ Blatt \_ Erstellen**</span><span class="sxs-lookup"><span data-stu-id="ecfd0-118">**WM\_ADSPROP\_SHEET\_CREATE**</span></span>](wm-adsprop-sheet-create.md)
-   [<span data-ttu-id="ecfd0-119">**WM- \_ DSA- \_ Blatt " \_ Schließen \_ "**</span><span class="sxs-lookup"><span data-stu-id="ecfd0-119">**WM\_DSA\_SHEET\_CLOSE\_NOTIFY**</span></span>](wm-dsa-sheet-close-notify.md)
-   [<span data-ttu-id="ecfd0-120">**WM \_ - \_ Blatt "DSA \_ Erstellen \_ "**</span><span class="sxs-lookup"><span data-stu-id="ecfd0-120">**WM\_DSA\_SHEET\_CREATE\_NOTIFY**</span></span>](wm-dsa-sheet-create-notify.md)

 

 




