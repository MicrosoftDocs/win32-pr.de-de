---
description: Wenn Sie eine Sitzung löschen oder trennen, wird die Kommunikation beendet. Die Anwendung hat die Möglichkeit, Benutzer Benutzerinformationen zum Zeitpunkt der Trennung zu senden, wenn Sie vom Dienstanbieter unterstützt wird.
ms.assetid: dc348bb2-d564-40f8-afe3-5473c5769fa4
title: Verwerfen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a9bf3705d9b104b8816ce4b493ec6b188c5fe1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958816"
---
# <a name="drop"></a><span data-ttu-id="eafd0-104">Verwerfen</span><span class="sxs-lookup"><span data-stu-id="eafd0-104">Drop</span></span>

<span data-ttu-id="eafd0-105">Wenn Sie eine Sitzung löschen oder trennen, wird die Kommunikation beendet.</span><span class="sxs-lookup"><span data-stu-id="eafd0-105">Dropping or disconnecting a session terminates communication.</span></span> <span data-ttu-id="eafd0-106">Die Anwendung hat die Möglichkeit, Benutzer Benutzerinformationen zum Zeitpunkt der Trennung zu senden, wenn Sie vom Dienstanbieter unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="eafd0-106">The application has the option of sending user-user information at the time of the disconnect, if the service provider supports it.</span></span>

<span data-ttu-id="eafd0-107">Die üblichen Gründe für das Löschen einer Sitzung ist, dass ein Benutzer eine Trennung angefordert hat oder das andere Ende der Sitzung gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="eafd0-107">The usual reasons for dropping a session is a user has requested a disconnect or the other end of the session has dropped.</span></span> <span data-ttu-id="eafd0-108">Ein Drop-Vorgang kann auch aufgerufen werden, wenn TAPI eine Sitzung für die Anwendung anbietet.</span><span class="sxs-lookup"><span data-stu-id="eafd0-108">A drop operation may also be called when TAPI offers a session to the application.</span></span> <span data-ttu-id="eafd0-109">Wenn der Dienstanbieter dies unterstützt, hat dies den Effekt, dass die Anwendung den-Befehl ablehnt.</span><span class="sxs-lookup"><span data-stu-id="eafd0-109">If the service provider supports this, the effect is that the application rejects the call.</span></span>

<span data-ttu-id="eafd0-110">Beim Aufrufen eines Drop-Vorgangs können auch Verwandte Sitzungen beeinträchtigt werden.</span><span class="sxs-lookup"><span data-stu-id="eafd0-110">When invoking a drop operation, related sessions can sometimes be affected as well.</span></span> <span data-ttu-id="eafd0-111">Beispielsweise können durch das Löschen eines Konferenz Aufrufes alle einzelnen Teilnehmer gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="eafd0-111">For example, dropping a conference call can drop all individual participants.</span></span> <span data-ttu-id="eafd0-112">Zustands Änderungs Meldungen werden für alle Aufrufe, deren Status betroffen ist, an die Anwendung gesendet.</span><span class="sxs-lookup"><span data-stu-id="eafd0-112">State change messages are sent to the application for all calls whose state is affected.</span></span>

<span data-ttu-id="eafd0-113">In verschiedenen überbrückenden oder parteigebundenen Konfigurationen wird der-Vorgang möglicherweise nicht durch einen Drop-Vorgang gelöscht, wenn mehrere Parteien den-Befehl aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="eafd0-113">In various bridged or party-line configurations when multiple parties are on the call, a drop operation may not actually clear the call.</span></span> <span data-ttu-id="eafd0-114">Beispielsweise kann der-Befehl in einer überbrückten Situation nicht gelöscht werden, da der Status anderer Stationen des Aufrufes steuern kann.</span><span class="sxs-lookup"><span data-stu-id="eafd0-114">For example, in a bridged situation, the call may not be dropped because the status of other stations on the call may govern.</span></span> <span data-ttu-id="eafd0-115">Stattdessen kann der-Befehl einfach in den inaktiven Zustand geändert werden, während er an anderen Stationen verbunden bleibt.</span><span class="sxs-lookup"><span data-stu-id="eafd0-115">Instead, the call may simply be changed to the inactive state while remaining connected at other stations.</span></span>

<span data-ttu-id="eafd0-116">Nach einem Drop-Vorgang können die Sitzungs-ID und die meisten Ressourcen, die der Sitzung zugeordnet sind, für die meisten Abfrage Vorgänge verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="eafd0-116">Following a drop operation, the session identifier and most resources associated with the session will remain usable for most query operations.</span></span> <span data-ttu-id="eafd0-117">Wenn eine Anwendung diese Ressourcen nicht mehr benötigt, muss Sie [die Sitzung beenden](terminate-a-session-ovr.md) , um Speicher Verluste zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="eafd0-117">When an application no longer requires these resources, it must [terminate the session](terminate-a-session-ovr.md) in order to avoid memory leaks.</span></span>

<span data-ttu-id="eafd0-118">**TAPI 2. x:** Siehe [**linedrop**](/windows/win32/api/tapi/nf-tapi-linedrop).</span><span class="sxs-lookup"><span data-stu-id="eafd0-118">**TAPI 2.x:** See [**lineDrop**](/windows/win32/api/tapi/nf-tapi-linedrop).</span></span>

<span data-ttu-id="eafd0-119">**TAPI 3. x:** Weitere Informationen finden Sie unter [**itbasiccallcontrol::D isconnect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-disconnect).</span><span class="sxs-lookup"><span data-stu-id="eafd0-119">**TAPI 3.x:** See [**ITBasicCallControl::Disconnect**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-disconnect).</span></span>

 

 
