---
title: Verwenden der Windows-Ereignis Sammlung
description: In diesem Abschnitt werden die Themen aufgeführt, in denen die Aufgaben erläutert werden, die mit dem Windows-Ereignis Sammler-SDK ausgeführt werden können. Code Beispiele und Erläuterungen für alle Aufgaben sind in den folgenden Themen enthalten.
ms.assetid: 3396454a-4f43-45d0-951e-3096b9a4a077
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc618ced4cefc7f17fb63b27bb1e097e65b3adac
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106339411"
---
# <a name="using-windows-event-collector"></a><span data-ttu-id="0b72b-104">Verwenden der Windows-Ereignis Sammlung</span><span class="sxs-lookup"><span data-stu-id="0b72b-104">Using Windows Event Collector</span></span>

<span data-ttu-id="0b72b-105">In diesem Abschnitt werden die Themen aufgeführt, in denen die Aufgaben erläutert werden, die mit dem Windows-Ereignis Sammler-SDK ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="0b72b-105">This section lists the topics that explain the tasks that can be accomplished using the Windows Event Collector SDK.</span></span> <span data-ttu-id="0b72b-106">Code Beispiele und Erläuterungen für alle Aufgaben sind in den folgenden Themen enthalten.</span><span class="sxs-lookup"><span data-stu-id="0b72b-106">Code examples and explanations for all the tasks are included in each of the following topics.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="0b72b-107">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="0b72b-107">In This Section</span></span>

-   [<span data-ttu-id="0b72b-108">Erstellen eines vom Collector initiierten Abonnements</span><span class="sxs-lookup"><span data-stu-id="0b72b-108">Creating a Collector Initiated Subscription</span></span>](creating-an-event-collector-subscription.md)

    <span data-ttu-id="0b72b-109">Enthält Informationen und ein C++-Codebeispiel zum Erstellen eines vom Collector initiierten Abonnements.</span><span class="sxs-lookup"><span data-stu-id="0b72b-109">Provides information and a C++ code example for creating a collector-initiated subscription.</span></span> <span data-ttu-id="0b72b-110">Ein vom Collector initiiertes Abonnement ermöglicht Ihnen das Empfangen von Ereignissen auf einem lokalen Computer (dem Ereignis Sammler), die von einem Remote Computer (einer Ereignis Quelle) weitergeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="0b72b-110">A collector-initiated subscription enables you to receive events on a local computer (the event collector) that are forwarded from a remote computer (an event source).</span></span>

-   [<span data-ttu-id="0b72b-111">Einrichten eines von der Quelle initiierten Abonnements</span><span class="sxs-lookup"><span data-stu-id="0b72b-111">Setting up a Source Initiated Subscription</span></span>](setting-up-a-source-initiated-subscription.md)

    <span data-ttu-id="0b72b-112">Enthält Informationen und ein C++-Codebeispiel zum Erstellen eines Quell initiierten Abonnements.</span><span class="sxs-lookup"><span data-stu-id="0b72b-112">Provides information and a C++ code example for creating a source-initiated subscription.</span></span> <span data-ttu-id="0b72b-113">Mit einem Quell initiierten Abonnement können Sie Ereignisse auf einem lokalen Computer (dem Ereignis Sammler) empfangen, die von einem Remote Computer (einer Ereignis Quelle) weitergeleitet werden, ohne die Ereignis Quellen im Abonnement anzugeben.</span><span class="sxs-lookup"><span data-stu-id="0b72b-113">A source-initiated subscription enables you to receive events on a local computer (the event collector) that are forwarded from a remote computer (an event source) without specifying the event sources in the subscription.</span></span>

-   [<span data-ttu-id="0b72b-114">Hinzufügen einer Ereignis Quelle zu einem vom Collector initiierten Abonnement</span><span class="sxs-lookup"><span data-stu-id="0b72b-114">Adding an Event Source to a Collector Initiated Subscription</span></span>](adding-an-event-source-to-an-event-collector-subscription.md)

    <span data-ttu-id="0b72b-115">Enthält Informationen und ein C++-Codebeispiel zum Hinzufügen einer Ereignis Quelle (lokaler Computer oder Remote Computer) zu einem vom Collector initiierten Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0b72b-115">Provides information and a C++ code example for adding an event source (local computer or remote computer) to a collector-initiated subscription.</span></span> <span data-ttu-id="0b72b-116">Ein vom Collector initiiertes Abonnement kann erst mit dem Erfassen von Ereignissen beginnen, wenn dem Abonnement eine Ereignis Quelle hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="0b72b-116">A collector initiated subscription cannot start collecting events until an event source is added to the subscription.</span></span>

-   [<span data-ttu-id="0b72b-117">Erstellen von Hardware Ereignis Abonnements</span><span class="sxs-lookup"><span data-stu-id="0b72b-117">Creating Hardware Event Subscriptions</span></span>](creating-hardware-event-subscriptions.md)

    <span data-ttu-id="0b72b-118">Enthält Informationen zum Erstellen eines Ereignis Abonnements, um Hardware Ereignisse von einem Computer zu empfangen, auf dem ein Baseboard-Verwaltungs Controller (BMC) installiert ist.</span><span class="sxs-lookup"><span data-stu-id="0b72b-118">Provides information about how to create an event subscription in order to receive hardware events from a computer that has a Baseboard Management Controller (BMC) installed.</span></span>

-   [<span data-ttu-id="0b72b-119">Löschen eines Ereignis Sammler Abonnements</span><span class="sxs-lookup"><span data-stu-id="0b72b-119">Deleting an Event Collector Subscription</span></span>](deleting-an-event-collector-subscription.md)

    <span data-ttu-id="0b72b-120">Enthält Informationen und ein C++-Codebeispiel zum Löschen eines Ereignis Sammler Abonnements von einem lokalen Computer.</span><span class="sxs-lookup"><span data-stu-id="0b72b-120">Provides information and a C++ code example for deleting an Event Collector subscription from a local computer.</span></span>

-   [<span data-ttu-id="0b72b-121">Anzeigen der Eigenschaften eines Ereignis Sammler Abonnements</span><span class="sxs-lookup"><span data-stu-id="0b72b-121">Displaying the Properties of an Event Collector Subscription</span></span>](displaying-the-properties-of-an-event-collector-subscription.md)

    <span data-ttu-id="0b72b-122">Stellt Informationen und ein C++-Codebeispiel zum Anzeigen der Eigenschaftswerte eines Ereignis Sammler Abonnements bereit.</span><span class="sxs-lookup"><span data-stu-id="0b72b-122">Provides information and a C++ code example for displaying the property values of an Event Collector subscription.</span></span> <span data-ttu-id="0b72b-123">Eigenschaftswerte können nützliche Informationen bereitstellen, z. b. die Adressen von Ereignis Quellen, den Status des Abonnements und die Ereignis Quellen sowie Informationen zur Übermittlung von Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="0b72b-123">Property values can provide useful information, such as the addresses of event sources, the status of the subscription and event sources, and information about how events are delivered.</span></span>

-   [<span data-ttu-id="0b72b-124">Anzeigen des Status eines Ereignis Sammler Abonnements</span><span class="sxs-lookup"><span data-stu-id="0b72b-124">Displaying the Status of an Event Collector Subscription</span></span>](displaying-the-status-of-an-event-collector-subscription.md)

    <span data-ttu-id="0b72b-125">Enthält Informationen und ein C++-Codebeispiel zum Anzeigen des Lauf Zeit Status von Ereignis Quellen, die einem Ereignis Sammler Abonnement zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="0b72b-125">Provides information and a C++ code example for displaying the run time status of events sources that are associated to an Event Collector subscription.</span></span> <span data-ttu-id="0b72b-126">Dies ermöglicht es Ihnen, Fehlermeldungen anzuzeigen, die helfen können, Probleme zu beheben, die verhindern, dass Ereignisse von einer Ereignis Quelle weitergeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="0b72b-126">This enables you to view error messages that can help solve problems, which prevent an event source from forwarding events.</span></span>

-   [<span data-ttu-id="0b72b-127">Auflisten von Event Collector-Abonnements</span><span class="sxs-lookup"><span data-stu-id="0b72b-127">Listing Event Collector Subscriptions</span></span>](listing-event-collector-subscriptions.md)

    <span data-ttu-id="0b72b-128">Enthält Informationen und ein C++-Codebeispiel zum Auflisten der Abonnements, die auf einem lokalen Computer vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="0b72b-128">Provides information and a C++ code example for listing the subscriptions that exist on a local computer.</span></span> <span data-ttu-id="0b72b-129">Sie können die Abonnement Namen, die in diesem Beispiel abgerufen werden, zum Löschen eines Abonnements, Hinzufügen einer Ereignis Quelle zu einem Abonnement, Abrufen der Eigenschaften eines Abonnements oder Anzeigen des Status eines Abonnements verwenden.</span><span class="sxs-lookup"><span data-stu-id="0b72b-129">You can use the subscription names that are obtained with this example to delete a subscription, add an event source to a subscription, retrieve the properties of a subscription, or view the status of a subscription.</span></span>

-   [<span data-ttu-id="0b72b-130">Entfernen einer Ereignis Quelle aus einem vom Collector initiierten Abonnement</span><span class="sxs-lookup"><span data-stu-id="0b72b-130">Removing an Event Source from a Collector Initiated Subscription</span></span>](removing-an-event-source-from-an-event-collector-subscription.md)

    <span data-ttu-id="0b72b-131">Enthält Informationen und ein C++-Codebeispiel zum Entfernen einer Ereignis Quelle aus einem vom Collector initiierten Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0b72b-131">Provides information and a C++ code example for removing an event source from a collector-initiated subscription.</span></span> <span data-ttu-id="0b72b-132">Sie können eine Ereignis Quelle aus einem vom Collector initiierten Abonnement entfernen, ohne das Abonnement zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="0b72b-132">You can remove an event source from a collector-initiated subscription without disabling the subscription.</span></span>

-   [<span data-ttu-id="0b72b-133">Wiederholungsversuch für ein Ereignis Sammler Abonnement</span><span class="sxs-lookup"><span data-stu-id="0b72b-133">Retrying an Event Collector Subscription</span></span>](retrying-an-event-collector-subscription.md)

    <span data-ttu-id="0b72b-134">Enthält Informationen und ein C++-Codebeispiel zum Wiederholen eines Ereignis Sammler Abonnements, wenn mindestens eine Ereignis Quelle fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="0b72b-134">Provides information and a C++ code example for retrying an Event Collector subscription when one or more event sources have failed.</span></span> <span data-ttu-id="0b72b-135">Sie können eine einzelne Ereignis Quelle wiederholen, oder Sie können das gesamte Abonnement wiederholen.</span><span class="sxs-lookup"><span data-stu-id="0b72b-135">You can retry a single event source or you can retry the entire subscription.</span></span>

 

 




