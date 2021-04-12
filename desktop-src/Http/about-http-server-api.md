---
title: Informationen zur HTTP-Server-API
description: Die HTTP-Server-API stellt Entwicklern eine Low-Level-Schnittstelle der Server Seite der HTTP-Funktionalität bereit, die in RFC 2616 definiert ist.
ms.assetid: 74ad3a1d-cde2-4849-a412-d9d4101eaf12
keywords:
- HTTP-Server-API, Übersicht
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e00fcfe6527b77be32a849f00f62222396f42b5
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "104389951"
---
# <a name="about-http-server-api"></a><span data-ttu-id="93461-104">Informationen zur HTTP-Server-API</span><span class="sxs-lookup"><span data-stu-id="93461-104">About HTTP Server API</span></span>

<span data-ttu-id="93461-105">Die HTTP-Server-API stellt Entwicklern eine Low-Level-Schnittstelle der Server Seite der HTTP-Funktionalität bereit, die in [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt)definiert ist.</span><span class="sxs-lookup"><span data-stu-id="93461-105">The HTTP Server API provides developers with a low-level interface to the server side of the HTTP functionality as defined in [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt).</span></span> <span data-ttu-id="93461-106">Die API ermöglicht es einer Anwendung, HTTP-Anforderungen an URLs zu empfangen und HTTP-Antworten zu senden.</span><span class="sxs-lookup"><span data-stu-id="93461-106">The API enables an application to receive HTTP requests directed to URLs and send HTTP responses.</span></span> <span data-ttu-id="93461-107">Zum Senden dynamischer Antworten werden die ISAPI-oder ASP.NET-Schnittstellen empfohlen.</span><span class="sxs-lookup"><span data-stu-id="93461-107">For sending dynamic responses, the ISAPI or ASP.NET interfaces are recommended.</span></span>

<span data-ttu-id="93461-108">Die HTTP-Server-API ermöglicht die Koexistenz mehrerer Anwendungen auf einem System, wobei derselbe TCP-Port (z. b. Port 80 für http oder Port 443 für HTTPS) und verschiedene Teile des URL-Namespace verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="93461-108">The HTTP Server API enables multiple applications to coexist on a system, sharing the same TCP port (for example, port 80 for HTTP or port 443 for HTTPS) and serving different parts of the URL namespace.</span></span>

<span data-ttu-id="93461-109">Die HTTP-Server-API erfordert Kenntnisse über die Programmiersprache C und eine Vertrautheit mit der Windows-API-Programmierung.</span><span class="sxs-lookup"><span data-stu-id="93461-109">The HTTP Server API requires knowledge of the C programming language and a familiarity with Windows API programming.</span></span> <span data-ttu-id="93461-110">Anwendungen, die keinen Low-Level-Zugriff auf http benötigen, sollten die IIS-ISAPI oder die .NET Framework Klassen für HTTP-basierte Lösungen verwenden.</span><span class="sxs-lookup"><span data-stu-id="93461-110">Applications that do not require low-level access to HTTP should use the IIS ISAPI or the .NET Framework classes for HTTP-based solutions.</span></span>

 

 




