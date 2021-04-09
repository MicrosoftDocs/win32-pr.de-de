---
description: Steuercode Ruft den Umleitungs Kontext für einen Umleitungs Daten Satz ab, der von einem Windows-Filter für die Platt Form Umleitung verwendet wird
ms.assetid: 87DB11BB-E08D-49DF-A211-133D813373E0
title: SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT Steuerungs Codes
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 1e5e5f6c56411ada1e87e8cdf240a89f9c293e4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129128"
---
# <a name="sio_query_wfp_connection_redirect_context-control-code"></a><span data-ttu-id="7806e-103">SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT Steuerungs Codes</span><span class="sxs-lookup"><span data-stu-id="7806e-103">SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT Control Code</span></span>

## <a name="description"></a><span data-ttu-id="7806e-104">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7806e-104">Description</span></span>

<span data-ttu-id="7806e-105">Der Kontext Steuerungs Code für die **\_ \_ WFP- \_ Verbindungs \_ \_ Umleitung für den WFP-Abfrage** Ruft den Umleitungs Kontext für einen von einem WFP-Umleitungs Dienst (Windows Filtering Platform) verwendeten Umleitungs Daten Satz ab</span><span class="sxs-lookup"><span data-stu-id="7806e-105">The **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_CONTEXT** control code retrieves the redirect context for a redirect record used by a Windows Filtering Platform (WFP) redirect service.</span></span>

<span data-ttu-id="7806e-106">Um diesen Vorgang auszuführen, wenden Sie die [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) -oder **wspioctl** -Funktion mit den folgenden Parametern an.</span><span class="sxs-lookup"><span data-stu-id="7806e-106">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
  (socket) s,             // descriptor identifying a socket
  SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT, // dwIoControlCode
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
  SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT, // dwIoControlCode
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

## <a name="parameters"></a><span data-ttu-id="7806e-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="7806e-107">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="7806e-108">s</span><span class="sxs-lookup"><span data-stu-id="7806e-108">s</span></span>

<span data-ttu-id="7806e-109">Ein Deskriptor, der einen Socket identifiziert.</span><span class="sxs-lookup"><span data-stu-id="7806e-109">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="7806e-110">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="7806e-110">dwIoControlCode</span></span>

<span data-ttu-id="7806e-111">Der Steuerelement Code für den Vorgang.</span><span class="sxs-lookup"><span data-stu-id="7806e-111">The control code for the operation.</span></span>
<span data-ttu-id="7806e-112">Verwenden Sie für diesen Vorgang den **\_ \_ WFP- \_ Verbindungs \_ Umleitungs \_ Kontext** der-Abfrage.</span><span class="sxs-lookup"><span data-stu-id="7806e-112">Use **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_CONTEXT** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="7806e-113">lpvinbuffer</span><span class="sxs-lookup"><span data-stu-id="7806e-113">lpvInBuffer</span></span>

<span data-ttu-id="7806e-114">Ein Zeiger auf den Eingabepuffer.</span><span class="sxs-lookup"><span data-stu-id="7806e-114">A pointer to the input buffer.</span></span>
<span data-ttu-id="7806e-115">Dieser Parameter wird für diesen Vorgang nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="7806e-115">This parameter is unused for this operation.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="7806e-116">cbinbuffer</span><span class="sxs-lookup"><span data-stu-id="7806e-116">cbInBuffer</span></span>

<span data-ttu-id="7806e-117">Die Größe des Eingabe Puffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="7806e-117">The size, in bytes, of the input buffer.</span></span>
<span data-ttu-id="7806e-118">Dieser Parameter wird für diesen Vorgang nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="7806e-118">This parameter is unused for this operation.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="7806e-119">lpvoutbuffer</span><span class="sxs-lookup"><span data-stu-id="7806e-119">lpvOutBuffer</span></span>

<span data-ttu-id="7806e-120">Ein Zeiger auf den Ausgabepuffer.</span><span class="sxs-lookup"><span data-stu-id="7806e-120">A pointer to the output buffer.</span></span>
<span data-ttu-id="7806e-121">Dieser Parameter sollte auf einen **ulong** -Datentyp zeigen, wenn die Parameter *lpoverlgetauscht* und *lpCompletionRoutine* **null** sind.</span><span class="sxs-lookup"><span data-stu-id="7806e-121">This parameter should point to a **ULONG** data type if the *lpOverlapped* and *lpCompletionRoutine* parameters are **NULL**.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="7806e-122">cboutbuffer</span><span class="sxs-lookup"><span data-stu-id="7806e-122">cbOutBuffer</span></span>

<span data-ttu-id="7806e-123">Die Größe des Ausgabepuffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="7806e-123">The size, in bytes, of the output buffer.</span></span>
<span data-ttu-id="7806e-124">Dieser Parameter muss mindestens die Größe eines **ulong** -Datentyps aufweisen.</span><span class="sxs-lookup"><span data-stu-id="7806e-124">This parameter must be at least the size of a **ULONG** data type.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="7806e-125">lpcbbyteszurück gegeben</span><span class="sxs-lookup"><span data-stu-id="7806e-125">lpcbBytesReturned</span></span>

<span data-ttu-id="7806e-126">Ein Zeiger auf eine Variable, die die Größe der im Ausgabepuffer gespeicherten Daten (in Bytes) empfängt.</span><span class="sxs-lookup"><span data-stu-id="7806e-126">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>

<span data-ttu-id="7806e-127">Wenn der Ausgabepuffer zu klein ist, schlägt der-Befehl fehl, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) gibt [**WSAEINVAL**](windows-sockets-error-codes-2.md)zurück, und der *lpcbbytesreturns* -Parameter verweist auf den **DWORD** -Wert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="7806e-127">If the output buffer is too small, the call fails, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns [**WSAEINVAL**](windows-sockets-error-codes-2.md), and the *lpcbBytesReturned* parameter points to a **DWORD** value of zero.</span></span>

<span data-ttu-id="7806e-128">Wenn *lpoverlgetauscht* gleich **null** ist, kann der **DWORD** -Wert, auf den der *lpcbbytesall* -Parameter verweist, der bei einem erfolgreichen-Vorgang zurückgegeben wird, nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="7806e-128">If *lpOverlapped* is **NULL**, the **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned on a successful call cannot be zero.</span></span>

<span data-ttu-id="7806e-129">Wenn der *lpoverllapp* -Parameter für überlappende Sockets nicht **null** ist, werden Vorgänge, die nicht sofort abgeschlossen werden können, initiiert, und der Abschluss wird zu einem späteren Zeitpunkt angegeben.</span><span class="sxs-lookup"><span data-stu-id="7806e-129">If the *lpOverlapped* parameter is not **NULL** for overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>
<span data-ttu-id="7806e-130">Der **DWORD** -Wert, auf den der zurückgegebene *lpcbbyteszurück gegebene* Parameter verweist, kann NULL sein, da die Größe der gespeicherten Daten erst bestimmt werden kann, wenn der überlappende Vorgang abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="7806e-130">The **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned may be zero since the size of the data stored can't be determined until the overlapped operation has completed.</span></span>
<span data-ttu-id="7806e-131">Der endgültige Abschluss Status kann abgerufen werden, wenn die geeignete Vervollständigungs Methode signalisiert wird, wenn der Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="7806e-131">The final completion status can be retrieved when the appropriate completion method is signaled when the operation has completed.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="7806e-132">lpvoverlgetauscht</span><span class="sxs-lookup"><span data-stu-id="7806e-132">lpvOverlapped</span></span>

<span data-ttu-id="7806e-133">Ein Zeiger auf eine [**wsaoverllapp**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="7806e-133">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="7806e-134">Wenn Socket *s* ohne das überlappende Attribut erstellt wurde, wird der *lpoverllapp* -Parameter ignoriert.</span><span class="sxs-lookup"><span data-stu-id="7806e-134">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="7806e-135">Wenn *s* mit dem überlappenden Attribut geöffnet wurde und der *lpoverlgetauscht* -Parameter nicht **null** ist, wird der Vorgang als überlappende (asynchrone) Operation ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7806e-135">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="7806e-136">In diesem Fall muss der *lpoverllapp* -Parameter auf eine gültige [**wsaoverllapp**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) -Struktur zeigen.</span><span class="sxs-lookup"><span data-stu-id="7806e-136">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="7806e-137">Bei überlappenden Vorgängen gibt die Funktion [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) oder **wspioctl** sofort zurück, und die entsprechende Vervollständigungs Methode wird signalisiert, wenn der Vorgang abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="7806e-137">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="7806e-138">Andernfalls gibt die Funktion nicht zurück, bis der Vorgang abgeschlossen ist oder ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="7806e-138">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="7806e-139">lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="7806e-139">lpCompletionRoutine</span></span>

<span data-ttu-id="7806e-140">Typ: \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="7806e-140">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="7806e-141">Ein Zeiger auf die Vervollständigungs Routine, die aufgerufen wird, wenn der Vorgang abgeschlossen wurde (bei nicht überlappenden Sockets ignoriert).</span><span class="sxs-lookup"><span data-stu-id="7806e-141">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="7806e-142">lpthreadid</span><span class="sxs-lookup"><span data-stu-id="7806e-142">lpThreadId</span></span>

<span data-ttu-id="7806e-143">Ein Zeiger auf eine [**wsathreadid**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) -Struktur, die vom Anbieter in einem nachfolgenden [**wpuqueueapc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc)-Rückruf verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7806e-143">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="7806e-144">Der Anbieter sollte die referenzierte [**wsathreadid**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) -Struktur (nicht den Zeiger auf dieselbe) speichern, bis die [**wpuqueueapc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) -Funktion zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="7806e-144">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="7806e-145">**Hinweis**  Dieser Parameter gilt nur für die **wspioctl** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="7806e-145">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="7806e-146">lperrno</span><span class="sxs-lookup"><span data-stu-id="7806e-146">lpErrno</span></span>

<span data-ttu-id="7806e-147">Ein Zeiger auf den Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="7806e-147">A pointer to the error code.</span></span>

<span data-ttu-id="7806e-148">**Hinweis**  Dieser Parameter gilt nur für die **wspioctl** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="7806e-148">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="7806e-149">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7806e-149">Return value</span></span>

<span data-ttu-id="7806e-150">Wenn der Vorgang erfolgreich abgeschlossen wird, gibt die [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) -oder **wspioctl** -Funktion NULL zurück.</span><span class="sxs-lookup"><span data-stu-id="7806e-150">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="7806e-151">Wenn der Vorgang fehlschlägt oder aussteht, gibt die Funktion [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) oder **wspioctl** einen **\_ Socketfehler** zurück.</span><span class="sxs-lookup"><span data-stu-id="7806e-151">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="7806e-152">Um erweiterte Fehlerinformationen abzurufen, nennen Sie [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="7806e-152">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="7806e-153">Fehlercode</span><span class="sxs-lookup"><span data-stu-id="7806e-153">Error code</span></span> | <span data-ttu-id="7806e-154">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="7806e-154">Meaning</span></span> |
|------------|---------|
| <span data-ttu-id="7806e-155">**ausstehende WSA-e/a \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7806e-155">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="7806e-156">Ein übergebener Vorgang wurde erfolgreich initiiert, und der Abschluss wird zu einem späteren Zeitpunkt angegeben.</span><span class="sxs-lookup"><span data-stu-id="7806e-156">An overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="7806e-157">**WSA- \_ Vorgang \_ abgebrochen**</span><span class="sxs-lookup"><span data-stu-id="7806e-157">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="7806e-158">Ein über Lapp ender Vorgang wurde aufgrund der Schließung des Sockets oder der Ausführung des SIO_FLUSH ioctl-Befehls abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="7806e-158">An overlapped operation was canceled due to the closure of the socket or the execution of the SIO_FLUSH IOCTL command.</span></span> |
| <span data-ttu-id="7806e-159">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="7806e-159">**WSAEFAULT**</span></span> | <span data-ttu-id="7806e-160">Der Parameter " *lpvoutbuffer*", " *lpcbbytesis*", " *lpoverlgetauscht*" oder " *lpCompletionRoutine* " ist nicht vollständig in einem gültigen Teil des Benutzer Adressraums enthalten.</span><span class="sxs-lookup"><span data-stu-id="7806e-160">The *lpvOutBuffer*, *lpcbBytesReturned*, *lpOverlapped*, or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="7806e-161">**Wsaeingabe Progress**</span><span class="sxs-lookup"><span data-stu-id="7806e-161">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="7806e-162">Die-Funktion wird aufgerufen, wenn ein Rückruf ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7806e-162">The function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="7806e-163">**Wsaeingabe**</span><span class="sxs-lookup"><span data-stu-id="7806e-163">**WSAEINTR**</span></span> | <span data-ttu-id="7806e-164">Ein Blockierungs Vorgang wurde unterbrochen.</span><span class="sxs-lookup"><span data-stu-id="7806e-164">A blocking operation was interrupted.</span></span> |
| <span data-ttu-id="7806e-165">**Wsaabval**</span><span class="sxs-lookup"><span data-stu-id="7806e-165">**WSAEINVAL**</span></span> | <span data-ttu-id="7806e-166">Der *dwIoControlCode* -Parameter ist kein gültiger Befehl, oder ein angegebener Eingabeparameter ist nicht zulässig, oder der Befehl ist nicht auf den angegebenen Sockettyp anwendbar.</span><span class="sxs-lookup"><span data-stu-id="7806e-166">The *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> <span data-ttu-id="7806e-167">Dieser Fehler wird zurückgegeben, wenn der *cboutbuffer* -Parameter kleiner als die Größe eines **ulong** -Datentyps ist.</span><span class="sxs-lookup"><span data-stu-id="7806e-167">This error is returned if the *cbOutBuffer* parameter is less than the size of a **ULONG** data type.</span></span> |
| <span data-ttu-id="7806e-168">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="7806e-168">**WSAENETDOWN**</span></span> | <span data-ttu-id="7806e-169">Das Netzwerk Subsystem ist fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="7806e-169">The network subsystem has failed.</span></span> |
| <span data-ttu-id="7806e-170">**Wsaumoproumopt**</span><span class="sxs-lookup"><span data-stu-id="7806e-170">**WSAENOPROTOOPT**</span></span> | <span data-ttu-id="7806e-171">Die Socketoption wird für das angegebene Protokoll nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7806e-171">The socket option is not supported on the specified protocol.</span></span> |
| <span data-ttu-id="7806e-172">**WSAENOTCONN**</span><span class="sxs-lookup"><span data-stu-id="7806e-172">**WSAENOTCONN**</span></span> | <span data-ttu-id="7806e-173">Die Socket *s* ist nicht verbunden.</span><span class="sxs-lookup"><span data-stu-id="7806e-173">The socket *s* is not connected.</span></span> |
| <span data-ttu-id="7806e-174">**Wsaumotsock**</span><span class="sxs-lookup"><span data-stu-id="7806e-174">**WSAENOTSOCK**</span></span> | <span data-ttu-id="7806e-175">Der Deskriptor *s* ist kein Socket.</span><span class="sxs-lookup"><span data-stu-id="7806e-175">The descriptor *s* is not a socket.</span></span> |
| <span data-ttu-id="7806e-176">**WSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="7806e-176">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="7806e-177">Der angegebene ioctl-Befehl wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7806e-177">The specified IOCTL command is not supported.</span></span> <span data-ttu-id="7806e-178">Dieser Fehler wird zurückgegeben, wenn der Kontext der IOCTL-Abfrage für die **\_ \_ WFP- \_ Verbindungs \_ \_ Umleitung** vom Transportanbieter nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="7806e-178">This error is returned if the **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_CONTEXT** IOCTL is not supported by the transport provider.</span></span> |

## <a name="remarks"></a><span data-ttu-id="7806e-179">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7806e-179">Remarks</span></span>

<span data-ttu-id="7806e-180">Der **\_ \_ \_ Verbindungs \_ Umleitungs \_ Kontext** ioctl für die WFP-Abfrage wird unter Windows 8, Windows Server 2012 und neueren Versionen des Betriebssystems unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7806e-180">The **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_CONTEXT** IOCTL is supported on Windows 8, and Windows Server 2012, and later versions of the operating system.</span></span>

<span data-ttu-id="7806e-181">WFP ermöglicht den Zugriff auf den TCP/IP-Paket Verarbeitungs Pfad, in dem ausgehende und eingehende Pakete überprüft oder geändert werden können, bevor Sie weiterverarbeitet werden können.</span><span class="sxs-lookup"><span data-stu-id="7806e-181">WFP allows access to the TCP/IP packet processing path, wherein outgoing and incoming packets can be examined or changed before allowing them to be processed further.</span></span>
<span data-ttu-id="7806e-182">Durch das Tippen auf den TCP/IP-Verarbeitungs Pfad können unabhängige Softwarehersteller (ISVs) leichter Firewalls, Antivirussoftware, Diagnosesoftware und andere Arten von Anwendungen und Diensten erstellen.</span><span class="sxs-lookup"><span data-stu-id="7806e-182">By tapping into the TCP/IP processing path, independent software vendors (ISVs) can more easily create firewalls, antivirus software, diagnostic software, and other types of applications and services.</span></span>
<span data-ttu-id="7806e-183">WFP stellt Komponenten im Benutzermodus und im Kernel Modus bereit, sodass Drittanbieter-ISVs an den Filter Entscheidungen teilnehmen können, die auf mehreren Ebenen im TCP/IP-Protokollstapel und im gesamten Betriebssystem stattfinden.</span><span class="sxs-lookup"><span data-stu-id="7806e-183">WFP provides user-mode and kernel-mode components so that third-party ISVs can participate in the filtering decisions that take place at several layers in the TCP/IP protocol stack and throughout the operating system.</span></span>
<span data-ttu-id="7806e-184">Mithilfe des WFP-Verbindungs Umleitungs Features kann ein WFP-Legenden-Kernel-Treiber eine Verbindung lokal an einen Benutzermodusprozess umleiten, eine Inhalts Untersuchung im Benutzermodus durchführen und den überprüften Inhalt mithilfe einer anderen Verbindung zum ursprünglichen Ziel weiterleiten.</span><span class="sxs-lookup"><span data-stu-id="7806e-184">The WFP connection redirect feature allows a WFP callout kernel driver to redirect a connection locally to a user-mode process, perform content inspection in user-mode, and forward the inspected content using a different connection to the original destination.</span></span>

<span data-ttu-id="7806e-185">Der **Netzwerk \_ \_ \_ Verbindungs \_ Weiterleitungs \_ Kontext** ioctl und mehrere andere verwandte IOCTLs-Abfragen sind im Benutzermodus enthalten, mit denen mehrere WFP-basierte Verbindungs Proxy Anwendungen den gleichen Daten Verkehrsfluss auf kooperative Weise überprüfen können.</span><span class="sxs-lookup"><span data-stu-id="7806e-185">The **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_CONTEXT** IOCTL and several other related IOCTLS are user-mode components used to allow multiple WFP-based connection proxy applications to inspect the same traffic flow in a cooperative manner.</span></span>
<span data-ttu-id="7806e-186">Jeder Inspektions Agent kann den Netzwerk Datenverkehr, der bereits von einem anderen Inspektions Agent überprüft wurde, sicher erneut überprüfen.</span><span class="sxs-lookup"><span data-stu-id="7806e-186">Each inspection agent can safely re-inspect network traffic that has already been inspected by another inspection agent.</span></span>
<span data-ttu-id="7806e-187">Durch das vorhanden sein mehrerer Proxys (z. b. durch verschiedene ISVs) kann die Verbindung, die von einem Proxy für die Kommunikation mit dem endgültigen Ziel verwendet wird, wiederum von einem zweiten Proxy umgeleitet werden, und diese neue Verbindung kann erneut vom ursprünglichen Proxy umgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="7806e-187">With the presence of multiple proxies (developed by different ISVs, for example) the connection used by one proxy to communicate with the final destination could in turn be redirected by a second proxy, and that new connection could again be redirected by the original proxy.</span></span>
<span data-ttu-id="7806e-188">Ohne Verbindungs Nachverfolgung erreicht die ursprüngliche Verbindung möglicherweise nie das endgültige Ziel, weil Sie in einer unendlichen Proxy Schleife hängen bleibt.</span><span class="sxs-lookup"><span data-stu-id="7806e-188">Without connection tracking, the original connection might never reach its final destination as it gets stuck in an infinite proxy loop.</span></span>

<span data-ttu-id="7806e-189">Der **\_ \_ \_ Verbindungs \_ Umleitungs \_ Kontext** ioctl für die WFP-Abfrage wird verwendet, um mehreren WFP-basierten Verbindungs Proxy Anwendungen die Möglichkeit zu geben, denselben Daten Verkehrsfluss auf kooperative Weise zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="7806e-189">The **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_CONTEXT** IOCTL is used to allow multiple WFP-based connection proxy applications to inspect the same traffic flow in a cooperative manner.</span></span>
<span data-ttu-id="7806e-190">Jeder Inspektions Agent kann den Netzwerk Datenverkehr, der bereits von einem anderen Inspektions Agent überprüft wurde, sicher erneut überprüfen.</span><span class="sxs-lookup"><span data-stu-id="7806e-190">Each inspection agent can safely re-inspect network traffic that has already been inspected by another inspection agent.</span></span>
<span data-ttu-id="7806e-191">Durch das vorhanden sein mehrerer Proxys (z. b. durch verschiedene ISVs) kann die Verbindung, die von einem Proxy für die Kommunikation mit dem endgültigen Ziel verwendet wird, wiederum von einem zweiten Proxy umgeleitet werden, und diese neue Verbindung kann erneut vom ursprünglichen Proxy umgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="7806e-191">With the presence of multiple proxies (developed by different ISVs, for example) the connection used by one proxy to communicate with the final destination could in turn be redirected by a second proxy, and that new connection could again be redirected by the original proxy.</span></span>
<span data-ttu-id="7806e-192">Ohne Verbindungs Nachverfolgung erreicht die ursprüngliche Verbindung möglicherweise nie das endgültige Ziel, weil Sie in einer unendlichen Proxy Schleife hängen bleibt.</span><span class="sxs-lookup"><span data-stu-id="7806e-192">Without connection tracking, the original connection might never reach its final destination as it gets stuck in an infinite proxy loop.</span></span>
<span data-ttu-id="7806e-193">Der **\_ \_ \_ Verbindungs \_ Umleitungs \_ Kontext** ioctl für die WFP-Abfrage wird verwendet, um die Proxy Verbindungs Nachverfolgung für umgeleitete Socketverbindungen bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="7806e-193">The **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_CONTEXT** IOCTL is used to provide proxied connection tracking on redirected socket connections.</span></span>
<span data-ttu-id="7806e-194">Diese WFP-Funktion ermöglicht das Nachverfolgen von Umleitungs Datensätzen von der anfänglichen Umleitung einer Verbindung zur endgültigen Verbindung zum Ziel.</span><span class="sxs-lookup"><span data-stu-id="7806e-194">This WFP feature facilitates tracking of redirection records from the initial redirect of a connection to the final connection to the destination.</span></span>

<span data-ttu-id="7806e-195">Die **\_ Abfrage Datensätze für die WFP-Verbindung mit der Leistungs \_ \_ \_ \_ Datensätze** ". ioctl" werden von einem WFP-basierten Umleitungs Dienst verwendet, um den Umleitungs Daten Satz von der akzeptierten TCP/IP-Paket Verbindung (z. b. den verbundenen Socket für einen TCP-Socket oder einen UDP-Socket) abzurufen **\_ \_**</span><span class="sxs-lookup"><span data-stu-id="7806e-195">The **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL is used by a WFP-based redirect service to retrieve the redirect record from the accepted TCP/IP packet connection (the connected socket for a TCP socket or a UDP socket, for example) redirected to it by its companion kernel-mode callout registered at **ALE\_CONNECT\_REDIRECT** layers in a kernel-mode driver.</span></span>
<span data-ttu-id="7806e-196">Der Kontext der IOCTL- **\_ Abfrage- \_ WFP- \_ Verbindungs \_ Umleitung \_** wird von einem WFP-basierten Umleitungs Dienst verwendet, um den Umleitungs Kontext für einen Umleitungs Daten Satz von der akzeptierten TCP/IP-Paket Verbindung abzurufen (z. b. den verbundenen Socket für einen TCP-Socket oder einen UDP-Socket), der durch seine Begleit Legende auf **ALE_CONNECT_REDIRECT** Ebenen registriert wird.</span><span class="sxs-lookup"><span data-stu-id="7806e-196">The **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_CONTEXT** IOCTL is used by a WFP-based redirect service to retrieve the redirect context for a redirect record from the accepted TCP/IP packet connection (the connected socket for a TCP socket or a UDP socket, for example) redirected to it by its companion callout registered at **ALE_CONNECT_REDIRECT** layers.</span></span>
<span data-ttu-id="7806e-197">Der Umleitungs Kontext ist optional und wird verwendet, wenn der aktuelle Umleitungs Status einer Verbindung darin besteht, dass die Verbindung vom aufrufenden Umleitungs Dienst umgeleitet wurde oder die Verbindung zuvor vom aufrufenden Umleitungs Dienst umgeleitet, aber später von einem anderen Umleitungs Dienst umgeleitet wurde.</span><span class="sxs-lookup"><span data-stu-id="7806e-197">The redirect context is optional and is used if the current redirection state of a connection is that the connection was redirected by the calling redirect service or the connection was previously redirected by the calling redirect service but later redirected again by a different redirect service.</span></span>
<span data-ttu-id="7806e-198">Der Umleitungs Dienst überträgt den abgerufenen Umleitungs Daten Satz an den TCP-Socket, den er zum Proxy des ursprünglichen Inhalts verwendet, indem er die IOCTL- **\_ \_ \_ Verbindungs \_ \_ Datensätze der WFP-Verbindung** verwendet</span><span class="sxs-lookup"><span data-stu-id="7806e-198">The redirect service transfers the retrieved redirect record to the TCP socket it uses to proxy the original content using the **SIO\_SET\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL.</span></span>

<span data-ttu-id="7806e-199">Da der WFP-Umleitungs Kontext ein vom Umleitungs Dienst festgelegter datblob mit variabler Länge ist, kann der Aufrufer entweder einen großen Ausgabepuffer bereitstellen (z. b. einen 1K-Puffer, auf den der *lpvoutbuffer* -Parameter zeigt) oder als Ausgabepuffergröße im *cboutbuffer* -Parameter 0 übergeben, um die Puffergröße abzufragen,</span><span class="sxs-lookup"><span data-stu-id="7806e-199">Since the WFP redirect context is a variable length data blob set by the redirect service, the caller can either supply a large output buffer (a 1K buffer pointed to by the *lpvOutBuffer* parameter, for example) or can pass as an output buffer size in the *cbOutBuffer* parameter of 0 to query the buffer size required to hold the returned blob.</span></span>
<span data-ttu-id="7806e-200">Wenn die Ausgabepuffergröße nicht ausreichen, um die Daten zu speichern, gibt die [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) -oder **wspioctl** -Funktion den **Fehler "Fehler \_ unzureichend \_** " zurück, und die erforderliche Puffergröße wird als Wert zurückgegeben, auf den der *lpcbbytesreturn* -Parameter verweist.</span><span class="sxs-lookup"><span data-stu-id="7806e-200">If the output buffer size is not sufficient the hold the data, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** functions will return **ERROR\_INSUFFICIENT\_BUFFER** and the required buffer size will be returned in value pointed to by the *lpcbBytesReturned* parameter.</span></span>

<span data-ttu-id="7806e-201">Die Anwendung, die **den \_ WF-Abfrage- \_ WF \-P_CONNECTION \_ Umleitungs \_ Datensätze aufführt** , muss das BLOB, das die abgerufenen Umleitungs Datensätze enthält, nicht verstehen.</span><span class="sxs-lookup"><span data-stu-id="7806e-201">The application calling the **SIO\_QUERY\_WF\P_CONNECTION\_REDIRECT\_RECORDS** IOCTL does not need to understand the blob containing the redirect records retrieved.</span></span>
<span data-ttu-id="7806e-202">Dies ist ein undurchsichtiges BLOB von Daten, das die Anwendung abrufen und an den neuen Socket zurückgeben muss.</span><span class="sxs-lookup"><span data-stu-id="7806e-202">This is an opaque blob of data that the application needs to retrieve and pass back to the new socket.</span></span>

## <a name="see-also"></a><span data-ttu-id="7806e-203">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7806e-203">See also</span></span>

[<span data-ttu-id="7806e-204">**IPPROTO_IP Socketoptionen**</span><span class="sxs-lookup"><span data-stu-id="7806e-204">**IPPROTO_IP Socket Options**</span></span>](/windows/desktop/winsock/ipproto-ip-socket-options)

[<span data-ttu-id="7806e-205">**SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS**</span><span class="sxs-lookup"><span data-stu-id="7806e-205">**SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS**</span></span>](sio-query-wfp-connection-redirect-records.md)

[<span data-ttu-id="7806e-206">**SIO_SET_WFP_CONNECTION_REDIRECT_RECORDS**</span><span class="sxs-lookup"><span data-stu-id="7806e-206">**SIO_SET_WFP_CONNECTION_REDIRECT_RECORDS**</span></span>](sio-set-wfp-connection-redirect-records.md)

[<span data-ttu-id="7806e-207">**Glühbirne**</span><span class="sxs-lookup"><span data-stu-id="7806e-207">**socket**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="7806e-208">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="7806e-208">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[<span data-ttu-id="7806e-209">**Wsagein verlappedresult**</span><span class="sxs-lookup"><span data-stu-id="7806e-209">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="7806e-210">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="7806e-210">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="7806e-211">**Wsaoverlgetauscht**</span><span class="sxs-lookup"><span data-stu-id="7806e-211">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="7806e-212">**Wsasocketa**</span><span class="sxs-lookup"><span data-stu-id="7806e-212">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="7806e-213">**Wsasocketw**</span><span class="sxs-lookup"><span data-stu-id="7806e-213">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
