---
description: Der Hold-Vorgang ermöglicht es einer einzelnen Adresse, mehrere Kommunikationssitzungen zu verarbeiten.
ms.assetid: 65e22e4e-e346-41c2-929a-ba0d1f7f1732
title: Aufbewahrung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2df54b246c5bde5914a14b53dd56b71688d92a5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863231"
---
# <a name="hold"></a><span data-ttu-id="93714-103">Aufbewahrung</span><span class="sxs-lookup"><span data-stu-id="93714-103">Hold</span></span>

<span data-ttu-id="93714-104">Der Hold-Vorgang ermöglicht es einer einzelnen Adresse, mehrere Kommunikationssitzungen zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="93714-104">The hold operation allows a single address to handle multiple communications sessions.</span></span> <span data-ttu-id="93714-105">Durch das Platzieren einer Sitzung auf einer Festplatte wird die Zeile/Adresse des Benutzers für andere Anrufe freigegeben.</span><span class="sxs-lookup"><span data-stu-id="93714-105">Placing a session on a hard hold frees the user's line/address to make other calls.</span></span> <span data-ttu-id="93714-106">Ein-aufruhalte kann in der Regel nicht übertragen oder in einen Konferenzgespräch eingeschlossen werden, aber ein Beratungsgespräch ist möglich.</span><span class="sxs-lookup"><span data-stu-id="93714-106">A call on hard hold typically cannot be transferred or included in a conference call, but a consultation call can.</span></span> <span data-ttu-id="93714-107">Beratungs Anrufe werden mithilfe von [Konferenz](conference-ovr.md) -oder [Übertragungs](transfer-ovr.md) Vorgängen initiiert.</span><span class="sxs-lookup"><span data-stu-id="93714-107">Consultation calls are initiated using [conference](conference-ovr.md) or [transfer](transfer-ovr.md) operations.</span></span>

<span data-ttu-id="93714-108">Nachdem ein Anruf erfolgreich angehalten wurde, wechselt der Anrufstatus in der Regel in den OnHold-Status.</span><span class="sxs-lookup"><span data-stu-id="93714-108">After a call has been successfully placed on hold, the call state typically transitions to the onhold state.</span></span> <span data-ttu-id="93714-109">Während ein-Rückruf aktiv ist, kann die Anwendung Nachrichten zu Zustandsänderungen des gehaltenen Aufrufes empfangen.</span><span class="sxs-lookup"><span data-stu-id="93714-109">While a call is on hold, the application can receive messages about state changes of the held call.</span></span> <span data-ttu-id="93714-110">Wenn die Partei beispielsweise angehalten wird, kann der Status des Aufrufes zu "getrennt" übergehen.</span><span class="sxs-lookup"><span data-stu-id="93714-110">For example, if the held party hangs up, the call state can transition to disconnected.</span></span>

<span data-ttu-id="93714-111">In einer überbrückten Situation wird der anhalte Vorgang durch den Hold-Vorgang möglicherweise nicht angehalten.</span><span class="sxs-lookup"><span data-stu-id="93714-111">In a bridged situation, the hold operation may not actually place the call on hold.</span></span> <span data-ttu-id="93714-112">Der Status anderer Stationen im-Befehl kann Steuern (z. b. Wenn Sie versuchen, einen-Befehl anzuhalten, wenn keine anderen Stationen teilnehmen); Stattdessen kann der-Befehl einfach in den inaktiven Zustand geändert werden, während er an anderen Stationen verbunden bleibt.</span><span class="sxs-lookup"><span data-stu-id="93714-112">The status of other stations on the call can govern (for example, attempting to "hold" a call when other stations are participating is not possible); instead, the call can simply be changed to the inactive state while it remains connected at other stations.</span></span>

<span data-ttu-id="93714-113">Nicht alle Dienstanbieter unterstützen die Verwendung dieses Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="93714-113">Not all service providers support use of this operation.</span></span>

<span data-ttu-id="93714-114">**TAPI 2. x:** Weitere Informationen finden Sie unter [**linehold**](/windows/win32/api/tapi/nf-tapi-linehold), [**lineunhold**](/windows/win32/api/tapi/nf-tapi-lineunhold).</span><span class="sxs-lookup"><span data-stu-id="93714-114">**TAPI 2.x:** See [**lineHold**](/windows/win32/api/tapi/nf-tapi-linehold), [**lineUnhold**](/windows/win32/api/tapi/nf-tapi-lineunhold).</span></span>

<span data-ttu-id="93714-115">**TAPI 3. x:** Siehe [**itbasiccallcontrol:: Hold**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-hold).</span><span class="sxs-lookup"><span data-stu-id="93714-115">**TAPI 3.x:** See [**ITBasicCallControl::Hold**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-hold).</span></span>

 

 
