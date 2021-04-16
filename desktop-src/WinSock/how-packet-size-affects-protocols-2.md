---
description: Probleme mit der Medienpaket Größe, die im Thema Informationen zur Medienpaket Größe erläutert werden, wirken sich auf die verschiedenen PF- \_ IPX-Protokolle aus.
ms.assetid: 7f0643b8-6bb2-4dbb-b306-d9b2e0d0e03c
title: Auswirkungen der Paketgröße auf Protokolle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c778ee6c75cd558d19cdf1cbb76052065e03c427
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343508"
---
# <a name="how-packet-size-affects-protocols"></a><span data-ttu-id="d0a96-103">Auswirkungen der Paketgröße auf Protokolle</span><span class="sxs-lookup"><span data-stu-id="d0a96-103">How Packet Size Affects Protocols</span></span>

<span data-ttu-id="d0a96-104">Probleme mit der Medienpaket Größe, die im Thema [Informationen zur Medienpaket Größe](about-media-packet-size-2.md)erläutert werden, wirken sich auf die verschiedenen PF- \_ IPX-Protokolle aus.</span><span class="sxs-lookup"><span data-stu-id="d0a96-104">Media packet size issues discussed in the topic, [About Media Packet Size](about-media-packet-size-2.md), affect the various PF\_IPX protocols differently.</span></span> <span data-ttu-id="d0a96-105">Eine gängige Strategie für die Behandlung verschiedener Beschränkungen von Router und Mediengrößen besteht darin, die vollständige Mediengröße zu verwenden, wenn die Netzwerk Nummer der Remote Station mit der lokalen Station übereinstimmt, und andernfalls auf die minimale Paketgröße zurückgreifen.</span><span class="sxs-lookup"><span data-stu-id="d0a96-105">A common strategy for handling various router and media size constraints is to use the full media size when the remote station's network number matches the local station, and fall back to the minimum packet size otherwise.</span></span>

## <a name="parameters"></a><span data-ttu-id="d0a96-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d0a96-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0a96-107"><span id="NSPROTO_IPX"></span><span id="nsproto_ipx"></span>nsproto- \_ IPX</span><span class="sxs-lookup"><span data-stu-id="d0a96-107"><span id="NSPROTO_IPX"></span><span id="nsproto_ipx"></span>NSPROTO\_IPX</span></span>
</dt> <dd>

<span data-ttu-id="d0a96-108">Stellt einen Datagramm-Dienst bereit. jedes Datagramm muss innerhalb der maximalen Paketgröße liegen.</span><span class="sxs-lookup"><span data-stu-id="d0a96-108">Provides a datagram service; each datagram must reside within the maximum packet size.</span></span> <span data-ttu-id="d0a96-109">Winsock legt die maximale datagrammpaketgröße auf die lokale Medienpaket Größe abzüglich des IPX-Headers fest.</span><span class="sxs-lookup"><span data-stu-id="d0a96-109">Winsock sets the maximum datagram packet size to the local media packet size minus the IPX header.</span></span> <span data-ttu-id="d0a96-110">Beachten Sie jedoch, dass beim Weiterleiten des Pakets möglicherweise routereinschränkungen auf die Route-Route trifft.</span><span class="sxs-lookup"><span data-stu-id="d0a96-110">Keep in mind, however, that if the packet is routed, it may hit router restrictions en route.</span></span> <span data-ttu-id="d0a96-111">Stellen Sie sicher, dass die Anwendung auf die 546-Byte-Datagramme zurückgreifen kann.</span><span class="sxs-lookup"><span data-stu-id="d0a96-111">Make sure your application can fall back to 546-byte datagrams.</span></span>

</dd> <dt>

<span data-ttu-id="d0a96-112"><span id="NSPROTO_SPX"></span><span id="nsproto_spx"></span>nsproto- \_ SPX</span><span class="sxs-lookup"><span data-stu-id="d0a96-112"><span id="NSPROTO_SPX"></span><span id="nsproto_spx"></span>NSPROTO\_SPX</span></span>
</dt> <dd>

<span data-ttu-id="d0a96-113">Stellt Stream-und sequenzierte Paketdienste bereit.</span><span class="sxs-lookup"><span data-stu-id="d0a96-113">Provides stream and sequenced-packet services.</span></span> <span data-ttu-id="d0a96-114">WinSock IPX/SPX ermöglicht Datenstreams und Nachrichten, die mehrere Pakete umfassen, sodass die Paketgröße nicht die Menge der von [**Send**](/windows/desktop/api/Winsock2/nf-winsock2-send) und [**empfangener**](/windows/desktop/api/winsock/nf-winsock-recv)behandelten Daten beschränkt.</span><span class="sxs-lookup"><span data-stu-id="d0a96-114">Winsock IPX/SPX lets data streams and messages span multiple packets, so packet size does not limit the amount of data handled by [**send**](/windows/desktop/api/Winsock2/nf-winsock2-send) and [**recv**](/windows/desktop/api/winsock/nf-winsock-recv).</span></span> <span data-ttu-id="d0a96-115">Allerdings muss die Größe des zugrunde liegenden Mediums ordnungsgemäß festgelegt werden, oder das erste große Paket kann nicht zugestellt werden, und die Verbindung wird zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="d0a96-115">However, the underlying media size must be set correctly or the first large packet will be undeliverable and the connection will reset.</span></span> <span data-ttu-id="d0a96-116">Wenn sich die Zielstation im lokalen Netzwerk befindet, legt Winsock die Paketgröße auf die Medienpaket Größe fest.</span><span class="sxs-lookup"><span data-stu-id="d0a96-116">If the target station is on the local network, Winsock sets its packet size to the media packet size.</span></span> <span data-ttu-id="d0a96-117">Andernfalls ist der Standardwert 512 Bytes.</span><span class="sxs-lookup"><span data-stu-id="d0a96-117">Otherwise, it defaults to 512 bytes.</span></span> <span data-ttu-id="d0a96-118">Diese Größe kann unmittelbar nach [**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) oder [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept) über [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)geändert werden.</span><span class="sxs-lookup"><span data-stu-id="d0a96-118">This size can be changed immediately after [**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect) or [**accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept) through [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt).</span></span>

</dd> <dt>

<span data-ttu-id="d0a96-119"><span id="NSPROTO_SPXII"></span><span id="nsproto_spxii"></span>nsproto- \_ SPXII</span><span class="sxs-lookup"><span data-stu-id="d0a96-119"><span id="NSPROTO_SPXII"></span><span id="nsproto_spxii"></span>NSPROTO\_SPXII</span></span>
</dt> <dd>

<span data-ttu-id="d0a96-120">SPXII bietet eine große Internet Paket Aushandlung, um die Größe der Pakete mit der optimalen Anpassung zu gewährleisten und erfordert keinen programmiereingriff.</span><span class="sxs-lookup"><span data-stu-id="d0a96-120">SPXII features large Internet packet negotiation to maintain a best-fit size for packets and does not require programmer intervention.</span></span> <span data-ttu-id="d0a96-121">Wenn die Remote Station SPXII jedoch nicht unterstützt und in Standard-SPX aushandiert, sind die nsproto \_ SPX-Regeln wirksam.</span><span class="sxs-lookup"><span data-stu-id="d0a96-121">However, if the remote station does not support SPXII and negotiates down to standard SPX, the NSPROTO\_SPX rules are in effect.</span></span>



| <span data-ttu-id="d0a96-122">Protokoll</span><span class="sxs-lookup"><span data-stu-id="d0a96-122">Protocol</span></span>     | <span data-ttu-id="d0a96-123">Medien</span><span class="sxs-lookup"><span data-stu-id="d0a96-123">Media</span></span>      | <span data-ttu-id="d0a96-124">type</span><span class="sxs-lookup"><span data-stu-id="d0a96-124">Type</span></span>        | <span data-ttu-id="d0a96-125">Größe des Datenpakets</span><span class="sxs-lookup"><span data-stu-id="d0a96-125">Data packet size</span></span> |
|--------------|------------|-------------|------------------|
| <span data-ttu-id="d0a96-126">nsproto- \_ IPX</span><span class="sxs-lookup"><span data-stu-id="d0a96-126">NSPROTO\_IPX</span></span> | <span data-ttu-id="d0a96-127">Ethernet</span><span class="sxs-lookup"><span data-stu-id="d0a96-127">Ethernet</span></span>   | <span data-ttu-id="d0a96-128">Ethernet II</span><span class="sxs-lookup"><span data-stu-id="d0a96-128">Ethernet II</span></span> |                  |
|              |            | <span data-ttu-id="d0a96-129">802.3</span><span class="sxs-lookup"><span data-stu-id="d0a96-129">802.3</span></span>       |                  |
|              |            | <span data-ttu-id="d0a96-130">802.2</span><span class="sxs-lookup"><span data-stu-id="d0a96-130">802.2</span></span>       | <span data-ttu-id="d0a96-131">1466</span><span class="sxs-lookup"><span data-stu-id="d0a96-131">1466</span></span>             |
|              |            | <span data-ttu-id="d0a96-132">Einbruch</span><span class="sxs-lookup"><span data-stu-id="d0a96-132">SNAP</span></span>        |                  |
|              | <span data-ttu-id="d0a96-133">Token Ring</span><span class="sxs-lookup"><span data-stu-id="d0a96-133">Token Ring</span></span> | <span data-ttu-id="d0a96-134">4 Megabit</span><span class="sxs-lookup"><span data-stu-id="d0a96-134">4 megabit</span></span>   |                  |
|              |            | <span data-ttu-id="d0a96-135">16 Megabit</span><span class="sxs-lookup"><span data-stu-id="d0a96-135">16 megabit</span></span>  |                  |
| <span data-ttu-id="d0a96-136">nsproto- \_ SPX</span><span class="sxs-lookup"><span data-stu-id="d0a96-136">NSPROTO\_SPX</span></span> | <span data-ttu-id="d0a96-137">Ethernet</span><span class="sxs-lookup"><span data-stu-id="d0a96-137">Ethernet</span></span>   | <span data-ttu-id="d0a96-138">Ethernet II</span><span class="sxs-lookup"><span data-stu-id="d0a96-138">Ethernet II</span></span> |                  |
|              |            | <span data-ttu-id="d0a96-139">802.3</span><span class="sxs-lookup"><span data-stu-id="d0a96-139">802.3</span></span>       |                  |
|              |            | <span data-ttu-id="d0a96-140">802.2</span><span class="sxs-lookup"><span data-stu-id="d0a96-140">802.2</span></span>       | <span data-ttu-id="d0a96-141">1454</span><span class="sxs-lookup"><span data-stu-id="d0a96-141">1454</span></span>             |
|              |            | <span data-ttu-id="d0a96-142">Einbruch</span><span class="sxs-lookup"><span data-stu-id="d0a96-142">SNAP</span></span>        |                  |
|              | <span data-ttu-id="d0a96-143">Token Ring</span><span class="sxs-lookup"><span data-stu-id="d0a96-143">Token Ring</span></span> | <span data-ttu-id="d0a96-144">4 Megabit</span><span class="sxs-lookup"><span data-stu-id="d0a96-144">4 megabit</span></span>   |                  |
|              |            | <span data-ttu-id="d0a96-145">16 Megabit</span><span class="sxs-lookup"><span data-stu-id="d0a96-145">16 megabit</span></span>  |                  |



 

</dd> </dl>

 

 



