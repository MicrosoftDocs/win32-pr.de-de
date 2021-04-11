---
title: HTTP-Server-API-Funktionen
description: In diesem Thema werden und nicht unterstützte Funktionen der HTTP-Server-API unterstützt.
ms.assetid: 448fe5a5-e79f-4c3a-aa76-94cff988f24f
keywords:
- HTTP-Server-API-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48d5f529811b08999d6e1cfffa99fc85288ec471
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310999"
---
# <a name="http-server-api-features"></a><span data-ttu-id="d0e74-104">HTTP-Server-API-Funktionen</span><span class="sxs-lookup"><span data-stu-id="d0e74-104">HTTP Server API Features</span></span>

<span data-ttu-id="d0e74-105">In der folgenden Liste werden die unterstützten und nicht unterstützten Funktionen der HTTP-Server-API beschrieben.</span><span class="sxs-lookup"><span data-stu-id="d0e74-105">The following lists describe supported and unsupported features of the HTTP Server API.</span></span>

## <a name="features-supported"></a><span data-ttu-id="d0e74-106">Unterstützte Features</span><span class="sxs-lookup"><span data-stu-id="d0e74-106">Features Supported</span></span>

<span data-ttu-id="d0e74-107">HTTP unterstützt die folgenden Funktionen:</span><span class="sxs-lookup"><span data-stu-id="d0e74-107">HTTP supports the following features:</span></span>

-   <span data-ttu-id="d0e74-108">HTTP v 1.0-und v 1.1-Serverfunktionen.</span><span class="sxs-lookup"><span data-stu-id="d0e74-108">HTTP v1.0 and v1.1 server functionality.</span></span>
-   <span data-ttu-id="d0e74-109">Secure Sockets Layer 3,0 (SSL) mit Unterstützung für Client-und Server Zertifikate.</span><span class="sxs-lookup"><span data-stu-id="d0e74-109">Secure Sockets Layer 3.0 (SSL) with support for client and server certificates.</span></span>
-   <span data-ttu-id="d0e74-110">Zwischenspeichern von Daten Fragmenten zur Verwendung in nachfolgenden Antworten.</span><span class="sxs-lookup"><span data-stu-id="d0e74-110">Caching of data fragments for use in subsequent responses.</span></span>
-   <span data-ttu-id="d0e74-111">Unterstützung für IPv6-und IPv4-Adressierung.</span><span class="sxs-lookup"><span data-stu-id="d0e74-111">Support for IPv6 and IPv4 addressing.</span></span>
-   <span data-ttu-id="d0e74-112">URL-Namespace Reservierungen für die Anwendungssicherheit.</span><span class="sxs-lookup"><span data-stu-id="d0e74-112">URL namespace reservations for application security.</span></span>
-   <span data-ttu-id="d0e74-113">True-Handles für alle-Objekte.</span><span class="sxs-lookup"><span data-stu-id="d0e74-113">True handles for all objects.</span></span>
-   <span data-ttu-id="d0e74-114">Synchrone und asynchrone e/a-Modelle.</span><span class="sxs-lookup"><span data-stu-id="d0e74-114">Synchronous and asynchronous I/O models.</span></span>
-   <span data-ttu-id="d0e74-115">Unterstützung für WOW64 auf Computern unter 64-Bit-Windows ab Windows Server 2003 mit Service Pack 1 (SP1).</span><span class="sxs-lookup"><span data-stu-id="d0e74-115">Support for WOW64 on computers running on 64-bit Windows starting with Windows Server 2003 with Service Pack 1 (SP1).</span></span>

## <a name="features-not-supported"></a><span data-ttu-id="d0e74-116">Nicht unterstützte Funktionen</span><span class="sxs-lookup"><span data-stu-id="d0e74-116">Features Not Supported</span></span>

<span data-ttu-id="d0e74-117">Die HTTP-Server-API unterstützt nicht die folgenden Funktionen:</span><span class="sxs-lookup"><span data-stu-id="d0e74-117">The HTTP Server API does not support the following functionality:</span></span>

-   <span data-ttu-id="d0e74-118">Die HTTP-Server-API führt keine Client-oder Server Authentifizierung basierend auf dem Inhalt der HTTP-Anforderungs Header aus.</span><span class="sxs-lookup"><span data-stu-id="d0e74-118">The HTTP Server API does not perform client or server authentication based on the contents of the HTTP request headers.</span></span> <span data-ttu-id="d0e74-119">Die erforderliche Authentifizierung muss von der Anwendung implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="d0e74-119">Any required authentication must be implemented by the application.</span></span>
-   <span data-ttu-id="d0e74-120">WOW64 auf Computern, die auf 64-Bit-Windows-Computern ausgeführt werden, wird unter Windows Server 2003 und Windows XP mit Service Pack 2 (SP2) und früher nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d0e74-120">WOW64 on computers running on 64-bit Windows is not supported on Windows Server 2003, and Windows XP with Service Pack 2 (SP2) and earlier.</span></span>
-   <span data-ttu-id="d0e74-121">Die HTTP-Server-API unterstützt keine Protokollierung von HTTP-Anforderungen und-Antworten.</span><span class="sxs-lookup"><span data-stu-id="d0e74-121">The HTTP Server API does not support logging HTTP requests and responses.</span></span>
-   <span data-ttu-id="d0e74-122">Die HTTP-Server-API segmentieren ausgehende HTTP-Antworten nicht.</span><span class="sxs-lookup"><span data-stu-id="d0e74-122">The HTTP Server API does not chunk outgoing HTTP responses.</span></span> <span data-ttu-id="d0e74-123">Die Anwendung muss bei Bedarf die Antwort Segmentierung implementieren.</span><span class="sxs-lookup"><span data-stu-id="d0e74-123">The application must implement response chunking if required.</span></span>

 

 




