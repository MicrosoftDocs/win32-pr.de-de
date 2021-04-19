---
description: Der Steuerungs Code Ruft den Umleitungs Daten Satz für die akzeptierte TCP/IP-Verbindung für die Verwendung durch einen Windows-Filter Plattform-Umleitungs Dienst ab.
ms.assetid: E0D7CC1A-8F93-45A0-9543-3F2ACAF352F5
title: SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS Steuerungs Codes
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 2389914d29bd403a33e23065c29f549a01adbb67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347895"
---
# <a name="sio_query_wfp_connection_redirect_records-control-code"></a><span data-ttu-id="795da-103">SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS Steuerungs Codes</span><span class="sxs-lookup"><span data-stu-id="795da-103">SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS Control Code</span></span>

## <a name="description"></a><span data-ttu-id="795da-104">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="795da-104">Description</span></span>

<span data-ttu-id="795da-105">Der Verwaltungs Code für die **\_ \_ WFP- \_ \_ verbindungsumleitungs- \_ Datensätze** der zentrale Abfrage ruft den Umleitungs Daten Satz für die akzeptierte TCP/IP-Verbindung für die Verwendung durch einen WFP-Umleitungs Dienst (Windows Filtering Platform</span><span class="sxs-lookup"><span data-stu-id="795da-105">The **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_RECORDS** control code retrieves the redirect record for the accepted TCP/IP connection for use by a Windows Filtering Platform (WFP) redirect service.</span></span>

<span data-ttu-id="795da-106">Um diesen Vorgang auszuführen, wenden Sie die [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) -oder **wspioctl** -Funktion mit den folgenden Parametern an.</span><span class="sxs-lookup"><span data-stu-id="795da-106">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS, // dwIoControlCode
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
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS, // dwIoControlCode
  NULL,                         // lpvInBuffer
  0,                            // cbInBuffer
  (LPVOID) lpvOutBuffer,         // output buffer
  (DWORD) cbOutBuffer,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

## <a name="parameters"></a><span data-ttu-id="795da-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="795da-107">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="795da-108">s</span><span class="sxs-lookup"><span data-stu-id="795da-108">s</span></span>

<span data-ttu-id="795da-109">Ein Deskriptor, der einen Socket identifiziert.</span><span class="sxs-lookup"><span data-stu-id="795da-109">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="795da-110">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="795da-110">dwIoControlCode</span></span>

<span data-ttu-id="795da-111">Der Steuerelement Code für den Vorgang.</span><span class="sxs-lookup"><span data-stu-id="795da-111">The control code for the operation.</span></span>
<span data-ttu-id="795da-112">Verwenden Sie für diesen Vorgang die **\_ \_ WFP- \_ Verbindungs \_ \_ Einträge für die WFP-Abfrage** .</span><span class="sxs-lookup"><span data-stu-id="795da-112">Use **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_RECORDS** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="795da-113">lpvinbuffer</span><span class="sxs-lookup"><span data-stu-id="795da-113">lpvInBuffer</span></span>

<span data-ttu-id="795da-114">Ein Zeiger auf den Eingabepuffer.</span><span class="sxs-lookup"><span data-stu-id="795da-114">A pointer to the input buffer.</span></span>
<span data-ttu-id="795da-115">Dieser Parameter wird für diesen Vorgang nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="795da-115">This parameter is unused for this operation.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="795da-116">cbinbuffer</span><span class="sxs-lookup"><span data-stu-id="795da-116">cbInBuffer</span></span>

<span data-ttu-id="795da-117">Die Größe des Eingabe Puffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="795da-117">The size, in bytes, of the input buffer.</span></span>
<span data-ttu-id="795da-118">Dieser Parameter wird für diesen Vorgang nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="795da-118">This parameter is unused for this operation.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="795da-119">lpvoutbuffer</span><span class="sxs-lookup"><span data-stu-id="795da-119">lpvOutBuffer</span></span>

<span data-ttu-id="795da-120">Ein Zeiger auf den Ausgabepuffer.</span><span class="sxs-lookup"><span data-stu-id="795da-120">A pointer to the output buffer.</span></span>
<span data-ttu-id="795da-121">Dieser Parameter sollte auf einen **ulong** -Datentyp zeigen, wenn die Parameter *lpoverlgetauscht* und *lpCompletionRoutine* **null** sind.</span><span class="sxs-lookup"><span data-stu-id="795da-121">This parameter should point to a **ULONG** data type if the *lpOverlapped* and *lpCompletionRoutine* parameters are **NULL**.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="795da-122">cboutbuffer</span><span class="sxs-lookup"><span data-stu-id="795da-122">cbOutBuffer</span></span>

<span data-ttu-id="795da-123">Die Größe des Ausgabepuffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="795da-123">The size, in bytes, of the output buffer.</span></span>
<span data-ttu-id="795da-124">Dieser Parameter muss mindestens die Größe eines **ulong** -Datentyps aufweisen.</span><span class="sxs-lookup"><span data-stu-id="795da-124">This parameter must be at least the size of a **ULONG** data type.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="795da-125">lpcbbyteszurück gegeben</span><span class="sxs-lookup"><span data-stu-id="795da-125">lpcbBytesReturned</span></span>

<span data-ttu-id="795da-126">Ein Zeiger auf eine Variable, die die Größe der im Ausgabepuffer gespeicherten Daten (in Bytes) empfängt.</span><span class="sxs-lookup"><span data-stu-id="795da-126">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>

<span data-ttu-id="795da-127">Wenn der Ausgabepuffer zu klein ist, schlägt der-Befehl fehl, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) gibt [**WSAEINVAL**](windows-sockets-error-codes-2.md)zurück, und der *lpcbbytesreturns* -Parameter verweist auf den **DWORD** -Wert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="795da-127">If the output buffer is too small, the call fails, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns [**WSAEINVAL**](windows-sockets-error-codes-2.md), and the *lpcbBytesReturned* parameter points to a **DWORD** value of zero.</span></span>

<span data-ttu-id="795da-128">Wenn *lpoverlgetauscht* gleich **null** ist, kann der **DWORD** -Wert, auf den der *lpcbbytesall* -Parameter verweist, der bei einem erfolgreichen-Vorgang zurückgegeben wird, nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="795da-128">If *lpOverlapped* is **NULL**, the **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned on a successful call cannot be zero.</span></span>

<span data-ttu-id="795da-129">Wenn der *lpoverllapp* -Parameter für überlappende Sockets nicht **null** ist, werden Vorgänge, die nicht sofort abgeschlossen werden können, initiiert, und der Abschluss wird zu einem späteren Zeitpunkt angegeben.</span><span class="sxs-lookup"><span data-stu-id="795da-129">If the *lpOverlapped* parameter is not **NULL** for overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>
<span data-ttu-id="795da-130">Der **DWORD** -Wert, auf den der zurückgegebene *lpcbbyteszurück gegebene* Parameter verweist, kann NULL sein, da die Größe der gespeicherten Daten erst bestimmt werden kann, wenn der überlappende Vorgang abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="795da-130">The **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned may be zero since the size of the data stored can't be determined until the overlapped operation has completed.</span></span>
<span data-ttu-id="795da-131">Der endgültige Abschluss Status kann abgerufen werden, wenn die geeignete Vervollständigungs Methode signalisiert wird, wenn der Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="795da-131">The final completion status can be retrieved when the appropriate completion method is signaled when the operation has completed.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="795da-132">lpvoverlgetauscht</span><span class="sxs-lookup"><span data-stu-id="795da-132">lpvOverlapped</span></span>

<span data-ttu-id="795da-133">Ein Zeiger auf eine [**wsaoverllapp**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="795da-133">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="795da-134">Wenn Socket *s* ohne das überlappende Attribut erstellt wurde, wird der *lpoverllapp* -Parameter ignoriert.</span><span class="sxs-lookup"><span data-stu-id="795da-134">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="795da-135">Wenn *s* mit dem überlappenden Attribut geöffnet wurde und der *lpoverlgetauscht* -Parameter nicht **null** ist, wird der Vorgang als überlappende (asynchrone) Operation ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="795da-135">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="795da-136">In diesem Fall muss der *lpoverllapp* -Parameter auf eine gültige [**wsaoverllapp**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) -Struktur zeigen.</span><span class="sxs-lookup"><span data-stu-id="795da-136">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="795da-137">Bei überlappenden Vorgängen gibt die Funktion [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) oder **wspioctl** sofort zurück, und die entsprechende Vervollständigungs Methode wird signalisiert, wenn der Vorgang abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="795da-137">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="795da-138">Andernfalls gibt die Funktion nicht zurück, bis der Vorgang abgeschlossen ist oder ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="795da-138">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="795da-139">lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="795da-139">lpCompletionRoutine</span></span>

<span data-ttu-id="795da-140">Typ: \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="795da-140">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="795da-141">Ein Zeiger auf die Vervollständigungs Routine, die aufgerufen wird, wenn der Vorgang abgeschlossen wurde (bei nicht überlappenden Sockets ignoriert).</span><span class="sxs-lookup"><span data-stu-id="795da-141">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="795da-142">lpthreadid</span><span class="sxs-lookup"><span data-stu-id="795da-142">lpThreadId</span></span>

<span data-ttu-id="795da-143">Ein Zeiger auf eine [**wsathreadid**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) -Struktur, die vom Anbieter in einem nachfolgenden [**wpuqueueapc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc)-Rückruf verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="795da-143">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="795da-144">Der Anbieter sollte die referenzierte [**wsathreadid**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) -Struktur (nicht den Zeiger auf dieselbe) speichern, bis die [**wpuqueueapc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) -Funktion zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="795da-144">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="795da-145">**Hinweis**  Dieser Parameter gilt nur für die **wspioctl** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="795da-145">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="795da-146">lperrno</span><span class="sxs-lookup"><span data-stu-id="795da-146">lpErrno</span></span>

<span data-ttu-id="795da-147">Ein Zeiger auf den Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="795da-147">A pointer to the error code.</span></span>

<span data-ttu-id="795da-148">**Hinweis**  Dieser Parameter gilt nur für die **wspioctl** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="795da-148">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="795da-149">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="795da-149">Return value</span></span>

<span data-ttu-id="795da-150">Wenn der Vorgang erfolgreich abgeschlossen wird, gibt die [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) -oder **wspioctl** -Funktion NULL zurück.</span><span class="sxs-lookup"><span data-stu-id="795da-150">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="795da-151">Wenn der Vorgang fehlschlägt oder aussteht, gibt die Funktion [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) oder **wspioctl** einen **\_ Socketfehler** zurück.</span><span class="sxs-lookup"><span data-stu-id="795da-151">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="795da-152">Um erweiterte Fehlerinformationen abzurufen, nennen Sie [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="795da-152">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="795da-153">Fehlercode</span><span class="sxs-lookup"><span data-stu-id="795da-153">Error code</span></span> | <span data-ttu-id="795da-154">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="795da-154">Meaning</span></span> |
|------------|---------|
| <span data-ttu-id="795da-155">**Fehler \_ beim \_ Puffer.**</span><span class="sxs-lookup"><span data-stu-id="795da-155">**ERROR\_INSUFFICIENT\_BUFFER**</span></span> | <span data-ttu-id="795da-156">Der an einen System Rückruf über gegebene Datenbereich ist zu klein.</span><span class="sxs-lookup"><span data-stu-id="795da-156">The data area passed to a system call is too small.</span></span> <span data-ttu-id="795da-157">Dieser Fehler wird zurückgegeben, wenn der Puffer, auf den der *lpvoutbuffer* -Parameter verweist, eine Puffergröße hat, die im *cboutbuffer* -Parameter übergeben wurde, zu klein ist.</span><span class="sxs-lookup"><span data-stu-id="795da-157">This error is returned if the buffer pointed to by the *lpvOutBuffer* parameter with a buffer size passed in the *cbOutBuffer* parameter is too small.</span></span> <span data-ttu-id="795da-158">Die erforderliche Puffergröße wird im Parameter " *lpcbbytes}* " zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="795da-158">The buffer size required will be returned in the *lpcbBytesReturned* parameter.</span></span> |
| <span data-ttu-id="795da-159">**WSA_IO_PENDING**</span><span class="sxs-lookup"><span data-stu-id="795da-159">**WSA_IO_PENDING**</span></span> | <span data-ttu-id="795da-160">Ein übergebener Vorgang wurde erfolgreich initiiert, und der Abschluss wird zu einem späteren Zeitpunkt angegeben.</span><span class="sxs-lookup"><span data-stu-id="795da-160">An overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="795da-161">**WSA_OPERATION_ABORTED**</span><span class="sxs-lookup"><span data-stu-id="795da-161">**WSA_OPERATION_ABORTED**</span></span> | <span data-ttu-id="795da-162">Ein über Lapp ender Vorgang wurde aufgrund der Schließung des Sockets oder der Ausführung des **SIO_FLUSH** ioctl-Befehls abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="795da-162">An overlapped operation was canceled due to the closure of the socket or the execution of the **SIO_FLUSH** IOCTL command.</span></span> |
| <span data-ttu-id="795da-163">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="795da-163">**WSAEFAULT**</span></span> | <span data-ttu-id="795da-164">Der Parameter " *lpvoutbuffer*", " *lpcbbytesis*", " *lpoverlgetauscht*" oder " *lpCompletionRoutine* " ist nicht vollständig in einem gültigen Teil des Benutzer Adressraums enthalten.</span><span class="sxs-lookup"><span data-stu-id="795da-164">The *lpvOutBuffer*, *lpcbBytesReturned*, *lpOverlapped*, or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="795da-165">**Wsaeingabe Progress**</span><span class="sxs-lookup"><span data-stu-id="795da-165">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="795da-166">Die-Funktion wird aufgerufen, wenn ein Rückruf ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="795da-166">The function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="795da-167">**Wsaeingabe**</span><span class="sxs-lookup"><span data-stu-id="795da-167">**WSAEINTR**</span></span> | <span data-ttu-id="795da-168">Ein Blockierungs Vorgang wurde unterbrochen.</span><span class="sxs-lookup"><span data-stu-id="795da-168">A blocking operation was interrupted.</span></span> |
| <span data-ttu-id="795da-169">**Wsaabval**</span><span class="sxs-lookup"><span data-stu-id="795da-169">**WSAEINVAL**</span></span> | <span data-ttu-id="795da-170">Der *dwIoControlCode* -Parameter ist kein gültiger Befehl, oder ein angegebener Eingabeparameter ist nicht zulässig, oder der Befehl ist nicht auf den angegebenen Sockettyp anwendbar.</span><span class="sxs-lookup"><span data-stu-id="795da-170">The *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> <span data-ttu-id="795da-171">Dieser Fehler wird zurückgegeben, wenn der *cboutbuffer* -Parameter kleiner als die Größe eines **ulong** -Datentyps ist.</span><span class="sxs-lookup"><span data-stu-id="795da-171">This error is returned if the *cbOutBuffer* parameter is less than the size of a **ULONG** data type.</span></span> |
| <span data-ttu-id="795da-172">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="795da-172">**WSAENETDOWN**</span></span> | <span data-ttu-id="795da-173">Das Netzwerk Subsystem ist fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="795da-173">The network subsystem has failed.</span></span> |
| <span data-ttu-id="795da-174">**Wsaumoproumopt**</span><span class="sxs-lookup"><span data-stu-id="795da-174">**WSAENOPROTOOPT**</span></span> | <span data-ttu-id="795da-175">Die Socketoption wird für das angegebene Protokoll nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="795da-175">The socket option is not supported on the specified protocol.</span></span> |
| <span data-ttu-id="795da-176">**WSAENOTCONN**</span><span class="sxs-lookup"><span data-stu-id="795da-176">**WSAENOTCONN**</span></span> | <span data-ttu-id="795da-177">Die Socket *s* ist nicht verbunden.</span><span class="sxs-lookup"><span data-stu-id="795da-177">The socket *s* is not connected.</span></span> |
| <span data-ttu-id="795da-178">**Wsaumotsock**</span><span class="sxs-lookup"><span data-stu-id="795da-178">**WSAENOTSOCK**</span></span> | <span data-ttu-id="795da-179">Der Deskriptor *s* ist kein Socket.</span><span class="sxs-lookup"><span data-stu-id="795da-179">The descriptor *s* is not a socket.</span></span> |
| <span data-ttu-id="795da-180">**WSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="795da-180">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="795da-181">Der angegebene ioctl-Befehl wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="795da-181">The specified IOCTL command is not supported.</span></span> <span data-ttu-id="795da-182">Dieser Fehler wird zurückgegeben, wenn die **\_ Abfrage der \_ WFP-Verbindungs Umleitung für den \_ \_ \_ Daten bankverbindungs** -Datensatz ioctl vom Transportanbieter nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="795da-182">This error is returned if the **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL is not supported by the transport provider.</span></span> |

## <a name="remarks"></a><span data-ttu-id="795da-183">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="795da-183">Remarks</span></span>

<span data-ttu-id="795da-184">Die **Konfigurations \_ \_ \_ \_ \_ Datensätze der WFP-Verbindungs Umleitung** werden von Windows 8, Windows Server 2012 und neueren Versionen des Betriebssystems unterstützt.</span><span class="sxs-lookup"><span data-stu-id="795da-184">The **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL is supported on Windows 8, and Windows Server 2012, and later versions of the operating system.</span></span>

<span data-ttu-id="795da-185">WFP ermöglicht den Zugriff auf den TCP/IP-Paket Verarbeitungs Pfad, in dem ausgehende und eingehende Pakete überprüft oder geändert werden können, bevor Sie weiterverarbeitet werden können.</span><span class="sxs-lookup"><span data-stu-id="795da-185">WFP allows access to the TCP/IP packet processing path, wherein outgoing and incoming packets can be examined or changed before allowing them to be processed further.</span></span>
<span data-ttu-id="795da-186">Durch das Tippen auf den TCP/IP-Verarbeitungs Pfad können unabhängige Softwarehersteller (ISVs) leichter Firewalls, Antivirussoftware, Diagnosesoftware und andere Arten von Anwendungen und Diensten erstellen.</span><span class="sxs-lookup"><span data-stu-id="795da-186">By tapping into the TCP/IP processing path, independent software vendors (ISVs) can more easily create firewalls, antivirus software, diagnostic software, and other types of applications and services.</span></span>
<span data-ttu-id="795da-187">WFP stellt Komponenten im Benutzermodus und im Kernel Modus bereit, sodass Drittanbieter-ISVs an den Filter Entscheidungen teilnehmen können, die auf mehreren Ebenen im TCP/IP-Protokollstapel und im gesamten Betriebssystem stattfinden.</span><span class="sxs-lookup"><span data-stu-id="795da-187">WFP provides user-mode and kernel-mode components so that third-party ISVs can participate in the filtering decisions that take place at several layers in the TCP/IP protocol stack and throughout the operating system.</span></span>
<span data-ttu-id="795da-188">Mithilfe des WFP-Verbindungs Umleitungs Features kann ein WFP-Legenden-Kernel-Treiber eine Verbindung lokal an einen Benutzermodusprozess umleiten, eine Inhalts Untersuchung im Benutzermodus durchführen und den überprüften Inhalt mithilfe einer anderen Verbindung zum ursprünglichen Ziel weiterleiten.</span><span class="sxs-lookup"><span data-stu-id="795da-188">The WFP connection redirect feature allows a WFP callout kernel driver to redirect a connection locally to a user-mode process, perform content inspection in user-mode, and forward the inspected content using a different connection to the original destination.</span></span>

<span data-ttu-id="795da-189">Bei der Verbindung mit der **\_ \_ WFP-Verbindungs \_ Umleitung \_ \_** für die zentral Abfrage werden ioctl und mehrere andere verwandte IOCTLs-Datensätze im benutzermodusbereich verwendet, damit mehrere WFP-basierte Verbindungs Proxy Anwendungen den gleichen Daten Verkehrsfluss auf kooperative Weise überprüfen können.</span><span class="sxs-lookup"><span data-stu-id="795da-189">The **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL and several other related IOCTLS are user-mode components used to allow multiple WFP-based connection proxy applications to inspect the same traffic flow in a cooperative manner.</span></span>
<span data-ttu-id="795da-190">Jeder Inspektions Agent kann den Netzwerk Datenverkehr, der bereits von einem anderen Inspektions Agent überprüft wurde, sicher erneut überprüfen.</span><span class="sxs-lookup"><span data-stu-id="795da-190">Each inspection agent can safely re-inspect network traffic that has already been inspected by another inspection agent.</span></span>
<span data-ttu-id="795da-191">Durch das vorhanden sein mehrerer Proxys (z. b. durch verschiedene ISVs) kann die Verbindung, die von einem Proxy für die Kommunikation mit dem endgültigen Ziel verwendet wird, wiederum von einem zweiten Proxy umgeleitet werden, und diese neue Verbindung kann erneut vom ursprünglichen Proxy umgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="795da-191">With the presence of multiple proxies (developed by different ISVs, for example) the connection used by one proxy to communicate with the final destination could in turn be redirected by a second proxy, and that new connection could again be redirected by the original proxy.</span></span>
<span data-ttu-id="795da-192">Ohne Verbindungs Nachverfolgung erreicht die ursprüngliche Verbindung möglicherweise nie das endgültige Ziel, weil Sie in einer unendlichen Proxy Schleife hängen bleibt.</span><span class="sxs-lookup"><span data-stu-id="795da-192">Without connection tracking, the original connection might never reach its final destination as it gets stuck in an infinite proxy loop.</span></span>

<span data-ttu-id="795da-193">Die **\_ \_ \_ \_ \_ Datensätze der WFP-Verbindungs Umleitung** mit der Datenbank ". ioctl" werden verwendet, um eine Proxy Verbindung für umgeleitete Socketverbindungen herzustellen.</span><span class="sxs-lookup"><span data-stu-id="795da-193">The **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL is used to provide proxied connection tracking on redirected socket connections.</span></span>
<span data-ttu-id="795da-194">Diese WFP-Funktion ermöglicht das Nachverfolgen von Umleitungs Datensätzen von der anfänglichen Umleitung einer Verbindung zur endgültigen Verbindung zum Ziel.</span><span class="sxs-lookup"><span data-stu-id="795da-194">This WFP feature facilitates tracking of redirection records from the initial redirect of a connection to the final connection to the destination.</span></span>

<span data-ttu-id="795da-195">Die **\_ Abfrage Datensätze für die WFP-Verbindung mit der Leistungs \_ \_ \_ \_ Datensätze** ". ioctl" wird von einem WFP-basierten Umleitungs Dienst verwendet, um den Umleitungs Daten Satz von der akzeptierten TCP/IP-Paket Verbindung (z. b. den verbundenen Socket für einen TCP-Socket oder einen UDP-Socket **ALE_CONNECT_REDIRECT** ) abzurufen</span><span class="sxs-lookup"><span data-stu-id="795da-195">The **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL is used by a WFP-based redirect service to retrieve the redirect record from the accepted TCP/IP packet connection (the connected socket for a TCP socket or a UDP socket, for example) redirected to it by its companion kernel-mode callout registered at **ALE_CONNECT_REDIRECT** layers in a kernel-mode driver.</span></span>
<span data-ttu-id="795da-196">Der **\_ \_ \_ Verbindungs \_ Umleitungs \_ Kontext** ioctl für die WFP-Abfrage wird von einem WFP-basierten Umleitungs Dienst verwendet, um den Umleitungs Kontext für einen Umleitungs Daten Satz von der akzeptierten TCP/IP-Paket Verbindung (z. b. den verbundenen Socket für einen TCP-Socket oder einen UDP-Socket **) \_ \_** abzurufen</span><span class="sxs-lookup"><span data-stu-id="795da-196">The **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_CONTEXT** IOCTL is used by a WFP-based redirect service to retrieve the redirect context for a redirect record from the accepted TCP/IP packet connection (the connected socket for a TCP socket or a UDP socket, for example) redirected to it by its companion callout registered at **ALE\_CONNECT\_REDIRECT** layers.</span></span>
<span data-ttu-id="795da-197">Der Umleitungs Kontext ist ein optionaler vom Treiber zugewiesener Kontext, der verwendet wird, wenn der aktuelle Umleitungs Status einer Verbindung darin besteht, dass die Verbindung vom aufrufenden Umleitungs Dienst umgeleitet wurde oder die Verbindung zuvor durch den aufrufenden Umleitungs Dienst umgeleitet, aber später von einem anderen Umleitungs Dienst umgeleitet wurde.</span><span class="sxs-lookup"><span data-stu-id="795da-197">The redirect context is an optional driver-allocated context used if the current redirection state of a connection is that the connection was redirected by the calling redirect service or the connection was previously redirected by the calling redirect service but later redirected again by a different redirect service.</span></span>
<span data-ttu-id="795da-198">Bei einer TCP-Proxy Verbindung überträgt der Umleitungs Dienst den abgerufenen Umleitungs Daten Satz an den TCP-Socket, der zum Proxy des ursprünglichen Inhalts verwendet wird, indem er die IOCTL- **\_ \_ \_ Verbindungs \_ \_ Datensätze der WFP-Verbindung** verwendet.</span><span class="sxs-lookup"><span data-stu-id="795da-198">For a TCP proxy connection, the redirect service transfers the retrieved redirect record to the TCP socket it uses to proxy the original content using the **SIO\_SET\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL.</span></span>

<span data-ttu-id="795da-199">Wenn der Umleitungs Dienst einen nicht-TCP-Socket umleitet (z. b. UDP), wird durch die von der Leistungsindikator- **\_ \_ WFP- \_ Verbindungs \_ Umleitung \_** zurückgegebenen Umleitungs Datensätze ioctl darauf hingewiesen, dass die [**wsamsg**](/windows/desktop/api/ws2def/ns-ws2def-wsamsg) -Struktur mit der Funktion [**LPFN_WSARECVMSG (wsarecvmsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="795da-199">When the redirect service is redirecting a non-TCP socket (UDP, for example), the redirect records returned by the **SIO\_QUERY\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL indicate this to the redirect service using the [**WSAMSG**](/windows/desktop/api/ws2def/ns-ws2def-wsamsg) structure used with the [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) function.</span></span>
<span data-ttu-id="795da-200">Das Steuerelementmember der [**wsamsg**](/windows/desktop/api/ws2def/ns-ws2def-wsamsg) -Struktur hätte eine cmsg_type in der **wsacmsghdr** -Struktur, die auf den **\_ \_ Umleitungs \_ Daten Satz der IP-Verbindung** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="795da-200">The Control member of the [**WSAMSG**](/windows/desktop/api/ws2def/ns-ws2def-wsamsg) structure would have a cmsg_type in the **WSACMSGHDR** structure set to **IP\_CONNECTION\_REDIRECT\_RECORD**.</span></span>
<span data-ttu-id="795da-201">Der [**LPFN_WSARECVMSG Parameter (wsarecvmsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) muss vom Umleitungs Dienst bereitgestellt werden, wenn nicht-TCP-Umleitungen akzeptiert werden.</span><span class="sxs-lookup"><span data-stu-id="795da-201">The [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) parameter must be supplied by the redirect service when accepting non-TCP redirects.</span></span>

<span data-ttu-id="795da-202">Bei nicht-TCP-Datenverkehr wird der Umleitungs Daten Satz mithilfe der [**wsamsg**](/windows/desktop/api/ws2def/ns-ws2def-wsamsg) -Struktur mit der [**wsasendmsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) -Funktion weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="795da-202">For non-TCP traffic, the redirect record is forwarded using the [**WSAMSG**](/windows/desktop/api/ws2def/ns-ws2def-wsamsg) structure with the [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) function.</span></span>

<span data-ttu-id="795da-203">Beachten Sie, dass für nicht-TCP-Datenverkehr nur das Flow-Erfassungs Paket den **Datensatz der IP- \_ Verbindungs \_ Umleitung \_** enthält.</span><span class="sxs-lookup"><span data-stu-id="795da-203">Note that for non-TCP traffic, only the flow-creating packet will carry the **IP\_CONNECTION\_REDIRECT\_RECORD**.</span></span>
<span data-ttu-id="795da-204">Folglich muss nur das erste Proxy Paket diese Informationen mithilfe der [**LPFN_WSARECVMSG (wsarecvmsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) -Funktion einschließen.</span><span class="sxs-lookup"><span data-stu-id="795da-204">As a result, only the first proxied packet needs to include this information using the [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) function.</span></span>

<span data-ttu-id="795da-205">Da der WFP-Umleitungs Daten Satz ein Daten-BLOB mit variabler Länge ist, kann der Aufrufer entweder einen großen Ausgabepuffer (z. b. einen 1.024-Byte-Puffer, auf den der *lpvoutbuffer* -Parameter zeigt) bereitstellen oder eine Ausgabepuffergröße im *cboutbuffer* -Parameter von 0 übergeben, um die Puffergröße abzufragen, die für das</span><span class="sxs-lookup"><span data-stu-id="795da-205">Since the WFP redirect record is a variable length data blob, the caller can either supply a large output buffer (a 1,024 byte buffer pointed to by the *lpvOutBuffer* parameter, for example) or can pass an output buffer size in the *cbOutBuffer* parameter of 0 to query the buffer size required to hold the returned blob.</span></span>
<span data-ttu-id="795da-206">Wenn die Ausgabepuffergröße nicht ausreichend ist, um die Daten zu speichern, gibt die [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) -oder **wspioctl** -Funktion den **Fehler "Fehler \_ unzureichend \_** " zurück, und die erforderliche Puffergröße wird als Wert zurückgegeben, auf den der *lpcbbytesreturn* -Parameter verweist.</span><span class="sxs-lookup"><span data-stu-id="795da-206">If the output buffer size is not sufficient to the hold the data, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** functions will return **ERROR\_INSUFFICIENT\_BUFFER** and the required buffer size will be returned in value pointed to by the *lpcbBytesReturned* parameter.</span></span>

<span data-ttu-id="795da-207">Die Anwendung, die den [**SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT**](sio-query-wfp-connection-redirect-context.md) aufrufen, muss das BLOB, das den abgerufenen Umleitungs Kontext enthält, nicht verstehen.</span><span class="sxs-lookup"><span data-stu-id="795da-207">The application calling the [**SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT**](sio-query-wfp-connection-redirect-context.md) does not need to understand the blob containing the redirect context retrieved.</span></span>
<span data-ttu-id="795da-208">Dies ist ein undurchsichtiges BLOB von Daten, das die Anwendung abrufen und an den neuen Socket zurückgeben muss.</span><span class="sxs-lookup"><span data-stu-id="795da-208">This is an opaque blob of data that the application needs to retrieve and pass back to the new socket.</span></span>

## <a name="see-also"></a><span data-ttu-id="795da-209">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="795da-209">See also</span></span>

[<span data-ttu-id="795da-210">**IPPROTO_IP Socketoptionen**</span><span class="sxs-lookup"><span data-stu-id="795da-210">**IPPROTO_IP Socket Options**</span></span>](/windows/desktop/winsock/ipproto-ip-socket-options)

[<span data-ttu-id="795da-211">**SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT**</span><span class="sxs-lookup"><span data-stu-id="795da-211">**SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT**</span></span>](sio-query-wfp-connection-redirect-context.md)

[<span data-ttu-id="795da-212">**Glühbirne**</span><span class="sxs-lookup"><span data-stu-id="795da-212">**socket**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="795da-213">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="795da-213">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[<span data-ttu-id="795da-214">**Wsagein verlappedresult**</span><span class="sxs-lookup"><span data-stu-id="795da-214">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="795da-215">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="795da-215">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="795da-216">**Wsamsg**</span><span class="sxs-lookup"><span data-stu-id="795da-216">**WSAMSG**</span></span>](/windows/desktop/api/ws2def/ns-ws2def-wsamsg)

[<span data-ttu-id="795da-217">**Wsaoverlgetauscht**</span><span class="sxs-lookup"><span data-stu-id="795da-217">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="795da-218">**LPFN_WSARECVMSG (wsarecvmsg)**</span><span class="sxs-lookup"><span data-stu-id="795da-218">**LPFN_WSARECVMSG (WSARecvMsg)**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)

[<span data-ttu-id="795da-219">**Wsasendmsg**</span><span class="sxs-lookup"><span data-stu-id="795da-219">**WSASendMsg**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg)

[<span data-ttu-id="795da-220">**Wsasocketa**</span><span class="sxs-lookup"><span data-stu-id="795da-220">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="795da-221">**Wsasocketw**</span><span class="sxs-lookup"><span data-stu-id="795da-221">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
