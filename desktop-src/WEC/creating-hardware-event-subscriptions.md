---
title: Erstellen von Hardware Ereignis Abonnements
description: Auf Computern, auf denen ein Baseboard-Verwaltungs Controller (BMC) installiert ist, werden Hardware Ereignisse ausgelöst und im System Ereignisprotokoll (SEL) protokolliert, bei dem es sich um den BMC-Ereignisspeicher handelt, der in nichtflüchtigem Speicher gespeichert ist.
ms.assetid: 646ab546-500e-44ee-8b08-2f835e57e3e6
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bc5f904e74d1f29b0666c9cb02b13689a0633bc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315915"
---
# <a name="creating-hardware-event-subscriptions"></a><span data-ttu-id="97ef4-103">Erstellen von Hardware Ereignis Abonnements</span><span class="sxs-lookup"><span data-stu-id="97ef4-103">Creating Hardware Event Subscriptions</span></span>

<span data-ttu-id="97ef4-104">Auf Computern, auf denen ein Baseboard-Verwaltungs Controller (BMC) installiert ist, werden Hardware Ereignisse ausgelöst und im System Ereignisprotokoll (SEL) protokolliert, bei dem es sich um den BMC-Ereignisspeicher handelt, der in nichtflüchtigem Speicher gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="97ef4-104">On computers that have a Baseboard Management Controller (BMC) installed, hardware events are raised and logged in the System event log (SEL), which is the BMC event store that is stored in nonvolatile memory.</span></span> <span data-ttu-id="97ef4-105">Um diese Hardware Ereignisse unter Windows Server 2008 mithilfe des Ereignisanzeige zu lesen, müssen Sie ein Abonnement für die Ereignisse erstellen.</span><span class="sxs-lookup"><span data-stu-id="97ef4-105">To read these hardware events on Windows Server 2008 using the Event Viewer, you must create a subscription to the events.</span></span> <span data-ttu-id="97ef4-106">Die Hardware Ereignis Abonnements funktionieren nur auf Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="97ef4-106">The hardware event subscriptions will only work on Windows Server 2008.</span></span>

<span data-ttu-id="97ef4-107">Das folgende Verfahren definiert, wie das SEL-Ereignis Abonnement zum Abrufen der Hardware Ereignisse erstellt wird:</span><span class="sxs-lookup"><span data-stu-id="97ef4-107">The following procedure defines how to create the SEL event subscription to retrieve the hardware events:</span></span>

1.  <span data-ttu-id="97ef4-108">Speichern Sie den folgenden XML-Code in einer XML-Datei (in diesem Beispiel heißt die Datei Wsmanselrg.xml).</span><span class="sxs-lookup"><span data-stu-id="97ef4-108">Save the following XML in an .xml file (in this example the file is named Wsmanselrg.xml).</span></span> <span data-ttu-id="97ef4-109">Dieser XML-Code definiert das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="97ef4-109">This XML defines the subscription.</span></span>

    ```XML
    <Subscription xmlns="http://schemas.microsoft.com/2006/03/windows/events/subscription">
        <Description>A subscription for the HardwareEvents</Description>
        <SubscriptionId>WSManSelRg</SubscriptionId>
        <Uri>http://schemas.microsoft.com/wbem/wsman/1/logrecord/sel</Uri>
        <EventSources>
            <EventSource>
                <Address>LOCALHOST</Address>
            </EventSource>
        </EventSources>
        <LogFile>HardwareEvents</LogFile>
        <Delivery Mode="pull">
            <PushSettings>
                <Heartbeat Interval="10000"/>
            </PushSettings>
        </Delivery>
    </Subscription>
    ```

    

2.  <span data-ttu-id="97ef4-110">Erstellen Sie ein Ereignis Abonnement, indem Sie den folgenden Befehl in einem Eingabe Aufforderungs Fenster ausführen (das Wecutil.exe Programm befindet sich im Verzeichnis% systemroot% \\ system32.):</span><span class="sxs-lookup"><span data-stu-id="97ef4-110">Create an event subscription by executing the following command in a command prompt window (the Wecutil.exe program is located in the %SYSTEMROOT%\\System32 directory.):</span></span>

    <span data-ttu-id="97ef4-111">**Wecutil** - *<path> \\wsmanselrg.xml*</span><span class="sxs-lookup"><span data-stu-id="97ef4-111">**Wecutil cs** *<path>\\wsmanselrg.xml*</span></span>

3.  <span data-ttu-id="97ef4-112">Stellen Sie sicher, dass das Abonnement aktiv ist, indem Sie den folgenden Befehl in einem Eingabe Aufforderungs Fenster ausführen:</span><span class="sxs-lookup"><span data-stu-id="97ef4-112">Ensure that the subscription is active by executing the following command in a command prompt window:</span></span>

    <span data-ttu-id="97ef4-113">**Wecutil GR** *wsmanselrg*</span><span class="sxs-lookup"><span data-stu-id="97ef4-113">**Wecutil gr** *wsmanselrg*</span></span>

<span data-ttu-id="97ef4-114">Der BMC ist ein lokal an einen Server angefügter Mikrocontroller.</span><span class="sxs-lookup"><span data-stu-id="97ef4-114">The BMC is a microcontroller attached locally to a server.</span></span> <span data-ttu-id="97ef4-115">BMCs verfügen über Sensoren, die den physischen Zustand des Servers und eine separate Netzwerkverbindung überwachen, die über das Netzwerk kommunizieren kann, auch wenn der Server offline ist.</span><span class="sxs-lookup"><span data-stu-id="97ef4-115">BMCs have sensors that monitor the physical state of the server and a separate network connection that can communicate over the network, even if the server is offline.</span></span> <span data-ttu-id="97ef4-116">Sie haben Zugriff auf BMC-Daten über den WMI-Anbieter (Intelligent Platform Management Interface).</span><span class="sxs-lookup"><span data-stu-id="97ef4-116">You have access to BMC data through the Intelligent Platform Management Interface (IPMI) WMI Provider.</span></span> <span data-ttu-id="97ef4-117">Weitere Informationen zum IPMI-Anbieter finden Sie unter [IPMI-Anbieter](/previous-versions/windows/desktop/ipmiprv/ipmi-provider).</span><span class="sxs-lookup"><span data-stu-id="97ef4-117">For more information about the IPMI provider, see [IPMI Provider](/previous-versions/windows/desktop/ipmiprv/ipmi-provider).</span></span>

<span data-ttu-id="97ef4-118">Auf dem Computer muss der BMC und der IPMI-Anbieter installiert sein, damit das Ereignis Abonnement funktioniert.</span><span class="sxs-lookup"><span data-stu-id="97ef4-118">The computer must have the BMC and the IPMI provider installed for the event subscription to work.</span></span> <span data-ttu-id="97ef4-119">Für Computer, die unter Windows Server 2008 ausgeführt werden, wird der IPMI-Anbieter standardmäßig installiert.</span><span class="sxs-lookup"><span data-stu-id="97ef4-119">For computers running on Windows Server 2008, the IPMI provider is installed by default.</span></span> <span data-ttu-id="97ef4-120">Wenn der BMC nicht verfügbar ist, kann der IPMI-Treiber nicht installiert werden, und der Abonnement Lauf Zeit Status zeigt immer einen Fehler an (0x8004001-WMI Generic Failure).</span><span class="sxs-lookup"><span data-stu-id="97ef4-120">If the BMC is not available, then IPMI driver cannot be installed and the subscription runtime status will always display an error (0x8004001 - WMI Generic Failure).</span></span>

 

 