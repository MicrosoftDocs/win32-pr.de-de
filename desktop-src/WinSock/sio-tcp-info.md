---
description: Steuerungs Code Ruft die TCP (Transmission Control Protocol)-Statistik für einen angegebenen Socket ab.
ms.assetid: AB5F25B6-D2D2-42D7-8189-06CAC4842C66
title: SIO_TCP_INFO Steuerungs Codes
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: cea9a2d31654d1263f285ee9967b24700fe25138
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/06/2021
ms.locfileid: "106364309"
---
# <a name="sio_tcp_info-control-code"></a><span data-ttu-id="154ab-103">SIO_TCP_INFO Steuerungs Codes</span><span class="sxs-lookup"><span data-stu-id="154ab-103">SIO_TCP_INFO Control Code</span></span>

## <a name="description"></a><span data-ttu-id="154ab-104">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="154ab-104">Description</span></span>

<span data-ttu-id="154ab-105">Der **\_ KTCP- \_ Informations** Steuerungs Code Ruft die TCP (Transmission Control Protocol)-Statistik für einen angegebenen Socket ab.</span><span class="sxs-lookup"><span data-stu-id="154ab-105">The **SIO\_TCP\_INFO** control code retrieves the Transmission Control Protocol (TCP) statistics for a specified socket.</span></span>

<span data-ttu-id="154ab-106">Um diesen Vorgang auszuführen, wenden Sie die [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) -oder **wspioctl** -Funktion mit den folgenden Parametern an.</span><span class="sxs-lookup"><span data-stu-id="154ab-106">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_TCP_INFO,                // dwIoControlCode
  (LPVOID) lpvInBuffer,   // pointer to a DWORD
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,         // pointer to a TCP_INFO_v0 structure
  (DWORD) cbOutBuffer,       // size of the output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_TCP_INFO,                // dwIoControlCode
  (LPVOID) lpvInBuffer,   // pointer to a DWORD
  (DWORD) cbInBuffer,           // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,         // pointer to a TCP_INFO_v0 structure
  (DWORD) cbOutBuffer,       // size of the output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,   // a WSATHREADID structure
  (LPINT) lpErrno   // a pointer to the error code.
);
```

## <a name="parameters"></a><span data-ttu-id="154ab-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="154ab-107">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="154ab-108">s</span><span class="sxs-lookup"><span data-stu-id="154ab-108">s</span></span>

<span data-ttu-id="154ab-109">Ein Deskriptor, der einen Socket identifiziert.</span><span class="sxs-lookup"><span data-stu-id="154ab-109">A descriptor that identifies a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="154ab-110">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="154ab-110">dwIoControlCode</span></span>

<span data-ttu-id="154ab-111">Der Steuerelement Code für den Vorgang.</span><span class="sxs-lookup"><span data-stu-id="154ab-111">The control code for the operation.</span></span>
<span data-ttu-id="154ab-112">Verwenden Sie für diesen Vorgang die **\_ TCP-TCP- \_ Informationen** .</span><span class="sxs-lookup"><span data-stu-id="154ab-112">Use **SIO\_TCP\_INFO** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="154ab-113">lpvinbuffer</span><span class="sxs-lookup"><span data-stu-id="154ab-113">lpvInBuffer</span></span>

<span data-ttu-id="154ab-114">Ein Zeiger auf den Eingabepuffer.</span><span class="sxs-lookup"><span data-stu-id="154ab-114">A pointer to the input buffer.</span></span>
<span data-ttu-id="154ab-115">Dieser Parameter enthält einen Zeiger auf ein **DWORD** , das die Version des von Ihnen verwendeten CI- **\_ TCP- \_ Info** -Steuerungs Codes angibt.</span><span class="sxs-lookup"><span data-stu-id="154ab-115">This parameter contains a pointer to a **DWORD** that specifies the version of the **SIO\_TCP\_INFO** control code that you are using.</span></span> <span data-ttu-id="154ab-116">Geben Sie 0 an, um [TCP_INFO_v0](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v0)zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="154ab-116">Specify 0 to use [TCP_INFO_v0](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v0).</span></span> <span data-ttu-id="154ab-117">Geben Sie 1 an, um [TCP_INFO_v1](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v1)zu verwenden, bei dem weitere Felder angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="154ab-117">Specify 1 to use [TCP_INFO_v1](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v1), which povides more fields.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="154ab-118">cbinbuffer</span><span class="sxs-lookup"><span data-stu-id="154ab-118">cbInBuffer</span></span>

<span data-ttu-id="154ab-119">Die Größe des Eingabe Puffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="154ab-119">The size, in bytes, of the input buffer.</span></span>
<span data-ttu-id="154ab-120">Dieser Parameter sollte die Größe des **DWORD** -Datentyps sein.</span><span class="sxs-lookup"><span data-stu-id="154ab-120">This parameter should be the size of the **DWORD** data type.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="154ab-121">lpvoutbuffer</span><span class="sxs-lookup"><span data-stu-id="154ab-121">lpvOutBuffer</span></span>

<span data-ttu-id="154ab-122">Ein Zeiger auf den Ausgabepuffer.</span><span class="sxs-lookup"><span data-stu-id="154ab-122">A pointer to the output buffer.</span></span>
<span data-ttu-id="154ab-123">Bei erfolgreicher Ausgabe enthält dieser Parameter einen Zeiger auf eine [**TCP_INFO_v0**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_info_v0) -Struktur, die die TCP-Statistik für den angegebenen Socket enthält.</span><span class="sxs-lookup"><span data-stu-id="154ab-123">On successful output, this parameter contains a pointer to a [**TCP_INFO_v0**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_info_v0) structure that contains the TCP statistics for the specified socket.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="154ab-124">cboutbuffer</span><span class="sxs-lookup"><span data-stu-id="154ab-124">cbOutBuffer</span></span>

<span data-ttu-id="154ab-125">Die Größe des Ausgabepuffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="154ab-125">The size, in bytes, of the output buffer.</span></span>
<span data-ttu-id="154ab-126">Dieser Parameter muss mindestens die Größe der [**TCP_INFO_v0**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_info_v0) Struktur aufweisen.</span><span class="sxs-lookup"><span data-stu-id="154ab-126">This parameter must be at least the size of the [**TCP_INFO_v0**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_info_v0) structure.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="154ab-127">lpcbbyteszurück gegeben</span><span class="sxs-lookup"><span data-stu-id="154ab-127">lpcbBytesReturned</span></span>

<span data-ttu-id="154ab-128">Ein Zeiger auf eine Variable, die die Größe der im Ausgabepuffer gespeicherten Daten (in Bytes) empfängt.</span><span class="sxs-lookup"><span data-stu-id="154ab-128">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>

<span data-ttu-id="154ab-129">Wenn der Ausgabepuffer zu klein ist, schlägt der-Befehl fehl, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) gibt [**WSAEINVAL**](windows-sockets-error-codes-2.md)zurück, und der *lpcbbytesreturns* -Parameter verweist auf den **DWORD** -Wert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="154ab-129">If the output buffer is too small, the call fails, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns [**WSAEINVAL**](windows-sockets-error-codes-2.md), and the *lpcbBytesReturned* parameter points to a **DWORD** value of zero.</span></span>

<span data-ttu-id="154ab-130">Wenn *lpoverlgetauscht* gleich **null** ist, kann der **DWORD** -Wert, auf den der *lpcbbytesall* -Parameter verweist, der bei einem erfolgreichen-Vorgang zurückgegeben wird, nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="154ab-130">If *lpOverlapped* is **NULL**, the **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned on a successful call cannot be zero.</span></span>

<span data-ttu-id="154ab-131">Wenn der *lpoverllapp* -Parameter für überlappende Sockets nicht **null** ist, werden Vorgänge, die nicht sofort abgeschlossen werden können, initiiert, und der Abschluss wird zu einem späteren Zeitpunkt angegeben.</span><span class="sxs-lookup"><span data-stu-id="154ab-131">If the *lpOverlapped* parameter is not **NULL** for overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>
<span data-ttu-id="154ab-132">Der **DWORD** -Wert, auf den der zurückgegebene *lpcbbyteszurück gegebene* Parameter verweist, kann NULL sein, da die Größe der gespeicherten Daten erst bestimmt werden kann, wenn der überlappende Vorgang abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="154ab-132">The **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned may be zero since the size of the data stored can't be determined until the overlapped operation has completed.</span></span>
<span data-ttu-id="154ab-133">Der endgültige Abschluss Status kann abgerufen werden, wenn die geeignete Vervollständigungs Methode signalisiert wird, wenn der Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="154ab-133">The final completion status can be retrieved when the appropriate completion method is signaled when the operation has completed.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="154ab-134">lpvoverlgetauscht</span><span class="sxs-lookup"><span data-stu-id="154ab-134">lpvOverlapped</span></span>

<span data-ttu-id="154ab-135">Ein Zeiger auf eine [**wsaoverllapp**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="154ab-135">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="154ab-136">Wenn Socket *s* ohne das überlappende Attribut erstellt wurde, wird der *lpoverllapp* -Parameter ignoriert.</span><span class="sxs-lookup"><span data-stu-id="154ab-136">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="154ab-137">Wenn *s* mit dem überlappenden Attribut geöffnet wurde und der *lpoverlgetauscht* -Parameter nicht **null** ist, wird der Vorgang als überlappende (asynchrone) Operation ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="154ab-137">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="154ab-138">In diesem Fall muss der *lpoverllapp* -Parameter auf eine gültige [**wsaoverllapp**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) -Struktur zeigen.</span><span class="sxs-lookup"><span data-stu-id="154ab-138">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="154ab-139">Bei überlappenden Vorgängen gibt die Funktion [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) oder **wspioctl** sofort zurück, und die entsprechende Vervollständigungs Methode wird signalisiert, wenn der Vorgang abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="154ab-139">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="154ab-140">Andernfalls gibt die Funktion nicht zurück, bis der Vorgang abgeschlossen ist oder ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="154ab-140">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="154ab-141">lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="154ab-141">lpCompletionRoutine</span></span>

<span data-ttu-id="154ab-142">Typ: \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="154ab-142">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="154ab-143">Ein Zeiger auf die Vervollständigungs Routine, die aufgerufen wird, wenn der Vorgang abgeschlossen wurde (bei nicht überlappenden Sockets ignoriert).</span><span class="sxs-lookup"><span data-stu-id="154ab-143">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="154ab-144">lpthreadid</span><span class="sxs-lookup"><span data-stu-id="154ab-144">lpThreadId</span></span>

<span data-ttu-id="154ab-145">Ein Zeiger auf eine [**wsathreadid**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) -Struktur, die vom Anbieter in einem nachfolgenden [**wpuqueueapc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc)-Rückruf verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="154ab-145">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="154ab-146">Der Anbieter sollte die referenzierte [**wsathreadid**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) -Struktur (nicht den Zeiger auf dieselbe) speichern, bis die [**wpuqueueapc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) -Funktion zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="154ab-146">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="154ab-147">**Hinweis**  Dieser Parameter gilt nur für die **wspioctl** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="154ab-147">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="154ab-148">lperrno</span><span class="sxs-lookup"><span data-stu-id="154ab-148">lpErrno</span></span>

<span data-ttu-id="154ab-149">Ein Zeiger auf den Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="154ab-149">A pointer to the error code.</span></span>

<span data-ttu-id="154ab-150">**Hinweis**  Dieser Parameter gilt nur für die **wspioctl** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="154ab-150">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="154ab-151">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="154ab-151">Return value</span></span>

<span data-ttu-id="154ab-152">Wenn der Vorgang erfolgreich abgeschlossen wird, gibt die [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) -oder **wspioctl** -Funktion NULL zurück.</span><span class="sxs-lookup"><span data-stu-id="154ab-152">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="154ab-153">Wenn der Vorgang fehlschlägt oder aussteht, gibt die Funktion [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) oder **wspioctl** einen **\_ Socketfehler** zurück.</span><span class="sxs-lookup"><span data-stu-id="154ab-153">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="154ab-154">Um erweiterte Fehlerinformationen abzurufen, nennen Sie [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="154ab-154">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="154ab-155">Fehlercode</span><span class="sxs-lookup"><span data-stu-id="154ab-155">Error code</span></span> | <span data-ttu-id="154ab-156">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="154ab-156">Meaning</span></span> |
|------------|---------|
| <span data-ttu-id="154ab-157">**WSAEMSGSIZE**</span><span class="sxs-lookup"><span data-stu-id="154ab-157">**WSAEMSGSIZE**</span></span> | <span data-ttu-id="154ab-158">Der Zeiger auf den Eingabepuffer war **null**, oder die angegebene Größe des Eingabe Puffers war nicht richtig.</span><span class="sxs-lookup"><span data-stu-id="154ab-158">The pointer to the input buffer was **NULL**, or the specified size of the input buffer was not correct.</span></span> |
| <span data-ttu-id="154ab-159">**Wsaabval**</span><span class="sxs-lookup"><span data-stu-id="154ab-159">**WSAEINVAL**</span></span> | <span data-ttu-id="154ab-160">Ein ungültiges Argument wurde angegeben.</span><span class="sxs-lookup"><span data-stu-id="154ab-160">An invalid argument was supplied.</span></span> <span data-ttu-id="154ab-161">Dieser Fehler wird zurückgegeben, wenn der *dwIoControlCode* -Parameter kein gültiger Befehl ist oder wenn ein angegebener Eingabeparameter nicht zulässig ist oder der Befehl nicht auf den angegebenen Sockettyp anwendbar ist.</span><span class="sxs-lookup"><span data-stu-id="154ab-161">This error is returned if the *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> |

## <a name="remarks"></a><span data-ttu-id="154ab-162">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="154ab-162">Remarks</span></span>

<span data-ttu-id="154ab-163">Im Gegensatz zum Abrufen von TCP-Statistiken mit der [**getpertcpconnectionestats**](/windows/desktop/api/iphlpapi/nf-iphlpapi-getpertcpconnectionestats) -Funktion ist es für das Abrufen von TCP-Statistiken mit diesem Steuerungs Code nicht erforderlich, dass der Benutzercode die TCP-Verbindungstabelle lädt, speichert und filtert und keine erhöhten Rechte für die Verwendung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="154ab-163">Unlike retrieving TCP statistics with the [**GetPerTcpConnectionEStats**](/windows/desktop/api/iphlpapi/nf-iphlpapi-getpertcpconnectionestats) function, retrieving TCP statistics with this control code does not require the user code to load, store, and filter the TCP connection table, and does not require elevated privileges to use.</span></span>

## <a name="see-also"></a><span data-ttu-id="154ab-164">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="154ab-164">See also</span></span>

[<span data-ttu-id="154ab-165">Glühbirne</span><span class="sxs-lookup"><span data-stu-id="154ab-165">socket</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="154ab-166">**TCP_INFO_v0**</span><span class="sxs-lookup"><span data-stu-id="154ab-166">**TCP_INFO_v0**</span></span>](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_info_v0)

[<span data-ttu-id="154ab-167">**Getpertcpconnectionestats**</span><span class="sxs-lookup"><span data-stu-id="154ab-167">**GetPerTcpConnectionEStats**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-getpertcpconnectionestats)

[<span data-ttu-id="154ab-168">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="154ab-168">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[<span data-ttu-id="154ab-169">**Wsagein verlappedresult**</span><span class="sxs-lookup"><span data-stu-id="154ab-169">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="154ab-170">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="154ab-170">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="154ab-171">**Wsaoverlgetauscht**</span><span class="sxs-lookup"><span data-stu-id="154ab-171">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="154ab-172">**Wsasocketa**</span><span class="sxs-lookup"><span data-stu-id="154ab-172">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="154ab-173">**Wsasocketw**</span><span class="sxs-lookup"><span data-stu-id="154ab-173">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
