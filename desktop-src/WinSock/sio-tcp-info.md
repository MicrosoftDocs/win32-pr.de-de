---
description: Der Steuerungscode ruft die TCP-Statistik (Transmission Control Protocol) für einen angegebenen Socket ab.
ms.assetid: AB5F25B6-D2D2-42D7-8189-06CAC4842C66
title: SIO_TCP_INFO-Steuerelementcode
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: f6076440f117ed287ad544c308e574454f33e2b7
ms.sourcegitcommit: 749dea42142dec076d41a8f26cb57ae8db46e848
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/24/2021
ms.locfileid: "112587801"
---
# <a name="sio_tcp_info-control-code"></a><span data-ttu-id="47c87-103">SIO_TCP_INFO-Steuerelementcode</span><span class="sxs-lookup"><span data-stu-id="47c87-103">SIO_TCP_INFO Control Code</span></span>

## <a name="description"></a><span data-ttu-id="47c87-104">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="47c87-104">Description</span></span>

<span data-ttu-id="47c87-105">Der **SIO \_ TCP \_ INFO-Steuerungscode** ruft die TCP-Statistik (Transmission Control Protocol) für einen angegebenen Socket ab.</span><span class="sxs-lookup"><span data-stu-id="47c87-105">The **SIO\_TCP\_INFO** control code retrieves the Transmission Control Protocol (TCP) statistics for a specified socket.</span></span>

<span data-ttu-id="47c87-106">Rufen Sie zum Ausführen dieses Vorgangs die [**Funktion WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) oder **WSPIoctl** mit den folgenden Parametern auf.</span><span class="sxs-lookup"><span data-stu-id="47c87-106">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

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

## <a name="parameters"></a><span data-ttu-id="47c87-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="47c87-107">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="47c87-108">s</span><span class="sxs-lookup"><span data-stu-id="47c87-108">s</span></span>

<span data-ttu-id="47c87-109">Ein Deskriptor, der einen Socket identifiziert.</span><span class="sxs-lookup"><span data-stu-id="47c87-109">A descriptor that identifies a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="47c87-110">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="47c87-110">dwIoControlCode</span></span>

<span data-ttu-id="47c87-111">Der Steuerelementcode für den Vorgang.</span><span class="sxs-lookup"><span data-stu-id="47c87-111">The control code for the operation.</span></span>
<span data-ttu-id="47c87-112">Verwenden Sie für diesen Vorgang **SIO \_ TCP \_ INFO.**</span><span class="sxs-lookup"><span data-stu-id="47c87-112">Use **SIO\_TCP\_INFO** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="47c87-113">lpvInBuffer</span><span class="sxs-lookup"><span data-stu-id="47c87-113">lpvInBuffer</span></span>

<span data-ttu-id="47c87-114">Ein Zeiger auf den Eingabepuffer.</span><span class="sxs-lookup"><span data-stu-id="47c87-114">A pointer to the input buffer.</span></span>
<span data-ttu-id="47c87-115">Dieser Parameter enthält einen Zeiger auf ein **DWORD,** das die Version des verwendeten **SIO \_ TCP \_ INFO-Steuerelementcodes** angibt.</span><span class="sxs-lookup"><span data-stu-id="47c87-115">This parameter contains a pointer to a **DWORD** that specifies the version of the **SIO\_TCP\_INFO** control code that you are using.</span></span> <span data-ttu-id="47c87-116">Geben Sie 0 an, um [TCP_INFO_v0](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v0)zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="47c87-116">Specify 0 to use [TCP_INFO_v0](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v0).</span></span> <span data-ttu-id="47c87-117">Geben Sie 1 an, um [TCP_INFO_v1](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v1)zu verwenden, der weitere Felder bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="47c87-117">Specify 1 to use [TCP_INFO_v1](/windows/win32/api/mstcpip/ns-mstcpip-tcp_info_v1), which provides more fields.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="47c87-118">cbInBuffer</span><span class="sxs-lookup"><span data-stu-id="47c87-118">cbInBuffer</span></span>

<span data-ttu-id="47c87-119">Die Größe des Eingabepuffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="47c87-119">The size, in bytes, of the input buffer.</span></span>
<span data-ttu-id="47c87-120">Dieser Parameter sollte die Größe des **DWORD-Datentyps** aufweisen.</span><span class="sxs-lookup"><span data-stu-id="47c87-120">This parameter should be the size of the **DWORD** data type.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="47c87-121">lpvOutBuffer</span><span class="sxs-lookup"><span data-stu-id="47c87-121">lpvOutBuffer</span></span>

<span data-ttu-id="47c87-122">Ein Zeiger auf den Ausgabepuffer.</span><span class="sxs-lookup"><span data-stu-id="47c87-122">A pointer to the output buffer.</span></span>
<span data-ttu-id="47c87-123">Bei erfolgreicher Ausgabe enthält dieser Parameter einen Zeiger auf eine [**TCP_INFO_v0**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_info_v0) Struktur, die die TCP-Statistiken für den angegebenen Socket enthält.</span><span class="sxs-lookup"><span data-stu-id="47c87-123">On successful output, this parameter contains a pointer to a [**TCP_INFO_v0**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_info_v0) structure that contains the TCP statistics for the specified socket.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="47c87-124">cbOutBuffer</span><span class="sxs-lookup"><span data-stu-id="47c87-124">cbOutBuffer</span></span>

<span data-ttu-id="47c87-125">Die Größe des Ausgabepuffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="47c87-125">The size, in bytes, of the output buffer.</span></span>
<span data-ttu-id="47c87-126">Dieser Parameter muss mindestens die Größe der [**TCP_INFO_v0-Struktur**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_info_v0) aufweisen.</span><span class="sxs-lookup"><span data-stu-id="47c87-126">This parameter must be at least the size of the [**TCP_INFO_v0**](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_info_v0) structure.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="47c87-127">lpcbBytesReturned</span><span class="sxs-lookup"><span data-stu-id="47c87-127">lpcbBytesReturned</span></span>

<span data-ttu-id="47c87-128">Ein Zeiger auf eine Variable, die die Größe der im Ausgabepuffer gespeicherten Daten in Bytes empfängt.</span><span class="sxs-lookup"><span data-stu-id="47c87-128">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>

<span data-ttu-id="47c87-129">Wenn der Ausgabepuffer zu klein ist, schlägt der Aufruf fehl, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) gibt [**WSAEINVAL**](windows-sockets-error-codes-2.md)zurück, und der *lpcbBytesReturned-Parameter* zeigt auf den **DWORD-Wert** 0 (null).</span><span class="sxs-lookup"><span data-stu-id="47c87-129">If the output buffer is too small, the call fails, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns [**WSAEINVAL**](windows-sockets-error-codes-2.md), and the *lpcbBytesReturned* parameter points to a **DWORD** value of zero.</span></span>

<span data-ttu-id="47c87-130">Wenn *lpOverlapped* **NULL** ist, darf der **DWORD-Wert,** auf den der *lpcbBytesReturned-Parameter* zeigt, der bei einem erfolgreichen Aufruf zurückgegeben wird, nicht 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="47c87-130">If *lpOverlapped* is **NULL**, the **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned on a successful call cannot be zero.</span></span>

<span data-ttu-id="47c87-131">Wenn der *lpOverlapped-Parameter* für überlappende Sockets nicht **NULL** ist, werden Vorgänge initiiert, die nicht sofort abgeschlossen werden können, und der Abschluss wird zu einem späteren Zeitpunkt angegeben.</span><span class="sxs-lookup"><span data-stu-id="47c87-131">If the *lpOverlapped* parameter is not **NULL** for overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>
<span data-ttu-id="47c87-132">Der **DWORD-Wert,** auf den der *lpcbBytesReturned-Parameter* zeigt, der zurückgegeben wird, kann 0 (null) sein, da die Größe der gespeicherten Daten erst bestimmt werden kann, nachdem der überlappende Vorgang abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="47c87-132">The **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned may be zero since the size of the data stored can't be determined until the overlapped operation has completed.</span></span>
<span data-ttu-id="47c87-133">Der endgültige Abschlussstatus kann abgerufen werden, wenn die entsprechende Vervollständigungsmethode signalisiert wird, wenn der Vorgang abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="47c87-133">The final completion status can be retrieved when the appropriate completion method is signaled when the operation has completed.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="47c87-134">lpvOverlapped</span><span class="sxs-lookup"><span data-stu-id="47c87-134">lpvOverlapped</span></span>

<span data-ttu-id="47c87-135">Ein Zeiger auf eine [**WSAOVERLAPPED-Struktur.**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)</span><span class="sxs-lookup"><span data-stu-id="47c87-135">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="47c87-136">Wenn *Sockets* ohne das überlappende Attribut erstellt wurden, wird der *lpOverlapped-Parameter* ignoriert.</span><span class="sxs-lookup"><span data-stu-id="47c87-136">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="47c87-137">Wenn *s* mit dem überlappende Attribut geöffnet wurde und der *lpOverlapped-Parameter* nicht **NULL** ist, wird der Vorgang als überlappender (asynchroner) Vorgang ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="47c87-137">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="47c87-138">In diesem Fall muss der *lpOverlapped-Parameter* auf eine gültige [**WSAOVERLAPPED-Struktur**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) verweisen.</span><span class="sxs-lookup"><span data-stu-id="47c87-138">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="47c87-139">Für überlappende Vorgänge gibt die [**WSAIoctl-**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) oder **WSPIoctl-Funktion** sofort zurück, und die entsprechende Vervollständigungsmethode wird signalisiert, wenn der Vorgang abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="47c87-139">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="47c87-140">Andernfalls gibt die Funktion erst dann zurück, wenn der Vorgang abgeschlossen wurde oder ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="47c87-140">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="47c87-141">lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="47c87-141">lpCompletionRoutine</span></span>

<span data-ttu-id="47c87-142">Typ: \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="47c87-142">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="47c87-143">Ein Zeiger auf die Abschlussroutine, die aufgerufen wird, wenn der Vorgang abgeschlossen wurde (wird für nicht überlappende Sockets ignoriert).</span><span class="sxs-lookup"><span data-stu-id="47c87-143">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="47c87-144">lpThreadId</span><span class="sxs-lookup"><span data-stu-id="47c87-144">lpThreadId</span></span>

<span data-ttu-id="47c87-145">Ein Zeiger auf eine [**WSATHREADID-Struktur,**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) die vom Anbieter in einem nachfolgenden Aufruf von [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc)verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="47c87-145">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="47c87-146">Der Anbieter sollte die [**referenzierte WSATHREADID-Struktur**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) (nicht den Zeiger auf denselben) speichern, bis die [**WPUQueueApc-Funktion**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="47c87-146">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="47c87-147">**Hinweis**  Dieser Parameter gilt nur für die **WSPIoctl-Funktion.**</span><span class="sxs-lookup"><span data-stu-id="47c87-147">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="47c87-148">lpErrno</span><span class="sxs-lookup"><span data-stu-id="47c87-148">lpErrno</span></span>

<span data-ttu-id="47c87-149">Ein Zeiger auf den Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="47c87-149">A pointer to the error code.</span></span>

<span data-ttu-id="47c87-150">**Hinweis**  Dieser Parameter gilt nur für die **WSPIoctl-Funktion.**</span><span class="sxs-lookup"><span data-stu-id="47c87-150">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="47c87-151">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="47c87-151">Return value</span></span>

<span data-ttu-id="47c87-152">Wenn der Vorgang erfolgreich abgeschlossen wurde, gibt die [**WSAIoctl-**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) oder **WSPIoctl-Funktion** 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="47c87-152">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="47c87-153">Wenn der Vorgang fehlschlägt oder aussteht, gibt die [**WSAIoctl-**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) oder **WSPIoctl-Funktion** **SOCKET \_ ERROR** zurück.</span><span class="sxs-lookup"><span data-stu-id="47c87-153">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="47c87-154">Um erweiterte Fehlerinformationen abzurufen, rufen [**Sie WSAGetLastError auf.**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)</span><span class="sxs-lookup"><span data-stu-id="47c87-154">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="47c87-155">Fehlercode</span><span class="sxs-lookup"><span data-stu-id="47c87-155">Error code</span></span> | <span data-ttu-id="47c87-156">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="47c87-156">Meaning</span></span> |
|------------|---------|
| <span data-ttu-id="47c87-157">**WSAEMSGSIZE**</span><span class="sxs-lookup"><span data-stu-id="47c87-157">**WSAEMSGSIZE**</span></span> | <span data-ttu-id="47c87-158">Der Zeiger auf den Eingabepuffer war **NULL,** oder die angegebene Größe des Eingabepuffers war nicht richtig.</span><span class="sxs-lookup"><span data-stu-id="47c87-158">The pointer to the input buffer was **NULL**, or the specified size of the input buffer was not correct.</span></span> |
| <span data-ttu-id="47c87-159">**WSAEINVAL**</span><span class="sxs-lookup"><span data-stu-id="47c87-159">**WSAEINVAL**</span></span> | <span data-ttu-id="47c87-160">Ein ungültiges Argument wurde angegeben.</span><span class="sxs-lookup"><span data-stu-id="47c87-160">An invalid argument was supplied.</span></span> <span data-ttu-id="47c87-161">Dieser Fehler wird zurückgegeben, wenn der *dwIoControlCode-Parameter* kein gültiger Befehl ist oder ein angegebener Eingabeparameter nicht akzeptabel ist oder der Befehl nicht auf den angegebenen Sockettyp anwendbar ist.</span><span class="sxs-lookup"><span data-stu-id="47c87-161">This error is returned if the *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> |

## <a name="remarks"></a><span data-ttu-id="47c87-162">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="47c87-162">Remarks</span></span>

<span data-ttu-id="47c87-163">Im Gegensatz zum Abrufen von TCP-Statistiken mit der [**GetPerTcpConnectionEStats-Funktion**](/windows/desktop/api/iphlpapi/nf-iphlpapi-getpertcpconnectionestats) erfordert das Abrufen von TCP-Statistiken mit diesem Steuerungscode nicht, dass der Benutzercode die TCP-Verbindungstabelle lädt, speichert und filtert, und erfordert keine erhöhten Berechtigungen für die Verwendung.</span><span class="sxs-lookup"><span data-stu-id="47c87-163">Unlike retrieving TCP statistics with the [**GetPerTcpConnectionEStats**](/windows/desktop/api/iphlpapi/nf-iphlpapi-getpertcpconnectionestats) function, retrieving TCP statistics with this control code does not require the user code to load, store, and filter the TCP connection table, and does not require elevated privileges to use.</span></span>

## <a name="see-also"></a><span data-ttu-id="47c87-164">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="47c87-164">See also</span></span>

[<span data-ttu-id="47c87-165">Socket</span><span class="sxs-lookup"><span data-stu-id="47c87-165">socket</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="47c87-166">**TCP_INFO_v0**</span><span class="sxs-lookup"><span data-stu-id="47c87-166">**TCP_INFO_v0**</span></span>](/windows/desktop/api/mstcpip/ns-mstcpip-tcp_info_v0)

[<span data-ttu-id="47c87-167">**GetPerTcpConnectionEStats**</span><span class="sxs-lookup"><span data-stu-id="47c87-167">**GetPerTcpConnectionEStats**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-getpertcpconnectionestats)

[<span data-ttu-id="47c87-168">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="47c87-168">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[<span data-ttu-id="47c87-169">**WSAGetOverlappedResult**</span><span class="sxs-lookup"><span data-stu-id="47c87-169">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="47c87-170">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="47c87-170">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="47c87-171">**WSAOVERLAPPED**</span><span class="sxs-lookup"><span data-stu-id="47c87-171">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="47c87-172">**WSASocketA**</span><span class="sxs-lookup"><span data-stu-id="47c87-172">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="47c87-173">**WSASocketW**</span><span class="sxs-lookup"><span data-stu-id="47c87-173">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
