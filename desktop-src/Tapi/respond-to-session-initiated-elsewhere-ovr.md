---
description: Wenn eine neue Kommunikationssitzung eintrifft, werden TAPI-Anwendungen, die ein Interesse an der Adresse und dem Medientyp registriert haben, eine Ereignis Benachrichtigung gesendet.
ms.assetid: 6074619c-6aa0-4b03-9208-10268682e704
title: Reagieren auf die an anderer Stelle initiierte Sitzung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85e25651b58f8841ac4de9bf14f4d139161c1359
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366267"
---
# <a name="respond-to-session-initiated-elsewhere"></a><span data-ttu-id="df387-103">Reagieren auf die an anderer Stelle initiierte Sitzung</span><span class="sxs-lookup"><span data-stu-id="df387-103">Respond to Session Initiated Elsewhere</span></span>

<span data-ttu-id="df387-104">Wenn eine neue Kommunikationssitzung eintrifft, werden TAPI-Anwendungen, die ein Interesse an der [Adresse](address-ovr.md) und dem [Medientyp](media-type-ovr.md) registriert haben, eine [Ereignis Benachrichtigung](event-notification.md)gesendet.</span><span class="sxs-lookup"><span data-stu-id="df387-104">When a new communications session arrives, TAPI applications that registered an interest in the [address](address-ovr.md) and [media type](media-type-ovr.md) will be sent an [event notification](event-notification.md).</span></span> <span data-ttu-id="df387-105">Nur eine Anwendung erhält Besitz [Rechte](privilege-ovr.md) für die Sitzung.</span><span class="sxs-lookup"><span data-stu-id="df387-105">Only one application will be offered ownership [privileges](privilege-ovr.md) over the session.</span></span> <span data-ttu-id="df387-106">Diese Anwendung kann die Sitzung nicht ablehnen.</span><span class="sxs-lookup"><span data-stu-id="df387-106">This application cannot refuse the session.</span></span>

<span data-ttu-id="df387-107">Der erste Ansichts Zustand einer eingehenden Sitzung ist "Angebot".</span><span class="sxs-lookup"><span data-stu-id="df387-107">The initial call state of an incoming session is offering.</span></span> <span data-ttu-id="df387-108">Während sich der-Befehl im Angebots Zustand befindet, kann eine Anwendung Informationen wie den bearermodus und den Abruf Grund abrufen, wenn die Dienstanbieter diese Informationen bereitgestellt haben und verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="df387-108">While the call is in the offering state, an application can obtain information such as bearer mode and call reason, if the service providers supplied this information and it is available.</span></span> <span data-ttu-id="df387-109">Einige Aufruf Informationen sind möglicherweise nicht sofort verfügbar, z. b. die Aufruferkennung.</span><span class="sxs-lookup"><span data-stu-id="df387-109">Some call information may not be available immediately, such as caller ID.</span></span>

<span data-ttu-id="df387-110">Es gibt sechs einfache Antworten auf eine angebotene Sitzung: " [Answer](answer-ovr.md)", " [Accept](accept-ovr.md)", " [Übergabe](handoffs-ovr.md)", " [Drop](drop-ovr.md)", " [Forward](forward-ovr.md)" und " [Redirect](redirect-ovr.md)</span><span class="sxs-lookup"><span data-stu-id="df387-110">There are six basic responses to an offered session: [answer](answer-ovr.md), [accept](accept-ovr.md), [handoff](handoffs-ovr.md), [drop](drop-ovr.md), [forward](forward-ovr.md), and [redirect](redirect-ovr.md).</span></span> <span data-ttu-id="df387-111">Abhängig vom Dienstanbieter ist der vollständige Satz dieser Vorgänge möglicherweise nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="df387-111">Depending on the service provider, the full set of these operations may not be available.</span></span>

 

 



