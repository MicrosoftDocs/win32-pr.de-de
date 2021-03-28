---
description: Anbieter sind Anwendungen, die die Ereignis Ablauf Verfolgungs Instrumentation enthalten.
ms.assetid: b522f16d-8d61-4db3-9194-d965b6d859ec
title: Bereitstellen von Ereignissen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc53daa602662dfabd163560e8e9d69a888be610
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977633"
---
# <a name="providing-events"></a><span data-ttu-id="26619-103">Bereitstellen von Ereignissen</span><span class="sxs-lookup"><span data-stu-id="26619-103">Providing Events</span></span>

<span data-ttu-id="26619-104">Anbieter sind Anwendungen, die die Ereignis Ablauf Verfolgungs Instrumentation enthalten.</span><span class="sxs-lookup"><span data-stu-id="26619-104">Providers are applications that contain event tracing instrumentation.</span></span> <span data-ttu-id="26619-105">Nachdem sich ein Anbieter registriert hat, kann ein Controller die Ereignis Ablauf Verfolgung im Anbieter aktivieren bzw. deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="26619-105">After a provider registers itself, a controller can then enable or disable event tracing in the provider.</span></span> <span data-ttu-id="26619-106">Der Anbieter definiert seine Interpretation, dass er aktiviert oder deaktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="26619-106">The provider defines its interpretation of being enabled or disabled.</span></span> <span data-ttu-id="26619-107">Im Allgemeinen werden von einem aktivierten Anbieter Ereignisse generiert, die nicht von einem deaktivierten Anbieter verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="26619-107">Generally, an enabled provider generates events, and a disabled provider does not.</span></span> <span data-ttu-id="26619-108">Auf diese Weise können Sie der Anwendung die Ereignis Ablauf Verfolgung hinzufügen, ohne dass die Ereignisse immer generiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="26619-108">This lets you add event tracing to your application without requiring that it generate events all the time.</span></span>

<span data-ttu-id="26619-109">In diesem Abschnitt erfahren Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="26619-109">This section shows you how to:</span></span>

-   [<span data-ttu-id="26619-110">Ereignisse schreiben</span><span class="sxs-lookup"><span data-stu-id="26619-110">Write events</span></span>](writing-events.md)
-   [<span data-ttu-id="26619-111">Verwandte Ereignisse schreiben</span><span class="sxs-lookup"><span data-stu-id="26619-111">Write related events</span></span>](writing-related-events-in-an-end-to-end-scenario.md)
-   [<span data-ttu-id="26619-112">Veröffentlichen Ihres Ereignis Schemas für die Freigabe mit Consumern</span><span class="sxs-lookup"><span data-stu-id="26619-112">Publish your event schema to share with consumers</span></span>](publishing-your-event-schema.md)

<span data-ttu-id="26619-113">Informationen zum Steuern von Ereignis Ablauf Verfolgungs Sitzungen finden Sie unter [Steuern von Ereignis Ablauf Verfolgungs Sitzungen](controlling-event-tracing-sessions.md).</span><span class="sxs-lookup"><span data-stu-id="26619-113">For information about controlling event tracing sessions, see [Controlling Event Tracing Sessions](controlling-event-tracing-sessions.md).</span></span> <span data-ttu-id="26619-114">Informationen zum Verarbeiten von Ereignissen von einem Ereignis Ablauf Verfolgungs Anbieter finden Sie unter Verwenden von [Ereignissen](consuming-events.md).</span><span class="sxs-lookup"><span data-stu-id="26619-114">For information about consuming events from an event trace provider, see [Consuming Events](consuming-events.md).</span></span>

 

 



