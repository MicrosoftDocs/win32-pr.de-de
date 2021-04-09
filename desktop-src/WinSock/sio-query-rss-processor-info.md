---
description: Steuerungs Code fragt die Zuordnung zwischen einem Socket und einem RSS-Prozessor Core und einem NUMA-Knoten ab.
ms.assetid: DAF18C92-B479-474F-B438-0746CBA20653
title: SIO_QUERY_RSS_PROCESSOR_INFO Steuerungs Codes
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: a2d251fa4fee996adaec51599e7b1d140a296b89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958921"
---
# <a name="sio_query_rss_processor_info-control-code"></a><span data-ttu-id="2cc22-103">SIO_QUERY_RSS_PROCESSOR_INFO Steuerungs Codes</span><span class="sxs-lookup"><span data-stu-id="2cc22-103">SIO_QUERY_RSS_PROCESSOR_INFO Control Code</span></span>

## <a name="description"></a><span data-ttu-id="2cc22-104">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2cc22-104">Description</span></span>

<span data-ttu-id="2cc22-105">Der Code der **\_ RSS-Abfrage-RSS- \_ \_ Prozessor \_ Info-Abfrage** steuert die Zuordnung zwischen einem Socket und einem RSS-Prozessor Core und einem NUMA-Knoten.</span><span class="sxs-lookup"><span data-stu-id="2cc22-105">The **SIO\_QUERY\_RSS\_PROCESSOR\_INFO** control code queries the association between a socket and an RSS processor core and NUMA node.</span></span>

<span data-ttu-id="2cc22-106">Um diesen Vorgang auszuführen, wenden Sie die [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) -oder **wspioctl** -Funktion mit den folgenden Parametern an.</span><span class="sxs-lookup"><span data-stu-id="2cc22-106">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_QUERY_RSS_PROCESSOR_INFO, // dwIoControlCode
  NULL,                         // lpvInBuffer
  0,                            // cbInBuffer
  (LPVOID) lpvOutBuffer,         // output buffer
  (DWORD) cbOutBuffer,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_QUERY_RSS_PROCESSOR_INFO, // dwIoControlCode
  NULL,                         // lpvInBuffer
  0,                            // cbInBuffer
  (LPVOID) lpvOutBuffer,         // output buffer
  (DWORD) cbOutBuffer,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,   // a WSATHREADID structure
  (LPINT) lpErrno   // a pointer to the error code.
);
```

## <a name="parameters"></a><span data-ttu-id="2cc22-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="2cc22-107">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="2cc22-108">s</span><span class="sxs-lookup"><span data-stu-id="2cc22-108">s</span></span>

<span data-ttu-id="2cc22-109">Ein Deskriptor, der einen Socket identifiziert.</span><span class="sxs-lookup"><span data-stu-id="2cc22-109">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="2cc22-110">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="2cc22-110">dwIoControlCode</span></span>

<span data-ttu-id="2cc22-111">Der Steuerelement Code für den Vorgang.</span><span class="sxs-lookup"><span data-stu-id="2cc22-111">The control code for the operation.</span></span>
<span data-ttu-id="2cc22-112">Verwenden Sie für diesen Vorgang die RSS-Abfrage für die **\_ \_ RSS- \_ \_ Abfrage** .</span><span class="sxs-lookup"><span data-stu-id="2cc22-112">Use **SIO\_QUERY\_RSS\_PROCESSOR\_INFO** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="2cc22-113">lpvinbuffer</span><span class="sxs-lookup"><span data-stu-id="2cc22-113">lpvInBuffer</span></span>

<span data-ttu-id="2cc22-114">Ein Zeiger auf den Eingabepuffer.</span><span class="sxs-lookup"><span data-stu-id="2cc22-114">A pointer to the input buffer.</span></span>
<span data-ttu-id="2cc22-115">Dieser Parameter wird für diesen Vorgang nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="2cc22-115">This parameter is unused for this operation.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="2cc22-116">cbinbuffer</span><span class="sxs-lookup"><span data-stu-id="2cc22-116">cbInBuffer</span></span>

<span data-ttu-id="2cc22-117">Die Größe des Eingabe Puffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="2cc22-117">The size, in bytes, of the input buffer.</span></span>
<span data-ttu-id="2cc22-118">Dieser Parameter wird für diesen Vorgang nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="2cc22-118">This parameter is unused for this operation.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="2cc22-119">lpvoutbuffer</span><span class="sxs-lookup"><span data-stu-id="2cc22-119">lpvOutBuffer</span></span>

<span data-ttu-id="2cc22-120">Ein Zeiger auf den Ausgabepuffer.</span><span class="sxs-lookup"><span data-stu-id="2cc22-120">A pointer to the output buffer.</span></span>
<span data-ttu-id="2cc22-121">Dieser Parameter sollte auf eine [**Affinitäts Struktur des \_ socketprozessors \_**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) zeigen, wenn die Parameter *lpoverlgetauscht* und *lpCompletionRoutine* **null** sind.</span><span class="sxs-lookup"><span data-stu-id="2cc22-121">This parameter should point to a [**SOCKET\_PROCESSOR\_AFFINITY**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) structure if the *lpOverlapped* and *lpCompletionRoutine* parameters are **NULL**.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="2cc22-122">cboutbuffer</span><span class="sxs-lookup"><span data-stu-id="2cc22-122">cbOutBuffer</span></span>

<span data-ttu-id="2cc22-123">Die Größe des Ausgabepuffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="2cc22-123">The size, in bytes, of the output buffer.</span></span>
<span data-ttu-id="2cc22-124">Dieser Parameter muss mindestens die Größe einer [**\_ socketprozessoraffinitäts \_**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) -Struktur aufweisen.</span><span class="sxs-lookup"><span data-stu-id="2cc22-124">This parameter must be at least the size of a [**SOCKET\_PROCESSOR\_AFFINITY**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) structure.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="2cc22-125">lpcbbyteszurück gegeben</span><span class="sxs-lookup"><span data-stu-id="2cc22-125">lpcbBytesReturned</span></span>

<span data-ttu-id="2cc22-126">Ein Zeiger auf eine Variable, die die Größe der im Ausgabepuffer gespeicherten Daten (in Bytes) empfängt.</span><span class="sxs-lookup"><span data-stu-id="2cc22-126">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>

<span data-ttu-id="2cc22-127">Wenn der Ausgabepuffer zu klein ist, schlägt der-Befehl fehl, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) gibt [**WSAEINVAL**](windows-sockets-error-codes-2.md)zurück, und der *lpcbbytesreturns* -Parameter verweist auf den *DWORD* -Wert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="2cc22-127">If the output buffer is too small, the call fails, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns [**WSAEINVAL**](windows-sockets-error-codes-2.md), and the *lpcbBytesReturned* parameter points to a *DWORD* value of zero.</span></span>

<span data-ttu-id="2cc22-128">Wenn *lpoverlgetauscht* gleich **null** ist, kann der **DWORD** -Wert, auf den der *lpcbbytesall* -Parameter verweist, der bei einem erfolgreichen-Vorgang zurückgegeben wird, nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="2cc22-128">If *lpOverlapped* is **NULL**, the **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned on a successful call cannot be zero.</span></span>

<span data-ttu-id="2cc22-129">Wenn der *lpoverllapp* -Parameter für überlappende Sockets nicht **null** ist, werden Vorgänge, die nicht sofort abgeschlossen werden können, initiiert, und der Abschluss wird zu einem späteren Zeitpunkt angegeben.</span><span class="sxs-lookup"><span data-stu-id="2cc22-129">If the *lpOverlapped* parameter is not **NULL** for overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>
<span data-ttu-id="2cc22-130">Der **DWORD** -Wert, auf den der zurückgegebene *lpcbbyteszurück gegebene* Parameter verweist, kann NULL sein, da die Größe der gespeicherten Daten erst bestimmt werden kann, wenn der überlappende Vorgang abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="2cc22-130">The **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned may be zero since the size of the data stored can't be determined until the overlapped operation has completed.</span></span>
<span data-ttu-id="2cc22-131">Der endgültige Abschluss Status kann abgerufen werden, wenn die geeignete Vervollständigungs Methode signalisiert wird, wenn der Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="2cc22-131">The final completion status can be retrieved when the appropriate completion method is signaled when the operation has completed.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="2cc22-132">lpvoverlgetauscht</span><span class="sxs-lookup"><span data-stu-id="2cc22-132">lpvOverlapped</span></span>

<span data-ttu-id="2cc22-133">Ein Zeiger auf eine [**wsaoverllapp**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="2cc22-133">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="2cc22-134">Wenn Socket *s* ohne das überlappende Attribut erstellt wurde, wird der *lpoverllapp* -Parameter ignoriert.</span><span class="sxs-lookup"><span data-stu-id="2cc22-134">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="2cc22-135">Wenn *s* mit dem überlappenden Attribut geöffnet wurde und der *lpoverlgetauscht* -Parameter nicht **null** ist, wird der Vorgang als überlappende (asynchrone) Operation ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2cc22-135">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="2cc22-136">In diesem Fall muss der *lpoverllapp* -Parameter auf eine gültige [**wsaoverllapp**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) -Struktur zeigen.</span><span class="sxs-lookup"><span data-stu-id="2cc22-136">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="2cc22-137">Bei überlappenden Vorgängen gibt die Funktion [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) oder **wspioctl** sofort zurück, und die entsprechende Vervollständigungs Methode wird signalisiert, wenn der Vorgang abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="2cc22-137">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="2cc22-138">Andernfalls gibt die Funktion nicht zurück, bis der Vorgang abgeschlossen ist oder ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="2cc22-138">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="2cc22-139">lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="2cc22-139">lpCompletionRoutine</span></span>

<span data-ttu-id="2cc22-140">Typ: \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="2cc22-140">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="2cc22-141">Ein Zeiger auf die Vervollständigungs Routine, die aufgerufen wird, wenn der Vorgang abgeschlossen wurde (bei nicht überlappenden Sockets ignoriert).</span><span class="sxs-lookup"><span data-stu-id="2cc22-141">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="2cc22-142">lpthreadid</span><span class="sxs-lookup"><span data-stu-id="2cc22-142">lpThreadId</span></span>

<span data-ttu-id="2cc22-143">Ein Zeiger auf eine [**wsathreadid**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) -Struktur, die vom Anbieter in einem nachfolgenden [**wpuqueueapc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc)-Rückruf verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="2cc22-143">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="2cc22-144">Der Anbieter sollte die referenzierte [**wsathreadid**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) -Struktur (nicht den Zeiger auf dieselbe) speichern, bis die [**wpuqueueapc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc) -Funktion zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="2cc22-144">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="2cc22-145">**Hinweis**  Dieser Parameter gilt nur für die **wspioctl** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="2cc22-145">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="2cc22-146">lperrno</span><span class="sxs-lookup"><span data-stu-id="2cc22-146">lpErrno</span></span>

<span data-ttu-id="2cc22-147">Ein Zeiger auf den Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="2cc22-147">A pointer to the error code.</span></span>

<span data-ttu-id="2cc22-148">**Hinweis**  Dieser Parameter gilt nur für die **wspioctl** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="2cc22-148">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="2cc22-149">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2cc22-149">Return value</span></span>

<span data-ttu-id="2cc22-150">Wenn der Vorgang erfolgreich abgeschlossen wird, gibt die [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) -oder **wspioctl** -Funktion NULL zurück.</span><span class="sxs-lookup"><span data-stu-id="2cc22-150">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="2cc22-151">Wenn der Vorgang fehlschlägt oder aussteht, gibt die Funktion [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) oder **wspioctl** einen **\_ Socketfehler** zurück.</span><span class="sxs-lookup"><span data-stu-id="2cc22-151">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="2cc22-152">Um erweiterte Fehlerinformationen abzurufen, nennen Sie [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="2cc22-152">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="2cc22-153">Fehlercode</span><span class="sxs-lookup"><span data-stu-id="2cc22-153">Error code</span></span> | <span data-ttu-id="2cc22-154">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="2cc22-154">Meaning</span></span> |
|------------|---------|
| <span data-ttu-id="2cc22-155">**Fehler \_ beim \_ Puffer.**</span><span class="sxs-lookup"><span data-stu-id="2cc22-155">**ERROR\_INSUFFICIENT\_BUFFER**</span></span> | <span data-ttu-id="2cc22-156">Der an einen System Rückruf über gegebene Datenbereich ist zu klein.</span><span class="sxs-lookup"><span data-stu-id="2cc22-156">The data area passed to a system call is too small.</span></span> <span data-ttu-id="2cc22-157">Dieser Fehler wird zurückgegeben, wenn der Puffer, auf den der *lpvoutbuffer* -Parameter verweist, eine Puffergröße hat, die im *cboutbuffer* -Parameter übergeben wurde, zu klein ist.</span><span class="sxs-lookup"><span data-stu-id="2cc22-157">This error is returned if the buffer pointed to by the *lpvOutBuffer* parameter with a buffer size passed in the *cbOutBuffer* parameter is too small.</span></span> <span data-ttu-id="2cc22-158">Die erforderliche Puffergröße wird im Parameter " *lpcbbytes}* " zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2cc22-158">The buffer size required will be returned in the *lpcbBytesReturned* parameter.</span></span> <span data-ttu-id="2cc22-159">Dieser Fehler wird zurückgegeben, wenn der *cboutbuffer* -Parameter kleiner als die Größe [**einer \_ socketprozessoraffinitäts \_**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) -Struktur ist.</span><span class="sxs-lookup"><span data-stu-id="2cc22-159">This error is returned if the *cbOutBuffer* parameter is less than the size of a [**SOCKET\_PROCESSOR\_AFFINITY**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) structure.</span></span> |
| <span data-ttu-id="2cc22-160">**ausstehende WSA-e/a \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2cc22-160">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="2cc22-161">Ein übergebener Vorgang wurde erfolgreich initiiert, und der Abschluss wird zu einem späteren Zeitpunkt angegeben.</span><span class="sxs-lookup"><span data-stu-id="2cc22-161">An overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="2cc22-162">**WSA- \_ Vorgang \_ abgebrochen**</span><span class="sxs-lookup"><span data-stu-id="2cc22-162">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="2cc22-163">Ein über Lapp ender Vorgang wurde aufgrund der Schließung des Sockets oder der Ausführung des Befehls " **SIO \_ Flush** ioctl" abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="2cc22-163">An overlapped operation was canceled due to the closure of the socket or the execution of the **SIO\_FLUSH** IOCTL command.</span></span> |
| <span data-ttu-id="2cc22-164">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="2cc22-164">**WSAEFAULT**</span></span> | <span data-ttu-id="2cc22-165">Der Parameter " *lpvinbuffer*", " *lpvoutbuffer*", " *lpcbbytesgab*", " *lpoverlgetauscht* " oder " *lpCompletionRoutine* " ist nicht vollständig in einem gültigen Teil des Benutzer Adressraums enthalten.</span><span class="sxs-lookup"><span data-stu-id="2cc22-165">The *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="2cc22-166">**Wsaeingabe Progress**</span><span class="sxs-lookup"><span data-stu-id="2cc22-166">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="2cc22-167">Die-Funktion wird aufgerufen, wenn ein Rückruf ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2cc22-167">The function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="2cc22-168">**Wsaeingabe**</span><span class="sxs-lookup"><span data-stu-id="2cc22-168">**WSAEINTR**</span></span> | <span data-ttu-id="2cc22-169">Ein Blockierungs Vorgang wurde unterbrochen.</span><span class="sxs-lookup"><span data-stu-id="2cc22-169">A blocking operation was interrupted.</span></span> |
| <span data-ttu-id="2cc22-170">**Wsaabval**</span><span class="sxs-lookup"><span data-stu-id="2cc22-170">**WSAEINVAL**</span></span> | <span data-ttu-id="2cc22-171">Der *dwIoControlCode* -Parameter ist kein gültiger Befehl, oder ein angegebener Eingabeparameter ist nicht zulässig, oder der Befehl ist nicht auf den angegebenen Sockettyp anwendbar.</span><span class="sxs-lookup"><span data-stu-id="2cc22-171">The *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> <span data-ttu-id="2cc22-172">Dieser Fehler wird zurückgegeben, wenn der *cboutbuffer* -Parameter kleiner als die Größe [**einer \_ socketprozessoraffinitäts \_**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) -Struktur ist.</span><span class="sxs-lookup"><span data-stu-id="2cc22-172">This error is returned if the *cbOutBuffer* parameter is less than the size of a [**SOCKET\_PROCESSOR\_AFFINITY**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) structure.</span></span>
| <span data-ttu-id="2cc22-173">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="2cc22-173">**WSAENETDOWN**</span></span> | <span data-ttu-id="2cc22-174">Das Netzwerk Subsystem ist fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="2cc22-174">The network subsystem has failed.</span></span> |
| <span data-ttu-id="2cc22-175">**Wsaumoproumopt**</span><span class="sxs-lookup"><span data-stu-id="2cc22-175">**WSAENOPROTOOPT**</span></span> | <span data-ttu-id="2cc22-176">Die Socketoption wird für das angegebene Protokoll nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2cc22-176">The socket option is not supported on the specified protocol.</span></span> |
| <span data-ttu-id="2cc22-177">**WSAENOTCONN**</span><span class="sxs-lookup"><span data-stu-id="2cc22-177">**WSAENOTCONN**</span></span> | <span data-ttu-id="2cc22-178">Die Socket *s* ist nicht verbunden.</span><span class="sxs-lookup"><span data-stu-id="2cc22-178">The socket *s* is not connected.</span></span> |
| <span data-ttu-id="2cc22-179">**Wsaumotsock**</span><span class="sxs-lookup"><span data-stu-id="2cc22-179">**WSAENOTSOCK**</span></span> | <span data-ttu-id="2cc22-180">Der Deskriptor *s* ist kein Socket.</span><span class="sxs-lookup"><span data-stu-id="2cc22-180">The descriptor *s* is not a socket.</span></span> |
| <span data-ttu-id="2cc22-181">**WSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="2cc22-181">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="2cc22-182">Der angegebene ioctl-Befehl wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2cc22-182">The specified IOCTL command is not supported.</span></span> <span data-ttu-id="2cc22-183">Dieser Fehler wird zurückgegeben, wenn die vom Transportanbieter nicht unterstützte ioctl-Abfrage für die **\_ RSS-Abfrage-RSS- \_ \_ \_ Verarbeitung** von der</span><span class="sxs-lookup"><span data-stu-id="2cc22-183">This error is returned if the **SIO\_QUERY\_RSS\_PROCESSOR\_INFO** IOCTL is not supported by the transport provider.</span></span> |

## <a name="remarks"></a><span data-ttu-id="2cc22-184">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2cc22-184">Remarks</span></span>

<span data-ttu-id="2cc22-185">Die Konfigurations-ioctl für die **\_ RSS-Abfrage \_ RSS \_ \_ -Abfrage** wird unter Windows 8, Windows Server 2012 und neueren Versionen des Betriebssystems unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2cc22-185">The **SIO\_QUERY\_RSS\_PROCESSOR\_INFO** IOCTL is supported on Windows 8, and Windows Server 2012, and later versions of the operating system.</span></span>

<span data-ttu-id="2cc22-186">Die Informationen ioctl der **\_ Prozessor-Abfrage \_ RSS \_ \_ -Abfrage** wird verwendet, um die Zuordnung zwischen einem Socket und einem RSS-Prozessor Core und einem NUMA-Knoten zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="2cc22-186">The **SIO\_QUERY\_RSS\_PROCESSOR\_INFO** IOCTL is used to determine the association between a socket and an RSS processor core and NUMA node.</span></span>
<span data-ttu-id="2cc22-187">Diese IOCTL gibt eine [**\_ socketprozessoraffinitäts \_**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) -Struktur zurück, die die [**Prozessor \_ Nummer**](/windows/desktop/api/winnt/ns-winnt-processor_number) und die NUMA-Knoten-ID enthält.</span><span class="sxs-lookup"><span data-stu-id="2cc22-187">This IOCTL returns a [**SOCKET\_PROCESSOR\_AFFINITY**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) structure that contains the [**PROCESSOR\_NUMBER**](/windows/desktop/api/winnt/ns-winnt-processor_number) and the NUMA node ID.</span></span>
<span data-ttu-id="2cc22-188">Die zurückgegebene [**Prozessor \_ Zahlen**](/windows/desktop/api/winnt/ns-winnt-processor_number) Struktur enthält eine Gruppennummer und eine relative Prozessornummer in der Gruppe.</span><span class="sxs-lookup"><span data-stu-id="2cc22-188">The returned [**PROCESSOR\_NUMBER**](/windows/desktop/api/winnt/ns-winnt-processor_number) structure contains a group number and relative processor number within the group.</span></span>

<span data-ttu-id="2cc22-189">Wenn es sich bei dem Socket um einen UDP-Socket handelt, muss der Socket verbunden sein, damit die IOCTL- **Abfrage "RSS-Abfrage-RSS- \_ \_ \_ Prozessor \_ Informationen** "</span><span class="sxs-lookup"><span data-stu-id="2cc22-189">If the socket is a UDP socket, the socket must be connected for the **SIO\_QUERY\_RSS\_PROCESSOR\_INFO** IOCTL to work properly.</span></span>

## <a name="see-also"></a><span data-ttu-id="2cc22-190">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2cc22-190">See also</span></span>

[<span data-ttu-id="2cc22-191">**PROCESSOR_NUMBER**</span><span class="sxs-lookup"><span data-stu-id="2cc22-191">**PROCESSOR_NUMBER**</span></span>](/windows/desktop/api/winnt/ns-winnt-processor_number)

[<span data-ttu-id="2cc22-192">**Glühbirne**</span><span class="sxs-lookup"><span data-stu-id="2cc22-192">**socket**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="2cc22-193">**SOCKET_PROCESSOR_AFFINITY**</span><span class="sxs-lookup"><span data-stu-id="2cc22-193">**SOCKET_PROCESSOR_AFFINITY**</span></span>](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity)

[<span data-ttu-id="2cc22-194">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="2cc22-194">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)

[<span data-ttu-id="2cc22-195">**Wsagein verlappedresult**</span><span class="sxs-lookup"><span data-stu-id="2cc22-195">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="2cc22-196">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="2cc22-196">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="2cc22-197">**Wsaoverlgetauscht**</span><span class="sxs-lookup"><span data-stu-id="2cc22-197">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="2cc22-198">**Wsasocketa**</span><span class="sxs-lookup"><span data-stu-id="2cc22-198">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="2cc22-199">**Wsasocketw**</span><span class="sxs-lookup"><span data-stu-id="2cc22-199">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
