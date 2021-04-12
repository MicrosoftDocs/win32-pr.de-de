---
title: Create-Session
description: Verwenden Sie das Create-Session Paket, um eine Uploadsitzung mit dem BITS-Server anzufordern.
ms.assetid: eeb8ff83-2a7f-4fef-9df7-8c12febfcf36
keywords:
- Create-Session Bits
topic_type:
- apiref
api_name:
- Create-Session
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 425ad3bd36305f94547cf2cd8b13c1a420491499
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104471860"
---
# <a name="create-session"></a><span data-ttu-id="15f30-104">Create-Session</span><span class="sxs-lookup"><span data-stu-id="15f30-104">Create-Session</span></span>

<span data-ttu-id="15f30-105">Verwenden Sie das Paket " **Create-Session** ", um eine Uploadsitzung mit dem BITS-Server anzufordern.</span><span class="sxs-lookup"><span data-stu-id="15f30-105">Use the **Create-Session** packet to request an upload session with the BITS server.</span></span>

``` syntax
BITS_POST remote-URL HTTP/1.1
BITS-Packet-Type: Create-Session
BITS-Supported-Protocols: {guid1} ... {guidN}
```

## <a name="headers"></a><span data-ttu-id="15f30-106">Header</span><span class="sxs-lookup"><span data-stu-id="15f30-106">Headers</span></span>

<dl> <dt>

<span data-ttu-id="15f30-107"><span id="BITS_POST"></span><span id="bits_post"></span>Bits- \_ Post</span><span class="sxs-lookup"><span data-stu-id="15f30-107"><span id="BITS_POST"></span><span id="bits_post"></span>BITS\_POST</span></span>
</dt> <dd>

<span data-ttu-id="15f30-108">Bits-spezifisches Verb, das dieses Paket für den BITS-Server identifiziert.</span><span class="sxs-lookup"><span data-stu-id="15f30-108">BITS-specific verb that identifies this packet to the BITS server.</span></span>

<span data-ttu-id="15f30-109">Ersetzen Sie Remote-URL durch den absoluten oder relativen URI.</span><span class="sxs-lookup"><span data-stu-id="15f30-109">Replace remote-URL with the absolute or relative URI.</span></span> <span data-ttu-id="15f30-110">Ersetzen Sie in der Regel Remote-URL durch den Remote Dateinamen des Auftrags.</span><span class="sxs-lookup"><span data-stu-id="15f30-110">Typically, replace remote-URL with the remote file name of the job.</span></span> <span data-ttu-id="15f30-111">Überlegungen zum Netzwerk Lastenausgleich finden Sie unter dem Bits-Host-ID-Header.</span><span class="sxs-lookup"><span data-stu-id="15f30-111">For network load balancing considerations, see the BITS-Host-Id header.</span></span>

</dd> <dt>

<span data-ttu-id="15f30-112"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>Bits-Pakettyp</span><span class="sxs-lookup"><span data-stu-id="15f30-112"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type</span></span>
</dt> <dd>

<span data-ttu-id="15f30-113">Identifiziert dieses Anforderungspaket als Create-Session Paket.</span><span class="sxs-lookup"><span data-stu-id="15f30-113">Identifies this request packet as a Create-Session packet.</span></span>

</dd> <dt>

<span data-ttu-id="15f30-114"><span id="BITS-Supported-Protocols"></span><span id="bits-supported-protocols"></span><span id="BITS-SUPPORTED-PROTOCOLS"></span>Bits-unterstützte Protokolle</span><span class="sxs-lookup"><span data-stu-id="15f30-114"><span id="BITS-Supported-Protocols"></span><span id="bits-supported-protocols"></span><span id="BITS-SUPPORTED-PROTOCOLS"></span>BITS-Supported-Protocols</span></span>
</dt> <dd>

<span data-ttu-id="15f30-115">Durch Leerzeichen getrennte Liste der Protokolle, die vom Client unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="15f30-115">Space-delimited list of the protocols that the client supports.</span></span> <span data-ttu-id="15f30-116">Verwenden Sie Zeichen folgen-GUIDs, um die Protokolle zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="15f30-116">Use string GUIDs to identify the protocols.</span></span> <span data-ttu-id="15f30-117">Geben Sie die Liste in der bevorzugten Reihenfolge als die am wenigsten bevorzugte Liste an.</span><span class="sxs-lookup"><span data-stu-id="15f30-117">Specify the list in order of preference from most to least preferred.</span></span> <span data-ttu-id="15f30-118">In der folgenden Tabelle wird das Protokoll aufgelistet, das vom BITS-Client unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="15f30-118">The following table lists the protocol that the BITS client supports.</span></span> <span data-ttu-id="15f30-119">{GUID1} ersetzen... {guidn} mit einer oder mehreren Zeichen folgen-GUIDs aus der Liste.</span><span class="sxs-lookup"><span data-stu-id="15f30-119">Replace {guid1} ... {guidN} with one or more string GUIDs from the list.</span></span>



| <span data-ttu-id="15f30-120">Protokoll</span><span class="sxs-lookup"><span data-stu-id="15f30-120">Protocol</span></span>                                          | <span data-ttu-id="15f30-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="15f30-121">Description</span></span>                         |
|---------------------------------------------------|-------------------------------------|
| <span data-ttu-id="15f30-122">{7df0354d-249b-430t-820d-3d2a9bef 4931}</span><span class="sxs-lookup"><span data-stu-id="15f30-122">{7df0354d-249b-430f-820d-3d2a9bef4931}</span></span><br/> | <span data-ttu-id="15f30-123">Bits 1,5-uploadprotokoll</span><span class="sxs-lookup"><span data-stu-id="15f30-123">BITS 1.5 Upload Protocol</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="15f30-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="15f30-124">Remarks</span></span>

<span data-ttu-id="15f30-125">Sie sollten ein [**Ping**](ping.md) -Paket senden, um eine HTTP-Verbindung herzustellen, bevor Sie das Create-Session Paket senden.</span><span class="sxs-lookup"><span data-stu-id="15f30-125">You should send a [**Ping**](ping.md) packet to establish an HTTP connection before sending the Create-Session packet.</span></span> <span data-ttu-id="15f30-126">Das Create-Session Paket kann auch die Verbindung herstellen. Das Create-Session Paket ist jedoch weniger effizient.</span><span class="sxs-lookup"><span data-stu-id="15f30-126">The Create-Session packet can also establish the connection; however, the Create-Session packet is less efficient.</span></span>

<span data-ttu-id="15f30-127">Der Server wählt das gewünschte Protokoll aus der Liste aus, die der Client im Header Bits-supported-Protokolls bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="15f30-127">The server selects the protocol it wants to use from the list the client provides in the BITS-Supported-Protocols header.</span></span> <span data-ttu-id="15f30-128">Der Server gibt das ausgewählte Protokoll im BITS-Protocol-Header der Bestätigung für das Antwortpaket " [**Create-Session**](ack-for-create-session.md) " zurück.</span><span class="sxs-lookup"><span data-stu-id="15f30-128">The server returns the selected protocol in the BITS-Protocol header of the [**Ack for Create-Session**](ack-for-create-session.md) response packet.</span></span>

<span data-ttu-id="15f30-129">Der Client erwartet, dass der Server eine Bestätigung für das Antwortpaket " [**Create-Session**](ack-for-create-session.md) " zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="15f30-129">The client expects the server to return an [**Ack for Create-Session**](ack-for-create-session.md) response packet.</span></span> <span data-ttu-id="15f30-130">Wenn der Server eine Sitzung einrichten konnte, verwendet der Client das [**fragmentanforderungs**](fragment.md) Paket, um Bereiche der Datei an den Server zu senden.</span><span class="sxs-lookup"><span data-stu-id="15f30-130">If the server was able to establish a session, the client uses the [**Fragment**](fragment.md) request packet to send ranges of the file to the server.</span></span>

## <a name="see-also"></a><span data-ttu-id="15f30-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="15f30-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15f30-132">**Bestätigung für Create-Session**</span><span class="sxs-lookup"><span data-stu-id="15f30-132">**Ack for Create-Session**</span></span>](ack-for-create-session.md)
</dt> <dt>

[<span data-ttu-id="15f30-133">**Fragment**</span><span class="sxs-lookup"><span data-stu-id="15f30-133">**Fragment**</span></span>](fragment.md)
</dt> <dt>

[<span data-ttu-id="15f30-134">**Ping**</span><span class="sxs-lookup"><span data-stu-id="15f30-134">**Ping**</span></span>](ping.md)
</dt> </dl>

 

 





