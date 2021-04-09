---
title: Informationen zu WinInet
description: Mit der Windows Internet (WinInet) Application Programming Interface (API) kann Ihre Anwendung mit FTP-und HTTP-Protokollen interagieren, um auf Internet Ressourcen zuzugreifen.
ms.assetid: 0a06f2af-957a-4dff-a8cc-187370181b5c
keywords:
- Informationen zu WinInet WinInet
- WinInet WinInet, Informationen zu
- WinInet WinInet, Startseite
- Windows Internet Wininet
- Internet, Windows Internet Wininet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4513e5c3912a483fd4dbef96f452c5712717c8a5
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "103948470"
---
# <a name="about-wininet"></a><span data-ttu-id="623b9-108">Informationen zu WinInet</span><span class="sxs-lookup"><span data-stu-id="623b9-108">About WinINet</span></span>

> [!NOTE]
> <span data-ttu-id="623b9-109">Für App-Container seit Windows 10, Version 1709, ist http/2 (siehe [RFC7540](https://tools.ietf.org/html/rfc7540)) standardmäßig aktiviert.</span><span class="sxs-lookup"><span data-stu-id="623b9-109">For app containers since Windows 10, version 1709, HTTP/2 (see [RFC7540](https://tools.ietf.org/html/rfc7540)) is on by default.</span></span>

<span data-ttu-id="623b9-110">Mit der Windows Internet (WinInet) Application Programming Interface (API) kann Ihre Anwendung mit FTP-und HTTP-Protokollen interagieren, um auf Internet Ressourcen zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="623b9-110">The Windows Internet (WinINet) application programming interface (API) enables your application to interact with FTP and HTTP protocols to access Internet resources.</span></span> <span data-ttu-id="623b9-111">Bei der Weiterentwicklung von Standards behandeln diese Funktionen die Änderungen in den zugrunde liegenden Protokollen, sodass Sie konsistentes Verhalten gewährleisten können.</span><span class="sxs-lookup"><span data-stu-id="623b9-111">As standards evolve, these functions handle the changes in underlying protocols, enabling them to maintain consistent behavior.</span></span>

<span data-ttu-id="623b9-112">**Windows XP und Windows Server 2003 R2 und früher:** Auch aktivierte Anwendungen können mit Gopher interagieren.</span><span class="sxs-lookup"><span data-stu-id="623b9-112">**Windows XP and Windows Server 2003 R2 and earlier:** Also enabled applications to interact with Gopher.</span></span>

<span data-ttu-id="623b9-113">Weitere Informationen finden Sie unter</span><span class="sxs-lookup"><span data-stu-id="623b9-113">For more information, see:</span></span>

-   [<span data-ttu-id="623b9-114">WinInet im Vergleich zu WinHTTP</span><span class="sxs-lookup"><span data-stu-id="623b9-114">WinINet vs. WinHTTP</span></span>](wininet-vs-winhttp.md)
-   [<span data-ttu-id="623b9-115">HINTERNET-Handles</span><span class="sxs-lookup"><span data-stu-id="623b9-115">HINTERNET Handles</span></span>](appendix-a-hinternet-handles.md)
-   [<span data-ttu-id="623b9-116">Unterstützung von IP-Version 6</span><span class="sxs-lookup"><span data-stu-id="623b9-116">IP Version 6 Support</span></span>](ip-version-6-support.md)
-   [<span data-ttu-id="623b9-117">Inhalts \_ Codierung</span><span class="sxs-lookup"><span data-stu-id="623b9-117">Content\_Encoding</span></span>](content-encoding.md)
-   [<span data-ttu-id="623b9-118">Zwischenspeichern</span><span class="sxs-lookup"><span data-stu-id="623b9-118">Caching</span></span>](caching.md)
-   [<span data-ttu-id="623b9-119">Allgemeine Funktionen</span><span class="sxs-lookup"><span data-stu-id="623b9-119">Common Functions</span></span>](common-functions.md)
-   [<span data-ttu-id="623b9-120">FTP-Sitzungen</span><span class="sxs-lookup"><span data-stu-id="623b9-120">FTP Sessions</span></span>](ftp-sessions.md)
-   [<span data-ttu-id="623b9-121">HTTP-Sitzungen</span><span class="sxs-lookup"><span data-stu-id="623b9-121">HTTP Sessions</span></span>](http-sessions.md)
-   [<span data-ttu-id="623b9-122">HTTP-Cookies</span><span class="sxs-lookup"><span data-stu-id="623b9-122">HTTP Cookies</span></span>](http-cookies.md)
-   [<span data-ttu-id="623b9-123">Asynchroner Vorgang</span><span class="sxs-lookup"><span data-stu-id="623b9-123">Asynchronous Operation</span></span>](asynchronous-operation.md)
-   [<span data-ttu-id="623b9-124">Behandeln der Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="623b9-124">Handling Authentication</span></span>](handling-authentication.md)
-   [<span data-ttu-id="623b9-125">Behandeln von Uniform Resource Locators</span><span class="sxs-lookup"><span data-stu-id="623b9-125">Handling Uniform Resource Locators</span></span>](handling-uniform-resource-locators.md)
-   [<span data-ttu-id="623b9-126">Sicherheits \_ Richtlinie</span><span class="sxs-lookup"><span data-stu-id="623b9-126">Security\_Guideline</span></span>](security-guidelines.md)

## <a name="internet-protocols"></a><span data-ttu-id="623b9-127">Internet Protokolle</span><span class="sxs-lookup"><span data-stu-id="623b9-127">Internet Protocols</span></span>

<span data-ttu-id="623b9-128">Die beiden primären Internet Protokolle sind FTP und http.</span><span class="sxs-lookup"><span data-stu-id="623b9-128">The two primary Internet protocols are FTP and HTTP.</span></span> <span data-ttu-id="623b9-129">Weitere Informationen zu diesen Protokollen finden Sie in den RFC-Dokumenten (Request for Comments) für FTP und http:</span><span class="sxs-lookup"><span data-stu-id="623b9-129">For more information about these protocols, see the Request For Comments (RFC) documents for FTP and HTTP:</span></span>

-   <span data-ttu-id="623b9-130">[RFC 959](https://www.ietf.org/rfc/rfc0959.txt), *File Transfer Protocol (FTP)*.</span><span class="sxs-lookup"><span data-stu-id="623b9-130">[RFC 959](https://www.ietf.org/rfc/rfc0959.txt), *File Transfer Protocol (FTP)*.</span></span>
-   <span data-ttu-id="623b9-131">[RFC 1945](ftp://ftp.isi.edu/in-notes/rfc1945.txt), *Hypertext Transfer Protocol-HTTP/1.0*.</span><span class="sxs-lookup"><span data-stu-id="623b9-131">[RFC 1945](ftp://ftp.isi.edu/in-notes/rfc1945.txt), *Hypertext Transfer Protocol - HTTP/1.0*.</span></span>
-   <span data-ttu-id="623b9-132">[RFC 2616](https://www.ietf.org/rfc/rfc2616.txt), *Hypertext Transfer Protocol-HTTP/1.1*.</span><span class="sxs-lookup"><span data-stu-id="623b9-132">[RFC 2616](https://www.ietf.org/rfc/rfc2616.txt), *Hypertext Transfer Protocol - HTTP/1.1*.</span></span>

> [!NOTE]  
> <span data-ttu-id="623b9-133">(Diese Ressourcen sind in einigen Sprachen und Ländern möglicherweise nicht verfügbar.)</span><span class="sxs-lookup"><span data-stu-id="623b9-133">(These resources may not be available in some languages and countries.)</span></span>

<span data-ttu-id="623b9-134">**Windows XP und Windows Server 2003 R2 und früher:** Das Gopher-Protokoll wurde ebenfalls unterstützt.</span><span class="sxs-lookup"><span data-stu-id="623b9-134">**Windows XP and Windows Server 2003 R2 and earlier:** The Gopher protocol was also supported.</span></span> <span data-ttu-id="623b9-135">Weitere Informationen finden Sie unter [RFC 1436](https://www.ietf.org/rfc/rfc1436.txt), *dem Internet Gopher-Protokoll*.</span><span class="sxs-lookup"><span data-stu-id="623b9-135">See [RFC 1436](https://www.ietf.org/rfc/rfc1436.txt), *The Internet Gopher Protocol*.</span></span>
