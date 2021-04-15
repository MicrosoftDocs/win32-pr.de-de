---
description: Ein Steuerelement Code, der die anfänglichen RTO-Parameter (Neuübertragungs Timeout) für einen Socket konfiguriert.
ms.assetid: F5ABAE57-E0F0-4AEB-825C-B53AEE8210E7
title: SIO_TCP_INITIAL_RTO Steuerungs Codes
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 116bab23c2c5f4ef21b77a1b7f9fefa8b3ff3099
ms.sourcegitcommit: 191184ea30e209f67267ebe5b222dc16965e54e0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2020
ms.locfileid: "104474583"
---
# <a name="sio_tcp_initial_rto-control-code"></a><span data-ttu-id="fa446-103">SIO_TCP_INITIAL_RTO Steuerungs Codes</span><span class="sxs-lookup"><span data-stu-id="fa446-103">SIO_TCP_INITIAL_RTO control code</span></span>

## <a name="description"></a><span data-ttu-id="fa446-104">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fa446-104">Description</span></span>

<span data-ttu-id="fa446-105">Der **SIO_TCP_INITIAL_RTO** -Steuerungs Code konfiguriert anfängliche RTO-Parameter (Neuübertragungs Timeout) für einen Socket.</span><span class="sxs-lookup"><span data-stu-id="fa446-105">The **SIO_TCP_INITIAL_RTO** control code configures initial retransmission timeout (RTO) parameters on a socket.</span></span>

<span data-ttu-id="fa446-106">Um diesen Vorgang auszuführen, wenden Sie die [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) -oder **wspioctl** -Funktion mit den folgenden Parametern an.</span><span class="sxs-lookup"><span data-stu-id="fa446-106">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_TCP_INITIAL_RTO,                // dwIoControlCode
  (LPVOID) lpvInBuffer,   // pointer to a TCP_INITIAL_RTO_PARAMETERS structure
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,         // pointer to output buffer
  (DWORD) cbOutBuffer,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_TCP_INITIAL_RTO,                // dwIoControlCode
  (LPVOID) lpvInBuffer,   // pointer to a TCP_INITIAL_RTO_PARAMETERS structure
  (DWORD) cbInBuffer,           // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,         // pointer to output buffer
  (DWORD) cbOutBuffer,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,   // a WSATHREADID structure
  (LPINT) lpErrno   // a pointer to the error code.
);
```

## <a name="parameters"></a><span data-ttu-id="fa446-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="fa446-107">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="fa446-108">s</span><span class="sxs-lookup"><span data-stu-id="fa446-108">s</span></span>

<span data-ttu-id="fa446-109">Ein Deskriptor, der einen Socket identifiziert.</span><span class="sxs-lookup"><span data-stu-id="fa446-109">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="fa446-110">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="fa446-110">dwIoControlCode</span></span>

<span data-ttu-id="fa446-111">Der Steuerelement Code für den Vorgang.</span><span class="sxs-lookup"><span data-stu-id="fa446-111">The control code for the operation.</span></span>
<span data-ttu-id="fa446-112">Verwenden Sie **SIO_TCP_INITIAL_RTO** für diesen Vorgang.</span><span class="sxs-lookup"><span data-stu-id="fa446-112">Use **SIO_TCP_INITIAL_RTO** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="fa446-113">lpvinbuffer</span><span class="sxs-lookup"><span data-stu-id="fa446-113">lpvInBuffer</span></span>

<span data-ttu-id="fa446-114">Ein Zeiger auf den Eingabepuffer.</span><span class="sxs-lookup"><span data-stu-id="fa446-114">A pointer to the input buffer.</span></span>
<span data-ttu-id="fa446-115">Dieser Parameter enthält einen Zeiger auf die [**TCP_INITIAL_RTO_PARAMETERS**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_initial_rto_parameters) , die dem Socket zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="fa446-115">This parameter contains a pointer to the [**TCP_INITIAL_RTO_PARAMETERS**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_initial_rto_parameters) associated with the socket.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="fa446-116">cbinbuffer</span><span class="sxs-lookup"><span data-stu-id="fa446-116">cbInBuffer</span></span>

<span data-ttu-id="fa446-117">Die Größe des Eingabe Puffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="fa446-117">The size, in bytes, of the input buffer.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="fa446-118">lpvoutbuffer</span><span class="sxs-lookup"><span data-stu-id="fa446-118">lpvOutBuffer</span></span>

<span data-ttu-id="fa446-119">Ein Zeiger auf den Ausgabepuffer.</span><span class="sxs-lookup"><span data-stu-id="fa446-119">A pointer to the output buffer.</span></span>
<span data-ttu-id="fa446-120">Dieser Parameter wird für diesen Vorgang nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="fa446-120">This parameter is unused for this operation.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="fa446-121">cboutbuffer</span><span class="sxs-lookup"><span data-stu-id="fa446-121">cbOutBuffer</span></span>

<span data-ttu-id="fa446-122">Die Größe des Ausgabepuffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="fa446-122">The size, in bytes, of the output buffer.</span></span>
<span data-ttu-id="fa446-123">Dieser Parameter muss auf 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="fa446-123">This parameter must be set to zero.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="fa446-124">lpcbbyteszurück gegeben</span><span class="sxs-lookup"><span data-stu-id="fa446-124">lpcbBytesReturned</span></span>

<span data-ttu-id="fa446-125">Ein Zeiger auf eine Variable, die die Größe der im Ausgabepuffer gespeicherten Daten (in Bytes) empfängt.</span><span class="sxs-lookup"><span data-stu-id="fa446-125">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>

<span data-ttu-id="fa446-126">Wenn der Ausgabepuffer zu klein ist, schlägt der-Befehl fehl, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) gibt [**WSAEINVAL**](windows-sockets-error-codes-2.md)zurück, und der *lpcbbytesreturns* -Parameter verweist auf den **DWORD** -Wert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="fa446-126">If the output buffer is too small, the call fails, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns [**WSAEINVAL**](windows-sockets-error-codes-2.md), and the *lpcbBytesReturned* parameter points to a **DWORD** value of zero.</span></span>

<span data-ttu-id="fa446-127">Wenn *lpoverlgetauscht* gleich **null** ist, kann der **DWORD** -Wert, auf den der *lpcbbytesall* -Parameter verweist, der bei einem erfolgreichen-Vorgang zurückgegeben wird, nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="fa446-127">If *lpOverlapped* is **NULL**, the **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned on a successful call cannot be zero.</span></span>

<span data-ttu-id="fa446-128">Wenn der *lpoverllapp* -Parameter für überlappende Sockets nicht **null** ist, werden Vorgänge, die nicht sofort abgeschlossen werden können, initiiert, und der Abschluss wird zu einem späteren Zeitpunkt angegeben.</span><span class="sxs-lookup"><span data-stu-id="fa446-128">If the *lpOverlapped* parameter is not **NULL** for overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>
<span data-ttu-id="fa446-129">Der **DWORD** -Wert, auf den der zurückgegebene *lpcbbyteszurück gegebene* Parameter verweist, kann NULL sein, da die Größe der gespeicherten Daten erst bestimmt werden kann, wenn der überlappende Vorgang abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="fa446-129">The **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned may be zero since the size of the data stored can't be determined until the overlapped operation has completed.</span></span>
<span data-ttu-id="fa446-130">Der endgültige Abschluss Status kann abgerufen werden, wenn die geeignete Vervollständigungs Methode signalisiert wird, wenn der Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="fa446-130">The final completion status can be retrieved when the appropriate completion method is signaled when the operation has completed.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="fa446-131">lpvoverlgetauscht</span><span class="sxs-lookup"><span data-stu-id="fa446-131">lpvOverlapped</span></span>

<span data-ttu-id="fa446-132">Ein Zeiger auf eine [**wsaoverllapp**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="fa446-132">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="fa446-133">Wenn Socket *s* ohne das überlappende Attribut erstellt wurde, wird der *lpoverllapp* -Parameter ignoriert.</span><span class="sxs-lookup"><span data-stu-id="fa446-133">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="fa446-134">Wenn *s* mit dem überlappenden Attribut geöffnet wurde und der *lpoverlgetauscht* -Parameter nicht **null** ist, wird der Vorgang als überlappende (asynchrone) Operation ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fa446-134">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="fa446-135">In diesem Fall muss der *lpoverllapp* -Parameter auf eine gültige [**wsaoverllapp**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) -Struktur zeigen.</span><span class="sxs-lookup"><span data-stu-id="fa446-135">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="fa446-136">Bei überlappenden Vorgängen gibt die Funktion [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) oder **wspioctl** sofort zurück, und die entsprechende Vervollständigungs Methode wird signalisiert, wenn der Vorgang abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="fa446-136">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="fa446-137">Andernfalls gibt die Funktion nicht zurück, bis der Vorgang abgeschlossen ist oder ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="fa446-137">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="fa446-138">lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="fa446-138">lpCompletionRoutine</span></span>

<span data-ttu-id="fa446-139">Typ: \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="fa446-139">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="fa446-140">Ein Zeiger auf die Vervollständigungs Routine, die aufgerufen wird, wenn der Vorgang abgeschlossen wurde (bei nicht überlappenden Sockets ignoriert).</span><span class="sxs-lookup"><span data-stu-id="fa446-140">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="fa446-141">lpthreadid</span><span class="sxs-lookup"><span data-stu-id="fa446-141">lpThreadId</span></span>

<span data-ttu-id="fa446-142">Ein Zeiger auf eine [**wsathreadid**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) -Struktur, die vom Anbieter in einem nachfolgenden [**wpuqueueapc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc)-Rückruf verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="fa446-142">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="fa446-143">Der Anbieter sollte die referenzierte [**wsathreadid**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) -Struktur (nicht den Zeiger auf dieselbe) speichern, bis die [**wpuqueueapc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) -Funktion zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="fa446-143">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="fa446-144">**Hinweis**  Dieser Parameter gilt nur für die **wspioctl** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="fa446-144">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="fa446-145">lperrno</span><span class="sxs-lookup"><span data-stu-id="fa446-145">lpErrno</span></span>

<span data-ttu-id="fa446-146">Ein Zeiger auf den Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="fa446-146">A pointer to the error code.</span></span>

<span data-ttu-id="fa446-147">**Hinweis**  Dieser Parameter gilt nur für die **wspioctl** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="fa446-147">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="fa446-148">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fa446-148">Return value</span></span>

<span data-ttu-id="fa446-149">Wenn der Vorgang erfolgreich abgeschlossen wird, gibt die [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) -oder **wspioctl** -Funktion NULL zurück.</span><span class="sxs-lookup"><span data-stu-id="fa446-149">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="fa446-150">Wenn der Vorgang fehlschlägt oder aussteht, gibt die Funktion [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) oder **wspioctl** einen **\_ Socketfehler** zurück.</span><span class="sxs-lookup"><span data-stu-id="fa446-150">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="fa446-151">Um erweiterte Fehlerinformationen abzurufen, nennen Sie [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="fa446-151">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="fa446-152">Fehlercode</span><span class="sxs-lookup"><span data-stu-id="fa446-152">Error code</span></span> | <span data-ttu-id="fa446-153">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="fa446-153">Meaning</span></span> |
|------------|---------|
| <span data-ttu-id="fa446-154">**ausstehende WSA-e/a \_ \_**</span><span class="sxs-lookup"><span data-stu-id="fa446-154">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="fa446-155">Überlappende e/a-Vorgänge werden ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fa446-155">Overlapped I/O operation is in progress.</span></span> <span data-ttu-id="fa446-156">Dieser Wert wird zurückgegeben, wenn ein überlappende Vorgang erfolgreich initiiert wurde und die Beendigung zu einem späteren Zeitpunkt angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="fa446-156">This value is returned if an overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="fa446-157">**WSA- \_ Vorgang \_ abgebrochen**</span><span class="sxs-lookup"><span data-stu-id="fa446-157">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="fa446-158">Der e/a-Vorgang wurde aufgrund eines Thread Beendigungs-oder einer Anwendungsanforderung abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="fa446-158">The I/O operation has been aborted because of either a thread exit or an application request.</span></span> <span data-ttu-id="fa446-159">Dieser Fehler wird zurückgegeben, wenn ein über Lapp ender Vorgang aufgrund der Schließung des Sockets oder der Ausführung des Befehls " **SIO \_ Flush** ioctl" abgebrochen wurde.</span><span class="sxs-lookup"><span data-stu-id="fa446-159">This error is returned if an overlapped operation was canceled due to the closure of the socket or the execution of the **SIO\_FLUSH** IOCTL command.</span></span> |
| <span data-ttu-id="fa446-160">**WSAEACCES**</span><span class="sxs-lookup"><span data-stu-id="fa446-160">**WSAEACCES**</span></span> | <span data-ttu-id="fa446-161">Es wurde versucht, auf einen Socket auf eine Weise zuzugreifen, die durch seine Zugriffsberechtigungen unzulässig ist.</span><span class="sxs-lookup"><span data-stu-id="fa446-161">An attempt was made to access a socket in a way forbidden by its access permissions.</span></span> <span data-ttu-id="fa446-162">Dieser Fehler wird unter mehreren Bedingungen zurückgegeben, die Folgendes umfassen: dem Benutzer fehlen die erforderlichen Administratorrechte auf dem lokalen Computer, oder die Anwendung wird nicht in einer erweiterten Shell als integrierter Administrator () ausgeführt `RunAs administrator` .</span><span class="sxs-lookup"><span data-stu-id="fa446-162">This error is returned under several conditions that include the following: the user lacks the required administrative privileges on the local computer or the application is not running in an enhanced shell as the built-in Administrator (`RunAs administrator`).</span></span> |
| <span data-ttu-id="fa446-163">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="fa446-163">**WSAEFAULT**</span></span> | <span data-ttu-id="fa446-164">Das System hat bei dem Versuch, ein Zeigerargument in einem-Befehl zu verwenden, eine ungültige Zeiger Adresse erkannt.</span><span class="sxs-lookup"><span data-stu-id="fa446-164">The system detected an invalid pointer address in attempting to use a pointer argument in a call.</span></span> <span data-ttu-id="fa446-165">Dieser Fehler wird zurückgegeben, wenn der Parameter *lpvinbuffer*, *lpvoutbuffer*, *lpcbbytesall*, *lpoverlgetauscht* oder *lpCompletionRoutine* nicht vollständig in einem gültigen Teil des Benutzer Adressraums enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="fa446-165">This error is returned of the *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="fa446-166">**Wsaeingabe Progress**</span><span class="sxs-lookup"><span data-stu-id="fa446-166">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="fa446-167">Ein Blockierungsvorgang wird momentan ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fa446-167">A blocking operation is currently executing.</span></span> <span data-ttu-id="fa446-168">Dieser Fehler wird zurückgegeben, wenn die Funktion aufgerufen wird, wenn ein Rückruf ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fa446-168">This error is returned if the function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="fa446-169">**Wsaeingabe**</span><span class="sxs-lookup"><span data-stu-id="fa446-169">**WSAEINTR**</span></span> | <span data-ttu-id="fa446-170">Ein Blockierungs Vorgang wurde durch einen *wsacancelblockingstatement*-Aufrufvorgang unterbrochen.</span><span class="sxs-lookup"><span data-stu-id="fa446-170">A blocking operation was interrupted by a call to *WSACancelBlockingCall*.</span></span> <span data-ttu-id="fa446-171">Dieser Fehler wird zurückgegeben, wenn ein Blockierungs Vorgang unterbrochen wurde.</span><span class="sxs-lookup"><span data-stu-id="fa446-171">This error is returned if a blocking operation was interrupted.</span></span> |
| <span data-ttu-id="fa446-172">**Wsaabval**</span><span class="sxs-lookup"><span data-stu-id="fa446-172">**WSAEINVAL**</span></span> | <span data-ttu-id="fa446-173">Ein ungültiges Argument wurde angegeben.</span><span class="sxs-lookup"><span data-stu-id="fa446-173">An invalid argument was supplied.</span></span> <span data-ttu-id="fa446-174">Dieser Fehler wird zurückgegeben, wenn der *dwIoControlCode* -Parameter kein gültiger Befehl ist oder wenn ein angegebener Eingabeparameter nicht zulässig ist oder der Befehl nicht auf den angegebenen Sockettyp anwendbar ist.</span><span class="sxs-lookup"><span data-stu-id="fa446-174">This error is returned if the *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> |
| <span data-ttu-id="fa446-175">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="fa446-175">**WSAENETDOWN**</span></span> | <span data-ttu-id="fa446-176">Bei einem Socketvorgang war das Netzwerk inaktiv.</span><span class="sxs-lookup"><span data-stu-id="fa446-176">A socket operation encountered a dead network.</span></span> <span data-ttu-id="fa446-177">Dieser Fehler wird zurückgegeben, wenn das Netzwerk Subsystem fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="fa446-177">This error is returned if the network subsystem has failed.</span></span> |
| <span data-ttu-id="fa446-178">**Wsaumotsock**</span><span class="sxs-lookup"><span data-stu-id="fa446-178">**WSAENOTSOCK**</span></span> | <span data-ttu-id="fa446-179">Es wurde versucht, einen Vorgang für etwas auszuführen, das kein Socket ist.</span><span class="sxs-lookup"><span data-stu-id="fa446-179">An operation was attempted on something that is not a socket.</span></span> <span data-ttu-id="fa446-180">Dieser Fehler wird zurückgegeben, wenn es sich bei den Deskriptoren nicht um einen Socket handelt.</span><span class="sxs-lookup"><span data-stu-id="fa446-180">This error is returned if the descriptor s is not a socket.</span></span> |
| <span data-ttu-id="fa446-181">**WSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="fa446-181">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="fa446-182">Der versuchte Vorgang wird für den Typ des Objekts, auf das verwiesen wird, nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="fa446-182">The attempted operation is not supported for the type of object referenced.</span></span> <span data-ttu-id="fa446-183">Dieser Fehler wird zurückgegeben, wenn der angegebene ioctl-Befehl nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="fa446-183">This error is returned if the specified IOCTL command is not supported.</span></span> <span data-ttu-id="fa446-184">Dieser Fehler wird auch zurückgegeben, wenn der **SIO_TCP_INITIAL_RTO** ioctl vom Transportanbieter nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="fa446-184">This error is also returned if the **SIO_TCP_INITIAL_RTO** IOCTL is not supported by the transport provider.</span></span> |

## <a name="remarks"></a><span data-ttu-id="fa446-185">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fa446-185">Remarks</span></span>

<span data-ttu-id="fa446-186">Eine Anwendung kann die **SIO_TCP_INITIAL_RTO** ioctl verwenden, um die anfänglichen Neuübertragungs-Eigenschaften (SYN/SYN + ACK) eines TCP-Sockets bei Bedarf zu steuern.</span><span class="sxs-lookup"><span data-stu-id="fa446-186">An application can use the **SIO_TCP_INITIAL_RTO** IOCTL to control the initial (SYN / SYN+ACK) retransmission characteristics of a TCP socket if required.</span></span>
<span data-ttu-id="fa446-187">Eine Anwendung muss, wenn diese Option verwendet wird, geeignete Werte bereitstellen, bevor ein TCP-Verbindungsversuch für den Socket gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="fa446-187">An application, if using this option, must supply suitable values before starting a TCP connection attempt on the socket.</span></span>

<span data-ttu-id="fa446-188">Der [**TCP_INITIAL_RTO_PARAMETERS**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_initial_rto_parameters) ioctl ermöglicht es einer Anwendung, das anfängliche (SYN) Neuübertragungs Timeout (RTO) zu konfigurieren, das vom Socket verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fa446-188">The [**TCP_INITIAL_RTO_PARAMETERS**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_initial_rto_parameters) IOCTL allows an application to configure the initial (SYN) retransmission timeout (RTO) used by the socket.</span></span>

<span data-ttu-id="fa446-189">Ein Zeiger auf eine [**TCP_INITIAL_RTO_PARAMETERS**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_initial_rto_parameters) Struktur, die im *lpvinbuffer* -Parameter übergeben wird, ermöglicht es einer Anwendung, die anfängliche Roundtripzeit (RTT) zu konfigurieren, die zum Berechnen des Neuübertragungs Timeouts verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fa446-189">A pointer to a [**TCP_INITIAL_RTO_PARAMETERS**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_initial_rto_parameters) structure passed in the *lpvInBuffer* parameter allows an application to configure the initial round trip time (RTT) used to compute the retransmission timeout.</span></span>
<span data-ttu-id="fa446-190">Die Anwendung kann auch die Anzahl der erneuten Übertragungen konfigurieren, die versucht werden, bevor der Verbindungsversuch fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="fa446-190">The application can also configure the number of retransmissions that will be attempted before the connection attempt fails.</span></span>

## <a name="see-also"></a><span data-ttu-id="fa446-191">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fa446-191">See also</span></span>

[<span data-ttu-id="fa446-192">Glühbirne</span><span class="sxs-lookup"><span data-stu-id="fa446-192">socket</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="fa446-193">**TCP_INITIAL_RTO_PARAMETERS**</span><span class="sxs-lookup"><span data-stu-id="fa446-193">**TCP_INITIAL_RTO_PARAMETERS**</span></span>](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_initial_rto_parameters)

[<span data-ttu-id="fa446-194">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="fa446-194">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[<span data-ttu-id="fa446-195">**Wsagein verlappedresult**</span><span class="sxs-lookup"><span data-stu-id="fa446-195">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="fa446-196">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="fa446-196">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="fa446-197">**Wsaoverlgetauscht**</span><span class="sxs-lookup"><span data-stu-id="fa446-197">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="fa446-198">**Wsasocketa**</span><span class="sxs-lookup"><span data-stu-id="fa446-198">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="fa446-199">**Wsasocketw**</span><span class="sxs-lookup"><span data-stu-id="fa446-199">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
