---
title: WebSocket-Protokoll Komponenten-API
description: .
ms.assetid: ae73fd5e-9715-448c-b7ca-898f2705e228
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24edd74fe87185db498e6309a7fda5fa091c7d60
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101962"
---
# <a name="websocket-protocol-component-api"></a><span data-ttu-id="e8b4a-103">WebSocket-Protokoll Komponenten-API</span><span class="sxs-lookup"><span data-stu-id="e8b4a-103">WebSocket Protocol Component API</span></span>

## <a name="purpose"></a><span data-ttu-id="e8b4a-104">Zweck</span><span class="sxs-lookup"><span data-stu-id="e8b4a-104">Purpose</span></span>

<span data-ttu-id="e8b4a-105">Die WebSocket-Protokoll Komponenten-API ermöglicht asynchrone bidirektionale Kommunikationskanäle über HTTP, die über vorhandene Netzwerk Vermittler hinweg funktionieren.</span><span class="sxs-lookup"><span data-stu-id="e8b4a-105">The WebSocket Protocol Component API enables asynchronous, bi-directional communication channels over HTTP that work across existing network intermediaries.</span></span> <span data-ttu-id="e8b4a-106">Mit der WebSocket-Protokoll Komponenten-API verwendet ein Client HTTP für die Kommunikation mit einem Server. dann wechseln beide Seiten zur Verwendung des zugrunde liegenden Protokolls, für das http überlagert wurde (z. b. TCP oder SSL).</span><span class="sxs-lookup"><span data-stu-id="e8b4a-106">With the WebSocket Protocol Component API, a client uses HTTP to communicate with a server, and then both sides switch to using the underlying protocol that HTTP was layered on (such as TCP or SSL).</span></span> <span data-ttu-id="e8b4a-107">Ziel ist es, zuerst http zum Durchlaufen von Netzwerk Vermittlern zu verwenden und dann den eingerichteten End-to-End-TCP/SSL-Kanal für die bidirektionale Anwendungs Kommunikation zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="e8b4a-107">The goal is to first use HTTP to traverse over network intermediaries, and then use the established end-to-end underlying TCP/SSL channel for bi-directional application communication.</span></span> <span data-ttu-id="e8b4a-108">Das WebSocket-Protokoll \[ [wsproto](https://tools.ietf.org/html/rfc6455) \] wird im IETF definiert, während ein zugeordnetes JavaScript-API- \[ [W3CAPI](https://dev.w3.org/html5/websockets/) \] im W3C definiert wird.</span><span class="sxs-lookup"><span data-stu-id="e8b4a-108">The WebSocket protocol \[[WSPROTO](https://tools.ietf.org/html/rfc6455)\] is defined at the IETF, while an associated Javascript API \[[W3CAPI](https://dev.w3.org/html5/websockets/)\] is defined at the W3C.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="e8b4a-109">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="e8b4a-109">In this section</span></span>



| <span data-ttu-id="e8b4a-110">Thema</span><span class="sxs-lookup"><span data-stu-id="e8b4a-110">Topic</span></span>                                                                                                          | <span data-ttu-id="e8b4a-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e8b4a-111">Description</span></span>                                                                 |
|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| [<span data-ttu-id="e8b4a-112">**Datentypen der WebSocket-Protokoll Komponenten-API**</span><span class="sxs-lookup"><span data-stu-id="e8b4a-112">**WebSocket Protocol Component API Data Types**</span></span>](web-socket-protocol-component-api-data-types.md)<br/> | <span data-ttu-id="e8b4a-113">Die WebSocket-Protokoll Komponenten-API definiert diese Datentypen.</span><span class="sxs-lookup"><span data-stu-id="e8b4a-113">The WebSocket Protocol Component API defines these data types.</span></span><br/>   |
| [<span data-ttu-id="e8b4a-114">API-Enumerationen der WebSocket-Protokoll Komponente</span><span class="sxs-lookup"><span data-stu-id="e8b4a-114">WebSocket Protocol Component API Enumerations</span></span>](web-socket-protocol-component-api-enumerations.md)<br/> | <span data-ttu-id="e8b4a-115">Die WebSocket-Protokoll Komponenten-API definiert diese Enumerationen.</span><span class="sxs-lookup"><span data-stu-id="e8b4a-115">The WebSocket Protocol Component API defines these enumerations.</span></span><br/> |
| [<span data-ttu-id="e8b4a-116">Funktionen der WebSocket-Protokoll Komponenten-API</span><span class="sxs-lookup"><span data-stu-id="e8b4a-116">WebSocket Protocol Component API Functions</span></span>](web-socket-protocol-component-api-functions.md)<br/>       | <span data-ttu-id="e8b4a-117">Die WebSocket-Protokoll Komponenten-API definiert diese Funktionen.</span><span class="sxs-lookup"><span data-stu-id="e8b4a-117">The WebSocket Protocol Component API defines these functions.</span></span><br/>    |
| [<span data-ttu-id="e8b4a-118">API-Strukturen der WebSocket-Protokoll Komponente</span><span class="sxs-lookup"><span data-stu-id="e8b4a-118">WebSocket Protocol Component API Structures</span></span>](web-socket-protocol-component-api-structures.md)<br/>     | <span data-ttu-id="e8b4a-119">Diese Strukturen werden von der WebSocket-Protokoll Komponenten-API definiert.</span><span class="sxs-lookup"><span data-stu-id="e8b4a-119">The WebSocket Protocol Component API defines these structures.</span></span><br/>   |



 

## <a name="developer-audience"></a><span data-ttu-id="e8b4a-120">Entwicklergruppe</span><span class="sxs-lookup"><span data-stu-id="e8b4a-120">Developer audience</span></span>

<span data-ttu-id="e8b4a-121">Die WebSocket-Protokoll Komponenten-API ist für die Verwendung durch C/C++-Programmierer konzipiert.</span><span class="sxs-lookup"><span data-stu-id="e8b4a-121">The WebSocket Protocol Component API is designed for use by use by C/C++ programmers.</span></span> <span data-ttu-id="e8b4a-122">Vertrautheit mit http-und Windows-Netzwerken ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e8b4a-122">Familiarity with HTTP and Windows networking is required.</span></span>

> [!Note]  
> <span data-ttu-id="e8b4a-123">Der bevorzugte Weg, das WebSocket-Protokoll unter Windows zu verwenden, ist die [Windows HTTP-Dienste (WinHTTP)-API](/windows/desktop/WinHttp/winhttp-start-page) oder der [Windows. Networking. Sockets-Namespace](/uwp/api/Windows.Networking.Sockets).</span><span class="sxs-lookup"><span data-stu-id="e8b4a-123">The preferred way to use the WebSocket protocol on Windows is through the [Windows HTTP Services (WinHTTP) API](/windows/desktop/WinHttp/winhttp-start-page) or the [Windows.Networking.Sockets namespace](/uwp/api/Windows.Networking.Sockets).</span></span>

 

## <a name="run-time-requirements"></a><span data-ttu-id="e8b4a-124">Laufzeitanforderungen</span><span class="sxs-lookup"><span data-stu-id="e8b4a-124">Run-time requirements</span></span>

<span data-ttu-id="e8b4a-125">Die WebSocket-Protokoll Komponenten-API erfordert Windows 8 und höhere Versionen des Windows-Betriebssystems.</span><span class="sxs-lookup"><span data-stu-id="e8b4a-125">The WebSocket Protocol Component API requires Windows 8 and later versions of the Windows operating system.</span></span> <span data-ttu-id="e8b4a-126">Die APIs können dynamisch über websocket.dll verknüpft werden.</span><span class="sxs-lookup"><span data-stu-id="e8b4a-126">The APIs can be dynamically linked through websocket.dll.</span></span>

> [!Note]  
> <span data-ttu-id="e8b4a-127">websocket.dll bietet Unterstützung für Client-und Server Handshake-bezogene HTTP-Header, überprüft empfangene Handshake-Daten und analysiert den WebSocket-Datenstrom.</span><span class="sxs-lookup"><span data-stu-id="e8b4a-127">websocket.dll provides support for client and server handshake related HTTP headers, verifies received handshake data, and parses the WebSocket data stream.</span></span> <span data-ttu-id="e8b4a-128">Er verarbeitet keine HTTP-spezifischen Vorgänge (Umleitung, Authentifizierung, Proxy Unterstützung) und führt keine e/a-Vorgänge aus (senden oder empfangen von WebSocket-Datenstrom Bytes).</span><span class="sxs-lookup"><span data-stu-id="e8b4a-128">It does not handle any HTTP-specific operations (redirection, authentication, proxy support) nor perform any I/O operations (sending or receiving WebSocket stream bytes).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="e8b4a-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e8b4a-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e8b4a-130">HTTP</span><span class="sxs-lookup"><span data-stu-id="e8b4a-130">HTTP</span></span>](/windows/desktop/Http/http-api-start-page)
</dt> <dt>

[<span data-ttu-id="e8b4a-131">Windows HTTP-Dienste (WinHTTP)</span><span class="sxs-lookup"><span data-stu-id="e8b4a-131">Windows HTTP Services (WinHTTP)</span></span>](/windows/desktop/WinHttp/winhttp-start-page)
</dt> </dl>

 

