---
description: Steuerungs Code gibt eine Lauf Zeit Reservierung für einen Block von TCP-oder UDP-Ports frei.
ms.assetid: 24D67A40-8CE9-4AF1-90BF-599D19C87B89
title: SIO_RELEASE_PORT_RESERVATION Steuerungs Codes
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 57f96d0396d661eba12f9e64238c492f38e97b2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347072"
---
# <a name="sio_release_port_reservation-control-code"></a><span data-ttu-id="e3d3e-103">SIO_RELEASE_PORT_RESERVATION Steuerungs Codes</span><span class="sxs-lookup"><span data-stu-id="e3d3e-103">SIO_RELEASE_PORT_RESERVATION Control Code</span></span>

## <a name="description"></a><span data-ttu-id="e3d3e-104">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e3d3e-104">Description</span></span>

<span data-ttu-id="e3d3e-105">Der Konfigurations Code für die **\_ Port- \_ \_ Reservierungs** Steuerung von SIO gibt eine Lauf Zeit Reservierung für einen Block von TCP-oder UDP-Ports frei.</span><span class="sxs-lookup"><span data-stu-id="e3d3e-105">The **SIO\_RELEASE\_PORT\_RESERVATION** control code releases a runtime reservation for a block of TCP or UDP ports.</span></span>
<span data-ttu-id="e3d3e-106">Die zu veröffentlichende Lauf Zeit Reservierung muss vom ausstellenden Prozess mithilfe der IOCTL- [**SIO_ACQUIRE_PORT_RESERVATION**](sio-acquire-port-reservation.md) abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="e3d3e-106">The runtime reservation to be released must have been obtained from the issuing process using the [**SIO_ACQUIRE_PORT_RESERVATION**](sio-acquire-port-reservation.md) IOCTL.</span></span>

<span data-ttu-id="e3d3e-107">Um diesen Vorgang auszuführen, wenden Sie die [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) -oder **wspioctl** -Funktion mit den folgenden Parametern an.</span><span class="sxs-lookup"><span data-stu-id="e3d3e-107">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_RELEASE_PORT_RESERVATION, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to a INET_PORT_RESERVATION_TOKEN structure
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  NULL,           // lpvOutBuffer is a pointer to the output buffer
  0,              // cbOutBuffer is the size, in bytes, of the output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);

```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_RELEASE_PORT_RESERVATION, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to a INET_PORT_RESERVATION_TOKEN structure
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  NULL,           // lpvOutBuffer is a pointer to the output buffer
  0,              // cbOutBuffer is the size, in bytes, of the output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,   // a WSATHREADID structure
  (LPINT) lpErrno   // a pointer to the error code.
);
```

## <a name="parameters"></a><span data-ttu-id="e3d3e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e3d3e-108">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="e3d3e-109">s</span><span class="sxs-lookup"><span data-stu-id="e3d3e-109">s</span></span>

<span data-ttu-id="e3d3e-110">Ein Deskriptor, der einen Socket identifiziert.</span><span class="sxs-lookup"><span data-stu-id="e3d3e-110">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="e3d3e-111">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="e3d3e-111">dwIoControlCode</span></span>

<span data-ttu-id="e3d3e-112">Der Steuerelement Code für den Vorgang.</span><span class="sxs-lookup"><span data-stu-id="e3d3e-112">The control code for the operation.</span></span>
<span data-ttu-id="e3d3e-113">Verwenden Sie für diesen Vorgang die **\_ \_ Port \_ Reservierung** für den SIO-Release.</span><span class="sxs-lookup"><span data-stu-id="e3d3e-113">Use **SIO\_RELEASE\_PORT\_RESERVATION** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="e3d3e-114">lpvinbuffer</span><span class="sxs-lookup"><span data-stu-id="e3d3e-114">lpvInBuffer</span></span>

<span data-ttu-id="e3d3e-115">Ein Zeiger auf den Eingabepuffer.</span><span class="sxs-lookup"><span data-stu-id="e3d3e-115">A pointer to the input buffer.</span></span>
<span data-ttu-id="e3d3e-116">Dieser Parameter enthält einen Zeiger auf eine [**INET_PORT_RESERVATION_TOKEN**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_token) Struktur mit dem Token für die zu veröffentlichende TCP-oder UDP-Port Reservierung.</span><span class="sxs-lookup"><span data-stu-id="e3d3e-116">This parameter contains a pointer to an [**INET_PORT_RESERVATION_TOKEN**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_token) structure with the token for the TCP or UDP port reservation to release.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="e3d3e-117">cbinbuffer</span><span class="sxs-lookup"><span data-stu-id="e3d3e-117">cbInBuffer</span></span>

<span data-ttu-id="e3d3e-118">Die Größe des Eingabe Puffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="e3d3e-118">The size, in bytes, of the input buffer.</span></span>
<span data-ttu-id="e3d3e-119">Dieser Parameter muss mindestens die Größe der [**INET_PORT_RESERVATION_TOKEN**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_token) Struktur aufweisen.</span><span class="sxs-lookup"><span data-stu-id="e3d3e-119">This parameter must be at least the size of the [**INET_PORT_RESERVATION_TOKEN**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_token) structure.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="e3d3e-120">lpvoutbuffer</span><span class="sxs-lookup"><span data-stu-id="e3d3e-120">lpvOutBuffer</span></span>

<span data-ttu-id="e3d3e-121">Ein Zeiger auf den Ausgabepuffer.</span><span class="sxs-lookup"><span data-stu-id="e3d3e-121">A pointer to the output buffer.</span></span>
<span data-ttu-id="e3d3e-122">Dieser Parameter wird für diesen Vorgang nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="e3d3e-122">This parameter is unused for this operation.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="e3d3e-123">cboutbuffer</span><span class="sxs-lookup"><span data-stu-id="e3d3e-123">cbOutBuffer</span></span>

<span data-ttu-id="e3d3e-124">Die Größe des Ausgabepuffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="e3d3e-124">The size, in bytes, of the output buffer.</span></span>
<span data-ttu-id="e3d3e-125">Dieser Parameter muss auf 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="e3d3e-125">This parameter must be set to zero.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="e3d3e-126">lpcbbyteszurück gegeben</span><span class="sxs-lookup"><span data-stu-id="e3d3e-126">lpcbBytesReturned</span></span>

<span data-ttu-id="e3d3e-127">Ein Zeiger auf eine Variable, die die Größe der im Ausgabepuffer gespeicherten Daten (in Bytes) empfängt.</span><span class="sxs-lookup"><span data-stu-id="e3d3e-127">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>

<span data-ttu-id="e3d3e-128">Wenn der Ausgabepuffer zu klein ist, schlägt der-Befehl fehl, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) gibt [**WSAEINVAL**](windows-sockets-error-codes-2.md)zurück, und der *lpcbbytesreturns* -Parameter verweist auf den **DWORD** -Wert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="e3d3e-128">If the output buffer is too small, the call fails, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns [**WSAEINVAL**](windows-sockets-error-codes-2.md), and the *lpcbBytesReturned* parameter points to a **DWORD** value of zero.</span></span>

<span data-ttu-id="e3d3e-129">Wenn *lpoverlgetauscht* gleich **null** ist, kann der **DWORD** -Wert, auf den der *lpcbbytesall* -Parameter verweist, der bei einem erfolgreichen-Vorgang zurückgegeben wird, nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="e3d3e-129">If *lpOverlapped* is **NULL**, the **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned on a successful call cannot be zero.</span></span>

<span data-ttu-id="e3d3e-130">Wenn der *lpoverllapp* -Parameter für überlappende Sockets nicht **null** ist, werden Vorgänge, die nicht sofort abgeschlossen werden können, initiiert, und der Abschluss wird zu einem späteren Zeitpunkt angegeben.</span><span class="sxs-lookup"><span data-stu-id="e3d3e-130">If the *lpOverlapped* parameter is not **NULL** for overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>
<span data-ttu-id="e3d3e-131">Der **DWORD** -Wert, auf den der zurückgegebene *lpcbbyteszurück gegebene* Parameter verweist, kann NULL sein, da die Größe der gespeicherten Daten erst bestimmt werden kann, wenn der überlappende Vorgang abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="e3d3e-131">The **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned may be zero since the size of the data stored can't be determined until the overlapped operation has completed.</span></span>
<span data-ttu-id="e3d3e-132">Der endgültige Abschluss Status kann abgerufen werden, wenn die geeignete Vervollständigungs Methode signalisiert wird, wenn der Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="e3d3e-132">The final completion status can be retrieved when the appropriate completion method is signaled when the operation has completed.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="e3d3e-133">lpvoverlgetauscht</span><span class="sxs-lookup"><span data-stu-id="e3d3e-133">lpvOverlapped</span></span>

<span data-ttu-id="e3d3e-134">Ein Zeiger auf eine [**wsaoverllapp**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="e3d3e-134">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="e3d3e-135">Wenn Socket *s* ohne das überlappende Attribut erstellt wurde, wird der *lpoverllapp* -Parameter ignoriert.</span><span class="sxs-lookup"><span data-stu-id="e3d3e-135">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="e3d3e-136">Wenn *s* mit dem überlappenden Attribut geöffnet wurde und der *lpoverlgetauscht* -Parameter nicht **null** ist, wird der Vorgang als überlappende (asynchrone) Operation ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e3d3e-136">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="e3d3e-137">In diesem Fall muss der *lpoverllapp* -Parameter auf eine gültige [**wsaoverllapp**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) -Struktur zeigen.</span><span class="sxs-lookup"><span data-stu-id="e3d3e-137">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="e3d3e-138">Bei überlappenden Vorgängen gibt die Funktion [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) oder **wspioctl** sofort zurück, und die entsprechende Vervollständigungs Methode wird signalisiert, wenn der Vorgang abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="e3d3e-138">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="e3d3e-139">Andernfalls gibt die Funktion nicht zurück, bis der Vorgang abgeschlossen ist oder ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="e3d3e-139">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="e3d3e-140">lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="e3d3e-140">lpCompletionRoutine</span></span>

<span data-ttu-id="e3d3e-141">Typ: \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="e3d3e-141">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="e3d3e-142">Ein Zeiger auf die Vervollständigungs Routine, die aufgerufen wird, wenn der Vorgang abgeschlossen wurde (bei nicht überlappenden Sockets ignoriert).</span><span class="sxs-lookup"><span data-stu-id="e3d3e-142">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="e3d3e-143">lpthreadid</span><span class="sxs-lookup"><span data-stu-id="e3d3e-143">lpThreadId</span></span>

<span data-ttu-id="e3d3e-144">Ein Zeiger auf eine [**wsathreadid**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) -Struktur, die vom Anbieter in einem nachfolgenden [**wpuqueueapc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc)-Rückruf verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e3d3e-144">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="e3d3e-145">Der Anbieter sollte die referenzierte [**wsathreadid**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) -Struktur (nicht den Zeiger auf dieselbe) speichern, bis die [**wpuqueueapc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) -Funktion zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="e3d3e-145">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="e3d3e-146">**Hinweis**  Dieser Parameter gilt nur für die **wspioctl** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="e3d3e-146">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="e3d3e-147">lperrno</span><span class="sxs-lookup"><span data-stu-id="e3d3e-147">lpErrno</span></span>

<span data-ttu-id="e3d3e-148">Ein Zeiger auf den Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="e3d3e-148">A pointer to the error code.</span></span>

<span data-ttu-id="e3d3e-149">**Hinweis**  Dieser Parameter gilt nur für die **wspioctl** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="e3d3e-149">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="e3d3e-150">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e3d3e-150">Return value</span></span>

<span data-ttu-id="e3d3e-151">Wenn der Vorgang erfolgreich abgeschlossen wird, gibt die [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) -oder **wspioctl** -Funktion NULL zurück.</span><span class="sxs-lookup"><span data-stu-id="e3d3e-151">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="e3d3e-152">Wenn der Vorgang fehlschlägt oder aussteht, gibt die Funktion [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) oder **wspioctl** einen **\_ Socketfehler** zurück.</span><span class="sxs-lookup"><span data-stu-id="e3d3e-152">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="e3d3e-153">Um erweiterte Fehlerinformationen abzurufen, nennen Sie [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="e3d3e-153">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="e3d3e-154">Fehlercode</span><span class="sxs-lookup"><span data-stu-id="e3d3e-154">Error code</span></span> | <span data-ttu-id="e3d3e-155">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="e3d3e-155">Meaning</span></span> |
|------------|---------|
| <span data-ttu-id="e3d3e-156">**ausstehende WSA-e/a \_ \_**</span><span class="sxs-lookup"><span data-stu-id="e3d3e-156">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="e3d3e-157">Überlappende e/a-Vorgänge werden ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e3d3e-157">Overlapped I/O operation is in progress.</span></span> <span data-ttu-id="e3d3e-158">Dieser Wert wird zurückgegeben, wenn ein überlappende Vorgang erfolgreich initiiert wurde und die Beendigung zu einem späteren Zeitpunkt angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="e3d3e-158">This value is returned if an overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="e3d3e-159">**WSA- \_ Vorgang \_ abgebrochen**</span><span class="sxs-lookup"><span data-stu-id="e3d3e-159">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="e3d3e-160">Der e/a-Vorgang wurde aufgrund eines Thread Beendigungs-oder einer Anwendungsanforderung abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="e3d3e-160">The I/O operation has been aborted because of either a thread exit or an application request.</span></span> <span data-ttu-id="e3d3e-161">Dieser Fehler wird zurückgegeben, wenn ein über Lapp ender Vorgang aufgrund der Schließung des Sockets oder der Ausführung des **SIO_FLUSH** ioctl-Befehls abgebrochen wurde.</span><span class="sxs-lookup"><span data-stu-id="e3d3e-161">This error is returned if an overlapped operation was canceled due to the closure of the socket or the execution of the **SIO_FLUSH** IOCTL command.</span></span> |
| <span data-ttu-id="e3d3e-162">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="e3d3e-162">**WSAEFAULT**</span></span> | <span data-ttu-id="e3d3e-163">Das System hat bei dem Versuch, ein Zeigerargument in einem-Befehl zu verwenden, eine ungültige Zeiger Adresse erkannt.</span><span class="sxs-lookup"><span data-stu-id="e3d3e-163">The system detected an invalid pointer address in attempting to use a pointer argument in a call.</span></span> <span data-ttu-id="e3d3e-164">Dieser Fehler wird zurückgegeben, wenn der *lpoverlgetauscht* -oder *lpCompletionRoutine* -Parameter nicht vollständig in einem gültigen Teil des Benutzer Adressraums enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="e3d3e-164">This error is returned of the *lpOverlapped* or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="e3d3e-165">**Wsaeingabe Progress**</span><span class="sxs-lookup"><span data-stu-id="e3d3e-165">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="e3d3e-166">Ein Blockierungsvorgang wird momentan ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e3d3e-166">A blocking operation is currently executing.</span></span> <span data-ttu-id="e3d3e-167">Dieser Fehler wird zurückgegeben, wenn die Funktion aufgerufen wird, wenn ein Rückruf ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e3d3e-167">This error is returned if the function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="e3d3e-168">**Wsaeingabe**</span><span class="sxs-lookup"><span data-stu-id="e3d3e-168">**WSAEINTR**</span></span> | <span data-ttu-id="e3d3e-169">Ein Blockierungs Vorgang wurde durch einen **wsacancelblockingstatement**-Aufrufvorgang unterbrochen.</span><span class="sxs-lookup"><span data-stu-id="e3d3e-169">A blocking operation was interrupted by a call to **WSACancelBlockingCall**.</span></span> <span data-ttu-id="e3d3e-170">Dieser Fehler wird zurückgegeben, wenn ein Blockierungs Vorgang unterbrochen wurde.</span><span class="sxs-lookup"><span data-stu-id="e3d3e-170">This error is returned if a blocking operation was interrupted.</span></span> |
| <span data-ttu-id="e3d3e-171">**Wsaabval**</span><span class="sxs-lookup"><span data-stu-id="e3d3e-171">**WSAEINVAL**</span></span> | <span data-ttu-id="e3d3e-172">Ein ungültiges Argument wurde angegeben.</span><span class="sxs-lookup"><span data-stu-id="e3d3e-172">An invalid argument was supplied.</span></span> <span data-ttu-id="e3d3e-173">Dieser Fehler wird zurückgegeben, wenn der *dwIoControlCode* -Parameter kein gültiger Befehl ist oder wenn ein angegebener Eingabeparameter nicht zulässig ist oder der Befehl nicht auf den angegebenen Sockettyp anwendbar ist.</span><span class="sxs-lookup"><span data-stu-id="e3d3e-173">This error is returned if the *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> |
| <span data-ttu-id="e3d3e-174">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="e3d3e-174">**WSAENETDOWN**</span></span> | <span data-ttu-id="e3d3e-175">Bei einem Socketvorgang war das Netzwerk inaktiv.</span><span class="sxs-lookup"><span data-stu-id="e3d3e-175">A socket operation encountered a dead network.</span></span> <span data-ttu-id="e3d3e-176">Dieser Fehler wird zurückgegeben, wenn das Netzwerk Subsystem fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="e3d3e-176">This error is returned if the network subsystem has failed.</span></span> |
| <span data-ttu-id="e3d3e-177">**Wsaumotsock**</span><span class="sxs-lookup"><span data-stu-id="e3d3e-177">**WSAENOTSOCK**</span></span> | <span data-ttu-id="e3d3e-178">Es wurde versucht, einen Vorgang für etwas auszuführen, das kein Socket ist.</span><span class="sxs-lookup"><span data-stu-id="e3d3e-178">An operation was attempted on something that is not a socket.</span></span> <span data-ttu-id="e3d3e-179">Dieser Fehler wird zurückgegeben, wenn es sich bei den *Deskriptoren nicht* um einen Socket handelt.</span><span class="sxs-lookup"><span data-stu-id="e3d3e-179">This error is returned if the descriptor *s* is not a socket.</span></span> |
| <span data-ttu-id="e3d3e-180">**WSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="e3d3e-180">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="e3d3e-181">Der versuchte Vorgang wird für den Typ des Objekts, auf das verwiesen wird, nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e3d3e-181">The attempted operation is not supported for the type of object referenced.</span></span> <span data-ttu-id="e3d3e-182">Dieser Fehler wird zurückgegeben, wenn der angegebene ioctl-Befehl nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="e3d3e-182">This error is returned if the specified IOCTL command is not supported.</span></span> <span data-ttu-id="e3d3e-183">Dieser Fehler wird auch zurückgegeben, wenn die IOCTL-ioctl des Zertifikat- **\_ \_ \_ releaseports** nicht vom Transportanbieter unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="e3d3e-183">This error is also returned if the **SIO\_RELEASE\_PORT\_RESERVATION** IOCTL is not supported by the transport provider.</span></span> <span data-ttu-id="e3d3e-184">Dieser Fehler wird auch zurückgegeben, wenn bei dem Versuch, die IOCTL-ioctl der Zertifikat- **\_ \_ \_ Releaseversion** zu verwenden, ein anderes als UDP oder TCP verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e3d3e-184">This error is also returned when an attempt to use the **SIO\_RELEASE\_PORT\_RESERVATION** IOCTL is made on a socket other than UDP or TCP.</span></span> |

## <a name="remarks"></a><span data-ttu-id="e3d3e-185">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e3d3e-185">Remarks</span></span>

<span data-ttu-id="e3d3e-186">Die IOCTL-ioctl der Zertifikat- **\_ \_ releaseport \_ Reservierung** wird unter Windows Vista und höheren Versionen des Betriebssystems unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e3d3e-186">The **SIO\_RELEASE\_PORT\_RESERVATION** IOCTL is supported on Windows Vista and later versions of the operating system.</span></span>

<span data-ttu-id="e3d3e-187">Anwendungen und Dienste, die Ports reservieren müssen, lassen sich in zwei Kategorien unterteilen.</span><span class="sxs-lookup"><span data-stu-id="e3d3e-187">Applications and services which need to reserve ports fall into two categories.</span></span>
<span data-ttu-id="e3d3e-188">Die erste Kategorie umfasst Komponenten, die einen bestimmten Port als Teil Ihres Vorgangs benötigen.</span><span class="sxs-lookup"><span data-stu-id="e3d3e-188">The first category includes components which need a particular port as part of their operation.</span></span>
<span data-ttu-id="e3d3e-189">Diese Komponenten bevorzugen in der Regel die Angabe Ihres erforderlichen Ports zur Installationszeit (z. b. in einem Anwendungs Manifest).</span><span class="sxs-lookup"><span data-stu-id="e3d3e-189">Such components will generally prefer to specify their required port at installation time (in an application manifest, for example).</span></span>
<span data-ttu-id="e3d3e-190">Die zweite Kategorie umfasst Komponenten, die zur Laufzeit einen beliebigen verfügbaren Port oder einen beliebigen Port Block benötigen.</span><span class="sxs-lookup"><span data-stu-id="e3d3e-190">The second category includes components which need any available port or block of ports at runtime.</span></span>
<span data-ttu-id="e3d3e-191">Diese beiden Kategorien entsprechen bestimmten Port Reservierungs Anforderungen für und Platzhalter.</span><span class="sxs-lookup"><span data-stu-id="e3d3e-191">These two categories correspond to specific and wildcard port reservation requests.</span></span>
<span data-ttu-id="e3d3e-192">Bestimmte Reservierungs Anforderungen sind möglicherweise persistent oder Laufzeit, während reservierte Port Reservierungs Anforderungen nur zur Laufzeit unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="e3d3e-192">Specific reservation requests may be persistent or runtime, while wildcard port reservation requests are only supported at runtime.</span></span>

<span data-ttu-id="e3d3e-193">Der [**SIO_ACQUIRE_PORT_RESERVATION**](sio-acquire-port-reservation.md) IOCTL wird verwendet, um eine Lauf Zeit Reservierung für einen Block von TCP-oder UDP-Ports anzufordern.</span><span class="sxs-lookup"><span data-stu-id="e3d3e-193">The [**SIO_ACQUIRE_PORT_RESERVATION**](sio-acquire-port-reservation.md) IOCTL is used to request a runtime reservation for a block of TCP or UDP ports.</span></span>
<span data-ttu-id="e3d3e-194">Bei Lauf Zeit Port Reservierungen erfordert der Port Pool, dass Reservierungen von dem Prozess verarbeitet werden, dessen Socket die Reservierung gewährt wurde.</span><span class="sxs-lookup"><span data-stu-id="e3d3e-194">For runtime port reservations, the port pool requires that reservations be consumed from the process on whose socket the reservation was granted.</span></span>
<span data-ttu-id="e3d3e-195">Lauf Zeit Port Reservierungen dauern nur so lange, wie die Lebensdauer des Sockets, auf dem die [**SIO_ACQUIRE_PORT_RESERVATION**](sio-acquire-port-reservation.md) ioctl aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="e3d3e-195">Runtime port reservations last only as long as the lifetime of the socket on which the [**SIO_ACQUIRE_PORT_RESERVATION**](sio-acquire-port-reservation.md) IOCTL was called.</span></span>
<span data-ttu-id="e3d3e-196">Im Gegensatz dazu können persistente Port Reservierungen, die mithilfe der Funktion " [**kreatepersistenttcpportreservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation) " oder " [**kreatepersistentudpportreservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation) " erstellt wurden, von jedem Prozess genutzt werden, der über die Möglichkeit zum Abrufen dauerhafter Reservierungen verfügt.</span><span class="sxs-lookup"><span data-stu-id="e3d3e-196">In contrast, persistent port reservations created using the [**CreatePersistentTcpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation) or [**CreatePersistentUdpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation) function may be consumed by any process with the ability to obtain persistent reservations.</span></span>

<span data-ttu-id="e3d3e-197">Mithilfe der IOCTL-ioctl-Version für die **\_ \_ Port \_ Reservierung** wird eine Lauf Zeit Reservierung für einen Block von TCP-oder UDP-Ports freigegeben.</span><span class="sxs-lookup"><span data-stu-id="e3d3e-197">The **SIO\_RELEASE\_PORT\_RESERVATION** IOCTL is used to release a runtime reservation for a block of TCP or UDP ports.</span></span>

<span data-ttu-id="e3d3e-198">Wenn die Parameter *lpoverlgetauscht* und *lpCompletionRoutine* **null** sind, wird der Socket in dieser Funktion als nicht überlappenden Socket behandelt.</span><span class="sxs-lookup"><span data-stu-id="e3d3e-198">If both *lpOverlapped* and *lpCompletionRoutine* parameters are **NULL**, the socket in this function will be treated as a non-overlapped socket.</span></span>
<span data-ttu-id="e3d3e-199">Bei einem nicht überlappenden Socket werden die Parameter *lpoverlgetauscht* und *lpCompletionRoutine* ignoriert, mit der Ausnahme, dass die Funktion blockiert werden kann, wenn sich Socket *s* im Blockierungs Modus befindet.</span><span class="sxs-lookup"><span data-stu-id="e3d3e-199">For a non-overlapped socket, *lpOverlapped* and *lpCompletionRoutine* parameters are ignored, except that the function can block if socket *s* is in blocking mode.</span></span>
<span data-ttu-id="e3d3e-200">Wenn sich Socket *s* im nicht blockierenden Modus befindet, wird diese Funktion immer noch blockiert, da diese spezielle ioctl den nicht blockierenden Modus nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e3d3e-200">If socket *s* is in non-blocking mode, this function will still block since this particular IOCTL does not support non-blocking mode.</span></span>

<span data-ttu-id="e3d3e-201">Bei überlappenden Sockets werden Vorgänge, die nicht sofort abgeschlossen werden können, initiiert, und der Abschluss wird zu einem späteren Zeitpunkt angegeben.</span><span class="sxs-lookup"><span data-stu-id="e3d3e-201">For overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>

<span data-ttu-id="e3d3e-202">Alle ioctl können unbegrenzt blockieren, abhängig von der Implementierung des Dienstanbieters.</span><span class="sxs-lookup"><span data-stu-id="e3d3e-202">Any IOCTL may block indefinitely, depending on the service provider's implementation.</span></span>
<span data-ttu-id="e3d3e-203">Wenn die Anwendung die Blockierung in einem [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) -oder **wspioctl** -Funktions aufrufnis nicht tolerieren kann, werden überlappende e/a-Vorgänge für IOCTLs empfohlen, die besonders wahrscheinlich blockiert werden.</span><span class="sxs-lookup"><span data-stu-id="e3d3e-203">If the application cannot tolerate blocking in a [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function call, overlapped I/O would be advised for IOCTLs that are especially likely to block.</span></span>

<span data-ttu-id="e3d3e-204">In den folgenden Fällen kann bei der IOCTL für die RSA- **\_ \_ \_ releaseportreservierung** ein Fehler auftreten, wenn **WSAEINTR** oder **WSA \_ \_ abgebrochen** wurde:</span><span class="sxs-lookup"><span data-stu-id="e3d3e-204">The **SIO\_RELEASE\_PORT\_RESERVATION** IOCTL can fail with **WSAEINTR** or **WSA\_OPERATION\_ABORTED** under the following cases:</span></span>

* <span data-ttu-id="e3d3e-205">Die Anforderung wird vom e/a-Manager abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="e3d3e-205">The request is canceled by the I/O Manager.</span></span>
* <span data-ttu-id="e3d3e-206">Der Socket ist geschlossen.</span><span class="sxs-lookup"><span data-stu-id="e3d3e-206">The socket is closed.</span></span>

## <a name="examples"></a><span data-ttu-id="e3d3e-207">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e3d3e-207">Examples</span></span>

<span data-ttu-id="e3d3e-208">Im folgenden Beispiel wird eine Lauf Zeit Port Reservierung angefordert und dann die Lauf Zeit Port Reservierung freigegeben.</span><span class="sxs-lookup"><span data-stu-id="e3d3e-208">The following example acquires a runtime port reservation and then releases the runtime port reservation.</span></span>

```cpp
#ifndef UNICODE
#define UNICODE
#endif

#ifndef WIN32_LEAN_AND_MEAN
#define WIN32_LEAN_AND_MEAN
#endif

#include <Windows.h.>
#include <winsock2.h>
#include <mstcpip.h>
#include <ws2ipdef.h>
#include <stdio.h>
#include <stdlib.h>

// Need to link with Ws2_32.lib for Winsock functions
#pragma comment(lib, "ws2_32.lib")

int wmain(int argc, WCHAR ** argv)
{

    // Declare and initialize variables

    int startPort = 0;          // host byte order
    int numPorts = 0;
    USHORT startPortns = 0;     // Network byte order

    INET_PORT_RANGE portRange = { 0 };
    INET_PORT_RESERVATION_INSTANCE portRes = { 0 };

    unsigned long status = 0;

    WSADATA wsaData = { 0 };
    int iResult = 0;

    SOCKET sock = INVALID_SOCKET;
    int iFamily = AF_INET;
    int iType = 0;
    int iProtocol = 0;

    SOCKET sockRes = INVALID_SOCKET;

    DWORD bytesReturned = 0;

    // Validate the parameters
    if (argc != 6) {
        wprintf
            (L"usage: %s <addressfamily> <type> <protocol> <StartingPort> <NumberOfPorts>\n",
             argv[0]);
        wprintf(L"Opens a socket for the specified family, type, & protocol\n");
        wprintf
            (L"and then acquires a runtime port reservation for the protocol specified\n");
        wprintf(L"%ws example usage\n", argv[0]);
        wprintf(L"   %ws 2 2 17 5000 20\n", argv[0]);
        wprintf(L"   where AF_INET=2 SOCK_DGRAM=2 IPPROTO_UDP=17 StartPort=5000 NumPorts=20", argv[0]);

        return 1;
    }

    iFamily = _wtoi(argv[1]);
    iType = _wtoi(argv[2]);
    iProtocol = _wtoi(argv[3]);

    startPort = _wtoi(argv[4]);
    if (startPort < 0 || startPort > 65535) {
        wprintf(L"Starting point must be either 0 or between 1 and 65,535\n");
        return 1;
    }
    startPortns = htons((USHORT) startPort);

    numPorts = _wtoi(argv[5]);
    if (numPorts < 0) {
        wprintf(L"Number of ports must be a positive number\n");
        return 1;
    }

    portRange.StartPort = startPortns;
    portRange.NumberOfPorts = (USHORT) numPorts;

    // Initialize Winsock
    iResult = WSAStartup(MAKEWORD(2, 2), &wsaData);
    if (iResult != 0) {
        wprintf(L"WSAStartup failed with error = %d\n", iResult);
        return 1;
    }

    sock = socket(iFamily, iType, iProtocol);
    if (sock == INVALID_SOCKET) {
        wprintf(L"socket function failed with error = %d\n", WSAGetLastError());
        WSACleanup();
        return 1;
    } else {
        wprintf(L"socket function succeeded\n");

        iResult =
            WSAIoctl(sock, SIO_ACQUIRE_PORT_RESERVATION, (LPVOID) & portRange,
                     sizeof (INET_PORT_RANGE), (LPVOID) & portRes,
                     sizeof (INET_PORT_RESERVATION_INSTANCE), &bytesReturned, NULL, NULL);
        if (iResult != 0) {
            wprintf(L"WSAIoctl(SIO_ACQUIRE_PORT_RESERVATION) failed with error = %d\n",
                    WSAGetLastError());
            closesocket(sock);
            WSACleanup();
            return 1;
        } else {
            wprintf
                (L"WSAIoctl(SIO_ACQUIRE_PORT_RESERVATION) succeeded, bytesReturned = %u\n",
                 bytesReturned);
            wprintf(L"  Starting port=%d,  Number of Ports=%d, Token=%I64d\n",
                    htons(portRes.Reservation.StartPort),
                    portRes.Reservation.NumberOfPorts, portRes.Token);

            iResult =
                WSAIoctl(sock, SIO_RELEASE_PORT_RESERVATION, (LPVOID) & portRes.Token,
                         sizeof (ULONG64), NULL, 0, &bytesReturned, NULL, NULL);
            if (iResult != 0) {
                wprintf
                    (L"WSAIoctl(SIO_RELEASE_PORT_RESERVATION) failed with error = %d\n",
                     WSAGetLastError());
            } else {
                wprintf
                    (L"WSAIoctl(SIO_RELEASE_PORT_RESERVATION) succeeded, bytesReturned = %u\n",
                     bytesReturned);
            }
        }

        if (sock != INVALID_SOCKET) {
            iResult = closesocket(sock);
            if (iResult == SOCKET_ERROR) {
                wprintf(L"closesocket for first socket failed with error = %d\n",
                        WSAGetLastError());
            }
        }
    }

    WSACleanup();

    return 0;
}
```

## <a name="see-also"></a><span data-ttu-id="e3d3e-209">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e3d3e-209">See also</span></span>

[<span data-ttu-id="e3d3e-210">**"Kreatepersistenttcpportreservation"**</span><span class="sxs-lookup"><span data-stu-id="e3d3e-210">**CreatePersistentTcpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation)

[<span data-ttu-id="e3d3e-211">**"Kreatepersistentudpportreservation"**</span><span class="sxs-lookup"><span data-stu-id="e3d3e-211">**CreatePersistentUdpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation)

[<span data-ttu-id="e3d3e-212">**Deletepersistenttcpportreservation**</span><span class="sxs-lookup"><span data-stu-id="e3d3e-212">**DeletePersistentTcpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-deletepersistenttcpportreservation)

[<span data-ttu-id="e3d3e-213">**Deletepersistentudpportreservation**</span><span class="sxs-lookup"><span data-stu-id="e3d3e-213">**DeletePersistentUdpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-deletepersistentudpportreservation)

[<span data-ttu-id="e3d3e-214">**INET_PORT_RESERVATION_TOKEN**</span><span class="sxs-lookup"><span data-stu-id="e3d3e-214">**INET_PORT_RESERVATION_TOKEN**</span></span>](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_token)

[<span data-ttu-id="e3d3e-215">**Lookuppersistenttcpportreservation**</span><span class="sxs-lookup"><span data-stu-id="e3d3e-215">**LookupPersistentTcpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-lookuppersistenttcpportreservation)

[<span data-ttu-id="e3d3e-216">**Lookuppersistentudpportreservation**</span><span class="sxs-lookup"><span data-stu-id="e3d3e-216">**LookupPersistentUdpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-lookuppersistentudpportreservation)

[<span data-ttu-id="e3d3e-217">**SIO_ACQUIRE_PORT_RESERVATION**</span><span class="sxs-lookup"><span data-stu-id="e3d3e-217">**SIO_ACQUIRE_PORT_RESERVATION**</span></span>](sio-acquire-port-reservation.md)

[<span data-ttu-id="e3d3e-218">**SIO_ASSOCIATE_PORT_RESERVATION**</span><span class="sxs-lookup"><span data-stu-id="e3d3e-218">**SIO_ASSOCIATE_PORT_RESERVATION**</span></span>](sio-associate-port-reservation.md)

[<span data-ttu-id="e3d3e-219">Glühbirne</span><span class="sxs-lookup"><span data-stu-id="e3d3e-219">socket</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="e3d3e-220">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="e3d3e-220">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[<span data-ttu-id="e3d3e-221">**Wsagein verlappedresult**</span><span class="sxs-lookup"><span data-stu-id="e3d3e-221">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="e3d3e-222">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="e3d3e-222">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="e3d3e-223">**Wsaoverlgetauscht**</span><span class="sxs-lookup"><span data-stu-id="e3d3e-223">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="e3d3e-224">**Wsasocketa**</span><span class="sxs-lookup"><span data-stu-id="e3d3e-224">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="e3d3e-225">**Wsasocketw**</span><span class="sxs-lookup"><span data-stu-id="e3d3e-225">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
