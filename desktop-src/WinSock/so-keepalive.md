---
description: Ermöglicht es einer Anwendung, Keep-Alive-Pakete für eine Socketverbindung zu aktivieren.
ms.assetid: d6da7761-7a09-4c91-9737-550590a773b3
title: SO_KEEPALIVE Socket-Option (Ws2def. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d829f957e23c48a325444de7d992397fba26d48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359210"
---
# <a name="so_keepalive-socket-option"></a><span data-ttu-id="cce93-103">\_KeepAlive-Socketoption</span><span class="sxs-lookup"><span data-stu-id="cce93-103">SO\_KEEPALIVE socket option</span></span>

<span data-ttu-id="cce93-104">Die Option " **so \_ KeepAlive** Socket" ermöglicht es einer Anwendung, Keep-Alive-Pakete für eine Socketverbindung zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="cce93-104">The **SO\_KEEPALIVE** socket option is designed to allow an application to enable keep-alive packets for a socket connection.</span></span>

<span data-ttu-id="cce93-105">Um den Status dieser Socketoption abzufragen, müssen Sie die [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="cce93-105">To query the status of this socket option, call the [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) function.</span></span> <span data-ttu-id="cce93-106">Um diese Option festzulegen, müssen Sie die Funktion [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) mit den folgenden Parametern aufrufen.</span><span class="sxs-lookup"><span data-stu-id="cce93-106">To set this option, call the [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function with the following parameters.</span></span>

## <a name="socket-option-value"></a><span data-ttu-id="cce93-107">Wert der Socketoption</span><span class="sxs-lookup"><span data-stu-id="cce93-107">Socket option value</span></span>

<span data-ttu-id="cce93-108">Die Konstante, die diese Socketoption darstellt, ist 0x0008.</span><span class="sxs-lookup"><span data-stu-id="cce93-108">The constant that represents this socket option is 0x0008.</span></span>

## <a name="syntax"></a><span data-ttu-id="cce93-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="cce93-109">Syntax</span></span>


```C++
int getsockopt(
  (SOCKET) s,      // descriptor identifying a socket 
  (int) SOL_SOCKET,   // level
  (int) SO_KEEPALIVE, // optname
  (char *) optval, // output buffer,
  (int) optlen,  // size of output buffer
);
```




```C++
int setsockopt(
  (SOCKET) s,      // descriptor identifying a socket 
  (int) SOL_SOCKET,   // level
  (int) SO_KEEPALIVE, // optname
  (char *) optval, // input buffer,
  (int) optlen,  // size of input buffer
);
```



## <a name="parameters"></a><span data-ttu-id="cce93-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="cce93-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cce93-111">*s* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cce93-111">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cce93-112">Ein Deskriptor, der den Socket identifiziert.</span><span class="sxs-lookup"><span data-stu-id="cce93-112">A descriptor identifying the socket.</span></span>

</dd> <dt>

<span data-ttu-id="cce93-113">*Ebene* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cce93-113">*level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cce93-114">Die Ebene, auf der die Option definiert ist.</span><span class="sxs-lookup"><span data-stu-id="cce93-114">The level at which the option is defined.</span></span> <span data-ttu-id="cce93-115">Verwenden Sie für diesen Vorgang den **Sol- \_ Socket** .</span><span class="sxs-lookup"><span data-stu-id="cce93-115">Use **SOL\_SOCKET** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="cce93-116">*optname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cce93-116">*optname* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cce93-117">Die Socketoption, für die der Wert festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="cce93-117">The socket option for which the value is to be set.</span></span> <span data-ttu-id="cce93-118">Verwenden Sie " **\_ KeepAlive** " für diesen Vorgang.</span><span class="sxs-lookup"><span data-stu-id="cce93-118">Use **SO\_KEEPALIVE** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="cce93-119">*optval* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="cce93-119">*optval* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cce93-120">Ein Zeiger auf den Puffer, der den Wert für die festzulegende Option enthält.</span><span class="sxs-lookup"><span data-stu-id="cce93-120">A pointer to the buffer containing the value for the option to set.</span></span> <span data-ttu-id="cce93-121">Dieser Parameter sollte auf einen Puffer zeigen, der größer oder gleich der Größe eines **DWORD** -Werts ist.</span><span class="sxs-lookup"><span data-stu-id="cce93-121">This parameter should point to buffer equal to or larger than the size of a **DWORD** value.</span></span>

<span data-ttu-id="cce93-122">Dieser Wert wird als boolescher Wert behandelt, wobei 0 verwendet wird, um **false** (deaktiviert) und einen Wert ungleich 0 (null) anzugeben, um **true** (aktiviert) anzugeben.</span><span class="sxs-lookup"><span data-stu-id="cce93-122">This value is treated as a boolean value with 0 used to indicate **FALSE** (disabled) and a nonzero value to indicate **TRUE** (enabled).</span></span>

</dd> <dt>

<span data-ttu-id="cce93-123">*optlen* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="cce93-123">*optlen* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="cce93-124">Ein Zeiger auf die Größe des *optval* -Puffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="cce93-124">A pointer to the size, in bytes, of the *optval* buffer.</span></span> <span data-ttu-id="cce93-125">Diese Größe muss größer oder gleich der Größe eines **DWORD** -Werts sein.</span><span class="sxs-lookup"><span data-stu-id="cce93-125">This size must be equal to or larger than the size of a **DWORD** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cce93-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cce93-126">Return value</span></span>

<span data-ttu-id="cce93-127">Wenn der Vorgang erfolgreich abgeschlossen wird, gibt [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="cce93-127">If the operation completes successfully, [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) returns zero.</span></span>

<span data-ttu-id="cce93-128">Wenn der Vorgang fehlschlägt, wird der Wert Socket \_ Error zurückgegeben, und es kann ein spezifischer Fehlercode durch Aufrufen von [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="cce93-128">If the operation fails, a value of SOCKET\_ERROR is returned and a specific error code can be retrieved by calling [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>



| <span data-ttu-id="cce93-129">Fehlercode</span><span class="sxs-lookup"><span data-stu-id="cce93-129">Error code</span></span>                                                                                                                                              | <span data-ttu-id="cce93-130">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="cce93-130">Meaning</span></span>                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="cce93-131"><dt>**[WSANOTINITIALISED](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="cce93-131"><dt>**[WSANOTINITIALISED](windows-sockets-error-codes-2.md)**</dt></span></span> </dl> | <span data-ttu-id="cce93-132">Ein erfolgreicher [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) -Befehl muss vor der Verwendung dieser Funktion ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="cce93-132">A successful [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) call must occur before using this function.</span></span><br/>                                                                                                                                                     |
| <dl> <span data-ttu-id="cce93-133"><dt>**[WSAENETDOWN](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="cce93-133"><dt>**[WSAENETDOWN](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>             | <span data-ttu-id="cce93-134">Das Netzwerk Subsystem ist fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="cce93-134">The network subsystem has failed.</span></span><br/>                                                                                                                                                                                                               |
| <dl> <span data-ttu-id="cce93-135"><dt>**[WSAEFAULT](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="cce93-135"><dt>**[WSAEFAULT](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>                 | <span data-ttu-id="cce93-136">Einer der *optval* -oder *optlen* -Parameter verweist auf den Arbeitsspeicher, der sich nicht in einem gültigen Teil des Benutzer Adressraums befindet.</span><span class="sxs-lookup"><span data-stu-id="cce93-136">One of the *optval* or the *optlen* parameters point to memory that is not in a valid part of the user address space.</span></span> <span data-ttu-id="cce93-137">Dieser Fehler wird auch zurückgegeben, wenn der Wert, auf den der *optlen* -Parameter verweist, kleiner ist als die Größe eines **DWORD** -Werts.</span><span class="sxs-lookup"><span data-stu-id="cce93-137">This error is also returned if the value pointed to by the *optlen* parameter is less than the size of a **DWORD** value.</span></span><br/> |
| <dl> <span data-ttu-id="cce93-138"><dt>**[Wsaeingabe Progress](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="cce93-138"><dt>**[WSAEINPROGRESS](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>       | <span data-ttu-id="cce93-139">Ein blockierender Windows Sockets 1,1-Rückruf wird gerade ausgeführt, oder der Dienstanbieter verarbeitet weiterhin eine Rückruffunktion.</span><span class="sxs-lookup"><span data-stu-id="cce93-139">A blocking Windows Sockets 1.1 call is in progress, or the service provider is still processing a callback function.</span></span><br/>                                                                                                                            |
| <dl> <span data-ttu-id="cce93-140"><dt>**[Wsaabval](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="cce93-140"><dt>**[WSAEINVAL](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>                 | <span data-ttu-id="cce93-141">Der *Level* -Parameter ist unbekannt oder ungültig.</span><span class="sxs-lookup"><span data-stu-id="cce93-141">The *level* parameter is unknown or invalid.</span></span> <span data-ttu-id="cce93-142">Unter Windows Vista und höher wird dieser Fehler auch zurückgegeben, wenn sich der Socket in einem Übergangszustand befunden hat.</span><span class="sxs-lookup"><span data-stu-id="cce93-142">On Windows Vista and later, this error is also returned if the socket was in a transitional state.</span></span><br/>                                                                                                 |
| <dl> <span data-ttu-id="cce93-143"><dt>**[Wsaumoproumopt](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="cce93-143"><dt>**[WSAENOPROTOOPT](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>       | <span data-ttu-id="cce93-144">Die Option ist unbekannt oder wird von der angegebener Protokollfamilie nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cce93-144">The option is unknown or unsupported by the indicated protocol family.</span></span> <span data-ttu-id="cce93-145">Dieser Fehler wird zurückgegeben, wenn der im *s* -Parameter übergebenen socketdeskriptor für einen Datagramm-Socket festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="cce93-145">This error is returned if the socket descriptor passed in the *s* parameter was for a datagram socket.</span></span><br/>                                                                   |
| <dl> <span data-ttu-id="cce93-146"><dt>**[Wsaumotsock](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="cce93-146"><dt>**[WSAENOTSOCK](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>             | <span data-ttu-id="cce93-147">Der Deskriptor ist kein Socket.</span><span class="sxs-lookup"><span data-stu-id="cce93-147">The descriptor is not a socket.</span></span><br/>                                                                                                                                                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="cce93-148">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cce93-148">Remarks</span></span>

<span data-ttu-id="cce93-149">Die [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) -Funktion, die mit der " **so \_ KeepAlive** "-Socketoption aufgerufen wird, ermöglicht es einer Anwendung, den aktuellen Zustand der KeepAlive-Option abzurufen, obwohl diese Funktion normalerweise nicht verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="cce93-149">The [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) function called with the **SO\_KEEPALIVE** socket option allows an application to retrieve the current state of the keepalive option, although this is feature not normally used.</span></span> <span data-ttu-id="cce93-150">Wenn eine Anwendung KeepAlive-Pakete für einen Socket aktivieren muss, ruft Sie die [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) -Funktion auf, um die Option zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="cce93-150">If an application needs to enable keepalive packets on a socket, it justs calls the [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function to enable the option.</span></span>

<span data-ttu-id="cce93-151">Die [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) -Funktion, die mit der Option " **so \_ KeepAlive** Socket" aufgerufen wird, ermöglicht einer Anwendung, Keep-Alive-Pakete für eine Socketverbindung zu aktivieren</span><span class="sxs-lookup"><span data-stu-id="cce93-151">The [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function called with the **SO\_KEEPALIVE** socket option allows an application to enable keep-alive packets for a socket connection.</span></span> <span data-ttu-id="cce93-152">Die Option " **so \_ KeepAlive** " für einen Socket ist standardmäßig deaktiviert (auf " **false**" festgelegt).</span><span class="sxs-lookup"><span data-stu-id="cce93-152">The **SO\_KEEPALIVE** option for a socket is disabled (set to **FALSE**) by default.</span></span>

<span data-ttu-id="cce93-153">Wenn diese Socketoption aktiviert ist, sendet der TCP-Stapel Keep-Alive-Pakete, wenn für die Verbindung innerhalb eines Intervalls keine Daten oder Bestätigungs Pakete empfangen wurden.</span><span class="sxs-lookup"><span data-stu-id="cce93-153">When this socket option is enabled, the TCP stack sends keep-alive packets when no data or acknowledgement packets have been received for the connection within an interval.</span></span> <span data-ttu-id="cce93-154">Weitere Informationen zur Keep-Alive-Option finden Sie im Abschnitt 4.2.3.6 zu den *Anforderungen für Internet Hosts –* in RFC 1122 angegebene Kommunikations Schichten auf der [IETF-Website](https://www.ietf.org/rfc/rfc1122.txt).</span><span class="sxs-lookup"><span data-stu-id="cce93-154">For more information on the keep-alive option, see section 4.2.3.6 on the *Requirements for Internet Hosts—Communication Layers* specified in RFC 1122 available at the [IETF website](https://www.ietf.org/rfc/rfc1122.txt).</span></span> <span data-ttu-id="cce93-155">(Diese Ressource ist möglicherweise nur in englischer Sprache verfügbar.)</span><span class="sxs-lookup"><span data-stu-id="cce93-155">(This resource may only be available in English.)</span></span>

<span data-ttu-id="cce93-156">Die Option " **so \_ KeepAlive** Socket" ist nur für Protokolle gültig, die das Konzept von Keep-Alive (Verbindungs orientierte Protokolle) unterstützen.</span><span class="sxs-lookup"><span data-stu-id="cce93-156">The **SO\_KEEPALIVE** socket option is valid only for protocols that support the notion of keep-alive (connection-oriented protocols).</span></span> <span data-ttu-id="cce93-157">Bei TCP beträgt das standardmäßige Keep-Alive-Timeout 2 Stunden, und das Keep-Alive-Intervall beträgt 1 Sekunde.</span><span class="sxs-lookup"><span data-stu-id="cce93-157">For TCP, the default keep-alive timeout is 2 hours and the keep-alive interval is 1 second.</span></span> <span data-ttu-id="cce93-158">Die Standard Anzahl von Keep-Alive-Tests variiert abhängig von der Windows-Version.</span><span class="sxs-lookup"><span data-stu-id="cce93-158">The default number of keep-alive probes varies based on the version of Windows.</span></span>

<span data-ttu-id="cce93-159">Der " [**SIO \_ KeepAlive \_ Vals**](/previous-versions/windows/desktop/legacy/dd877220(v=vs.85)) "-Steuerungs Code kann verwendet werden, um Keep-Alive zu aktivieren bzw. zu deaktivieren und den Timeout und das Intervall für eine einzelne Verbindung anzupassen.</span><span class="sxs-lookup"><span data-stu-id="cce93-159">The [**SIO\_KEEPALIVE\_VALS**](/previous-versions/windows/desktop/legacy/dd877220(v=vs.85)) control code can be used to enable or disable keep-alive, and adjust the timeout and interval, for a single connection.</span></span> <span data-ttu-id="cce93-160">Wenn Keep-Alive mit " **so \_ KeepAlive**" aktiviert ist, werden die TCP-Standardeinstellungen für Keep-Alive-Timeout und-Intervall verwendet, es sei denn, diese Werte wurden mithilfe von " **SIO \_ KeepAlive \_ Vals**" geändert.</span><span class="sxs-lookup"><span data-stu-id="cce93-160">If keep-alive is enabled with **SO\_KEEPALIVE**, then the default TCP settings are used for keep-alive timeout and interval unless these values have been changed using **SIO\_KEEPALIVE\_VALS**.</span></span>

<span data-ttu-id="cce93-161">Der standardmäßige systemweite Wert des Keep-Alive-Timeouts ist über die [KeepAliveTime](/previous-versions/windows/it-pro/windows-server-2003/cc782936(v=ws.10)) -Registrierungs Einstellung steuerbar, die einen Wert in Millisekunden annimmt.</span><span class="sxs-lookup"><span data-stu-id="cce93-161">The default system-wide value of the keep-alive timeout is controllable through the [KeepAliveTime](/previous-versions/windows/it-pro/windows-server-2003/cc782936(v=ws.10)) registry setting which takes a value in milliseconds.</span></span> <span data-ttu-id="cce93-162">Der standardmäßige systemweite Wert des Keep-Alive-Intervalls kann durch die [keepAliveInterval](/previous-versions/windows/it-pro/windows-server-2003/cc758083(v=ws.10)) -Registrierungs Einstellung gesteuert werden, die einen Wert in Millisekunden annimmt.</span><span class="sxs-lookup"><span data-stu-id="cce93-162">The default system-wide value of the keep-alive interval is controllable through the [KeepAliveInterval](/previous-versions/windows/it-pro/windows-server-2003/cc758083(v=ws.10)) registry setting which takes a value in milliseconds.</span></span>

<span data-ttu-id="cce93-163">Unter Windows Vista und höher wird die Anzahl von Keep-Alive-Tests (Neuübertragungen von Daten) auf 10 festgelegt und kann nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="cce93-163">On Windows Vista and later, the number of keep-alive probes (data retransmissions) is set to 10 and cannot be changed.</span></span>

<span data-ttu-id="cce93-164">Unter Windows Server 2003, Windows XP und Windows 2000 ist die Standardeinstellung für die Anzahl von Keep-Alive-Tests 5.</span><span class="sxs-lookup"><span data-stu-id="cce93-164">On Windows Server 2003, Windows XP, and Windows 2000, the default setting for number of keep-alive probes is 5.</span></span> <span data-ttu-id="cce93-165">Die Anzahl der Keep-Alive-Tests ist über die Registrierungs Einstellungen [TcpMaxDataRetransmissions](/previous-versions/windows/it-pro/windows-server-2003/cc780586(v=ws.10)) und [pptptcpmaxdataretransmissions](/previous-versions/windows/it-pro/windows-server-2003/cc775408(v=ws.10)) steuerbar.</span><span class="sxs-lookup"><span data-stu-id="cce93-165">The number of keep-alive probes is controllable through the [TcpMaxDataRetransmissions](/previous-versions/windows/it-pro/windows-server-2003/cc780586(v=ws.10)) and [PPTPTcpMaxDataRetransmissions](/previous-versions/windows/it-pro/windows-server-2003/cc775408(v=ws.10)) registry settings.</span></span> <span data-ttu-id="cce93-166">Die Anzahl der Keep-Alive-Tests wird auf den größeren der beiden Registrierungsschlüssel Werte festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cce93-166">The number of keep-alive probes is set to the larger of the two registry key values.</span></span> <span data-ttu-id="cce93-167">Wenn diese Zahl 0 ist, werden Keep-Alive-Tests nicht gesendet.</span><span class="sxs-lookup"><span data-stu-id="cce93-167">If this number is 0, then keep-alive probes will not be sent.</span></span> <span data-ttu-id="cce93-168">Wenn diese Zahl über 255 liegt, wird Sie an 255 angepasst.</span><span class="sxs-lookup"><span data-stu-id="cce93-168">If this number is above 255, then it is adjusted to 255.</span></span>

<span data-ttu-id="cce93-169">Unter Windows Vista und höher kann die Option " **so \_ KeepAlive** Socket" nur mithilfe der Funktion " [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) " festgelegt werden, wenn sich der Socket in einem bekannten Zustand befindet, der kein Übergangszustand ist.</span><span class="sxs-lookup"><span data-stu-id="cce93-169">On Windows Vista and later, the **SO\_KEEPALIVE** socket option can only be set using the [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function when the socket is in a well-known state not a transitional state.</span></span> <span data-ttu-id="cce93-170">Für TCP muss die Option " **so \_ KeepAlive** Socket" festgelegt werden, bevor die Connect-Funktion ("[**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect)", " [**connectex**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex)", " [**wsaconnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect)", " [**wsaconnectbylist**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist)" oder " [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea)") aufgerufen wird, oder nachdem die Verbindungsanforderung tatsächlich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="cce93-170">For TCP, the **SO\_KEEPALIVE** socket option should be set either before the connect function ([**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect), [**ConnectEx**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex), [**WSAConnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect), [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist), or [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea)) is called, or after the connection request is actually completed.</span></span> <span data-ttu-id="cce93-171">Wenn die Connect-Funktion asynchron aufgerufen wurde, erfordert dies das warten auf den Abschluss der Verbindung, bevor versucht wird, die Option " **so \_ KeepAlive** Socket" festzulegen.</span><span class="sxs-lookup"><span data-stu-id="cce93-171">If the connect function was called asynchronously, then this requires waiting for the connection completion before trying to set the **SO\_KEEPALIVE** socket option.</span></span> <span data-ttu-id="cce93-172">Wenn eine Anwendung versucht, die Option " **so \_ KeepAlive** Socket" festzulegen, wenn eine Verbindungsanforderung noch verarbeitet wird, schlägt die Funktion " **setsockopt** " fehl und gibt " [WSAEINVAL](windows-sockets-error-codes-2.md)" zurück.</span><span class="sxs-lookup"><span data-stu-id="cce93-172">If an application attempts to set the **SO\_KEEPALIVE** socket option when a connection request is still in process, the **setsockopt** function will fail and return [WSAEINVAL](windows-sockets-error-codes-2.md).</span></span>

<span data-ttu-id="cce93-173">Unter Windows Server 2003, Windows XP und Windows 2000 kann die Option " **so \_ KeepAlive** Socket" mithilfe der Funktion " [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) " festgelegt werden, wenn der Socket ein Übergangszustand ist (eine Verbindungsanforderung wird noch ausgeführt), sowie ein bekannter Zustand.</span><span class="sxs-lookup"><span data-stu-id="cce93-173">On Windows Server 2003, Windows XP, and Windows 2000, the **SO\_KEEPALIVE** socket option can be set using the [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function when the socket is a transitional state (a connection request is still in progress) as well as a well-known state.</span></span>

<span data-ttu-id="cce93-174">Beachten Sie, dass die Header Datei " *Ws2def. h* " automatisch in " *Winsock2. h*" enthalten ist und niemals direkt verwendet werden sollte.</span><span class="sxs-lookup"><span data-stu-id="cce93-174">Note that the *Ws2def.h* header file is automatically included in *Winsock2.h*, and should never be used directly.</span></span>

## <a name="requirements"></a><span data-ttu-id="cce93-175">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cce93-175">Requirements</span></span>



| <span data-ttu-id="cce93-176">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cce93-176">Requirement</span></span> | <span data-ttu-id="cce93-177">Wert</span><span class="sxs-lookup"><span data-stu-id="cce93-177">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cce93-178">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cce93-178">Minimum supported client</span></span><br/> | <span data-ttu-id="cce93-179">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cce93-179">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="cce93-180">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cce93-180">Minimum supported server</span></span><br/> | <span data-ttu-id="cce93-181">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cce93-181">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="cce93-182">Header</span><span class="sxs-lookup"><span data-stu-id="cce93-182">Header</span></span><br/>                   | <dl> <span data-ttu-id="cce93-183"><dt>Ws2def. h (Include Winsock2. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cce93-183"><dt>Ws2def.h (include Winsock2.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cce93-184">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cce93-184">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cce93-185">**getsockopt**</span><span class="sxs-lookup"><span data-stu-id="cce93-185">**getsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[<span data-ttu-id="cce93-186">**setsockopt**</span><span class="sxs-lookup"><span data-stu-id="cce93-186">**setsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> <dt>

<span data-ttu-id="cce93-187">[KeepAliveTime](/previous-versions/windows/it-pro/windows-server-2003/cc782936(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="cce93-187">[KeepAliveTime](/previous-versions/windows/it-pro/windows-server-2003/cc782936(v=ws.10))</span></span>
</dt> <dt>

<span data-ttu-id="cce93-188">[KeepAliveInterval](/previous-versions/windows/it-pro/windows-server-2003/cc758083(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="cce93-188">[KeepAliveInterval](/previous-versions/windows/it-pro/windows-server-2003/cc758083(v=ws.10))</span></span>
</dt> <dt>

<span data-ttu-id="cce93-189">[Pptptcpmaxdataretransmissions](/previous-versions/windows/it-pro/windows-server-2003/cc775408(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="cce93-189">[PPTPTcpMaxDataRetransmissions](/previous-versions/windows/it-pro/windows-server-2003/cc775408(v=ws.10))</span></span>
</dt> <dt>

[<span data-ttu-id="cce93-190">**Glühbirne**</span><span class="sxs-lookup"><span data-stu-id="cce93-190">**socket**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-socket)
</dt> <dt>

<span data-ttu-id="cce93-191">[**SIO \_ KeepAlive \_ Vals**](/previous-versions/windows/desktop/legacy/dd877220(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cce93-191">[**SIO\_KEEPALIVE\_VALS**](/previous-versions/windows/desktop/legacy/dd877220(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="cce93-192">[TcpMaxDataRetransmissions](/previous-versions/windows/it-pro/windows-server-2003/cc780586(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="cce93-192">[TcpMaxDataRetransmissions](/previous-versions/windows/it-pro/windows-server-2003/cc780586(v=ws.10))</span></span>
</dt> <dt>

[<span data-ttu-id="cce93-193">**WSAGetLastError**</span><span class="sxs-lookup"><span data-stu-id="cce93-193">**WSAGetLastError**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)
</dt> </dl>

 

 
