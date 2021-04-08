---
title: Threadsicherheit
description: Alle Funktionen in dieser API können gleichzeitig von verschiedenen Threads aus aufgerufen werden. Jedes Objekt, das als Parameter an die Funktionen übergeben wird, hat jedoch ein bestimmtes Threading Verhalten, wie unten beschrieben.
ms.assetid: 712d6750-884e-421a-8ecf-efcd4ec9b21d
keywords:
- Thread Sicherheit-Webdienste für Windows
- Wwsapi
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fed84cac9634148742c92f1b0d4b4ecdb905ac42
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "103734849"
---
# <a name="thread-safety"></a><span data-ttu-id="d2627-107">Threadsicherheit</span><span class="sxs-lookup"><span data-stu-id="d2627-107">Thread Safety</span></span>

<span data-ttu-id="d2627-108">Alle Funktionen in dieser API können gleichzeitig von verschiedenen Threads aus aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="d2627-108">All functions in this API are safe to call concurrently from different threads.</span></span> <span data-ttu-id="d2627-109">Jedes Objekt, das als Parameter an die Funktionen übergeben wird, hat jedoch ein bestimmtes Threading Verhalten, wie unten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="d2627-109">However, each object passed as a parameter to the functions have specific threading behavior, as described below.</span></span>


<span data-ttu-id="d2627-110">Die folgenden Handles sind Single Thread und unterstützen keine gleichzeitigen Vorgänge für eine bestimmte Instanz:</span><span class="sxs-lookup"><span data-stu-id="d2627-110">The following handles are single threaded and do not support concurrent operations for a particular instance:</span></span>

-   [<span data-ttu-id="d2627-111">WS- \_ Heap</span><span class="sxs-lookup"><span data-stu-id="d2627-111">WS\_HEAP</span></span>](ws-heap.md)
-   [<span data-ttu-id="d2627-112">WS- \_ Nachricht</span><span class="sxs-lookup"><span data-stu-id="d2627-112">WS\_MESSAGE</span></span>](ws-message.md)
-   [<span data-ttu-id="d2627-113">WS- \_ XML- \_ Puffer</span><span class="sxs-lookup"><span data-stu-id="d2627-113">WS\_XML\_BUFFER</span></span>](ws-xml-buffer.md)
-   [<span data-ttu-id="d2627-114">WS- \_ XML- \_ Reader</span><span class="sxs-lookup"><span data-stu-id="d2627-114">WS\_XML\_READER</span></span>](ws-xml-reader.md)
-   [<span data-ttu-id="d2627-115">WS- \_ XML- \_ Writer</span><span class="sxs-lookup"><span data-stu-id="d2627-115">WS\_XML\_WRITER</span></span>](ws-xml-writer.md)
-   [<span data-ttu-id="d2627-116">WS- \_ Fehler</span><span class="sxs-lookup"><span data-stu-id="d2627-116">WS\_ERROR</span></span>](ws-error.md)
-   [<span data-ttu-id="d2627-117">WS- \_ Vorgangs \_ Kontext</span><span class="sxs-lookup"><span data-stu-id="d2627-117">WS\_OPERATION\_CONTEXT</span></span>](ws-operation-context.md)
-   [<span data-ttu-id="d2627-118">WS- \_ Richtlinie</span><span class="sxs-lookup"><span data-stu-id="d2627-118">WS\_POLICY</span></span>](ws-policy.md)
-   [<span data-ttu-id="d2627-119">WS- \_ Metadaten</span><span class="sxs-lookup"><span data-stu-id="d2627-119">WS\_METADATA</span></span>](ws-metadata.md)
-   [<span data-ttu-id="d2627-120">WS- \_ Sicherheits \_ Token</span><span class="sxs-lookup"><span data-stu-id="d2627-120">WS\_SECURITY\_TOKEN</span></span>](ws-security-token.md)
-   [<span data-ttu-id="d2627-121">WS- \_ Sicherheits \_ Kontext</span><span class="sxs-lookup"><span data-stu-id="d2627-121">WS\_SECURITY\_CONTEXT</span></span>](ws-security-context.md)

<span data-ttu-id="d2627-122">Die folgenden Handles sind frei Thread und unterstützen gleichzeitige Vorgänge für eine bestimmte Instanz:</span><span class="sxs-lookup"><span data-stu-id="d2627-122">The following handles are free threaded and do support concurrent operations for a particular instance:</span></span>

-   [<span data-ttu-id="d2627-123">WS- \_ Kanal</span><span class="sxs-lookup"><span data-stu-id="d2627-123">WS\_CHANNEL</span></span>](ws-channel.md)
-   [<span data-ttu-id="d2627-124">WS- \_ Listener</span><span class="sxs-lookup"><span data-stu-id="d2627-124">WS\_LISTENER</span></span>](ws-listener.md)
-   [<span data-ttu-id="d2627-125">WS- \_ Dienst \_ Host</span><span class="sxs-lookup"><span data-stu-id="d2627-125">WS\_SERVICE\_HOST</span></span>](ws-service-host.md)
-   [<span data-ttu-id="d2627-126">WS- \_ Dienst \_ Proxy</span><span class="sxs-lookup"><span data-stu-id="d2627-126">WS\_SERVICE\_PROXY</span></span>](ws-service-proxy.md)

<span data-ttu-id="d2627-127">Für all diese Handles wird Threading in Bezug auf Vorgänge (nicht Funktionsaufrufe) definiert.</span><span class="sxs-lookup"><span data-stu-id="d2627-127">For all these handles, threading is defined in terms of operations (not function calls).</span></span> <span data-ttu-id="d2627-128">Ein Vorgang wird für Funktionen, die synchron aufgerufen werden, anders definiert als bei Funktionen, die asynchron aufgerufen werden:</span><span class="sxs-lookup"><span data-stu-id="d2627-128">An operation is defined differently for functions invoked synchronously versus functions invoked asynchronously:</span></span>

-   <span data-ttu-id="d2627-129">Bei Funktionen, die synchron aufgerufen werden, steht der Vorgang während der Ausführung der Funktion aus.</span><span class="sxs-lookup"><span data-stu-id="d2627-129">For functions invoked synchronously, the operation is pending during the execution of the function.</span></span>
-   <span data-ttu-id="d2627-130">Für Funktionen, die asynchron aufgerufen werden, ist der Vorgang während der Ausführung der Funktion ausstehend, wenn die Funktion einen anderen Rückgabecode als **WS \_ S \_** zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="d2627-130">For functions invoked asynchronously, if the function returns a return code other than **WS\_S\_ASYNC** the operation is pending during the execution of the function.</span></span> <span data-ttu-id="d2627-131">Wenn die Funktion jedoch **WS \_ S \_ Async** zurückgibt, ist der Vorgang bis zum Aufruf des asynchronen [**WS- \_ \_ Rückrufs**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback) ausstehend.</span><span class="sxs-lookup"><span data-stu-id="d2627-131">If the function returns **WS\_S\_ASYNC** , however, the operation is pending until the [**WS\_ASYNC\_CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback) is invoked.</span></span> <span data-ttu-id="d2627-132">Weitere Informationen zum asynchronen Aufrufen von Funktionen finden Sie im Thema zum [asynchronen Modell](asynchronous-model.md) .</span><span class="sxs-lookup"><span data-stu-id="d2627-132">For more information about invoking functions asynchronously, see the [Asynchronous Model](asynchronous-model.md) topic.</span></span> <span data-ttu-id="d2627-133">Fehlercodes finden Sie unter [Rückgabewerte für Windows-Webdienste](windows-web-services-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="d2627-133">For error codes, see [Windows Web Services Return Values](windows-web-services-return-values.md).</span></span>

<span data-ttu-id="d2627-134">Wenn der Threading Vertrag für ein Objekt nicht befolgt wird, führt dies zu einem nicht definierten Verhalten.</span><span class="sxs-lookup"><span data-stu-id="d2627-134">Failure to follow the threading contract for an object will result in undefined behavior.</span></span>

 

 




