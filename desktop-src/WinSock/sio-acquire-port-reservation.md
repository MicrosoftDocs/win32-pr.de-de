---
description: Der Steuerungs Code erhält eine Lauf Zeit Reservierung für einen Block von TCP-oder UDP-Ports.
ms.assetid: 1A2E3920-88D2-4109-B7EF-E66BD4AB6153
title: SIO_ACQUIRE_PORT_RESERVATION Steuerungs Codes
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 8eab53aeb945837b55c70560294b2fc295160a2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347917"
---
# <a name="sio_acquire_port_reservation-control-code"></a><span data-ttu-id="a01a1-103">SIO_ACQUIRE_PORT_RESERVATION Steuerungs Codes</span><span class="sxs-lookup"><span data-stu-id="a01a1-103">SIO_ACQUIRE_PORT_RESERVATION control code</span></span>

## <a name="description"></a><span data-ttu-id="a01a1-104">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a01a1-104">Description</span></span>

<span data-ttu-id="a01a1-105">Der Konfigurations Code für die **\_ Port- \_ \_ Reservierungs** Steuerung von SIO erhält eine Lauf Zeit Reservierung für einen Block von TCP-oder UDP-Ports.</span><span class="sxs-lookup"><span data-stu-id="a01a1-105">The **SIO\_ACQUIRE\_PORT\_RESERVATION** control code acquires a runtime reservation for a block of TCP or UDP ports.</span></span>

<span data-ttu-id="a01a1-106">Um diesen Vorgang auszuführen, wenden Sie die [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) -oder **wspioctl** -Funktion mit den folgenden Parametern an.</span><span class="sxs-lookup"><span data-stu-id="a01a1-106">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_ACQUIRE_PORT_RESERVATION, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to an INET_PORT_RANGE structure
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,             // pointer to an INET_PORT_RESERVATION_INSTANCE structure
  (DWORD) cbOutBuffer,   // size, in bytes, of the output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_ACQUIRE_PORT_RESERVATION, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to an INET_PORT_RANGE structure
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,             // pointer to a INET_PORT_RESERVATION_INSTANCE structure
  (DWORD) cbOutBuffer,   // size, in bytes, of the output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,   // a WSATHREADID structure
  (LPINT) lpErrno   // a pointer to the error code.
);
```

## <a name="parameters"></a><span data-ttu-id="a01a1-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="a01a1-107">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="a01a1-108">s</span><span class="sxs-lookup"><span data-stu-id="a01a1-108">s</span></span>

<span data-ttu-id="a01a1-109">Ein Deskriptor, der einen Socket identifiziert.</span><span class="sxs-lookup"><span data-stu-id="a01a1-109">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="a01a1-110">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="a01a1-110">dwIoControlCode</span></span>

<span data-ttu-id="a01a1-111">Der Steuerelement Code für den Vorgang.</span><span class="sxs-lookup"><span data-stu-id="a01a1-111">The control code for the operation.</span></span>
<span data-ttu-id="a01a1-112">Verwenden Sie für diesen Vorgang die **\_ \_ Port \_ Reservierung**  von "sio abrufen".</span><span class="sxs-lookup"><span data-stu-id="a01a1-112">Use **SIO\_ACQUIRE\_PORT\_RESERVATION**  for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="a01a1-113">lpvinbuffer</span><span class="sxs-lookup"><span data-stu-id="a01a1-113">lpvInBuffer</span></span>

<span data-ttu-id="a01a1-114">Ein Zeiger auf den Eingabepuffer.</span><span class="sxs-lookup"><span data-stu-id="a01a1-114">A pointer to the input buffer.</span></span>
<span data-ttu-id="a01a1-115">Dieser Parameter enthält einen Zeiger auf eine [**inet- \_ Port \_ Bereichs**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_range) Struktur, die die Startpunkt Nummer und die Anzahl der zu reservierenden Ports angibt.</span><span class="sxs-lookup"><span data-stu-id="a01a1-115">This parameter contains a pointer to an [**INET\_PORT\_RANGE**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_range) structure that specifies the starting point number and the number of ports to reserve.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="a01a1-116">cbinbuffer</span><span class="sxs-lookup"><span data-stu-id="a01a1-116">cbInBuffer</span></span>

<span data-ttu-id="a01a1-117">Die Größe des Eingabe Puffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="a01a1-117">The size, in bytes, of the input buffer.</span></span>
<span data-ttu-id="a01a1-118">Dieser Parameter sollte die Größe der inet- [**\_ Port \_ Bereichs**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_range) Struktur sein.</span><span class="sxs-lookup"><span data-stu-id="a01a1-118">This parameter should be the size of the [**INET\_PORT\_RANGE**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_range) structure.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="a01a1-119">lpvoutbuffer</span><span class="sxs-lookup"><span data-stu-id="a01a1-119">lpvOutBuffer</span></span>

<span data-ttu-id="a01a1-120">Ein Zeiger auf den Ausgabepuffer.</span><span class="sxs-lookup"><span data-stu-id="a01a1-120">A pointer to the output buffer.</span></span>
<span data-ttu-id="a01a1-121">Bei erfolgreicher Ausgabe enthält dieser Parameter einen Zeiger auf eine [**inet- \_ Port- \_ Reservierungs \_ Instanzstruktur**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_instance) .</span><span class="sxs-lookup"><span data-stu-id="a01a1-121">On successful output, this parameter contains a pointer to an [**INET\_PORT\_RESERVATION\_INSTANCE**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_instance) structure.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="a01a1-122">cboutbuffer</span><span class="sxs-lookup"><span data-stu-id="a01a1-122">cbOutBuffer</span></span>

<span data-ttu-id="a01a1-123">Die Größe des Ausgabepuffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="a01a1-123">The size, in bytes, of the output buffer.</span></span>
<span data-ttu-id="a01a1-124">Dieser Parameter muss mindestens die Größe der [**inet \_ Port- \_ Reservierungs \_ Instanzstruktur**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_instance) aufweisen.</span><span class="sxs-lookup"><span data-stu-id="a01a1-124">This parameter must be at least the size of the [**INET\_PORT\_RESERVATION\_INSTANCE**](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_instance) structure.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="a01a1-125">lpcbbyteszurück gegeben</span><span class="sxs-lookup"><span data-stu-id="a01a1-125">lpcbBytesReturned</span></span>

<span data-ttu-id="a01a1-126">Ein Zeiger auf eine Variable, die die Größe der im Ausgabepuffer gespeicherten Daten (in Bytes) empfängt.</span><span class="sxs-lookup"><span data-stu-id="a01a1-126">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>

<span data-ttu-id="a01a1-127">Wenn der Ausgabepuffer zu klein ist, schlägt der-Befehl fehl, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) gibt [**WSAEINVAL**](windows-sockets-error-codes-2.md)zurück, und der *lpcbbytesreturns* -Parameter verweist auf den **DWORD** -Wert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="a01a1-127">If the output buffer is too small, the call fails, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns [**WSAEINVAL**](windows-sockets-error-codes-2.md), and the *lpcbBytesReturned* parameter points to a **DWORD** value of zero.</span></span>

<span data-ttu-id="a01a1-128">Wenn *lpoverlgetauscht* gleich **null** ist, kann der **DWORD** -Wert, auf den der *lpcbbytesall* -Parameter verweist, der bei einem erfolgreichen-Vorgang zurückgegeben wird, nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="a01a1-128">If *lpOverlapped* is **NULL**, the **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned on a successful call cannot be zero.</span></span>

<span data-ttu-id="a01a1-129">Wenn der *lpoverllapp* -Parameter für überlappende Sockets nicht **null** ist, werden Vorgänge, die nicht sofort abgeschlossen werden können, initiiert, und der Abschluss wird zu einem späteren Zeitpunkt angegeben.</span><span class="sxs-lookup"><span data-stu-id="a01a1-129">If the *lpOverlapped* parameter is not **NULL** for overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>
<span data-ttu-id="a01a1-130">Der **DWORD** -Wert, auf den der zurückgegebene *lpcbbyteszurück gegebene* Parameter verweist, kann NULL sein, da die Größe der gespeicherten Daten erst bestimmt werden kann, wenn der überlappende Vorgang abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="a01a1-130">The **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned may be zero since the size of the data stored can't be determined until the overlapped operation has completed.</span></span>
<span data-ttu-id="a01a1-131">Der endgültige Abschluss Status kann abgerufen werden, wenn die geeignete Vervollständigungs Methode signalisiert wird, wenn der Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="a01a1-131">The final completion status can be retrieved when the appropriate completion method is signaled when the operation has completed.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="a01a1-132">lpvoverlgetauscht</span><span class="sxs-lookup"><span data-stu-id="a01a1-132">lpvOverlapped</span></span>

<span data-ttu-id="a01a1-133">Ein Zeiger auf eine [**wsaoverllapp**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="a01a1-133">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="a01a1-134">Wenn Socket *s* ohne das überlappende Attribut erstellt wurde, wird der *lpoverllapp* -Parameter ignoriert.</span><span class="sxs-lookup"><span data-stu-id="a01a1-134">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="a01a1-135">Wenn *s* mit dem überlappenden Attribut geöffnet wurde und der *lpoverlgetauscht* -Parameter nicht **null** ist, wird der Vorgang als überlappende (asynchrone) Operation ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a01a1-135">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="a01a1-136">In diesem Fall muss der *lpoverllapp* -Parameter auf eine gültige [**wsaoverllapp**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) -Struktur zeigen.</span><span class="sxs-lookup"><span data-stu-id="a01a1-136">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="a01a1-137">Bei überlappenden Vorgängen gibt die Funktion [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) oder **wspioctl** sofort zurück, und die entsprechende Vervollständigungs Methode wird signalisiert, wenn der Vorgang abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="a01a1-137">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="a01a1-138">Andernfalls gibt die Funktion nicht zurück, bis der Vorgang abgeschlossen ist oder ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="a01a1-138">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="a01a1-139">lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="a01a1-139">lpCompletionRoutine</span></span>

<span data-ttu-id="a01a1-140">Typ: \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="a01a1-140">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="a01a1-141">Ein Zeiger auf die Vervollständigungs Routine, die aufgerufen wird, wenn der Vorgang abgeschlossen wurde (bei nicht überlappenden Sockets ignoriert).</span><span class="sxs-lookup"><span data-stu-id="a01a1-141">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="a01a1-142">lpthreadid</span><span class="sxs-lookup"><span data-stu-id="a01a1-142">lpThreadId</span></span>

<span data-ttu-id="a01a1-143">Ein Zeiger auf eine [**wsathreadid**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) -Struktur, die vom Anbieter in einem nachfolgenden **wpuqueueapc**-Rückruf verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a01a1-143">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to **WPUQueueApc**.</span></span>
<span data-ttu-id="a01a1-144">Der Anbieter sollte die referenzierte [**wsathreadid**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) -Struktur (nicht den Zeiger auf dieselbe) speichern, bis die **wpuqueueapc** -Funktion zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="a01a1-144">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the **WPUQueueApc** function returns.</span></span>

<span data-ttu-id="a01a1-145">**Hinweis**  Dieser Parameter gilt nur für die **wspioctl** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="a01a1-145">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="a01a1-146">lperrno</span><span class="sxs-lookup"><span data-stu-id="a01a1-146">lpErrno</span></span>

<span data-ttu-id="a01a1-147">Ein Zeiger auf den Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="a01a1-147">A pointer to the error code.</span></span>

<span data-ttu-id="a01a1-148">**Hinweis**  Dieser Parameter gilt nur für die **wspioctl** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="a01a1-148">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="a01a1-149">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a01a1-149">Return value</span></span>

<span data-ttu-id="a01a1-150">Wenn der Vorgang erfolgreich abgeschlossen wird, gibt die [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) -oder **wspioctl** -Funktion NULL zurück.</span><span class="sxs-lookup"><span data-stu-id="a01a1-150">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="a01a1-151">Wenn der Vorgang fehlschlägt oder aussteht, gibt die Funktion [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) oder **wspioctl** einen **\_ Socketfehler** zurück.</span><span class="sxs-lookup"><span data-stu-id="a01a1-151">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="a01a1-152">Um erweiterte Fehlerinformationen abzurufen, nennen Sie [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="a01a1-152">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="a01a1-153">Fehlercode</span><span class="sxs-lookup"><span data-stu-id="a01a1-153">Error code</span></span> | <span data-ttu-id="a01a1-154">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="a01a1-154">Meaning</span></span> |
|------------|---------|
|<span data-ttu-id="a01a1-155">**ausstehende WSA-e/a \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a01a1-155">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="a01a1-156">Überlappende e/a-Vorgänge werden ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a01a1-156">Overlapped I/O operation is in progress.</span></span> <span data-ttu-id="a01a1-157">Dieser Wert wird zurückgegeben, wenn ein überlappende Vorgang erfolgreich initiiert wurde und die Beendigung zu einem späteren Zeitpunkt angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a01a1-157">This value is returned if an overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="a01a1-158">**WSA- \_ Vorgang \_ abgebrochen**</span><span class="sxs-lookup"><span data-stu-id="a01a1-158">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="a01a1-159">Der e/a-Vorgang wurde aufgrund eines Thread Beendigungs-oder einer Anwendungsanforderung abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="a01a1-159">The I/O operation has been aborted because of either a thread exit or an application request.</span></span> <span data-ttu-id="a01a1-160">Dieser Fehler wird zurückgegeben, wenn ein über Lapp ender Vorgang aufgrund der Schließung des Sockets oder der Ausführung des Befehls " **SIO \_ Flush** ioctl" abgebrochen wurde.</span><span class="sxs-lookup"><span data-stu-id="a01a1-160">This error is returned if an overlapped operation was canceled due to the closure of the socket or the execution of the **SIO\_FLUSH** IOCTL command.</span></span> |
| <span data-ttu-id="a01a1-161">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="a01a1-161">**WSAEFAULT**</span></span> | <span data-ttu-id="a01a1-162">Das System hat bei dem Versuch, ein Zeigerargument in einem-Befehl zu verwenden, eine ungültige Zeiger Adresse erkannt.</span><span class="sxs-lookup"><span data-stu-id="a01a1-162">The system detected an invalid pointer address in attempting to use a pointer argument in a call.</span></span> <span data-ttu-id="a01a1-163">Dieser Fehler wird zurückgegeben, wenn der Parameter *lpvinbuffer*, *lpvoutbuffer*, *lpcbbytesall*, *lpoverlgetauscht* oder *lpCompletionRoutine* nicht vollständig in einem gültigen Teil des Benutzer Adressraums enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="a01a1-163">This error is returned of the *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="a01a1-164">**Wsaeingabe Progress**</span><span class="sxs-lookup"><span data-stu-id="a01a1-164">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="a01a1-165">Ein Blockierungsvorgang wird momentan ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a01a1-165">A blocking operation is currently executing.</span></span> <span data-ttu-id="a01a1-166">Dieser Fehler wird zurückgegeben, wenn die Funktion aufgerufen wird, wenn ein Rückruf ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a01a1-166">This error is returned if the function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="a01a1-167">**Wsaeingabe**</span><span class="sxs-lookup"><span data-stu-id="a01a1-167">**WSAEINTR**</span></span> | <span data-ttu-id="a01a1-168">Ein Blockierungs Vorgang wurde durch einen [**wsacancelblockingstatement**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall)-Aufrufvorgang unterbrochen.</span><span class="sxs-lookup"><span data-stu-id="a01a1-168">A blocking operation was interrupted by a call to [**WSACancelBlockingCall**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall).</span></span> <span data-ttu-id="a01a1-169">Dieser Fehler wird zurückgegeben, wenn ein Blockierungs Vorgang unterbrochen wurde.</span><span class="sxs-lookup"><span data-stu-id="a01a1-169">This error is returned if a blocking operation was interrupted.</span></span> |
| <span data-ttu-id="a01a1-170">**Wsaabval**</span><span class="sxs-lookup"><span data-stu-id="a01a1-170">**WSAEINVAL**</span></span> | <span data-ttu-id="a01a1-171">Ein ungültiges Argument wurde angegeben.</span><span class="sxs-lookup"><span data-stu-id="a01a1-171">An invalid argument was supplied.</span></span> <span data-ttu-id="a01a1-172">Dieser Fehler wird zurückgegeben, wenn der *dwIoControlCode* -Parameter kein gültiger Befehl ist oder wenn ein angegebener Eingabeparameter nicht zulässig ist oder der Befehl nicht auf den angegebenen Sockettyp anwendbar ist.</span><span class="sxs-lookup"><span data-stu-id="a01a1-172">This error is returned if the *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> |
| <span data-ttu-id="a01a1-173">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="a01a1-173">**WSAENETDOWN**</span></span> | <span data-ttu-id="a01a1-174">Bei einem Socketvorgang war das Netzwerk inaktiv.</span><span class="sxs-lookup"><span data-stu-id="a01a1-174">A socket operation encountered a dead network.</span></span> <span data-ttu-id="a01a1-175">Dieser Fehler wird zurückgegeben, wenn das Netzwerk Subsystem fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="a01a1-175">This error is returned if the network subsystem has failed.</span></span> |
| <span data-ttu-id="a01a1-176">**Wsaumotsock**</span><span class="sxs-lookup"><span data-stu-id="a01a1-176">**WSAENOTSOCK**</span></span> | <span data-ttu-id="a01a1-177">Es wurde versucht, einen Vorgang für etwas auszuführen, das kein Socket ist.</span><span class="sxs-lookup"><span data-stu-id="a01a1-177">An operation was attempted on something that is not a socket.</span></span> <span data-ttu-id="a01a1-178">Dieser Fehler wird zurückgegeben, wenn es sich bei den *Deskriptoren nicht* um einen Socket handelt.</span><span class="sxs-lookup"><span data-stu-id="a01a1-178">This error is returned if the descriptor *s* is not a socket.</span></span> |
| <span data-ttu-id="a01a1-179">**WSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="a01a1-179">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="a01a1-180">Der versuchte Vorgang wird für den Typ des Objekts, auf das verwiesen wird, nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a01a1-180">The attempted operation is not supported for the type of object referenced.</span></span> <span data-ttu-id="a01a1-181">Dieser Fehler wird zurückgegeben, wenn der angegebene ioctl-Befehl nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="a01a1-181">This error is returned if the specified IOCTL command is not supported.</span></span> <span data-ttu-id="a01a1-182">Dieser Fehler wird auch zurückgegeben, wenn die IOCTL-ioctl zum Abrufen des Zertifikat **\_ \_ Anschlusses \_** vom Transportanbieter nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="a01a1-182">This error is also returned if the **SIO\_ACQUIRE\_PORT\_RESERVATION** IOCTL is not supported by the transport provider.</span></span> <span data-ttu-id="a01a1-183">Dieser Fehler wird auch zurückgegeben, wenn bei dem Versuch, die IOCTL für den Zertifikat **\_ \_ erstellungsport \_** zu verwenden, ein anderer Socket als UDP oder TCP verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a01a1-183">This error is also returned when an attempt to use the **SIO\_ACQUIRE\_PORT\_RESERVATION** IOCTL is made on a socket other than UDP or TCP.</span></span> |

## <a name="remarks"></a><span data-ttu-id="a01a1-184">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a01a1-184">Remarks</span></span>

<span data-ttu-id="a01a1-185">Die IOCTL- **\_ \_ \_ reservierte**  ioctl des Zertifikat Erstellungs Ports wird unter Windows Vista und höheren Versionen des Betriebssystems unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a01a1-185">The **SIO\_ACQUIRE\_PORT\_RESERVATION**  IOCTL is supported on Windows Vista and later versions of the operating system.</span></span>

<span data-ttu-id="a01a1-186">Anwendungen und Dienste, die Ports reservieren müssen, lassen sich in zwei Kategorien unterteilen.</span><span class="sxs-lookup"><span data-stu-id="a01a1-186">Applications and services which need to reserve ports fall into two categories.</span></span>
<span data-ttu-id="a01a1-187">Die erste Kategorie umfasst Komponenten, die einen bestimmten Port als Teil Ihres Vorgangs benötigen.</span><span class="sxs-lookup"><span data-stu-id="a01a1-187">The first category includes components which need a particular port as part of their operation.</span></span>
<span data-ttu-id="a01a1-188">Diese Komponenten bevorzugen in der Regel die Angabe Ihres erforderlichen Ports zur Installationszeit (z. b. in einem Anwendungs Manifest).</span><span class="sxs-lookup"><span data-stu-id="a01a1-188">Such components will generally prefer to specify their required port at installation time (in an application manifest, for example).</span></span>
<span data-ttu-id="a01a1-189">Die zweite Kategorie umfasst Komponenten, die zur Laufzeit einen beliebigen verfügbaren Port oder einen beliebigen Port Block benötigen.</span><span class="sxs-lookup"><span data-stu-id="a01a1-189">The second category includes components which need any available port or block of ports at runtime.</span></span>
<span data-ttu-id="a01a1-190">Diese beiden Kategorien entsprechen bestimmten Port Reservierungs Anforderungen für und Platzhalter.</span><span class="sxs-lookup"><span data-stu-id="a01a1-190">These two categories correspond to specific and wildcard port reservation requests.</span></span>
<span data-ttu-id="a01a1-191">Bestimmte Reservierungs Anforderungen sind möglicherweise persistent oder Laufzeit, während reservierte Port Reservierungs Anforderungen nur zur Laufzeit unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="a01a1-191">Specific reservation requests may be persistent or runtime, while wildcard port reservation requests are only supported at runtime.</span></span>

<span data-ttu-id="a01a1-192">Die IOCTL- **\_ \_ \_ reservierte**  ioctl-Anforderung zum Abrufen einer Lauf Zeit Reservierung wird für einen Block von TCP-oder UDP-Ports verwendet.</span><span class="sxs-lookup"><span data-stu-id="a01a1-192">The **SIO\_ACQUIRE\_PORT\_RESERVATION**  IOCTL is used to request a runtime reservation for a block of TCP or UDP ports.</span></span>
<span data-ttu-id="a01a1-193">Bei Lauf Zeit Port Reservierungen erfordert der Port Pool, dass Reservierungen von dem Prozess verarbeitet werden, dessen Socket die Reservierung gewährt wurde.</span><span class="sxs-lookup"><span data-stu-id="a01a1-193">For runtime port reservations, the port pool requires that reservations be consumed from the process on whose socket the reservation was granted.</span></span>
<span data-ttu-id="a01a1-194">Lauf Zeit Port Reservierungen dauern nur so lange, wie die Lebensdauer des Sockets, auf dem die IOCTL-ioctl-Reservierung für den Zertifikat Abruf **\_ \_ \_ reserviert**  wurde.</span><span class="sxs-lookup"><span data-stu-id="a01a1-194">Runtime port reservations last only as long as the lifetime of the socket on which the **SIO\_ACQUIRE\_PORT\_RESERVATION**  IOCTL was called.</span></span>
<span data-ttu-id="a01a1-195">Im Gegensatz dazu können persistente Port Reservierungen, die mithilfe der Funktion " [**kreatepersistenttcpportreservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation) " oder " [**kreatepersistentudpportreservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation) " erstellt wurden, von jedem Prozess genutzt werden, der über die Möglichkeit zum Abrufen dauerhafter Reservierungen verfügt.</span><span class="sxs-lookup"><span data-stu-id="a01a1-195">In contrast, persistent port reservations created using the [**CreatePersistentTcpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation) or [**CreatePersistentUdpPortReservation**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation) function may be consumed by any process with the ability to obtain persistent reservations.</span></span>

<span data-ttu-id="a01a1-196">Sobald eine TCP-oder UDP-Port Reservierung für die Laufzeit abgerufen wurde, kann eine Anwendung Port Zuweisungen von der Port Reservierung anfordern, indem Sie einen TCP-oder UDP-Socket öffnet und anschließend die [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) -Funktion aufruft, die die IOCTL-ioctl-IOCTL- [**\_ \_ \_ typreservierung**](sio-associate-port-reservation.md) angibt und vor dem Ausgeben eines Aufrufs an die Bind-Funktion des Sockets</span><span class="sxs-lookup"><span data-stu-id="a01a1-196">Once a runtime TCP or UDP port reservation has been obtained, an application can request port assignments from the port reservation by opening a TCP or UDP socket, then calling the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) function specifying the [**SIO\_ASSOCIATE\_PORT\_RESERVATION**](sio-associate-port-reservation.md) IOCTL and passing the reservation token before issuing a call to the bind function on the socket.</span></span>

<span data-ttu-id="a01a1-197">Wenn die Parameter *lpoverlgetauscht* und *lpCompletionRoutine* **null** sind, wird der Socket in dieser Funktion als nicht überlappenden Socket behandelt.</span><span class="sxs-lookup"><span data-stu-id="a01a1-197">If both *lpOverlapped* and *lpCompletionRoutine* parameters are **NULL**, the socket in this function will be treated as a non-overlapped socket.</span></span>
<span data-ttu-id="a01a1-198">Bei einem nicht überlappenden Socket werden die Parameter *lpoverlgetauscht* und *lpCompletionRoutine* ignoriert, mit der Ausnahme, dass die Funktion blockiert werden kann, wenn sich Socket *s* im Blockierungs Modus befindet.</span><span class="sxs-lookup"><span data-stu-id="a01a1-198">For a non-overlapped socket, *lpOverlapped* and *lpCompletionRoutine* parameters are ignored, except that the function can block if socket *s* is in blocking mode.</span></span>
<span data-ttu-id="a01a1-199">Wenn sich Socket *s* im nicht blockierenden Modus befindet, wird diese Funktion immer noch blockiert, da diese spezielle ioctl den nicht blockierenden Modus nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a01a1-199">If socket *s* is in non-blocking mode, this function will still block since this particular IOCTL does not support non-blocking mode.</span></span>

<span data-ttu-id="a01a1-200">Bei überlappenden Sockets werden Vorgänge, die nicht sofort abgeschlossen werden können, initiiert, und der Abschluss wird zu einem späteren Zeitpunkt angegeben.</span><span class="sxs-lookup"><span data-stu-id="a01a1-200">For overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>

<span data-ttu-id="a01a1-201">Alle ioctl können unbegrenzt blockieren, abhängig von der Implementierung des Dienstanbieters.</span><span class="sxs-lookup"><span data-stu-id="a01a1-201">Any IOCTL may block indefinitely, depending on the service provider's implementation.</span></span>
<span data-ttu-id="a01a1-202">Wenn die Anwendung die Blockierung in einem WSAIoctl-oder **wspioctl** -Funktions aufrufnis nicht tolerieren kann, werden überlappende e/a-Vorgänge für IOCTLs empfohlen, die besonders wahrscheinlich blockiert werden.</span><span class="sxs-lookup"><span data-stu-id="a01a1-202">If the application cannot tolerate blocking in a WSAIoctl or **WSPIoctl** function call, overlapped I/O would be advised for IOCTLs that are especially likely to block.</span></span>

<span data-ttu-id="a01a1-203">**In den** folgenden Fällen kann die IOCTL- **\_ \_ \_ Reservierungs** -ioctl für die RSA-Abruf Vorgänge fehlschlagen: **\_ \_**</span><span class="sxs-lookup"><span data-stu-id="a01a1-203">The **SIO\_ACQUIRE\_PORT\_RESERVATION**  IOCTL can fail with **WSAEINTR** or **WSA\_OPERATION\_ABORTED** under the following cases:</span></span>

* <span data-ttu-id="a01a1-204">Die Anforderung wird vom e/a-Manager abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="a01a1-204">The request is canceled by the I/O Manager.</span></span>
* <span data-ttu-id="a01a1-205">Der Socket ist geschlossen.</span><span class="sxs-lookup"><span data-stu-id="a01a1-205">The socket is closed.</span></span>

## <a name="examples"></a><span data-ttu-id="a01a1-206">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a01a1-206">Examples</span></span>

<span data-ttu-id="a01a1-207">Im folgenden Beispiel wird eine Lauf Zeit Port Reservierung angefordert, anschließend wird ein Socket erstellt und ein Port aus der Lauf Zeit Port Reservierung für den Socket zugewiesen. Anschließend wird der Socket geschlossen, und die Lauf Zeit Port Reservierung wird aufgehoben.</span><span class="sxs-lookup"><span data-stu-id="a01a1-207">The following example acquires a runtime port reservation, then creates a socket and allocates a port from the runtime port reservation for the socket, and then closes the socket and the releases the runtime port reservation.</span></span>

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

    // Note that the sockaddr_in struct works only with AF_INET not AF_INET6
    // An application needs to use the sockaddr_in6 for AF_INET6
    sockaddr_in service;
    sockaddr_in sockName;
    int nameLen = sizeof (sockName);

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

            sockRes = socket(iFamily, iType, iProtocol);
            if (sockRes == INVALID_SOCKET) {
                wprintf(L"socket function for second socket failed with error = %d\n",
                        WSAGetLastError());
                closesocket(sock);
                WSACleanup();
                return 1;
            } else {
                wprintf(L"socket function for second socket succeeded\n");

                iResult =
                    WSAIoctl(sock, SIO_ASSOCIATE_PORT_RESERVATION,
                             (LPVOID) & portRes.Token, sizeof (ULONG64), NULL, 0,
                             &bytesReturned, NULL, NULL);
                if (iResult != 0) {
                    wprintf
                        (L"WSAIoctl(SIO_ASSOCIATE_PORT_RESERVATION) failed with error = %d\n",
                         WSAGetLastError());
                } else {
                    wprintf
                        (L"WSAIoctl(SIO_ASSOCIATE_PORT_RESERVATION) succeeded, bytesReturned = %u\n",
                         bytesReturned);

                    service.sin_family = (ADDRESS_FAMILY) iFamily;
                    service.sin_addr.s_addr = INADDR_ANY;
                    service.sin_port = 0;

                    iResult = bind(sock, (SOCKADDR *) & service, sizeof (service));
                    if (iResult == SOCKET_ERROR)
                        wprintf(L"bind failed with error = %d\n", WSAGetLastError());
                    else {
                        wprintf(L"bind succeeded\n");
                        iResult = getsockname(sock, (SOCKADDR *) & sockName, &nameLen);
                        if (iResult == SOCKET_ERROR)
                            wprintf(L"getsockname failed with error = %d\n",
                                    WSAGetLastError());
                        else {
                            wprintf(L"getsockname succeeded\n");
                            wprintf(L"Port number allocated = %u\n",
                                    ntohs(sockName.sin_port));
                        }
                    }
                }
            }

            // comment out this block of code if you don't want to delete the reservation just created
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

        if (sockRes != INVALID_SOCKET) {
            iResult = closesocket(sockRes);
            if (iResult == SOCKET_ERROR) {
                wprintf(L"closesocket for second socket failed with error = %d\n",
                        WSAGetLastError());
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

## <a name="see-also"></a><span data-ttu-id="a01a1-208">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a01a1-208">See also</span></span>

[<span data-ttu-id="a01a1-209">**erst**</span><span class="sxs-lookup"><span data-stu-id="a01a1-209">**accept**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-accept)

[<span data-ttu-id="a01a1-210">**Zwick**</span><span class="sxs-lookup"><span data-stu-id="a01a1-210">**bind**</span></span>](/windows/desktop/api/winsock/nf-winsock-bind)

[<span data-ttu-id="a01a1-211">**"Kreatepersistenttcpportreservation"**</span><span class="sxs-lookup"><span data-stu-id="a01a1-211">**CreatePersistentTcpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation)

[<span data-ttu-id="a01a1-212">**"Kreatepersistentudpportreservation"**</span><span class="sxs-lookup"><span data-stu-id="a01a1-212">**CreatePersistentUdpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation)

[<span data-ttu-id="a01a1-213">**Deletepersistenttcpportreservation**</span><span class="sxs-lookup"><span data-stu-id="a01a1-213">**DeletePersistentTcpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-deletepersistenttcpportreservation)

[<span data-ttu-id="a01a1-214">**Deletepersistentudpportreservation**</span><span class="sxs-lookup"><span data-stu-id="a01a1-214">**DeletePersistentUdpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-deletepersistentudpportreservation)

[<span data-ttu-id="a01a1-215">**INET- \_ Port \_ Bereich**</span><span class="sxs-lookup"><span data-stu-id="a01a1-215">**INET\_PORT\_RANGE**</span></span>](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_range)

[<span data-ttu-id="a01a1-216">**INET- \_ Port \_ Reservierungs \_ Instanz**</span><span class="sxs-lookup"><span data-stu-id="a01a1-216">**INET\_PORT\_RESERVATION\_INSTANCE**</span></span>](/windows/desktop/api/mstcpip/ns-mstcpip-inet_port_reservation_instance)

[<span data-ttu-id="a01a1-217">**Lookuppersistenttcpportreservation**</span><span class="sxs-lookup"><span data-stu-id="a01a1-217">**LookupPersistentTcpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-lookuppersistenttcpportreservation)

[<span data-ttu-id="a01a1-218">**Lookuppersistentudpportreservation**</span><span class="sxs-lookup"><span data-stu-id="a01a1-218">**LookupPersistentUdpPortReservation**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-lookuppersistentudpportreservation)

[<span data-ttu-id="a01a1-219">**\_Zuordnen der \_ Port \_ Reservierung**</span><span class="sxs-lookup"><span data-stu-id="a01a1-219">**SIO\_ASSOCIATE\_PORT\_RESERVATION**</span></span>](sio-associate-port-reservation.md)

[<span data-ttu-id="a01a1-220">**\_ \_ Port \_ Reservierung für den SIO-Release**</span><span class="sxs-lookup"><span data-stu-id="a01a1-220">**SIO\_RELEASE\_PORT\_RESERVATION**</span></span>](sio-release-port-reservation.md)

[<span data-ttu-id="a01a1-221">**Glühbirne**</span><span class="sxs-lookup"><span data-stu-id="a01a1-221">**socket**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="a01a1-222">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="a01a1-222">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)

[<span data-ttu-id="a01a1-223">**Wsagein verlappedresult**</span><span class="sxs-lookup"><span data-stu-id="a01a1-223">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="a01a1-224">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="a01a1-224">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="a01a1-225">**Wsaoverlgetauscht**</span><span class="sxs-lookup"><span data-stu-id="a01a1-225">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="a01a1-226">**Wsasocketa**</span><span class="sxs-lookup"><span data-stu-id="a01a1-226">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="a01a1-227">**Wsasocketw**</span><span class="sxs-lookup"><span data-stu-id="a01a1-227">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
