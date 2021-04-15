---
description: Der Antwort Vorgang ist eine typische Anwendung der Antwort auf eine angebotene Kommunikationssitzung. Bei erfolgreicher Ausführung bewirkt dieser Vorgang, dass eine Sitzung in den verbundenen Zustand übergeht.
ms.assetid: 34ac0b34-1d1b-4657-a737-27a4ed9326af
title: Antwort
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e08081b32b7ba3a3a24cde3ec37c1a6118582cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529222"
---
# <a name="answer"></a><span data-ttu-id="43b12-104">Antwort</span><span class="sxs-lookup"><span data-stu-id="43b12-104">Answer</span></span>

<span data-ttu-id="43b12-105">Der Antwort Vorgang ist die typische Reaktion einer Anwendung auf eine angebotene Kommunikationssitzung.</span><span class="sxs-lookup"><span data-stu-id="43b12-105">The answer operation is an application's typical response to an offered communications session.</span></span> <span data-ttu-id="43b12-106">Bei erfolgreicher Ausführung bewirkt dieser Vorgang, dass eine Sitzung in den verbundenen Zustand übergeht.</span><span class="sxs-lookup"><span data-stu-id="43b12-106">If successful, this operation causes a session to transition into the connected state.</span></span>

<span data-ttu-id="43b12-107">In einigen Telefonieumgebungen (wie z. b. ISDN), in denen Benutzer Warnungen vom Anruf Angebot getrennt sind, kann die Anwendung einen Anruf [annehmen](accept-ovr.md) , bevor Sie antwortet oder den *Angebots* Anruf ablehnen ([Drop](drop-ovr.md)) oder [umleiten](redirect-ovr.md) .</span><span class="sxs-lookup"><span data-stu-id="43b12-107">In some telephony environments (like ISDN), where user alerting is separate from call offering, the application has the option to [accept](accept-ovr.md) a call prior to answering or to reject ([drop](drop-ovr.md)) or [redirect](redirect-ovr.md) the *offering* call.</span></span>

<span data-ttu-id="43b12-108">Wenn ein Antwort Vorgang für eine neue Sitzung ausgeführt wird, wenn eine Sitzung bereits aktiv ist, hängt die Auswirkung auf die vorhandene aktive Sitzung von den Funktionen des Dienstanbieters ab.</span><span class="sxs-lookup"><span data-stu-id="43b12-108">If an answer operation is performed for a new session when a session is already active, the effect this has on the existing active session depends on the service provider's capabilities.</span></span> <span data-ttu-id="43b12-109">Der erste Anruf kann nicht beeinträchtigt sein, er kann automatisch gelöscht werden, oder er kann automatisch angehalten werden.</span><span class="sxs-lookup"><span data-stu-id="43b12-109">The first call can be unaffected, it can automatically be dropped, or it can automatically be placed on hold.</span></span> <span data-ttu-id="43b12-110">TAPI sendet die entsprechenden Ereignis Benachrichtigungen zu beiden aufrufen.</span><span class="sxs-lookup"><span data-stu-id="43b12-110">TAPI will send the appropriate event notifications concerning both calls.</span></span>

<span data-ttu-id="43b12-111">Wenn ein Anruf verbunden ist, aber im aktiven Zustand ist, kann er in einer überbrückten Situation mithilfe des Antwort Vorgangs verknüpft werden.</span><span class="sxs-lookup"><span data-stu-id="43b12-111">In a bridged situation, if a call is connected but in the active state, it can be joined using the answer operation.</span></span>

<span data-ttu-id="43b12-112">Die Anwendung hat die Möglichkeit, Benutzer Benutzerinformationen zum Zeitpunkt der Antwort zu senden, wenn Sie vom Dienstanbieter unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="43b12-112">The application has the option to send user-user information at the time of the answer, if the service provider supports it.</span></span>

<span data-ttu-id="43b12-113">**TAPI 2. x:** Siehe [**lineanswer**](/windows/win32/api/tapi/nf-tapi-lineanswer).</span><span class="sxs-lookup"><span data-stu-id="43b12-113">**TAPI 2.x:** See [**lineAnswer**](/windows/win32/api/tapi/nf-tapi-lineanswer).</span></span>

<span data-ttu-id="43b12-114">**TAPI 3. x:** Siehe [**itbasiccallcontrol:: answer**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-answer).</span><span class="sxs-lookup"><span data-stu-id="43b12-114">**TAPI 3.x:** See [**ITBasicCallControl::Answer**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-answer).</span></span>

 

 
