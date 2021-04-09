---
title: HTTP-Server-API
description: Die HTTP-Server-API ermöglicht Anwendungen die Kommunikation über HTTP, ohne Microsoft Internet Information Server (IIS) zu verwenden.
ms.assetid: ef18716c-7511-4c8a-99bc-28369c3e46f4
keywords:
- HTTP-Server-API
- HTTP-Server-API, Startseite
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8f99045b24d0ef79c267615791c62da50ed8e40
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101623"
---
# <a name="http-server-api"></a><span data-ttu-id="5c862-105">HTTP-Server-API</span><span class="sxs-lookup"><span data-stu-id="5c862-105">HTTP Server API</span></span>

## <a name="purpose"></a><span data-ttu-id="5c862-106">Zweck</span><span class="sxs-lookup"><span data-stu-id="5c862-106">Purpose</span></span>

<span data-ttu-id="5c862-107">Die HTTP-Server-API ermöglicht Anwendungen die Kommunikation über HTTP, ohne Microsoft Internet Information Server (IIS) zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="5c862-107">The HTTP Server API enables applications to communicate over HTTP without using Microsoft Internet Information Server (IIS).</span></span> <span data-ttu-id="5c862-108">Anwendungen können sich registrieren, um HTTP-Anforderungen für bestimmte URLs zu empfangen, HTTP-Anforderungen zu empfangen und HTTP-Antworten zu senden.</span><span class="sxs-lookup"><span data-stu-id="5c862-108">Applications can register to receive HTTP requests for particular URLs, receive HTTP requests, and send HTTP responses.</span></span> <span data-ttu-id="5c862-109">Die HTTP-Server-API umfasst SSL-Unterstützung, sodass Anwendungen Daten über sichere HTTP-Verbindungen ohne IIS austauschen können.</span><span class="sxs-lookup"><span data-stu-id="5c862-109">The HTTP Server API includes SSL support so that applications can exchange data over secure HTTP connections without IIS.</span></span> <span data-ttu-id="5c862-110">Es ist auch für die Arbeit mit e/a-Abschlussports konzipiert.</span><span class="sxs-lookup"><span data-stu-id="5c862-110">It is also designed to work with I/O completion ports.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="5c862-111">Entwicklergruppe</span><span class="sxs-lookup"><span data-stu-id="5c862-111">Developer audience</span></span>

<span data-ttu-id="5c862-112">Diese API ist für die Verwendung durch C/C++-Programmierer konzipiert.</span><span class="sxs-lookup"><span data-stu-id="5c862-112">This API is designed for use by C/C++ programmers.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="5c862-113">Laufzeitanforderungen</span><span class="sxs-lookup"><span data-stu-id="5c862-113">Run-time requirements</span></span>

<span data-ttu-id="5c862-114">Die HTTP-Server-API wird auf Windows Server 2003-Betriebssystemen und unter Windows XP mit Service Pack 2 (SP2) unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5c862-114">The HTTP Server API is supported on Windows Server 2003 operating systems and on Windows XP with Service Pack 2 (SP2).</span></span> <span data-ttu-id="5c862-115">Beachten Sie, dass Microsoft IIS 5, das unter Windows XP mit SP2 ausgeführt wird, Port 80 nicht gemeinsam mit anderen HTTP-Anwendungen freigeben kann, die gleichzeitig ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="5c862-115">Be aware that Microsoft IIS 5 running on Windows XP with SP2 is not able to share port 80 with other HTTP applications running simultaneously.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="5c862-116">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="5c862-116">In this section</span></span>



| <span data-ttu-id="5c862-117">Thema</span><span class="sxs-lookup"><span data-stu-id="5c862-117">Topic</span></span>                                                                           | <span data-ttu-id="5c862-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5c862-118">Description</span></span>                                                                                             |
|---------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5c862-119">Informationen zur HTTP-Server-API</span><span class="sxs-lookup"><span data-stu-id="5c862-119">About HTTP Server API</span></span>](about-http-server-api.md)<br/>                   | <span data-ttu-id="5c862-120">Allgemeine Informationen zu http.</span><span class="sxs-lookup"><span data-stu-id="5c862-120">General information about HTTP.</span></span><br/>                                                              |
| [<span data-ttu-id="5c862-121">Verwenden der HTTP-Server-API</span><span class="sxs-lookup"><span data-stu-id="5c862-121">Using HTTP Server API</span></span>](using-http-server-api.md)<br/>                   | <span data-ttu-id="5c862-122">Leitfaden für Prozeduren zur Verwendung von http.</span><span class="sxs-lookup"><span data-stu-id="5c862-122">Procedural guide for using HTTP.</span></span><br/>                                                             |
| [<span data-ttu-id="5c862-123">HTTP-Server-API-Referenz</span><span class="sxs-lookup"><span data-stu-id="5c862-123">HTTP Server API Reference</span></span>](http-server-api-reference.md)<br/>           | <span data-ttu-id="5c862-124">Dokumentation zu bestimmten Funktionen, Strukturen und Enumerationstypen, die in http verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="5c862-124">Documentation of specific functions, structures, and enumeration types available in HTTP.</span></span><br/>    |
| [<span data-ttu-id="5c862-125">Beispielanwendung für http-Server</span><span class="sxs-lookup"><span data-stu-id="5c862-125">HTTP Server Sample Application</span></span>](http-server-sample-application.md)<br/> | <span data-ttu-id="5c862-126">Eine Beispielanwendung, die zeigt, wie die HTTP-Server-API verwendet wird, um Server seitige Aufgaben auszuführen.</span><span class="sxs-lookup"><span data-stu-id="5c862-126">A sample application that shows how to use the HTTP Server API to perform server-side tasks.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="5c862-127">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5c862-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5c862-128">Windows HTTP-Dienste (WinHTTP)</span><span class="sxs-lookup"><span data-stu-id="5c862-128">Windows HTTP Services (WinHTTP)</span></span>](/windows/desktop/WinHttp/winhttp-start-page)
</dt> </dl>

 

