---
description: Der Steuercode Ruft eine Liste der lokalen Transport Adressen der Protokollfamilie des Sockets ab, an die die Anwendung gebunden werden kann.
ms.assetid: 6b23a019-812c-4623-941b-87928acabbd2
title: SIO_ADDRESS_LIST_QUERY Steuerungs Codes
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 7a728293afa51ceb58d61141e7184077478b787c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349585"
---
# <a name="sio_address_list_query-control-code"></a><span data-ttu-id="dab27-103">SIO_ADDRESS_LIST_QUERY Steuerungs Codes</span><span class="sxs-lookup"><span data-stu-id="dab27-103">SIO_ADDRESS_LIST_QUERY Control Code</span></span>

## <a name="description"></a><span data-ttu-id="dab27-104">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dab27-104">Description</span></span>

<span data-ttu-id="dab27-105">Der Code für die **\_ \_ \_ Abfrage** Steuerung der Stamm Liste der Stamm Verwaltungs Server erhält eine Liste lokaler Transport Adressen der Protokollfamilie des Sockets, an die die Anwendung gebunden werden kann.</span><span class="sxs-lookup"><span data-stu-id="dab27-105">The **SIO\_ADDRESS\_LIST\_QUERY** control code obtains a list of local transport addresses of the socket's protocol family to which the application can bind.</span></span>
<span data-ttu-id="dab27-106">Die Liste der Adressen variiert je nach Adressfamilie, und einige Adressen werden aus der Liste ausgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="dab27-106">The list of addresses varies based on address family and some addresses are excluded from the list.</span></span>

<span data-ttu-id="dab27-107">Um diesen Vorgang auszuführen, wenden Sie die [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) -oder **wspioctl** -Funktion mit den folgenden Parametern an.</span><span class="sxs-lookup"><span data-stu-id="dab27-107">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,            // descriptor identifying a socket
  SIO_ADDRESS_LIST_QUERY,            // dwIoControlCode
  NULL,                              // lpvInBuffer
  0,                                 // cbInBuffer
  (LPVOID) lpvOutBuffer,          // output buffer
  (DWORD) cbOutBuffer,            // size of output buffer  
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped, // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,            // descriptor identifying a socket
  SIO_ADDRESS_LIST_QUERY,            // dwIoControlCode
  NULL,                              // lpvInBuffer
  0,                                 // cbInBuffer
  (LPVOID) lpvOutBuffer,          // output buffer
  (DWORD) cbOutBuffer,            // size of output buffer  
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped, // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,   // a WSATHREADID structure
  (LPINT) lpErrno   // a pointer to the error code.
);
```

## <a name="parameters"></a><span data-ttu-id="dab27-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="dab27-108">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="dab27-109">s</span><span class="sxs-lookup"><span data-stu-id="dab27-109">s</span></span>

<span data-ttu-id="dab27-110">Ein Deskriptor, der einen Socket identifiziert.</span><span class="sxs-lookup"><span data-stu-id="dab27-110">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="dab27-111">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="dab27-111">dwIoControlCode</span></span>

<span data-ttu-id="dab27-112">Der Steuerelement Code für den Vorgang.</span><span class="sxs-lookup"><span data-stu-id="dab27-112">The control code for the operation.</span></span>
<span data-ttu-id="dab27-113">Verwenden Sie für diesen Vorgang eine-Abfrage für die- **\_ \_ \_ Abfrage** .</span><span class="sxs-lookup"><span data-stu-id="dab27-113">Use **SIO\_ADDRESS\_LIST\_QUERY** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="dab27-114">lpvinbuffer</span><span class="sxs-lookup"><span data-stu-id="dab27-114">lpvInBuffer</span></span>

<span data-ttu-id="dab27-115">Ein Zeiger auf den Eingabepuffer.</span><span class="sxs-lookup"><span data-stu-id="dab27-115">A pointer to the input buffer.</span></span>
<span data-ttu-id="dab27-116">Dieser Parameter wird für diesen Vorgang nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="dab27-116">This parameter is unused for this operation.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="dab27-117">cbinbuffer</span><span class="sxs-lookup"><span data-stu-id="dab27-117">cbInBuffer</span></span>

<span data-ttu-id="dab27-118">Die Größe des Eingabe Puffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="dab27-118">The size, in bytes, of the input buffer.</span></span>
<span data-ttu-id="dab27-119">Dieser Parameter wird für diesen Vorgang nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="dab27-119">This parameter is unused for this operation.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="dab27-120">lpvoutbuffer</span><span class="sxs-lookup"><span data-stu-id="dab27-120">lpvOutBuffer</span></span>

<span data-ttu-id="dab27-121">Ein Zeiger auf den Ausgabepuffer.</span><span class="sxs-lookup"><span data-stu-id="dab27-121">A pointer to the output buffer.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="dab27-122">cboutbuffer</span><span class="sxs-lookup"><span data-stu-id="dab27-122">cbOutBuffer</span></span>

<span data-ttu-id="dab27-123">Die Größe des Ausgabepuffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="dab27-123">The size, in bytes, of the output buffer.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="dab27-124">lpcbbyteszurück gegeben</span><span class="sxs-lookup"><span data-stu-id="dab27-124">lpcbBytesReturned</span></span>

<span data-ttu-id="dab27-125">Ein Zeiger auf eine Variable, die die Größe der im Ausgabepuffer gespeicherten Daten (in Bytes) empfängt.</span><span class="sxs-lookup"><span data-stu-id="dab27-125">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="dab27-126">lpvoverlgetauscht</span><span class="sxs-lookup"><span data-stu-id="dab27-126">lpvOverlapped</span></span>

<span data-ttu-id="dab27-127">Ein Zeiger auf eine [**wsaoverllapp**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="dab27-127">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="dab27-128">Wenn Socket *s* ohne das überlappende Attribut erstellt wurde, wird der *lpoverllapp* -Parameter ignoriert.</span><span class="sxs-lookup"><span data-stu-id="dab27-128">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="dab27-129">Wenn *s* mit dem überlappenden Attribut geöffnet wurde und der *lpoverlgetauscht* -Parameter nicht **null** ist, wird der Vorgang als überlappende (asynchrone) Operation ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dab27-129">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="dab27-130">In diesem Fall muss der *lpoverllapp* -Parameter auf eine gültige [**wsaoverllapp**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) -Struktur zeigen.</span><span class="sxs-lookup"><span data-stu-id="dab27-130">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="dab27-131">Bei überlappenden Vorgängen gibt die Funktion [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) oder **wspioctl** sofort zurück, und die entsprechende Vervollständigungs Methode wird signalisiert, wenn der Vorgang abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="dab27-131">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="dab27-132">Andernfalls gibt die Funktion nicht zurück, bis der Vorgang abgeschlossen ist oder ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="dab27-132">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="dab27-133">lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="dab27-133">lpCompletionRoutine</span></span>

<span data-ttu-id="dab27-134">Typ: \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="dab27-134">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="dab27-135">Ein Zeiger auf die Vervollständigungs Routine, die aufgerufen wird, wenn der Vorgang abgeschlossen wurde (bei nicht überlappenden Sockets ignoriert).</span><span class="sxs-lookup"><span data-stu-id="dab27-135">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="dab27-136">lpthreadid</span><span class="sxs-lookup"><span data-stu-id="dab27-136">lpThreadId</span></span>

<span data-ttu-id="dab27-137">Ein Zeiger auf eine [**wsathreadid**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) -Struktur, die vom Anbieter in einem nachfolgenden [**wpuqueueapc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc)-Rückruf verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="dab27-137">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="dab27-138">Der Anbieter sollte die referenzierte [**wsathreadid**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) -Struktur (nicht den Zeiger auf dieselbe) speichern, bis die [**wpuqueueapc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc) -Funktion zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="dab27-138">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="dab27-139">**Hinweis**  Dieser Parameter gilt nur für die **wspioctl** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="dab27-139">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="dab27-140">lperrno</span><span class="sxs-lookup"><span data-stu-id="dab27-140">lpErrno</span></span>

<span data-ttu-id="dab27-141">Ein Zeiger auf den Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="dab27-141">A pointer to the error code.</span></span>

<span data-ttu-id="dab27-142">**Hinweis**  Dieser Parameter gilt nur für die **wspioctl** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="dab27-142">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="dab27-143">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dab27-143">Return value</span></span>

<span data-ttu-id="dab27-144">Wenn der Vorgang erfolgreich abgeschlossen wird, gibt die [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) -oder **wspioctl** -Funktion NULL zurück.</span><span class="sxs-lookup"><span data-stu-id="dab27-144">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="dab27-145">Wenn der Vorgang fehlschlägt oder aussteht, gibt die Funktion [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) oder **wspioctl** einen **\_ Socketfehler** zurück.</span><span class="sxs-lookup"><span data-stu-id="dab27-145">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="dab27-146">Um erweiterte Fehlerinformationen abzurufen, nennen Sie [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="dab27-146">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="dab27-147">Fehlercode</span><span class="sxs-lookup"><span data-stu-id="dab27-147">Error code</span></span> | <span data-ttu-id="dab27-148">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="dab27-148">Meaning</span></span> |
|------------|---------|
| <span data-ttu-id="dab27-149">**ausstehende WSA-e/a \_ \_**</span><span class="sxs-lookup"><span data-stu-id="dab27-149">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="dab27-150">Ein übergebener Vorgang wurde erfolgreich initiiert, und der Abschluss wird zu einem späteren Zeitpunkt angegeben.</span><span class="sxs-lookup"><span data-stu-id="dab27-150">An overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="dab27-151">**WSA- \_ Vorgang \_ abgebrochen**</span><span class="sxs-lookup"><span data-stu-id="dab27-151">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="dab27-152">Ein über Lapp ender Vorgang wurde aufgrund der Schließung des Sockets oder der Ausführung des Befehls " **SIO \_ Flush** ioctl" abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="dab27-152">An overlapped operation was canceled due to the closure of the socket or the execution of the **SIO\_FLUSH** IOCTL command.</span></span> |
| <span data-ttu-id="dab27-153">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="dab27-153">**WSAEFAULT**</span></span> | <span data-ttu-id="dab27-154">Der *lpoverllapp* -oder *lpCompletionRoutine* -Parameter ist nicht vollständig in einem gültigen Teil des Benutzer Adressraums enthalten.</span><span class="sxs-lookup"><span data-stu-id="dab27-154">The *lpOverlapped* or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="dab27-155">**Wsaeingabe Progress**</span><span class="sxs-lookup"><span data-stu-id="dab27-155">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="dab27-156">Die-Funktion wird aufgerufen, wenn ein Rückruf ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dab27-156">The function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="dab27-157">**Wsaeingabe**</span><span class="sxs-lookup"><span data-stu-id="dab27-157">**WSAEINTR**</span></span> | <span data-ttu-id="dab27-158">Ein Blockierungs Vorgang wurde unterbrochen.</span><span class="sxs-lookup"><span data-stu-id="dab27-158">A blocking operation was interrupted.</span></span> |
| <span data-ttu-id="dab27-159">**Wsaabval**</span><span class="sxs-lookup"><span data-stu-id="dab27-159">**WSAEINVAL**</span></span> | <span data-ttu-id="dab27-160">Der *dwIoControlCode* -Parameter ist kein gültiger Befehl, oder ein angegebener Eingabeparameter ist nicht zulässig, oder der Befehl ist nicht auf den angegebenen Sockettyp anwendbar.</span><span class="sxs-lookup"><span data-stu-id="dab27-160">The *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> <span data-ttu-id="dab27-161">Dieser Fehler wird zurückgegeben, wenn der *cbinbuffer* -Parameter nicht auf **null** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="dab27-161">This error is returned if the *cbInBuffer* parameter is not set to **NULL**.</span></span> |
| <span data-ttu-id="dab27-162">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="dab27-162">**WSAENETDOWN**</span></span> | <span data-ttu-id="dab27-163">Das Netzwerk Subsystem ist fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="dab27-163">The network subsystem has failed.</span></span> |
| <span data-ttu-id="dab27-164">**WSAENOBUFS**</span><span class="sxs-lookup"><span data-stu-id="dab27-164">**WSAENOBUFS**</span></span> | <span data-ttu-id="dab27-165">Es ist kein Pufferspeicher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="dab27-165">No buffer space available.</span></span> |
| <span data-ttu-id="dab27-166">**Wsaumoproumopt**</span><span class="sxs-lookup"><span data-stu-id="dab27-166">**WSAENOPROTOOPT**</span></span> | <span data-ttu-id="dab27-167">Die Socketoption wird für das angegebene Protokoll nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dab27-167">The socket option is not supported on the specified protocol.</span></span> |
| <span data-ttu-id="dab27-168">**Wsaumotsock**</span><span class="sxs-lookup"><span data-stu-id="dab27-168">**WSAENOTSOCK**</span></span> | <span data-ttu-id="dab27-169">Der Deskriptor *s* ist kein Socket.</span><span class="sxs-lookup"><span data-stu-id="dab27-169">The descriptor *s* is not a socket.</span></span> |
| <span data-ttu-id="dab27-170">**WSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="dab27-170">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="dab27-171">Der angegebene ioctl-Befehl wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dab27-171">The specified IOCTL command is not supported.</span></span> <span data-ttu-id="dab27-172">Dieser Fehler wird zurückgegeben, wenn die Liste der " **SIO- \_ Adress \_ Liste \_** " ioctl vom Transportanbieter nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="dab27-172">This error is returned if the **SIO\_ADDRESS\_LIST\_QUERY** IOCTL is not supported by the transport provider.</span></span> |

## <a name="remarks"></a><span data-ttu-id="dab27-173">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dab27-173">Remarks</span></span>

<span data-ttu-id="dab27-174">Die Abfrage "ioctl" der Liste "-IP- **\_ Adress \_ Liste \_** " wird unter Windows 2000 und höheren Versionen des Betriebssystems unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dab27-174">The **SIO\_ADDRESS\_LIST\_QUERY** IOCTL is supported on Windows 2000 and later versions of the operating system.</span></span>

<span data-ttu-id="dab27-175">Der Code für die **\_ \_ \_ Abfrage** Steuerung der Stamm Liste der Stamm Verwaltungs Server erhält eine Liste lokaler Transport Adressen der Protokollfamilie des Sockets, an die die Anwendung gebunden werden kann.</span><span class="sxs-lookup"><span data-stu-id="dab27-175">The **SIO\_ADDRESS\_LIST\_QUERY** control code obtains a list of local transport addresses of the socket's protocol family to which the application can bind.</span></span>
<span data-ttu-id="dab27-176">Die Liste der Adressen variiert je nach Adressfamilie.</span><span class="sxs-lookup"><span data-stu-id="dab27-176">The list of addresses varies based on address family.</span></span>

<span data-ttu-id="dab27-177">Für die Gruppe "AF \_ inet6 Address" werden alle Adressen außer den folgenden zurückgegeben:</span><span class="sxs-lookup"><span data-stu-id="dab27-177">For the AF\_INET6 address family, all addresses are returned except for the following:</span></span>

* <span data-ttu-id="dab27-178">Eine beliebige IP-Adresse, bei der der Status der doppelten Adresserkennung (DAD) nicht ipdadstatepreferred ist.</span><span class="sxs-lookup"><span data-stu-id="dab27-178">Any IP address where the duplicate address detection (DAD) state is not IpDadStatePreferred.</span></span>
* <span data-ttu-id="dab27-179">Eine beliebige IP-Adresse mit einer Bereichs Ebene unterhalb von scopelevelsubnet für eine Schnittstelle, bei der der Schnittstellentyp ist, **Wenn der \_ Typ \_ Software \_ Loopback** ist.</span><span class="sxs-lookup"><span data-stu-id="dab27-179">Any IP address with a scope level lower than ScopeLevelSubnet on an interface where the interface type is **IF\_TYPE\_SOFTWARE\_LOOPBACK**.</span></span>
<span data-ttu-id="dab27-180">Dies bedeutet, dass Link-Local-Adressen (FE80: \*) und Loopback (:: 1) für Schnittstellen von, **Wenn der \_ Typ \_ Software \_ Loopback** Type ausgeschlossen ist, nicht, wenn sich diese Adressen auf einer Schnittstelle mit einem anderen Typ befinden.</span><span class="sxs-lookup"><span data-stu-id="dab27-180">This means link-local (fe80:\*) and loopback (::1) addresses on interfaces of **IF\_TYPE\_SOFTWARE\_LOOPBACK** type are excluded, but not if these addresses are on an interface with a different type.</span></span>

<span data-ttu-id="dab27-181">Für die **AF \_ inet** -Adressfamilie werden alle Adressen außer den folgenden zurückgegeben:</span><span class="sxs-lookup"><span data-stu-id="dab27-181">For the **AF\_INET** address family, all addresses are returned except for the following:</span></span>

* <span data-ttu-id="dab27-182">Eine beliebige IP-Adresse, bei der der Status der doppelten Adresserkennung (DAD) nicht ipdadstatepreferred ist.</span><span class="sxs-lookup"><span data-stu-id="dab27-182">Any IP address where the duplicate address detection (DAD) state is not IpDadStatePreferred.</span></span>
* <span data-ttu-id="dab27-183">Eine beliebige IP-Adresse an einer Schnittstelle, bei der der Schnittstellentyp lautet, **Wenn der \_ Typ \_ Software \_ Loopback** und Link lokal ist.</span><span class="sxs-lookup"><span data-stu-id="dab27-183">Any IP address on an interface where the interface type is **IF\_TYPE\_SOFTWARE\_LOOPBACK** and link is local.</span></span>
<span data-ttu-id="dab27-184">Dies bedeutet, dass Link-Local-Adressen (169,254.*) und Loopback (127.*) für Schnittstellen von, **Wenn der \_ Typ \_ Software \_ Loopback** Type ausgeschlossen wird, nicht, wenn sich diese Adressen auf einer Schnittstelle mit einem anderen Typ befinden.</span><span class="sxs-lookup"><span data-stu-id="dab27-184">This means link-local (169.254.*) and loopback (127.*) addresses on interfaces of **IF\_TYPE\_SOFTWARE\_LOOPBACK** type are excluded, but not if these addresses are on an interface with a different type.</span></span>

<span data-ttu-id="dab27-185">Weitere Informationen zum Status "Dad" finden Sie in der IP-Hilfsdokumentation zur IP [**- \_ \_ Bundesstaaten**](/windows/desktop/api/nldef/ne-nldef-nl_dad_state) -Enumeration und [**IP- \_ Adapter- \_ \_ unicastadressstruktur**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_unicast_address_lh) sowie in der MIB-Dokumentation der [**MIB \_ unicastipaddress- \_ Zeilen**](/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row) Struktur.</span><span class="sxs-lookup"><span data-stu-id="dab27-185">For more information on DAD state, see the IP Helper documentation on the [**IP\_DAD\_STATE**](/windows/desktop/api/nldef/ne-nldef-nl_dad_state) enumeration and [**IP\_ADAPTER\_UNICAST\_ADDRESS**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_unicast_address_lh) structure and the MIB documentation on the [**MIB\_UNICASTIPADDRESS\_ROW**](/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row) structure.</span></span>
<span data-ttu-id="dab27-186">Weitere Informationen zum Schnittstellentyp finden Sie in der IP-Hilfsdokumentation zur Struktur der [**IP- \_ Adapter \_ Adressen**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_addresses_xp) und der Funktion [**getadaptersadressen**](/windows/desktop/api/iphlpapi/nf-iphlpapi-getadaptersaddresses) sowie in der MIB-Dokumentation zu [**MIB_IF_ROW2**](/windows/desktop/api/netioapi/ns-netioapi-mib_if_row2) Struktur.</span><span class="sxs-lookup"><span data-stu-id="dab27-186">For more information on interface type, see the IP Helper documentation on the [**IP\_ADAPTER\_ADDRESSES**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_addresses_xp) structure and the [**GetAdaptersAddresses**](/windows/desktop/api/iphlpapi/nf-iphlpapi-getadaptersaddresses) function and the MIB documentation on [**MIB_IF_ROW2**](/windows/desktop/api/netioapi/ns-netioapi-mib_if_row2) structure.</span></span>
<span data-ttu-id="dab27-187">Weitere Informationen zur Bereichs Ebene finden Sie in der IP-Hilfsobjekt in der [**IP_ADAPTER_ADDRESSES**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_addresses_xp) -Struktur und auf der [**\_ Bereichsebene**](/windows/desktop/api/ws2def/ne-ws2def-scope_level) -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="dab27-187">For more information on the scope level, see the IP Helper documentation on the [**IP_ADAPTER_ADDRESSES**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_addresses_xp) structure and the [**SCOPE\_LEVEL**](/windows/desktop/api/ws2def/ne-ws2def-scope_level) enumeration.</span></span>

<span data-ttu-id="dab27-188">Die im Ausgabepuffer, auf den der *lpvoutbuffer* -Parameter verweist, zurückgegebene Liste hat die Form [**einer \_ socketadresslist \_**](/windows/desktop/api/ws2def/ns-ws2def-socket_address_list) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="dab27-188">The list returned in the output buffer pointed to by the *lpvOutBuffer* parameter is in the form of a [**SOCKET\_ADDRESS\_LIST**](/windows/desktop/api/ws2def/ns-ws2def-socket_address_list) structure.</span></span>

<span data-ttu-id="dab27-189">Wenn der im *lpvoutbuffer* -Parameter angegebene Ausgabepuffer nicht groß genug ist, um die Adressliste aufzunehmen, wird der **\_ Socketfehler** als Ergebnis dieser ioctl zurückgegeben, und [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) gibt [wsaefault](windows-sockets-error-codes-2.md)zurück.</span><span class="sxs-lookup"><span data-stu-id="dab27-189">If the output buffer specified in the *lpvOutBuffer* parameter is not large enough to contain the address list, **SOCKET\_ERROR** is returned as the result of this IOCTL and [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns [WSAEFAULT](windows-sockets-error-codes-2.md).</span></span>
<span data-ttu-id="dab27-190">Die erforderliche Größe (in Bytes) für den Ausgabepuffer wird in diesem Fall im *lpcbbytesall* -Parameter zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="dab27-190">The required size, in bytes, for the output buffer is returned in the *lpcbBytesReturned* parameter in this case.</span></span>
<span data-ttu-id="dab27-191">Beachten Sie, dass der Fehlercode von [wsaefault](windows-sockets-error-codes-2.md) auch zurückgegeben wird, wenn der Parameter *lpvinbuffer*, *lpvoutbuffer* oder *lpcbbytesall* nicht vollständig in einem gültigen Teil des Benutzer Adressraums enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="dab27-191">Note the [WSAEFAULT](windows-sockets-error-codes-2.md) error code is also returned if the *lpvInBuffer*, *lpvOutBuffer*, or *lpcbBytesReturned* parameter is not completely contained in a valid part of the user address space.</span></span>

<span data-ttu-id="dab27-192">Die Liste der " **SIO- \_ Adress \_ Liste \_** " wird in der Regel synchron aufgerufen, wobei der *lpvoverllapp* -Parameter auf **null** festgelegt ist, da die Liste der Adressen sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="dab27-192">The **SIO\_ADDRESS\_LIST\_QUERY** IOCTL is normally called synchronously with the *lpvOverlapped* parameter set to **NULL**, since the list of addresses is returned immediately.</span></span>

<span data-ttu-id="dab27-193">**Hinweis**  In Windows-Plug-and-Play-Umgebungen können Adressen dynamisch hinzugefügt und entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="dab27-193">**Note**  In Windows Plug-n-Play environments, addresses can be added and removed dynamically.</span></span>
<span data-ttu-id="dab27-194">Daher können Anwendungen nicht darauf basieren, dass die von der-Abfrage der- **\_ \_ \_ Abfrage Liste** zurückgegebenen Informationen persistent sind.</span><span class="sxs-lookup"><span data-stu-id="dab27-194">Therefore, applications cannot rely on the information returned by **SIO\_ADDRESS\_LIST\_QUERY** to be persistent.</span></span>
<span data-ttu-id="dab27-195">Anwendungen können sich für Adress Änderungs Benachrichtigungen über die Übersicht über die Übersicht über die Übersicht über die Übersicht über die IOCTL-Adress **\_ \_ Liste \_** registrieren, die eine Benachrichtigung über das überlappende e/a oder das **\_ \_ \_ Änderungs** Ereignis für die</span><span class="sxs-lookup"><span data-stu-id="dab27-195">Applications may register for address change notifications through the **SIO\_ADDRESS\_LIST\_CHANGE** IOCTL which provides for notification through either overlapped I/O or **FD\_ADDRESS\_LIST\_CHANGE** event.</span></span>
<span data-ttu-id="dab27-196">Die folgende Sequenz von Aktionen kann verwendet werden, um sicherzustellen, dass die Anwendung immer über aktuelle Adresslisten Informationen verfügt:</span><span class="sxs-lookup"><span data-stu-id="dab27-196">The following sequence of actions can be used to guarantee that the application always has current address list information:</span></span>

* <span data-ttu-id="dab27-197">Problem bei der Änderung der " **SIO \_ Address \_ List \_** "-ioctl</span><span class="sxs-lookup"><span data-stu-id="dab27-197">Issue the **SIO\_ADDRESS\_LIST\_CHANGE** IOCTL</span></span>
* <span data-ttu-id="dab27-198">Problem mit der Liste "die der-IOCTL- **\_ \_ \_ Abfrage** "</span><span class="sxs-lookup"><span data-stu-id="dab27-198">Issue the **SIO\_ADDRESS\_LIST\_QUERY** IOCTL</span></span>
* <span data-ttu-id="dab27-199">Immer, wenn der IOCTL-Aufruf der " **SIO- \_ Adress \_ Liste \_** " die Anwendung über eine überlappende e/a-Änderung oder durch Signalisieren eines **FD- \_ Adresslisten- \_ \_ Änderungs** Ereignisses benachrichtigt, sollte die gesamte Sequenz von Aktionen wiederholt werden.</span><span class="sxs-lookup"><span data-stu-id="dab27-199">Whenever the **SIO\_ADDRESS\_LIST\_CHANGE** IOCTL call notifies the application of an address list change (either through overlapped I/O or by signaling **FD\_ADDRESS\_LIST\_CHANGE** event), the whole sequence of actions should be repeated.</span></span>

<span data-ttu-id="dab27-200">Auf dem Microsoft Windows Software Development Kit (SDK), das für Windows Vista und höher veröffentlicht wurde, hat sich die Organisation der Header Dateien geändert, und der Code der in der *Ws2def. h* -Header Datei definierten Abfrage Steuerungs Code der **SIO- \_ Adress \_ Liste \_** ist definiert.</span><span class="sxs-lookup"><span data-stu-id="dab27-200">On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later, the organization of header files has changed and the **SIO\_ADDRESS\_LIST\_QUERY** control code is defined in the *Ws2def.h* header file.</span></span>
<span data-ttu-id="dab27-201">Beachten Sie, dass die Header Datei " *Ws2def. h* " automatisch in " *Winsock2. h*" enthalten ist und niemals direkt verwendet werden sollte.</span><span class="sxs-lookup"><span data-stu-id="dab27-201">Note that the *Ws2def.h* header file is automatically included in *Winsock2.h*, and should never be used directly.</span></span>

## <a name="see-also"></a><span data-ttu-id="dab27-202">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dab27-202">See also</span></span>

[<span data-ttu-id="dab27-203">**Getadaptersadressen**</span><span class="sxs-lookup"><span data-stu-id="dab27-203">**GetAdaptersAddresses**</span></span>](/windows/desktop/api/iphlpapi/nf-iphlpapi-getadaptersaddresses)

[<span data-ttu-id="dab27-204">**IP_ADAPTER_ADDRESSES**</span><span class="sxs-lookup"><span data-stu-id="dab27-204">**IP_ADAPTER_ADDRESSES**</span></span>](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_addresses_xp)

[<span data-ttu-id="dab27-205">**IP_ADAPTER_UNICAST_ADDRESS**</span><span class="sxs-lookup"><span data-stu-id="dab27-205">**IP_ADAPTER_UNICAST_ADDRESS**</span></span>](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_unicast_address_lh)

[<span data-ttu-id="dab27-206">**IP_DAD_STATE**</span><span class="sxs-lookup"><span data-stu-id="dab27-206">**IP_DAD_STATE**</span></span>](/windows/desktop/api/nldef/ne-nldef-nl_dad_state)

[<span data-ttu-id="dab27-207">**MIB_IF_ROW2**</span><span class="sxs-lookup"><span data-stu-id="dab27-207">**MIB_IF_ROW2**</span></span>](/windows/desktop/api/netioapi/ns-netioapi-mib_if_row2)

[<span data-ttu-id="dab27-208">**MIB_UNICASTIPADDRESS_ROW**</span><span class="sxs-lookup"><span data-stu-id="dab27-208">**MIB_UNICASTIPADDRESS_ROW**</span></span>](/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row)

[<span data-ttu-id="dab27-209">**SCOPE_LEVEL**</span><span class="sxs-lookup"><span data-stu-id="dab27-209">**SCOPE_LEVEL**</span></span>](/windows/desktop/api/ws2def/ne-ws2def-scope_level)

[<span data-ttu-id="dab27-210">**SOCKET_ADDRESS_LIST**</span><span class="sxs-lookup"><span data-stu-id="dab27-210">**SOCKET_ADDRESS_LIST**</span></span>](/windows/desktop/api/ws2def/ns-ws2def-socket_address_list)

[<span data-ttu-id="dab27-211">**Glühbirne**</span><span class="sxs-lookup"><span data-stu-id="dab27-211">**socket**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="dab27-212">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="dab27-212">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)

[<span data-ttu-id="dab27-213">**Wsagein verlappedresult**</span><span class="sxs-lookup"><span data-stu-id="dab27-213">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="dab27-214">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="dab27-214">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="dab27-215">**Wsaoverlgetauscht**</span><span class="sxs-lookup"><span data-stu-id="dab27-215">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="dab27-216">**Wsasocketa**</span><span class="sxs-lookup"><span data-stu-id="dab27-216">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="dab27-217">**Wsasocketw**</span><span class="sxs-lookup"><span data-stu-id="dab27-217">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
