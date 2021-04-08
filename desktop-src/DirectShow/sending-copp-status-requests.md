---
description: Senden von COPP-Status Anforderungen
ms.assetid: 9f9950ff-469f-4cea-924e-3f9471eb4838
title: Senden von COPP-Status Anforderungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e5494b0e856df573bdbfc9b1554ab82be206a95
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745416"
---
# <a name="sending-copp-status-requests"></a><span data-ttu-id="4e7c9-103">Senden von COPP-Status Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4e7c9-103">Sending COPP Status Requests</span></span>

<span data-ttu-id="4e7c9-104">Um eine zertifizierte COPP-Status Anforderung (Output Protection Protocol) zu senden, geben Sie eine [**amcoppstatusinput**](/windows/win32/api/strmif/ns-strmif-amcoppstatusinput) -Struktur mit den Anforderungs Daten ein.</span><span class="sxs-lookup"><span data-stu-id="4e7c9-104">To send a Certified Output Protection Protocol (COPP) status request, fill in an [**AMCOPPStatusInput**](/windows/win32/api/strmif/ns-strmif-amcoppstatusinput) structure with the request data.</span></span> <span data-ttu-id="4e7c9-105">Die Strukturmember lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="4e7c9-105">The structure members are:</span></span>

-   <span data-ttu-id="4e7c9-106">**rApp**.</span><span class="sxs-lookup"><span data-stu-id="4e7c9-106">**rApp**.</span></span> <span data-ttu-id="4e7c9-107">Eine 128-Bit-Zufallszahl, die als GUID typisiert ist.</span><span class="sxs-lookup"><span data-stu-id="4e7c9-107">A 128-bit random number, typed as a GUID.</span></span> <span data-ttu-id="4e7c9-108">Die gleiche Zahl wird in der Antwort des Treibers zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="4e7c9-108">The same number is returned in the driver's response.</span></span> <span data-ttu-id="4e7c9-109">Sie sollten die Zufallszahl auf dem Heap zuordnen und Sie dann in die Struktur kopieren.</span><span class="sxs-lookup"><span data-stu-id="4e7c9-109">You should allocate the random number on the heap and then copy it into structure.</span></span> <span data-ttu-id="4e7c9-110">Dies schützt gegen Angriffe, bei denen der Angreifer den Inhalt der [**amcoppstatusinput**](/windows/win32/api/strmif/ns-strmif-amcoppstatusinput) -Struktur ändert.</span><span class="sxs-lookup"><span data-stu-id="4e7c9-110">This guards against attacks where the attacker modifies the contents of the [**AMCOPPStatusInput**](/windows/win32/api/strmif/ns-strmif-amcoppstatusinput) structure.</span></span>
-   <span data-ttu-id="4e7c9-111">**guidstatuus RequestId**.</span><span class="sxs-lookup"><span data-stu-id="4e7c9-111">**guidStatusRequestID**.</span></span> <span data-ttu-id="4e7c9-112">Eine GUID, die die Anforderung identifiziert.</span><span class="sxs-lookup"><span data-stu-id="4e7c9-112">A GUID that identifies the request.</span></span> <span data-ttu-id="4e7c9-113">Siehe [COPP-Abfrage Verweis](copp-query-reference.md).</span><span class="sxs-lookup"><span data-stu-id="4e7c9-113">See [COPP Query Reference](copp-query-reference.md).</span></span>
-   <span data-ttu-id="4e7c9-114">**dwsequence**.</span><span class="sxs-lookup"><span data-stu-id="4e7c9-114">**dwSequence**.</span></span> <span data-ttu-id="4e7c9-115">Die Status Sequenznummer.</span><span class="sxs-lookup"><span data-stu-id="4e7c9-115">The status sequence number.</span></span> <span data-ttu-id="4e7c9-116">Erhöhen Sie diesen Wert nach jeder Status Anforderung.</span><span class="sxs-lookup"><span data-stu-id="4e7c9-116">Increment this value after each status request.</span></span> <span data-ttu-id="4e7c9-117">(Im Abschnitt [Initiieren einer COPP-Sitzung](initiating-a-copp-session.md)wird dieser Wert in den Codebeispielen als *ustatus-SEQ* angezeigt.)</span><span class="sxs-lookup"><span data-stu-id="4e7c9-117">(In the section [Initiating a COPP Session](initiating-a-copp-session.md), this value is shown as *uStatusSeq* in the code examples.)</span></span>
-   <span data-ttu-id="4e7c9-118">**cbsizedata**.</span><span class="sxs-lookup"><span data-stu-id="4e7c9-118">**cbSizeData**.</span></span> <span data-ttu-id="4e7c9-119">Die Größe (in Bytes) aller zusätzlichen Daten, die für die Anforderung benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="4e7c9-119">The size, in bytes, of any additional data needed for the request.</span></span>
-   <span data-ttu-id="4e7c9-120">**Statusdaten**.</span><span class="sxs-lookup"><span data-stu-id="4e7c9-120">**StatusData**.</span></span> <span data-ttu-id="4e7c9-121">Daten für die Status Anforderung.</span><span class="sxs-lookup"><span data-stu-id="4e7c9-121">Data for the status request.</span></span>

<span data-ttu-id="4e7c9-122">Übergeben Sie die [**amcoppstatusinput**](/windows/win32/api/strmif/ns-strmif-amcoppstatusinput) -Struktur an die [**iamcertifiedoutputprotection::P rotectionstatus**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-protectionstatus) -Methode.</span><span class="sxs-lookup"><span data-stu-id="4e7c9-122">Pass the [**AMCOPPStatusInput**](/windows/win32/api/strmif/ns-strmif-amcoppstatusinput) structure to the [**IAMCertifiedOutputProtection::ProtectionStatus**](/windows/desktop/api/Strmif/nf-strmif-iamcertifiedoutputprotection-protectionstatus) method.</span></span> <span data-ttu-id="4e7c9-123">Der folgende Code sendet z. b. eine Status Anforderung, mit der abgefragt wird, welche Schutzmechanismen verfügbar sind:</span><span class="sxs-lookup"><span data-stu-id="4e7c9-123">For example, the following code sends a status request that queries which protection mechanisms are available:</span></span>


```C++
AMCOPPStatusInput input;
AMCOPPStatusOutput output;

// Create a 128-bit random number.
GUID *pGuid = new GUID();
if (pGuid == NULL)
{
    // Handle out-of-memory condition.
}
CryptGenRandom(hCSP, sizeof(GUID), (BYTE*)pGuid);  

// Copy the random number into the command structure.
memcpy(&input.rApp, pGuid, sizeof(GUID));

// Fill in the other data.
input.guidStatusRequestID = DXVA_COPPQueryProtectionType; // Request type.
input.dwSequence = uStatusSeq;  // Status sequence number.
input.cbSizeData = 0            // No other data for this query.

// Send the request.
hr = pCOPP->ProtectionStatus(&input, &output);

// Increment the sequence number each time.
++uStatusSeq;
```



<span data-ttu-id="4e7c9-124">Die Antwort wird in den Member " **coppstatus** " der [**amcoppstatusoutput**](/windows/win32/api/strmif/ns-strmif-amcoppstatusoutput) -Struktur geschrieben.</span><span class="sxs-lookup"><span data-stu-id="4e7c9-124">The response is written into the **COPPStatus** member of the [**AMCOPPStatusOutput**](/windows/win32/api/strmif/ns-strmif-amcoppstatusoutput) structure.</span></span> <span data-ttu-id="4e7c9-125">Die Größe der gültigen Daten in der Antwort wird im **cbsizedata** -Member angegeben.</span><span class="sxs-lookup"><span data-stu-id="4e7c9-125">The size of the valid data in the response is given in the **cbSizeData** member.</span></span> <span data-ttu-id="4e7c9-126">Um die Integrität der Nachricht sicherzustellen, berechnet der Treiber einen Mac (Message Authentication Code) mithilfe des OMAC 1-Algorithmus und gibt diesen Wert im **mackdi** -Member der Struktur zurück.</span><span class="sxs-lookup"><span data-stu-id="4e7c9-126">To ensure the integrity of the message, the driver computes a message authentication code (MAC) using the OMAC 1 algorithm, and returns this value in the structure's **macKDI** member.</span></span> <span data-ttu-id="4e7c9-127">Die Anwendung sollte diesen Wert wie folgt überprüfen:</span><span class="sxs-lookup"><span data-stu-id="4e7c9-127">The application should verify this value as follows:</span></span>

1.  <span data-ttu-id="4e7c9-128">Berechnen Sie das OMAC-Tag für den Datenblock, der nach dem **mackdi** -Member der [**amcoppstatusoutput**](/windows/win32/api/strmif/ns-strmif-amcoppstatusoutput) -Struktur angezeigt wird (also **cbsizedata** Plus **coppstatus**).</span><span class="sxs-lookup"><span data-stu-id="4e7c9-128">Calculate the OMAC tag for the block of data that appears after the **macKDI** member of the [**AMCOPPStatusOutput**](/windows/win32/api/strmif/ns-strmif-amcoppstatusoutput) structure (in other words, **cbSizeData** plus **COPPStatus**).</span></span>
2.  <span data-ttu-id="4e7c9-129">Vergleichen Sie dieses Tag mit dem Wert in **mackdi** mithilfe eines geraden **memcmp**.</span><span class="sxs-lookup"><span data-stu-id="4e7c9-129">Compare this tag with the value in **macKDI**, using a straight **memcmp**.</span></span>

<span data-ttu-id="4e7c9-130">Der OMAC 1-Algorithmus wird ausführlich unter beschrieben [https://www.nuee.nagoya-u.ac.jp/labs/tiwata/omac/omac.html](https://www.nuee.nagoya-u.ac.jp/labs/tiwata/omac/omac.html) .</span><span class="sxs-lookup"><span data-stu-id="4e7c9-130">The OMAC 1 algorithm is described in detail at [https://www.nuee.nagoya-u.ac.jp/labs/tiwata/omac/omac.html](https://www.nuee.nagoya-u.ac.jp/labs/tiwata/omac/omac.html).</span></span> <span data-ttu-id="4e7c9-131">COPP verwendet die folgenden OMAC-1-Parameter:</span><span class="sxs-lookup"><span data-stu-id="4e7c9-131">COPP uses the following OMAC-1 parameters:</span></span>

-   <span data-ttu-id="4e7c9-132">E = AES</span><span class="sxs-lookup"><span data-stu-id="4e7c9-132">E = AES</span></span>
-   <span data-ttu-id="4e7c9-133">t = 128 Bits</span><span class="sxs-lookup"><span data-stu-id="4e7c9-133">t = 128 bits</span></span>

<span data-ttu-id="4e7c9-134">Die von der Status Anforderung zurückgegebenen Daten beginnen immer mit zwei Elementen:</span><span class="sxs-lookup"><span data-stu-id="4e7c9-134">The data returned from the status request always starts with two items:</span></span>

-   <span data-ttu-id="4e7c9-135">Der gleiche Wert von **rApp** , der von der Anwendung übermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="4e7c9-135">The same value of **rApp** that was passed by the application.</span></span> <span data-ttu-id="4e7c9-136">Überprüfen Sie, ob dieser Wert mit dem auf dem Heap gespeicherten ursprünglichen Wert übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="4e7c9-136">You should verify that this value matches the original value stored on the heap.</span></span>
-   <span data-ttu-id="4e7c9-137">Ein [**COPP \_ Statusflags**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_statusflags) -Wert, der angibt, ob sich der Status des Ausgabe Schutzes geändert hat.</span><span class="sxs-lookup"><span data-stu-id="4e7c9-137">A [**COPP\_StatusFlags**](/windows/desktop/api/dxva9typ/ne-dxva9typ-copp_statusflags) value that indicates whether the output protection status has changed.</span></span>

<span data-ttu-id="4e7c9-138">Da die Verbindung verloren gehen oder neu konfiguriert werden kann, sollte die Anwendung den Treiber regelmäßig auf den aktuellen Statusabfragen.</span><span class="sxs-lookup"><span data-stu-id="4e7c9-138">Because the connection can be lost or reconfigured, the application should periodically poll the driver for the current status.</span></span> <span data-ttu-id="4e7c9-139">Wenn das COPP-Flag für die erneute Aushandlung \_ erforderlich ist, sollte die Anwendung versuchen, die Schutz Ebene zurückzusetzen.</span><span class="sxs-lookup"><span data-stu-id="4e7c9-139">If the COPP\_RenegotiationRequired flag is set, the application should attempt to reset the protection level.</span></span> <span data-ttu-id="4e7c9-140">Wenn das COPP \_ linklost-Flag festgelegt ist, sollte die Anwendung die Wiedergabe des Inhalts abbrechen.</span><span class="sxs-lookup"><span data-stu-id="4e7c9-140">If the COPP\_LinkLost flag is set, the application should stop playing the content.</span></span> <span data-ttu-id="4e7c9-141">Beispielsweise kann das COPP \_ linklost-Flag zurückgegeben werden, weil der Benutzer den ausgabeconnector getrennt hat.</span><span class="sxs-lookup"><span data-stu-id="4e7c9-141">For example, the COPP\_LinkLost flag can be returned because the user disconnected the output connector.</span></span> <span data-ttu-id="4e7c9-142">Die Anwendung sollte die aktuelle Instanz von VMR freigeben, eine neue Instanz von VMR erstellen und eine neue COPP-Sitzung einrichten (einschließlich Schlüsselaustausch und Zertifikat Überprüfung).</span><span class="sxs-lookup"><span data-stu-id="4e7c9-142">The application should release the current instance of the VMR, create a new instance of the VMR, and establish a new COPP session (including key exchange and certificate validation).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4e7c9-143">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4e7c9-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4e7c9-144">Verwenden des Certified Output Protection-Protokolls (COPP)</span><span class="sxs-lookup"><span data-stu-id="4e7c9-144">Using Certified Output Protection Protocol (COPP)</span></span>](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



