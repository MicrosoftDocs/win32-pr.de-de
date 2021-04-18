---
title: Ping
description: Verwenden Sie das pingpaket zum Herstellen einer Verbindung und Aushandeln der Sicherheit mit dem Server.
ms.assetid: 10b01fe8-d1a3-4a3b-ac35-e3557d3ef4ee
keywords:
- Ping-Bits
topic_type:
- apiref
api_name:
- Ping
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86c9428a39cfaebbce150583d47a344c4a36ca66
ms.sourcegitcommit: 476861130ea63675206d1f06e517059705b930ed
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2019
ms.locfileid: "106340472"
---
# <a name="ping"></a><span data-ttu-id="6c0d7-104">Ping</span><span class="sxs-lookup"><span data-stu-id="6c0d7-104">Ping</span></span>

<span data-ttu-id="6c0d7-105">Verwenden Sie das **pingpaket** zum Herstellen einer Verbindung und Aushandeln der Sicherheit mit dem Server.</span><span class="sxs-lookup"><span data-stu-id="6c0d7-105">Use the **Ping** packet to establish a connection and negotiate security with the server.</span></span>

``` syntax
BITS_POST remote-URL HTTP/1.1
BITS-Packet-Type: Ping
```

## <a name="headers"></a><span data-ttu-id="6c0d7-106">Header</span><span class="sxs-lookup"><span data-stu-id="6c0d7-106">Headers</span></span>

<dl> <dt>

<span data-ttu-id="6c0d7-107"><span id="BITS_POST"></span><span id="bits_post"></span>Bits- \_ Post</span><span class="sxs-lookup"><span data-stu-id="6c0d7-107"><span id="BITS_POST"></span><span id="bits_post"></span>BITS\_POST</span></span>
</dt> <dd>

<span data-ttu-id="6c0d7-108">Bits-spezifisches Verb, das dieses Paket für den BITS-Server identifiziert.</span><span class="sxs-lookup"><span data-stu-id="6c0d7-108">BITS-specific verb that identifies this packet to the BITS server.</span></span>

<span data-ttu-id="6c0d7-109">Ersetzen Sie Remote-URL durch den absoluten oder relativen URI.</span><span class="sxs-lookup"><span data-stu-id="6c0d7-109">Replace remote-URL with the absolute or relative URI.</span></span> <span data-ttu-id="6c0d7-110">Ersetzen Sie in der Regel Remote-URL durch den Remote Dateinamen des Auftrags.</span><span class="sxs-lookup"><span data-stu-id="6c0d7-110">Typically, replace remote-URL with the remote file name of the job.</span></span>

</dd> <dt>

<span data-ttu-id="6c0d7-111"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>Bits-Pakettyp</span><span class="sxs-lookup"><span data-stu-id="6c0d7-111"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type</span></span>
</dt> <dd>

<span data-ttu-id="6c0d7-112">Identifiziert dieses Anforderungspaket als Ping-Paket.</span><span class="sxs-lookup"><span data-stu-id="6c0d7-112">Identifies this request packet as a Ping packet.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6c0d7-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6c0d7-113">Remarks</span></span>

<span data-ttu-id="6c0d7-114">Das **Ping** -Paket ist optional.</span><span class="sxs-lookup"><span data-stu-id="6c0d7-114">The **Ping** packet is optional.</span></span> <span data-ttu-id="6c0d7-115">Anstatt ein **Ping** -Paket zu senden, können Sie das Paket " [**Create-Session**](create-session.md) " verwenden, um eine Verbindung herzustellen und Sicherheit auszuhandeln.</span><span class="sxs-lookup"><span data-stu-id="6c0d7-115">Instead of sending a **Ping** packet, you can use the [**Create-Session**](create-session.md) packet to establish a connection and negotiate security.</span></span> <span data-ttu-id="6c0d7-116">Es ist jedoch effizienter, das **Ping** -Paket zu diesem Zweck zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="6c0d7-116">However, it is more efficient to use the **Ping** packet for this purpose.</span></span>

## <a name="see-also"></a><span data-ttu-id="6c0d7-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6c0d7-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c0d7-118">**Bestätigung für Ping**</span><span class="sxs-lookup"><span data-stu-id="6c0d7-118">**Ack for Ping**</span></span>](ack-for-ping.md)
</dt> <dt>

[<span data-ttu-id="6c0d7-119">**Create-Session**</span><span class="sxs-lookup"><span data-stu-id="6c0d7-119">**Create-Session**</span></span>](create-session.md)
</dt> </dl>

 

 




