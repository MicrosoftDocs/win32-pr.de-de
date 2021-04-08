---
title: Close-Session
description: Verwenden Sie das Close-Session Paket, um dem BITS-Server mitzuteilen, dass der Datei Upload abgeschlossen ist, und um die Sitzung zu beenden.
ms.assetid: 9d4b658a-8b41-4678-b996-f2174784cdd6
keywords:
- Close-Session Bits
topic_type:
- apiref
api_name:
- Close-Session
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fe791ba4706689fd23dea8886f5b8f54f135841
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103857128"
---
# <a name="close-session"></a><span data-ttu-id="14c15-104">Close-Session</span><span class="sxs-lookup"><span data-stu-id="14c15-104">Close-Session</span></span>

<span data-ttu-id="14c15-105">Verwenden Sie das **Close-Session-** Paket, um dem BITS-Server mitzuteilen, dass der Datei Upload abgeschlossen ist, und um die Sitzung zu beenden.</span><span class="sxs-lookup"><span data-stu-id="14c15-105">Use the **Close-Session** packet to tell the BITS server that file upload is complete and to end the session.</span></span>

``` syntax
BITS_POST remote-URL HTTP/1.1
BITS-Packet-Type: Close-Session
BITS-Session-Id: {guid}
```

## <a name="headers"></a><span data-ttu-id="14c15-106">Header</span><span class="sxs-lookup"><span data-stu-id="14c15-106">Headers</span></span>

<dl> <dt>

<span data-ttu-id="14c15-107"><span id="BITS_POST"></span><span id="bits_post"></span>Bits- \_ Post</span><span class="sxs-lookup"><span data-stu-id="14c15-107"><span id="BITS_POST"></span><span id="bits_post"></span>BITS\_POST</span></span>
</dt> <dd>

<span data-ttu-id="14c15-108">Bits-spezifisches Verb, das dieses Paket für den BITS-Server identifiziert.</span><span class="sxs-lookup"><span data-stu-id="14c15-108">BITS-specific verb that identifies this packet to the BITS server.</span></span>

<span data-ttu-id="14c15-109">Ersetzen Sie Remote-URL durch den absoluten oder relativen URI.</span><span class="sxs-lookup"><span data-stu-id="14c15-109">Replace remote-URL with the absolute or relative URI.</span></span> <span data-ttu-id="14c15-110">Ersetzen Sie in der Regel Remote-URL durch den Remote Dateinamen des Auftrags.</span><span class="sxs-lookup"><span data-stu-id="14c15-110">Typically, replace remote-URL with the remote file name of the job.</span></span> <span data-ttu-id="14c15-111">Überlegungen zum Netzwerk Lastenausgleich finden Sie im "Bits-Host-ID"-Header im Paket " [**Create-Session**](create-session.md) ".</span><span class="sxs-lookup"><span data-stu-id="14c15-111">For network load balancing considerations, see the BITS-Host-Id header in the [**Create-Session**](create-session.md) packet.</span></span>

</dd> <dt>

<span data-ttu-id="14c15-112"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>Bits-Pakettyp</span><span class="sxs-lookup"><span data-stu-id="14c15-112"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type</span></span>
</dt> <dd>

<span data-ttu-id="14c15-113">Identifiziert dieses Anforderungspaket als Close-Session Paket.</span><span class="sxs-lookup"><span data-stu-id="14c15-113">Identifies this request packet as a Close-Session packet.</span></span>

</dd> <dt>

<span data-ttu-id="14c15-114"><span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>Bits-Session-ID</span><span class="sxs-lookup"><span data-stu-id="14c15-114"><span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BITS-Session-Id</span></span>
</dt> <dd>

<span data-ttu-id="14c15-115">Zeichen folgen-GUID, die die Sitzung mit dem Server identifiziert.</span><span class="sxs-lookup"><span data-stu-id="14c15-115">String GUID that identifies the session to the server.</span></span> <span data-ttu-id="14c15-116">Ersetzen Sie {GUID} durch die Sitzungs-ID, die der Server in der Bestätigung für das Antwortpaket " [**Create-Session**](ack-for-create-session.md) " zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="14c15-116">Replace {guid} with the session identifier that the server returns in the [**Ack for Create-Session**](ack-for-create-session.md) response packet.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="14c15-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="14c15-117">Remarks</span></span>

<span data-ttu-id="14c15-118">Der BITS-Server gibt alle Ressourcen frei und löscht beim Empfang dieses Pakets alle temporären Dateien.</span><span class="sxs-lookup"><span data-stu-id="14c15-118">The BITS server releases all resources and deletes all temporary files when it receives this packet.</span></span>

<span data-ttu-id="14c15-119">Für Upload-Antwort-Aufträge müssen Sie die Antwort vor dem Senden der **Close-Session** herunterladen.</span><span class="sxs-lookup"><span data-stu-id="14c15-119">For upload-reply jobs, you must download the reply before sending **Close-Session**.</span></span> <span data-ttu-id="14c15-120">Andernfalls geht die Antwort verloren.</span><span class="sxs-lookup"><span data-stu-id="14c15-120">Otherwise, the reply is lost.</span></span>

<span data-ttu-id="14c15-121">Wenn Sie dieses Paket vor dem Hochladen aller Fragmente senden, wird die Uploaddatei gelöscht. eine partielle Datei kann nicht hochgeladen werden.</span><span class="sxs-lookup"><span data-stu-id="14c15-121">If you send this packet before uploading all fragments, the upload file is deleted; you cannot upload a partial file.</span></span>

## <a name="see-also"></a><span data-ttu-id="14c15-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="14c15-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14c15-123">**Bestätigung für Close-Session**</span><span class="sxs-lookup"><span data-stu-id="14c15-123">**Ack for Close-Session**</span></span>](ack-for-close-session.md)
</dt> <dt>

[<span data-ttu-id="14c15-124">**Abbrechen-Sitzung**</span><span class="sxs-lookup"><span data-stu-id="14c15-124">**Cancel-Session**</span></span>](cancel-session.md)
</dt> <dt>

[<span data-ttu-id="14c15-125">**Create-Session**</span><span class="sxs-lookup"><span data-stu-id="14c15-125">**Create-Session**</span></span>](create-session.md)
</dt> </dl>

 

 




