---
description: Das folgende Material enthält Richtlinien für die Verwendung von TAPI zum Schreiben von Anwendungen für die Endbenutzer-oder Serverkommunikation. Diese Informationen sind auch für Dienstanbieter Programmierer äußerst relevant.
ms.assetid: fb97aff7-910e-451f-b183-36324a459423
title: TAPI-Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6836f33af120171016b080693ae7a8315f9b9d7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369804"
---
# <a name="tapi-applications"></a><span data-ttu-id="891d6-104">TAPI-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="891d6-104">TAPI Applications</span></span>

<span data-ttu-id="891d6-105">Das folgende Material enthält Richtlinien für die Verwendung von TAPI zum Schreiben von Anwendungen für die Endbenutzer-oder Serverkommunikation.</span><span class="sxs-lookup"><span data-stu-id="891d6-105">The following material provides guidelines on using TAPI to write end-user or server communications applications.</span></span> <span data-ttu-id="891d6-106">Diese Informationen sind auch für Dienstanbieter Programmierer äußerst relevant.</span><span class="sxs-lookup"><span data-stu-id="891d6-106">This information is also highly relevant to service provider programmers.</span></span>

<span data-ttu-id="891d6-107">Die erste Entscheidung, die ein Programmierer bei der Verwendung von TAPI treffen muss, ist die erforderliche Dienst Ebene.</span><span class="sxs-lookup"><span data-stu-id="891d6-107">The first decision a programmer needs to make in using TAPI is the level of service required.</span></span> <span data-ttu-id="891d6-108">Wenn eine Anwendung z. b. eine Menü Auswahl erfordert, die eine Telefonnummer wählen kann, ist wahrscheinlich keine vollständige TAPI-Anwendung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="891d6-108">For example, if an application requires a menu selection that can dial a phone number, a full TAPI application is probably not required.</span></span> <span data-ttu-id="891d6-109">Unterstützte Telefonieoptionen können diese Option schnell und einfach aktivieren.</span><span class="sxs-lookup"><span data-stu-id="891d6-109">Assisted Telephony can enable this option quickly and simply.</span></span> <span data-ttu-id="891d6-110">Weitere Informationen zum Unterschied zwischen vollständigen TAPI-Anwendungen und der unterstützten Telefonie finden Sie unter [TAPI-Dienst Ebenen](tapi-levels-of-service.md) .</span><span class="sxs-lookup"><span data-stu-id="891d6-110">Please see [TAPI Levels of Service](tapi-levels-of-service.md) for more information on the distinction between full TAPI applications and Assisted Telephony.</span></span>

<span data-ttu-id="891d6-111">Die zweite wichtige Entscheidung ist, ob TAPI 2. x, die C-basierte API oder TAPI 3. x, die auf com basiert, verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="891d6-111">The second important decision is whether to use TAPI 2.x, the C-based API, or TAPI 3.x, which is based on COM.</span></span> <span data-ttu-id="891d6-112">Eine Erörterung wichtiger Aspekte bei der Entscheidung, welche verwendet werden soll, finden Sie unter [TAPI 3. x vs. TAPI 2. x](tapi-3-x-versus-tapi-2-x.md) .</span><span class="sxs-lookup"><span data-stu-id="891d6-112">Please see [TAPI 3.x vs. TAPI 2.x](tapi-3-x-versus-tapi-2-x.md) for a discussion of important considerations in deciding which one to use.</span></span>

<span data-ttu-id="891d6-113">Im folgenden Diagramm werden die grundlegenden Bausteine einer vollständigen TAPI-Anwendung veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="891d6-113">The following diagram illustrates the basic building blocks of a full TAPI application.</span></span> <span data-ttu-id="891d6-114">TAPI 2. x und TAPI 3. x werden in diesen Abschnitten behandelt.</span><span class="sxs-lookup"><span data-stu-id="891d6-114">TAPI 2.x and TAPI 3.x are both addressed in these sections.</span></span> <span data-ttu-id="891d6-115">Material, das sehr spezifisch ist, wird in den Übersichts Abschnitten für TAPI 2. x oder TAPI 3. x behandelt.</span><span class="sxs-lookup"><span data-stu-id="891d6-115">Material that is highly specific to one is addressed in the overview sections for TAPI 2.x or TAPI 3.x.</span></span>

![Bausteine einer TAPI-Anwendung](images/tapior3.png)

<span data-ttu-id="891d6-117">Die folgenden Links stellen Inhalt bereit, der den Abbildungen in der obigen Abbildung entspricht:</span><span class="sxs-lookup"><span data-stu-id="891d6-117">The following links provide content that corresponds to the figures in the above image:</span></span>

| <span data-ttu-id="891d6-118">Re</span><span class="sxs-lookup"><span data-stu-id="891d6-118">Figure</span></span> | <span data-ttu-id="891d6-119">Dokumentation</span><span class="sxs-lookup"><span data-stu-id="891d6-119">Documentation</span></span>                                                                    |
|--------|----------------------------------------------------------------------------------|
| <span data-ttu-id="891d6-120">1</span><span class="sxs-lookup"><span data-stu-id="891d6-120">1</span></span>      | [<span data-ttu-id="891d6-121">TAPI-Initialisierung</span><span class="sxs-lookup"><span data-stu-id="891d6-121">TAPI Initialization</span></span>](tapi-initialization.md)                                   |
| <span data-ttu-id="891d6-122">2</span><span class="sxs-lookup"><span data-stu-id="891d6-122">2</span></span>      | [<span data-ttu-id="891d6-123">Sitzungssteuerung</span><span class="sxs-lookup"><span data-stu-id="891d6-123">Session Control</span></span>](session-control.md)                                           |
| <span data-ttu-id="891d6-124">3</span><span class="sxs-lookup"><span data-stu-id="891d6-124">3</span></span>      | [<span data-ttu-id="891d6-125">Gerätesteuerung</span><span class="sxs-lookup"><span data-stu-id="891d6-125">Device Control</span></span>](device-control.md)                                             |
| <span data-ttu-id="891d6-126">4</span><span class="sxs-lookup"><span data-stu-id="891d6-126">4</span></span>      | [<span data-ttu-id="891d6-127">Mediensteuer Element</span><span class="sxs-lookup"><span data-stu-id="891d6-127">Media Control</span></span>](media-control.md)                                               |
| <span data-ttu-id="891d6-128">5</span><span class="sxs-lookup"><span data-stu-id="891d6-128">5</span></span>      | [<span data-ttu-id="891d6-129">Informationen zu Callcenter-Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="891d6-129">About Call Center Controls</span></span>](about-call-center-controls.md)                     |
| <span data-ttu-id="891d6-130">6</span><span class="sxs-lookup"><span data-stu-id="891d6-130">6</span></span>      | [<span data-ttu-id="891d6-131">Rendezvous-IP-telefoniekonferenzen</span><span class="sxs-lookup"><span data-stu-id="891d6-131">Rendezvous IP Telephony Conferencing</span></span>](rendezvous-ip-telephony-conferencing.md) |
| <span data-ttu-id="891d6-132">7</span><span class="sxs-lookup"><span data-stu-id="891d6-132">7</span></span>      | [<span data-ttu-id="891d6-133">TAPI Herunterfahren</span><span class="sxs-lookup"><span data-stu-id="891d6-133">TAPI Shutdown</span></span>](tapi-shutdown.md)                                               |



 

 

 



