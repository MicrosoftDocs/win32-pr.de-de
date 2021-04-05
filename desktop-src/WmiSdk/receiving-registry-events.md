---
description: Der System Registrierungs Anbieter versucht, für jedes auftretende Ereignis eine Benachrichtigung zu senden.
ms.assetid: 51ef0ccb-02d5-4dac-9c71-a7f4e25a0d00
ms.tgt_platform: multiple
title: Empfangen von Registrierungs Ereignissen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87f0da8c039f83e3d4eb1f51d6b6707d0edd6b3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042005"
---
# <a name="receiving-registry-events"></a><span data-ttu-id="4ea61-103">Empfangen von Registrierungs Ereignissen</span><span class="sxs-lookup"><span data-stu-id="4ea61-103">Receiving Registry Events</span></span>

<span data-ttu-id="4ea61-104">Der System Registrierungs Anbieter versucht, für jedes auftretende Ereignis eine Benachrichtigung zu senden.</span><span class="sxs-lookup"><span data-stu-id="4ea61-104">The System Registry provider attempts to send one notification for every event that occurs.</span></span> <span data-ttu-id="4ea61-105">Der System Registrierungs Anbieter garantiert jedoch nicht, dass der Consumer ein oder alle Ereignisse empfängt.</span><span class="sxs-lookup"><span data-stu-id="4ea61-105">However, the System Registry provider does not guarantee that the consumer will receive any or all events.</span></span> <span data-ttu-id="4ea61-106">Die Ausnahme besteht darin, dass der System Registrierungs Anbieter sicherstellt, dass ein Consumer eine Benachrichtigung für jede Ereignis Registrierung erhält.</span><span class="sxs-lookup"><span data-stu-id="4ea61-106">The exception is that the System Registry provider does ensure that a consumer will receive one notification for each event registration.</span></span>

<span data-ttu-id="4ea61-107">Nehmen wir beispielsweise an, ein Consumer registriert sich für zwei Struktur Änderungs Ereignisse, die eine Benachrichtigung für [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent) -Instanzen anfordern.</span><span class="sxs-lookup"><span data-stu-id="4ea61-107">For example, suppose a consumer registers for two tree change events, requesting notification for [**RegistryTreeChangeEvent**](/previous-versions/windows/desktop/regprov/registrytreechangeevent) instances.</span></span> <span data-ttu-id="4ea61-108">Jede Registrierung hat denselben Hive-Wert (Unterstruktur), aber einen anderen RootPath-Wert.</span><span class="sxs-lookup"><span data-stu-id="4ea61-108">Each registration has the same Hive (subtree) value but a different RootPath value.</span></span> <span data-ttu-id="4ea61-109">Wenn sich die Schlüssel in beiden Pfaden mehrmals ändern, stellt der System Registrierungs Anbieter sicher, dass der Consumer eine Benachrichtigung für jeden Pfad erhält.</span><span class="sxs-lookup"><span data-stu-id="4ea61-109">If keys in both paths change multiple times, the System Registry provider guarantees that the consumer will receive a notification for each path.</span></span> <span data-ttu-id="4ea61-110">Abhängig von der Antwortzeit der Registrierung und des System Registrierungs Anbieters erhält der Consumer möglicherweise so viele Benachrichtigungen wie Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="4ea61-110">Depending on the response time of the registry and the System Registry provider, the consumer may receive as many notifications as there were occurrences of events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4ea61-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4ea61-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4ea61-112">Registrierung für System Registrierungs Ereignisse</span><span class="sxs-lookup"><span data-stu-id="4ea61-112">Registering for System Registry Events</span></span>](registering-for-system-registry-events.md)
</dt> </dl>

 

 
