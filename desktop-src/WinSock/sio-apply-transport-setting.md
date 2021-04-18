---
description: Der Steuercode wendet mindestens eine Transport Einstellung auf einen Socket an.
ms.assetid: FA0657EE-B65E-4EFA-AF1E-CA0EA7B27715
title: SIO_APPLY_TRANSPORT_SETTING Steuerungs Codes
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: e167a87e70dc3c6c44a263308beb333176a3d525
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343799"
---
# <a name="sio_apply_transport_setting-control-code"></a><span data-ttu-id="2dbfb-103">SIO_APPLY_TRANSPORT_SETTING Steuerungs Codes</span><span class="sxs-lookup"><span data-stu-id="2dbfb-103">SIO_APPLY_TRANSPORT_SETTING Control Code</span></span>

## <a name="description"></a><span data-ttu-id="2dbfb-104">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2dbfb-104">Description</span></span>

<span data-ttu-id="2dbfb-105">Der Verwaltungs Code für die **\_ \_ Transport \_ Einstellung von SIO** wendet mindestens eine Transport Einstellung auf einen Socket an.</span><span class="sxs-lookup"><span data-stu-id="2dbfb-105">The **SIO\_APPLY\_TRANSPORT\_SETTING** control code applies one or more transport settings to a socket.</span></span>

<span data-ttu-id="2dbfb-106">Um diesen Vorgang auszuführen, wenden Sie die [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) -oder **wspioctl** -Funktion mit den folgenden Parametern an.</span><span class="sxs-lookup"><span data-stu-id="2dbfb-106">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_APPLY_TRANSPORT_SETTING, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to the input buffer
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,             // pointer to the output buffer
  (DWORD) cbOutBuffer,   // size, in bytes, of the output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_APPLY_TRANSPORT_SETTING, // dwIoControlCode
  (LPVOID) lpvInBuffer,  // pointer to the input buffer
  (DWORD) cbInBuffer,    // size, in bytes, of the input buffer
  (LPVOID) lpvOutBuffer,             // pointer to the output buffer
  (DWORD) cbOutBuffer,   // size, in bytes, of the output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,   // a WSATHREADID structure
  (LPINT) lpErrno   // a pointer to the error code.
);
```

## <a name="parameters"></a><span data-ttu-id="2dbfb-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="2dbfb-107">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="2dbfb-108">s</span><span class="sxs-lookup"><span data-stu-id="2dbfb-108">s</span></span>

<span data-ttu-id="2dbfb-109">Ein Deskriptor, der einen Socket identifiziert.</span><span class="sxs-lookup"><span data-stu-id="2dbfb-109">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="2dbfb-110">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="2dbfb-110">dwIoControlCode</span></span>

<span data-ttu-id="2dbfb-111">Der Steuerelement Code für den Vorgang.</span><span class="sxs-lookup"><span data-stu-id="2dbfb-111">The control code for the operation.</span></span>
<span data-ttu-id="2dbfb-112">Verwenden Sie für diesen Vorgang die **\_ \_ Transport \_ Einstellung für "sio anwenden** ".</span><span class="sxs-lookup"><span data-stu-id="2dbfb-112">Use **SIO\_APPLY\_TRANSPORT\_SETTING** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="2dbfb-113">lpvinbuffer</span><span class="sxs-lookup"><span data-stu-id="2dbfb-113">lpvInBuffer</span></span>

<span data-ttu-id="2dbfb-114">Ein Zeiger auf den Eingabepuffer.</span><span class="sxs-lookup"><span data-stu-id="2dbfb-114">A pointer to the input buffer.</span></span>
<span data-ttu-id="2dbfb-115">Dieser Parameter enthält einen Zeiger auf eine-Struktur, in der der erste Member der-Struktur eine [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) Struktur ist, die bestimmt, welche Transport Einstellung angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="2dbfb-115">This parameter contains a pointer to a structure where the first member of the structure is a [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) structure that determines what transport setting is being applied.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="2dbfb-116">cbinbuffer</span><span class="sxs-lookup"><span data-stu-id="2dbfb-116">cbInBuffer</span></span>

<span data-ttu-id="2dbfb-117">Die Größe des Eingabe Puffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="2dbfb-117">The size, in bytes, of the input buffer.</span></span>
<span data-ttu-id="2dbfb-118">Dieser Parameter hängt von der angewendeten Transport Einstellung ab.</span><span class="sxs-lookup"><span data-stu-id="2dbfb-118">This parameter depends on the transport setting being applied.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="2dbfb-119">lpvoutbuffer</span><span class="sxs-lookup"><span data-stu-id="2dbfb-119">lpvOutBuffer</span></span>

<span data-ttu-id="2dbfb-120">Ein Zeiger auf den Ausgabepuffer.</span><span class="sxs-lookup"><span data-stu-id="2dbfb-120">A pointer to the output buffer.</span></span>
<span data-ttu-id="2dbfb-121">Dieser Parameter hängt von der angewendeten Transport Einstellung ab.</span><span class="sxs-lookup"><span data-stu-id="2dbfb-121">This parameter depends on the transport setting being applied.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="2dbfb-122">cboutbuffer</span><span class="sxs-lookup"><span data-stu-id="2dbfb-122">cbOutBuffer</span></span>

<span data-ttu-id="2dbfb-123">Die Größe des Ausgabepuffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="2dbfb-123">The size, in bytes, of the output buffer.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="2dbfb-124">lpcbbyteszurück gegeben</span><span class="sxs-lookup"><span data-stu-id="2dbfb-124">lpcbBytesReturned</span></span>

<span data-ttu-id="2dbfb-125">Ein Zeiger auf eine Variable, die die Größe der im Ausgabepuffer gespeicherten Daten (in Bytes) empfängt.</span><span class="sxs-lookup"><span data-stu-id="2dbfb-125">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>

<span data-ttu-id="2dbfb-126">Wenn der Ausgabepuffer zu klein ist, schlägt der-Befehl fehl, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) gibt [**WSAEINVAL**](windows-sockets-error-codes-2.md)zurück, und der *lpcbbytesreturns* -Parameter verweist auf den **DWORD** -Wert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="2dbfb-126">If the output buffer is too small, the call fails, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns [**WSAEINVAL**](windows-sockets-error-codes-2.md), and the *lpcbBytesReturned* parameter points to a **DWORD** value of zero.</span></span>

<span data-ttu-id="2dbfb-127">Wenn *lpoverlgetauscht* gleich **null** ist, kann der **DWORD** -Wert, auf den der *lpcbbytesall* -Parameter verweist, der bei einem erfolgreichen-Vorgang zurückgegeben wird, nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="2dbfb-127">If *lpOverlapped* is **NULL**, the **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned on a successful call cannot be zero.</span></span>

<span data-ttu-id="2dbfb-128">Wenn der *lpoverllapp* -Parameter für überlappende Sockets nicht **null** ist, werden Vorgänge, die nicht sofort abgeschlossen werden können, initiiert, und der Abschluss wird zu einem späteren Zeitpunkt angegeben.</span><span class="sxs-lookup"><span data-stu-id="2dbfb-128">If the *lpOverlapped* parameter is not **NULL** for overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>
<span data-ttu-id="2dbfb-129">Der **DWORD** -Wert, auf den der zurückgegebene *lpcbbyteszurück gegebene* Parameter verweist, kann NULL sein, da die Größe der gespeicherten Daten erst bestimmt werden kann, wenn der überlappende Vorgang abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="2dbfb-129">The **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned may be zero since the size of the data stored can't be determined until the overlapped operation has completed.</span></span>
<span data-ttu-id="2dbfb-130">Der endgültige Abschluss Status kann abgerufen werden, wenn die geeignete Vervollständigungs Methode signalisiert wird, wenn der Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="2dbfb-130">The final completion status can be retrieved when the appropriate completion method is signaled when the operation has completed.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="2dbfb-131">lpvoverlgetauscht</span><span class="sxs-lookup"><span data-stu-id="2dbfb-131">lpvOverlapped</span></span>

<span data-ttu-id="2dbfb-132">Ein Zeiger auf eine [**wsaoverllapp**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="2dbfb-132">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="2dbfb-133">Wenn Socket *s* ohne das überlappende Attribut erstellt wurde, wird der *lpoverllapp* -Parameter ignoriert.</span><span class="sxs-lookup"><span data-stu-id="2dbfb-133">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="2dbfb-134">Wenn *s* mit dem überlappenden Attribut geöffnet wurde und der *lpoverlgetauscht* -Parameter nicht **null** ist, wird der Vorgang als überlappende (asynchrone) Operation ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2dbfb-134">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="2dbfb-135">In diesem Fall muss der *lpoverllapp* -Parameter auf eine gültige [**wsaoverllapp**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) -Struktur zeigen.</span><span class="sxs-lookup"><span data-stu-id="2dbfb-135">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="2dbfb-136">Bei überlappenden Vorgängen gibt die Funktion [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) oder **wspioctl** sofort zurück, und die entsprechende Vervollständigungs Methode wird signalisiert, wenn der Vorgang abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="2dbfb-136">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="2dbfb-137">Andernfalls gibt die Funktion nicht zurück, bis der Vorgang abgeschlossen ist oder ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="2dbfb-137">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="2dbfb-138">lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="2dbfb-138">lpCompletionRoutine</span></span>

<span data-ttu-id="2dbfb-139">Typ: \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="2dbfb-139">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="2dbfb-140">Ein Zeiger auf die Vervollständigungs Routine, die aufgerufen wird, wenn der Vorgang abgeschlossen wurde (bei nicht überlappenden Sockets ignoriert).</span><span class="sxs-lookup"><span data-stu-id="2dbfb-140">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="2dbfb-141">lpthreadid</span><span class="sxs-lookup"><span data-stu-id="2dbfb-141">lpThreadId</span></span>

<span data-ttu-id="2dbfb-142">Ein Zeiger auf eine [**wsathreadid**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) -Struktur, die vom Anbieter in einem nachfolgenden [**wpuqueueapc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc)-Rückruf verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="2dbfb-142">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="2dbfb-143">Der Anbieter sollte die referenzierte [**wsathreadid**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) -Struktur (nicht den Zeiger auf dieselbe) speichern, bis die [**wpuqueueapc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) -Funktion zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="2dbfb-143">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="2dbfb-144">**Hinweis**  Dieser Parameter gilt nur für die **wspioctl** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="2dbfb-144">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="2dbfb-145">lperrno</span><span class="sxs-lookup"><span data-stu-id="2dbfb-145">lpErrno</span></span>

<span data-ttu-id="2dbfb-146">Ein Zeiger auf den Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="2dbfb-146">A pointer to the error code.</span></span>

<span data-ttu-id="2dbfb-147">**Hinweis**  Dieser Parameter gilt nur für die **wspioctl** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="2dbfb-147">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="2dbfb-148">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2dbfb-148">Return value</span></span>

<span data-ttu-id="2dbfb-149">Wenn der Vorgang erfolgreich abgeschlossen wird, gibt die [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) -oder **wspioctl** -Funktion NULL zurück.</span><span class="sxs-lookup"><span data-stu-id="2dbfb-149">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="2dbfb-150">Wenn der Vorgang fehlschlägt oder aussteht, gibt die Funktion [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) oder **wspioctl** einen **\_ Socketfehler** zurück.</span><span class="sxs-lookup"><span data-stu-id="2dbfb-150">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="2dbfb-151">Um erweiterte Fehlerinformationen abzurufen, nennen Sie [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="2dbfb-151">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="2dbfb-152">Fehlercode</span><span class="sxs-lookup"><span data-stu-id="2dbfb-152">Error code</span></span> | <span data-ttu-id="2dbfb-153">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="2dbfb-153">Meaning</span></span> |
|------------|---------|
|<span data-ttu-id="2dbfb-154">**ausstehende WSA-e/a \_ \_**</span><span class="sxs-lookup"><span data-stu-id="2dbfb-154">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="2dbfb-155">Überlappende e/a-Vorgänge werden ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2dbfb-155">Overlapped I/O operation is in progress.</span></span> <span data-ttu-id="2dbfb-156">Dieser Wert wird zurückgegeben, wenn ein überlappende Vorgang erfolgreich initiiert wurde und die Beendigung zu einem späteren Zeitpunkt angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="2dbfb-156">This value is returned if an overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="2dbfb-157">**WSA- \_ Vorgang \_ abgebrochen**</span><span class="sxs-lookup"><span data-stu-id="2dbfb-157">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="2dbfb-158">Der e/a-Vorgang wurde aufgrund eines Thread Beendigungs-oder einer Anwendungsanforderung abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="2dbfb-158">The I/O operation has been aborted because of either a thread exit or an application request.</span></span> <span data-ttu-id="2dbfb-159">Dieser Fehler wird zurückgegeben, wenn ein über Lapp ender Vorgang aufgrund der Schließung des Sockets oder der Ausführung des Befehls " **SIO \_ Flush** ioctl" abgebrochen wurde.</span><span class="sxs-lookup"><span data-stu-id="2dbfb-159">This error is returned if an overlapped operation was canceled due to the closure of the socket or the execution of the **SIO\_FLUSH** IOCTL command.</span></span> |
| <span data-ttu-id="2dbfb-160">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="2dbfb-160">**WSAEFAULT**</span></span> | <span data-ttu-id="2dbfb-161">Das System hat bei dem Versuch, ein Zeigerargument in einem-Befehl zu verwenden, eine ungültige Zeiger Adresse erkannt.</span><span class="sxs-lookup"><span data-stu-id="2dbfb-161">The system detected an invalid pointer address in attempting to use a pointer argument in a call.</span></span> <span data-ttu-id="2dbfb-162">Dieser Fehler wird zurückgegeben, wenn der Parameter *lpvinbuffer*, *lpvoutbuffer*, *lpcbbytesall*, *lpoverlgetauscht* oder *lpCompletionRoutine* nicht vollständig in einem gültigen Teil des Benutzer Adressraums enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="2dbfb-162">This error is returned of the *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="2dbfb-163">**Wsaeingabe Progress**</span><span class="sxs-lookup"><span data-stu-id="2dbfb-163">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="2dbfb-164">Ein Blockierungsvorgang wird momentan ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2dbfb-164">A blocking operation is currently executing.</span></span> <span data-ttu-id="2dbfb-165">Dieser Fehler wird zurückgegeben, wenn die Funktion aufgerufen wird, wenn ein Rückruf ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2dbfb-165">This error is returned if the function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="2dbfb-166">**Wsaeingabe**</span><span class="sxs-lookup"><span data-stu-id="2dbfb-166">**WSAEINTR**</span></span> | <span data-ttu-id="2dbfb-167">Ein Blockierungs Vorgang wurde durch einen [**wsacancelblockingstatement**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall)-Aufrufvorgang unterbrochen.</span><span class="sxs-lookup"><span data-stu-id="2dbfb-167">A blocking operation was interrupted by a call to [**WSACancelBlockingCall**](/windows/desktop/api/winsock2/nf-winsock2-wsacancelblockingcall).</span></span> <span data-ttu-id="2dbfb-168">Dieser Fehler wird zurückgegeben, wenn ein Blockierungs Vorgang unterbrochen wurde.</span><span class="sxs-lookup"><span data-stu-id="2dbfb-168">This error is returned if a blocking operation was interrupted.</span></span> |
| <span data-ttu-id="2dbfb-169">**Wsaabval**</span><span class="sxs-lookup"><span data-stu-id="2dbfb-169">**WSAEINVAL**</span></span> | <span data-ttu-id="2dbfb-170">Ein ungültiges Argument wurde angegeben.</span><span class="sxs-lookup"><span data-stu-id="2dbfb-170">An invalid argument was supplied.</span></span> <span data-ttu-id="2dbfb-171">Dieser Fehler wird zurückgegeben, wenn der *dwIoControlCode* -Parameter kein gültiger Befehl ist oder wenn ein angegebener Eingabeparameter nicht zulässig ist oder der Befehl nicht auf den angegebenen Sockettyp anwendbar ist.</span><span class="sxs-lookup"><span data-stu-id="2dbfb-171">This error is returned if the *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> |
| <span data-ttu-id="2dbfb-172">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="2dbfb-172">**WSAENETDOWN**</span></span> | <span data-ttu-id="2dbfb-173">Bei einem Socketvorgang war das Netzwerk inaktiv.</span><span class="sxs-lookup"><span data-stu-id="2dbfb-173">A socket operation encountered a dead network.</span></span> <span data-ttu-id="2dbfb-174">Dieser Fehler wird zurückgegeben, wenn das Netzwerk Subsystem fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="2dbfb-174">This error is returned if the network subsystem has failed.</span></span> |
| <span data-ttu-id="2dbfb-175">**Wsaumotsock**</span><span class="sxs-lookup"><span data-stu-id="2dbfb-175">**WSAENOTSOCK**</span></span> | <span data-ttu-id="2dbfb-176">Es wurde versucht, einen Vorgang für etwas auszuführen, das kein Socket ist.</span><span class="sxs-lookup"><span data-stu-id="2dbfb-176">An operation was attempted on something that is not a socket.</span></span> <span data-ttu-id="2dbfb-177">Dieser Fehler wird zurückgegeben, wenn es sich bei den *Deskriptoren nicht* um einen Socket handelt.</span><span class="sxs-lookup"><span data-stu-id="2dbfb-177">This error is returned if the descriptor *s* is not a socket.</span></span> |
| <span data-ttu-id="2dbfb-178">**WSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="2dbfb-178">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="2dbfb-179">Der versuchte Vorgang wird für den Typ des Objekts, auf das verwiesen wird, nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2dbfb-179">The attempted operation is not supported for the type of object referenced.</span></span> <span data-ttu-id="2dbfb-180">Dieser Fehler wird zurückgegeben, wenn der angegebene ioctl-Befehl nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="2dbfb-180">This error is returned if the specified IOCTL command is not supported.</span></span> <span data-ttu-id="2dbfb-181">Dieser Fehler wird auch zurückgegeben, wenn die IOCTL- **\_ \_ Transport \_ Einstellung für** die Transport Einstellung vom Transport Anbieter nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="2dbfb-181">This error is also returned if the **SIO\_APPLY\_TRANSPORT\_SETTING** IOCTL is not supported by the transport provider.</span></span> <span data-ttu-id="2dbfb-182">Dieser Fehler wird auch zurückgegeben, wenn bei dem Versuch, die IOCTL- **\_ \_ Transport \_ Einstellung für "sio Apply** " zu verwenden, ein anderer Socket als UDP oder TCP verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2dbfb-182">This error is also returned when an attempt to use the **SIO\_APPLY\_TRANSPORT\_SETTING** IOCTL is made on a socket other than UDP or TCP.</span></span> |

## <a name="remarks"></a><span data-ttu-id="2dbfb-183">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2dbfb-183">Remarks</span></span>

<span data-ttu-id="2dbfb-184">Die IOCTL- **\_ \_ Transport \_ Einstellung** für das Betriebssystem Windows 8, Windows Server 2012 und höhere Versionen des Betriebssystems wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="2dbfb-184">The **SIO\_APPLY\_TRANSPORT\_SETTING** IOCTL is supported on Windows 8, and Windows Server 2012, and later versions of the operating system.</span></span>

<span data-ttu-id="2dbfb-185">Die IOCTL- **\_ \_ Transport \_ Einstellung** für "sio" ist eine generische IOCTL, die zum Anwenden der Transport Einstellung auf Socket verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2dbfb-185">The **SIO\_APPLY\_TRANSPORT\_SETTING** IOCTL is a generic IOCTL used to apply transport setting to socket.</span></span>
<span data-ttu-id="2dbfb-186">Die angewendete Transport Einstellung basiert auf der [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) , die im *lpvinbuffer* -Parameter übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="2dbfb-186">The transport setting being applied is based on the [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) passed in the *lpvInBuffer* parameter.</span></span>

<span data-ttu-id="2dbfb-187">Ab Windows 8 und Windows Server 2012 definiert das System die **REAL_TIME_NOTIFICATION_CAPABILITY** Funktion auf einem TCP-Socket.</span><span class="sxs-lookup"><span data-stu-id="2dbfb-187">Starting with Windows 8 and Windows Server 2012, the system defines the **REAL_TIME_NOTIFICATION_CAPABILITY** capability on a TCP socket.</span></span>
<span data-ttu-id="2dbfb-188">Ab Windows 10 und Windows Server 2016 wird auch **der \_ \_ Kontext "nameres zuordnen** " definiert.</span><span class="sxs-lookup"><span data-stu-id="2dbfb-188">Starting with Windows 10 and Windows Server 2016, **ASSOCIATE\_NAMERES\_CONTEXT** is also defined.</span></span>
<span data-ttu-id="2dbfb-189">Weitere Informationen finden Sie unter [**addrinfoex4**](/windows/desktop/api/ws2def/ns-ws2def-addrinfoex4) und [**ASSOCIATE_NAMERES_CONTEXT_INPUT**](/windows/desktop/api/mstcpip/ns-mstcpip-associate_nameres_context_input).</span><span class="sxs-lookup"><span data-stu-id="2dbfb-189">For more information, see [**addrinfoex4**](/windows/desktop/api/ws2def/ns-ws2def-addrinfoex4) and [**ASSOCIATE_NAMERES_CONTEXT_INPUT**](/windows/desktop/api/mstcpip/ns-mstcpip-associate_nameres_context_input).</span></span>

<span data-ttu-id="2dbfb-190">Wenn für die [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) , die im lpvinbuffer-Parameter übergeben wird, das GUID-Element auf **echt \_ Zeit \_ Benachrichtigungs \_ Funktion** festgelegt ist, ist dies eine Anforderung zum Anwenden von Echt Zeit Benachrichtigungseinstellungen für den TCP-Socket, der mit dem [**controlchannel-**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) Parameter verwendet wird, um Hintergrund Netzwerk Benachrichtigungen in einer Windows Store-App</span><span class="sxs-lookup"><span data-stu-id="2dbfb-190">If the [**TRANSPORT_SETTING_ID**](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id) passed in the lpvInBuffer parameter has the Guid member set to **REAL\_TIME\_NOTIFICATION\_CAPABILITY**, then this is a request to apply real time notification settings for the TCP socket used with the [**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) to receive background network notifications in a Windows Store app.</span></span>
<span data-ttu-id="2dbfb-191">Der *lpvinbuffer* -Parameter sollte auf eine **REAL_TIME_NOTIFICATION_SETTING_INPUT** Struktur zeigen.</span><span class="sxs-lookup"><span data-stu-id="2dbfb-191">The *lpvInBuffer* parameter should point to a **REAL_TIME_NOTIFICATION_SETTING_INPUT** structure.</span></span>
<span data-ttu-id="2dbfb-192">Der *lpvoutbuffer* -Parameter wird für diesen Vorgang nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="2dbfb-192">The *lpvOutBuffer* parameter is unused for this operation.</span></span>
<span data-ttu-id="2dbfb-193">Diese Transport Einstellung gilt nur für TCP-Sockets.</span><span class="sxs-lookup"><span data-stu-id="2dbfb-193">This transport setting applies only to TCP sockets.</span></span>
<span data-ttu-id="2dbfb-194">Mit dieser Transport Einstellung können WinInet oder ähnliche Netzwerkdienste einen bestimmten TCP-Socket als aktivierten [**controlchannel-**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) Wert markieren.</span><span class="sxs-lookup"><span data-stu-id="2dbfb-194">This transport setting provides a way for WinInet or similar network services to mark a given TCP socket as [**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) enabled.</span></span>
<span data-ttu-id="2dbfb-195">Windows markiert den entsprechenden TCP-Socket und konfiguriert die entsprechenden Hardware-und Softwareeinstellungen, wenn diese Option aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="2dbfb-195">Windows will mark the corresponding TCP socket and configure appropriate hardware and software settings when this option is called.</span></span>
<span data-ttu-id="2dbfb-196">Eine Windows Store-App ruft diese IOCTL nicht direkt auf.</span><span class="sxs-lookup"><span data-stu-id="2dbfb-196">A Windows Store app will not call this IOCTL directly.</span></span>

## <a name="see-also"></a><span data-ttu-id="2dbfb-197">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2dbfb-197">See also</span></span>

[<span data-ttu-id="2dbfb-198">**ControlChannelTrigger**</span><span class="sxs-lookup"><span data-stu-id="2dbfb-198">**ControlChannelTrigger**</span></span>](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger)

[<span data-ttu-id="2dbfb-199">Glühbirne</span><span class="sxs-lookup"><span data-stu-id="2dbfb-199">socket</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="2dbfb-200">**SIO_QUERY_TRANSPORT_SETTING**</span><span class="sxs-lookup"><span data-stu-id="2dbfb-200">**SIO_QUERY_TRANSPORT_SETTING**</span></span>](sio-query-transport-setting.md)

[<span data-ttu-id="2dbfb-201">**TRANSPORT_SETTING_ID**</span><span class="sxs-lookup"><span data-stu-id="2dbfb-201">**TRANSPORT_SETTING_ID**</span></span>](/windows/desktop/api/mstcpip/ns-mstcpip-transport_setting_id)

[<span data-ttu-id="2dbfb-202">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="2dbfb-202">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)

[<span data-ttu-id="2dbfb-203">**Wsagein verlappedresult**</span><span class="sxs-lookup"><span data-stu-id="2dbfb-203">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="2dbfb-204">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="2dbfb-204">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="2dbfb-205">**Wsaoverlgetauscht**</span><span class="sxs-lookup"><span data-stu-id="2dbfb-205">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="2dbfb-206">**Wsasocketa**</span><span class="sxs-lookup"><span data-stu-id="2dbfb-206">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="2dbfb-207">**Wsasocketw**</span><span class="sxs-lookup"><span data-stu-id="2dbfb-207">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
