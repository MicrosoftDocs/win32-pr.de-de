---
title: WebSocket-Protokollkomponenten-API
description: WebSocket-Protokollkomponenten-API
ms.assetid: ae73fd5e-9715-448c-b7ca-898f2705e228
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c16290a7af5b5fea406e5f47c0db718d775e4d17
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088818"
---
# <a name="websocket-protocol-component-api"></a><span data-ttu-id="ef014-103">WebSocket-Protokollkomponenten-API</span><span class="sxs-lookup"><span data-stu-id="ef014-103">WebSocket Protocol Component API</span></span>

## <a name="purpose"></a><span data-ttu-id="ef014-104">Zweck</span><span class="sxs-lookup"><span data-stu-id="ef014-104">Purpose</span></span>

<span data-ttu-id="ef014-105">Die WebSocket-Protokollkomponenten-API ermöglicht asynchrone, bidirektionale Kommunikationskanäle über HTTP, die über vorhandene Netzwerkhändler hinweg funktionieren.</span><span class="sxs-lookup"><span data-stu-id="ef014-105">The WebSocket Protocol Component API enables asynchronous, bi-directional communication channels over HTTP that work across existing network intermediaries.</span></span> <span data-ttu-id="ef014-106">Mit der WebSocket-Protokollkomponenten-API verwendet ein Client HTTP für die Kommunikation mit einem Server, und dann wechseln beide Seiten zur Verwendung des zugrunde liegenden Protokolls, über das HTTP überlagert wurde (z. B. TCP oder SSL).</span><span class="sxs-lookup"><span data-stu-id="ef014-106">With the WebSocket Protocol Component API, a client uses HTTP to communicate with a server, and then both sides switch to using the underlying protocol that HTTP was layered on (such as TCP or SSL).</span></span> <span data-ttu-id="ef014-107">Ziel ist es, zuerst HTTP zu verwenden, um Netzwerkhändler zu durchlaufen, und dann den eingerichteten zugrunde liegenden End-to-End-TCP/SSL-Kanal für die bidirektionale Anwendungskommunikation zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="ef014-107">The goal is to first use HTTP to traverse over network intermediaries, and then use the established end-to-end underlying TCP/SSL channel for bi-directional application communication.</span></span> <span data-ttu-id="ef014-108">Das WebSocket-Protokoll \[ [WSPROTO](https://tools.ietf.org/html/rfc6455) wird in der IETF definiert, während eine zugeordnete \] JavaScript-API \[ [W3CAPI](https://dev.w3.org/html5/websockets/) im \] W3C definiert ist.</span><span class="sxs-lookup"><span data-stu-id="ef014-108">The WebSocket protocol \[[WSPROTO](https://tools.ietf.org/html/rfc6455)\] is defined at the IETF, while an associated Javascript API \[[W3CAPI](https://dev.w3.org/html5/websockets/)\] is defined at the W3C.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="ef014-109">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="ef014-109">In this section</span></span>



| <span data-ttu-id="ef014-110">Thema</span><span class="sxs-lookup"><span data-stu-id="ef014-110">Topic</span></span>                                                                                                          | <span data-ttu-id="ef014-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ef014-111">Description</span></span>                                                                 |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [<span data-ttu-id="ef014-112">**API-Datentypen der WebSocket-Protokollkomponente**</span><span class="sxs-lookup"><span data-stu-id="ef014-112">**WebSocket Protocol Component API Data Types**</span></span>](web-socket-protocol-component-api-data-types.md)<br/> | <span data-ttu-id="ef014-113">Die WebSocket-Protokollkomponenten-API definiert diese Datentypen.</span><span class="sxs-lookup"><span data-stu-id="ef014-113">The WebSocket Protocol Component API defines these data types.</span></span><br/>   |
| [<span data-ttu-id="ef014-114">WebSocket-Protokollkomponenten-API-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="ef014-114">WebSocket Protocol Component API Enumerations</span></span>](web-socket-protocol-component-api-enumerations.md)<br/> | <span data-ttu-id="ef014-115">Die WebSocket-Protokollkomponenten-API definiert diese Enumerationen.</span><span class="sxs-lookup"><span data-stu-id="ef014-115">The WebSocket Protocol Component API defines these enumerations.</span></span><br/> |
| [<span data-ttu-id="ef014-116">Api-Funktionen der WebSocket-Protokollkomponente</span><span class="sxs-lookup"><span data-stu-id="ef014-116">WebSocket Protocol Component API Functions</span></span>](web-socket-protocol-component-api-functions.md)<br/>       | <span data-ttu-id="ef014-117">Die WebSocket-Protokollkomponenten-API definiert diese Funktionen.</span><span class="sxs-lookup"><span data-stu-id="ef014-117">The WebSocket Protocol Component API defines these functions.</span></span><br/>    |
| [<span data-ttu-id="ef014-118">API-Strukturen der WebSocket-Protokollkomponente</span><span class="sxs-lookup"><span data-stu-id="ef014-118">WebSocket Protocol Component API Structures</span></span>](web-socket-protocol-component-api-structures.md)<br/>     | <span data-ttu-id="ef014-119">Die WebSocket-Protokollkomponenten-API definiert diese Strukturen.</span><span class="sxs-lookup"><span data-stu-id="ef014-119">The WebSocket Protocol Component API defines these structures.</span></span><br/>   |



 

## <a name="developer-audience"></a><span data-ttu-id="ef014-120">Entwicklergruppe</span><span class="sxs-lookup"><span data-stu-id="ef014-120">Developer audience</span></span>

<span data-ttu-id="ef014-121">Die WebSocket-Protokollkomponenten-API ist für die Verwendung durch C/C++-Programmierer konzipiert.</span><span class="sxs-lookup"><span data-stu-id="ef014-121">The WebSocket Protocol Component API is designed for use by use by C/C++ programmers.</span></span> <span data-ttu-id="ef014-122">Sie müssen mit HTTP- und Windows-Netzwerken vertraut sein.</span><span class="sxs-lookup"><span data-stu-id="ef014-122">Familiarity with HTTP and Windows networking is required.</span></span>

> [!Note]  
> <span data-ttu-id="ef014-123">Die bevorzugte Methode zur Verwendung des WebSocket-Protokolls unter Windows ist die Verwendung der [Windows HTTP Services-API (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page) oder des [Windows.Networking.Sockets-Namespace.](/uwp/api/Windows.Networking.Sockets)</span><span class="sxs-lookup"><span data-stu-id="ef014-123">The preferred way to use the WebSocket protocol on Windows is through the [Windows HTTP Services (WinHTTP) API](/windows/desktop/WinHttp/winhttp-start-page) or the [Windows.Networking.Sockets namespace](/uwp/api/Windows.Networking.Sockets).</span></span>

 

## <a name="run-time-requirements"></a><span data-ttu-id="ef014-124">Laufzeitanforderungen</span><span class="sxs-lookup"><span data-stu-id="ef014-124">Run-time requirements</span></span>

<span data-ttu-id="ef014-125">Die WebSocket-Protokollkomponenten-API erfordert Windows 8 und neuere Versionen des Windows-Betriebssystems.</span><span class="sxs-lookup"><span data-stu-id="ef014-125">The WebSocket Protocol Component API requires Windows 8 and later versions of the Windows operating system.</span></span> <span data-ttu-id="ef014-126">Die APIs können dynamisch über die websocket.dll.</span><span class="sxs-lookup"><span data-stu-id="ef014-126">The APIs can be dynamically linked through websocket.dll.</span></span>

> [!Note]  
> <span data-ttu-id="ef014-127">websocket.dll unterstützt Client- und Serverhandshake-bezogene HTTP-Header, überprüft empfangene Handshakedaten und analysiert den WebSocket-Datenstrom.</span><span class="sxs-lookup"><span data-stu-id="ef014-127">websocket.dll provides support for client and server handshake related HTTP headers, verifies received handshake data, and parses the WebSocket data stream.</span></span> <span data-ttu-id="ef014-128">Er verarbeitet keine HTTP-spezifischen Vorgänge (Umleitung, Authentifizierung, Proxyunterstützung) und führt keine E/A-Vorgänge aus (Senden oder Empfangen von WebSocket-Streambytes).</span><span class="sxs-lookup"><span data-stu-id="ef014-128">It does not handle any HTTP-specific operations (redirection, authentication, proxy support) nor perform any I/O operations (sending or receiving WebSocket stream bytes).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="ef014-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ef014-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ef014-130">HTTP</span><span class="sxs-lookup"><span data-stu-id="ef014-130">HTTP</span></span>](/windows/desktop/Http/http-api-start-page)
</dt> <dt>

[<span data-ttu-id="ef014-131">Windows-HTTP-Dienste (WinHTTP)</span><span class="sxs-lookup"><span data-stu-id="ef014-131">Windows HTTP Services (WinHTTP)</span></span>](/windows/desktop/WinHttp/winhttp-start-page)
</dt> </dl>

 

