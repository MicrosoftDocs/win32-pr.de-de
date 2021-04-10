---
title: Fragment
description: Verwenden Sie das Fragment-Paket, um ein Fragment der Uploaddatei an den Server zu senden.
ms.assetid: d6df7e47-a240-4be2-a9c4-24a13e622861
keywords:
- Fragmentbits
topic_type:
- apiref
api_name:
- Fragment
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f5103e90ec84a20ff4c04d9036a744919d9b1fd
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "104101282"
---
# <a name="fragment"></a><span data-ttu-id="aad3b-104">Fragment</span><span class="sxs-lookup"><span data-stu-id="aad3b-104">Fragment</span></span>

<span data-ttu-id="aad3b-105">Verwenden Sie das **Fragment** -Paket, um ein Fragment der Uploaddatei an den Server zu senden.</span><span class="sxs-lookup"><span data-stu-id="aad3b-105">Use the **Fragment** packet to send a fragment of the upload file to the server.</span></span>

``` syntax
BITS_POST remote-URL HTTP/1.1
BITS-Packet-Type: Fragment
BITS-Session-Id: {guid}
Content-Name: filename
Content-Length: length
Content-Range: Bytes range/total-length
Content-Encoding: encoding
```

## <a name="headers"></a><span data-ttu-id="aad3b-106">Header</span><span class="sxs-lookup"><span data-stu-id="aad3b-106">Headers</span></span>

<dl> <dt>

<span data-ttu-id="aad3b-107"><span id="BITS_POST"></span><span id="bits_post"></span>Bits- \_ Post</span><span class="sxs-lookup"><span data-stu-id="aad3b-107"><span id="BITS_POST"></span><span id="bits_post"></span>BITS\_POST</span></span>
</dt> <dd>

<span data-ttu-id="aad3b-108">Bits-spezifisches Verb, das dieses Paket für den BITS-Server identifiziert.</span><span class="sxs-lookup"><span data-stu-id="aad3b-108">BITS-specific verb that identifies this packet to the BITS server.</span></span>

<span data-ttu-id="aad3b-109">Ersetzen Sie Remote-URL durch den absoluten oder relativen URI.</span><span class="sxs-lookup"><span data-stu-id="aad3b-109">Replace remote-URL with the absolute or relative URI.</span></span> <span data-ttu-id="aad3b-110">Ersetzen Sie in der Regel Remote-URL durch den Remote Dateinamen des Auftrags.</span><span class="sxs-lookup"><span data-stu-id="aad3b-110">Typically, replace remote-URL with the remote file name of the job.</span></span> <span data-ttu-id="aad3b-111">Überlegungen zum Netzwerk Lastenausgleich finden Sie im "Bits-Host-ID"-Header im Paket " [**Create-Session**](create-session.md) ".</span><span class="sxs-lookup"><span data-stu-id="aad3b-111">For network load balancing considerations, see the BITS-Host-Id header in the [**Create-Session**](create-session.md) packet.</span></span>

</dd> <dt>

<span data-ttu-id="aad3b-112"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>Bits-Pakettyp</span><span class="sxs-lookup"><span data-stu-id="aad3b-112"><span id="BITS-Packet-Type"></span><span id="bits-packet-type"></span><span id="BITS-PACKET-TYPE"></span>BITS-Packet-Type</span></span>
</dt> <dd>

<span data-ttu-id="aad3b-113">Identifiziert dieses Anforderungspaket als fragmentpaket.</span><span class="sxs-lookup"><span data-stu-id="aad3b-113">Identifies this request packet as a Fragment packet.</span></span>

</dd> <dt>

<span data-ttu-id="aad3b-114"><span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>Bits-Session-ID</span><span class="sxs-lookup"><span data-stu-id="aad3b-114"><span id="BITS-Session-Id"></span><span id="bits-session-id"></span><span id="BITS-SESSION-ID"></span>BITS-Session-Id</span></span>
</dt> <dd>

<span data-ttu-id="aad3b-115">Zeichen folgen-GUID, die die Sitzung mit dem Server identifiziert.</span><span class="sxs-lookup"><span data-stu-id="aad3b-115">String GUID that identifies the session to the server.</span></span> <span data-ttu-id="aad3b-116">Ersetzen Sie {GUID} durch die Sitzungs-ID, die der Server in der Bestätigung für das Antwortpaket " [**Create-Session**](ack-for-create-session.md) " zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="aad3b-116">Replace {guid} with the session identifier that the server returns in the [**Ack for Create-Session**](ack-for-create-session.md) response packet.</span></span>

</dd> <dt>

<span data-ttu-id="aad3b-117"><span id="Content-Name"></span><span id="content-name"></span><span id="CONTENT-NAME"></span>Inhalts Name</span><span class="sxs-lookup"><span data-stu-id="aad3b-117"><span id="Content-Name"></span><span id="content-name"></span><span id="CONTENT-NAME"></span>Content-Name</span></span>
</dt> <dd>

<span data-ttu-id="aad3b-118">Geben Sie diesen Header nur mit dem anfänglichen Fragment an.</span><span class="sxs-lookup"><span data-stu-id="aad3b-118">Specify this header only with the initial fragment.</span></span> <span data-ttu-id="aad3b-119">Ersetzen Sie filename durch den Namen des lokalen Datei namens aus dem Auftrag.</span><span class="sxs-lookup"><span data-stu-id="aad3b-119">Replace filename with the name of the local file name from the job.</span></span> <span data-ttu-id="aad3b-120">Der Name enthält nicht den Pfad.</span><span class="sxs-lookup"><span data-stu-id="aad3b-120">The name does not include the path.</span></span>

</dd> <dt>

<span data-ttu-id="aad3b-121"><span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Inhalts Länge</span><span class="sxs-lookup"><span data-stu-id="aad3b-121"><span id="Content-Length"></span><span id="content-length"></span><span id="CONTENT-LENGTH"></span>Content-Length</span></span>
</dt> <dd>

<span data-ttu-id="aad3b-122">Ersetzen Sie die Länge durch die Anzahl von Bytes, die im Fragmenttext gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="aad3b-122">Replace length with the number of bytes sent in the fragment body.</span></span>

</dd> <dt>

<span data-ttu-id="aad3b-123"><span id="Content-Range"></span><span id="content-range"></span><span id="CONTENT-RANGE"></span>Inhalts Bereich</span><span class="sxs-lookup"><span data-stu-id="aad3b-123"><span id="Content-Range"></span><span id="content-range"></span><span id="CONTENT-RANGE"></span>Content-Range</span></span>
</dt> <dd>

<span data-ttu-id="aad3b-124">Weist den Server an, wo der Bereich in der Zieldatei angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="aad3b-124">Tells the server where to apply the range in the destination file.</span></span> <span data-ttu-id="aad3b-125">Ersetzen Sie Range durch die Start-und Endoffsets des Bereichs in der Zieldatei.</span><span class="sxs-lookup"><span data-stu-id="aad3b-125">Replace range with the start and end offsets of the range in the destination file.</span></span> <span data-ttu-id="aad3b-126">Die Offsets sind NULL basiert.</span><span class="sxs-lookup"><span data-stu-id="aad3b-126">The offsets are zero-based.</span></span> <span data-ttu-id="aad3b-127">Wenn der angegebene Bereich einen vorhandenen Bereich überlappt, schreibt Bits nur den nicht überlappenden Bereich des Bereichs. Vorhandene Inhalte werden von Bits nicht überschrieben.</span><span class="sxs-lookup"><span data-stu-id="aad3b-127">If the given range overlaps an existing range, BITS writes only the non-overlapping portion of the range; BITS does not overwrite existing content.</span></span> <span data-ttu-id="aad3b-128">Wenn das erste Paket z. b. den Bereich von 0 bis 100 enthielt und das zweite Paket den Bereich 50 bis 150 enthielt, schreibt Bits nur die Bytes 101 über 150 aus dem zweiten Paket.</span><span class="sxs-lookup"><span data-stu-id="aad3b-128">For example, if the first packet contained the range 0 through 100 and the second packet contained the range 50 through 150, BITS writes only bytes 101 through 150 from the second packet.</span></span> <span data-ttu-id="aad3b-129">Ersetzen Sie Total-Length durch die Gesamtzahl der Bytes in der Datei.</span><span class="sxs-lookup"><span data-stu-id="aad3b-129">Replace total-length with the total number of bytes in the file.</span></span>

</dd> <dt>

<span data-ttu-id="aad3b-130"><span id="Content-Encoding"></span><span id="content-encoding"></span><span id="CONTENT-ENCODING"></span>Inhalts Codierung</span><span class="sxs-lookup"><span data-stu-id="aad3b-130"><span id="Content-Encoding"></span><span id="content-encoding"></span><span id="CONTENT-ENCODING"></span>Content-Encoding</span></span>
</dt> <dd>

<span data-ttu-id="aad3b-131">Ersetzen Sie Encoding durch den Codierungstyp, den der Client für das Fragment verwendet.</span><span class="sxs-lookup"><span data-stu-id="aad3b-131">Replace encoding with the type of encoding the client uses on the fragment.</span></span> <span data-ttu-id="aad3b-132">Der Client muss die Codierung verwenden, die der Server im Accept-Encoding-Header der Bestätigung für das Antwortpaket [**Create-Session**](ack-for-create-session.md) identifiziert.</span><span class="sxs-lookup"><span data-stu-id="aad3b-132">The client must use the encoding that the server identifies in the Accept-Encoding header of the [**Ack for Create-Session**](ack-for-create-session.md) response packet.</span></span> <span data-ttu-id="aad3b-133">Der Server verwendet den Codierungstyp zum Decodieren des Fragments.</span><span class="sxs-lookup"><span data-stu-id="aad3b-133">The server uses the encoding type to decode the fragment.</span></span> <span data-ttu-id="aad3b-134">Alle Fragmente müssen dieselbe Codierung angeben.</span><span class="sxs-lookup"><span data-stu-id="aad3b-134">All fragments must specify the same encoding.</span></span>

<span data-ttu-id="aad3b-135">Senden Sie diesen Header nicht, wenn der Codierungstyp Identity ist.</span><span class="sxs-lookup"><span data-stu-id="aad3b-135">Do not send this header if the encoding type is Identity.</span></span> <span data-ttu-id="aad3b-136">Der BITS-Server unterstützt nur die Identitäts Codierung.</span><span class="sxs-lookup"><span data-stu-id="aad3b-136">The BITS server supports only Identity encoding.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="aad3b-137">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="aad3b-137">Remarks</span></span>

<span data-ttu-id="aad3b-138">Das Fragment ist ein Bereich von Bytes, die im Text des Pakets gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="aad3b-138">The fragment is a range of bytes sent in the body of the packet.</span></span> <span data-ttu-id="aad3b-139">Der Client sendet die Fragmente in sequenzieller Reihenfolge, beginnend mit Offset 0; der Server verfolgt nicht zusammenhängende Bereiche nach.</span><span class="sxs-lookup"><span data-stu-id="aad3b-139">The client sends the fragments in sequential order starting with offset zero; the server does not keep track of non-contiguous ranges.</span></span> <span data-ttu-id="aad3b-140">Wenn der Client nicht zusammenhängende Bereiche sendet, gibt der Server in der Bestätigung [**für die fragmentantwort**](ack-for-fragment.md) einen HTTP 416-Rückgabecode (Bereichs-nicht-satis-fähig) zurück.</span><span class="sxs-lookup"><span data-stu-id="aad3b-140">If the client sends non-contiguous ranges, the server returns an HTTP 416 (range-not-satisfiable) return code in the [**Ack for Fragment**](ack-for-fragment.md) response.</span></span>

<span data-ttu-id="aad3b-141">Die Content-*xxxx* -Header sind HTTP 1,1-Standard Header.</span><span class="sxs-lookup"><span data-stu-id="aad3b-141">The Content-*xxxx* headers are standard HTTP 1.1 headers.</span></span> <span data-ttu-id="aad3b-142">Weitere Informationen zu den Content-*xxxx* -Headern finden Sie in der Spezifikation von [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt) .</span><span class="sxs-lookup"><span data-stu-id="aad3b-142">For more details on the Content-*xxxx* headers, see the [RFC 2616](https://www.ietf.org/rfc/rfc2616.txt) specification.</span></span>

## <a name="see-also"></a><span data-ttu-id="aad3b-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aad3b-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aad3b-144">**Bestätigung für Fragment**</span><span class="sxs-lookup"><span data-stu-id="aad3b-144">**Ack for Fragment**</span></span>](ack-for-fragment.md)
</dt> <dt>

[<span data-ttu-id="aad3b-145">**Sitzung schließen**</span><span class="sxs-lookup"><span data-stu-id="aad3b-145">**Close-Session**</span></span>](close-session.md)
</dt> <dt>

[<span data-ttu-id="aad3b-146">**Create-Session**</span><span class="sxs-lookup"><span data-stu-id="aad3b-146">**Create-Session**</span></span>](create-session.md)
</dt> </dl>

 

 




