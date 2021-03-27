---
description: Der Synchronisierungs-Manager bietet eine zentralisierte Standardtechnologie zum Synchronisieren von Dateien für die Offline Verwendung auf einem mobilen Computer oder einem Computer, der mit einem lokalen Netzwerk verbunden ist.
title: Synchronisierungs-Manager
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 6cdac7e5-8985-407a-98bb-936bb20ed069
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbOrient
ms.openlocfilehash: 2fc56b2afec4fdedf98fe213437a27f2592ce72b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104994783"
---
# <a name="synchronization-manager"></a><span data-ttu-id="1ac04-103">Synchronisierungs-Manager</span><span class="sxs-lookup"><span data-stu-id="1ac04-103">Synchronization Manager</span></span>

## <a name="purpose"></a><span data-ttu-id="1ac04-104">Zweck</span><span class="sxs-lookup"><span data-stu-id="1ac04-104">Purpose</span></span>

<span data-ttu-id="1ac04-105">Der Synchronisierungs-Manager bietet eine zentralisierte Standardtechnologie zum Synchronisieren von Dateien für die Offline Verwendung auf einem mobilen Computer oder einem Computer, der mit einem lokalen Netzwerk verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="1ac04-105">The Synchronization Manager provides a centralized, standard technology for synchronizing files for offline use on a mobile computer or a computer connected to a local area network.</span></span> <span data-ttu-id="1ac04-106">Zusammen mit den Konnektivitätsfunktionen, Benachrichtigungen (System Ereignis Benachrichtigungsdienst) und Client seitiger Zwischenspeicherung stellt der Synchronisierungs-Manager eine Infrastruktur zur Unterstützung von mobilen Computing bereit.</span><span class="sxs-lookup"><span data-stu-id="1ac04-106">Together with the connectivity functions, notifications (System Event Notification Service), and client side caching, the Synchronization Manager provides an infrastructure to support mobile computing.</span></span> <span data-ttu-id="1ac04-107">Anstatt jede Anwendung zu implementieren, die ihre eigene Technologie zum Zwischenspeichern und Synchronisieren von Netzwerkressourcen für die lokale Verwendung implementiert, stellt das Betriebssystem ein integriertes Modell bereit, das von allen Anwendungen verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="1ac04-107">Instead of each application implementing its own technology to cache and synchronize network resources for local use, the operating system provides an integrated model that all applications can use.</span></span> <span data-ttu-id="1ac04-108">Dateien werden unabhängig vom Protokoll synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="1ac04-108">Files are synchronized independent of the protocol.</span></span> <span data-ttu-id="1ac04-109">Ein e-Mail-Programm kann z. b. seine Nachrichten mithilfe von SMTP, NMTP oder POP3 übertragen, während ein Browser http verwenden kann und eine Datenbank Remote Prozedur Aufruf (RPC) verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="1ac04-109">For example, an email program can transfer its messages using SMTP, NMTP, or POP3, while a browser can use HTTP, and a database can use remote procedure call (RPC) (RPC).</span></span> <span data-ttu-id="1ac04-110">Entwickler können die gemeinsame Schnittstelle für den Synchronisierungs-Manager in Ihren Anwendungen verwenden, um Dateien zwischen dem lokalen Computer des Benutzers und dem Netzwerkspeicher zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="1ac04-110">Developers can use the common interface to the Synchronization Manager in their applications to synchronize files between the user's local computer and network storage.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="1ac04-111">Anwendungsbereich</span><span class="sxs-lookup"><span data-stu-id="1ac04-111">Where applicable</span></span>

<span data-ttu-id="1ac04-112">Der Synchronisierungs-Manager ist für Anwendungen vorgesehen, die in erster Linie auf mobilen Computern ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="1ac04-112">The Synchronization Manager is intended for applications that run primarily on mobile computers.</span></span> <span data-ttu-id="1ac04-113">Anwendungen, die auf Computern ausgeführt werden, die mit den lokalen Netzwerken mit hoher Latenz verbunden sind, können auch von der Verwendung der Synchronisierungs Verwaltung</span><span class="sxs-lookup"><span data-stu-id="1ac04-113">Applications that run on computers connected to high latency local area networks may also benefit from using the Synchronization Manager.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="1ac04-114">Entwicklergruppe</span><span class="sxs-lookup"><span data-stu-id="1ac04-114">Developer audience</span></span>

<span data-ttu-id="1ac04-115">Dieses Dokument richtet sich an Softwareentwickler, die Anwendungen für das Mobile Computing und die lokalen Netzwerke mit hoher Latenzzeit entwickeln.</span><span class="sxs-lookup"><span data-stu-id="1ac04-115">This document is intended for software developers who develop applications for mobile computing and high latency local area networks.</span></span> <span data-ttu-id="1ac04-116">Dieses Dokument enthält eine vollständige Referenz aller Teile des Synchronisierungs-Managers, einschließlich der Methoden und Schnittstellen für den Synchronisierungs-Manager.</span><span class="sxs-lookup"><span data-stu-id="1ac04-116">This document provides a complete reference of all parts of the Synchronization Manager including the methods and interfaces to the Synchronization Manager.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="1ac04-117">Laufzeitanforderungen</span><span class="sxs-lookup"><span data-stu-id="1ac04-117">Run-time requirements</span></span>

<span data-ttu-id="1ac04-118">Erfordert Windows Server 2003, Windows XP, Windows 2000 oder Windows Millennium Edition (Windows Me).</span><span class="sxs-lookup"><span data-stu-id="1ac04-118">Requires Windows Server 2003, Windows XP, Windows 2000, or Windows Millennium Edition (Windows Me).</span></span> <span data-ttu-id="1ac04-119">Auch als verteilbare Komponente für Microsoft Windows NT 4,0, Windows 98 und Windows 95 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="1ac04-119">Also available as a redistributable for Microsoft Windows NT 4.0, Windows 98, and Windows 95.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="1ac04-120">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="1ac04-120">In this section</span></span>



| <span data-ttu-id="1ac04-121">Thema</span><span class="sxs-lookup"><span data-stu-id="1ac04-121">Topic</span></span>                                                                                       | <span data-ttu-id="1ac04-122">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1ac04-122">Description</span></span>                                                                                                                                         |
|---------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1ac04-123">Informationen zur Synchronisierungs Verwaltung</span><span class="sxs-lookup"><span data-stu-id="1ac04-123">About Synchronization Manager</span></span>](syncmgr-about.md)<br/>                               | <span data-ttu-id="1ac04-124">Der Synchronisierungs-Manager stellt eine zentralisierte Standardtechnologie zum Synchronisieren von Dateien für die Offline Verwendung auf einem lokalen Computer bereit.</span><span class="sxs-lookup"><span data-stu-id="1ac04-124">The Synchronization Manager provides a centralized, standard technology for synchronizing files for offline use on a local computer.</span></span><br/>     |
| [<span data-ttu-id="1ac04-125">Mobile Computing-Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="1ac04-125">Mobile Computing Configurations</span></span>](syncmgr-mobile-computing-configs.md)<br/>          | <span data-ttu-id="1ac04-126">Anwendungen können den Sychronization Manager verwenden, um Dateien und Ressourcen lokal zwischengespeichert und auf mobilen Computern und Desktop Computern zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="1ac04-126">Applications can use Sychronization Manager to keep files and resources cached locally and synchronized on mobile and desktop computers.</span></span><br/> |
| [<span data-ttu-id="1ac04-127">Anwendungs Szenarios</span><span class="sxs-lookup"><span data-stu-id="1ac04-127">Application Scenarios</span></span>](syncmgr-app-scenarios.md)<br/>                               | <span data-ttu-id="1ac04-128">Anwendungen und Dienste, die den Synchronisierungs-Manager verwenden können.</span><span class="sxs-lookup"><span data-stu-id="1ac04-128">Applications and services that can use Synchronization Manager.</span></span><br/>                                                                          |
| [<span data-ttu-id="1ac04-129">Architektur der Synchronisierungs Verwaltung</span><span class="sxs-lookup"><span data-stu-id="1ac04-129">Synchronization Manager Architecture</span></span>](syncmgr-architecture.md)<br/>                 |                                                                                                                                                     |
| [<span data-ttu-id="1ac04-130">Verwenden des Synchronisierungs-Managers aus einem Programm</span><span class="sxs-lookup"><span data-stu-id="1ac04-130">Using Synchronization Manager from a Program</span></span>](syncmgr-using-from-a-program.md)<br/> |                                                                                                                                                     |
| [<span data-ttu-id="1ac04-131">Synchronisierungs-Manager</span><span class="sxs-lookup"><span data-stu-id="1ac04-131">Synchronization Manager Reference</span></span>](syncmgr-reference.md)<br/>                       | <span data-ttu-id="1ac04-132">Die folgenden Programmier Elemente bilden die API für den Synchronisierungs-Manager.</span><span class="sxs-lookup"><span data-stu-id="1ac04-132">The following programming elements make up the API for Synchronization Manager.</span></span><br/>                                                          |



 

## <a name="related-topics"></a><span data-ttu-id="1ac04-133">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1ac04-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1ac04-134">Informationen zum System Ereignis Benachrichtigungsdienst</span><span class="sxs-lookup"><span data-stu-id="1ac04-134">About System Event Notification Service</span></span>](../sens/about-system-event-notification-service.md)
</dt> </dl>

 

 
