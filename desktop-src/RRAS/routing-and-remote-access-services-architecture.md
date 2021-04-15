---
title: Architektur der Routing-und RAS-Dienste
description: Die folgende Abbildung zeigt eine allgemeine Architektur Ansicht des Windows 2000-Routers.
ms.assetid: 599435e2-e2f3-4632-8a79-441172aacf13
keywords:
- RRAS-, Routing-und RAS-Dienst Architektur-RRAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a3e72f7c61bc9cb558b020c3470718a7f419c04
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471516"
---
# <a name="routing-and-remote-access-services-architecture"></a><span data-ttu-id="575b7-104">Architektur der Routing-und RAS-Dienste</span><span class="sxs-lookup"><span data-stu-id="575b7-104">Routing and Remote Access Services Architecture</span></span>

<span data-ttu-id="575b7-105">Die folgende Abbildung zeigt eine allgemeine Architektur Ansicht des Windows 2000-Routers.</span><span class="sxs-lookup"><span data-stu-id="575b7-105">The following illustration presents a general architectural view of the Windows 2000 router.</span></span>

<span data-ttu-id="575b7-106">Komponenten, die für die IP-Protokollfamilie spezifisch sind, werden hellgrau dargestellt.</span><span class="sxs-lookup"><span data-stu-id="575b7-106">Components that are specific to the IP protocol family are shown in light gray.</span></span> <span data-ttu-id="575b7-107">Komponenten, die für die IPX-Protokollfamilie spezifisch sind, werden in dunkelgrau dargestellt.</span><span class="sxs-lookup"><span data-stu-id="575b7-107">Components that are specific to the IPX protocol family are shown in dark gray.</span></span> <span data-ttu-id="575b7-108">Komponenten, die allgemein für alle Protokoll Familien gelten, sind schattiert.</span><span class="sxs-lookup"><span data-stu-id="575b7-108">Components that are general to all protocol families are unshaded.</span></span>

<span data-ttu-id="575b7-109">Der Routing-und RAS-Dienst stellt APIs zum Verwalten und Konfigurieren des-Dienstanbieter bereit.</span><span class="sxs-lookup"><span data-stu-id="575b7-109">The Routing and Remote Access Service provides APIs for administering and configuring the service.</span></span> <span data-ttu-id="575b7-110">Diese APIs enthalten SNMP-Agents sowohl für IP als auch für IPX.</span><span class="sxs-lookup"><span data-stu-id="575b7-110">These APIs include SNMP agents for both IP and IPX.</span></span>

<span data-ttu-id="575b7-111">RRAS umfasst Routing Protokolle sowohl für IP als auch für IPX.</span><span class="sxs-lookup"><span data-stu-id="575b7-111">RRAS includes routing protocols for both IP and IPX.</span></span> <span data-ttu-id="575b7-112">Bei IP stellt RRAS das Routing Information-Protokoll (RIP) und Open kürzeste Path First (OSPF)-Routing Protokolle bereit.</span><span class="sxs-lookup"><span data-stu-id="575b7-112">For IP, RRAS provides the Routing Information Protocol (RIP) and Open Shortest Path First (OSPF) routing protocols.</span></span> <span data-ttu-id="575b7-113">Für IPX stellt RRAS das IPX-RIP-und Service Advertising-Protokoll (SAP) bereit.</span><span class="sxs-lookup"><span data-stu-id="575b7-113">For IPX, RRAS provides IPX RIP and Service Advertising Protocol (SAP).</span></span>

<span data-ttu-id="575b7-114">RRAS verwendet einen Routing Tabellen-Manager (RTM) sowohl für IP als auch für IPX.</span><span class="sxs-lookup"><span data-stu-id="575b7-114">RRAS uses one Routing Table Manager (RTM) for both IP and IPX.</span></span> <span data-ttu-id="575b7-115">Jede Protokollfamilie verfügt jedoch über einen eigenen routermanager.</span><span class="sxs-lookup"><span data-stu-id="575b7-115">However, each protocol family has its own Router Manager.</span></span> <span data-ttu-id="575b7-116">RRAS verfügt auch über eine separate Komponente zum Verwalten von Multicast Gruppen.</span><span class="sxs-lookup"><span data-stu-id="575b7-116">RRAS also has separate component for managing Multicast Groups.</span></span>

<span data-ttu-id="575b7-117">Die Schnittstellen von Dynamic Interface Manager (Dim) mit PPP-und TAPI-Diensten zur Verwaltung von PPP-Schnittstellen, die von einigen Routen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="575b7-117">The Dynamic Interface Manager (DIM) interfaces with PPP and TAPI services in order to manage PPP interfaces used by some routes.</span></span>

![allgemeine Architektur Ansicht des Windows 2000-Routers](images/rtarch.png)

 

 




