---
title: Treiber Meldungen
description: Treiber Meldungen
ms.assetid: ed3748ac-08e6-418e-b345-30c796fa38f3
keywords:
- installierbare Treiber, Meldungen
- installierbare Treiber, benutzerdefinierte Meldungen
- Treiber Meldungen
- benutzerdefinierte Treiber Meldungen
- installierbare Treiber, driverproc-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25e03f9d68254752655be8abe9040a17d44dc0ff
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038854"
---
# <a name="driver-messages"></a><span data-ttu-id="5cfc9-108">Treiber Meldungen</span><span class="sxs-lookup"><span data-stu-id="5cfc9-108">Driver Messages</span></span>

<span data-ttu-id="5cfc9-109">Jede Treiber Meldung besteht aus einem Nachrichten Bezeichner und 2 32-Bit-Parametern.</span><span class="sxs-lookup"><span data-stu-id="5cfc9-109">Each driver message consists of a message identifier and two 32-bit parameters.</span></span> <span data-ttu-id="5cfc9-110">Der Nachrichten Bezeichner ist ein eindeutiger Wert, den die [driverproc](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc) -Funktion prüft, um zu bestimmen, welche Aktion ausgeführt werden soll. Die Bedeutung der Nachrichten Parameter hängt von der Nachricht ab.</span><span class="sxs-lookup"><span data-stu-id="5cfc9-110">The message identifier is a unique value that the [DriverProc](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc) function checks to determine which action to carry out. The meaning of the message parameters depends on the message.</span></span> <span data-ttu-id="5cfc9-111">Die Parameter können Werte oder Adressen darstellen.</span><span class="sxs-lookup"><span data-stu-id="5cfc9-111">The parameters may represent values or addresses.</span></span> <span data-ttu-id="5cfc9-112">In vielen Fällen werden die Parameter nicht verwendet und auf 0 (null) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5cfc9-112">In many cases, the parameters are not used and are set to zero.</span></span>

<span data-ttu-id="5cfc9-113">Treiber Nachrichten können Standard oder Benutzer definiert sein.</span><span class="sxs-lookup"><span data-stu-id="5cfc9-113">Driver messages can be standard or custom.</span></span> <span data-ttu-id="5cfc9-114">Windows sendet Standardtreiber Nachrichten wie z. b. [**drv \_ Open**](drv-open.md), [**drv \_ Close**](drv-close.md)und [**drv \_ configure**](drv-configure.md)an einen installierbaren Treiber als Reaktion auf eine Anforderung zum Öffnen, schließen oder Konfigurieren des Treibers.</span><span class="sxs-lookup"><span data-stu-id="5cfc9-114">Windows sends standard driver messages, such as [**DRV\_OPEN**](drv-open.md), [**DRV\_CLOSE**](drv-close.md), and [**DRV\_CONFIGURE**](drv-configure.md), to an installable driver in response to a request to open, close, or configure the driver.</span></span> <span data-ttu-id="5cfc9-115">Die Standard Meldungen leiten den installierbaren Treiber an, seine Ressourcen zu laden oder zu entladen, den Vorgang zu aktivieren oder zu deaktivieren, eine Treiber Instanz zu öffnen oder zu schließen und ein Konfigurations Dialogfeld anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="5cfc9-115">The standard messages direct the installable driver to load or unload its resources, enable or disable its operation, open or close a driver instance, and display a configuration dialog box.</span></span> <span data-ttu-id="5cfc9-116">Einige Standard Meldungen, wie z. b. [**drv \_ Power**](drv-power.md) und [**drv \_ exitsession**](drv-exitsession.md), benachrichtigen den Treiber über systemweite Ereignisse, die sich auf den Betrieb des Treibers oder auf zugehörige Hardware auswirken.</span><span class="sxs-lookup"><span data-stu-id="5cfc9-116">Some standard messages, such as [**DRV\_POWER**](drv-power.md) and [**DRV\_EXITSESSION**](drv-exitsession.md), notify the driver of system-wide events that affect the operation of the driver or any related hardware.</span></span>

<span data-ttu-id="5cfc9-117">Anwendungen und DLLs senden benutzerdefinierte Treiber Nachrichten, um einen installierbaren Treiber zum Ausführen von treiberspezifischen Aktionen zu leiten.</span><span class="sxs-lookup"><span data-stu-id="5cfc9-117">Applications and DLLs send custom driver messages to direct an installable driver to carry out driver-specific actions.</span></span> <span data-ttu-id="5cfc9-118">Installierbare Treiber, die benutzerdefinierte Nachrichten unterstützen, müssen die entsprechende Verarbeitung in der **driverproc** -Funktion einschließen</span><span class="sxs-lookup"><span data-stu-id="5cfc9-118">Installable drivers that support custom messages must include appropriate processing in the **DriverProc** function.</span></span> <span data-ttu-id="5cfc9-119">Zur Vermeidung von Konflikten zwischen benutzerdefinierten und Standardtreiber Nachrichten müssen benutzerdefinierte Meldungs-IDs Werte aufweisen, die von \_ dem für den drv-Benutzer reservierten drv reichen \_ .</span><span class="sxs-lookup"><span data-stu-id="5cfc9-119">To prevent conflict between custom and standard driver messages, custom message identifiers must have values ranging from DRV\_RESERVED to DRV\_USER.</span></span> <span data-ttu-id="5cfc9-120">An die [defdriverproc](/windows/win32/api/mmiscapi/nf-mmiscapi-defdriverproc) -Funktion übergebene benutzerdefinierte Nachrichten werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="5cfc9-120">Custom messages passed to the [DefDriverProc](/windows/win32/api/mmiscapi/nf-mmiscapi-defdriverproc) function are ignored.</span></span>

 

 