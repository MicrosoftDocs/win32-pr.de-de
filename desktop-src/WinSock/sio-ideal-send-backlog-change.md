---
description: Der Steuercode benachrichtigt eine Anwendung, wenn sich der ideale Wert für den Sende Rückstand für die Verbindung ändert.
ms.assetid: 337883a5-7ceb-40d3-b318-b86dd488b94a
title: SIO_IDEAL_SEND_BACKLOG_CHANGE Steuerungs Codes
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 4eb07efecd39774c60d47cbcf7245c5831760e06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755072"
---
# <a name="sio_ideal_send_backlog_change-control-code"></a><span data-ttu-id="99561-103">SIO_IDEAL_SEND_BACKLOG_CHANGE Steuerungs Codes</span><span class="sxs-lookup"><span data-stu-id="99561-103">SIO_IDEAL_SEND_BACKLOG_CHANGE Control Code</span></span>

## <a name="description"></a><span data-ttu-id="99561-104">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="99561-104">Description</span></span>

<span data-ttu-id="99561-105">Der optimale Änderungs Steuerungs Code für den "sio"- **\_ \_ \_ senderückstand \_** benachrichtigt eine Anwendung, wenn sich der Wert des idealen Sende Rückstands (ISB) für die Verbindung ändert.</span><span class="sxs-lookup"><span data-stu-id="99561-105">The **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** control code notifies an application when the ideal send backlog (ISB) value changes for the connection.</span></span>

<span data-ttu-id="99561-106">Um diesen Vorgang auszuführen, wenden Sie die [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) -oder **wspioctl** -Funktion mit den folgenden Parametern an.</span><span class="sxs-lookup"><span data-stu-id="99561-106">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_IDEAL_SEND_BACKLOG_CHANGE, // dwIoControlCode
  NULL,                         // lpvInBuffer
  0,                            // cbInBuffer
  NULL,         // output buffer
  0,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_IDEAL_SEND_BACKLOG_CHANGE, // dwIoControlCode
  NULL,                         // lpvInBuffer
  0,                            // cbInBuffer
  NULL,         // output buffer
  0,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,   // a WSATHREADID structure
  (LPINT) lpErrno   // a pointer to the error code.
);
```

## <a name="parameters"></a><span data-ttu-id="99561-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="99561-107">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="99561-108">s</span><span class="sxs-lookup"><span data-stu-id="99561-108">s</span></span>

<span data-ttu-id="99561-109">Ein Deskriptor, der einen Socket identifiziert.</span><span class="sxs-lookup"><span data-stu-id="99561-109">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="99561-110">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="99561-110">dwIoControlCode</span></span>

<span data-ttu-id="99561-111">Der Steuerelement Code für den Vorgang.</span><span class="sxs-lookup"><span data-stu-id="99561-111">The control code for the operation.</span></span>
<span data-ttu-id="99561-112">Verwenden Sie für diesen Vorgang die **\_ optimale \_ \_ \_ Änderung** des sendebacklogs von SIO.</span><span class="sxs-lookup"><span data-stu-id="99561-112">Use **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="99561-113">lpvinbuffer</span><span class="sxs-lookup"><span data-stu-id="99561-113">lpvInBuffer</span></span>

<span data-ttu-id="99561-114">Ein Zeiger auf den Eingabepuffer.</span><span class="sxs-lookup"><span data-stu-id="99561-114">A pointer to the input buffer.</span></span>
<span data-ttu-id="99561-115">Dieser Parameter wird für diesen Vorgang nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="99561-115">This parameter is unused for this operation.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="99561-116">cbinbuffer</span><span class="sxs-lookup"><span data-stu-id="99561-116">cbInBuffer</span></span>

<span data-ttu-id="99561-117">Die Größe des Eingabe Puffers in Bytes. Dieser Parameter wird für diesen Vorgang nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="99561-117">The size, in bytes, of the input buffer.This parameter is unused for this operation.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="99561-118">lpvoutbuffer</span><span class="sxs-lookup"><span data-stu-id="99561-118">lpvOutBuffer</span></span>

<span data-ttu-id="99561-119">Ein Zeiger auf den Ausgabepuffer.</span><span class="sxs-lookup"><span data-stu-id="99561-119">A pointer to the output buffer.</span></span>
<span data-ttu-id="99561-120">Dieser Parameter wird für diesen Vorgang nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="99561-120">This parameter is unused for this operation.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="99561-121">cboutbuffer</span><span class="sxs-lookup"><span data-stu-id="99561-121">cbOutBuffer</span></span>

<span data-ttu-id="99561-122">Die Größe des Ausgabepuffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="99561-122">The size, in bytes, of the output buffer.</span></span>
<span data-ttu-id="99561-123">Dieser Parameter muss auf 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="99561-123">This parameter must be set to zero.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="99561-124">lpcbbyteszurück gegeben</span><span class="sxs-lookup"><span data-stu-id="99561-124">lpcbBytesReturned</span></span>

<span data-ttu-id="99561-125">Ein Zeiger auf eine Variable, die die Größe der im Ausgabepuffer gespeicherten Daten (in Bytes) empfängt.</span><span class="sxs-lookup"><span data-stu-id="99561-125">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>
<span data-ttu-id="99561-126">Dieser zurückgegebene Parameter verweist auf einen **DWORD** -Wert von 0 (null) für diesen Vorgang, da keine Ausgabe vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="99561-126">This returned parameter points to a **DWORD** value of zero for this operation, since there is no output.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="99561-127">lpvoverlgetauscht</span><span class="sxs-lookup"><span data-stu-id="99561-127">lpvOverlapped</span></span>

<span data-ttu-id="99561-128">Ein Zeiger auf eine [**wsaoverllapp**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="99561-128">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="99561-129">Wenn Socket *s* ohne das überlappende Attribut erstellt wurde, wird der *lpoverllapp* -Parameter ignoriert.</span><span class="sxs-lookup"><span data-stu-id="99561-129">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="99561-130">Wenn *s* mit dem überlappenden Attribut geöffnet wurde und der *lpoverlgetauscht* -Parameter nicht **null** ist, wird der Vorgang als überlappende (asynchrone) Operation ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="99561-130">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="99561-131">In diesem Fall muss der *lpoverllapp* -Parameter auf eine gültige [**wsaoverllapp**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) -Struktur zeigen.</span><span class="sxs-lookup"><span data-stu-id="99561-131">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="99561-132">Bei überlappenden Vorgängen gibt die Funktion [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) oder **wspioctl** sofort zurück, und die entsprechende Vervollständigungs Methode wird signalisiert, wenn der Vorgang abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="99561-132">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="99561-133">Andernfalls gibt die Funktion nicht zurück, bis der Vorgang abgeschlossen ist oder ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="99561-133">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="99561-134">lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="99561-134">lpCompletionRoutine</span></span>

<span data-ttu-id="99561-135">Typ: \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="99561-135">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="99561-136">Ein Zeiger auf die Vervollständigungs Routine, die aufgerufen wird, wenn der Vorgang abgeschlossen wurde (bei nicht überlappenden Sockets ignoriert).</span><span class="sxs-lookup"><span data-stu-id="99561-136">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="99561-137">lpthreadid</span><span class="sxs-lookup"><span data-stu-id="99561-137">lpThreadId</span></span>

<span data-ttu-id="99561-138">Ein Zeiger auf eine [**wsathreadid**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) -Struktur, die vom Anbieter in einem nachfolgenden [**wpuqueueapc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc)-Rückruf verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="99561-138">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="99561-139">Der Anbieter sollte die referenzierte [**wsathreadid**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) -Struktur (nicht den Zeiger auf dieselbe) speichern, bis die [**wpuqueueapc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc) -Funktion zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="99561-139">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="99561-140">**Hinweis**  Dieser Parameter gilt nur für die **wspioctl** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="99561-140">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="99561-141">lperrno</span><span class="sxs-lookup"><span data-stu-id="99561-141">lpErrno</span></span>

<span data-ttu-id="99561-142">Ein Zeiger auf den Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="99561-142">A pointer to the error code.</span></span>

<span data-ttu-id="99561-143">**Hinweis**  Dieser Parameter gilt nur für die **wspioctl** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="99561-143">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="99561-144">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="99561-144">Return value</span></span>

<span data-ttu-id="99561-145">Wenn der Vorgang erfolgreich abgeschlossen wird, gibt die [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) -oder **wspioctl** -Funktion NULL zurück.</span><span class="sxs-lookup"><span data-stu-id="99561-145">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="99561-146">Wenn der Vorgang fehlschlägt oder aussteht, gibt die Funktion [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) oder **wspioctl** einen **\_ Socketfehler** zurück.</span><span class="sxs-lookup"><span data-stu-id="99561-146">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="99561-147">Um erweiterte Fehlerinformationen abzurufen, nennen Sie [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="99561-147">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="99561-148">Fehlercode</span><span class="sxs-lookup"><span data-stu-id="99561-148">Error code</span></span> | <span data-ttu-id="99561-149">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="99561-149">Meaning</span></span> |
|------------|---------|
| <span data-ttu-id="99561-150">**ausstehende WSA-e/a \_ \_**</span><span class="sxs-lookup"><span data-stu-id="99561-150">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="99561-151">Ein übergebener Vorgang wurde erfolgreich initiiert, und der Abschluss wird zu einem späteren Zeitpunkt angegeben.</span><span class="sxs-lookup"><span data-stu-id="99561-151">An overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="99561-152">**WSA- \_ Vorgang \_ abgebrochen**</span><span class="sxs-lookup"><span data-stu-id="99561-152">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="99561-153">Ein über Lapp ender Vorgang wurde aufgrund der Schließung des Sockets oder der Ausführung des Befehls " **SIO \_ Flush** ioctl" abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="99561-153">An overlapped operation was canceled due to the closure of the socket or the execution of the **SIO\_FLUSH** IOCTL command.</span></span> |
| <span data-ttu-id="99561-154">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="99561-154">**WSAEFAULT**</span></span> | <span data-ttu-id="99561-155">Der *lpoverllapp* -oder *lpCompletionRoutine* -Parameter ist nicht vollständig in einem gültigen Teil des Benutzer Adressraums enthalten.</span><span class="sxs-lookup"><span data-stu-id="99561-155">The *lpOverlapped* or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="99561-156">**Wsaeingabe Progress**</span><span class="sxs-lookup"><span data-stu-id="99561-156">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="99561-157">Die-Funktion wird aufgerufen, wenn ein Rückruf ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="99561-157">The function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="99561-158">**Wsaeingabe**</span><span class="sxs-lookup"><span data-stu-id="99561-158">**WSAEINTR**</span></span> | <span data-ttu-id="99561-159">Ein Blockierungs Vorgang wurde unterbrochen.</span><span class="sxs-lookup"><span data-stu-id="99561-159">A blocking operation was interrupted.</span></span> |
| <span data-ttu-id="99561-160">**Wsaabval**</span><span class="sxs-lookup"><span data-stu-id="99561-160">**WSAEINVAL**</span></span> | <span data-ttu-id="99561-161">Der *dwIoControlCode* -Parameter ist kein gültiger Befehl, oder ein angegebener Eingabeparameter ist nicht zulässig, oder der Befehl ist nicht auf den angegebenen Sockettyp anwendbar.</span><span class="sxs-lookup"><span data-stu-id="99561-161">The *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> <span data-ttu-id="99561-162">Dieser Fehler wird zurückgegeben, wenn der *cboutbuffer* -Parameter nicht 0 (null) ist.</span><span class="sxs-lookup"><span data-stu-id="99561-162">This error is returned if the *cbOutBuffer* parameter is not zero.</span></span> |
| <span data-ttu-id="99561-163">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="99561-163">**WSAENETDOWN**</span></span> | <span data-ttu-id="99561-164">Das Netzwerk Subsystem ist fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="99561-164">The network subsystem has failed.</span></span> |
| <span data-ttu-id="99561-165">**Wsaumoproumopt**</span><span class="sxs-lookup"><span data-stu-id="99561-165">**WSAENOPROTOOPT**</span></span> | <span data-ttu-id="99561-166">Die Socketoption wird für das angegebene Protokoll nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="99561-166">The socket option is not supported on the specified protocol.</span></span> |
| <span data-ttu-id="99561-167">**WSAENOTCONN**</span><span class="sxs-lookup"><span data-stu-id="99561-167">**WSAENOTCONN**</span></span> | <span data-ttu-id="99561-168">Die Socket *s* ist nicht verbunden.</span><span class="sxs-lookup"><span data-stu-id="99561-168">The socket *s* is not connected.</span></span> |
| <span data-ttu-id="99561-169">**Wsaumotsock**</span><span class="sxs-lookup"><span data-stu-id="99561-169">**WSAENOTSOCK**</span></span> | <span data-ttu-id="99561-170">Der Deskriptor *s* ist kein Socket.</span><span class="sxs-lookup"><span data-stu-id="99561-170">The descriptor *s* is not a socket.</span></span> |
| <span data-ttu-id="99561-171">**WSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="99561-171">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="99561-172">Der angegebene ioctl-Befehl wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="99561-172">The specified IOCTL command is not supported.</span></span> <span data-ttu-id="99561-173">Dieser Fehler wird zurückgegeben, wenn die IOCTL-IOCTL- **\_ Änderung des idealen \_ Sende \_ Rückstands \_** nicht vom Transportanbieter unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="99561-173">This error is returned if the **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** IOCTL is not supported by the transport provider.</span></span> <span data-ttu-id="99561-174">Dieser Fehler wird auch zurückgegeben, wenn ein Versuch der Verwendung der optimalen ioctl-Änderung für das **\_ \_ Sende \_ Rückstands \_** Element für einen Datagramm-Socket durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="99561-174">This error is also returned when an attempt to use the **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** IOCTL is made on a datagram socket.</span></span> |

## <a name="remarks"></a><span data-ttu-id="99561-175">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="99561-175">Remarks</span></span>

<span data-ttu-id="99561-176">Die optimale IOCTL- **\_ \_ \_ \_ Änderung des Sende** Backlogs wird unter Windows Server 2008, Windows Vista mit Service Pack 1 (SP1) und höheren Versionen des Betriebssystems unterstützt.</span><span class="sxs-lookup"><span data-stu-id="99561-176">The **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** IOCTL is supported on Windows Server 2008, Windows Vista with Service Pack 1 (SP1), and later versions of the operating system.</span></span>

<span data-ttu-id="99561-177">Beim Senden von Daten über eine TCP-Verbindung mithilfe von Windows Sockets ist es wichtig, dass Sie eine ausreichende Menge an ausstehenden Daten (gesendet, aber noch nicht bestätigt) in TCP aufbewahren, um den höchsten Durchsatz zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="99561-177">When sending data over a TCP connection using Windows sockets, it is important to keep a sufficient amount of data outstanding (sent but not acknowledged yet) in TCP in order to achieve the highest throughput.</span></span>
<span data-ttu-id="99561-178">Der ideale Wert für die Datenmenge, die für den optimalen Durchsatz für die TCP-Verbindung aussteht, wird als ideale Größe des sendebacklogs (ISB) bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="99561-178">The ideal value for the amount of data outstanding to achieve the best throughput for the TCP connection is called the ideal send backlog (ISB) size.</span></span>
<span data-ttu-id="99561-179">Der ISB-Wert ist eine Funktion des Produkts zur Bandbreiten Verzögerung der TCP-Verbindung und des angekündigten Empfangs Fensters des Empfängers (und zum Teil der Überlastung im Netzwerk).</span><span class="sxs-lookup"><span data-stu-id="99561-179">The ISB value is a function of the bandwidth-delay product of the TCP connection and the receiver's advertised receive window (and partly the amount of congestion in the network).</span></span>

<span data-ttu-id="99561-180">Der ISB-Wert pro Verbindung ist über die TCP-Protokoll Implementierung in Windows Server 2008, Windows Vista mit SP1 und höheren Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="99561-180">The ISB value per connection is available from the TCP protocol implementation in Windows Server 2008, Windows Vista with SP1, and later versions of the operating system.</span></span>
<span data-ttu-id="99561-181">Die optimale IOCTL- **\_ \_ \_ \_ Änderung des Sende** Backlogs kann von einer Anwendung verwendet werden, um eine Benachrichtigung zu erhalten, wenn der ISB-Wert für eine Verbindung dynamisch geändert wird.</span><span class="sxs-lookup"><span data-stu-id="99561-181">The **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** IOCTL can be used by an application to get a notification when the ISB value changes dynamically for a connection.</span></span>

<span data-ttu-id="99561-182">Unter Windows Server 2008, Windows Vista mit SP1 und höheren Versionen des Betriebssystems werden die Daten von **der \_ optimalen \_ Sende \_ Rückstands \_ Änderung** und der [**\_ optimalen \_ Sende \_ Rückstand \_ Abfrage**](sio-ideal-send-backlog-query.md) IOCTLs von der optimalen Sende Rückstands Abfrage für Stream-orientierte Sockets unterstützt, die verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="99561-182">On Windows Server 2008, Windows Vista with SP1, and later versions of the operating system, the **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** and [**SIO\_IDEAL\_SEND\_BACKLOG\_QUERY**](sio-ideal-send-backlog-query.md) IOCTLs are supported on stream-oriented sockets that are in a connected state.</span></span>

<span data-ttu-id="99561-183">Der Bereich für den ISB-Wert einer TCP-Verbindung kann theoretisch von 0 bis maximal 16 Megabyte abweichen.</span><span class="sxs-lookup"><span data-stu-id="99561-183">The range for the ISB value for a TCP connection can theoretically vary from 0 to a maximum of 16 megabytes.</span></span>

<span data-ttu-id="99561-184">Eine typische Verwendung des ISB-Mechanismus zur Erzielung eines besseren Durchsatzes bei Produkt Verbindungen mit hoher Bandbreiten Verzögerung finden Sie auf der Referenzseite zur IOCTL- [**\_ \_ \_ \_ Abfrage**](sio-ideal-send-backlog-query.md) für den optimalen sendebackbackdukt.</span><span class="sxs-lookup"><span data-stu-id="99561-184">See the [**SIO\_IDEAL\_SEND\_BACKLOG\_QUERY**](sio-ideal-send-backlog-query.md) IOCTL reference page for typical usage of the ISB mechanism for achieving better throughput over high bandwidth-delay product connections.</span></span>

<span data-ttu-id="99561-185">Die optimale IOCTL- **\_ \_ \_ \_ Änderung des Sende** Backlogs ist nur auf einem Stream-Socket zulässig, der sich im verbundenen Zustand befindet.</span><span class="sxs-lookup"><span data-stu-id="99561-185">The **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** IOCTL is allowed only on a stream socket that is in the connected state.</span></span>
<span data-ttu-id="99561-186">Andernfalls schlägt die Funktion [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) oder **wspioctl** mit **wsaenotconn** fehl.</span><span class="sxs-lookup"><span data-stu-id="99561-186">Otherwise the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function will fail with **WSAENOTCONN**.</span></span>

<span data-ttu-id="99561-187">Die optimale IOCTL- **\_ \_ \_ \_ Änderung des Sende** Backlogs von "Port" verwendet keine Eingabe-oder Ausgabepuffer und-IDs oder-Blöcke, bis eine ISB-Änderung an der zugrunde liegenden Verbindung erfolgt</span><span class="sxs-lookup"><span data-stu-id="99561-187">The **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** IOCTL uses no input or output buffers and pends or blocks until an ISB change occurs on the underlying connection.</span></span>
<span data-ttu-id="99561-188">Wenn diese IOCTL abgeschlossen ist, kann eine Winsock-Anwendung die IOCTL- [**Abfrage "sio \_ ideal Send \_ backbackbackquery \_ \_**](sio-ideal-send-backlog-query.md) " verwenden, um den neuen ISB-Wert für die Verbindung abzurufen.</span><span class="sxs-lookup"><span data-stu-id="99561-188">When this IOCTL is completed, a Winsock application can use the [**SIO\_IDEAL\_SEND\_BACKLOG\_QUERY**](sio-ideal-send-backlog-query.md) IOCTL to retrieve the new ISB value on the connection.</span></span>

<span data-ttu-id="99561-189">Die optimale IOCTL- **\_ \_ \_ \_ Änderung des Sende** Backlogs unterstützt den nicht blockierenden Modus nicht.</span><span class="sxs-lookup"><span data-stu-id="99561-189">The **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** IOCTL does not support non-blocking mode.</span></span>
<span data-ttu-id="99561-190">Eine Anwendung ist berechtigt, diese IOCTL für einen nicht blockierenden Socket auszugeben, aber die IOCTL wird einfach blockiert oder per ausgesetzt blockiert, bis der ISB-Wert geändert wird.</span><span class="sxs-lookup"><span data-stu-id="99561-190">An application is allowed to issue this IOCTL on a non-blocking socket, but the IOCTL will simply block or pend until the ISB value changes.</span></span>

<span data-ttu-id="99561-191">Wenn die Parameter *lpoverlgetauscht* und *lpCompletionRoutine* NULL sind, wird der Socket in dieser Funktion als nicht überlappenden Socket behandelt.</span><span class="sxs-lookup"><span data-stu-id="99561-191">If both *lpOverlapped* and *lpCompletionRoutine* parameters are NULL, the socket in this function will be treated as a non-overlapped socket.</span></span>
<span data-ttu-id="99561-192">Bei einem nicht überlappenden Socket werden die Parameter *lpoverlgetauscht* und *lpCompletionRoutine* ignoriert, mit der Ausnahme, dass die Funktion blockiert werden kann, wenn sich Socket *s* im Blockierungs Modus befindet.</span><span class="sxs-lookup"><span data-stu-id="99561-192">For a non-overlapped socket, *lpOverlapped* and *lpCompletionRoutine* parameters are ignored, except that the function can block if socket *s* is in blocking mode.</span></span>
<span data-ttu-id="99561-193">Wenn sich Socket *s* im nicht blockierenden Modus befindet, wird diese Funktion immer noch blockiert, da diese spezielle ioctl den nicht blockierenden Modus nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="99561-193">If socket *s* is in non-blocking mode, this function will still block since this particular IOCTL does not support non-blocking mode.</span></span>

<span data-ttu-id="99561-194">Bei überlappenden Sockets werden Vorgänge, die nicht sofort abgeschlossen werden können, initiiert, und der Abschluss wird zu einem späteren Zeitpunkt angegeben.</span><span class="sxs-lookup"><span data-stu-id="99561-194">For overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>

<span data-ttu-id="99561-195">Alle ioctl können unbegrenzt blockieren, abhängig von der Implementierung des Dienstanbieters.</span><span class="sxs-lookup"><span data-stu-id="99561-195">Any IOCTL may block indefinitely, depending on the service provider's implementation.</span></span>
<span data-ttu-id="99561-196">Wenn die Anwendung die Blockierung in einem [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) -oder **wspioctl** -Funktions aufrufnis nicht tolerieren kann, werden überlappende e/a-Vorgänge für IOCTLs empfohlen, die besonders wahrscheinlich blockiert werden.</span><span class="sxs-lookup"><span data-stu-id="99561-196">If the application cannot tolerate blocking in a [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function call, overlapped I/O would be advised for IOCTLs that are especially likely to block.</span></span>

<span data-ttu-id="99561-197">Der optimale ioctl-Wert für die **\_ \_ Sende \_ Rückstands \_ Änderung** von "sio" stellt eine Benachrichtigung bereit und wird erwartet, bis der ISB-Wert geändert wird.</span><span class="sxs-lookup"><span data-stu-id="99561-197">The **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** IOCTL provides a notification and is expected to block or pend until the ISB value changes.</span></span>
<span data-ttu-id="99561-198">Daher wird er normalerweise asynchron aufgerufen, wenn der *lpoverllapp* -Parameter auf eine gültige, wsaoverllapp Ende Struktur festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="99561-198">So it would commonly be called asynchronously with the *lpOverlapped* parameter set to a valid WSAOVERLAPPED structure.</span></span>

<span data-ttu-id="99561-199">**In den** folgenden Fällen kann bei der Änderung der IOCTL-Änderung bei der **\_ optimalen \_ Sende \_ Rückstands \_ Änderung** **ein Fehler auftreten \_ \_** :</span><span class="sxs-lookup"><span data-stu-id="99561-199">The **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** IOCTL can fail with **WSAEINTR** or **WSA\_OPERATION\_ABORTED** under the following cases:</span></span>

* <span data-ttu-id="99561-200">Die TCP-Verbindung ist in der Senderichtung ordnungsgemäß getrennt.</span><span class="sxs-lookup"><span data-stu-id="99561-200">The TCP connection is gracefully disconnected in the send direction.</span></span> <span data-ttu-id="99561-201">Dies kann ein Ergebnis eines Aufrufs der Funktion zum Herunterfahren mit dem auf **SD \_ Send** festgelegten Parameter, einem Aufrufen der **disconnectex** -Funktion oder eines Aufrufs der Funktion **TransmitFile** oder **transmitpaketen** mit dem Parameter *dwFlags* , der auf **tf \_ Disconnect** oder TF- **\_ Wiederverwendung** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="99561-201">This can occur as a result of a call to shutdown function with the how parameter set to **SD\_SEND**, a call to the **DisconnectEx** function, or a call to the **TransmitFile** or **TransmitPackets** function with *dwFlags* parameter set to **TF\_DISCONNECT** or **TF\_REUSE**.</span></span>
* <span data-ttu-id="99561-202">Die TCP-Verbindung wurde zurückgesetzt oder abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="99561-202">The TCP connection has been reset or aborted.</span></span>
* <span data-ttu-id="99561-203">Die Anwendung gibt die IOCTL-Änderung von "sio ideal Send backbackbacklogs" aus, wenn bereits eine Benachrichtigung über eine **\_ \_ gesendete \_ \_** Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="99561-203">The application issues a **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** IOCTL when there is already a pended notification request.</span></span> <span data-ttu-id="99561-204">Nur 1 1 gesendete SIO-ideale Änderungsanforderungen für den **\_ \_ Sende \_ Rückstand \_** sind gleichzeitig zulässig.</span><span class="sxs-lookup"><span data-stu-id="99561-204">Only one one pended **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** request is allowed at a time.</span></span>
* <span data-ttu-id="99561-205">Die Anforderung wird vom e/a-Manager abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="99561-205">The request is canceled by the I/O Manager.</span></span>
* <span data-ttu-id="99561-206">Der Socket ist geschlossen.</span><span class="sxs-lookup"><span data-stu-id="99561-206">The socket is closed.</span></span>

<span data-ttu-id="99561-207">In der Header Datei " *Ws2tcpip. h* " sind zwei Inline-Wrapper Funktionen für diese IOCTLs definiert.</span><span class="sxs-lookup"><span data-stu-id="99561-207">Two inline wrapper functions for these IOCTLs are defined in the *Ws2tcpip.h* header file.</span></span>
<span data-ttu-id="99561-208">Es wird empfohlen, dass diese Inline Funktionen anstelle der **\_ optimalen optimalen \_ Sende \_ Rückstands \_ Änderung** und der [**\_ optimalen \_ Sende Rückstands Abfrage von der optimalen Sende \_ Rückstands \_ Abfrage**](sio-ideal-send-backlog-query.md) IOCTLs verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="99561-208">It is recommended that these inline functions be used instead of using the **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** and [**SIO\_IDEAL\_SEND\_BACKLOG\_QUERY**](sio-ideal-send-backlog-query.md) IOCTLs directly.</span></span>

<span data-ttu-id="99561-209">Die Funktion "Inline Wrapper" für die IOCTL-Änderung von " **SIO \_ ideal \_ Send \_ \_** Backlogs" ist die Funktion " **idesendbacklognotify** ".</span><span class="sxs-lookup"><span data-stu-id="99561-209">The inline wrapper function for the **SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE** IOCTL is the **idealsendbacklognotify** function.</span></span>

<span data-ttu-id="99561-210">Die Funktion "Inline Wrapper" für die IOCTL- [**\_ \_ \_ \_ Abfrage des optimalen**](sio-ideal-send-backlog-query.md) sendebacklogs ist die Funktion " **ideal Send backlogquery** ".</span><span class="sxs-lookup"><span data-stu-id="99561-210">The inline wrapper function for the [**SIO\_IDEAL\_SEND\_BACKLOG\_QUERY**](sio-ideal-send-backlog-query.md) IOCTL is the **idealsendbacklogquery** function.</span></span>

## <a name="see-also"></a><span data-ttu-id="99561-211">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="99561-211">See also</span></span>

[<span data-ttu-id="99561-212">**SIO_IDEAL_SEND_BACKLOG_QUERY**</span><span class="sxs-lookup"><span data-stu-id="99561-212">**SIO_IDEAL_SEND_BACKLOG_QUERY**</span></span>](sio-ideal-send-backlog-query.md)

[<span data-ttu-id="99561-213">**Glühbirne**</span><span class="sxs-lookup"><span data-stu-id="99561-213">**socket**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="99561-214">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="99561-214">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)

[<span data-ttu-id="99561-215">**Wsagein verlappedresult**</span><span class="sxs-lookup"><span data-stu-id="99561-215">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="99561-216">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="99561-216">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="99561-217">**Wsaoverlgetauscht**</span><span class="sxs-lookup"><span data-stu-id="99561-217">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="99561-218">**Wsasocketa**</span><span class="sxs-lookup"><span data-stu-id="99561-218">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="99561-219">**Wsasocketw**</span><span class="sxs-lookup"><span data-stu-id="99561-219">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
