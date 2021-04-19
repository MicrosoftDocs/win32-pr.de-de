---
description: Steuerungs Code legt den Umleitungs Daten Satz auf den neuen TCP-Socket fest, der zum Verbinden des Umleitungs dienstan
ms.assetid: 0AC78ED4-A6EC-4D62-919C-1EF7CDE8EE80
title: SIO_SET_WFP_CONNECTION_REDIRECT_RECORDS-Steuerungscode
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 11ce07c94104ecd986dc117b00dba2a49a7b5dc5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106364108"
---
# <a name="sio_set_wfp_connection_redirect_records-control-code"></a><span data-ttu-id="b15b5-103">SIO_SET_WFP_CONNECTION_REDIRECT_RECORDS-Steuerungscode</span><span class="sxs-lookup"><span data-stu-id="b15b5-103">SIO_SET_WFP_CONNECTION_REDIRECT_RECORDS Control Code</span></span>

## <a name="description"></a><span data-ttu-id="b15b5-104">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b15b5-104">Description</span></span>

<span data-ttu-id="b15b5-105">Der Code für die **\_ \_ WFP- \_ \_ verbindungsumleitungs- \_ Datensätze der WFP-Verbindung** legt den Umleitungs Daten Satz auf den neuen TCP-Socket fest, der zum Herstellen der Verbindung mit dem endgültigen Ziel verwendet wird, um von einem Windows-Filter Plattform</span><span class="sxs-lookup"><span data-stu-id="b15b5-105">The **SIO\_SET\_WFP\_CONNECTION\_REDIRECT\_RECORDS** control code sets the redirect record to the new TCP socket used for connecting to the final destination for use by a Windows Filtering Platform (WFP) redirect service.</span></span>

<span data-ttu-id="b15b5-106">Um diesen Vorgang auszuführen, wenden Sie die [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) -oder **wspioctl** -Funktion mit den folgenden Parametern an.</span><span class="sxs-lookup"><span data-stu-id="b15b5-106">To perform this operation, call the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function with the following parameters.</span></span>

```cpp
int WSAIoctl(
  (socket) s,                              // descriptor identifying a socket
  SIO_SET_WFP_CONNECTION_REDIRECT_RECORDS, // dwIoControlCode
  (LPVOID) lpvInputBuffer,                 // lpvInBuffer
  (DWORD) cbInputBuffer,                   // cbInBuffer
  NULL,                                    // output buffer
  0,                                       // size of output buffer
  (LPDWORD) lpcbBytesReturned,             // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,          // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine, // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,                              // descriptor identifying a socket
  SIO_SET_WFP_CONNECTION_REDIRECT_RECORDS, // dwIoControlCode
  (LPVOID) lpvInputBuffer,                 // lpvInBuffer
  (DWORD) cbInputBuffer,                   // cbInBuffer
  NULL,                                    // output buffer
  0,                                       // size of output buffer
  (LPDWORD) lpcbBytesReturned,             // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,          // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,              // a WSATHREADID structure
  (LPINT) lpErrno                          // a pointer to the error code.
);
```

## <a name="parameters"></a><span data-ttu-id="b15b5-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="b15b5-107">Parameters</span></span>

### <a name="s"></a><span data-ttu-id="b15b5-108">s</span><span class="sxs-lookup"><span data-stu-id="b15b5-108">s</span></span>

<span data-ttu-id="b15b5-109">Ein Deskriptor, der einen Socket identifiziert.</span><span class="sxs-lookup"><span data-stu-id="b15b5-109">A descriptor identifying a socket.</span></span>

### <a name="dwiocontrolcode"></a><span data-ttu-id="b15b5-110">dwIoControlCode</span><span class="sxs-lookup"><span data-stu-id="b15b5-110">dwIoControlCode</span></span>

<span data-ttu-id="b15b5-111">Der Steuerelement Code für den Vorgang.</span><span class="sxs-lookup"><span data-stu-id="b15b5-111">The control code for the operation.</span></span>
<span data-ttu-id="b15b5-112">Verwenden Sie für diesen Vorgang die **\_ \_ \_ Verbindungs \_ \_ Datensätze der WFP-Verbindung** mit der</span><span class="sxs-lookup"><span data-stu-id="b15b5-112">Use **SIO\_SET\_WFP\_CONNECTION\_REDIRECT\_RECORDS** for this operation.</span></span>

### <a name="lpvinbuffer"></a><span data-ttu-id="b15b5-113">lpvinbuffer</span><span class="sxs-lookup"><span data-stu-id="b15b5-113">lpvInBuffer</span></span>

<span data-ttu-id="b15b5-114">Ein Zeiger auf den Eingabepuffer.</span><span class="sxs-lookup"><span data-stu-id="b15b5-114">A pointer to the input buffer.</span></span>
<span data-ttu-id="b15b5-115">Dieser Parameter enthält einen Zeiger auf den dem Socket zugeordneten WFP-Umleitungs Daten Satz.</span><span class="sxs-lookup"><span data-stu-id="b15b5-115">This parameter contains a pointer to the WFP redirect record associated with the socket.</span></span>

### <a name="cbinbuffer"></a><span data-ttu-id="b15b5-116">cbinbuffer</span><span class="sxs-lookup"><span data-stu-id="b15b5-116">cbInBuffer</span></span>

<span data-ttu-id="b15b5-117">Die Größe des Eingabe Puffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="b15b5-117">The size, in bytes, of the input buffer.</span></span>

### <a name="lpvoutbuffer"></a><span data-ttu-id="b15b5-118">lpvoutbuffer</span><span class="sxs-lookup"><span data-stu-id="b15b5-118">lpvOutBuffer</span></span>

<span data-ttu-id="b15b5-119">Ein Zeiger auf den Ausgabepuffer.</span><span class="sxs-lookup"><span data-stu-id="b15b5-119">A pointer to the output buffer.</span></span>
<span data-ttu-id="b15b5-120">Dieser Parameter wird für diesen Vorgang nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="b15b5-120">This parameter is unused for this operation.</span></span>

### <a name="cboutbuffer"></a><span data-ttu-id="b15b5-121">cboutbuffer</span><span class="sxs-lookup"><span data-stu-id="b15b5-121">cbOutBuffer</span></span>

<span data-ttu-id="b15b5-122">Die Größe des Ausgabepuffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="b15b5-122">The size, in bytes, of the output buffer.</span></span>
<span data-ttu-id="b15b5-123">Dieser Parameter muss auf 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="b15b5-123">This parameter must be set to zero.</span></span>

### <a name="lpcbbytesreturned"></a><span data-ttu-id="b15b5-124">lpcbbyteszurück gegeben</span><span class="sxs-lookup"><span data-stu-id="b15b5-124">lpcbBytesReturned</span></span>

<span data-ttu-id="b15b5-125">Ein Zeiger auf eine Variable, die die Größe der im Ausgabepuffer gespeicherten Daten (in Bytes) empfängt.</span><span class="sxs-lookup"><span data-stu-id="b15b5-125">A pointer to a variable that receives the size, in bytes, of the data stored in the output buffer.</span></span>

<span data-ttu-id="b15b5-126">Wenn der Ausgabepuffer zu klein ist, schlägt der-Befehl fehl, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) gibt [**WSAEINVAL**](windows-sockets-error-codes-2.md)zurück, und der *lpcbbytesreturns* -Parameter verweist auf den **DWORD** -Wert 0 (null).</span><span class="sxs-lookup"><span data-stu-id="b15b5-126">If the output buffer is too small, the call fails, [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) returns [**WSAEINVAL**](windows-sockets-error-codes-2.md), and the *lpcbBytesReturned* parameter points to a **DWORD** value of zero.</span></span>

<span data-ttu-id="b15b5-127">Wenn *lpoverlgetauscht* gleich **null** ist, kann der **DWORD** -Wert, auf den der *lpcbbytesall* -Parameter verweist, der bei einem erfolgreichen-Vorgang zurückgegeben wird, nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="b15b5-127">If *lpOverlapped* is **NULL**, the **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned on a successful call cannot be zero.</span></span>

<span data-ttu-id="b15b5-128">Wenn der *lpoverllapp* -Parameter für überlappende Sockets nicht **null** ist, werden Vorgänge, die nicht sofort abgeschlossen werden können, initiiert, und der Abschluss wird zu einem späteren Zeitpunkt angegeben.</span><span class="sxs-lookup"><span data-stu-id="b15b5-128">If the *lpOverlapped* parameter is not **NULL** for overlapped sockets, operations that cannot be completed immediately will be initiated, and completion will be indicated at a later time.</span></span>
<span data-ttu-id="b15b5-129">Der **DWORD** -Wert, auf den der zurückgegebene *lpcbbyteszurück gegebene* Parameter verweist, kann NULL sein, da die Größe der gespeicherten Daten erst bestimmt werden kann, wenn der überlappende Vorgang abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="b15b5-129">The **DWORD** value pointed to by the *lpcbBytesReturned* parameter that is returned may be zero since the size of the data stored can't be determined until the overlapped operation has completed.</span></span>
<span data-ttu-id="b15b5-130">Der endgültige Abschluss Status kann abgerufen werden, wenn die geeignete Vervollständigungs Methode signalisiert wird, wenn der Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="b15b5-130">The final completion status can be retrieved when the appropriate completion method is signaled when the operation has completed.</span></span>

### <a name="lpvoverlapped"></a><span data-ttu-id="b15b5-131">lpvoverlgetauscht</span><span class="sxs-lookup"><span data-stu-id="b15b5-131">lpvOverlapped</span></span>

<span data-ttu-id="b15b5-132">Ein Zeiger auf eine [**wsaoverllapp**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="b15b5-132">A pointer to a [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="b15b5-133">Wenn Socket *s* ohne das überlappende Attribut erstellt wurde, wird der *lpoverllapp* -Parameter ignoriert.</span><span class="sxs-lookup"><span data-stu-id="b15b5-133">If socket *s* was created without the overlapped attribute, the *lpOverlapped* parameter is ignored.</span></span>

<span data-ttu-id="b15b5-134">Wenn *s* mit dem überlappenden Attribut geöffnet wurde und der *lpoverlgetauscht* -Parameter nicht **null** ist, wird der Vorgang als überlappende (asynchrone) Operation ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b15b5-134">If *s* was opened with the overlapped attribute and the *lpOverlapped* parameter is not **NULL**, the operation is performed as an overlapped (asynchronous) operation.</span></span>
<span data-ttu-id="b15b5-135">In diesem Fall muss der *lpoverllapp* -Parameter auf eine gültige [**wsaoverllapp**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) -Struktur zeigen.</span><span class="sxs-lookup"><span data-stu-id="b15b5-135">In this case, *lpOverlapped* parameter must point to a valid [**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) structure.</span></span>

<span data-ttu-id="b15b5-136">Bei überlappenden Vorgängen gibt die Funktion [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) oder **wspioctl** sofort zurück, und die entsprechende Vervollständigungs Methode wird signalisiert, wenn der Vorgang abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="b15b5-136">For overlapped operations, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns immediately, and the appropriate completion method is signaled when the operation has been completed.</span></span>
<span data-ttu-id="b15b5-137">Andernfalls gibt die Funktion nicht zurück, bis der Vorgang abgeschlossen ist oder ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="b15b5-137">Otherwise, the function does not return until the operation has been completed or an error occurs.</span></span>

### <a name="lpcompletionroutine"></a><span data-ttu-id="b15b5-138">lpCompletionRoutine</span><span class="sxs-lookup"><span data-stu-id="b15b5-138">lpCompletionRoutine</span></span>

<span data-ttu-id="b15b5-139">Typ: \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span><span class="sxs-lookup"><span data-stu-id="b15b5-139">Type: \_In_opt\_ [**LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)</span></span>

<span data-ttu-id="b15b5-140">Ein Zeiger auf die Vervollständigungs Routine, die aufgerufen wird, wenn der Vorgang abgeschlossen wurde (bei nicht überlappenden Sockets ignoriert).</span><span class="sxs-lookup"><span data-stu-id="b15b5-140">A pointer to the completion routine called when the operation has been completed (ignored for non-overlapped sockets).</span></span>

### <a name="lpthreadid"></a><span data-ttu-id="b15b5-141">lpthreadid</span><span class="sxs-lookup"><span data-stu-id="b15b5-141">lpThreadId</span></span>

<span data-ttu-id="b15b5-142">Ein Zeiger auf eine [**wsathreadid**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) -Struktur, die vom Anbieter in einem nachfolgenden [**wpuqueueapc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc)-Rückruf verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b15b5-142">A pointer to a [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure to be used by the provider in a subsequent call to [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc).</span></span>
<span data-ttu-id="b15b5-143">Der Anbieter sollte die referenzierte [**wsathreadid**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) -Struktur (nicht den Zeiger auf dieselbe) speichern, bis die [**wpuqueueapc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) -Funktion zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="b15b5-143">The provider should store the referenced [**WSATHREADID**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) structure (not the pointer to same) until after the [**WPUQueueApc**](/windows/desktop/api/ws2spi/nf-ws2spi-wpuqueueapc) function returns.</span></span>

<span data-ttu-id="b15b5-144">**Hinweis**  Dieser Parameter gilt nur für die **wspioctl** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="b15b5-144">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

### <a name="lperrno"></a><span data-ttu-id="b15b5-145">lperrno</span><span class="sxs-lookup"><span data-stu-id="b15b5-145">lpErrno</span></span>

<span data-ttu-id="b15b5-146">Ein Zeiger auf den Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="b15b5-146">A pointer to the error code.</span></span>

<span data-ttu-id="b15b5-147">**Hinweis**  Dieser Parameter gilt nur für die **wspioctl** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="b15b5-147">**Note**  This parameter applies only to the **WSPIoctl** function.</span></span>

## <a name="return-value"></a><span data-ttu-id="b15b5-148">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b15b5-148">Return value</span></span>

<span data-ttu-id="b15b5-149">Wenn der Vorgang erfolgreich abgeschlossen wird, gibt die [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) -oder **wspioctl** -Funktion NULL zurück.</span><span class="sxs-lookup"><span data-stu-id="b15b5-149">If the operation completes successfully, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns zero.</span></span>

<span data-ttu-id="b15b5-150">Wenn der Vorgang fehlschlägt oder aussteht, gibt die Funktion [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) oder **wspioctl** einen **\_ Socketfehler** zurück.</span><span class="sxs-lookup"><span data-stu-id="b15b5-150">If the operation fails or is pending, the [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) or **WSPIoctl** function returns **SOCKET\_ERROR**.</span></span>
<span data-ttu-id="b15b5-151">Um erweiterte Fehlerinformationen abzurufen, nennen Sie [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span><span class="sxs-lookup"><span data-stu-id="b15b5-151">To get extended error information, call [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>

| <span data-ttu-id="b15b5-152">Fehlercode</span><span class="sxs-lookup"><span data-stu-id="b15b5-152">Error code</span></span> | <span data-ttu-id="b15b5-153">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="b15b5-153">Meaning</span></span> |
|------------|---------|
| <span data-ttu-id="b15b5-154">**ausstehende WSA-e/a \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b15b5-154">**WSA\_IO\_PENDING**</span></span> | <span data-ttu-id="b15b5-155">Überlappende e/a-Vorgänge werden ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b15b5-155">Overlapped I/O operation is in progress.</span></span> <span data-ttu-id="b15b5-156">Dieser Wert wird zurückgegeben, wenn ein überlappende Vorgang erfolgreich initiiert wurde und die Beendigung zu einem späteren Zeitpunkt angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="b15b5-156">This value is returned if an overlapped operation was successfully initiated and completion will be indicated at a later time.</span></span> |
| <span data-ttu-id="b15b5-157">**WSA- \_ Vorgang \_ abgebrochen**</span><span class="sxs-lookup"><span data-stu-id="b15b5-157">**WSA\_OPERATION\_ABORTED**</span></span> | <span data-ttu-id="b15b5-158">Der e/a-Vorgang wurde aufgrund eines Thread Beendigungs-oder einer Anwendungsanforderung abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="b15b5-158">The I/O operation has been aborted because of either a thread exit or an application request.</span></span> <span data-ttu-id="b15b5-159">Dieser Fehler wird zurückgegeben, wenn ein über Lapp ender Vorgang aufgrund der Schließung des Sockets oder der Ausführung des **SIO_FLUSH** ioctl-Befehls abgebrochen wurde.</span><span class="sxs-lookup"><span data-stu-id="b15b5-159">This error is returned if an overlapped operation was canceled due to the closure of the socket or the execution of the **SIO_FLUSH** IOCTL command.</span></span> |
| <span data-ttu-id="b15b5-160">**WSAEACCES**</span><span class="sxs-lookup"><span data-stu-id="b15b5-160">**WSAEACCES**</span></span> | <span data-ttu-id="b15b5-161">Es wurde versucht, auf einen Socket auf eine Weise zuzugreifen, die durch seine Zugriffsberechtigungen unzulässig ist.</span><span class="sxs-lookup"><span data-stu-id="b15b5-161">An attempt was made to access a socket in a way forbidden by its access permissions.</span></span> <span data-ttu-id="b15b5-162">Dieser Fehler wird unter mehreren Bedingungen zurückgegeben, die Folgendes umfassen: dem Benutzer fehlen die erforderlichen Administratorrechte auf dem lokalen Computer, oder die Anwendung wird nicht in einer erweiterten Shell als integrierter Administrator () ausgeführt `RunAs administrator` .</span><span class="sxs-lookup"><span data-stu-id="b15b5-162">This error is returned under several conditions that include the following: the user lacks the required administrative privileges on the local computer or the application is not running in an enhanced shell as the built-in Administrator (`RunAs administrator`).</span></span> |
| <span data-ttu-id="b15b5-163">**WSAEFAULT**</span><span class="sxs-lookup"><span data-stu-id="b15b5-163">**WSAEFAULT**</span></span> | <span data-ttu-id="b15b5-164">Das System hat bei dem Versuch, ein Zeigerargument in einem-Befehl zu verwenden, eine ungültige Zeiger Adresse erkannt.</span><span class="sxs-lookup"><span data-stu-id="b15b5-164">The system detected an invalid pointer address in attempting to use a pointer argument in a call.</span></span> <span data-ttu-id="b15b5-165">Dieser Fehler wird zurückgegeben, wenn der Parameter *lpvinbuffer*, *lpvoutbuffer*, *lpcbbytesall*, *lpoverlgetauscht* oder *lpCompletionRoutine* nicht vollständig in einem gültigen Teil des Benutzer Adressraums enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="b15b5-165">This error is returned of the *lpvInBuffer*, *lpvoutBuffer*, *lpcbBytesReturned*, *lpOverlapped* or *lpCompletionRoutine* parameter is not totally contained in a valid part of the user address space.</span></span> |
| <span data-ttu-id="b15b5-166">**Wsaeingabe Progress**</span><span class="sxs-lookup"><span data-stu-id="b15b5-166">**WSAEINPROGRESS**</span></span> | <span data-ttu-id="b15b5-167">Ein Blockierungsvorgang wird momentan ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b15b5-167">A blocking operation is currently executing.</span></span> <span data-ttu-id="b15b5-168">Dieser Fehler wird zurückgegeben, wenn die Funktion aufgerufen wird, wenn ein Rückruf ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b15b5-168">This error is returned if the function is invoked when a callback is in progress.</span></span> |
| <span data-ttu-id="b15b5-169">**Wsaeingabe**</span><span class="sxs-lookup"><span data-stu-id="b15b5-169">**WSAEINTR**</span></span> | <span data-ttu-id="b15b5-170">Ein Blockierungs Vorgang wurde durch einen **wsacancelblockingstatement**-Aufrufvorgang unterbrochen.</span><span class="sxs-lookup"><span data-stu-id="b15b5-170">A blocking operation was interrupted by a call to **WSACancelBlockingCall**.</span></span> <span data-ttu-id="b15b5-171">Dieser Fehler wird zurückgegeben, wenn ein Blockierungs Vorgang unterbrochen wurde.</span><span class="sxs-lookup"><span data-stu-id="b15b5-171">This error is returned if a blocking operation was interrupted.</span></span> |
| <span data-ttu-id="b15b5-172">**Wsaabval**</span><span class="sxs-lookup"><span data-stu-id="b15b5-172">**WSAEINVAL**</span></span> | <span data-ttu-id="b15b5-173">Ein ungültiges Argument wurde angegeben.</span><span class="sxs-lookup"><span data-stu-id="b15b5-173">An invalid argument was supplied.</span></span> <span data-ttu-id="b15b5-174">Dieser Fehler wird zurückgegeben, wenn der *dwIoControlCode* -Parameter kein gültiger Befehl ist oder wenn ein angegebener Eingabeparameter nicht zulässig ist oder der Befehl nicht auf den angegebenen Sockettyp anwendbar ist.</span><span class="sxs-lookup"><span data-stu-id="b15b5-174">This error is returned if the *dwIoControlCode* parameter is not a valid command, or a specified input parameter is not acceptable, or the command is not applicable to the type of socket specified.</span></span> |
| <span data-ttu-id="b15b5-175">**WSAENETDOWN**</span><span class="sxs-lookup"><span data-stu-id="b15b5-175">**WSAENETDOWN**</span></span> | <span data-ttu-id="b15b5-176">Bei einem Socketvorgang war das Netzwerk inaktiv.</span><span class="sxs-lookup"><span data-stu-id="b15b5-176">A socket operation encountered a dead network.</span></span> <span data-ttu-id="b15b5-177">Dieser Fehler wird zurückgegeben, wenn das Netzwerk Subsystem fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="b15b5-177">This error is returned if the network subsystem has failed.</span></span> |
| <span data-ttu-id="b15b5-178">**Wsaumotsock**</span><span class="sxs-lookup"><span data-stu-id="b15b5-178">**WSAENOTSOCK**</span></span> | <span data-ttu-id="b15b5-179">Es wurde versucht, einen Vorgang für etwas auszuführen, das kein Socket ist.</span><span class="sxs-lookup"><span data-stu-id="b15b5-179">An operation was attempted on something that is not a socket.</span></span> <span data-ttu-id="b15b5-180">Dieser Fehler wird zurückgegeben, wenn es sich bei den *Deskriptoren nicht* um einen Socket handelt.</span><span class="sxs-lookup"><span data-stu-id="b15b5-180">This error is returned if the descriptor *s* is not a socket.</span></span> |
| <span data-ttu-id="b15b5-181">**WSAEOPNOTSUPP**</span><span class="sxs-lookup"><span data-stu-id="b15b5-181">**WSAEOPNOTSUPP**</span></span> | <span data-ttu-id="b15b5-182">Der versuchte Vorgang wird für den Typ des Objekts, auf das verwiesen wird, nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b15b5-182">The attempted operation is not supported for the type of object referenced.</span></span> <span data-ttu-id="b15b5-183">Dieser Fehler wird zurückgegeben, wenn der angegebene ioctl-Befehl nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="b15b5-183">This error is returned if the specified IOCTL command is not supported.</span></span> <span data-ttu-id="b15b5-184">Dieser Fehler wird auch zurückgegeben, wenn die **\_ \_ \_ \_ \_ Datensätze der WFP-Verbindungs Umleitung** von der Gruppe "ioctl" vom Transportanbieter nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="b15b5-184">This error is also returned if the **SIO\_SET\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL is not supported by the transport provider.</span></span> |

## <a name="remarks"></a><span data-ttu-id="b15b5-185">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b15b5-185">Remarks</span></span>

<span data-ttu-id="b15b5-186">Die **\_ \_ \_ \_ \_ Datensätze der WFP-Verbindungs Umleitung** werden von Windows 8, Windows Server 2012 und neueren Versionen des Betriebssystems unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b15b5-186">The **SIO\_SET\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL is supported on Windows 8, and Windows Server 2012, and later versions of the operating system.</span></span>

<span data-ttu-id="b15b5-187">WFP ermöglicht den Zugriff auf den TCP/IP-Paket Verarbeitungs Pfad, in dem ausgehende und eingehende Pakete überprüft oder geändert werden können, bevor Sie weiterverarbeitet werden können.</span><span class="sxs-lookup"><span data-stu-id="b15b5-187">WFP allows access to the TCP/IP packet processing path, wherein outgoing and incoming packets can be examined or changed before allowing them to be processed further.</span></span>
<span data-ttu-id="b15b5-188">Durch das Tippen auf den TCP/IP-Verarbeitungs Pfad können unabhängige Softwarehersteller (ISVs) leichter Firewalls, Antivirussoftware, Diagnosesoftware und andere Arten von Anwendungen und Diensten erstellen.</span><span class="sxs-lookup"><span data-stu-id="b15b5-188">By tapping into the TCP/IP processing path, independent software vendors (ISVs) can more easily create firewalls, antivirus software, diagnostic software, and other types of applications and services.</span></span>
<span data-ttu-id="b15b5-189">WFP stellt Komponenten im Benutzermodus und im Kernel Modus bereit, sodass Drittanbieter-ISVs an den Filter Entscheidungen teilnehmen können, die auf mehreren Ebenen im TCP/IP-Protokollstapel und im gesamten Betriebssystem stattfinden.</span><span class="sxs-lookup"><span data-stu-id="b15b5-189">WFP provides user-mode and kernel-mode components so that third-party ISVs can participate in the filtering decisions that take place at several layers in the TCP/IP protocol stack and throughout the operating system.</span></span>
<span data-ttu-id="b15b5-190">Mithilfe des WFP-Verbindungs Umleitungs Features kann ein WFP-Legenden-Kernel-Treiber eine Verbindung lokal an einen Benutzermodusprozess umleiten, eine Inhalts Untersuchung im Benutzermodus durchführen und den überprüften Inhalt mithilfe einer anderen Verbindung zum ursprünglichen Ziel weiterleiten.</span><span class="sxs-lookup"><span data-stu-id="b15b5-190">The WFP connection redirect feature allows a WFP callout kernel driver to redirect a connection locally to a user-mode process, perform content inspection in user-mode, and forward the inspected content using a different connection to the original destination.</span></span>

<span data-ttu-id="b15b5-191">Die **Datensätze der WFP-Verbindungs Umleitung werden von der Datei "ioctl" und mehrere andere verwandte IOCTLs- \_ \_ \_ \_ \_ Datensätze erfasst** . Diese werden verwendet, um mehreren WFP-basierten Verbindungs Proxy Anwendungen zu ermöglichen, denselben Daten Verkehrsfluss auf kooperative Weise zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="b15b5-191">The **SIO\_SET\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL and several other related IOCTLS are user-mode components used to allow multiple WFP-based connection proxy applications to inspect the same traffic flow in a cooperative manner.</span></span>
<span data-ttu-id="b15b5-192">Jeder Inspektions Agent kann den Netzwerk Datenverkehr, der bereits von einem anderen Inspektions Agent überprüft wurde, sicher erneut überprüfen.</span><span class="sxs-lookup"><span data-stu-id="b15b5-192">Each inspection agent can safely re-inspect network traffic that has already been inspected by another inspection agent.</span></span>
<span data-ttu-id="b15b5-193">Durch das vorhanden sein mehrerer Proxys (z. b. durch verschiedene ISVs) kann die Verbindung, die von einem Proxy für die Kommunikation mit dem endgültigen Ziel verwendet wird, wiederum von einem zweiten Proxy umgeleitet werden, und diese neue Verbindung kann erneut vom ursprünglichen Proxy umgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="b15b5-193">With the presence of multiple proxies (developed by different ISVs, for example) the connection used by one proxy to communicate with the final destination could in turn be redirected by a second proxy, and that new connection could again be redirected by the original proxy.</span></span>
<span data-ttu-id="b15b5-194">Ohne Verbindungs Nachverfolgung erreicht die ursprüngliche Verbindung möglicherweise nie das endgültige Ziel, weil Sie in einer unendlichen Proxy Schleife hängen bleibt.</span><span class="sxs-lookup"><span data-stu-id="b15b5-194">Without connection tracking, the original connection might never reach its final destination as it gets stuck in an infinite proxy loop.</span></span>

<span data-ttu-id="b15b5-195">Die **\_ \_ \_ \_ \_ Datensätze der WFP-Verbindungs Umleitung** in der Gruppe "ioctl" werden mithilfe von "ioctl" für die Verbindungs Protokollierung über umgeleitet</span><span class="sxs-lookup"><span data-stu-id="b15b5-195">The **SIO\_SET\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL is used to provide proxied connection tracking on redirected socket connections.</span></span>
<span data-ttu-id="b15b5-196">Diese WFP-Funktion ermöglicht das Nachverfolgen von Umleitungs Datensätzen von der anfänglichen Umleitung einer Verbindung zur endgültigen Verbindung zum Ziel.</span><span class="sxs-lookup"><span data-stu-id="b15b5-196">This WFP feature facilitates tracking of redirection records from the initial redirect of a connection to the final connection to the destination.</span></span>

<span data-ttu-id="b15b5-197">Der [**SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS**](sio-query-wfp-connection-redirect-records.md) IOCTL wird von einem WFP-basierten Umleitungs Dienst verwendet, um den Umleitungs Daten Satz von der akzeptierten TCP/IP-Paket Verbindung abzurufen (z. b. den verbundenen Socket für einen TCP-Socket oder einen UDP-Socket), der durch seine begleitende kernelmoduslegende, die bei der  **ALE \_ Connect- \_ Umleitungs** Schicht in einem Kernelmodustreiber</span><span class="sxs-lookup"><span data-stu-id="b15b5-197">The [**SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS**](sio-query-wfp-connection-redirect-records.md) IOCTL is used by a WFP-based redirect service to retrieve the redirect record from the accepted TCP/IP packet connection (the connected socket for a TCP socket or a UDP socket, for example) redirected to it by its companion kernel-mode callout registered at  **ALE\_CONNECT\_REDIRECT** layers in a kernel-mode driver.</span></span>
<span data-ttu-id="b15b5-198">Der [**SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT**](sio-query-wfp-connection-redirect-context.md) ioctl Ruft den Umleitungs Kontext für einen Umleitungs Daten Satz ab, der verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b15b5-198">The [**SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT**](sio-query-wfp-connection-redirect-context.md) IOCTL retrieves the redirect context for a redirect record, which is used.</span></span>
<span data-ttu-id="b15b5-199">Der Umleitungs Kontext ist optional und wird verwendet, wenn der aktuelle Umleitungs Status einer Verbindung darin besteht, dass die Verbindung vom aufrufenden Umleitungs Dienst umgeleitet wurde oder die Verbindung zuvor vom aufrufenden Umleitungs Dienst umgeleitet, aber später von einem anderen Umleitungs Dienst umgeleitet wurde. Der Umleitungs Dienst überträgt den abgerufenen Umleitungs Daten Satz an den TCP-Socket, den er zum Proxy des ursprünglichen Inhalts verwendet, indem er die IOCTL- **\_ \_ \_ Verbindungs \_ \_ Datensätze der WFP-Verbindung** verwendet</span><span class="sxs-lookup"><span data-stu-id="b15b5-199">The redirect context is optional and is used if the current redirection state of a connection is that the connection was redirected by the calling redirect service or the connection was previously redirected by the calling redirect service but later redirected again by a different redirect service.The redirect service transfers the retrieved redirect record to the TCP socket it uses to proxy the original content using the **SIO\_SET\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL.</span></span>

<span data-ttu-id="b15b5-200">Die Anwendung, die **die \_ \_ \_ \_ \_ Datensätze für die WFP-Verbindungs Umleitung des Daten** Satzes "moctl" aufrufen, muss das BLOB mit dem festgelegten Umleitungs Daten Satz nicht verstehen.</span><span class="sxs-lookup"><span data-stu-id="b15b5-200">The application calling the **SIO\_SET\_WFP\_CONNECTION\_REDIRECT\_RECORDS** IOCTL does not need to understand the blob containing the redirect record being set.</span></span>
<span data-ttu-id="b15b5-201">Hierbei handelt es sich um ein nicht transparentes BLOB von Daten, die die Anwendung an den neuen Socket zurückgeben muss.</span><span class="sxs-lookup"><span data-stu-id="b15b5-201">This is an opaque blob of data that the application needs to pass back to the new socket.</span></span>

## <a name="see-also"></a><span data-ttu-id="b15b5-202">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b15b5-202">See also</span></span>

[<span data-ttu-id="b15b5-203">**IPPROTO_IP Socketoptionen**</span><span class="sxs-lookup"><span data-stu-id="b15b5-203">**IPPROTO_IP Socket Options**</span></span>](/windows/desktop/winsock/ipproto-ip-socket-options)

[<span data-ttu-id="b15b5-204">**SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT**</span><span class="sxs-lookup"><span data-stu-id="b15b5-204">**SIO_QUERY_WFP_CONNECTION_REDIRECT_CONTEXT**</span></span>](sio-query-wfp-connection-redirect-context.md)

[<span data-ttu-id="b15b5-205">**SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS**</span><span class="sxs-lookup"><span data-stu-id="b15b5-205">**SIO_QUERY_WFP_CONNECTION_REDIRECT_RECORDS**</span></span>](sio-query-wfp-connection-redirect-records.md)

[<span data-ttu-id="b15b5-206">**Glühbirne**</span><span class="sxs-lookup"><span data-stu-id="b15b5-206">**socket**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-socket)

[<span data-ttu-id="b15b5-207">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="b15b5-207">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetlasterror)

[<span data-ttu-id="b15b5-208">**Wsagein verlappedresult**</span><span class="sxs-lookup"><span data-stu-id="b15b5-208">**WSAGetOverlappedResult**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[<span data-ttu-id="b15b5-209">**WSAIoctl**</span><span class="sxs-lookup"><span data-stu-id="b15b5-209">**WSAIoctl**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[<span data-ttu-id="b15b5-210">**Wsaoverlgetauscht**</span><span class="sxs-lookup"><span data-stu-id="b15b5-210">**WSAOVERLAPPED**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[<span data-ttu-id="b15b5-211">**Wsasocketa**</span><span class="sxs-lookup"><span data-stu-id="b15b5-211">**WSASocketA**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[<span data-ttu-id="b15b5-212">**Wsasocketw**</span><span class="sxs-lookup"><span data-stu-id="b15b5-212">**WSASocketW**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
