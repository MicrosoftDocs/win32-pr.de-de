---
description: Der Steuercode fragt die Transport Einstellungen für einen Socket ab.
ms.assetid: 3845BE07-A414-4118-96E8-8BEF1DEDB1D3
title: SIO_QUERY_TRANSPORT_SETTING Steuerungs Codes
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 592301f0fcdbbb0d3d5babba446583d2e48db086
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863804"
---
# <a name="sio_query_transport_setting-control-code"></a><span data-ttu-id="1cc9b-103">SIO_QUERY_TRANSPORT_SETTING Steuerungs Codes</span><span class="sxs-lookup"><span data-stu-id="1cc9b-103">SIO_QUERY_TRANSPORT_SETTING Control Code</span></span>

## <a name="description"></a><span data-ttu-id="1cc9b-104">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1cc9b-104">Description</span></span>

<span data-ttu-id="1cc9b-105">Der Verwaltungs Code für die Übertragung der **\_ Abfrage- \_ Transport \_** Einstellungen fragt die Transport Einstellungen für einen Socket ab.</span><span class="sxs-lookup"><span data-stu-id="1cc9b-105">The **SIO\_QUERY\_TRANSPORT\_SETTING** control code queries the transport settings on a socket.</span></span>

<span data-ttu-id="1cc9b-106">Um diesen Vorgang auszuführen, wenden Sie die [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) -oder **wspioctl** -Funktion mit den folgenden Parametern an.</span><span class="sxs-lookup"><span data-stu-id="1cc9b-106">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_QUERY_TRANSPORT_SETTING, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to the input buffer
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,     // pointer to the output buffer
  (DWORD) cbOutBuffer,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_QUERY_TRANSPORT_SETTING, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to the input buffer
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,     // pointer to the output buffer
  (DWORD) cbOutBuffer,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,   // a WSATHREADID structure
  (LPINT) lpErrno   // a pointer to the error code.
);
```

## <a name="parameters"></a><span data-ttu-id="1cc9b-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="1cc9b-107">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="1cc9b-108">s</span><span class="sxs-lookup"><span data-stu-id="1cc9b-108">s</span></span>

<span data-ttu-id="1cc9b-109">Ein Deskriptor, der einen Socket identifiziert.</span><span class="sxs-lookup"><span data-stu-id="1cc9b-109">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="1cc9b-110">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="1cc9b-110">dwIoControlCode</span></span>

<span data-ttu-id="1cc9b-111">Der Steuerelement Code für den Vorgang.</span><span class="sxs-lookup"><span data-stu-id="1cc9b-111">The control code for the operation.</span></span>
<span data-ttu-id="1cc9b-112">Verwenden Sie für diesen Vorgang die **\_ \_ Transport \_ Einstellung "sio-Abfrage** ".</span><span class="sxs-lookup"><span data-stu-id="1cc9b-112">Use **SIO\_QUERY\_TRANSPORT\_SETTING** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="1cc9b-113">lpvinbuffer</span><span class="sxs-lookup"><span data-stu-id="1cc9b-113">lpvInBuffer</span></span>

<span data-ttu-id="1cc9b-114">Ein Zeiger auf den Eingabepuffer.</span><span class="sxs-lookup"><span data-stu-id="1cc9b-114">A pointer to the input buffer.</span></span>
<span data-ttu-id="1cc9b-115">Dieser Parameter enthält einen Zeiger auf eine-Struktur, in der der erste Member der-Struktur eine [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) Struktur ist, die bestimmt, welche Transport Einstellung abgefragt wird.</span><span class="sxs-lookup"><span data-stu-id="1cc9b-115">This parameter contains a pointer to a structure where the first member of the structure is a [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) structure that determines what transport setting is being queried.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="1cc9b-116">cbinbuffer</span><span class="sxs-lookup"><span data-stu-id="1cc9b-116">cbInBuffer</span></span>

<span data-ttu-id="1cc9b-117">Die Größe des Eingabe Puffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="1cc9b-117">The size, in bytes, of the input buffer.</span></span>
<span data-ttu-id="1cc9b-118">Dieser Parameter hängt von der abgefragten Transport Einstellung ab.</span><span class="sxs-lookup"><span data-stu-id="1cc9b-118">This parameter depends on the transport setting being queried.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="1cc9b-119">lpvoutbuffer</span><span class="sxs-lookup"><span data-stu-id="1cc9b-119">lpvOutBuffer</span></span>

<span data-ttu-id="1cc9b-120">Ein Zeiger auf den Ausgabepuffer.</span><span class="sxs-lookup"><span data-stu-id="1cc9b-120">A pointer to the output buffer.</span></span>
<span data-ttu-id="1cc9b-121">Dieser Parameter hängt von der Transport Einstellung ab, die abgefragt wird, wenn die Parameter *lpoverlgetauscht* und *lpCompletionRoutine* **null** sind.</span><span class="sxs-lookup"><span data-stu-id="1cc9b-121">This parameter depends on the transport setting being queried if the *lpOverlapped* and *lpCompletionRoutine* parameters are **NULL**.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="1cc9b-122">cboutbuffer</span><span class="sxs-lookup"><span data-stu-id="1cc9b-122">cbOutBuffer</span></span>

<span data-ttu-id="1cc9b-123">Die Größe des Ausgabepuffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="1cc9b-123">The size, in bytes, of the output buffer.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="1cc9b-124">lpcbbyteszurück gegeben</span><span class="sxs-lookup"><span data-stu-id="1cc9b-124">lpcbBytesReturned</span></span>

<span data-ttu-id="1cc9b-125">Ein Zeiger auf eine Variable, die die Größe der im Ausgabepuffer gespeicherten Daten (in Bytes) empfängt.</span><span class="sxs-lookup"><span data-stu-id="1cc9b-125">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>

<span data-ttu-id="1cc9b-126">Wenn der Ausgabepuffer zu klein ist, schlägt der-Befehl fehl, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) gibt [**WSAEINVAL**](windows-sockets-error-codes-2.md)zurück, und der *lpcbbytesreturns* -Parameter verweist auf den **DWORD** -Wert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="1cc9b-126">If the output buffer is too small, the call fails, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns [**WSAEINVAL**](windows-sockets-error-codes-2.md), and the *lpcbBytesReturned* parameter points to a **DWORD** value of zero.</span></span>

<span data-ttu-id="1cc9b-127">Wenn *lpoverlgetauscht* gleich **null** ist, kann der **DWORD** -Wert, auf den der *lpcbbytesall* -Parameter verweist, der bei einem erfolgreichen-Vorgang zurückgegeben wird, nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="1cc9b-127">If *lpOverlapped* is **NULL**, the **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned on a successful call cannot be zero.</span></span>

<span data-ttu-id="1cc9b-128">Wenn der *lpoverllapp* -Parameter für überlappende Sockets nicht **null** ist, werden Vorgänge, die nicht sofort abgeschlossen werden können, initiiert, und der Abschluss wird zu einem späteren Zeitpunkt angegeben.</span><span class="sxs-lookup"><span data-stu-id="1cc9b-128">If the *lpOverlapped* parameter is not **NULL** for overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>
<span data-ttu-id="1cc9b-129">Der **DWORD** -Wert, auf den der zurückgegebene *lpcbbyteszurück gegebene* Parameter verweist, kann NULL sein, da die Größe der gespeicherten Daten erst bestimmt werden kann, wenn der überlappende Vorgang abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="1cc9b-129">The **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned may be zero since the size of the data stored can't be determined until the overlapped operation has completed.</span></span>
<span data-ttu-id="1cc9b-130">Der endgültige Abschluss Status kann abgerufen werden, wenn die geeignete Vervollständigungs Methode signalisiert wird, wenn der Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="1cc9b-130">The final completion status can be retrieved when the appropriate completion method is signaled when the operation has completed.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="1cc9b-131">lpvoverlgetauscht</span><span class="sxs-lookup"><span data-stu-id="1cc9b-131">lpvOverlapped</span></span>

<span data-ttu-id="1cc9b-132">Ein Zeiger auf eine [**wsaoverllapp**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="1cc9b-132">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="1cc9b-133">Wenn Socket *s* ohne das überlappende Attribut erstellt wurde, wird der *lpoverllapp* -Parameter ignoriert.</span><span class="sxs-lookup"><span data-stu-id="1cc9b-133">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="1cc9b-134">Wenn *s* mit dem überlappenden Attribut geöffnet wurde und der *lpoverlgetauscht* -Parameter nicht **null** ist, wird der Vorgang als überlappende (asynchrone) Operation ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1cc9b-134">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="1cc9b-135">In diesem Fall muss der *lpoverllapp* -Parameter auf eine gültige [**wsaoverllapp**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) -Struktur zeigen.</span><span class="sxs-lookup"><span data-stu-id="1cc9b-135">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="1cc9b-136">Bei überlappenden Vorgängen gibt die Funktion [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) oder **wspioctl** sofort zurück, und die entsprechende Vervollständigungs Methode wird signalisiert, wenn der Vorgang abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="1cc9b-136">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="1cc9b-137">Andernfalls gibt die Funktion nicht zurück, bis der Vorgang abgeschlossen ist oder ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="1cc9b-137">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="1cc9b-138">lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="1cc9b-138">lpCompletionRoutine</span></span>

<span data-ttu-id="1cc9b-139">Typ: \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="1cc9b-139">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="1cc9b-140">Ein Zeiger auf die Vervollständigungs Routine, die aufgerufen wird, wenn der Vorgang abgeschlossen wurde (bei nicht überlappenden Sockets ignoriert).</span><span class="sxs-lookup"><span data-stu-id="1cc9b-140">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="1cc9b-141">lpthreadid</span><span class="sxs-lookup"><span data-stu-id="1cc9b-141">lpThreadId</span></span>

<span data-ttu-id="1cc9b-142">Ein Zeiger auf eine [**wsathreadid**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) -Struktur, die vom Anbieter in einem nachfolgenden [**wpuqueueapc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc)-Rückruf verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1cc9b-142">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="1cc9b-143">Der Anbieter sollte die referenzierte [**wsathreadid**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) -Struktur (nicht den Zeiger auf dieselbe) speichern, bis die [**wpuqueueapc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) -Funktion zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="1cc9b-143">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="1cc9b-144">**Hinweis**  Dieser Parameter gilt nur für die **wspioctl** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="1cc9b-144">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="1cc9b-145">lperrno</span><span class="sxs-lookup"><span data-stu-id="1cc9b-145">lpErrno</span></span>

<span data-ttu-id="1cc9b-146">Ein Zeiger auf den Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="1cc9b-146">A pointer to the error code.</span></span>

<span data-ttu-id="1cc9b-147">**Hinweis**  Dieser Parameter gilt nur für die **wspioctl** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="1cc9b-147">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="1cc9b-148">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1cc9b-148">Return value</span></span>

<span data-ttu-id="1cc9b-149">Wenn der Vorgang erfolgreich abgeschlossen wird, gibt die [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) -oder **wspioctl** -Funktion NULL zurück.</span><span class="sxs-lookup"><span data-stu-id="1cc9b-149">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="1cc9b-150">Wenn der Vorgang fehlschlägt oder aussteht, gibt die Funktion [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) oder **wspioctl** einen **\_ Socketfehler** zurück.</span><span class="sxs-lookup"><span data-stu-id="1cc9b-150">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="1cc9b-151">Um erweiterte Fehlerinformationen abzurufen, nennen Sie [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="1cc9b-151">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="1cc9b-152">Fehlercode</span><span class="sxs-lookup"><span data-stu-id="1cc9b-152">Error code</span></span> | <span data-ttu-id="1cc9b-153">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="1cc9b-153">Meaning</span></span> |
|------------|---------|
| <span data-ttu-id="1cc9b-154">**Fehler \_ beim \_ Puffer.**</span><span class="sxs-lookup"><span data-stu-id="1cc9b-154">**ERROR\_INSUFFICIENT\_BUFFER**</span></span> | <span data-ttu-id="1cc9b-155">Der an einen System Rückruf über gegebene Datenbereich ist zu klein.</span><span class="sxs-lookup"><span data-stu-id="1cc9b-155">The data area passed to a system call is too small.</span></span> <span data-ttu-id="1cc9b-156">Dieser Fehler wird zurückgegeben, wenn der Puffer, auf den der *lpvoutbuffer* -Parameter verweist, eine Puffergröße hat, die im *cboutbuffer* -Parameter übergeben wurde, zu klein ist.</span><span class="sxs-lookup"><span data-stu-id="1cc9b-156">This error is returned if the buffer pointed to by the *lpvOutBuffer* parameter with a buffer size passed in the *cbOutBuffer* parameter is too small.</span></span> <span data-ttu-id="1cc9b-157">Die erforderliche Puffergröße wird im Parameter " *lpcbbytes}* " zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1cc9b-157">The buffer size required will be returned in the *lpcbBytesReturned* parameter.</span></span> |
| <span data-ttu-id="1cc9b-158">**ausstehende WSA-e/a \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1cc9b-158">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="1cc9b-159">Ein übergebener Vorgang wurde erfolgreich initiiert, und der Abschluss wird zu einem späteren Zeitpunkt angegeben.</span><span class="sxs-lookup"><span data-stu-id="1cc9b-159">An overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="1cc9b-160">**WSA- \_ Vorgang \_ abgebrochen**</span><span class="sxs-lookup"><span data-stu-id="1cc9b-160">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="1cc9b-161">Ein über Lapp ender Vorgang wurde aufgrund der Schließung des Sockets oder der Ausführung des Befehls " **SIO \_ Flush** ioctl" abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="1cc9b-161">An overlapped operation was canceled due to the closure of the socket or the execution of the **SIO\_FLUSH** IOCTL command.</span></span> |
| <span data-ttu-id="1cc9b-162">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="1cc9b-162">**WSAEFAULT**</span></span> | <span data-ttu-id="1cc9b-163">Der Parameter " *lpvoutbuffer*", " *lpcbbytesis*", " *lpoverlgetauscht*" oder " *lpCompletionRoutine* " ist nicht vollständig in einem gültigen Teil des Benutzer Adressraums enthalten.</span><span class="sxs-lookup"><span data-stu-id="1cc9b-163">The *lpvOutBuffer*, *lpcbBytesReturned*, *lpOverlapped*, or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="1cc9b-164">**Wsaeingabe Progress**</span><span class="sxs-lookup"><span data-stu-id="1cc9b-164">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="1cc9b-165">Die-Funktion wird aufgerufen, wenn ein Rückruf ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1cc9b-165">The function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="1cc9b-166">**Wsaeingabe**</span><span class="sxs-lookup"><span data-stu-id="1cc9b-166">**WSAEINTR**</span></span> | <span data-ttu-id="1cc9b-167">Ein Blockierungs Vorgang wurde unterbrochen.</span><span class="sxs-lookup"><span data-stu-id="1cc9b-167">A blocking operation was interrupted.</span></span> |
| <span data-ttu-id="1cc9b-168">**Wsaabval**</span><span class="sxs-lookup"><span data-stu-id="1cc9b-168">**WSAEINVAL**</span></span> | <span data-ttu-id="1cc9b-169">Der *dwIoControlCode* -Parameter ist kein gültiger Befehl, oder ein angegebener Eingabeparameter ist nicht zulässig, oder der Befehl ist nicht auf den angegebenen Sockettyp anwendbar.</span><span class="sxs-lookup"><span data-stu-id="1cc9b-169">The *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> |
| <span data-ttu-id="1cc9b-170">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="1cc9b-170">**WSAENETDOWN**</span></span> | <span data-ttu-id="1cc9b-171">Das Netzwerk Subsystem ist fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="1cc9b-171">The network subsystem has failed.</span></span> |
| <span data-ttu-id="1cc9b-172">**Wsaumoproumopt**</span><span class="sxs-lookup"><span data-stu-id="1cc9b-172">**WSAENOPROTOOPT**</span></span> | <span data-ttu-id="1cc9b-173">Die Socketoption wird für das angegebene Protokoll nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1cc9b-173">The socket option is not supported on the specified protocol.</span></span> |
| <span data-ttu-id="1cc9b-174">**WSAENOTCONN**</span><span class="sxs-lookup"><span data-stu-id="1cc9b-174">**WSAENOTCONN**</span></span> | <span data-ttu-id="1cc9b-175">Die Socket s ist nicht verbunden.</span><span class="sxs-lookup"><span data-stu-id="1cc9b-175">The socket s is not connected.</span></span> |
| <span data-ttu-id="1cc9b-176">**Wsaumotsock**</span><span class="sxs-lookup"><span data-stu-id="1cc9b-176">**WSAENOTSOCK**</span></span> | <span data-ttu-id="1cc9b-177">Der Deskriptor s ist kein Socket.</span><span class="sxs-lookup"><span data-stu-id="1cc9b-177">The descriptor s is not a socket.</span></span> |
| <span data-ttu-id="1cc9b-178">**WSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="1cc9b-178">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="1cc9b-179">Der angegebene ioctl-Befehl wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1cc9b-179">The specified IOCTL command is not supported.</span></span> <span data-ttu-id="1cc9b-180">Dieser Fehler wird zurückgegeben, wenn die IOCTL- **\_ Abfrage \_ Transport \_ Einstellung** des Transport Anbieters vom Transport Anbieter nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="1cc9b-180">This error is returned if the **SIO\_QUERY\_TRANSPORT\_SETTING** IOCTL is not supported by the transport provider.</span></span> |

## <a name="remarks"></a><span data-ttu-id="1cc9b-181">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1cc9b-181">Remarks</span></span>

<span data-ttu-id="1cc9b-182">Die IOCTL- **\_ Abfrage \_ Transport \_ Einstellung** ist unter Windows 8, Windows Server 2012 und neueren Versionen des Betriebssystems unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1cc9b-182">The **SIO\_QUERY\_TRANSPORT\_SETTING** IOCTL is supported on Windows 8, and Windows Server 2012, and later versions of the operating system.</span></span>

<span data-ttu-id="1cc9b-183">Die IOCTL- **\_ Abfrage \_ Transport \_ Einstellung** ist eine generische IOCTL, die zum Abfragen der Transport Einstellungen eines Sockets verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1cc9b-183">The **SIO\_QUERY\_TRANSPORT\_SETTING** IOCTL is a generic IOCTL used to query the transport settings on a socket.</span></span>
<span data-ttu-id="1cc9b-184">Die abgefragte Transport Einstellung basiert auf der [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) , die im *lpvinbuffer* -Parameter übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="1cc9b-184">The transport setting being queried is based on the [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) passed in the *lpvInBuffer* parameter.</span></span>

<span data-ttu-id="1cc9b-185">Die einzige Transport Einstellung, die derzeit definiert, ist die Funktion für die **echt \_ Zeit \_ Benachrichtigungs \_ Funktion** in einem TCP-Socket.</span><span class="sxs-lookup"><span data-stu-id="1cc9b-185">The only transport setting currently defines is for the **REAL\_TIME\_NOTIFICATION\_CAPABILITY** capability on a TCP socket.</span></span>

<span data-ttu-id="1cc9b-186">Wenn für die [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) , die im *lpvinbuffer* -Parameter übergeben wurde, das GUID-Element auf **echt \_ Zeit \_ Benachrichtigungs \_ Funktion** festgelegt ist, ist dies eine Anforderung zum Abfragen der Echt Zeit Benachrichtigungseinstellungen für den TCP-Socket, der mit dem [**controlchannel-**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) Parameter verwendet wird, um Hintergrund Netzwerk Benachrichtigungen in einer Windows Store-App zu empfangen</span><span class="sxs-lookup"><span data-stu-id="1cc9b-186">If the [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) passed in the *lpvInBuffer* parameter has the Guid member set to **REAL\_TIME\_NOTIFICATION\_CAPABILITY**, then this is a request to query the real time notification settings for the TCP socket used with the [**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) to receive background network notifications in a Windows Store app.</span></span>
<span data-ttu-id="1cc9b-187">Der *lpvinbuffer* -Parameter sollte auf eine [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) Struktur zeigen.</span><span class="sxs-lookup"><span data-stu-id="1cc9b-187">The *lpvInBuffer* parameter should point to a [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) structure.</span></span>
<span data-ttu-id="1cc9b-188">Der *lpvoutbuffer* -Parameter sollte auf eine **Ausgabestruktur in Echtzeit- \_ \_ Benachrichtigungs \_ Einstellungen \_** zeigen.</span><span class="sxs-lookup"><span data-stu-id="1cc9b-188">The *lpvOutBuffer* parameter should point to a **REAL\_TIME\_NOTIFICATION\_SETTING\_OUTPUT** structure.</span></span>
<span data-ttu-id="1cc9b-189">Diese Transport Einstellung gilt nur für TCP-Sockets.</span><span class="sxs-lookup"><span data-stu-id="1cc9b-189">This transport setting applies only to TCP sockets.</span></span>
<span data-ttu-id="1cc9b-190">Mit dieser Transport Einstellung kann WinInet oder ähnliche Netzwerkdienste einen bestimmten TCP-Socket Abfragen, um den Status des [**controlchannel-Auslösers**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="1cc9b-190">This transport setting provides a way for WinInet or similar network services to query a given TCP socket to determine the [**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) status.</span></span>
<span data-ttu-id="1cc9b-191">Eine Windows Store-App ruft diese IOCTL nicht direkt auf.</span><span class="sxs-lookup"><span data-stu-id="1cc9b-191">A Windows Store app will not call this IOCTL directly.</span></span>
<span data-ttu-id="1cc9b-192">Wenn der Aufruf von [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) oder **wspioctl** erfolgreich ist, gibt diese IOCTL eine Ausgabestruktur der **echt \_ Zeit \_ Benachrichtigungs \_ Einstellung \_** mit dem aktuellen Status zurück.</span><span class="sxs-lookup"><span data-stu-id="1cc9b-192">If the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** call is successful, this IOCTL returns a **REAL\_TIME\_NOTIFICATION\_SETTING\_OUTPUT** structure with the current status.</span></span>

<span data-ttu-id="1cc9b-193">Die IOCTL- **\_ Abfrage \_ Transport \_ Einstellung** ist eine Möglichkeit für WinInet oder ähnliche Netzwerkdienste, den Transport Einstellungs Status für einen bestimmten TCP-Socket abzufragen, um zu bestimmen, ob [**controlchannel-Auslösers**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) auf dem Socket aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="1cc9b-193">The **SIO\_QUERY\_TRANSPORT\_SETTING** IOCTL provides a way for WinInet or similar network services to query for the transport setting status for a given TCP socket to determine if [**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) is enabled on the socket.</span></span>
<span data-ttu-id="1cc9b-194">Eine Windows Store-App ruft diese IOCTL nicht direkt auf.</span><span class="sxs-lookup"><span data-stu-id="1cc9b-194">A Windows Store app will not call this IOCTL directly.</span></span>

<span data-ttu-id="1cc9b-195">Diese IOCTL gilt nur für TCP-Sockets.</span><span class="sxs-lookup"><span data-stu-id="1cc9b-195">This IOCTL applies only to TCP sockets.</span></span>

## <a name="see-also"></a><span data-ttu-id="1cc9b-196">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1cc9b-196">See also</span></span>

[<span data-ttu-id="1cc9b-197">**CONTROL_CHANNEL_TRIGGER_STATUS**</span><span class="sxs-lookup"><span data-stu-id="1cc9b-197">**CONTROL_CHANNEL_TRIGGER_STATUS**</span></span>](/windows/desktop/api/mstcpip/ne-mstcpip-control_channel_trigger_status)

[<span data-ttu-id="1cc9b-198">**ControlChannelTrigger**</span><span class="sxs-lookup"><span data-stu-id="1cc9b-198">**ControlChannelTrigger**</span></span>](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger)

[<span data-ttu-id="1cc9b-199">**REAL_TIME_NOTIFICATION_SETTING_OUTPUT**</span><span class="sxs-lookup"><span data-stu-id="1cc9b-199">**REAL_TIME_NOTIFICATION_SETTING_OUTPUT**</span></span>](/windows/desktop/api/mstcpip/ns-mstcpip-real_time_notification_setting_output)

[<span data-ttu-id="1cc9b-200">**SIO_APPLY_TRANSPORT_SETTING**</span><span class="sxs-lookup"><span data-stu-id="1cc9b-200">**SIO_APPLY_TRANSPORT_SETTING**</span></span>](sio-apply-transport-setting.md)

[<span data-ttu-id="1cc9b-201">Glühbirne</span><span class="sxs-lookup"><span data-stu-id="1cc9b-201">socket</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="1cc9b-202">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="1cc9b-202">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[<span data-ttu-id="1cc9b-203">**Wsagein verlappedresult**</span><span class="sxs-lookup"><span data-stu-id="1cc9b-203">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="1cc9b-204">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="1cc9b-204">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="1cc9b-205">**Wsaoverlgetauscht**</span><span class="sxs-lookup"><span data-stu-id="1cc9b-205">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="1cc9b-206">**Wsasocketa**</span><span class="sxs-lookup"><span data-stu-id="1cc9b-206">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="1cc9b-207">**Wsasocketw**</span><span class="sxs-lookup"><span data-stu-id="1cc9b-207">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
