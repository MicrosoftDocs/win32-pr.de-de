---
title: Informationen zur Netzwerk Listen-Manager-API
description: Informationen zur Netzwerk Listen-Manager-API
ms.assetid: 675cf7ed-9f57-4d62-8091-1f4e8812f2ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6230251e627671b7fd33adbf50b3904703bc9847
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713589"
---
# <a name="about-the-network-list-manager-api"></a><span data-ttu-id="2337d-103">Informationen zur Netzwerk Listen-Manager-API</span><span class="sxs-lookup"><span data-stu-id="2337d-103">About the Network List Manager API</span></span>

<span data-ttu-id="2337d-104">Mit der Microsoft Windows-Netzwerkumgebung können mehrfach vernetzte Computer gleichzeitig eine Verbindung mit mehreren Netzwerken herstellen.</span><span class="sxs-lookup"><span data-stu-id="2337d-104">The Microsoft Windows networking environment allows multihomed computers to connect to several networks simultaneously.</span></span> <span data-ttu-id="2337d-105">Möglicherweise sind mehrere Drahtlos Netzwerke zusammen mit LAN-und DFÜ-Verbindungen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2337d-105">There may be multiple wireless networks available along with LAN and dial-up connections.</span></span> <span data-ttu-id="2337d-106">Der Netzwerk Listen-Manager identifiziert verfügbare Netzwerke und gibt Netzwerk Attributdaten an die Anwendung zurück.</span><span class="sxs-lookup"><span data-stu-id="2337d-106">Network List Manager identifies available networks and returns network attribute data to the application.</span></span>

<span data-ttu-id="2337d-107">Die Netzwerk Listen-Manager-API interagiert mit dem Netzwerk Listen-Manager-Dienst, um die Eigenschaften jedes Netzwerks zu identifizieren und abzurufen, mit dem der PC eine Verbindung herstellt.</span><span class="sxs-lookup"><span data-stu-id="2337d-107">The Network List Manager API interacts with the Network List Manager service to identify and retrieve properties of each network that the PC connects to.</span></span> <span data-ttu-id="2337d-108">Jedes Netzwerk wird durch eine Netzwerk Signatur basierend auf den eindeutig identifizierbaren Eigenschaften dieses Netzwerks eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="2337d-108">Each network is uniquely identified with a network signature based on the uniquely identifiable properties of that network.</span></span> <span data-ttu-id="2337d-109">Wenn eine Anwendung für Benachrichtigungen des Netzwerk Listen-Managers registriert wird, erhält die Anwendung Benachrichtigungen über die Verfügbarkeit neuer Netzwerkverbindungen oder Änderungen an vorhandenen Netzwerkverbindungen.</span><span class="sxs-lookup"><span data-stu-id="2337d-109">When an application registers for Network List Manager notifications, the application receives notifications about the availability of new network connections or changes to existing network connections.</span></span> <span data-ttu-id="2337d-110">Anwendungen können Ihre Logik abhängig von dem Netzwerk anpassen, mit dem Sie verbunden sind. die Netzwerkverbindung, mit der Sie verbunden sind; oder die Netzwerk Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2337d-110">Applications can adjust their logic depending on: which network they are connected to; which network connection they are connected to; or what the network properties are.</span></span> <span data-ttu-id="2337d-111">Mit diesen Informationen können Anwendungen ihre Aktionen basierend auf den aktuellen Netzwerkbedingungen optimieren.</span><span class="sxs-lookup"><span data-stu-id="2337d-111">With this information applications can fine tune their actions based on current network conditions</span></span>

<span data-ttu-id="2337d-112">In Windows Vista werden neue Schnittstellen eingeführt, die verwendet werden können, um ausführliche Informationen zu diesen Netzwerk Merkmalen und mehr zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="2337d-112">Windows Vista introduces new interfaces that can be used to obtain detailed information about these network characteristics and more.</span></span> <span data-ttu-id="2337d-113">Mit der [**inetworklistmanager**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworklistmanager) -Schnittstelle ist es ganz einfach, alle Netzwerke ([**iNetwork**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork)), die ein Computer jemals gesehen hat, oder nur die verbundenen Netzwerke aufzuzählen.</span><span class="sxs-lookup"><span data-stu-id="2337d-113">With the [**INetworkListManager**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworklistmanager) interface it is easy to enumerate all networks ([**INetwork**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork)) a computer has ever seen, or just the connected networks, or just the disconnected networks.</span></span> <span data-ttu-id="2337d-114">Die **inetworklistmanager** -Schnittstelle vereinfacht auch das Auflisten der Netzwerkschnittstellen auf einem Computer.</span><span class="sxs-lookup"><span data-stu-id="2337d-114">The **INetworkListManager** interface also makes it easy to enumerate the network interfaces on a computer.</span></span>

<span data-ttu-id="2337d-115">Die [**iNetwork**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork) -Schnittstelle wird verwendet, um die Eigenschaften einer Netzwerkverbindung zu bestimmen: Name, Beschreibung, ID, verwaltet/authentifiziert, verbunden/getrennt und mehr.</span><span class="sxs-lookup"><span data-stu-id="2337d-115">The [**INetwork**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork) interface is used to determine the properties of a network connection: name, description, ID, managed/authenticated, connected/disconnected, and more.</span></span> <span data-ttu-id="2337d-116">Es ist möglich, dass ein einzelnes Netzwerk mit mehreren Schnittstellen verbunden ist, sodass Sie über eine **iNetwork** -Schnittstelle auch die Instanzen der verwendeten **iNetwork** -Schnittstelle auflisten können.</span><span class="sxs-lookup"><span data-stu-id="2337d-116">It is possible that a single network is connected to several interfaces, so through an **INetwork** interface you can also enumerate the instances of the **INetwork** interface being used.</span></span>

<span data-ttu-id="2337d-117">Die [**iNetwork**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork) -Schnittstelle zeigt Ihnen die relevanten Eigenschaften einer Schnittstelle an: ID, Guid, Typ (verwaltet, authentifiziert) und Status (verbunden, getrennt, v4 lokal, v4-Internet, V6 local, V6 Internet).</span><span class="sxs-lookup"><span data-stu-id="2337d-117">The [**INetwork**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetwork) interface tells you the relevant properties of an interface: ID, GUID, Type (managed, authenticated), and State (connected, disconnected, V4 Local, V4 Internet, V6 Local, V6 Internet).</span></span> <span data-ttu-id="2337d-118">V4 local bedeutet lokalen IPv4-Zugriff (Internet Protocol Version 4).</span><span class="sxs-lookup"><span data-stu-id="2337d-118">V4 Local means Internet Protocol version 4 (IPv4) local access.</span></span> <span data-ttu-id="2337d-119">V4 Internet bedeutet IPv4 mit Internet Zugang.</span><span class="sxs-lookup"><span data-stu-id="2337d-119">V4 Internet means IPv4 with internet access.</span></span> <span data-ttu-id="2337d-120">V6 local und V6 Internet bedeuten IPv6.</span><span class="sxs-lookup"><span data-stu-id="2337d-120">V6 Local and V6 Internet mean IPv6.</span></span>

<span data-ttu-id="2337d-121">Der Stamm der Objektstruktur für Network Location ist die [**inetworklistmanager**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworklistmanager) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="2337d-121">The root of the object tree for Network Location is the [**INetworkListManager**](/windows/desktop/api/Netlistmgr/nn-netlistmgr-inetworklistmanager) interface.</span></span> <span data-ttu-id="2337d-122">Diese Schnittstelle wird in der **CLSID \_ networklistmanager** -Co-Klasse implementiert.</span><span class="sxs-lookup"><span data-stu-id="2337d-122">This interface is implemented on the **CLSID\_NetworkListManager** coclass.</span></span> <span data-ttu-id="2337d-123">Um diese Schnittstelle verwenden zu können, muss das COM-Objekt " **CLSID \_ networklistmanager** " wie folgt erstellt werden:</span><span class="sxs-lookup"><span data-stu-id="2337d-123">In order to use this interface, it is necessary to create the **CLSID\_NetworkListManager** COM object as demonstrated:</span></span>


```C++
#include <windows.h>
#include <netlistmgr.h>

#pragma comment(lib, "ole32.lib")

void main()
{
    INetworkListManager *pNetworkListManager = NULL; 
    HRESULT hr = CoCreateInstance(CLSID_NetworkListManager, NULL,
            CLSCTX_ALL, IID_INetworkListManager,
            (LPVOID *)&pNetworkListManager);
}
```



 

 




