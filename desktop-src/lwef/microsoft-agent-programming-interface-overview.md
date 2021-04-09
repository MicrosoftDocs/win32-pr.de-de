---
title: Übersicht über die Microsoft Agent-Programmierschnittstelle
description: Übersicht über die Microsoft Agent-Programmierschnittstelle
ms.assetid: 8709441b-9739-4f11-a2de-40a5f5eefb72
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad89249e064eb89d37f497fb79cb8982c79cb83c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856215"
---
# <a name="microsoft-agent-programming-interface-overview"></a><span data-ttu-id="261ce-103">Übersicht über die Microsoft Agent-Programmierschnittstelle</span><span class="sxs-lookup"><span data-stu-id="261ce-103">Microsoft Agent Programming Interface Overview</span></span>

<span data-ttu-id="261ce-104">\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="261ce-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="261ce-105">Die Microsoft-Agent-API bietet Dienste, die die Anzeige und Animation von animierten Zeichen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="261ce-105">The Microsoft Agent API provides services that support the display and animation of animated characters.</span></span> <span data-ttu-id="261ce-106">Der Microsoft-Agent wird als OLE-Automatisierungsserver (Component Object Model \[ com \] ) implementiert und ermöglicht, dass mehrere Anwendungen, so genannte Clients oder Client Anwendungen, gleichzeitig auf die Animation, die Eingabe und die Ausgabe Dienste zugreifen und darauf zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="261ce-106">Implemented as an OLE Automation (Component Object Model \[COM\]) server, Microsoft Agent enables multiple applications, called clients or client applications, to host and access its animation, input, and output services at the same time.</span></span> <span data-ttu-id="261ce-107">Ein Client kann eine beliebige Anwendung sein, die eine Verbindung mit den COM-Schnittstellen des Microsoft-Agents herstellt.</span><span class="sxs-lookup"><span data-stu-id="261ce-107">A client can be any application that connects to the Microsoft Agent's COM interfaces.</span></span>

<span data-ttu-id="261ce-108">Als com-Server wird der Microsoft-Agent automatisch gestartet, wenn eine Client Anwendung die COM-Schnittstellen und Anforderungen zum Herstellen einer Verbindung verwendet.</span><span class="sxs-lookup"><span data-stu-id="261ce-108">As a COM server, Microsoft Agent automatically starts up only when a client application uses the COM interfaces and requests to connect to it.</span></span> <span data-ttu-id="261ce-109">Sie wird weiterhin ausgeführt, bis alle Clients ihre Verbindungen schließen.</span><span class="sxs-lookup"><span data-stu-id="261ce-109">It remains running until all clients close their connections.</span></span> <span data-ttu-id="261ce-110">Wenn keine verbundenen Clients vorhanden sind, wird der Microsoft-Agent automatisch beendet.</span><span class="sxs-lookup"><span data-stu-id="261ce-110">When no connected clients remain, Microsoft Agent automatically exits.</span></span>

<span data-ttu-id="261ce-111">Obwohl Sie die COM-Schnittstellen des Microsoft-Agents direkt abrufen können, enthält der Microsoft-Agent auch ein Microsoft ActiveX-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="261ce-111">Although you can call Microsoft Agent's COM interfaces directly, Microsoft Agent also includes a Microsoft ActiveX control.</span></span> <span data-ttu-id="261ce-112">Dieses Steuerelement erleichtert den Zugriff auf die Dienste von Microsoft Agent von Programmiersprachen, die die ActiveX-Steuerelement Schnittstelle unterstützen.</span><span class="sxs-lookup"><span data-stu-id="261ce-112">This control makes it easy to access Microsoft Agent's services from programming languages that support the ActiveX control interface.</span></span>

<span data-ttu-id="261ce-113">Zusätzlich zur Unterstützung eigenständiger Programme, die für Windows geschrieben wurden, kann der-Agent für die Unterstützung von Webseiten erstellt werden, vorausgesetzt, der Browser unterstützt die ActiveX-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="261ce-113">In addition to supporting stand-alone programs written for Windows, Agent can be scripted to support webpages, provided that the browser supports the ActiveX interface.</span></span> <span data-ttu-id="261ce-114">Microsoft Internet Explorer bietet Unterstützung für ActiveX und Skriptsprachen, die Sie zum Programmieren von-Agents verwenden können.</span><span class="sxs-lookup"><span data-stu-id="261ce-114">Microsoft Internet Explorer includes support for ActiveX as well as scripting languages that you can use to program Agent.</span></span> <span data-ttu-id="261ce-115">Wenn Sie nicht Internet Explorer verwenden, wenden Sie sich an Ihren Hersteller oder Lieferanten über die Unterstützung von ActiveX im Browser.</span><span class="sxs-lookup"><span data-stu-id="261ce-115">If you are not using Internet Explorer, consult with your vendor or supplier about the browser's support for ActiveX.</span></span>

<span data-ttu-id="261ce-116">Die folgenden Informationen bieten eine kurze Übersicht über die Programmierschnittstellen für die Microsoft-Agent-Software.</span><span class="sxs-lookup"><span data-stu-id="261ce-116">The following information provides a brief overview of the programming interfaces for the Microsoft Agent software.</span></span>

-   [<span data-ttu-id="261ce-117">Animations Dienste</span><span class="sxs-lookup"><span data-stu-id="261ce-117">Animation Services</span></span>](animation-services.md)
-   [<span data-ttu-id="261ce-118">Eingabe Dienste</span><span class="sxs-lookup"><span data-stu-id="261ce-118">Input Services</span></span>](input-services.md)
-   [<span data-ttu-id="261ce-119">Das Fenster "Sprachbefehle"</span><span class="sxs-lookup"><span data-stu-id="261ce-119">The Voice Commands Window</span></span>](the-voice-commands-window.md)
-   [<span data-ttu-id="261ce-120">Ausgabe Dienste</span><span class="sxs-lookup"><span data-stu-id="261ce-120">Output Services</span></span>](output-services.md)

 

 




