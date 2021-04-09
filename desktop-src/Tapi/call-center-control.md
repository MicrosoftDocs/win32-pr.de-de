---
description: Die grundlegende TAPI 2,2 kann verwendet werden, um Callcenter und andere Elemente der Telefonienetzwerkinfrastruktur (z. b. IVR-und Voicemail-Server) über die Anruf Steuerung von Drittanbietern zu verwalten.
ms.assetid: e920dc4a-adb4-4a36-ac04-f265538531eb
title: Callcenter-Steuerelement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4200ff434249856507109915f41f7f1479eddfd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866928"
---
# <a name="call-center-control"></a><span data-ttu-id="c73c8-103">Callcenter-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="c73c8-103">Call Center Control</span></span>

<span data-ttu-id="c73c8-104">Die grundlegende TAPI 2,2 kann verwendet werden, um Callcenter und andere Elemente der Telefonienetzwerkinfrastruktur (z. b. IVR-und Voicemail-Server) über die Anruf Steuerung von Drittanbietern zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="c73c8-104">Basic TAPI 2.2 can be used to manage call centers and other elements of Telephony network infrastructure (such as IVR and voice mail servers) through third-party call control.</span></span> <span data-ttu-id="c73c8-105">Zur Unterstützung der Erstellung von ACD-Proxys, die auf Servern ausgeführt werden, wurden TAPI 2,2 Funktionen hinzugefügt, um Anwendungsentwicklern zusätzliche Unterstützung zu bieten.</span><span class="sxs-lookup"><span data-stu-id="c73c8-105">To help create ACD proxies that will run on servers, functions have been added to TAPI 2.2 to provide additional assistance to application developers.</span></span>

<span data-ttu-id="c73c8-106">In den folgenden Themen werden die TAPI 2,2-Features beschrieben, die Sie zum Implementieren von callcentersteuerelementen verwenden können:</span><span class="sxs-lookup"><span data-stu-id="c73c8-106">The following topics describe the TAPI 2.2 features that you can use to implement call center controls:</span></span>

-   [<span data-ttu-id="c73c8-107">Modellieren eines Callcenter</span><span class="sxs-lookup"><span data-stu-id="c73c8-107">Modeling of a Call Center</span></span>](modeling-of-a-call-center.md)
-   [<span data-ttu-id="c73c8-108">Station</span><span class="sxs-lookup"><span data-stu-id="c73c8-108">Stations</span></span>](stations.md)
-   [<span data-ttu-id="c73c8-109">Vorhersagbare Wahl</span><span class="sxs-lookup"><span data-stu-id="c73c8-109">Predictive Dialing</span></span>](predictive-dialing.md)
-   [<span data-ttu-id="c73c8-110">Callwarteschlangen und Routenpunkte</span><span class="sxs-lookup"><span data-stu-id="c73c8-110">Call Queues and Route Points</span></span>](call-queues-and-route-points.md)
-   [<span data-ttu-id="c73c8-111">Überwachung und Steuerung des ACD-Agents</span><span class="sxs-lookup"><span data-stu-id="c73c8-111">ACD Agent Monitoring and Control</span></span>](acd-agent-monitoring-and-control.md)
-   [<span data-ttu-id="c73c8-112">Stations Status-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="c73c8-112">Station Status Control</span></span>](station-status-control.md)
-   [<span data-ttu-id="c73c8-113">Stations Status-Steuerelement</span><span class="sxs-lookup"><span data-stu-id="c73c8-113">Station Status Control</span></span>](station-status-control.md)
-   [<span data-ttu-id="c73c8-114">Timer für den CallState</span><span class="sxs-lookup"><span data-stu-id="c73c8-114">Call State Timer</span></span>](call-state-timer.md)
-   [<span data-ttu-id="c73c8-115">Medienereignis Timer</span><span class="sxs-lookup"><span data-stu-id="c73c8-115">Media Event Timers</span></span>](media-event-timers.md)

<span data-ttu-id="c73c8-116">TAPI 3. x ist die bevorzugte API zum Schreiben von ACD-Agent-Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="c73c8-116">TAPI 3.x is the preferred API of writing ACD Agent applications.</span></span> <span data-ttu-id="c73c8-117">Informationen zur Verwendung dieser Schnittstellen und Methoden finden Sie im Abschnitt " [callcentersteuerelemente](./about-call-center-controls.md) ".</span><span class="sxs-lookup"><span data-stu-id="c73c8-117">Please see the [Call Center Controls](./about-call-center-controls.md) section for information on using these interfaces and methods.</span></span> <span data-ttu-id="c73c8-118">TAPI 2,2 bleibt jedoch bei Bedarf für vollständige ACD-Anwendungs Suites verwendbar.</span><span class="sxs-lookup"><span data-stu-id="c73c8-118">However, TAPI 2.2 remains usable for full ACD application suites if desired.</span></span>

 

 
