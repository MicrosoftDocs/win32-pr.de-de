---
description: Der Steuerungs Code konfiguriert einen TCP-Socket für eine geringere Latenz und schnellere Vorgänge an der Loopback Schnittstelle.
ms.assetid: 4F7A6454-E3ED-4529-A531-B0640B0767EF
title: SIO_LOOPBACK_FAST_PATH Steuerungs Codes
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: f32cba8a081d2eb268a3e93a362ccec9bf414d8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360715"
---
# <a name="sio_loopback_fast_path-control-code"></a><span data-ttu-id="8d869-103">SIO_LOOPBACK_FAST_PATH Steuerungs Codes</span><span class="sxs-lookup"><span data-stu-id="8d869-103">SIO_LOOPBACK_FAST_PATH Control Code</span></span>

## <a name="description"></a><span data-ttu-id="8d869-104">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8d869-104">Description</span></span>

<span data-ttu-id="8d869-105">Der Code für die **\_ \_ schnelle \_ Pfad Steuerung von SIO Loopback** konfiguriert einen TCP-Socket für eine geringere Latenz und schnellere Vorgänge in der Loopback Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="8d869-105">The **SIO\_LOOPBACK\_FAST\_PATH** control code configures a TCP socket for lower latency and faster operations on the loopback interface.</span></span>

<span data-ttu-id="8d869-106">**Wichtig**  Der **\_ \_ schnelle \_ Pfad des SIO-Loopbacks** ist veraltet und wird nicht für die Verwendung im Code empfohlen.</span><span class="sxs-lookup"><span data-stu-id="8d869-106">**Important**  The **SIO\_LOOPBACK\_FAST\_PATH** is deprecated and is not recommended to be used in your code.</span></span>

<span data-ttu-id="8d869-107">Um diesen Vorgang auszuführen, wenden Sie die [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) -oder **wspioctl** -Funktion mit den folgenden Parametern an.</span><span class="sxs-lookup"><span data-stu-id="8d869-107">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_LOOPBACK_FAST_PATH,                // dwIoControlCode
  (LPVOID) lpvInBuffer,   // pointer to a Boolean value
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
  SIO_LOOPBACK_FAST_PATH,                // dwIoControlCode
  (LPVOID) lpvInBuffer,   // pointer to a Boolean value
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

## <a name="parameters"></a><span data-ttu-id="8d869-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="8d869-108">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="8d869-109">s</span><span class="sxs-lookup"><span data-stu-id="8d869-109">s</span></span>

<span data-ttu-id="8d869-110">Ein Deskriptor, der einen Socket identifiziert.</span><span class="sxs-lookup"><span data-stu-id="8d869-110">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="8d869-111">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="8d869-111">dwIoControlCode</span></span>

<span data-ttu-id="8d869-112">Der Steuerelement Code für den Vorgang.</span><span class="sxs-lookup"><span data-stu-id="8d869-112">The control code for the operation.</span></span>
<span data-ttu-id="8d869-113">Verwenden Sie für diesen Vorgang einen **\_ \_ schnellen \_ Pfad** für den hoch-Loopback.</span><span class="sxs-lookup"><span data-stu-id="8d869-113">Use **SIO\_LOOPBACK\_FAST\_PATH** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="8d869-114">lpvinbuffer</span><span class="sxs-lookup"><span data-stu-id="8d869-114">lpvInBuffer</span></span>

<span data-ttu-id="8d869-115">Ein Zeiger auf den Eingabepuffer.</span><span class="sxs-lookup"><span data-stu-id="8d869-115">A pointer to the input buffer.</span></span>
<span data-ttu-id="8d869-116">Dieser Parameter enthält einen Zeiger auf einen booleschen Wert, der angibt, ob der Socket für schnelle Loopback Vorgänge konfiguriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="8d869-116">This parameter contains a pointer to a Boolean value that indicates if the socket should be configured for fast loopback operations.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="8d869-117">cbinbuffer</span><span class="sxs-lookup"><span data-stu-id="8d869-117">cbInBuffer</span></span>

<span data-ttu-id="8d869-118">Die Größe des Eingabe Puffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="8d869-118">The size, in bytes, of the input buffer.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="8d869-119">lpvoutbuffer</span><span class="sxs-lookup"><span data-stu-id="8d869-119">lpvOutBuffer</span></span>

<span data-ttu-id="8d869-120">Ein Zeiger auf den Ausgabepuffer.</span><span class="sxs-lookup"><span data-stu-id="8d869-120">A pointer to the output buffer.</span></span>
<span data-ttu-id="8d869-121">Dieser Parameter wird für diesen Vorgang nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="8d869-121">This parameter is unused for this operation.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="8d869-122">cboutbuffer</span><span class="sxs-lookup"><span data-stu-id="8d869-122">cbOutBuffer</span></span>

<span data-ttu-id="8d869-123">Die Größe des Ausgabepuffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="8d869-123">The size, in bytes, of the output buffer.</span></span>
<span data-ttu-id="8d869-124">Dieser Parameter muss auf 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="8d869-124">This parameter must be set to zero.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="8d869-125">lpcbbyteszurück gegeben</span><span class="sxs-lookup"><span data-stu-id="8d869-125">lpcbBytesReturned</span></span>

<span data-ttu-id="8d869-126">Ein Zeiger auf eine Variable, die die Größe der im Ausgabepuffer gespeicherten Daten (in Bytes) empfängt.</span><span class="sxs-lookup"><span data-stu-id="8d869-126">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>

<span data-ttu-id="8d869-127">Wenn der Ausgabepuffer zu klein ist, schlägt der-Befehl fehl, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) gibt [**WSAEINVAL**](windows-sockets-error-codes-2.md)zurück, und der *lpcbbytesreturns* -Parameter verweist auf den **DWORD** -Wert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="8d869-127">If the output buffer is too small, the call fails, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns [**WSAEINVAL**](windows-sockets-error-codes-2.md), and the *lpcbBytesReturned* parameter points to a **DWORD** value of zero.</span></span>

<span data-ttu-id="8d869-128">Wenn *lpoverlgetauscht* gleich **null** ist, kann der **DWORD** -Wert, auf den der *lpcbbytesall* -Parameter verweist, der bei einem erfolgreichen-Vorgang zurückgegeben wird, nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="8d869-128">If *lpOverlapped* is **NULL**, the **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned on a successful call cannot be zero.</span></span>

<span data-ttu-id="8d869-129">Wenn der *lpoverllapp* -Parameter für überlappende Sockets nicht **null** ist, werden Vorgänge, die nicht sofort abgeschlossen werden können, initiiert, und der Abschluss wird zu einem späteren Zeitpunkt angegeben.</span><span class="sxs-lookup"><span data-stu-id="8d869-129">If the *lpOverlapped* parameter is not **NULL** for overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>
<span data-ttu-id="8d869-130">Der **DWORD** -Wert, auf den der zurückgegebene *lpcbbyteszurück gegebene* Parameter verweist, kann NULL sein, da die Größe der gespeicherten Daten erst bestimmt werden kann, wenn der überlappende Vorgang abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="8d869-130">The **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned may be zero since the size of the data stored can't be determined until the overlapped operation has completed.</span></span>
<span data-ttu-id="8d869-131">Der endgültige Abschluss Status kann abgerufen werden, wenn die geeignete Vervollständigungs Methode signalisiert wird, wenn der Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="8d869-131">The final completion status can be retrieved when the appropriate completion method is signaled when the operation has completed.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="8d869-132">lpvoverlgetauscht</span><span class="sxs-lookup"><span data-stu-id="8d869-132">lpvOverlapped</span></span>

<span data-ttu-id="8d869-133">Ein Zeiger auf eine [**wsaoverllapp**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="8d869-133">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="8d869-134">Wenn Socket *s* ohne das überlappende Attribut erstellt wurde, wird der *lpoverllapp* -Parameter ignoriert.</span><span class="sxs-lookup"><span data-stu-id="8d869-134">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="8d869-135">Wenn *s* mit dem überlappenden Attribut geöffnet wurde und der *lpoverlgetauscht* -Parameter nicht **null** ist, wird der Vorgang als überlappende (asynchrone) Operation ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8d869-135">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="8d869-136">In diesem Fall muss der *lpoverllapp* -Parameter auf eine gültige [**wsaoverllapp**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) -Struktur zeigen.</span><span class="sxs-lookup"><span data-stu-id="8d869-136">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="8d869-137">Bei überlappenden Vorgängen gibt die Funktion [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) oder **wspioctl** sofort zurück, und die entsprechende Vervollständigungs Methode wird signalisiert, wenn der Vorgang abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="8d869-137">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="8d869-138">Andernfalls gibt die Funktion nicht zurück, bis der Vorgang abgeschlossen ist oder ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="8d869-138">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="8d869-139">lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="8d869-139">lpCompletionRoutine</span></span>

<span data-ttu-id="8d869-140">Typ: \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="8d869-140">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="8d869-141">Ein Zeiger auf die Vervollständigungs Routine, die aufgerufen wird, wenn der Vorgang abgeschlossen wurde (bei nicht überlappenden Sockets ignoriert).</span><span class="sxs-lookup"><span data-stu-id="8d869-141">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="8d869-142">lpthreadid</span><span class="sxs-lookup"><span data-stu-id="8d869-142">lpThreadId</span></span>

<span data-ttu-id="8d869-143">Ein Zeiger auf eine [**wsathreadid**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) -Struktur, die vom Anbieter in einem nachfolgenden [**wpuqueueapc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc)-Rückruf verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8d869-143">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="8d869-144">Der Anbieter sollte die referenzierte [**wsathreadid**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) -Struktur (nicht den Zeiger auf dieselbe) speichern, bis die [**wpuqueueapc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) -Funktion zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="8d869-144">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="8d869-145">**Hinweis**  Dieser Parameter gilt nur für die **wspioctl** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="8d869-145">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="8d869-146">lperrno</span><span class="sxs-lookup"><span data-stu-id="8d869-146">lpErrno</span></span>

<span data-ttu-id="8d869-147">Ein Zeiger auf den Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="8d869-147">A pointer to the error code.</span></span>

<span data-ttu-id="8d869-148">**Hinweis**  Dieser Parameter gilt nur für die **wspioctl** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="8d869-148">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="8d869-149">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8d869-149">Return value</span></span>

<span data-ttu-id="8d869-150">Wenn der Vorgang erfolgreich abgeschlossen wird, gibt die [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) -oder **wspioctl** -Funktion NULL zurück.</span><span class="sxs-lookup"><span data-stu-id="8d869-150">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="8d869-151">Wenn der Vorgang fehlschlägt oder aussteht, gibt die Funktion [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) oder **wspioctl** einen **\_ Socketfehler** zurück.</span><span class="sxs-lookup"><span data-stu-id="8d869-151">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="8d869-152">Um erweiterte Fehlerinformationen abzurufen, nennen Sie [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="8d869-152">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="8d869-153">Fehlercode</span><span class="sxs-lookup"><span data-stu-id="8d869-153">Error code</span></span> | <span data-ttu-id="8d869-154">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="8d869-154">Meaning</span></span> |
|------------|---------|
|<span data-ttu-id="8d869-155">**ausstehende WSA-e/a \_ \_**</span><span class="sxs-lookup"><span data-stu-id="8d869-155">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="8d869-156">Überlappende e/a-Vorgänge werden ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8d869-156">Overlapped I/O operation is in progress.</span></span> <span data-ttu-id="8d869-157">Dieser Wert wird zurückgegeben, wenn ein überlappende Vorgang erfolgreich initiiert wurde und die Beendigung zu einem späteren Zeitpunkt angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="8d869-157">This value is returned if an overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="8d869-158">**WSA- \_ Vorgang \_ abgebrochen**</span><span class="sxs-lookup"><span data-stu-id="8d869-158">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="8d869-159">Der e/a-Vorgang wurde aufgrund eines Thread Beendigungs-oder einer Anwendungsanforderung abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="8d869-159">The I/O operation has been aborted because of either a thread exit or an application request.</span></span> <span data-ttu-id="8d869-160">Dieser Fehler wird zurückgegeben, wenn ein über Lapp ender Vorgang aufgrund der Schließung des Sockets oder der Ausführung des Befehls " **SIO \_ Flush ioctl** " abgebrochen wurde.</span><span class="sxs-lookup"><span data-stu-id="8d869-160">This error is returned if an overlapped operation was canceled due to the closure of the socket or the execution of the **SIO\_FLUSH IOCTL** command.</span></span> |
| <span data-ttu-id="8d869-161">**WSAEACCES**</span><span class="sxs-lookup"><span data-stu-id="8d869-161">**WSAEACCES**</span></span> | <span data-ttu-id="8d869-162">Es wurde versucht, auf einen Socket auf eine Weise zuzugreifen, die durch seine Zugriffsberechtigungen unzulässig ist.</span><span class="sxs-lookup"><span data-stu-id="8d869-162">An attempt was made to access a socket in a way forbidden by its access permissions.</span></span> <span data-ttu-id="8d869-163">Dieser Fehler wird unter mehreren Bedingungen für persistente Port Reservierungen zurückgegeben, die Folgendes umfassen: dem Benutzer fehlen die erforderlichen Administratorrechte auf dem lokalen Computer, oder die Anwendung wird nicht in einer erweiterten Shell als integrierter Administrator ( `RunAs administrator` ) ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8d869-163">This error is returned under several conditions for persistent port reservations that include the following: the user lacks the required administrative privileges on the local computer or the application is not running in an enhanced shell as the built-in Administrator (`RunAs administrator`).</span></span> |
| <span data-ttu-id="8d869-164">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="8d869-164">**WSAEFAULT**</span></span> | <span data-ttu-id="8d869-165">Das System hat bei dem Versuch, ein Zeigerargument in einem-Befehl zu verwenden, eine ungültige Zeiger Adresse erkannt.</span><span class="sxs-lookup"><span data-stu-id="8d869-165">The system detected an invalid pointer address in attempting to use a pointer argument in a call.</span></span> <span data-ttu-id="8d869-166">Dieser Fehler wird zurückgegeben, wenn der Parameter *lpvinbuffer*, *lpvoutbuffer*, *lpcbbytesall*, *lpoverlgetauscht* oder *lpCompletionRoutine* nicht vollständig in einem gültigen Teil des Benutzer Adressraums enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="8d869-166">This error is returned of the *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="8d869-167">**Wsaeingabe Progress**</span><span class="sxs-lookup"><span data-stu-id="8d869-167">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="8d869-168">Ein Blockierungsvorgang wird momentan ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8d869-168">A blocking operation is currently executing.</span></span> <span data-ttu-id="8d869-169">Dieser Fehler wird zurückgegeben, wenn die Funktion aufgerufen wird, wenn ein Rückruf ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8d869-169">This error is returned if the function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="8d869-170">**Wsaeingabe**</span><span class="sxs-lookup"><span data-stu-id="8d869-170">**WSAEINTR**</span></span> | <span data-ttu-id="8d869-171">Ein Blockierungs Vorgang wurde durch einen [**wsacancelblockingstatement**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall)-Aufrufvorgang unterbrochen.</span><span class="sxs-lookup"><span data-stu-id="8d869-171">A blocking operation was interrupted by a call to [**WSACancelBlockingCall**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall).</span></span> <span data-ttu-id="8d869-172">Dieser Fehler wird zurückgegeben, wenn ein Blockierungs Vorgang unterbrochen wurde.</span><span class="sxs-lookup"><span data-stu-id="8d869-172">This error is returned if a blocking operation was interrupted.</span></span> |
| <span data-ttu-id="8d869-173">**Wsaabval**</span><span class="sxs-lookup"><span data-stu-id="8d869-173">**WSAEINVAL**</span></span> | <span data-ttu-id="8d869-174">Ein ungültiges Argument wurde angegeben.</span><span class="sxs-lookup"><span data-stu-id="8d869-174">An invalid argument was supplied.</span></span> <span data-ttu-id="8d869-175">Dieser Fehler wird zurückgegeben, wenn der *dwIoControlCode* -Parameter kein gültiger Befehl ist oder wenn ein angegebener Eingabeparameter nicht zulässig ist oder der Befehl nicht auf den angegebenen Sockettyp anwendbar ist.</span><span class="sxs-lookup"><span data-stu-id="8d869-175">This error is returned if the *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> |
| <span data-ttu-id="8d869-176">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="8d869-176">**WSAENETDOWN**</span></span> | <span data-ttu-id="8d869-177">Bei einem Socketvorgang war das Netzwerk inaktiv.</span><span class="sxs-lookup"><span data-stu-id="8d869-177">A socket operation encountered a dead network.</span></span> <span data-ttu-id="8d869-178">Dieser Fehler wird zurückgegeben, wenn das Netzwerk Subsystem fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="8d869-178">This error is returned if the network subsystem has failed.</span></span> |
| <span data-ttu-id="8d869-179">**Wsaumotsock**</span><span class="sxs-lookup"><span data-stu-id="8d869-179">**WSAENOTSOCK**</span></span> | <span data-ttu-id="8d869-180">Es wurde versucht, einen Vorgang für etwas auszuführen, das kein Socket ist.</span><span class="sxs-lookup"><span data-stu-id="8d869-180">An operation was attempted on something that is not a socket.</span></span> <span data-ttu-id="8d869-181">Dieser Fehler wird zurückgegeben, wenn es sich bei den *Deskriptoren nicht* um einen Socket handelt.</span><span class="sxs-lookup"><span data-stu-id="8d869-181">This error is returned if the descriptor *s* is not a socket.</span></span> |
| <span data-ttu-id="8d869-182">**WSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="8d869-182">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="8d869-183">Der versuchte Vorgang wird für den Typ des Objekts, auf das verwiesen wird, nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8d869-183">The attempted operation is not supported for the type of object referenced.</span></span> <span data-ttu-id="8d869-184">Dieser Fehler wird zurückgegeben, wenn der angegebene ioctl-Befehl nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="8d869-184">This error is returned if the specified IOCTL command is not supported.</span></span> <span data-ttu-id="8d869-185">Dieser Fehler wird auch zurückgegeben, wenn der IOCTL-Pfad für die hoch- **\_ Loopback \_ \_** -Schleife vom Transportanbieter nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="8d869-185">This error is also returned if the **SIO\_LOOPBACK\_FAST\_PATH** IOCTL is not supported by the transport provider.</span></span> |

## <a name="remarks"></a><span data-ttu-id="8d869-186">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8d869-186">Remarks</span></span>

<span data-ttu-id="8d869-187">Eine Anwendung kann die IOCTL-Schleife für den **\_ \_ schnellen \_ Loopback** Bereich verwenden, um die Latenz zu verringern und die Leistung von Loopback Vorgängen auf einem TCP-Socket zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="8d869-187">An application can use the **SIO\_LOOPBACK\_FAST\_PATH** IOCTL to reduce the latency and improve the performance of loopback operations on a TCP socket.</span></span>
<span data-ttu-id="8d869-188">Diese IOCTL fordert an, dass der TCP/IP-Stapel einen speziellen schnellen Pfad für Loopback Vorgänge in diesem Socket verwendet.</span><span class="sxs-lookup"><span data-stu-id="8d869-188">This IOCTL requests that the TCP/IP stack uses a special fast path for loopback operations on this socket.</span></span>
<span data-ttu-id="8d869-189">Die IOCTL-Schleife für den " **SIO \_ Loopback \_ \_** " kann nur mit TCP-Sockets verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8d869-189">The **SIO\_LOOPBACK\_FAST\_PATH** IOCTL can be used only with TCP sockets.</span></span>
<span data-ttu-id="8d869-190">Diese IOCTL muss auf beiden Seiten der Loopback Sitzung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8d869-190">This IOCTL must be used on both sides of the loopback session.</span></span>
<span data-ttu-id="8d869-191">Der schnelle TCP-Loopback Pfad wird entweder über die IPv4-oder IPv6-loopback Schnittstelle unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8d869-191">The TCP loopback fast path is supported using either the IPv4 or IPv6 loopback interface.</span></span>

<span data-ttu-id="8d869-192">Der Socket, der die Verbindungsanforderung initiieren soll, muss diese IOCTL vor dem Herstellen der Verbindungsanforderung anwenden.</span><span class="sxs-lookup"><span data-stu-id="8d869-192">The socket that plans to initiate the connection request must apply this IOCTL before making the connection request.</span></span>
<span data-ttu-id="8d869-193">Der von der [**Connect**](/windows/desktop/api/winsock2/nf-winsock2-connect)-, [**connectex**](/windows/desktop/api/mswsock/nc-mswsock-lpfn_connectex)-, [**wsaconnect**](/windows/desktop/api/winsock2/nf-winsock2-wsaconnect)-, [**wsaconnectbylist**](/windows/desktop/api/winsock2/nf-winsock2-wsaconnectbylist)-oder [**WSAConnectByName**](/windows/desktop/api/winsock2/nf-winsock2-wsaconnectbynamew) -Funktion verwendete Socket zum Initiieren der Verbindung muss daher diese IOCTL anwenden, um den schnellen Pfad für Loopback Vorgänge zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="8d869-193">So the socket used by the [**connect**](/windows/desktop/api/winsock2/nf-winsock2-connect), [**ConnectEx**](/windows/desktop/api/mswsock/nc-mswsock-lpfn_connectex), [**WSAConnect**](/windows/desktop/api/winsock2/nf-winsock2-wsaconnect), [**WSAConnectByList**](/windows/desktop/api/winsock2/nf-winsock2-wsaconnectbylist), or [**WSAConnectByName**](/windows/desktop/api/winsock2/nf-winsock2-wsaconnectbynamew) function to initiate the connection must apply this IOCTL to use the fast path for loopback operations.</span></span>

<span data-ttu-id="8d869-194">Der Socket, der die Verbindungsanforderung überwacht, muss diese IOCTL anwenden, bevor die Verbindung akzeptiert wird.</span><span class="sxs-lookup"><span data-stu-id="8d869-194">The socket that is listening for the connection request must apply this IOCTL before accepting the connection.</span></span>
<span data-ttu-id="8d869-195">Der von der Funktion "lauschen" verwendete Socket muss daher diese IOCTL anwenden, sodass alle akzeptierten Sockets den schnellen Pfad für Loopback verwenden.</span><span class="sxs-lookup"><span data-stu-id="8d869-195">So the socket used by the listen function must apply this IOCTL so any sockets that are accepted will use the fast path for loopback.</span></span>
<span data-ttu-id="8d869-196">Alle Sockets, die von der Funktion "lauschen" zurückgegeben und an die Funktion " [**Accept**](/windows/desktop/api/winsock2/nf-winsock2-accept)", " [**Accept**](/windows/desktop/api/winsock/nf-winsock-acceptex)" oder " [**wsaaccept**](/windows/desktop/api/winsock2/nf-winsock2-wsaaccept) " übermittelt werden, werden für die Verwendung des speziellen schnellen Pfads für Loopback Vorgänge</span><span class="sxs-lookup"><span data-stu-id="8d869-196">Any sockets returned by the listen function and passed to the [**accept**](/windows/desktop/api/winsock2/nf-winsock2-accept), [**AcceptEx**](/windows/desktop/api/winsock/nf-winsock-acceptex), or [**WSAAccept**](/windows/desktop/api/winsock2/nf-winsock2-wsaaccept) function will be marked to use the special fast path for loopback operations.</span></span>

<span data-ttu-id="8d869-197">Sobald eine Anwendung die Verbindung über eine Loopback Schnittstelle mithilfe des schnellen Pfads herstellt, müssen alle Pakete für die Lebensdauer der Verbindung den schnellen Pfad verwenden.</span><span class="sxs-lookup"><span data-stu-id="8d869-197">Once an application establishes the connection on a loopback interface using the fast path, all packets for the lifetime of the connection must use the fast path.</span></span>

<span data-ttu-id="8d869-198">Wenn Sie den **\_ \_ schnellen \_ Pfad von SIO Loopback** auf einen Socket anwenden, der mit einem nicht-Loopback Pfad verbunden wird, hat dies keine Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="8d869-198">Applying **SIO\_LOOPBACK\_FAST\_PATH** to a socket which will be connected to a non-loopback path will have no effect.</span></span>

<span data-ttu-id="8d869-199">Diese TCP-Loopback Optimierung führt zu Paketen, die über die Transport Schicht (TL) statt über das herkömmliche Loopback durch die Netzwerkschicht fließen.</span><span class="sxs-lookup"><span data-stu-id="8d869-199">This TCP loopback optimization results in packets that flow through the Transport Layer (TL) instead of the traditional loopback through the Network Layer.</span></span>
<span data-ttu-id="8d869-200">Diese Optimierung erhöht die Latenz für Loopback Pakete.</span><span class="sxs-lookup"><span data-stu-id="8d869-200">This optimization improves the latency for loopback packets.</span></span>
<span data-ttu-id="8d869-201">Wenn sich eine Anwendung für eine Einstellung auf Verbindungs Ebene für die Verwendung des schnellen Loopbacks-Pfads entscheidet, werden alle Pakete dem Loopback Pfad folgen.</span><span class="sxs-lookup"><span data-stu-id="8d869-201">Once an application opts in for a connection level setting to use the loopback fast path, all packets will follow the loopback path.</span></span>
<span data-ttu-id="8d869-202">Bei der Loopback Kommunikation werden Überlastung und Paket Ablagevorgang nicht erwartet.</span><span class="sxs-lookup"><span data-stu-id="8d869-202">For loopback communications, congestion and packet drop are not expected.</span></span>
<span data-ttu-id="8d869-203">Das Konzept der Überlastungs Steuerung und der zuverlässigen Übermittlung in TCP ist unnötig.</span><span class="sxs-lookup"><span data-stu-id="8d869-203">The notion of congestion control and reliable delivery in TCP will be unnecessary.</span></span>
<span data-ttu-id="8d869-204">Dies gilt jedoch nicht für die Fluss Steuerung.</span><span class="sxs-lookup"><span data-stu-id="8d869-204">This, however, is not true for flow control.</span></span>
<span data-ttu-id="8d869-205">Ohne Fluss Steuerung kann der Absender den Empfangs Puffer überlasten, was zu einem fehlerhaften TCP-Loopback Verhalten führt.</span><span class="sxs-lookup"><span data-stu-id="8d869-205">Without flow control, the sender can overwhelm the receive buffer, leading to erroneous TCP loopback behavior.</span></span>
<span data-ttu-id="8d869-206">Die Fluss Steuerung im TCP-optimierten Loopback Pfad wird durch das Platzieren von Sende Anforderungen in einer Warteschlange beibehalten.</span><span class="sxs-lookup"><span data-stu-id="8d869-206">The flow control in the TCP optimized loopback path is maintained by placing send requests in a queue.</span></span>
<span data-ttu-id="8d869-207">Wenn der Empfangs Puffer voll ist, gewährleistet der TCP/IP-Stapel, dass die Sende Vorgänge nicht vollständig ausgeführt werden, bis die Warteschlange gewartet hat</span><span class="sxs-lookup"><span data-stu-id="8d869-207">When receive buffer is full, the TCP/IP stack guarantees that the sends won't complete until the queue is serviced maintaining flow control.</span></span>

<span data-ttu-id="8d869-208">TCP-schnell Pfad Loopback Verbindungen bei vorhanden sein einer Windows-Filter Plattform (WFP) für Verbindungsdaten müssen den nicht optimierten langsamen Pfad für Loopback annehmen.</span><span class="sxs-lookup"><span data-stu-id="8d869-208">TCP fast path loopback connections in the presence of a Windows Filtering Platform (WFP) callout for connection data must take the un-optimized slow path for loopback.</span></span>
<span data-ttu-id="8d869-209">WFP-Filter verhindern also, dass dieser neue schnelle Pfad für Loopbacks verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8d869-209">So WFP filters will prevent this new loopback fast path from being used.</span></span>
<span data-ttu-id="8d869-210">Wenn ein WFP-Filter aktiviert ist, wird der langsame Pfad auch dann verwendet, wenn der IOCTL-Wert für den **\_ \_ schnell \_ Pfad für "sio Loopback** " festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="8d869-210">When a WFP filter is enabled, the system we will use the slow path even if the **SIO\_LOOPBACK\_FAST\_PATH** IOCTL was set.</span></span>
<span data-ttu-id="8d869-211">Dadurch wird sichergestellt, dass Benutzermodus-Anwendungen über die gesamte WFP-Sicherheitsfunktion verfügen.</span><span class="sxs-lookup"><span data-stu-id="8d869-211">This ensures that user-mode applications have the full WFP security capability.</span></span>

<span data-ttu-id="8d869-212">Standardmäßig ist **der \_ \_ schnelle \_ Pfad** für die hoch-Loopback Option deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="8d869-212">By default, **SIO\_LOOPBACK\_FAST\_PATH** is disabled.</span></span>

<span data-ttu-id="8d869-213">Es wird nur eine Teilmenge der TCP/IP-Socketoptionen unterstützt, wenn die IOCTL-Schleife für den Schleifen-Schleifen- **\_ \_ schnell \_ Pfad** verwendet wird, um den schnellen Loopback Pfad für einen Socket zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="8d869-213">Only a subset of the TCP/IP socket options are supported when the **SIO\_LOOPBACK\_FAST\_PATH** IOCTL is used to enable the loopback fast path on a socket.</span></span>
<span data-ttu-id="8d869-214">Die Liste der unterstützten Optionen umfasst Folgendes:</span><span class="sxs-lookup"><span data-stu-id="8d869-214">The list of supported options includes the following:</span></span>

* <span data-ttu-id="8d869-215">**IP- \_ TTL**</span><span class="sxs-lookup"><span data-stu-id="8d869-215">**IP\_TTL**</span></span>
* <span data-ttu-id="8d869-216">**IP- \_ Unicast \_ if**</span><span class="sxs-lookup"><span data-stu-id="8d869-216">**IP\_UNICAST\_IF**</span></span>
* <span data-ttu-id="8d869-217">**IPv6- \_ \_ unicasthops**</span><span class="sxs-lookup"><span data-stu-id="8d869-217">**IPV6\_UNICAST\_HOPS**</span></span>
* <span data-ttu-id="8d869-218">**IPv6- \_ Unicast, \_ Wenn**</span><span class="sxs-lookup"><span data-stu-id="8d869-218">**IPV6\_UNICAST\_IF**</span></span>
* <span data-ttu-id="8d869-219">**IPv6- \_ V6ONLY**</span><span class="sxs-lookup"><span data-stu-id="8d869-219">**IPV6\_V6ONLY**</span></span>
* <span data-ttu-id="8d869-220">**\_bedingte \_ Annahme**</span><span class="sxs-lookup"><span data-stu-id="8d869-220">**SO\_CONDITIONAL\_ACCEPT**</span></span>
* <span data-ttu-id="8d869-221">**" \_ exclusiveaddruse"**</span><span class="sxs-lookup"><span data-stu-id="8d869-221">**SO\_EXCLUSIVEADDRUSE**</span></span>
* <span data-ttu-id="8d869-222">**\_Port \_ Skalierbarkeit**</span><span class="sxs-lookup"><span data-stu-id="8d869-222">**SO\_PORT\_SCALABILITY**</span></span>
* <span data-ttu-id="8d869-223">**\_rcvbuf**</span><span class="sxs-lookup"><span data-stu-id="8d869-223">**SO\_RCVBUF**</span></span>
* <span data-ttu-id="8d869-224">**\_reuseaddr**</span><span class="sxs-lookup"><span data-stu-id="8d869-224">**SO\_REUSEADDR**</span></span>
* <span data-ttu-id="8d869-225">**TCP- \_ bsdurgent**</span><span class="sxs-lookup"><span data-stu-id="8d869-225">**TCP\_BSDURGENT**</span></span>

## <a name="see-also"></a><span data-ttu-id="8d869-226">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8d869-226">See also</span></span>

[<span data-ttu-id="8d869-227">**IPPROTO_IP Socketoptionen**</span><span class="sxs-lookup"><span data-stu-id="8d869-227">**IPPROTO_IP Socket Options**</span></span>](/windows/desktop/winsock/ipproto-ip-socket-options)

[<span data-ttu-id="8d869-228">**IPPROTO_IPV6 Socketoptionen**</span><span class="sxs-lookup"><span data-stu-id="8d869-228">**IPPROTO_IPV6 Socket Options**</span></span>](/windows/desktop/winsock/ipproto-ipv6-socket-options)

[<span data-ttu-id="8d869-229">**IPPROTO_TCP Socketoptionen**</span><span class="sxs-lookup"><span data-stu-id="8d869-229">**IPPROTO_TCP Socket Options**</span></span>](/windows/desktop/winsock/ipproto-tcp-socket-options)

[<span data-ttu-id="8d869-230">**Glühbirne**</span><span class="sxs-lookup"><span data-stu-id="8d869-230">**socket**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="8d869-231">**SOL_SOCKET Socketoptionen**</span><span class="sxs-lookup"><span data-stu-id="8d869-231">**SOL_SOCKET Socket Options**</span></span>](/windows/desktop/winsock/sol-socket-socket-options)

[<span data-ttu-id="8d869-232">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="8d869-232">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[<span data-ttu-id="8d869-233">**Wsagein verlappedresult**</span><span class="sxs-lookup"><span data-stu-id="8d869-233">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="8d869-234">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="8d869-234">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="8d869-235">**Wsaoverlgetauscht**</span><span class="sxs-lookup"><span data-stu-id="8d869-235">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="8d869-236">**Wsasocketa**</span><span class="sxs-lookup"><span data-stu-id="8d869-236">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="8d869-237">**Wsasocketw**</span><span class="sxs-lookup"><span data-stu-id="8d869-237">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
