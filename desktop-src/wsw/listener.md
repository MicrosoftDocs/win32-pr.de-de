---
title: Listener
description: Ein Listener wird vom Client verwendet, um einen eingehenden Kanal von einem Dienst zu akzeptieren.
ms.assetid: fffda587-23f5-4c7a-93c5-f03d9d3fafb2
keywords:
- Listenerweb Dienste für Windows
- Wwsapi
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e372f3fa9109647e009f0258c059cc4c2065f6bc
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104391247"
---
# <a name="listener"></a><span data-ttu-id="c7164-106">Listener</span><span class="sxs-lookup"><span data-stu-id="c7164-106">Listener</span></span>

<span data-ttu-id="c7164-107">Ein Listener wird vom Client verwendet, um einen eingehenden [Kanal](channel.md) von einem Dienst zu akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="c7164-107">A listener is used by the client to accept an incoming [channel](channel.md) from a service.</span></span>

<span data-ttu-id="c7164-108">Zum Erstellen eines listners geben Sie den Kanaltyp als Enumerationswert für den [**WS- \_ \_ Kanaltyp**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) , die [Bindungs](binding.md) Informationen und die zu überwachende [URL](url.md) an.</span><span class="sxs-lookup"><span data-stu-id="c7164-108">To create a listner, you specify the channel type as a [**WS\_CHANNEL\_TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) enumeration value, the [binding](binding.md) information, and the [URL](url.md) to listen on.</span></span>


<span data-ttu-id="c7164-109">Um mit dem lauschen an der URL zu beginnen, müssen Sie die [**wsopenlistener**](/windows/desktop/api/WebServices/nf-webservices-wsopenlistener) -Funktion aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="c7164-109">To start listening on the URL, call the [**WsOpenListener**](/windows/desktop/api/WebServices/nf-webservices-wsopenlistener) function.</span></span>

<span data-ttu-id="c7164-110">Um eingehende Verbindungen zu akzeptieren, wenden Sie [**wsaccept-Channel**](/windows/desktop/api/WebServices/nf-webservices-wsacceptchannel)an.</span><span class="sxs-lookup"><span data-stu-id="c7164-110">To accept incoming communications, call [**WsAcceptChannel**](/windows/desktop/api/WebServices/nf-webservices-wsacceptchannel).</span></span>

<span data-ttu-id="c7164-111">Zum Abbrechen ausstehender e/a-Vorgänge für einen Listener rufen Sie [**wsabortlistener**](/windows/desktop/api/WebServices/nf-webservices-wsabortlistener)auf.</span><span class="sxs-lookup"><span data-stu-id="c7164-111">To cancel pending IO for a listener, call [**WsAbortListener**](/windows/desktop/api/WebServices/nf-webservices-wsabortlistener).</span></span>

<span data-ttu-id="c7164-112">Informationen zu den Status Übergängen für einen Listener finden Sie in der [**WS-listenerstatusenumeration \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_state) .</span><span class="sxs-lookup"><span data-stu-id="c7164-112">For information on the state transitions for a listener, see the [**WS\_LISTENER\_STATE**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_state) enumeration.</span></span>

<span data-ttu-id="c7164-113">Die folgenden Rückrufe sind Teil des-Listener:</span><span class="sxs-lookup"><span data-stu-id="c7164-113">The following callbacks are part of the listener:</span></span>

-   [<span data-ttu-id="c7164-114">**WS- \_ Abbruch- \_ Listener- \_ Rückruf**</span><span class="sxs-lookup"><span data-stu-id="c7164-114">**WS\_ABORT\_LISTENER\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_abort_listener_callback)
-   [<span data-ttu-id="c7164-115">**WS \_ Accept \_ Channel- \_ Rückruf**</span><span class="sxs-lookup"><span data-stu-id="c7164-115">**WS\_ACCEPT\_CHANNEL\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_accept_channel_callback)
-   [<span data-ttu-id="c7164-116">**WS \_ Close \_ Listener \_ Callback**</span><span class="sxs-lookup"><span data-stu-id="c7164-116">**WS\_CLOSE\_LISTENER\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_close_listener_callback)
-   [<span data-ttu-id="c7164-117">**WS \_ Create \_ Channel \_ für \_ \_ listenerrückruf**</span><span class="sxs-lookup"><span data-stu-id="c7164-117">**WS\_CREATE\_CHANNEL\_FOR\_LISTENER\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_create_channel_for_listener_callback)
-   [<span data-ttu-id="c7164-118">**WS \_ Create \_ Listener- \_ Rückruf**</span><span class="sxs-lookup"><span data-stu-id="c7164-118">**WS\_CREATE\_LISTENER\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_create_listener_callback)
-   [<span data-ttu-id="c7164-119">**WS- \_ freier \_ Listener- \_ Rückruf**</span><span class="sxs-lookup"><span data-stu-id="c7164-119">**WS\_FREE\_LISTENER\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_free_listener_callback)
-   [<span data-ttu-id="c7164-120">**WS \_ get \_ Listener- \_ Eigenschaften \_ Rückruf**</span><span class="sxs-lookup"><span data-stu-id="c7164-120">**WS\_GET\_LISTENER\_PROPERTY\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_get_listener_property_callback)
-   [<span data-ttu-id="c7164-121">**WS \_ Open \_ Listener- \_ Rückruf**</span><span class="sxs-lookup"><span data-stu-id="c7164-121">**WS\_OPEN\_LISTENER\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_open_listener_callback)
-   [<span data-ttu-id="c7164-122">**WS-rücksetzungs \_ \_ \_ Rückruf**</span><span class="sxs-lookup"><span data-stu-id="c7164-122">**WS\_RESET\_LISTENER\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_reset_listener_callback)
-   [<span data-ttu-id="c7164-123">**WS- \_ Satz \_ Listener- \_ Eigenschaften \_ Rückruf**</span><span class="sxs-lookup"><span data-stu-id="c7164-123">**WS\_SET\_LISTENER\_PROPERTY\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_set_listener_property_callback)

<span data-ttu-id="c7164-124">Die folgenden Enumerationen sind Teil des-Listener:</span><span class="sxs-lookup"><span data-stu-id="c7164-124">The following enumerations are part of the listener:</span></span>

-   [<span data-ttu-id="c7164-125">**WS \_ -IP- \_ Version**</span><span class="sxs-lookup"><span data-stu-id="c7164-125">**WS\_IP\_VERSION**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_ip_version)
-   [<span data-ttu-id="c7164-126">**WS- \_ Listener- \_ Eigenschaften- \_ ID**</span><span class="sxs-lookup"><span data-stu-id="c7164-126">**WS\_LISTENER\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_listener_property_id)
-   [<span data-ttu-id="c7164-127">**WS \_ - \_ listenerstatus**</span><span class="sxs-lookup"><span data-stu-id="c7164-127">**WS\_LISTENER\_STATE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_listener_state)

<span data-ttu-id="c7164-128">Die folgenden Funktionen sind Teil des-Listener:</span><span class="sxs-lookup"><span data-stu-id="c7164-128">The following functions are part of the listener:</span></span>

-   [<span data-ttu-id="c7164-129">**Wsabortlistener**</span><span class="sxs-lookup"><span data-stu-id="c7164-129">**WsAbortListener**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsabortlistener)
-   [<span data-ttu-id="c7164-130">**Wsakzeptchannel**</span><span class="sxs-lookup"><span data-stu-id="c7164-130">**WsAcceptChannel**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsacceptchannel)
-   [<span data-ttu-id="c7164-131">**Wscloselistener**</span><span class="sxs-lookup"><span data-stu-id="c7164-131">**WsCloseListener**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscloselistener)
-   [<span data-ttu-id="c7164-132">**Wscreatelistener**</span><span class="sxs-lookup"><span data-stu-id="c7164-132">**WsCreateListener**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscreatelistener)
-   [<span data-ttu-id="c7164-133">**Wsfreelistener**</span><span class="sxs-lookup"><span data-stu-id="c7164-133">**WsFreeListener**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsfreelistener)
-   [<span data-ttu-id="c7164-134">**Wsgetlistenerproperty**</span><span class="sxs-lookup"><span data-stu-id="c7164-134">**WsGetListenerProperty**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetlistenerproperty)
-   [<span data-ttu-id="c7164-135">**Wsopumlistener**</span><span class="sxs-lookup"><span data-stu-id="c7164-135">**WsOpenListener**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsopenlistener)
-   [<span data-ttu-id="c7164-136">**Wsresetlistener**</span><span class="sxs-lookup"><span data-stu-id="c7164-136">**WsResetListener**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsresetlistener)
-   [<span data-ttu-id="c7164-137">**Wssetlistenerproperty**</span><span class="sxs-lookup"><span data-stu-id="c7164-137">**WsSetListenerProperty**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wssetlistenerproperty)

<span data-ttu-id="c7164-138">Das folgende Handle ist Teil des-Listener:</span><span class="sxs-lookup"><span data-stu-id="c7164-138">The following handle is part of the listener:</span></span>

-   [<span data-ttu-id="c7164-139">WS- \_ Listener</span><span class="sxs-lookup"><span data-stu-id="c7164-139">WS\_LISTENER</span></span>](ws-listener.md)

<span data-ttu-id="c7164-140">Die folgenden Strukturen sind Teil des-Listener:</span><span class="sxs-lookup"><span data-stu-id="c7164-140">The following structures are part of the listener:</span></span>

-   [<span data-ttu-id="c7164-141">**WS \_ Custom \_ Listener \_ -Rückrufe**</span><span class="sxs-lookup"><span data-stu-id="c7164-141">**WS\_CUSTOM\_LISTENER\_CALLBACKS**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_custom_listener_callbacks)
-   [<span data-ttu-id="c7164-142">**nicht zulässige WS-Teil Zeichenfolgen des \_ \_ Benutzer- \_ Agents \_**</span><span class="sxs-lookup"><span data-stu-id="c7164-142">**WS\_DISALLOWED\_USER\_AGENT\_SUBSTRINGS**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_disallowed_user_agent_substrings)
-   [<span data-ttu-id="c7164-143">**WS \_ - \_ Hostnamen**</span><span class="sxs-lookup"><span data-stu-id="c7164-143">**WS\_HOST\_NAMES**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_host_names)
-   [<span data-ttu-id="c7164-144">**WS \_ - \_ Listenereigenschaften**</span><span class="sxs-lookup"><span data-stu-id="c7164-144">**WS\_LISTENER\_PROPERTIES**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_listener_properties)
-   [<span data-ttu-id="c7164-145">**WS \_ - \_ Listenereigenschaft**</span><span class="sxs-lookup"><span data-stu-id="c7164-145">**WS\_LISTENER\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_listener_property)

 

 




