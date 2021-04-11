---
description: Der Steuerungs Code aktiviert oder deaktiviert die Einstellung pro Verbindung der TCP-Keep-Alive-Option, die das TCP-Keep-Alive-Timeout und-Intervall angibt.
ms.assetid: c02e8ad5-bfad-489f-83bf-39b53fd68bde
title: SIO_KEEPALIVE_VALS Steuerungs Codes
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: ea8aabf452436ca2bbd6307366e7fc24f913dbdb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104131020"
---
# <a name="sio_keepalive_vals-control-code"></a><span data-ttu-id="bbaca-103">SIO_KEEPALIVE_VALS Steuerungs Codes</span><span class="sxs-lookup"><span data-stu-id="bbaca-103">SIO_KEEPALIVE_VALS Control Code</span></span>

## <a name="description"></a><span data-ttu-id="bbaca-104">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bbaca-104">Description</span></span>

<span data-ttu-id="bbaca-105">Der " **SIO \_ KeepAlive \_ Vals** -Steuerungs Code" aktiviert oder deaktiviert die Einstellung pro Verbindung der TCP-Keep-Alive-Option, die das TCP-Keep-Alive-Timeout und-Intervall angibt.</span><span class="sxs-lookup"><span data-stu-id="bbaca-105">The **SIO\_KEEPALIVE\_VALS** control code enables or disables the per-connection setting of the TCP keep-alive option which specifies the TCP keep-alive timeout and interval.</span></span>

<span data-ttu-id="bbaca-106">Um diesen Vorgang auszuführen, wenden Sie die [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) -oder **wspioctl** -Funktion mit den folgenden Parametern an.</span><span class="sxs-lookup"><span data-stu-id="bbaca-106">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,              // descriptor identifying a socket
  SIO_KEEPALIVE_VALS,                  // dwIoControlCode
  (LPVOID) lpvInBuffer,    // pointer to tcp_keepalive struct
  (DWORD) cbInBuffer,      // length of input buffer
  NULL,         // output buffer
  0,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,              // descriptor identifying a socket
  SIO_KEEPALIVE_VALS,                  // dwIoControlCode
  (LPVOID) lpvInBuffer,    // pointer to tcp_keepalive struct
  (DWORD) cbInBuffer,      // length of input buffer
  NULL,         // output buffer
  0,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,   // a WSATHREADID structure
  (LPINT) lpErrno   // a pointer to the error code.
);
```

## <a name="parameters"></a><span data-ttu-id="bbaca-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="bbaca-107">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="bbaca-108">s</span><span class="sxs-lookup"><span data-stu-id="bbaca-108">s</span></span>

<span data-ttu-id="bbaca-109">Ein Deskriptor, der einen Socket identifiziert.</span><span class="sxs-lookup"><span data-stu-id="bbaca-109">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="bbaca-110">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="bbaca-110">dwIoControlCode</span></span>

<span data-ttu-id="bbaca-111">Der Steuerelement Code für den Vorgang.</span><span class="sxs-lookup"><span data-stu-id="bbaca-111">The control code for the operation.</span></span>
<span data-ttu-id="bbaca-112">Verwenden Sie für diesen Vorgang den " **SIO \_ KeepAlive \_ Vals** ".</span><span class="sxs-lookup"><span data-stu-id="bbaca-112">Use **SIO\_KEEPALIVE\_VALS** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="bbaca-113">lpvinbuffer</span><span class="sxs-lookup"><span data-stu-id="bbaca-113">lpvInBuffer</span></span>

<span data-ttu-id="bbaca-114">Ein Zeiger auf den Eingabepuffer.</span><span class="sxs-lookup"><span data-stu-id="bbaca-114">A pointer to the input buffer.</span></span>
<span data-ttu-id="bbaca-115">Dieser Parameter sollte auf eine **TCP \_ KeepAlive** -Struktur zeigen.</span><span class="sxs-lookup"><span data-stu-id="bbaca-115">This parameter should point to a **tcp\_keepalive** structure.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="bbaca-116">cbinbuffer</span><span class="sxs-lookup"><span data-stu-id="bbaca-116">cbInBuffer</span></span>

<span data-ttu-id="bbaca-117">Die Größe des Eingabe Puffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="bbaca-117">The size, in bytes, of the input buffer.</span></span>
<span data-ttu-id="bbaca-118">Dieser Parameter muss größer oder gleich der Größe der **TCP \_ KeepAlive** -Struktur sein, auf die durch den *lpvinbuffer* -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="bbaca-118">This parameter should equal to or greater than the size of the **tcp\_keepalive** structure pointed to by the *lpvInBuffer* parameter.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="bbaca-119">lpvoutbuffer</span><span class="sxs-lookup"><span data-stu-id="bbaca-119">lpvOutBuffer</span></span>

<span data-ttu-id="bbaca-120">Ein Zeiger auf den Ausgabepuffer.</span><span class="sxs-lookup"><span data-stu-id="bbaca-120">A pointer to the output buffer.</span></span>
<span data-ttu-id="bbaca-121">Dieser Parameter wird für diesen Vorgang nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="bbaca-121">This parameter is unused for this operation.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="bbaca-122">cboutbuffer</span><span class="sxs-lookup"><span data-stu-id="bbaca-122">cbOutBuffer</span></span>

<span data-ttu-id="bbaca-123">Die Größe des Ausgabepuffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="bbaca-123">The size, in bytes, of the output buffer.</span></span>
<span data-ttu-id="bbaca-124">Dieser Parameter muss auf 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="bbaca-124">This parameter must be set to zero.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="bbaca-125">lpcbbyteszurück gegeben</span><span class="sxs-lookup"><span data-stu-id="bbaca-125">lpcbBytesReturned</span></span>

<span data-ttu-id="bbaca-126">Ein Zeiger auf eine Variable, die die Größe der im Ausgabepuffer gespeicherten Daten (in Bytes) empfängt.</span><span class="sxs-lookup"><span data-stu-id="bbaca-126">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>
<span data-ttu-id="bbaca-127">Dieser zurückgegebene Parameter verweist auf einen **DWORD** -Wert von 0 (null) für diesen Vorgang, da keine Ausgabe vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="bbaca-127">This returned parameter points to a **DWORD** value of zero for this operation, since there is no output.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="bbaca-128">lpvoverlgetauscht</span><span class="sxs-lookup"><span data-stu-id="bbaca-128">lpvOverlapped</span></span>

<span data-ttu-id="bbaca-129">Ein Zeiger auf eine [**wsaoverllapp**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="bbaca-129">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="bbaca-130">Wenn Socket *s* ohne das überlappende Attribut erstellt wurde, wird der *lpoverllapp* -Parameter ignoriert.</span><span class="sxs-lookup"><span data-stu-id="bbaca-130">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="bbaca-131">Wenn *s* mit dem überlappenden Attribut geöffnet wurde und der *lpoverlgetauscht* -Parameter nicht **null** ist, wird der Vorgang als überlappende (asynchrone) Operation ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bbaca-131">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="bbaca-132">In diesem Fall muss der *lpoverllapp* -Parameter auf eine gültige [**wsaoverllapp**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) -Struktur zeigen.</span><span class="sxs-lookup"><span data-stu-id="bbaca-132">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="bbaca-133">Bei überlappenden Vorgängen gibt die Funktion [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) oder **wspioctl** sofort zurück, und die entsprechende Vervollständigungs Methode wird signalisiert, wenn der Vorgang abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="bbaca-133">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="bbaca-134">Andernfalls gibt die Funktion nicht zurück, bis der Vorgang abgeschlossen ist oder ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="bbaca-134">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="bbaca-135">lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="bbaca-135">lpCompletionRoutine</span></span>

<span data-ttu-id="bbaca-136">Typ: \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="bbaca-136">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="bbaca-137">Ein Zeiger auf die Vervollständigungs Routine, die aufgerufen wird, wenn der Vorgang abgeschlossen wurde (bei nicht überlappenden Sockets ignoriert).</span><span class="sxs-lookup"><span data-stu-id="bbaca-137">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="bbaca-138">lpthreadid</span><span class="sxs-lookup"><span data-stu-id="bbaca-138">lpThreadId</span></span>

<span data-ttu-id="bbaca-139">Ein Zeiger auf eine [**wsathreadid**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) -Struktur, die vom Anbieter in einem nachfolgenden [**wpuqueueapc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc)-Rückruf verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="bbaca-139">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="bbaca-140">Der Anbieter sollte die referenzierte [**wsathreadid**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) -Struktur (nicht den Zeiger auf dieselbe) speichern, bis die [**wpuqueueapc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) -Funktion zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="bbaca-140">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="bbaca-141">**Hinweis**  Dieser Parameter gilt nur für die **wspioctl** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="bbaca-141">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="bbaca-142">lperrno</span><span class="sxs-lookup"><span data-stu-id="bbaca-142">lpErrno</span></span>

<span data-ttu-id="bbaca-143">Ein Zeiger auf den Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="bbaca-143">A pointer to the error code.</span></span>

<span data-ttu-id="bbaca-144">**Hinweis**  Dieser Parameter gilt nur für die **wspioctl** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="bbaca-144">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="bbaca-145">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bbaca-145">Return value</span></span>

<span data-ttu-id="bbaca-146">Wenn der Vorgang erfolgreich abgeschlossen wird, gibt die [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) -oder **wspioctl** -Funktion NULL zurück.</span><span class="sxs-lookup"><span data-stu-id="bbaca-146">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="bbaca-147">Wenn der Vorgang fehlschlägt oder aussteht, gibt die Funktion [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) oder **wspioctl** einen **\_ Socketfehler** zurück.</span><span class="sxs-lookup"><span data-stu-id="bbaca-147">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="bbaca-148">Um erweiterte Fehlerinformationen abzurufen, nennen Sie [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="bbaca-148">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="bbaca-149">Fehlercode</span><span class="sxs-lookup"><span data-stu-id="bbaca-149">Error code</span></span> | <span data-ttu-id="bbaca-150">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="bbaca-150">Meaning</span></span> |
|------------|---------|
|<span data-ttu-id="bbaca-151">**ausstehende WSA-e/a \_ \_**</span><span class="sxs-lookup"><span data-stu-id="bbaca-151">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="bbaca-152">Ein übergebener Vorgang wurde erfolgreich initiiert, und der Abschluss wird zu einem späteren Zeitpunkt angegeben.</span><span class="sxs-lookup"><span data-stu-id="bbaca-152">An overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="bbaca-153">**WSA- \_ Vorgang \_ abgebrochen**</span><span class="sxs-lookup"><span data-stu-id="bbaca-153">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="bbaca-154">Ein über Lapp ender Vorgang wurde aufgrund der Schließung des Sockets oder der Ausführung des **SIO_FLUSH ioctl** -Befehls abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="bbaca-154">An overlapped operation was canceled due to the closure of the socket or the execution of the **SIO_FLUSH IOCTL** command.</span></span> |
| <span data-ttu-id="bbaca-155">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="bbaca-155">**WSAEFAULT**</span></span> | <span data-ttu-id="bbaca-156">Der *lpoverllapp* -oder *lpCompletionRoutine* -Parameter ist nicht vollständig in einem gültigen Teil des Benutzer Adressraums enthalten.</span><span class="sxs-lookup"><span data-stu-id="bbaca-156">The *lpOverlapped* or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="bbaca-157">**Wsaeingabe Progress**</span><span class="sxs-lookup"><span data-stu-id="bbaca-157">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="bbaca-158">Die-Funktion wird aufgerufen, wenn ein Rückruf ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bbaca-158">The function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="bbaca-159">**Wsaeingabe**</span><span class="sxs-lookup"><span data-stu-id="bbaca-159">**WSAEINTR**</span></span> | <span data-ttu-id="bbaca-160">Ein Blockierungs Vorgang wurde unterbrochen.</span><span class="sxs-lookup"><span data-stu-id="bbaca-160">A blocking operation was interrupted.</span></span> |
| <span data-ttu-id="bbaca-161">**Wsaabval**</span><span class="sxs-lookup"><span data-stu-id="bbaca-161">**WSAEINVAL**</span></span> | <span data-ttu-id="bbaca-162">Der *dwIoControlCode* -Parameter ist kein gültiger Befehl, oder ein angegebener Eingabeparameter ist nicht zulässig, oder der Befehl ist nicht auf den angegebenen Sockettyp anwendbar.</span><span class="sxs-lookup"><span data-stu-id="bbaca-162">The *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> |
| <span data-ttu-id="bbaca-163">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="bbaca-163">**WSAENETDOWN**</span></span> | <span data-ttu-id="bbaca-164">Das Netzwerk Subsystem ist fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="bbaca-164">The network subsystem has failed.</span></span> |
| <span data-ttu-id="bbaca-165">**Wsaumoproumopt**</span><span class="sxs-lookup"><span data-stu-id="bbaca-165">**WSAENOPROTOOPT**</span></span> | <span data-ttu-id="bbaca-166">Die Socketoption wird für das angegebene Protokoll nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bbaca-166">The socket option is not supported on the specified protocol.</span></span> <span data-ttu-id="bbaca-167">Dieser Fehler wird für einen Datagramm-Socket zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="bbaca-167">This error is returned for a datagram socket.</span></span> |
| <span data-ttu-id="bbaca-168">**Wsaumotsock**</span><span class="sxs-lookup"><span data-stu-id="bbaca-168">**WSAENOTSOCK**</span></span> | <span data-ttu-id="bbaca-169">Der Deskriptor s ist kein Socket.</span><span class="sxs-lookup"><span data-stu-id="bbaca-169">The descriptor s is not a socket.</span></span> |
| <span data-ttu-id="bbaca-170">**WSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="bbaca-170">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="bbaca-171">Der angegebene ioctl-Befehl wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bbaca-171">The specified IOCTL command is not supported.</span></span> <span data-ttu-id="bbaca-172">Dieser Fehler wird zurückgegeben, wenn der " **SIO \_ KeepAlive \_ Vals** ioctl" vom Transportanbieter nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="bbaca-172">This error is returned if the **SIO\_KEEPALIVE\_VALS** IOCTL is not supported by the transport provider.</span></span> |

## <a name="remarks"></a><span data-ttu-id="bbaca-173">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bbaca-173">Remarks</span></span>

<span data-ttu-id="bbaca-174">Der " **SIO \_ KeepAlive \_ Vals** ioctl" wird unter Windows 2000 und höheren Versionen des Betriebssystems unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bbaca-174">The **SIO\_KEEPALIVE\_VALS** IOCTL is supported on Windows 2000 and later versions of the operating system.</span></span>

<span data-ttu-id="bbaca-175">Der " **SIO \_ KeepAlive \_ Vals** "-Steuerungs Code aktiviert oder deaktiviert die Einstellung pro Verbindung der TCP-Keep-Alive-Option, die das TCP-Keep-Alive-Timeout und das für TCP-Keep-Alive-Pakete verwendete Intervall angibt.</span><span class="sxs-lookup"><span data-stu-id="bbaca-175">The **SIO\_KEEPALIVE\_VALS** control code enables or disables the per-connection setting of the TCP keep-alive option which specifies the TCP keep-alive timeout and interval used for TCP keep-alive packets.</span></span>
<span data-ttu-id="bbaca-176">Weitere Informationen zur Keep-Alive-Option finden Sie im Abschnitt 4.2.3.6 zu den Anforderungen für Internet Hosts – in RFC 1122 angegebene Kommunikations Schichten auf der [IETF-Website](https://www.ietf.org/rfc/rfc1122.txt).</span><span class="sxs-lookup"><span data-stu-id="bbaca-176">For more information on the keep-alive option, see section 4.2.3.6 on the Requirements for Internet Hosts—Communication Layers specified in RFC 1122 available at the [IETF website](https://www.ietf.org/rfc/rfc1122.txt).</span></span>
<span data-ttu-id="bbaca-177">(Diese Ressource ist möglicherweise nur in englischer Sprache verfügbar.)</span><span class="sxs-lookup"><span data-stu-id="bbaca-177">(This resource may only be available in English.)</span></span>

<span data-ttu-id="bbaca-178">Der *lpvinbuffer* -Parameter sollte auf eine **TCP- \_ KeepAlive** -Struktur verweisen, die in der Header Datei " *MSTCPIP. h* " definiert ist.</span><span class="sxs-lookup"><span data-stu-id="bbaca-178">The *lpvInBuffer* parameter should point to a **tcp\_keepalive** structure defined in the *Mstcpip.h* header file.</span></span>
<span data-ttu-id="bbaca-179">Diese Struktur ist wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="bbaca-179">This structure is defined as follows:</span></span>

```cpp
/* Argument structure for SIO_KEEPALIVE_VALS */
struct tcp_keepalive {
    u_long  onoff;
    u_long  keepalivetime;
    u_long  keepaliveinterval;
};
```

<span data-ttu-id="bbaca-180">Der im **ToggleMicrophoneOnOff** -Member angegebene Wert bestimmt, ob TCP Keep-Alive aktiviert oder deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="bbaca-180">The value specified in the **onoff** member determines if TCP keep-alive is enabled or disabled.</span></span>
<span data-ttu-id="bbaca-181">Wenn der **ToggleMicrophoneOnOff** -Member auf einen Wert ungleich 0 (null) festgelegt ist, wird TCP Keep-Alive aktiviert, und die anderen Elemente in der Struktur werden verwendet.</span><span class="sxs-lookup"><span data-stu-id="bbaca-181">If the **onoff** member is set to a nonzero value, TCP keep-alive is enabled and the other members in the structure are used.</span></span>
<span data-ttu-id="bbaca-182">Der **"KeepAliveTime"** -Member gibt das Timeout (in Millisekunden) ohne Aktivität an, bis das erste Keep-Alive-Paket gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="bbaca-182">The **keepalivetime** member specifies the timeout, in milliseconds, with no activity until the first keep-alive packet is sent.</span></span>
<span data-ttu-id="bbaca-183">Der **"KeepAliveInterval"** -Member gibt das Intervall (in Millisekunden) zwischen dem Senden von Keep-Alive-Paketen an, wenn keine Bestätigung empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="bbaca-183">The **keepaliveinterval** member specifies the interval, in milliseconds, between when successive keep-alive packets are sent if no acknowledgement is received.</span></span>

<span data-ttu-id="bbaca-184">Die Option [**SO_KEEPALIVE**](/windows/desktop/winsock/so-keepalive) , die eine der [**SOL_SOCKET Socketoptionen**](/windows/desktop/winsock/sol-socket-socket-options)ist, kann auch verwendet werden, um den TCP-Keep-Alive-Vorgang für eine Verbindung zu aktivieren oder zu deaktivieren und den aktuellen Status dieser Option abzufragen.</span><span class="sxs-lookup"><span data-stu-id="bbaca-184">The [**SO_KEEPALIVE**](/windows/desktop/winsock/so-keepalive) option, which is one of the [**SOL_SOCKET Socket Options**](/windows/desktop/winsock/sol-socket-socket-options), can also be used to enable or disable the TCP keep-alive on a connection, as well as query the current state of this option.</span></span>
<span data-ttu-id="bbaca-185">Um abzufragen, ob TCP Keep-Alive für einen Socket aktiviert ist, kann die getsockopt-Funktion mit der [**SO_KEEPALIVE**](/windows/desktop/winsock/so-keepalive) -Option aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="bbaca-185">To query whether TCP keep-alive is enabled on a socket, the getsockopt function can be called with the [**SO_KEEPALIVE**](/windows/desktop/winsock/so-keepalive) option.</span></span>
<span data-ttu-id="bbaca-186">Um TCP Keep-Alive zu aktivieren oder zu deaktivieren, kann die Funktion **setsockopt** mit der Option [**SO_KEEPALIVE**](/windows/desktop/winsock/so-keepalive) aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="bbaca-186">To enable or disable TCP keep-alive, the **setsockopt** function can be called with the [**SO_KEEPALIVE**](/windows/desktop/winsock/so-keepalive) option.</span></span>
<span data-ttu-id="bbaca-187">Wenn TCP Keep-Alive mit [**SO_KEEPALIVE**](/windows/desktop/winsock/so-keepalive)aktiviert ist, werden die standardmäßigen TCP-Einstellungen für Keep-Alive-Timeout und-Intervall verwendet, es sei denn, diese Werte wurden mithilfe von " **SIO \_ KeepAlive \_ Vals**" geändert.</span><span class="sxs-lookup"><span data-stu-id="bbaca-187">If TCP keep-alive is enabled with [**SO_KEEPALIVE**](/windows/desktop/winsock/so-keepalive), then the default TCP settings are used for keep-alive timeout and interval unless these values have been changed using **SIO\_KEEPALIVE\_VALS**.</span></span>

<span data-ttu-id="bbaca-188">Der standardmäßige systemweite Wert des Keep-Alive-Timeouts ist über die [**KeepAliveTime**](/previous-versions/windows/it-pro/windows-server-2003/cc782936(v=ws.10)) -Registrierungs Einstellung steuerbar, die einen Wert in Millisekunden annimmt.</span><span class="sxs-lookup"><span data-stu-id="bbaca-188">The default system-wide value of the keep-alive timeout is controllable through the [**KeepAliveTime**](/previous-versions/windows/it-pro/windows-server-2003/cc782936(v=ws.10)) registry setting which takes a value in milliseconds.</span></span> <span data-ttu-id="bbaca-189">Wenn der Schlüssel nicht festgelegt ist, beträgt der Standardwert für Keep-Alive-Timeout 2 Stunden.</span><span class="sxs-lookup"><span data-stu-id="bbaca-189">If the key is not set, the default keep-alive timeout is 2 hours.</span></span>
<span data-ttu-id="bbaca-190">Der standardmäßige systemweite Wert des Keep-Alive-Intervalls kann durch die [**keepAliveInterval**](/previous-versions/windows/it-pro/windows-server-2003/cc758083(v=ws.10)) -Registrierungs Einstellung gesteuert werden, die einen Wert in Millisekunden annimmt.</span><span class="sxs-lookup"><span data-stu-id="bbaca-190">The default system-wide value of the keep-alive interval is controllable through the [**KeepAliveInterval**](/previous-versions/windows/it-pro/windows-server-2003/cc758083(v=ws.10)) registry setting which takes a value in milliseconds.</span></span> <span data-ttu-id="bbaca-191">Wenn der Schlüssel nicht festgelegt ist, beträgt das standardmäßige Keep-Alive-Intervall 1 Sekunde.</span><span class="sxs-lookup"><span data-stu-id="bbaca-191">If the key is not set, the default keep-alive interval is 1 second.</span></span>

<span data-ttu-id="bbaca-192">Unter Windows Vista und höher wird die Anzahl von Keep-Alive-Tests (Neuübertragungen von Daten) auf 10 festgelegt und kann nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="bbaca-192">On Windows Vista and later, the number of keep-alive probes (data retransmissions) is set to 10 and cannot be changed.</span></span>

<span data-ttu-id="bbaca-193">Unter Windows Server 2003, Windows XP und Windows 2000 ist die Standardeinstellung für die Anzahl von Keep-Alive-Tests 5.</span><span class="sxs-lookup"><span data-stu-id="bbaca-193">On Windows Server 2003, Windows XP, and Windows 2000, the default setting for number of keep-alive probes is 5.</span></span>
<span data-ttu-id="bbaca-194">Die Anzahl der Keep-Alive-Tests ist über die Registrierungs Einstellungen **TcpMaxDataRetransmissions** und [**pptptcpmaxdataretransmissions**](/previous-versions/windows/it-pro/windows-server-2003/cc775408(v=ws.10)) steuerbar.</span><span class="sxs-lookup"><span data-stu-id="bbaca-194">The number of keep-alive probes is controllable through the **TcpMaxDataRetransmissions** and [**PPTPTcpMaxDataRetransmissions**](/previous-versions/windows/it-pro/windows-server-2003/cc775408(v=ws.10)) registry settings.</span></span>
<span data-ttu-id="bbaca-195">Die Anzahl der Keep-Alive-Tests wird auf den größeren der beiden Registrierungsschlüssel Werte festgelegt.</span><span class="sxs-lookup"><span data-stu-id="bbaca-195">The number of keep-alive probes is set to the larger of the two registry key values.</span></span>
<span data-ttu-id="bbaca-196">Wenn diese Zahl 0 ist, werden Keep-Alive-Tests nicht gesendet.</span><span class="sxs-lookup"><span data-stu-id="bbaca-196">If this number is 0, then keep-alive probes will not be sent.</span></span>
<span data-ttu-id="bbaca-197">Wenn diese Zahl über 255 liegt, wird Sie an 255 angepasst.</span><span class="sxs-lookup"><span data-stu-id="bbaca-197">If this number is above 255, then it is adjusted to 255.</span></span>

## <a name="see-also"></a><span data-ttu-id="bbaca-198">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bbaca-198">See also</span></span>

<span data-ttu-id="bbaca-199">[**KeepAliveTime**](/previous-versions/windows/it-pro/windows-server-2003/cc782936(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="bbaca-199">[**KeepAliveTime**](/previous-versions/windows/it-pro/windows-server-2003/cc782936(v=ws.10))</span></span>

<span data-ttu-id="bbaca-200">[**KeepAliveInterval**](/previous-versions/windows/it-pro/windows-server-2003/cc758083(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="bbaca-200">[**KeepAliveInterval**](/previous-versions/windows/it-pro/windows-server-2003/cc758083(v=ws.10))</span></span>

<span data-ttu-id="bbaca-201">[**Pptptcpmaxdataretransmissions**](/previous-versions/windows/it-pro/windows-server-2003/cc775408(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="bbaca-201">[**PPTPTcpMaxDataRetransmissions**](/previous-versions/windows/it-pro/windows-server-2003/cc775408(v=ws.10))</span></span>

[<span data-ttu-id="bbaca-202">Glühbirne</span><span class="sxs-lookup"><span data-stu-id="bbaca-202">socket</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="bbaca-203">**SO_KEEPALIVE**</span><span class="sxs-lookup"><span data-stu-id="bbaca-203">**SO_KEEPALIVE**</span></span>](/windows/desktop/winsock/so-keepalive)

[<span data-ttu-id="bbaca-204">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="bbaca-204">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[<span data-ttu-id="bbaca-205">**Wsagein verlappedresult**</span><span class="sxs-lookup"><span data-stu-id="bbaca-205">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="bbaca-206">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="bbaca-206">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="bbaca-207">**Wsaoverlgetauscht**</span><span class="sxs-lookup"><span data-stu-id="bbaca-207">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="bbaca-208">**Wsasocketa**</span><span class="sxs-lookup"><span data-stu-id="bbaca-208">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="bbaca-209">**Wsasocketw**</span><span class="sxs-lookup"><span data-stu-id="bbaca-209">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
