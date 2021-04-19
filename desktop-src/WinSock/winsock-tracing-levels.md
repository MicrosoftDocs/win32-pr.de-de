---
description: 'Weitere Informationen finden Sie hier: Winsock-Ablauf Verfolgungs Ebenen'
ms.assetid: a92bc4d2-257a-478a-b10d-4fada4323c9b
title: Winsock-Ablauf Verfolgungs Ebenen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b225558015fb823cd02028a1ae1433d3d0549896
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349584"
---
# <a name="winsock-tracing-levels"></a><span data-ttu-id="19b8f-103">Winsock-Ablauf Verfolgungs Ebenen</span><span class="sxs-lookup"><span data-stu-id="19b8f-103">Winsock Tracing Levels</span></span>

## <a name="levels-of-winsock-tracing"></a><span data-ttu-id="19b8f-104">Ebenen der Winsock-Ablauf Verfolgung</span><span class="sxs-lookup"><span data-stu-id="19b8f-104">Levels of Winsock Tracing</span></span>

<span data-ttu-id="19b8f-105">Die Winsock-Ablauf Verfolgung kann auf zwei Ebenen protokolliert werden:</span><span class="sxs-lookup"><span data-stu-id="19b8f-105">There are two levels of logging possible in Winsock tracing:</span></span>

-   <span data-ttu-id="19b8f-106">Information</span><span class="sxs-lookup"><span data-stu-id="19b8f-106">Information</span></span>
-   <span data-ttu-id="19b8f-107">Ausführlich</span><span class="sxs-lookup"><span data-stu-id="19b8f-107">Verbose</span></span>

<span data-ttu-id="19b8f-108">Die Informationsebene verfolgt socketerstellungs-und schließereignisse sowie alle Fehler, die auf dem Socket auftreten.</span><span class="sxs-lookup"><span data-stu-id="19b8f-108">The information level traces socket create and close events, as well as any errors that occur on the socket.</span></span>

<span data-ttu-id="19b8f-109">Die ausführliche Ebene umfasst die Ereignisse auf Informationsebene und fügt zusätzliche Ablauf Verfolgung für Sende-und Empfangs Ereignisse hinzu.</span><span class="sxs-lookup"><span data-stu-id="19b8f-109">The verbose level includes the information level events, and adds additional tracing for send and receive events.</span></span> <span data-ttu-id="19b8f-110">Die ausführliche Protokollierung wird verwendet, um Puffer Beschädigungs Probleme und schlecht geschriebene Anwendungen abzufangen.</span><span class="sxs-lookup"><span data-stu-id="19b8f-110">The verbose logging would be used to catch buffer corruption issues as well as poorly written applications.</span></span>

<span data-ttu-id="19b8f-111">Die Informationen oder die ausführliche Ebene können mit der Winsock-Netzwerk Ereignis Ablauf Verfolgung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="19b8f-111">Either the information or verbose level can be used with the Winsock Network Event tracing.</span></span> <span data-ttu-id="19b8f-112">Die Änderungs Ablauf Verfolgung für den Winsock-Katalog unterstützt nur Informationsebenen.</span><span class="sxs-lookup"><span data-stu-id="19b8f-112">The Winsock Catalog Change tracing supports only information level.</span></span>

## <a name="information-event-tracing"></a><span data-ttu-id="19b8f-113">Ablauf Verfolgung von Informations Ereignissen</span><span class="sxs-lookup"><span data-stu-id="19b8f-113">Information Event Tracing</span></span>

<span data-ttu-id="19b8f-114">In der folgenden Liste sind die Winsock-netzwerkereignissocketvorgänge aufgeführt, die auf der Informationsebene nachverfolgt werden:</span><span class="sxs-lookup"><span data-stu-id="19b8f-114">The following list details those Winsock network event socket operations that are traced at the information level:</span></span>

-   <span data-ttu-id="19b8f-115">Socketerstellung</span><span class="sxs-lookup"><span data-stu-id="19b8f-115">Socket creation</span></span>

    <span data-ttu-id="19b8f-116">Ein Ereignis wird bei der Socketerstellung protokolliert, die zum Verfolgen der Lebensdauer eines Sockets verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="19b8f-116">An event is logged on socket creation which can be used to trace the lifetime of a socket.</span></span> <span data-ttu-id="19b8f-117">Diese Ereignisse umfassen auch Sockets, die durch die Annahme von Verbindungen an einem Abhör Socket erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="19b8f-117">These events also includes sockets created by accepting connections on a listening socket.</span></span>

-   <span data-ttu-id="19b8f-118">Bind</span><span class="sxs-lookup"><span data-stu-id="19b8f-118">Bind</span></span>

    <span data-ttu-id="19b8f-119">Die lokale IP-Adresse wird protokolliert, um die Winsock-Ablauf Verfolgungs Informationen mit den socketaufrufen einer Anwendung zu korrelieren.</span><span class="sxs-lookup"><span data-stu-id="19b8f-119">The local IP address is logged to help correlate the Winsock tracing information to an application's socket calls.</span></span>

-   <span data-ttu-id="19b8f-120">Verbinden</span><span class="sxs-lookup"><span data-stu-id="19b8f-120">Connect</span></span>

    <span data-ttu-id="19b8f-121">Die Remote-IP-Adresse des verbundenen Sockets wird protokolliert, um die Winsock-Ablauf Verfolgungs Informationen mit den socketaufrufen einer Anwendung zu korrelieren.</span><span class="sxs-lookup"><span data-stu-id="19b8f-121">The remote IP address of the connected socket is logged to help correlate the Winsock tracing information to an application's socket calls.</span></span>

-   <span data-ttu-id="19b8f-122">Winsock-initiierte Abbrüche und Abbruch</span><span class="sxs-lookup"><span data-stu-id="19b8f-122">Winsock-initiated aborts and cancels</span></span>

    <span data-ttu-id="19b8f-123">Jedes Mal, wenn Winsock eine Anforderung aktiv abbricht oder abbricht, wird das Ereignis protokolliert.</span><span class="sxs-lookup"><span data-stu-id="19b8f-123">Anytime Winsock actively aborts or cancels a request, the event is logged.</span></span>

-   <span data-ttu-id="19b8f-124">Vom Transport initiierte zurück Stellungen</span><span class="sxs-lookup"><span data-stu-id="19b8f-124">Transport initiated resets</span></span>

    <span data-ttu-id="19b8f-125">Jedes Mal, wenn der zugrunde liegende Transport angibt, dass eine Verbindung zurückgesetzt wurde, wird das Ereignis protokolliert.</span><span class="sxs-lookup"><span data-stu-id="19b8f-125">Anytime the underlying transport indicates a connection has been reset, the event is logged.</span></span>

-   <span data-ttu-id="19b8f-126">Sende-und Empfangs Fehler</span><span class="sxs-lookup"><span data-stu-id="19b8f-126">Send and receive errors</span></span>

    <span data-ttu-id="19b8f-127">Wenn ein Sende-oder Empfangs Aufruf an den zugrunde liegenden Transport fehlschlägt, wird das Ereignis protokolliert.</span><span class="sxs-lookup"><span data-stu-id="19b8f-127">Whenever a send or receive call to the underlying transport fails, the event is logged.</span></span>

-   <span data-ttu-id="19b8f-128">Sockettrennung und-schließen</span><span class="sxs-lookup"><span data-stu-id="19b8f-128">Socket disconnect and close</span></span>

    <span data-ttu-id="19b8f-129">Ein Ereignis wird protokolliert, wenn ein Sockethandle geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="19b8f-129">An event is logged when a socket handle is closed.</span></span>

## <a name="verbose-event-tracing"></a><span data-ttu-id="19b8f-130">Ausführliche Ereignis Ablauf Verfolgung</span><span class="sxs-lookup"><span data-stu-id="19b8f-130">Verbose Event Tracing</span></span>

<span data-ttu-id="19b8f-131">Alle Informations Ereignisse werden auf ausführliche-Ebene verfolgt.</span><span class="sxs-lookup"><span data-stu-id="19b8f-131">All of the information events are traced at the verbose level.</span></span> <span data-ttu-id="19b8f-132">In der folgenden Liste werden die zusätzlichen Winsock-netzwerkereignissocketvorgänge ausführlich erläutert, die auf ausführlicher Ebene verfolgt werden:</span><span class="sxs-lookup"><span data-stu-id="19b8f-132">The following list details those additional Winsock network event socket operations that are traced at the verbose level:</span></span>

-   <span data-ttu-id="19b8f-133">Sende-und Empfangs Puffer</span><span class="sxs-lookup"><span data-stu-id="19b8f-133">Send and receive buffers</span></span>

    <span data-ttu-id="19b8f-134">Ereignisse werden von Benutzer Puffer Adressen und-Längen protokolliert, wenn Sende-und Empfangs Aufrufe an Winsock gesendet werden, und nach Abschluss dieser Aufrufe.</span><span class="sxs-lookup"><span data-stu-id="19b8f-134">Events are logged of user buffer addresses and lengths when send and receive calls are posted to Winsock, as well as upon completion of these calls.</span></span> <span data-ttu-id="19b8f-135">Dies ist nützlich für die Diagnose von Problemen bei der Wiederverwendung von Puffern sowie für die ineffiziente Verwendung von Puffern.</span><span class="sxs-lookup"><span data-stu-id="19b8f-135">This is useful for diagnosing buffer re-use issues as well as inefficient use of buffers.</span></span>

-   <span data-ttu-id="19b8f-136">Socketoptionen</span><span class="sxs-lookup"><span data-stu-id="19b8f-136">Socket options</span></span>

    <span data-ttu-id="19b8f-137">Ein Ereignis wird protokolliert, wenn eine Anwendung bestimmte socketoptionswerte ändert.</span><span class="sxs-lookup"><span data-stu-id="19b8f-137">An event is logged when an application changes certain socket option values.</span></span> <span data-ttu-id="19b8f-138">Zu den protokollierten Optionen zählen \_ beispielsweise sndbuf, \_ rcvbuf, die Option für \_ \_ zirkuläre \_ Warteschlangen und "fonbio".</span><span class="sxs-lookup"><span data-stu-id="19b8f-138">Some of the options logged include SO\_SNDBUF, SO\_RCVBUF, SIO\_ENABLE\_CIRCULAR\_QUEUEING, and FIONBIO.</span></span>

-   <span data-ttu-id="19b8f-139">Wsapoll und SELECT</span><span class="sxs-lookup"><span data-stu-id="19b8f-139">WSAPoll and select</span></span>

    <span data-ttu-id="19b8f-140">Ein Ereignis wird in der Verwendung von [**wsapoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) und [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) -Aufrufen der Anwendung protokolliert, die zum Auffinden von Leistungs Engpässen verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="19b8f-140">An event is logged of an application's usage of [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) and [**select**](/windows/desktop/api/Winsock2/nf-winsock2-select) calls which can be used to find performance bottlenecks.</span></span>

-   <span data-ttu-id="19b8f-141">Winsock-initiierte Abbrüche und Abbruch</span><span class="sxs-lookup"><span data-stu-id="19b8f-141">Winsock-initiated aborts and cancels</span></span>

    <span data-ttu-id="19b8f-142">Jedes Mal, wenn Winsock eine Anforderung aktiv abbricht oder abbricht, wird das Ereignis protokolliert.</span><span class="sxs-lookup"><span data-stu-id="19b8f-142">Anytime Winsock actively aborts or cancels a request, the event is logged.</span></span>

-   <span data-ttu-id="19b8f-143">Ereignis Maske</span><span class="sxs-lookup"><span data-stu-id="19b8f-143">Event mask</span></span>

    <span data-ttu-id="19b8f-144">Ein Ereignis wird von der Ereignis Maske protokolliert, die eine Anwendung für die Verwendung der [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) -Funktion registriert.</span><span class="sxs-lookup"><span data-stu-id="19b8f-144">An event is logged of the event mask an application registers for using the [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) function.</span></span>

-   <span data-ttu-id="19b8f-145">Datagramm</span><span class="sxs-lookup"><span data-stu-id="19b8f-145">Datagram</span></span>

    <span data-ttu-id="19b8f-146">Ein Ereignis wird immer dann protokolliert, wenn ein Datagramm eintrifft und kein Pufferbereich vorhanden ist, in dem es kopiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="19b8f-146">An event is logged whenever a datagram arrives and there is no buffer space in which to copy it.</span></span>

## <a name="related-topics"></a><span data-ttu-id="19b8f-147">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="19b8f-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19b8f-148">Kontrolle über die Winsock-Ablauf Verfolgung</span><span class="sxs-lookup"><span data-stu-id="19b8f-148">Control of Winsock Tracing</span></span>](control-of-winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="19b8f-149">Winsock-Ablauf Verfolgung</span><span class="sxs-lookup"><span data-stu-id="19b8f-149">Winsock Tracing</span></span>](winsock-tracing.md)
</dt> <dt>

[<span data-ttu-id="19b8f-150">Details zur Änderung der Winsock-Katalog Änderung</span><span class="sxs-lookup"><span data-stu-id="19b8f-150">Winsock Catalog Change Tracing Details</span></span>](winsock-layered-service-provider-tracing-event-details.md)
</dt> <dt>

[<span data-ttu-id="19b8f-151">Details der Winsock-Netzwerk Ereignis Ablauf Verfolgung</span><span class="sxs-lookup"><span data-stu-id="19b8f-151">Winsock Network Event Tracing Details</span></span>](winsock-tracing-event-details.md)
</dt> </dl>

 

 
