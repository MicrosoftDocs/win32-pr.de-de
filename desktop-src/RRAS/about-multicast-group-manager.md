---
title: Informationen zum Multicast-Gruppen-Manager
description: In dieser Dokumentation wird die Technologie von Multicast Group Manager (MGM) beschrieben.
ms.assetid: 55216742-d67c-4a17-aaf9-0b087938061e
keywords:
- RRAS für Multicast-Gruppen-Manager
- RRAS für Multicast-Gruppen-Manager, beschrieben
- RRAS für den Routing-und RAS-Dienst, Multicast-Gruppen-Manager
- Routing-und RAS-Dienst RRAS, Multicast-Gruppen-Manager, beschrieben
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 034d37b99aaa9ca0139b5425cd5b85e7b3f280e9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106342058"
---
# <a name="about-multicast-group-manager"></a><span data-ttu-id="58234-107">Informationen zum Multicast-Gruppen-Manager</span><span class="sxs-lookup"><span data-stu-id="58234-107">About Multicast Group Manager</span></span>

<span data-ttu-id="58234-108">In dieser Dokumentation wird die Technologie von Multicast Group Manager (MGM) beschrieben.</span><span class="sxs-lookup"><span data-stu-id="58234-108">This documentation describes the Multicast Group Manager (MGM) technology.</span></span>

<span data-ttu-id="58234-109">Multicasting ermöglicht einem Host das Senden von Daten an nur die Ziele, die speziell den Empfang der Daten anfordern.</span><span class="sxs-lookup"><span data-stu-id="58234-109">Multicasting allows a host to send data to only those destinations that specifically request to receive the data.</span></span> <span data-ttu-id="58234-110">Auf diese Weise unterscheidet sich Multicasting vom Senden von Broadcast Daten, da Broadcast Daten an alle Hosts gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="58234-110">In this way, multicasting differs from sending broadcast data, since broadcast data is sent to all hosts.</span></span>

<span data-ttu-id="58234-111">Multicasting spart Netzwerkbandbreite, da Multicast Daten nur von den Hosts empfangen werden, von denen die Daten angefordert werden, und die Daten werden nur einmal über einen Link übertragen.</span><span class="sxs-lookup"><span data-stu-id="58234-111">Multicasting saves network bandwidth because multicast data is only received by those hosts that request the data, and the data travels over any link only once.</span></span> <span data-ttu-id="58234-112">Multicasting spart Server Bandbreite, da ein Server anstelle einer Unicastnachricht pro Empfänger nur eine Multicast Nachricht pro Netzwerk senden muss.</span><span class="sxs-lookup"><span data-stu-id="58234-112">Multicasting saves server bandwidth because a server has to send only one multicast message per network instead of one unicast message per receiver.</span></span> <span data-ttu-id="58234-113">Beispiele für beliebte Multicast Anwendungen sind Online Besprechungen und Internet Radio.</span><span class="sxs-lookup"><span data-stu-id="58234-113">Examples of popular multicast applications are online meetings and Internet radio.</span></span>

<span data-ttu-id="58234-114">Die MGM-API ermöglicht Entwicklern das Schreiben von Multicast Routing Protokollen, die mit Routern interagieren, auf denen der Multicast-Gruppen-Manager ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="58234-114">The MGM API enables developers to write multicast routing protocols that interoperate with routers running the multicast group manager.</span></span>

<span data-ttu-id="58234-115">Wenn mehr als ein Multicast Routing Protokoll auf einem Router aktiviert ist, koordiniert der Multicast-Gruppen-Manager die Vorgänge zwischen allen Routing Protokollen.</span><span class="sxs-lookup"><span data-stu-id="58234-115">When more than one multicast routing protocol is enabled on a router, the multicast group manager coordinates operations between all routing protocols.</span></span> <span data-ttu-id="58234-116">Der Multicast-Gruppen-Manager informiert jedes Routing Protokoll, wenn Gruppen Mitgliedschafts Änderungen auftreten, und wenn Multicast Daten aus einer neuen Quelle oder einer neuen Gruppe empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="58234-116">The multicast group manager informs each routing protocol when group membership changes occur, and when multicast data from a new source or destined to a new group is received.</span></span>

<span data-ttu-id="58234-117">Die MGM-API bietet die folgenden Features:</span><span class="sxs-lookup"><span data-stu-id="58234-117">The MGM API provides the following features:</span></span>

-   <span data-ttu-id="58234-118">Protokoll Registrierung</span><span class="sxs-lookup"><span data-stu-id="58234-118">Protocol registration</span></span>
-   <span data-ttu-id="58234-119">Gruppenverwaltung</span><span class="sxs-lookup"><span data-stu-id="58234-119">Group management</span></span>
-   <span data-ttu-id="58234-120">MFE-Enumeration (Multicast Weiterleitungs Eintrag)</span><span class="sxs-lookup"><span data-stu-id="58234-120">Multicast forwarding entry (MFE) enumeration</span></span>
-   <span data-ttu-id="58234-121">Rückruf Definitionen für Multicast Routing Protokolle</span><span class="sxs-lookup"><span data-stu-id="58234-121">Callback definitions for multicast routing protocols</span></span>

<span data-ttu-id="58234-122">In dieser Übersicht werden die Komponenten der Multicast Architektur, die Client Szenarien, die für die Zusammenarbeit mit dem Multicast-Gruppen-Manager verwendet werden, sowie Programmier Überlegungen für die Verwendung der MGM-API beschrieben.</span><span class="sxs-lookup"><span data-stu-id="58234-122">This overview describes the components of the multicast architecture, the client scenarios that are used to interoperate with the multicast group manager, and programming considerations for using the MGM API.</span></span>

 

 




