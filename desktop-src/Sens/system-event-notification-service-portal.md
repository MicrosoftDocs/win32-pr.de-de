---
description: Überwachen von System Ereignis Benachrichtigungen von Programmen, die auf mobilen Computern ausgeführt werden, um die Bandbreite und Latenz der Netzwerkverbindung zu ermitteln Schreiben Sie optimierte Anwendungen für Mobile Computing und LANs mit hoher Latenz.
ms.assetid: a27386c5-1ab3-448a-88d9-8c9a18599e59
title: Benachrichtigungsdienst für Systemereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c3238441f82c26a33370c37fe09b3e4007639f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960447"
---
# <a name="system-event-notification-service"></a><span data-ttu-id="5ff5b-104">Benachrichtigungsdienst für Systemereignisse</span><span class="sxs-lookup"><span data-stu-id="5ff5b-104">System Event Notification Service</span></span>

## <a name="purpose"></a><span data-ttu-id="5ff5b-105">Zweck</span><span class="sxs-lookup"><span data-stu-id="5ff5b-105">Purpose</span></span>

<span data-ttu-id="5ff5b-106">Anwendungen, die zur Verwendung durch mobile Benutzer entwickelt wurden, benötigen einen eindeutigen Satz von Konnektivitätsfunktionen und-Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="5ff5b-106">Applications designed for use by mobile users require a unique set of connectivity functions and notifications.</span></span> <span data-ttu-id="5ff5b-107">In der Vergangenheit waren diese individuellen Anwendungen erforderlich, um diese Features intern zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="5ff5b-107">In the past these individual applications were required to implement these features internally.</span></span> <span data-ttu-id="5ff5b-108">Der System Event Notification Service (Sens) stellt diese Funktionen jetzt im Betriebs System bereit und erstellt eine einheitliche Konnektivität und Benachrichtigungs Schnittstelle für Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="5ff5b-108">The System Event Notification Service (SENS) now provides these capabilities in the operating system, creating a uniform connectivity and notification interface for applications.</span></span> <span data-ttu-id="5ff5b-109">Die Verwendung von Sens-Entwicklern kann die Verbindungs Bandbreite und Latenz Informationen aus Ihrer Anwendung heraus ermitteln und den Betrieb der Anwendung basierend auf diesen Bedingungen optimieren.</span><span class="sxs-lookup"><span data-stu-id="5ff5b-109">Using SENS developers can determine connection bandwidth and latency information from within their application and optimize the application's operation based on those conditions.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="5ff5b-110">Anwendungsbereich</span><span class="sxs-lookup"><span data-stu-id="5ff5b-110">Where applicable</span></span>

<span data-ttu-id="5ff5b-111">Die Konnektivitätsfunktionen und Benachrichtigungen von Sens sind für Anwendungen nützlich, die für mobile Computer oder Computer geschrieben wurden, die mit lokalen Netzwerken mit hoher Latenz verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="5ff5b-111">The connectivity functions and notifications of SENS are useful for applications written for mobile computers or computers connected to high latency local area networks.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="5ff5b-112">Entwicklergruppe</span><span class="sxs-lookup"><span data-stu-id="5ff5b-112">Developer audience</span></span>

<span data-ttu-id="5ff5b-113">Dieses Dokument richtet sich an Softwareentwickler, die Anwendungen für das Mobile Computing und die lokalen Netzwerke mit hoher Latenzzeit entwickeln.</span><span class="sxs-lookup"><span data-stu-id="5ff5b-113">This document is intended for software developers who develop applications for mobile computing and high latency local area networks.</span></span> <span data-ttu-id="5ff5b-114">Dieses Dokument enthält eine vollständige Referenz aller Teile des System Ereignis Benachrichtigungs Diensts, einschließlich des Sens-Objekts und der unterstützenden Methoden.</span><span class="sxs-lookup"><span data-stu-id="5ff5b-114">This document provides a complete reference of all parts of the System Event Notification Service including the SENS object and supporting methods.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="5ff5b-115">Laufzeitanforderungen</span><span class="sxs-lookup"><span data-stu-id="5ff5b-115">Run-time requirements</span></span>

<span data-ttu-id="5ff5b-116">Erfordert Microsoft Windows XP oder höher.</span><span class="sxs-lookup"><span data-stu-id="5ff5b-116">Requires Microsoft Windows XP or later.</span></span> <span data-ttu-id="5ff5b-117">Informationen dazu, welche Betriebssysteme für die Verwendung einer bestimmten Schnittstelle oder Funktion erforderlich sind, finden Sie im Abschnitt "Anforderungen" in der Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="5ff5b-117">For information about which operating systems are required to use a particular interface or function, see the Requirements section of the documentation.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="5ff5b-118">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="5ff5b-118">In this section</span></span>



| <span data-ttu-id="5ff5b-119">Thema</span><span class="sxs-lookup"><span data-stu-id="5ff5b-119">Topic</span></span>                                                              | <span data-ttu-id="5ff5b-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5ff5b-120">Description</span></span>                                                                           |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [<span data-ttu-id="5ff5b-121">Übersicht</span><span class="sxs-lookup"><span data-stu-id="5ff5b-121">Overview</span></span>](about-system-event-notification-service.md)<br/> | <span data-ttu-id="5ff5b-122">Allgemeine Informationen zum System Ereignis Benachrichtigungsdienst.</span><span class="sxs-lookup"><span data-stu-id="5ff5b-122">General information about System Event Notification Service.</span></span><br/>               |
| [<span data-ttu-id="5ff5b-123">Verweis</span><span class="sxs-lookup"><span data-stu-id="5ff5b-123">Reference</span></span>](sens-reference.md)<br/>                         | <span data-ttu-id="5ff5b-124">Dokumentation der Methoden und Schnittstellen des System Ereignis Benachrichtigungs Diensts.</span><span class="sxs-lookup"><span data-stu-id="5ff5b-124">Documentation of System Event Notification Service methods and interfaces.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="5ff5b-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5ff5b-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5ff5b-126">**Ieventabonnement**</span><span class="sxs-lookup"><span data-stu-id="5ff5b-126">**IEventSubscription**</span></span>](/windows/win32/api/eventsys/nn-eventsys-ieventsubscription)
</dt> </dl>

 

 
