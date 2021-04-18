---
title: Cancel-Session
description: Verwenden Sie das Cancel-Session Paket, um die Uploadsitzung mit dem BITS-Server zu beenden.
ms.assetid: 670d061e-ab73-4aa8-85ba-2c9693794235
keywords:
- Cancel-Session Bits
topic_type:
- apiref
api_name:
- Cancel-Session
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 017097bea656309aabf3d773f34152805fd6a579
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "106338630"
---
# <a name="cancel-session"></a><span data-ttu-id="d9a10-104">Cancel-Session</span><span class="sxs-lookup"><span data-stu-id="d9a10-104">Cancel-Session</span></span>

<span data-ttu-id="d9a10-105">Verwenden Sie das **Cancel-Session-** Paket, um die Uploadsitzung mit dem BITS-Server zu beenden.</span><span class="sxs-lookup"><span data-stu-id="d9a10-105">Use the **Cancel-Session** packet to terminate the upload session with the BITS server.</span></span>

``` syntax
BITS_POST remote-URL HTTP/1.1
BITS-Packet-Type: Cancel-Session
BITS-Session-Id: {guid}
```

## <a name="headers"></a><span data-ttu-id="d9a10-106">Header</span><span class="sxs-lookup"><span data-stu-id="d9a10-106">Headers</span></span>

<dl> <dt>

<span data-ttu-id="d9a10-107"><span id="BITS_POST"></span><span id="bits_post"></span>Bits- \_ Post</span><span class="sxs-lookup"><span data-stu-id="d9a10-107"><span id="BITS_POST"></span><span id="bits_post"></span>BITS\_POST</span></span>
</dt> <dd>

<span data-ttu-id="d9a10-108">Bits-spezifisches Verb, das dieses Paket für den BITS-Server identifiziert.</span><span class="sxs-lookup"><span data-stu-id="d9a10-108">BITS-specific verb that identifies this packet to the BITS server.</span></span>

<span data-ttu-id="d9a10-109">Ersetzen Sie Remote-URL durch den absoluten oder relativen URI.</span><span class="sxs-lookup"><span data-stu-id="d9a10-109">Replace remote-URL with the absolute or relative URI.</span></span> <span data-ttu-id="d9a10-110">Ersetzen Sie in der Regel Remote-URL durch den Remote Dateinamen des Auftrags.</span><span class="sxs-lookup"><span data-stu-id="d9a10-110">Typically, replace remote-URL with the remote file name of the job.</span></span> <span data-ttu-id="d9a10-111">Überlegungen zum Netzwerk Lastenausgleich finden Sie im "Bits-Host-ID"-Header im Paket " [**Create-Session**](create-session.md) ".</span><span class="sxs-lookup"><span data-stu-id="d9a10-111">For network load balancing considerations, see the BITS-Host-Id header in the [**Create-Session**](create-session.md) packet.</span></span>

</dd> <dt>

<span data-ttu-id="d9a10-112"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>Bits-Pakettyp</span><span class="sxs-lookup"><span data-stu-id="d9a10-112"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type</span></span>
</dt> <dd>

<span data-ttu-id="d9a10-113">Identifiziert dieses Anforderungspaket als Cancel-Session Paket.</span><span class="sxs-lookup"><span data-stu-id="d9a10-113">Identifies this request packet as a Cancel-Session packet.</span></span>

</dd> <dt>

<span data-ttu-id="d9a10-114"><span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>Bits-Session-ID</span><span class="sxs-lookup"><span data-stu-id="d9a10-114"><span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BITS-Session-Id</span></span>
</dt> <dd>

<span data-ttu-id="d9a10-115">Zeichen folgen-GUID, die die Sitzung mit dem Server identifiziert.</span><span class="sxs-lookup"><span data-stu-id="d9a10-115">String GUID that identifies the session to the server.</span></span> <span data-ttu-id="d9a10-116">Ersetzen Sie {GUID} durch die Sitzungs-ID, die der Server in der Bestätigung für das Antwortpaket " [**Create-Session**](ack-for-create-session.md) " zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="d9a10-116">Replace {guid} with the session identifier that the server returns in the [**Ack for Create-Session**](ack-for-create-session.md) response packet.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d9a10-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d9a10-117">Remarks</span></span>

<span data-ttu-id="d9a10-118">Dieses Paket bricht einen Uploadauftrag ab, wenn er vor dem Senden des letzten Fragments gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="d9a10-118">This packet cancels an upload job if it is sent before the last fragment is sent.</span></span> <span data-ttu-id="d9a10-119">Cancel-Session hat keine Auswirkung auf eine Datei, deren letztes Fragment bereits gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="d9a10-119">Cancel-Session has no effect on a file whose last fragment has already been sent.</span></span> <span data-ttu-id="d9a10-120">Wenn der BITS-Server das letzte Fragment empfängt, schreibt er die Datei in das endgültige Ziel und stellt die Datei im Falle einer Upload-Antwort an die Serveranwendung an.</span><span class="sxs-lookup"><span data-stu-id="d9a10-120">When the BITS server receives the last fragment, it writes the file to its final destination and, in the case of an upload-reply, posts the file to the server application.</span></span> <span data-ttu-id="d9a10-121">Beim Upload-Reply-Fall bricht das Cancel-Session Paket den Antwort Teil eines Upload-Antwort-Auftrags ab.</span><span class="sxs-lookup"><span data-stu-id="d9a10-121">In the upload-reply case, the Cancel-Session packet cancels the reply portion of an upload-reply job.</span></span>

<span data-ttu-id="d9a10-122">Der BITS-Server gibt alle Ressourcen frei und löscht beim Empfang dieses Pakets alle temporären Dateien.</span><span class="sxs-lookup"><span data-stu-id="d9a10-122">The BITS server releases all resources and deletes all temporary files when it receives this packet.</span></span>

<span data-ttu-id="d9a10-123">Der BITS-Client sendet dieses Paket, wenn der Benutzer den Auftrag abbricht.</span><span class="sxs-lookup"><span data-stu-id="d9a10-123">The BITS client sends this packet when the user cancels the job.</span></span>

## <a name="see-also"></a><span data-ttu-id="d9a10-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d9a10-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9a10-125">**Bestätigung für Create-Session**</span><span class="sxs-lookup"><span data-stu-id="d9a10-125">**Ack for Create-Session**</span></span>](ack-for-create-session.md)
</dt> <dt>

[<span data-ttu-id="d9a10-126">**Sitzung schließen**</span><span class="sxs-lookup"><span data-stu-id="d9a10-126">**Close-Session**</span></span>](close-session.md)
</dt> </dl>

 

 




