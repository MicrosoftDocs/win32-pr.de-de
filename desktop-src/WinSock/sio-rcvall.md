---
description: Mithilfe von Steuerungs Code kann ein Socket alle IPv4-oder IPv6-Pakete empfangen, die über eine Netzwerkschnittstelle übergeben werden.
ms.assetid: 1c198a70-6669-4599-bd9a-ffc26c9fe1d0
title: SIO_RCVALL Steuerungs Codes
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: ddff631f1fa4b6b9f9af74f71e2b1eb38a2bf48e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343676"
---
# <a name="sio_rcvall-control-code"></a><span data-ttu-id="29d8e-103">SIO_RCVALL Steuerungs Codes</span><span class="sxs-lookup"><span data-stu-id="29d8e-103">SIO_RCVALL Control Code</span></span>

## <a name="description"></a><span data-ttu-id="29d8e-104">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="29d8e-104">Description</span></span>
<span data-ttu-id="29d8e-105">Der " **SIO \_ rcvall** "-Steuerungs Code ermöglicht einem Socket, alle IPv4-oder IPv6-Pakete zu empfangen, die über eine Netzwerkschnittstelle übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="29d8e-105">The **SIO\_RCVALL** control code enables a socket to receive all IPv4 or IPv6 packets passing through a network interface.</span></span>

<span data-ttu-id="29d8e-106">Um diesen Vorgang auszuführen, wenden Sie die [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) -oder **wspioctl** -Funktion mit den folgenden Parametern an.</span><span class="sxs-lookup"><span data-stu-id="29d8e-106">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,            // descriptor identifying a socket
  SIO_RCV_ALL,                       // dwIoControlCode
  NULL,                              // lpvInBuffer0,                                 // cbInBuffer
  NULL,                              // lpvOutBuffer output buffer
  (DWORD) cbOutBuffer,            // size of output buffer  
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped, // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSAIoctl(
  (socket) s,            // descriptor identifying a socket
  SIO_RCV_ALL,                       // dwIoControlCode
  NULL,                              // lpvInBuffer
  0,                                 // cbInBuffer
  NULL,                              // lpvOutBuffer output buffer
  (DWORD) cbOutBuffer,            // size of output buffer  
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped, // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

## <a name="parameters"></a><span data-ttu-id="29d8e-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="29d8e-107">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="29d8e-108">s</span><span class="sxs-lookup"><span data-stu-id="29d8e-108">s</span></span>

<span data-ttu-id="29d8e-109">Ein Deskriptor, der einen Socket identifiziert.</span><span class="sxs-lookup"><span data-stu-id="29d8e-109">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="29d8e-110">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="29d8e-110">dwIoControlCode</span></span>

<span data-ttu-id="29d8e-111">Der Steuerelement Code für den Vorgang.</span><span class="sxs-lookup"><span data-stu-id="29d8e-111">The control code for the operation.</span></span>
<span data-ttu-id="29d8e-112">Verwenden Sie für diesen Vorgang " **SIO \_ rcvall** ".</span><span class="sxs-lookup"><span data-stu-id="29d8e-112">Use **SIO\_RCVALL** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="29d8e-113">lpvinbuffer</span><span class="sxs-lookup"><span data-stu-id="29d8e-113">lpvInBuffer</span></span>

<span data-ttu-id="29d8e-114">Ein Zeiger auf den Eingabepuffer, der den Optionswert enthalten soll.</span><span class="sxs-lookup"><span data-stu-id="29d8e-114">A pointer to the input buffer that should contain the option value.</span></span>
<span data-ttu-id="29d8e-115">Die möglichen Werte für die Option " **SIO \_ rcvall** ioctl" werden in der **RCVALL_VALUE** Enumeration angegeben, die in der Header Datei " *MSTCPIP. h* " definiert ist.</span><span class="sxs-lookup"><span data-stu-id="29d8e-115">The possible values for the **SIO\_RCVALL** IOCTL option are specified in the **RCVALL_VALUE** enumeration defined in the *Mstcpip.h* header file.</span></span>

<span data-ttu-id="29d8e-116">Die möglichen Werte für " **SIO \_ rcvall** " lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="29d8e-116">The possible values for **SIO\_RCVALL** are as follows:</span></span>

| <span data-ttu-id="29d8e-117">Wert</span><span class="sxs-lookup"><span data-stu-id="29d8e-117">Value</span></span> | <span data-ttu-id="29d8e-118">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="29d8e-118">Meaning</span></span> |
|-------|---------|
| <span data-ttu-id="29d8e-119">**rcvall \_ aus**</span><span class="sxs-lookup"><span data-stu-id="29d8e-119">**RCVALL\_OFF**</span></span> | <span data-ttu-id="29d8e-120">Deaktivieren Sie diese Option, damit ein Socket nicht alle IPv4-oder IPv6-Pakete empfängt, die über eine Netzwerkschnittstelle übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="29d8e-120">Disable this option so a socket does not receive all IPv4 or IPv6 packets passing through a network interface.</span></span> |
| <span data-ttu-id="29d8e-121">**rcvall \_ on**</span><span class="sxs-lookup"><span data-stu-id="29d8e-121">**RCVALL\_ON**</span></span> | <span data-ttu-id="29d8e-122">Aktivieren Sie diese Option, damit ein Socket alle IPv4-oder IPv6-Pakete empfängt, die über eine Netzwerkschnittstelle übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="29d8e-122">Enable this option so a socket receives all IPv4 or IPv6 packets passing through a network interface.</span></span> <span data-ttu-id="29d8e-123">Diese Option aktiviert den gemischten-Modus auf der Netzwerkschnittstellenkarte (NIC), wenn die NIC den gemischten-Modus unterstützt.</span><span class="sxs-lookup"><span data-stu-id="29d8e-123">This option enables promiscuous mode on the network interface card (NIC), if the NIC supports promiscuous mode.</span></span> <span data-ttu-id="29d8e-124">In einem LAN-Segment mit einem Netzwerkhub erfasst eine NIC, die den gemischten-Modus unterstützt, den gesamten IPv4-oder IPv6-Datenverkehr im LAN, einschließlich des Datenverkehrs zwischen anderen Computern desselben LAN-Segments.</span><span class="sxs-lookup"><span data-stu-id="29d8e-124">On a LAN segment with a network hub, a NIC that supports promiscuous mode will capture all IPv4 or IPv6 traffic on the LAN, including traffic between other computers on the same LAN segment.</span></span> <span data-ttu-id="29d8e-125">Alle aufgezeichneten Pakete (IPv4 oder IPv6, abhängig vom Socket) werden an den Rohdaten Socket übermittelt.</span><span class="sxs-lookup"><span data-stu-id="29d8e-125">All of the captured packets (IPv4 or IPv6, depending on the socket) will be delivered to the raw socket.</span></span> <span data-ttu-id="29d8e-126">Mit dieser Option werden nicht andere Pakete (z. b. ARP-, IPX-und NetBEUI-Pakete) auf der-Schnittstelle erfasst.</span><span class="sxs-lookup"><span data-stu-id="29d8e-126">This option will not capture other packets (ARP, IPX, and NetBEUI packets, for example) on the interface.</span></span> <span data-ttu-id="29d8e-127">NetMon verwendet den gleichen Modus für die Netzwerkschnittstelle, verwendet diese Option jedoch nicht zum Erfassen von Datenverkehr.</span><span class="sxs-lookup"><span data-stu-id="29d8e-127">Netmon uses the same mode for the network interface, but does not use this option to capture traffic.</span></span> |
| <span data-ttu-id="29d8e-128">**rcvall \_ socketlevelonly**</span><span class="sxs-lookup"><span data-stu-id="29d8e-128">**RCVALL\_SOCKETLEVELONLY**</span></span> | <span data-ttu-id="29d8e-129">Diese Funktion ist zurzeit nicht implementiert, sodass das Festlegen dieser Option keine Auswirkung hat.</span><span class="sxs-lookup"><span data-stu-id="29d8e-129">This feature is not currently implemented, so setting this option does not have any affect.</span></span> |
| <span data-ttu-id="29d8e-130">**rcvall \_ iplevel**</span><span class="sxs-lookup"><span data-stu-id="29d8e-130">**RCVALL\_IPLEVEL**</span></span> | <span data-ttu-id="29d8e-131">Aktivieren Sie diese Option, damit ein IPv4-oder IPv6-Socket alle Pakete auf IP-Ebene empfängt, die über eine Netzwerkschnittstelle übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="29d8e-131">Enable this option so an IPv4 or IPv6 socket receives all packets at the IP level passing through a network interface.</span></span> <span data-ttu-id="29d8e-132">Diese Option aktiviert nicht den gemischten-Modus auf der Netzwerkschnittstellenkarte.</span><span class="sxs-lookup"><span data-stu-id="29d8e-132">This option does not enable promiscuous mode on the network interface card.</span></span> <span data-ttu-id="29d8e-133">Diese Option wirkt sich nur auf die Paketverarbeitung auf IP-Ebene aus.</span><span class="sxs-lookup"><span data-stu-id="29d8e-133">This option only affects packet processing at the IP level.</span></span> <span data-ttu-id="29d8e-134">Die NIC empfängt weiterhin nur Pakete, die an die konfigurierten Unicast-und Multicast Adressen weitergeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="29d8e-134">The NIC still receives only packets directed to its configured unicast and multicast addresses.</span></span> <span data-ttu-id="29d8e-135">Ein Socket, für den diese Option aktiviert ist, empfängt jedoch nicht nur Pakete, die an bestimmte IP-Adressen weitergeleitet werden, sondern empfängt alle IPv4-oder IPv6-Pakete, die die NIC empfängt.</span><span class="sxs-lookup"><span data-stu-id="29d8e-135">However, a socket with this option enabled will receive not only packets directed to specific IP addresses, but will receive all the IPv4 or IPv6 packets the NIC receives.</span></span> <span data-ttu-id="29d8e-136">Mit dieser Option werden keine anderen Pakete (z. b. ARP-, IPX-und NetBEUI-Pakete) erfasst, die über die Schnittstelle empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="29d8e-136">This option will not capture other packets (ARP, IPX, and NetBEUI packets, for example) received on the interface.</span></span> |

### <a name="cbinbuffer"></a><span data-ttu-id="29d8e-137">cbinbuffer</span><span class="sxs-lookup"><span data-stu-id="29d8e-137">cbInBuffer</span></span>

<span data-ttu-id="29d8e-138">Die Größe des Eingabe Puffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="29d8e-138">The size, in bytes, of the input buffer.</span></span>
<span data-ttu-id="29d8e-139">Dieser Parameter muss größer oder gleich der Größe des **RCVALL_VALUE** Enumerationswerts sein, auf den der *lpvinbuffer* -Parameter verweist.</span><span class="sxs-lookup"><span data-stu-id="29d8e-139">This parameter should be equal to or greater than the size of the **RCVALL_VALUE** enumeration value pointed to by the *lpvInBuffer* parameter.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="29d8e-140">lpvoutbuffer</span><span class="sxs-lookup"><span data-stu-id="29d8e-140">lpvOutBuffer</span></span>

<span data-ttu-id="29d8e-141">Ein Zeiger auf den Ausgabepuffer.</span><span class="sxs-lookup"><span data-stu-id="29d8e-141">A pointer to the output buffer.</span></span>
<span data-ttu-id="29d8e-142">Dieser Parameter wird für diesen Vorgang nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="29d8e-142">This parameter is unused for this operation.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="29d8e-143">cboutbuffer</span><span class="sxs-lookup"><span data-stu-id="29d8e-143">cbOutBuffer</span></span>

<span data-ttu-id="29d8e-144">Die Größe des Ausgabepuffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="29d8e-144">The size, in bytes, of the output buffer.</span></span>
<span data-ttu-id="29d8e-145">Dieser Parameter wird für diesen Vorgang nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="29d8e-145">This parameter is unused for this operation.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="29d8e-146">lpcbbyteszurück gegeben</span><span class="sxs-lookup"><span data-stu-id="29d8e-146">lpcbBytesReturned</span></span>

<span data-ttu-id="29d8e-147">Ein Zeiger auf eine Variable, die die Größe der im Ausgabepuffer gespeicherten Daten (in Bytes) empfängt.</span><span class="sxs-lookup"><span data-stu-id="29d8e-147">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>
<span data-ttu-id="29d8e-148">Dieser Parameter wird für diesen Vorgang nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="29d8e-148">This parameter is unused for this operation.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="29d8e-149">lpvoverlgetauscht</span><span class="sxs-lookup"><span data-stu-id="29d8e-149">lpvOverlapped</span></span>

<span data-ttu-id="29d8e-150">Ein Zeiger auf eine [**wsaoverllapp**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="29d8e-150">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="29d8e-151">Wenn Socket *s* ohne das überlappende Attribut erstellt wurde, wird der *lpoverllapp* -Parameter ignoriert.</span><span class="sxs-lookup"><span data-stu-id="29d8e-151">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="29d8e-152">Wenn *s* mit dem überlappenden Attribut geöffnet wurde und der *lpoverlgetauscht* -Parameter nicht **null** ist, wird der Vorgang als überlappende (asynchrone) Operation ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="29d8e-152">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="29d8e-153">In diesem Fall muss der *lpoverllapp* -Parameter auf eine gültige [**wsaoverllapp**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) -Struktur zeigen.</span><span class="sxs-lookup"><span data-stu-id="29d8e-153">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="29d8e-154">Bei überlappenden Vorgängen gibt die Funktion [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) oder **wspioctl** sofort zurück, und die entsprechende Vervollständigungs Methode wird signalisiert, wenn der Vorgang abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="29d8e-154">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="29d8e-155">Andernfalls gibt die Funktion nicht zurück, bis der Vorgang abgeschlossen ist oder ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="29d8e-155">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="29d8e-156">lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="29d8e-156">lpCompletionRoutine</span></span>

<span data-ttu-id="29d8e-157">Typ: \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="29d8e-157">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="29d8e-158">Ein Zeiger auf die Vervollständigungs Routine, die aufgerufen wird, wenn der Vorgang abgeschlossen wurde (bei nicht überlappenden Sockets ignoriert).</span><span class="sxs-lookup"><span data-stu-id="29d8e-158">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="29d8e-159">lpthreadid</span><span class="sxs-lookup"><span data-stu-id="29d8e-159">lpThreadId</span></span>

<span data-ttu-id="29d8e-160">Ein Zeiger auf eine [**wsathreadid**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) -Struktur, die vom Anbieter in einem nachfolgenden [**wpuqueueapc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc)-Rückruf verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="29d8e-160">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="29d8e-161">Der Anbieter sollte die referenzierte [**wsathreadid**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) -Struktur (nicht den Zeiger auf dieselbe) speichern, bis die [**wpuqueueapc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) -Funktion zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="29d8e-161">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="29d8e-162">**Hinweis**  Dieser Parameter gilt nur für die **wspioctl** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="29d8e-162">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="29d8e-163">lperrno</span><span class="sxs-lookup"><span data-stu-id="29d8e-163">lpErrno</span></span>

<span data-ttu-id="29d8e-164">Ein Zeiger auf den Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="29d8e-164">A pointer to the error code.</span></span>

<span data-ttu-id="29d8e-165">**Hinweis**  Dieser Parameter gilt nur für die **wspioctl** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="29d8e-165">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="29d8e-166">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="29d8e-166">Return value</span></span>

<span data-ttu-id="29d8e-167">Wenn der Vorgang erfolgreich abgeschlossen wird, gibt die [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) -oder **wspioctl** -Funktion NULL zurück.</span><span class="sxs-lookup"><span data-stu-id="29d8e-167">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="29d8e-168">Wenn der Vorgang fehlschlägt oder aussteht, gibt die Funktion [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) oder **wspioctl** einen **\_ Socketfehler** zurück.</span><span class="sxs-lookup"><span data-stu-id="29d8e-168">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="29d8e-169">Um erweiterte Fehlerinformationen abzurufen, nennen Sie [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="29d8e-169">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="29d8e-170">Fehlercode</span><span class="sxs-lookup"><span data-stu-id="29d8e-170">Error code</span></span> | <span data-ttu-id="29d8e-171">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="29d8e-171">Meaning</span></span> |
|------------|---------|
| <span data-ttu-id="29d8e-172">**ausstehende WSA-e/a \_ \_**</span><span class="sxs-lookup"><span data-stu-id="29d8e-172">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="29d8e-173">Ein übergebener Vorgang wurde erfolgreich initiiert, und der Abschluss wird zu einem späteren Zeitpunkt angegeben.</span><span class="sxs-lookup"><span data-stu-id="29d8e-173">An overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="29d8e-174">**WSA- \_ Vorgang \_ abgebrochen**</span><span class="sxs-lookup"><span data-stu-id="29d8e-174">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="29d8e-175">Ein über Lapp ender Vorgang wurde aufgrund der Schließung des Sockets oder der Ausführung des **SIO_FLUSH** ioctl-Befehls abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="29d8e-175">An overlapped operation was canceled due to the closure of the socket or the execution of the **SIO_FLUSH** IOCTL command.</span></span> |
| <span data-ttu-id="29d8e-176">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="29d8e-176">**WSAEFAULT**</span></span> | <span data-ttu-id="29d8e-177">Der *lpoverllapp* -oder *lpCompletionRoutine* -Parameter ist nicht vollständig in einem gültigen Teil des Benutzer Adressraums enthalten.</span><span class="sxs-lookup"><span data-stu-id="29d8e-177">The *lpOverlapped* or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="29d8e-178">**Wsaeingabe Progress**</span><span class="sxs-lookup"><span data-stu-id="29d8e-178">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="29d8e-179">Die-Funktion wird aufgerufen, wenn ein Rückruf ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="29d8e-179">The function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="29d8e-180">**Wsaeingabe**</span><span class="sxs-lookup"><span data-stu-id="29d8e-180">**WSAEINTR**</span></span> | <span data-ttu-id="29d8e-181">Ein Blockierungs Vorgang wurde unterbrochen.</span><span class="sxs-lookup"><span data-stu-id="29d8e-181">A blocking operation was interrupted.</span></span> |
| <span data-ttu-id="29d8e-182">**Wsaabval**</span><span class="sxs-lookup"><span data-stu-id="29d8e-182">**WSAEINVAL**</span></span> | <span data-ttu-id="29d8e-183">Der *dwIoControlCode* -Parameter ist kein gültiger Befehl, oder ein angegebener Eingabeparameter ist nicht zulässig, oder der Befehl ist nicht auf den angegebenen Sockettyp anwendbar.</span><span class="sxs-lookup"><span data-stu-id="29d8e-183">The *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> <span data-ttu-id="29d8e-184">Dieser Fehler wird auch zurückgegeben, wenn der *cbinbuffer* -Parameter kleiner als `sizeof(UCHAR)` oder der *lpvinbuffer* -Parameter auf einen Wert verweist, der kein **RCVALL_VALUE** Enumerationswert ist.</span><span class="sxs-lookup"><span data-stu-id="29d8e-184">This error is also returned if the *cbInBuffer* parameter is less than the `sizeof(UCHAR)` or the *lpvInBuffer* parameter points to value that is not a **RCVALL_VALUE** enumeration value.</span></span> <span data-ttu-id="29d8e-185">Dieser Fehler kann auch zurückgegeben werden, wenn die dem Socket zugeordnete Netzwerkschnittstelle nicht gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="29d8e-185">This error can also be returned if the network interface associated with the socket cannot be found.</span></span> <span data-ttu-id="29d8e-186">Dies kann vorkommen, wenn die Netzwerkschnittstelle, die dem Socket zugeordnet ist, gelöscht oder entfernt wird (z. b. ein Entfernen von PCMCIA oder ein USB-Netzwerkgerät).</span><span class="sxs-lookup"><span data-stu-id="29d8e-186">This could occur if the network interface associated with the socket is deleted or removed (a remove PCMCIA or USB network device, for example).</span></span> |
| <span data-ttu-id="29d8e-187">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="29d8e-187">**WSAENETDOWN**</span></span> | <span data-ttu-id="29d8e-188">Das Netzwerk Subsystem ist fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="29d8e-188">The network subsystem has failed.</span></span> |
| <span data-ttu-id="29d8e-189">**WSAENOBUFS**</span><span class="sxs-lookup"><span data-stu-id="29d8e-189">**WSAENOBUFS**</span></span> | <span data-ttu-id="29d8e-190">Es ist kein Pufferspeicher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="29d8e-190">No buffer space available.</span></span> |
| <span data-ttu-id="29d8e-191">**Wsaumoproumopt**</span><span class="sxs-lookup"><span data-stu-id="29d8e-191">**WSAENOPROTOOPT**</span></span> | <span data-ttu-id="29d8e-192">Die Socketoption wird für das angegebene Protokoll nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="29d8e-192">The socket option is not supported on the specified protocol.</span></span> |
| <span data-ttu-id="29d8e-193">**Wsaumotsock**</span><span class="sxs-lookup"><span data-stu-id="29d8e-193">**WSAENOTSOCK**</span></span> | <span data-ttu-id="29d8e-194">Der Deskriptor *s* ist kein Socket.</span><span class="sxs-lookup"><span data-stu-id="29d8e-194">The descriptor *s* is not a socket.</span></span> |
| <span data-ttu-id="29d8e-195">**WSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="29d8e-195">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="29d8e-196">Der angegebene ioctl-Befehl wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="29d8e-196">The specified IOCTL command is not supported.</span></span> <span data-ttu-id="29d8e-197">Dieser Fehler wird zurückgegeben, wenn die " **SIO \_ rcvall** "-ioctl vom Transportanbieter nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="29d8e-197">This error is returned if the **SIO\_RCVALL** IOCTL is not supported by the transport provider.</span></span> |

## <a name="remarks"></a><span data-ttu-id="29d8e-198">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="29d8e-198">Remarks</span></span>

<span data-ttu-id="29d8e-199">Die IOCTL " **SIO \_ rcvall** " wird unter Windows 2000 und höheren Versionen des Betriebssystems unterstützt.</span><span class="sxs-lookup"><span data-stu-id="29d8e-199">The **SIO\_RCVALL** IOCTL is supported on Windows 2000 and later versions of the operating system.</span></span>

<span data-ttu-id="29d8e-200">Mit der " **SIO \_ rcvall** "-ioctl kann ein Socket alle IPv4-oder IPv6-Pakete an einer Netzwerkschnittstelle empfangen.</span><span class="sxs-lookup"><span data-stu-id="29d8e-200">The **SIO\_RCVALL** IOCTL enables a socket to receive all IPv4 or IPv6 packets on a network interface.</span></span>
<span data-ttu-id="29d8e-201">Das an die Funktion [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) oder **wspioctl** über gegebene Sockethandle muss einer der folgenden sein:</span><span class="sxs-lookup"><span data-stu-id="29d8e-201">The socket handle passed to the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function must be one of the following:</span></span>

* <span data-ttu-id="29d8e-202">Ein IPv4-Socket, der erstellt wurde, wobei die Adressfamilie auf AF_INET festgelegt ist, der socketyp auf SOCK_RAW und das Protokoll auf IPPROTO_IP festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="29d8e-202">An IPv4 socket that was created with the address family set to AF_INET, the socket type set to SOCK_RAW, and the protocol set to IPPROTO_IP.</span></span>
* <span data-ttu-id="29d8e-203">Ein IPv6-Socket, der erstellt wurde, wobei die Adressfamilie auf AF_INET6 festgelegt ist, der socketyp auf SOCK_RAW und das Protokoll auf IPPROTO_IPV6 festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="29d8e-203">An IPv6 socket that was created with the address family set to AF_INET6, the socket type set to SOCK_RAW, and the protocol set to IPPROTO_IPV6.</span></span>

<span data-ttu-id="29d8e-204">Weitere Informationen zu rohsockets finden Sie unter [**TCP/IP-rohsockets**](/windows/desktop/winsock/tcp-ip-raw-sockets-2).</span><span class="sxs-lookup"><span data-stu-id="29d8e-204">For more information on raw sockets, see [**TCP/IP Raw Sockets**](/windows/desktop/winsock/tcp-ip-raw-sockets-2).</span></span>

<span data-ttu-id="29d8e-205">Der Socket muss auch an eine explizite lokale IPv4-oder IPv6-Schnittstelle gebunden werden, was bedeutet, dass Sie keine Bindung an **inaddr \_ any** oder **in6addr \_ any** herstellen können.</span><span class="sxs-lookup"><span data-stu-id="29d8e-205">The socket also must be bound to an explicit local IPv4 or IPv6 interface, which means that you cannot bind to **INADDR\_ANY** or **in6addr\_any**.</span></span>

<span data-ttu-id="29d8e-206">Nachdem der Socket gebunden und die IOCTL erfolgreich abgeschlossen wurde, geben Aufrufe der [**WSARecv**](/windows/desktop/api/winsock2/nf-winsock2-wsarecv) -oder der [**empfangener**](/windows/desktop/api/winsock/nf-winsock-recv) -Funktion IPv4-Datagramme zurück, die die angegebene IPv4-Schnittstelle übergeben, oder geben IPv6-Datagramme zurück, die die angegebene IPv6-Schnittstelle übergeben.</span><span class="sxs-lookup"><span data-stu-id="29d8e-206">Once the socket is bound and the IOCTL completes successfully, calls to the [**WSARecv**](/windows/desktop/api/winsock2/nf-winsock2-wsarecv) or [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) functions return IPv4 datagrams passing through the given IPv4 interface or return IPv6 datagrams passing through the given IPv6 interface.</span></span>
<span data-ttu-id="29d8e-207">Beachten Sie, dass Sie einen ausreichend großen Puffer angeben müssen.</span><span class="sxs-lookup"><span data-stu-id="29d8e-207">Note that you must supply a sufficiently large buffer.</span></span>
<span data-ttu-id="29d8e-208">Durch Festlegen dieser ioctl werden nur IPv4-oder IPv6-Pakete für eine bestimmte Schnittstelle erfasst.</span><span class="sxs-lookup"><span data-stu-id="29d8e-208">Setting this IOCTL will only capture IPv4 or IPv6 packets on a given interface.</span></span>
<span data-ttu-id="29d8e-209">Mit dieser ioctl werden z. b. keine anderen Pakete (z. b. ARP-, IPX-und NetBEUI-Pakete) auf der-Schnittstelle erfasst.</span><span class="sxs-lookup"><span data-stu-id="29d8e-209">This IOCTL will not capture other packets (ARP, IPX, and NetBEUI packets, for example) on the interface.</span></span>

<span data-ttu-id="29d8e-210">Ein an eine bestimmte lokale Schnittstelle mit der " **SIO \_ rcvall** ioctl" gebundener Socket empfängt nur Pakete, die diese Schnittstelle passieren.</span><span class="sxs-lookup"><span data-stu-id="29d8e-210">A socket bound to a specific local interface with the **SIO\_RCVALL** IOCTL will receive only packets passing through that interface.</span></span>
<span data-ttu-id="29d8e-211">Er empfängt keine Pakete, die auf einer anderen Schnittstelle empfangen werden, und wird an eine andere Schnittstelle weitergeleitet, die sich von der mit der " **SIO \_ rcvall** ioctl" gebundenen</span><span class="sxs-lookup"><span data-stu-id="29d8e-211">It will not receive packets received on another interface and getting forwarded out on another interface different from the socket bound with **SIO\_RCVALL** IOCTL.</span></span>

<span data-ttu-id="29d8e-212">Unter Windows Server 2008 und früheren Versionen werden von der IOCTL-Einstellung " **SIO \_ rcvall** " keine lokalen Pakete erfasst, die von einer Netzwerkschnittstelle gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="29d8e-212">On Windows Server 2008 and earlier, the **SIO\_RCVALL** IOCTL setting would not capture local packets sent out of a network interface.</span></span>
<span data-ttu-id="29d8e-213">Diese enthielten Pakete, die auf einer anderen Schnittstelle empfangen wurden, und haben die für die IOCTL " **SIO \_ rcvall** " angegebene Netzwerkschnittstelle weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="29d8e-213">This included packets received on another interface and forwarded out the network interface specified for the **SIO\_RCVALL** IOCTL.</span></span>

<span data-ttu-id="29d8e-214">Unter Windows 7 und Windows Server 2008 R2 wurde dies geändert, sodass lokale Pakete, die von einer Netzwerkschnittstelle gesendet werden, ebenfalls aufgezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="29d8e-214">On Windows 7 and Windows Server 2008 R2 , this was changed so that local packets sent out of a network interface are also captured.</span></span>
<span data-ttu-id="29d8e-215">Dies schließt Pakete ein, die auf einer anderen Schnittstelle empfangen werden, und leitet dann die Netzwerkschnittstelle, die an den Socket gebunden ist, mit der " **SIO \_ rcvall** "</span><span class="sxs-lookup"><span data-stu-id="29d8e-215">This includes packets received on another interface and then forwarded out the network interface bound to the socket with **SIO\_RCVALL** IOCTL.</span></span>

<span data-ttu-id="29d8e-216">Das Festlegen dieser ioctl erfordert Administrator Rechte auf dem lokalen Computer.</span><span class="sxs-lookup"><span data-stu-id="29d8e-216">Setting this IOCTL requires Administrator privilege on the local computer.</span></span>

<span data-ttu-id="29d8e-217">Diese Funktion wird manchmal als gemischten-Modus bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="29d8e-217">This feature is sometimes referred to as promiscuous mode.</span></span>
<span data-ttu-id="29d8e-218">Jede direkte Änderung von der Anwendung dieser Option auf eine Schnittstelle und dann auf eine andere Schnittstelle mit einem einzigen-Befehl, der diese IOCTL verwendet, wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="29d8e-218">Any direct change from applying this option on one interface and then to another interface with a single call using this IOCTL is not supported.</span></span>
<span data-ttu-id="29d8e-219">Eine Anwendung muss zuerst dieses ioctl-Element verwenden, um das Verhalten auf der ersten Schnittstelle zu deaktivieren, und dann diese IOCTL verwenden, um das Verhalten für eine neue Schnittstelle zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="29d8e-219">An application must first use this IOCTL to turn off the behavior on the first interface, and then use this IOCTL to enable the behavior on a new interface.</span></span>

## <a name="see-also"></a><span data-ttu-id="29d8e-220">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="29d8e-220">See also</span></span>

[<span data-ttu-id="29d8e-221">**Glühbirne**</span><span class="sxs-lookup"><span data-stu-id="29d8e-221">**socket**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="29d8e-222">**TCP/IP-Rohdaten Sockets**</span><span class="sxs-lookup"><span data-stu-id="29d8e-222">**TCP/IP Raw Sockets**</span></span>](/windows/desktop/winsock/tcp-ip-raw-sockets-2)

[<span data-ttu-id="29d8e-223">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="29d8e-223">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[<span data-ttu-id="29d8e-224">**Wsagein verlappedresult**</span><span class="sxs-lookup"><span data-stu-id="29d8e-224">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="29d8e-225">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="29d8e-225">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="29d8e-226">**Wsaoverlgetauscht**</span><span class="sxs-lookup"><span data-stu-id="29d8e-226">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="29d8e-227">**Wsasocketa**</span><span class="sxs-lookup"><span data-stu-id="29d8e-227">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="29d8e-228">**Wsasocketw**</span><span class="sxs-lookup"><span data-stu-id="29d8e-228">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
