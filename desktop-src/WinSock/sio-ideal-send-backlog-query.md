---
description: Der Steuercode Ruft den idealen Wert für den Sende Rückstand für die zugrunde liegende Verbindung ab.
ms.assetid: 03fe964b-26f7-4af7-83bf-62cc877d01a8
title: SIO_IDEAL_SEND_BACKLOG_QUERY Steuerungs Codes
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 440e42477a8939a62eeb84b800c0fd8feead5aab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351409"
---
# <a name="sio_ideal_send_backlog_query-control-code"></a><span data-ttu-id="51ae7-103">SIO_IDEAL_SEND_BACKLOG_QUERY Steuerungs Codes</span><span class="sxs-lookup"><span data-stu-id="51ae7-103">SIO_IDEAL_SEND_BACKLOG_QUERY Control Code</span></span>

## <a name="description"></a><span data-ttu-id="51ae7-104">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="51ae7-104">Description</span></span>

<span data-ttu-id="51ae7-105">Der optimale Abfrage Steuerungs Code für den " **SIO- \_ \_ \_ senderückstand \_** " Ruft den idealen ISB-Wert (Send Rückstand) für die zugrunde liegende Verbindung ab.</span><span class="sxs-lookup"><span data-stu-id="51ae7-105">The **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** control code retrieves the ideal send backlog (ISB) value for the underlying connection.</span></span>

<span data-ttu-id="51ae7-106">Um diesen Vorgang auszuführen, wenden Sie die [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) -oder **wspioctl** -Funktion mit den folgenden Parametern an.</span><span class="sxs-lookup"><span data-stu-id="51ae7-106">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_IDEAL_SEND_BACKLOG_QUERY, // dwIoControlCode
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
  SIO_IDEAL_SEND_BACKLOG_QUERY, // dwIoControlCode
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

## <a name="parameters"></a><span data-ttu-id="51ae7-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="51ae7-107">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="51ae7-108">s</span><span class="sxs-lookup"><span data-stu-id="51ae7-108">s</span></span>

<span data-ttu-id="51ae7-109">Ein Deskriptor, der einen Socket identifiziert.</span><span class="sxs-lookup"><span data-stu-id="51ae7-109">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="51ae7-110">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="51ae7-110">dwIoControlCode</span></span>

<span data-ttu-id="51ae7-111">Der Steuerelement Code für den Vorgang.</span><span class="sxs-lookup"><span data-stu-id="51ae7-111">The control code for the operation.</span></span>
<span data-ttu-id="51ae7-112">Verwenden Sie für diesen Vorgang die **\_ optimale \_ \_ \_ Abfrage zum Senden** des sendebacklogs.</span><span class="sxs-lookup"><span data-stu-id="51ae7-112">Use **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="51ae7-113">lpvinbuffer</span><span class="sxs-lookup"><span data-stu-id="51ae7-113">lpvInBuffer</span></span>

<span data-ttu-id="51ae7-114">Ein Zeiger auf den Eingabepuffer.</span><span class="sxs-lookup"><span data-stu-id="51ae7-114">A pointer to the input buffer.</span></span>
<span data-ttu-id="51ae7-115">Dieser Parameter wird für diesen Vorgang nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="51ae7-115">This parameter is unused for this operation.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="51ae7-116">cbinbuffer</span><span class="sxs-lookup"><span data-stu-id="51ae7-116">cbInBuffer</span></span>

<span data-ttu-id="51ae7-117">Die Größe des Eingabe Puffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="51ae7-117">The size, in bytes, of the input buffer.</span></span>
<span data-ttu-id="51ae7-118">Dieser Parameter wird für diesen Vorgang nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="51ae7-118">This parameter is unused for this operation.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="51ae7-119">lpvoutbuffer</span><span class="sxs-lookup"><span data-stu-id="51ae7-119">lpvOutBuffer</span></span>

<span data-ttu-id="51ae7-120">Ein Zeiger auf den Ausgabepuffer.</span><span class="sxs-lookup"><span data-stu-id="51ae7-120">A pointer to the output buffer.</span></span>
<span data-ttu-id="51ae7-121">Dieser Parameter sollte auf einen **ulong** -Datentyp zeigen, wenn die Parameter *lpoverlgetauscht* und *lpCompletionRoutine* **null** sind.</span><span class="sxs-lookup"><span data-stu-id="51ae7-121">This parameter should point to a **ULONG** data type if the *lpOverlapped* and *lpCompletionRoutine* parameters are **NULL**.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="51ae7-122">cboutbuffer</span><span class="sxs-lookup"><span data-stu-id="51ae7-122">cbOutBuffer</span></span>

<span data-ttu-id="51ae7-123">Die Größe des Ausgabepuffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="51ae7-123">The size, in bytes, of the output buffer.</span></span>
<span data-ttu-id="51ae7-124">Dieser Parameter muss mindestens die Größe eines **ulong** -Datentyps aufweisen.</span><span class="sxs-lookup"><span data-stu-id="51ae7-124">This parameter must be at least the size of a **ULONG** data type.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="51ae7-125">lpcbbyteszurück gegeben</span><span class="sxs-lookup"><span data-stu-id="51ae7-125">lpcbBytesReturned</span></span>

<span data-ttu-id="51ae7-126">Ein Zeiger auf eine Variable, die die Größe der im Ausgabepuffer gespeicherten Daten (in Bytes) empfängt.</span><span class="sxs-lookup"><span data-stu-id="51ae7-126">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>

<span data-ttu-id="51ae7-127">Wenn der Ausgabepuffer zu klein ist, schlägt der-Befehl fehl, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) gibt [**WSAEINVAL**](windows-sockets-error-codes-2.md)zurück, und der *lpcbbytesreturns* -Parameter verweist auf den **DWORD** -Wert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="51ae7-127">If the output buffer is too small, the call fails, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns [**WSAEINVAL**](windows-sockets-error-codes-2.md), and the *lpcbBytesReturned* parameter points to a **DWORD** value of zero.</span></span>

<span data-ttu-id="51ae7-128">Wenn *lpoverlgetauscht* gleich **null** ist, kann der **DWORD** -Wert, auf den der *lpcbbytesall* -Parameter verweist, der bei einem erfolgreichen-Vorgang zurückgegeben wird, nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="51ae7-128">If *lpOverlapped* is **NULL**, the **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned on a successful call cannot be zero.</span></span>

<span data-ttu-id="51ae7-129">Wenn der *lpoverllapp* -Parameter für überlappende Sockets nicht **null** ist, werden Vorgänge, die nicht sofort abgeschlossen werden können, initiiert, und der Abschluss wird zu einem späteren Zeitpunkt angegeben.</span><span class="sxs-lookup"><span data-stu-id="51ae7-129">If the *lpOverlapped* parameter is not **NULL** for overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>
<span data-ttu-id="51ae7-130">Der **DWORD** -Wert, auf den der zurückgegebene *lpcbbyteszurück gegebene* Parameter verweist, kann NULL sein, da die Größe der gespeicherten Daten erst bestimmt werden kann, wenn der überlappende Vorgang abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="51ae7-130">The **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned may be zero since the size of the data stored can't be determined until the overlapped operation has completed.</span></span>
<span data-ttu-id="51ae7-131">Der endgültige Abschluss Status kann abgerufen werden, wenn die geeignete Vervollständigungs Methode signalisiert wird, wenn der Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="51ae7-131">The final completion status can be retrieved when the appropriate completion method is signaled when the operation has completed.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="51ae7-132">lpvoverlgetauscht</span><span class="sxs-lookup"><span data-stu-id="51ae7-132">lpvOverlapped</span></span>

<span data-ttu-id="51ae7-133">Ein Zeiger auf eine [**wsaoverllapp**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="51ae7-133">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="51ae7-134">Wenn Socket *s* ohne das überlappende Attribut erstellt wurde, wird der *lpoverllapp* -Parameter ignoriert.</span><span class="sxs-lookup"><span data-stu-id="51ae7-134">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="51ae7-135">Wenn *s* mit dem überlappenden Attribut geöffnet wurde und der *lpoverlgetauscht* -Parameter nicht **null** ist, wird der Vorgang als überlappende (asynchrone) Operation ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="51ae7-135">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="51ae7-136">In diesem Fall muss der *lpoverllapp* -Parameter auf eine gültige [**wsaoverllapp**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) -Struktur zeigen.</span><span class="sxs-lookup"><span data-stu-id="51ae7-136">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="51ae7-137">Bei überlappenden Vorgängen gibt die Funktion [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) oder **wspioctl** sofort zurück, und die entsprechende Vervollständigungs Methode wird signalisiert, wenn der Vorgang abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="51ae7-137">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="51ae7-138">Andernfalls gibt die Funktion nicht zurück, bis der Vorgang abgeschlossen ist oder ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="51ae7-138">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="51ae7-139">lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="51ae7-139">lpCompletionRoutine</span></span>

<span data-ttu-id="51ae7-140">Typ: \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="51ae7-140">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="51ae7-141">Ein Zeiger auf die Vervollständigungs Routine, die aufgerufen wird, wenn der Vorgang abgeschlossen wurde (bei nicht überlappenden Sockets ignoriert).</span><span class="sxs-lookup"><span data-stu-id="51ae7-141">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="51ae7-142">lpthreadid</span><span class="sxs-lookup"><span data-stu-id="51ae7-142">lpThreadId</span></span>

<span data-ttu-id="51ae7-143">Ein Zeiger auf eine [**wsathreadid**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) -Struktur, die vom Anbieter in einem nachfolgenden [**wpuqueueapc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc)-Rückruf verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="51ae7-143">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="51ae7-144">Der Anbieter sollte die referenzierte [**wsathreadid**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) -Struktur (nicht den Zeiger auf dieselbe) speichern, bis die [**wpuqueueapc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc) -Funktion zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="51ae7-144">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="51ae7-145">**Hinweis**  Dieser Parameter gilt nur für die **wspioctl** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="51ae7-145">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="51ae7-146">lperrno</span><span class="sxs-lookup"><span data-stu-id="51ae7-146">lpErrno</span></span>

<span data-ttu-id="51ae7-147">Ein Zeiger auf den Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="51ae7-147">A pointer to the error code.</span></span>

<span data-ttu-id="51ae7-148">**Hinweis**  Dieser Parameter gilt nur für die **wspioctl** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="51ae7-148">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="51ae7-149">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="51ae7-149">Return value</span></span>

<span data-ttu-id="51ae7-150">Wenn der Vorgang erfolgreich abgeschlossen wird, gibt die [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) -oder **wspioctl** -Funktion NULL zurück.</span><span class="sxs-lookup"><span data-stu-id="51ae7-150">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="51ae7-151">Wenn der Vorgang fehlschlägt oder aussteht, gibt die Funktion [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) oder **wspioctl** einen **\_ Socketfehler** zurück.</span><span class="sxs-lookup"><span data-stu-id="51ae7-151">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="51ae7-152">Um erweiterte Fehlerinformationen abzurufen, nennen Sie [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="51ae7-152">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="51ae7-153">Fehlercode</span><span class="sxs-lookup"><span data-stu-id="51ae7-153">Error code</span></span> | <span data-ttu-id="51ae7-154">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="51ae7-154">Meaning</span></span> |
|------------|---------|
| <span data-ttu-id="51ae7-155">**ausstehende WSA-e/a \_ \_**</span><span class="sxs-lookup"><span data-stu-id="51ae7-155">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="51ae7-156">Ein übergebener Vorgang wurde erfolgreich initiiert, und der Abschluss wird zu einem späteren Zeitpunkt angegeben.</span><span class="sxs-lookup"><span data-stu-id="51ae7-156">An overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="51ae7-157">**WSA- \_ Vorgang \_ abgebrochen**</span><span class="sxs-lookup"><span data-stu-id="51ae7-157">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="51ae7-158">Ein über Lapp ender Vorgang wurde aufgrund der Schließung des Sockets oder der Ausführung des Befehls " **SIO \_ Flush** ioctl" abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="51ae7-158">An overlapped operation was canceled due to the closure of the socket or the execution of the **SIO\_FLUSH** IOCTL command.</span></span> |
| <span data-ttu-id="51ae7-159">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="51ae7-159">**WSAEFAULT**</span></span> | <span data-ttu-id="51ae7-160">Der Parameter " *lpvinbuffer*", " *lpvoutbuffer*", " *lpcbbytesgab*", " *lpoverlgetauscht* " oder " *lpCompletionRoutine* " ist nicht vollständig in einem gültigen Teil des Benutzer Adressraums enthalten.</span><span class="sxs-lookup"><span data-stu-id="51ae7-160">The *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="51ae7-161">**Wsaeingabe Progress**</span><span class="sxs-lookup"><span data-stu-id="51ae7-161">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="51ae7-162">Die-Funktion wird aufgerufen, wenn ein Rückruf ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="51ae7-162">The function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="51ae7-163">**Wsaeingabe**</span><span class="sxs-lookup"><span data-stu-id="51ae7-163">**WSAEINTR**</span></span> | <span data-ttu-id="51ae7-164">Ein Blockierungs Vorgang wurde unterbrochen.</span><span class="sxs-lookup"><span data-stu-id="51ae7-164">A blocking operation was interrupted.</span></span> |
| <span data-ttu-id="51ae7-165">**Wsaabval**</span><span class="sxs-lookup"><span data-stu-id="51ae7-165">**WSAEINVAL**</span></span> | <span data-ttu-id="51ae7-166">Der *dwIoControlCode* -Parameter ist kein gültiger Befehl, oder ein angegebener Eingabeparameter ist nicht zulässig, oder der Befehl ist nicht auf den angegebenen Sockettyp anwendbar.</span><span class="sxs-lookup"><span data-stu-id="51ae7-166">The *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> <span data-ttu-id="51ae7-167">Dieser Fehler wird zurückgegeben, wenn der *cboutbuffer* -Parameter kleiner als die Größe eines **ulong** -Datentyps ist.</span><span class="sxs-lookup"><span data-stu-id="51ae7-167">This error is returned if the *cbOutBuffer* parameter is less than the size of a **ULONG** data type.</span></span>
| <span data-ttu-id="51ae7-168">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="51ae7-168">**WSAENETDOWN**</span></span> | <span data-ttu-id="51ae7-169">Das Netzwerk Subsystem ist fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="51ae7-169">The network subsystem has failed.</span></span> |
| <span data-ttu-id="51ae7-170">**Wsaumoproumopt**</span><span class="sxs-lookup"><span data-stu-id="51ae7-170">**WSAENOPROTOOPT**</span></span> | <span data-ttu-id="51ae7-171">Die Socketoption wird für das angegebene Protokoll nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="51ae7-171">The socket option is not supported on the specified protocol.</span></span> |
| <span data-ttu-id="51ae7-172">**WSAENOTCONN**</span><span class="sxs-lookup"><span data-stu-id="51ae7-172">**WSAENOTCONN**</span></span> | <span data-ttu-id="51ae7-173">Die Socket s ist nicht verbunden.</span><span class="sxs-lookup"><span data-stu-id="51ae7-173">The socket s is not connected.</span></span> |
| <span data-ttu-id="51ae7-174">**Wsaumotsock**</span><span class="sxs-lookup"><span data-stu-id="51ae7-174">**WSAENOTSOCK**</span></span> | <span data-ttu-id="51ae7-175">Der Deskriptor *s* ist kein Socket.</span><span class="sxs-lookup"><span data-stu-id="51ae7-175">The descriptor *s* is not a socket.</span></span> |
| <span data-ttu-id="51ae7-176">**WSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="51ae7-176">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="51ae7-177">Der angegebene ioctl-Befehl wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="51ae7-177">The specified IOCTL command is not supported.</span></span> <span data-ttu-id="51ae7-178">Dieser Fehler wird zurückgegeben, wenn die IOCTL- **\_ \_ \_ \_ Abfrage des optimalen** sendebacklogs nicht vom Transportanbieter unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="51ae7-178">This error is returned if the **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** IOCTL is not supported by the transport provider.</span></span> <span data-ttu-id="51ae7-179">Dieser Fehler wird auch zurückgegeben, wenn ein Versuch der Verwendung der " **SIO \_ ideal \_ Send \_ \_ backbackquery** ioctl" für einen Datagramm-Socket erfolgt.</span><span class="sxs-lookup"><span data-stu-id="51ae7-179">This error is also returned when an attempt to use the **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** IOCTL is made on a datagram socket.</span></span> |

## <a name="remarks"></a><span data-ttu-id="51ae7-180">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="51ae7-180">Remarks</span></span>

<span data-ttu-id="51ae7-181">Die IOCTL- **\_ \_ \_ \_ Abfrage des optimalen** sendebacklogs wird unter Windows Server 2008, Windows Vista mit Service Pack 1 (SP1) und höheren Versionen des Betriebssystems unterstützt.</span><span class="sxs-lookup"><span data-stu-id="51ae7-181">The **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** IOCTL is supported on Windows Server 2008, Windows Vista with Service Pack 1 (SP1), and later versions of the operating system.</span></span>

<span data-ttu-id="51ae7-182">Beim Senden von Daten über eine TCP-Verbindung mithilfe von Windows Sockets ist es wichtig, dass Sie eine ausreichende Menge an ausstehenden Daten (gesendet, aber noch nicht bestätigt) in TCP aufbewahren, um den höchsten Durchsatz zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="51ae7-182">When sending data over a TCP connection using Windows sockets, it is important to keep a sufficient amount of data outstanding (sent but not acknowledged yet) in TCP in order to achieve the highest throughput.</span></span>
<span data-ttu-id="51ae7-183">Der ideale Wert für die Datenmenge, die für den optimalen Durchsatz für die TCP-Verbindung aussteht, wird als ideale Größe des sendebacklogs (ISB) bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="51ae7-183">The ideal value for the amount of data outstanding to achieve the best throughput for the TCP connection is called the ideal send backlog (ISB) size.</span></span>
<span data-ttu-id="51ae7-184">Der ISB-Wert ist eine Funktion des Produkts zur Bandbreiten Verzögerung der TCP-Verbindung und des angekündigten Empfangs Fensters des Empfängers (und zum Teil der Überlastung im Netzwerk).</span><span class="sxs-lookup"><span data-stu-id="51ae7-184">The ISB value is a function of the bandwidth-delay product of the TCP connection and the receiver's advertised receive window (and partly the amount of congestion in the network).</span></span>

<span data-ttu-id="51ae7-185">Der ISB-Wert pro Verbindung ist über die TCP-Protokoll Implementierung in Windows Server 2008, Windows Vista mit SP1 und höheren Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="51ae7-185">The ISB value per connection is available from the TCP protocol implementation in Windows Server 2008, Windows Vista with SP1, and later versions of the operating system.</span></span>
<span data-ttu-id="51ae7-186">Der **\_ optimale \_ Abfrage \_ \_** -ioctl-Abfragedienst kann von einer Anwendung verwendet werden, um eine Benachrichtigung zu erhalten, wenn der ISB-Wert für eine Verbindung dynamisch geändert wird.</span><span class="sxs-lookup"><span data-stu-id="51ae7-186">The **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** IOCTL can be used by an application to get a notification when the ISB value changes dynamically for a connection.</span></span>

<span data-ttu-id="51ae7-187">Unter Windows Server 2008, Windows Vista mit SP1 und höheren Versionen des Betriebssystems werden die Daten von [**der \_ optimalen \_ Sende \_ Rückstands \_ Änderung**](sio-ideal-send-backlog-change.md) und der **\_ optimalen \_ Sende \_ Rückstand \_ Abfrage** IOCTLs von der optimalen Sende Rückstands Abfrage für Stream-orientierte Sockets unterstützt, die verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="51ae7-187">On Windows Server 2008, Windows Vista with SP1, and later versions of the operating system, the [**SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE**](sio-ideal-send-backlog-change.md) and **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** IOCTLs are supported on stream-oriented sockets that are in a connected state.</span></span>

<span data-ttu-id="51ae7-188">Der Bereich für den ISB-Wert einer TCP-Verbindung kann theoretisch von 0 bis maximal 16 Megabyte abweichen.</span><span class="sxs-lookup"><span data-stu-id="51ae7-188">The range for the ISB value for a TCP connection can theoretically vary from 0 to a maximum of 16 megabytes.</span></span>

<span data-ttu-id="51ae7-189">Die typische Verwendung der " [**SIO \_ ideal \_ Send \_ \_**](sio-ideal-send-backlog-change.md) Backlogs Change" und der " **SIO \_ ideal \_ Send \_ \_ backbackquery** IOCTLs" basiert auf der Send-Methode, die von den Anwendungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="51ae7-189">The typical usage of the [**SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE**](sio-ideal-send-backlog-change.md) and **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** IOCTLs is based on the send method used by the applications.</span></span>
<span data-ttu-id="51ae7-190">Es werden zwei gängige Fälle erläutert.</span><span class="sxs-lookup"><span data-stu-id="51ae7-190">Two common cases are discussed.</span></span>

<span data-ttu-id="51ae7-191">Anwendungen, die eine blockierende oder nicht blockierende Sende Anforderung gleichzeitig ausführen, basieren in der Regel auf der internen Sende Pufferung durch Winsock, um einen angemessenen Durchsatz zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="51ae7-191">Applications that perform one blocking or non-blocking send request at a time typically rely on internal send buffering by Winsock to achieve decent throughput.</span></span>
<span data-ttu-id="51ae7-192">Das Sendepuffer Limit für eine bestimmte Verbindung wird durch die **\_ sndbuf** -Socketoption "so" gesteuert.</span><span class="sxs-lookup"><span data-stu-id="51ae7-192">The send buffer limit for a given connection is controlled by the **SO\_SNDBUF** socket option.</span></span>
<span data-ttu-id="51ae7-193">Bei der blockierenden und nicht blockierenden Sende Methode bestimmt der Grenzwert für den Sendepuffer, wie viele Daten in TCP verbleiben.</span><span class="sxs-lookup"><span data-stu-id="51ae7-193">For the blocking and non-blocking send method, the send buffer limit determines how much data is kept outstanding in TCP.</span></span>
<span data-ttu-id="51ae7-194">Wenn der ISB-Wert für die Verbindung größer als das Sendepuffer Limit ist, ist der Durchsatz, der für die Verbindung erreicht wird, nicht optimal.</span><span class="sxs-lookup"><span data-stu-id="51ae7-194">If the ISB value for the connection is larger than the send buffer limit, then the throughput achieved on the connection will not be optimal.</span></span>
<span data-ttu-id="51ae7-195">Um einen besseren Durchsatz zu erzielen, können die Anwendungen den Grenzwert für den Sendepuffer basierend auf dem Ergebnis der ISB-Abfrage festlegen, da ISB-Änderungs Benachrichtigungen für die Verbindung auftreten.</span><span class="sxs-lookup"><span data-stu-id="51ae7-195">In order to achieve better throughput, the applications can set the send buffer limit based on the result of the ISB query as ISB change notifications occur on the connection.</span></span>

<span data-ttu-id="51ae7-196">Bei Anwendungen, die die überlappende Send-Methode mit ausstehenden ausstehenden Sende Anforderungen verwenden, wird die Menge der in TCP ausstehenden Daten durch das Sendepuffer Limit in Winsock und die Gesamtmenge der Daten, die in den ausstehenden überlappenden Sende Anforderungen enthalten sind, bestimmt.</span><span class="sxs-lookup"><span data-stu-id="51ae7-196">For applications that use the overlapped send method with multiple send requests outstanding, the amount of data kept outstanding in TCP is determined by the send buffer limit in Winsock and the total amount of data contained in the outstanding overlapped send requests.</span></span>
<span data-ttu-id="51ae7-197">In diesem Fall sollten Anwendungen den ISB-Wert verwenden, um zu bestimmen, wie viele ausstehende Sende Anforderungen aufbewahrt werden sollen und welche Daten für die einzelnen Sende Anforderungen verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="51ae7-197">In this case, applications should use the ISB value to determine how many outstanding send requests they should keep and what the data size for each send request should be.</span></span>
<span data-ttu-id="51ae7-198">Im Idealfall sollte die Anwendung versuchen, die folgende Gleichung zufrieden zu halten:</span><span class="sxs-lookup"><span data-stu-id="51ae7-198">Ideally, the application should try to keep the following equation satisfied:</span></span>

`ISB value == send buffer limit + (number of simultaneous overlapped send requests * data length per send request)`

<span data-ttu-id="51ae7-199">Beachten Sie, dass die Verwendung der ISB IOCTLs über TCP-Sockets in der obigen Weise zu einer erhöhten Speicherauslastung in Exchange führen kann, um den Durchsatz bei Verbindungen mit einem Produkt mit hoher Bandbreite zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="51ae7-199">Note that using the ISB IOCTLs over TCP sockets in the above fashion can lead to increased memory usage in exchange for increased throughput on connections with a high bandwidth-delay product.</span></span>
<span data-ttu-id="51ae7-200">Die TCP-Implementierung in Windows drosselt ISB-Werte nach Bedarf basierend auf der Gesamtauslastung des System Arbeitsspeichers.</span><span class="sxs-lookup"><span data-stu-id="51ae7-200">The TCP implementation in Windows will throttle ISB values as necessary based on overall system memory usage.</span></span>

<span data-ttu-id="51ae7-201">Die IOCTL- **\_ \_ \_ \_ Abfrage des optimalen Sende** Backlogs ist nur auf einem Stream-Socket zulässig, der sich im verbundenen Zustand befindet.</span><span class="sxs-lookup"><span data-stu-id="51ae7-201">The **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** IOCTL is allowed only on a stream socket that is in the connected state.</span></span>
<span data-ttu-id="51ae7-202">Andernfalls schlägt die Funktion [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) oder **wspioctl** mit **wsaenotconn** fehl.</span><span class="sxs-lookup"><span data-stu-id="51ae7-202">Otherwise the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function will fail with **WSAENOTCONN**.</span></span>

<span data-ttu-id="51ae7-203">Alle ioctl können unbegrenzt blockieren, abhängig von der Implementierung des Dienstanbieters.</span><span class="sxs-lookup"><span data-stu-id="51ae7-203">Any IOCTL may block indefinitely, depending on the service provider's implementation.</span></span>
<span data-ttu-id="51ae7-204">Wenn die Anwendung die Blockierung in einem [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) -oder **wspioctl** -Funktions aufrufnis nicht tolerieren kann, werden überlappende e/a-Vorgänge für IOCTLs empfohlen, die besonders wahrscheinlich blockiert werden.</span><span class="sxs-lookup"><span data-stu-id="51ae7-204">If the application cannot tolerate blocking in a [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function call, overlapped I/O would be advised for IOCTLs that are especially likely to block.</span></span>

<span data-ttu-id="51ae7-205">Die " **SIO \_ ideal Send \_ backbackquery \_ \_** ioctl" wird wahrscheinlich nicht blockiert, sodass Sie normalerweise synchron aufgerufen wird, wenn die Parameter " *lpoverlgetauscht* " und " *lpCompletionRoutine* " auf **null** festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="51ae7-205">The **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** IOCTL is not likely to block so it is normally called synchronously with the *lpOverlapped* and *lpCompletionRoutine* parameters set to **NULL**.</span></span>

<span data-ttu-id="51ae7-206">Bei der Verwendung der IOCTL- **\_ \_ \_ \_ Abfrage** für den optimalen sendebackbackioctl- **\_ Vorgang \_** **kann in den** folgenden Fällen ein Fehler auftreten.</span><span class="sxs-lookup"><span data-stu-id="51ae7-206">The **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** IOCTL can fail with **WSAEINTR** or **WSA\_OPERATION\_ABORTED** under the following cases:</span></span>

<span data-ttu-id="51ae7-207">Die TCP-Verbindung ist in der Senderichtung ordnungsgemäß getrennt.</span><span class="sxs-lookup"><span data-stu-id="51ae7-207">The TCP connection is gracefully disconnected in the send direction.</span></span>
<span data-ttu-id="51ae7-208">Dies kann ein Ergebnis eines Aufrufs der Funktion zum Herunterfahren mit dem auf **SD \_ Send** festgelegten Parameter, einem Aufrufen der **disconnectex** -Funktion oder eines Aufrufs der Funktion **TransmitFile** oder **transmitpaketen** mit dem Parameter *dwFlags* , der auf **tf \_ Disconnect** oder TF- **\_ Wiederverwendung** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="51ae7-208">This can occur as a result of a call to shutdown function with the how parameter set to **SD\_SEND**, a call to the **DisconnectEx** function, or a call to the **TransmitFile** or **TransmitPackets** function with *dwFlags* parameter set to **TF\_DISCONNECT** or **TF\_REUSE**.</span></span>
<span data-ttu-id="51ae7-209">Die TCP-Verbindung wurde zurückgesetzt oder abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="51ae7-209">The TCP connection has been reset or aborted.</span></span>
<span data-ttu-id="51ae7-210">Die Anforderung wird vom e/a-Manager abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="51ae7-210">The request is canceled by the I/O Manager.</span></span>

<span data-ttu-id="51ae7-211">In der Header Datei " *Ws2tcpip. h* " sind zwei Inline-Wrapper Funktionen für diese IOCTLs definiert.</span><span class="sxs-lookup"><span data-stu-id="51ae7-211">Two inline wrapper functions for these IOCTLs are defined in the *Ws2tcpip.h* header file.</span></span>
<span data-ttu-id="51ae7-212">Es wird empfohlen, dass diese Inline Funktionen anstelle der [**\_ optimalen optimalen \_ Sende \_ Rückstands \_ Änderung**](sio-ideal-send-backlog-change.md) und der **\_ optimalen \_ Sende Rückstands Abfrage von der optimalen Sende \_ Rückstands \_ Abfrage** IOCTLs verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="51ae7-212">It is recommended that these inline functions be used instead of using the [**SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE**](sio-ideal-send-backlog-change.md) and **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** IOCTLs directly.</span></span>

<span data-ttu-id="51ae7-213">Die Funktion "Inline Wrapper" für die IOCTL-Änderung von " [**SIO \_ ideal \_ Send \_ \_**](sio-ideal-send-backlog-change.md) Backlogs" ist die Funktion " **idesendbacklognotify** ".</span><span class="sxs-lookup"><span data-stu-id="51ae7-213">The inline wrapper function for the [**SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE**](sio-ideal-send-backlog-change.md) IOCTL is the **idealsendbacklognotify** function.</span></span>

<span data-ttu-id="51ae7-214">Die Funktion "Inline Wrapper" für die IOCTL- **\_ \_ \_ \_ Abfrage des optimalen** sendebacklogs ist die Funktion " **ideal Send backlogquery** ".</span><span class="sxs-lookup"><span data-stu-id="51ae7-214">The inline wrapper function for the **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** IOCTL is the **idealsendbacklogquery** function.</span></span>

<span data-ttu-id="51ae7-215">Die dynamische Sende Pufferung für TCP wurde unter Windows 7 und Windows Server 2008 R2 hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="51ae7-215">Dynamic send buffering for TCP was added on Windows 7 and Windows Server 2008 R2.</span></span>
<span data-ttu-id="51ae7-216">Standardmäßig ist die dynamische Sende Pufferung für TCP aktiviert, es sei denn, eine Anwendung legt die **\_ sndbuf** -Socketoption für den Datenstrom Socket fest.</span><span class="sxs-lookup"><span data-stu-id="51ae7-216">By default, dynamic send buffering for TCP is enabled unless an application sets the **SO\_SNDBUF** socket option on the stream socket.</span></span>

<span data-ttu-id="51ae7-217">Die Verwendung von Netsh ist die empfohlene Methode, um die dynamische Sende Pufferung für TCP abzufragen oder festzulegen.</span><span class="sxs-lookup"><span data-stu-id="51ae7-217">Using netsh is the recommended method to query or set dynamic send buffering for TCP.</span></span>

<span data-ttu-id="51ae7-218">Der aktuelle Wert für die dynamische Sende Pufferung für TCP kann mit dem folgenden Befehl abgerufen werden:</span><span class="sxs-lookup"><span data-stu-id="51ae7-218">The current value for dynamic send buffering for TCP can be retrieved using the following command:</span></span>

`netsh winsock show autotuning`

<span data-ttu-id="51ae7-219">Die dynamische Sende Pufferung für TCP kann mit dem folgenden Befehl deaktiviert werden:</span><span class="sxs-lookup"><span data-stu-id="51ae7-219">Dynamic send buffering for TCP can be disabled using the following command:</span></span>

`netsh winsock set autotuning off`

<span data-ttu-id="51ae7-220">Die dynamische Sende Pufferung für TCP kann mithilfe des folgenden Befehls aktiviert werden:</span><span class="sxs-lookup"><span data-stu-id="51ae7-220">Dynamic send buffering for TCP can be enabled using the following command:</span></span>

`netsh winsock set autotuning on`

<span data-ttu-id="51ae7-221">Obwohl es nicht empfohlen wird, kann die dynamische Sende Pufferung aus einer Anwendung deaktiviert werden, indem der folgende Registrierungs Wert auf 0 (null) festgelegt wird:</span><span class="sxs-lookup"><span data-stu-id="51ae7-221">While it is discouraged, dynamic send buffering can be disabled from an application by setting the following registry value to zero:</span></span>

`HKEY_LOCAL_MACHINE\SYSTEM\Current Control Set\Services\AFD\Parameters\DynamicSendBufferDisable`

<span data-ttu-id="51ae7-222">Wenn Sie den Wert für die dynamische Sende Pufferung mithilfe von NetSh.exe ändern oder den Registrierungs Wert ändern, muss der Computer neu gestartet werden, damit die Änderung wirksam wird.</span><span class="sxs-lookup"><span data-stu-id="51ae7-222">When changing the value for dynamic send buffering using NetSh.exe or changing the registry value, the computer must be restarted for the change to take effect.</span></span>

<span data-ttu-id="51ae7-223">Bei der dynamischen Sende Pufferung unter Windows 7 und Windows Server 2008 R2 werden die Anforderungen der [**\_ optimalen Sende \_ \_ Rückstands \_ Änderung**](sio-ideal-send-backlog-change.md) und **der \_ optimalen \_ Sende \_ Rückstand \_ Abfrage** IOCTLs der optimalen Sende Rückstand nur in besonderen Fällen benötigt.</span><span class="sxs-lookup"><span data-stu-id="51ae7-223">With dynamic send buffering on Windows 7 and Windows Server 2008 R2, the use of the [**SIO\_IDEAL\_SEND\_BACKLOG\_CHANGE**](sio-ideal-send-backlog-change.md) and **SIO\_IDEAL\_SEND\_BACKLOG\_QUERY** IOCTLs are needed only in special circumstances.</span></span>

## <a name="see-also"></a><span data-ttu-id="51ae7-224">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="51ae7-224">See also</span></span>

[<span data-ttu-id="51ae7-225">**SIO_IDEAL_SEND_BACKLOG_CHANGE**</span><span class="sxs-lookup"><span data-stu-id="51ae7-225">**SIO_IDEAL_SEND_BACKLOG_CHANGE**</span></span>](sio-ideal-send-backlog-change.md)

[<span data-ttu-id="51ae7-226">**Glühbirne**</span><span class="sxs-lookup"><span data-stu-id="51ae7-226">**socket**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="51ae7-227">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="51ae7-227">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)

[<span data-ttu-id="51ae7-228">**Wsagein verlappedresult**</span><span class="sxs-lookup"><span data-stu-id="51ae7-228">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="51ae7-229">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="51ae7-229">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="51ae7-230">**Wsaoverlgetauscht**</span><span class="sxs-lookup"><span data-stu-id="51ae7-230">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="51ae7-231">**Wsasocketa**</span><span class="sxs-lookup"><span data-stu-id="51ae7-231">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="51ae7-232">**Wsasocketw**</span><span class="sxs-lookup"><span data-stu-id="51ae7-232">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
