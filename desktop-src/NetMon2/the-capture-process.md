---
description: Der Aufzeichnungsprozess ist für jede der vier NPP-Schnittstellen identisch.
ms.assetid: f778aba5-8f66-4fc9-830b-f830c364da56
title: Der Erfassungsprozess
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e0ca1987266b7e042713f1d1c292cf63d5e3ccf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104552348"
---
# <a name="the-capture-process"></a><span data-ttu-id="894a7-103">Der Erfassungsprozess</span><span class="sxs-lookup"><span data-stu-id="894a7-103">The Capture Process</span></span>

<span data-ttu-id="894a7-104">Der Aufzeichnungsprozess ist für jede der vier NPP-Schnittstellen identisch.</span><span class="sxs-lookup"><span data-stu-id="894a7-104">The capture process is the same for each of the four NPP interfaces.</span></span> <span data-ttu-id="894a7-105">In jedem Fall umfasst der Prozess Folgendes:</span><span class="sxs-lookup"><span data-stu-id="894a7-105">In each case, the process includes:</span></span>

-   <span data-ttu-id="894a7-106">Abrufen des zu verwendenden NPP-Schnittstellen Objekts</span><span class="sxs-lookup"><span data-stu-id="894a7-106">Obtaining the NPP interface object to use</span></span>
-   <span data-ttu-id="894a7-107">Herstellen einer Verbindung mit dem Netzwerk</span><span class="sxs-lookup"><span data-stu-id="894a7-107">Connecting to the network</span></span>
-   <span data-ttu-id="894a7-108">Starten und anschließendes Beenden der [ *Erfassung*](c.md)</span><span class="sxs-lookup"><span data-stu-id="894a7-108">Starting and then stopping the [*capture*](c.md)</span></span>
-   <span data-ttu-id="894a7-109">Trennen der Verbindung mit dem Netzwerk</span><span class="sxs-lookup"><span data-stu-id="894a7-109">Disconnecting from the network</span></span>

> [!Note]  
> <span data-ttu-id="894a7-110">Wenn Sie das gewünschte Schnittstellen Objekt erhalten, stellen Sie sicher, dass Sie nur die in dieser Schnittstelle enthaltenen Methoden aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="894a7-110">When you obtain the interface object that you want, ensure you call only the methods included in that interface.</span></span> <span data-ttu-id="894a7-111">Die folgende Abbildung zeigt, dass jede Schnittstelle ähnliche Methoden zum Erfassen von Netzwerkdaten bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="894a7-111">The following illustration shows each interface provides similar methods for capturing network data.</span></span> <span data-ttu-id="894a7-112">Ein Fehler wird zurückgegeben, wenn Sie mit einer Schnittstelle eine Verbindung mit dem Netzwerk herstellen und dann versuchen, eine Erfassung mithilfe der Methoden einer anderen Schnittstelle auszuführen.</span><span class="sxs-lookup"><span data-stu-id="894a7-112">An error is returned if you connect to the network with one interface and then try to run a capture using the methods from another interface.</span></span>

 

<span data-ttu-id="894a7-113">Die folgenden Abbildungen zeigen zwei verschiedene Möglichkeiten, wie Sie eine Erfassung durchführen können.</span><span class="sxs-lookup"><span data-stu-id="894a7-113">The following illustrations show two different ways you could run a capture.</span></span> <span data-ttu-id="894a7-114">In der ersten Abbildung wird gezeigt, wie Sie eine oder mehrere sequenzielle Erfassungen ausführen, sodass Sie eine beliebige Anzahl von unabhängigen Erfassungen erstellen können.</span><span class="sxs-lookup"><span data-stu-id="894a7-114">The first illustration shows how to run one or more sequential captures, allowing you to create any number of independent captures.</span></span>

![sequenzielle Erfassung](images/capt1.png)

<span data-ttu-id="894a7-116">Wie oben gezeigt, können Sie nach dem Herstellen einer Verbindung mit dem Netzwerk eine Erfassung beliebig oft starten und Abbrechen, eine neue Erfassung starten und jedes Mal neue Statistiken erstellen, wenn Sie die Erfassung neu starten.</span><span class="sxs-lookup"><span data-stu-id="894a7-116">As shown above, after you connect to the network you can start and stop a capture as many times as you wish, starting a new capture and generating new statistics every time you restart the capture.</span></span> <span data-ttu-id="894a7-117">Bei einer verzögerten Erfassung mit der [**idelta-DC**](idelaydc.md) -Schnittstelle wird z. b. jedes Mal eine neue [*Erfassungs Datei*](c.md) erstellt, wenn Sie die Erfassung neu starten.</span><span class="sxs-lookup"><span data-stu-id="894a7-117">For example, for a delayed capture using the [**IDelaydC**](idelaydc.md) interface, a new [*capture file*](c.md) would be created each time you restarted the capture.</span></span>

<span data-ttu-id="894a7-118">Beachten Sie jedoch, dass Sie jedes Mal, wenn Sie den Erfassungsprozess neu starten, die geeignete Configure-Methode zum Neukonfigurieren der Verbindung abrufen müssen.</span><span class="sxs-lookup"><span data-stu-id="894a7-118">However, also be aware that every time you restart the capture process you must call the appropriate configure method to reconfigure the connection.</span></span> <span data-ttu-id="894a7-119">Für den ersten-Befehl zum Starten der Erfassung wird die Verbindung durch den-Befehl zum Herstellen einer Verbindung mit dem Netzwerk konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="894a7-119">For the initial call to start the capture, the connection is configured by the call to connect to the network.</span></span>

<span data-ttu-id="894a7-120">Die zweite Abbildung zeigt, wie Sie eine einzelne Erfassung ausführen können, indem Sie anhalten und neu starten.</span><span class="sxs-lookup"><span data-stu-id="894a7-120">The second illustration shows how you could run a single capture by pausing and restarting.</span></span>

![einzelne Erfassung durch anhalten und Neustarten](images/capt2.png)

<span data-ttu-id="894a7-122">In diesem Fall können Sie eine Erfassung beliebig oft anhalten und neu starten.</span><span class="sxs-lookup"><span data-stu-id="894a7-122">In this case, you can pause and restart a capture as many times as you want.</span></span> <span data-ttu-id="894a7-123">Bei diesem Ansatz können Sie eine Erfassung ausführen, deren Daten (und die zugehörigen Statistiken) als einzelne Erfassung aufgezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="894a7-123">With this approach, you can run a capture whose data (and its related statistics) are recorded as a single capture.</span></span> <span data-ttu-id="894a7-124">Um z. b. eine verzögerte Erfassung mithilfe der [**idelta-DC**](idelaydc.md) -Schnittstelle auszuführen, werden alle erfassten Netzwerkinformationen in einer einzigen [*Erfassungs Datei*](c.md)gespeichert.</span><span class="sxs-lookup"><span data-stu-id="894a7-124">For example, to perform a delayed capture using the [**IDelaydC**](idelaydc.md) interface, all the captured network information would be saved in a single [*capture file*](c.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="894a7-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="894a7-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="894a7-126">**"Kreatenppinterface"**</span><span class="sxs-lookup"><span data-stu-id="894a7-126">**CreateNPPInterface**</span></span>](createnppinterface.md)
</dt> <dt>

[<span data-ttu-id="894a7-127">**Idelta aydc:: Configure**</span><span class="sxs-lookup"><span data-stu-id="894a7-127">**IDelaydC::Configure**</span></span>](idelaydc-configure.md)
</dt> <dt>

[<span data-ttu-id="894a7-128">**Idelta aydc:: Connect**</span><span class="sxs-lookup"><span data-stu-id="894a7-128">**IDelaydC::Connect**</span></span>](idelaydc-connect.md)
</dt> <dt>

[<span data-ttu-id="894a7-129">**Idelta aydc::D isconnect**</span><span class="sxs-lookup"><span data-stu-id="894a7-129">**IDelaydC::Disconnect**</span></span>](idelaydc-disconnect.md)
</dt> <dt>

[<span data-ttu-id="894a7-130">**Idelta aydc::P ause**</span><span class="sxs-lookup"><span data-stu-id="894a7-130">**IDelaydC::Pause**</span></span>](idelaydc-pause.md)
</dt> <dt>

[<span data-ttu-id="894a7-131">**Idelta aydc:: Resume**</span><span class="sxs-lookup"><span data-stu-id="894a7-131">**IDelaydC::Resume**</span></span>](idelaydc-resume.md)
</dt> <dt>

[<span data-ttu-id="894a7-132">**Idelta aydc:: Start**</span><span class="sxs-lookup"><span data-stu-id="894a7-132">**IDelaydC::Start**</span></span>](idelaydc-start.md)
</dt> <dt>

[<span data-ttu-id="894a7-133">**Idelta aydc:: Beendigung**</span><span class="sxs-lookup"><span data-stu-id="894a7-133">**IDelaydC::Stop**</span></span>](idelaydc-stop.md)
</dt> <dt>

[<span data-ttu-id="894a7-134">**IESP:: Configure**</span><span class="sxs-lookup"><span data-stu-id="894a7-134">**IESP::Configure**</span></span>](iesp-configure.md)
</dt> <dt>

[<span data-ttu-id="894a7-135">**IESP:: Connect**</span><span class="sxs-lookup"><span data-stu-id="894a7-135">**IESP::Connect**</span></span>](iesp-connect.md)
</dt> <dt>

[<span data-ttu-id="894a7-136">**IESP::D isconnect**</span><span class="sxs-lookup"><span data-stu-id="894a7-136">**IESP::Disconnect**</span></span>](iesp-disconnect.md)
</dt> <dt>

[<span data-ttu-id="894a7-137">**IESP::P ause**</span><span class="sxs-lookup"><span data-stu-id="894a7-137">**IESP::Pause**</span></span>](iesp-pause.md)
</dt> <dt>

[<span data-ttu-id="894a7-138">**IESP:: Resume**</span><span class="sxs-lookup"><span data-stu-id="894a7-138">**IESP::Resume**</span></span>](iesp-resume.md)
</dt> <dt>

[<span data-ttu-id="894a7-139">**IESP:: Start**</span><span class="sxs-lookup"><span data-stu-id="894a7-139">**IESP::Start**</span></span>](iesp-start.md)
</dt> <dt>

[<span data-ttu-id="894a7-140">**IESP:: Beendigung**</span><span class="sxs-lookup"><span data-stu-id="894a7-140">**IESP::Stop**</span></span>](iesp-stop.md)
</dt> <dt>

[<span data-ttu-id="894a7-141">**"Iran:: Configure"**</span><span class="sxs-lookup"><span data-stu-id="894a7-141">**IRTC::Configure**</span></span>](irtc-configure.md)
</dt> <dt>

[<span data-ttu-id="894a7-142">**Iran:: Connect**</span><span class="sxs-lookup"><span data-stu-id="894a7-142">**IRTC::Connect**</span></span>](irtc-connect.md)
</dt> <dt>

[<span data-ttu-id="894a7-143">**:D isconnect**</span><span class="sxs-lookup"><span data-stu-id="894a7-143">**IRTC::Disconnect**</span></span>](irtc-disconnect.md)
</dt> <dt>

[<span data-ttu-id="894a7-144">**Iran::P ause**</span><span class="sxs-lookup"><span data-stu-id="894a7-144">**IRTC::Pause**</span></span>](irtc-pause.md)
</dt> <dt>

[<span data-ttu-id="894a7-145">**Iran:: Resume**</span><span class="sxs-lookup"><span data-stu-id="894a7-145">**IRTC::Resume**</span></span>](irtc-resume.md)
</dt> <dt>

[<span data-ttu-id="894a7-146">**"Iran:: Start"**</span><span class="sxs-lookup"><span data-stu-id="894a7-146">**IRTC::Start**</span></span>](irtc-start.md)
</dt> <dt>

[<span data-ttu-id="894a7-147">**Iran:: Beendigung**</span><span class="sxs-lookup"><span data-stu-id="894a7-147">**IRTC::Stop**</span></span>](irtc-stop.md)
</dt> <dt>

[<span data-ttu-id="894a7-148">**IStats:: Configure**</span><span class="sxs-lookup"><span data-stu-id="894a7-148">**IStats::Configure**</span></span>](istats-configure.md)
</dt> <dt>

[<span data-ttu-id="894a7-149">**IStats:: Connect**</span><span class="sxs-lookup"><span data-stu-id="894a7-149">**IStats::Connect**</span></span>](istats-connect.md)
</dt> <dt>

[<span data-ttu-id="894a7-150">**IStats::D isconnect**</span><span class="sxs-lookup"><span data-stu-id="894a7-150">**IStats::Disconnect**</span></span>](istats-disconnect.md)
</dt> <dt>

[<span data-ttu-id="894a7-151">**IStats::P ause**</span><span class="sxs-lookup"><span data-stu-id="894a7-151">**IStats::Pause**</span></span>](istats-pause.md)
</dt> <dt>

[<span data-ttu-id="894a7-152">**IStats:: Resume**</span><span class="sxs-lookup"><span data-stu-id="894a7-152">**IStats::Resume**</span></span>](istats-resume.md)
</dt> <dt>

[<span data-ttu-id="894a7-153">**IStats:: Start**</span><span class="sxs-lookup"><span data-stu-id="894a7-153">**IStats::Start**</span></span>](istats-start.md)
</dt> <dt>

[<span data-ttu-id="894a7-154">**IStats:: Beendigung**</span><span class="sxs-lookup"><span data-stu-id="894a7-154">**IStats::Stop**</span></span>](istats-stop.md)
</dt> </dl>

 

 



