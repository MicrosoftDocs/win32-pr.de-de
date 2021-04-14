---
description: Ermöglicht es einer Anwendung, die Rückgabe von Paketinformationen durch die wsarecvmsg-Funktion auf einem IPv4-Socket zu aktivieren oder zu deaktivieren.
ms.assetid: C6246899-0220-4F88-B43B-CED1B1FF7DC3
title: IP_PKTINFO Socket-Option (Ws2ipdef. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2134b31ead9efeb032b4ed72fcaedcd4cc9f67f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343489"
---
# <a name="ip_pktinfo-socket-option"></a><span data-ttu-id="ad537-103">IP \_ pktinfo-Socketoption</span><span class="sxs-lookup"><span data-stu-id="ad537-103">IP\_PKTINFO socket option</span></span>

<span data-ttu-id="ad537-104">Die IP \_ pktinfo-Socketoption ermöglicht es einer Anwendung, die Rückgabe von Paketinformationen durch die [**LPFN_WSARECVMSG (wsarecvmsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) -Funktion auf einem IPv4-Socket zu aktivieren oder zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="ad537-104">The IP\_PKTINFO socket option allows an application to enable or disable the return of packet information by the [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) function on an IPv4 socket..</span></span>

<span data-ttu-id="ad537-105">Um den Status dieser Socketoption abzufragen, müssen Sie die [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="ad537-105">To query the status of this socket option, call the [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) function.</span></span> <span data-ttu-id="ad537-106">Um diese Option festzulegen, müssen Sie die Funktion [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) mit den folgenden Parametern aufrufen.</span><span class="sxs-lookup"><span data-stu-id="ad537-106">To set this option, call the [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function with the following parameters.</span></span>

## <a name="socket-option-value"></a><span data-ttu-id="ad537-107">Wert der Socketoption</span><span class="sxs-lookup"><span data-stu-id="ad537-107">Socket option value</span></span>

<span data-ttu-id="ad537-108">Die Konstante, die diese Socketoption darstellt, ist 19.</span><span class="sxs-lookup"><span data-stu-id="ad537-108">The constant that represents this socket option is 19.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad537-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="ad537-109">Syntax</span></span>


```C++
int getsockopt(
  (SOCKET) s,      // descriptor identifying a socket 
  (int) IPPROTO_IP,   // level
  (int) IP_PKTINFO, // optname
  (char *) optval, // output buffer,
  (int) optlen,  // size of output buffer
);
```




```C++
int setsockopt(
  (SOCKET) s,      // descriptor identifying a socket 
  (int) IPPROTO_IP,   // level
  (int) IP_PKTINFO, // optname
  (char *) optval, // input buffer,
  (int) optlen,  // size of input buffer
);
```



## <a name="parameters"></a><span data-ttu-id="ad537-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ad537-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad537-111">*s* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ad537-111">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad537-112">Ein Deskriptor, der den Socket identifiziert.</span><span class="sxs-lookup"><span data-stu-id="ad537-112">A descriptor identifying the socket.</span></span>

</dd> <dt>

<span data-ttu-id="ad537-113">*Ebene* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ad537-113">*level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad537-114">Die Ebene, auf der die Option definiert ist.</span><span class="sxs-lookup"><span data-stu-id="ad537-114">The level at which the option is defined.</span></span> <span data-ttu-id="ad537-115">Verwenden Sie **ipproto \_ IP** für diesen Vorgang.</span><span class="sxs-lookup"><span data-stu-id="ad537-115">Use **IPPROTO\_IP** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="ad537-116">*optname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ad537-116">*optname* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad537-117">Die Socketoption, für die der Wert festgelegt oder festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ad537-117">The socket option for which to get or set the value.</span></span> <span data-ttu-id="ad537-118">Verwenden Sie \_ für diesen Vorgang IP pktinfo.</span><span class="sxs-lookup"><span data-stu-id="ad537-118">Use IP\_PKTINFO for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="ad537-119">*optval* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="ad537-119">*optval* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ad537-120">Ein Zeiger auf den Puffer, der den Wert für die festzulegende Option enthält.</span><span class="sxs-lookup"><span data-stu-id="ad537-120">A pointer to the buffer containing the value for the option to set.</span></span> <span data-ttu-id="ad537-121">Dieser Parameter sollte auf einen Puffer zeigen, der größer oder gleich der Größe eines **DWORD** -Werts ist.</span><span class="sxs-lookup"><span data-stu-id="ad537-121">This parameter should point to buffer equal to or larger than the size of a **DWORD** value.</span></span>

<span data-ttu-id="ad537-122">Dieser Wert wird als boolescher Wert behandelt, wobei 0 verwendet wird, um **false** (deaktiviert) und einen Wert ungleich 0 (null) anzugeben, um **true** (aktiviert) anzugeben.</span><span class="sxs-lookup"><span data-stu-id="ad537-122">This value is treated as a boolean value with 0 used to indicate **FALSE** (disabled) and a nonzero value to indicate **TRUE** (enabled).</span></span>

</dd> <dt>

<span data-ttu-id="ad537-123">*optlen* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="ad537-123">*optlen* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ad537-124">Ein Zeiger auf die Größe des *optval* -Puffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="ad537-124">A pointer to the size, in bytes, of the *optval* buffer.</span></span> <span data-ttu-id="ad537-125">Diese Größe muss größer oder gleich der Größe eines **DWORD** -Werts sein.</span><span class="sxs-lookup"><span data-stu-id="ad537-125">This size must be equal to or larger than the size of a **DWORD** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad537-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ad537-126">Return value</span></span>

<span data-ttu-id="ad537-127">Wenn der Vorgang erfolgreich abgeschlossen wird, gibt die Funktion [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) oder [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) NULL zurück.</span><span class="sxs-lookup"><span data-stu-id="ad537-127">If the operation completes successfully, the [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) or [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function returns zero.</span></span>

<span data-ttu-id="ad537-128">Wenn der Vorgang fehlschlägt, wird der Wert Socket \_ Error zurückgegeben, und es kann ein spezifischer Fehlercode durch Aufrufen von [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="ad537-128">If the operation fails, a value of SOCKET\_ERROR is returned and a specific error code can be retrieved by calling [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>



| <span data-ttu-id="ad537-129">Fehlercode</span><span class="sxs-lookup"><span data-stu-id="ad537-129">Error code</span></span>                                                                                                                                              | <span data-ttu-id="ad537-130">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="ad537-130">Meaning</span></span>                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ad537-131"><dt>**[WSANOTINITIALISED](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="ad537-131"><dt>**[WSANOTINITIALISED](windows-sockets-error-codes-2.md)**</dt></span></span> </dl> | <span data-ttu-id="ad537-132">Ein erfolgreicher [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) -Befehl muss vor der Verwendung dieser Funktion ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="ad537-132">A successful [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) call must occur before using this function.</span></span><br/>                                                                                                                                                     |
| <dl> <span data-ttu-id="ad537-133"><dt>**[WSAENETDOWN](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="ad537-133"><dt>**[WSAENETDOWN](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>             | <span data-ttu-id="ad537-134">Das Netzwerk Subsystem ist fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="ad537-134">The network subsystem has failed.</span></span><br/>                                                                                                                                                                                                               |
| <dl> <span data-ttu-id="ad537-135"><dt>**[WSAEFAULT](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="ad537-135"><dt>**[WSAEFAULT](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>                 | <span data-ttu-id="ad537-136">Einer der *optval* -oder *optlen* -Parameter verweist auf den Arbeitsspeicher, der sich nicht in einem gültigen Teil des Benutzer Adressraums befindet.</span><span class="sxs-lookup"><span data-stu-id="ad537-136">One of the *optval* or the *optlen* parameters point to memory that is not in a valid part of the user address space.</span></span> <span data-ttu-id="ad537-137">Dieser Fehler wird auch zurückgegeben, wenn der Wert, auf den der *optlen* -Parameter verweist, kleiner ist als die Größe eines **DWORD** -Werts.</span><span class="sxs-lookup"><span data-stu-id="ad537-137">This error is also returned if the value pointed to by the *optlen* parameter is less than the size of a **DWORD** value.</span></span><br/> |
| <dl> <span data-ttu-id="ad537-138"><dt>**[Wsaeingabe Progress](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="ad537-138"><dt>**[WSAEINPROGRESS](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>       | <span data-ttu-id="ad537-139">Ein blockierender Windows Sockets 1,1-Rückruf wird gerade ausgeführt, oder der Dienstanbieter verarbeitet weiterhin eine Rückruffunktion.</span><span class="sxs-lookup"><span data-stu-id="ad537-139">A blocking Windows Sockets 1.1 call is in progress, or the service provider is still processing a callback function.</span></span><br/>                                                                                                                            |
| <dl> <span data-ttu-id="ad537-140"><dt>**[Wsaabval](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="ad537-140"><dt>**[WSAEINVAL](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>                 | <span data-ttu-id="ad537-141">Ein ungültiges Argument wurde angegeben.</span><span class="sxs-lookup"><span data-stu-id="ad537-141">An invalid argument was supplied.</span></span> <span data-ttu-id="ad537-142">Dieser Fehler wird zurückgegeben, wenn der *Level* -Parameter unbekannt oder ungültig ist.</span><span class="sxs-lookup"><span data-stu-id="ad537-142">This error is returned if the *level* parameter is unknown or invalid.</span></span> <span data-ttu-id="ad537-143">Unter Windows Vista und höher wird dieser Fehler auch zurückgegeben, wenn sich der Socket in einem Übergangszustand befunden hat.</span><span class="sxs-lookup"><span data-stu-id="ad537-143">On Windows Vista and later, this error is also returned if the socket was in a transitional state.</span></span><br/>                                     |
| <dl> <span data-ttu-id="ad537-144"><dt>**[Wsaumoproumopt](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="ad537-144"><dt>**[WSAENOPROTOOPT](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>       | <span data-ttu-id="ad537-145">Die Option ist unbekannt oder wird von der angegebener Protokollfamilie nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ad537-145">The option is unknown or unsupported by the indicated protocol family.</span></span> <span data-ttu-id="ad537-146">Dieser Fehler wird zurückgegeben, wenn der *Typparameter für den socketdeskriptor* , der in den *s* -Parameter übergeben wurde, kein **Sock- \_ dgram** oder **Sock- \_ RAW** ist</span><span class="sxs-lookup"><span data-stu-id="ad537-146">This error is returned if the *type* parameter for the socket descriptor passed in the *s* parameter was not **SOCK\_DGRAM** or **SOCK\_RAW**.</span></span> <br/>                          |
| <dl> <span data-ttu-id="ad537-147"><dt>**[Wsaumotsock](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="ad537-147"><dt>**[WSAENOTSOCK](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>             | <span data-ttu-id="ad537-148">Der Deskriptor ist kein Socket.</span><span class="sxs-lookup"><span data-stu-id="ad537-148">The descriptor is not a socket.</span></span><br/>                                                                                                                                                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="ad537-149">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ad537-149">Remarks</span></span>

<span data-ttu-id="ad537-150">Die [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) -Funktion, die mit der IP \_ pktinfo-Socketoption aufgerufen wird, ermöglicht einer Anwendung, festzustellen, ob Paketinformationen von der [**LPFN_WSARECVMSG (wsarecvmsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)-Funktion für einen IPv4-Socket zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ad537-150">The [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) function called with the IP\_PKTINFO socket option allows an application to determine if packet information is to be returned by the [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)function for an IPv4 socket.</span></span>

<span data-ttu-id="ad537-151">Die [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) -Funktion, die mit der IP \_ pktinfo-Socketoption aufgerufen wird, ermöglicht es einer Anwendung, die Rückgabe von Paketinformationen durch die [**LPFN_WSARECVMSG (wsarecvmsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) -Funktion zu aktivieren oder zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="ad537-151">The [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function called with the IP\_PKTINFO socket option allows an application to enable or disable the return of packet information by the [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) function.</span></span> <span data-ttu-id="ad537-152">Die \_ Option IP pktinfo für einen Socket ist standardmäßig deaktiviert (auf **false** festgelegt).</span><span class="sxs-lookup"><span data-stu-id="ad537-152">The IP\_PKTINFO option for a socket is disabled (set to **FALSE**) by default.</span></span>

<span data-ttu-id="ad537-153">Wenn diese Socketoption auf einem IPv4-Socket vom Typ **Sock \_ dgram** oder **Sock \_ RAW** aktiviert ist, gibt die Funktion [**LPFN_WSARECVMSG (wsarecvmsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) Paketinformationen in der [**wsamsg**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) -Struktur zurück, auf die durch den *lpmsg* -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="ad537-153">When this socket option is enabled on an IPv4 socket of type **SOCK\_DGRAM** or **SOCK\_RAW**, the [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) function returns packet information in the [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) structure pointed to by the *lpMsg* parameter.</span></span> <span data-ttu-id="ad537-154">Eines der Steuerungsdaten Objekte in der zurückgegebenen **wsamsg** -Struktur enthält eine [**in \_ pktinfo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in_pktinfo) -Struktur, die zum Speichern von Informationen zu empfangenen Paket Adressen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ad537-154">One of the control data objects in the returned **WSAMSG** structure will contain an [**in\_pktinfo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in_pktinfo) structure used to store received packet address information.</span></span>

<span data-ttu-id="ad537-155">Für Datagramme, die von der [**LPFN_WSARECVMSG (wsarecvmsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) -Funktion über IPv4 empfangen werden, enthält das **Steuer** Element Mitglied der [**wsamsg**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) -Struktur eine [**WSABUF**](/windows/desktop/api/ws2def/ns-ws2def-wsabuf) -Struktur, die eine **wsacmsghdr** -Struktur enthält.</span><span class="sxs-lookup"><span data-stu-id="ad537-155">For datagrams received by the [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) function over IPv4, the **Control** member of the [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) structure received will contain a [**WSABUF**](/windows/desktop/api/ws2def/ns-ws2def-wsabuf) structure that contains a **WSACMSGHDR** structure.</span></span> <span data-ttu-id="ad537-156">Der Member der **CMSG- \_ Ebene** dieser **wsacmsghdr** -Struktur würde **ipproto \_ IP** enthalten, der **CMSG- \_ Typmember** dieser Struktur würde **IP \_ pktinfo** enthalten, und der **CMSG- \_ Datenmember** enthält eine [**in \_ pktinfo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in_pktinfo) -Struktur, die zum Speichern der empfangenen IPv4-Paket Adressinformationen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ad537-156">The **cmsg\_level** member of this **WSACMSGHDR** structure would contain **IPPROTO\_IP**, the **cmsg\_type** member of this structure would contain **IP\_PKTINFO**, and the **cmsg\_data** member would contain an [**in\_pktinfo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in_pktinfo) structure used to store received IPv4 packet address information.</span></span> <span data-ttu-id="ad537-157">Die IPv4-Adresse in der **in \_ pktinfo** -Struktur ist die IPv4-Adresse, von der das Paket empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="ad537-157">The IPv4 address in the **in\_pktinfo** structure is the IPv4 address from which the packet was received.</span></span>

<span data-ttu-id="ad537-158">Wenn eine Anwendung für einen Datagramm-Socket mit zwei Stapeln die [**LPFN_WSARECVMSG (wsarecvmsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) -Funktion benötigt, um Paketinformationen in einer [**wsamsg**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) -Struktur für über IPv4 Empfangene Datagramme zurückzugeben, muss die IP \_ pktinfo-Socketoption für den Socket auf true festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="ad537-158">For a dual-stack datagram socket, if an application requires the [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) function to return packet information in a [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) structure for datagrams received over IPv4, then IP\_PKTINFO socket option must be set to true on the socket.</span></span> <span data-ttu-id="ad537-159">Wenn nur die [IPv6- \_ pktinfo](ipv6-pktinfo.md) -Option im Socket auf true festgelegt ist, werden Paketinformationen für über IPv6 Empfangene Datagramme bereitgestellt, jedoch nicht für Datagramme, die über IPv4 empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="ad537-159">If only the [IPV6\_PKTINFO](ipv6-pktinfo.md) option is set to true on the socket, packet information will be provided for datagrams received over IPv6 but may not be provided for datagrams received over IPv4.</span></span>

<span data-ttu-id="ad537-160">Wenn eine Anwendung versucht, die IP- \_ pktinfo-Socketoption auf einem Dual-Stack-Datagramm-Socket festzulegen, und IPv4 auf dem System deaktiviert ist, schlägt die Funktion " [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) " fehl, und " [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) " wird mit dem Fehler " [WSAEINVAL](windows-sockets-error-codes-2.md)" zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ad537-160">If an application tries to set the IP\_PKTINFO socket option on a dual-stack datagram socket and IPv4 is disabled on the system, then the [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function will fail and [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) will return with an error of [WSAEINVAL](windows-sockets-error-codes-2.md).</span></span> <span data-ttu-id="ad537-161">Dieser Fehler wird auch durch die Funktion " **setsockopt** " aufgrund anderer Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ad537-161">This same error is also returned by the **setsockopt** function as a result of other errors.</span></span> <span data-ttu-id="ad537-162">Wenn eine Anwendung versucht, eine \_ Socketoption auf ipproto-IP-Ebene in einem Dual-Stack-Socket festzulegen, und Sie mit [WSAEINVAL](windows-sockets-error-codes-2.md)fehlschlägt, sollte die Anwendung ermitteln, ob IPv4 auf dem lokalen Computer deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="ad537-162">If an application tries to set an IPPROTO\_IP level socket option on a dual-stack socket and it fails with [WSAEINVAL](windows-sockets-error-codes-2.md), then the application should determine if IPv4 is disabled on the local computer.</span></span> <span data-ttu-id="ad537-163">Eine Methode, die verwendet werden kann, um zu ermitteln, ob IPv4 aktiviert oder deaktiviert ist, besteht darin, die [**Socketfunktion**](/windows/desktop/api/Winsock2/nf-winsock2-socket) mit dem auf AF inet festgelegten *AF* -Parameter aufzurufen, \_ um einen IPv4-Socket zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ad537-163">One method that can be used to detect if IPv4 is enabled or disabled is to call the [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) function with the *af* parameter set to AF\_INET to try and create an IPv4 socket.</span></span> <span data-ttu-id="ad537-164">Wenn die **Socketfunktion** ausfällt und **WSAGetLastError** einen Fehler von [WSAEAFNOSUPPORT](windows-sockets-error-codes-2.md)zurückgibt, bedeutet dies, dass IPv4 nicht aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="ad537-164">If the **socket** function fails and **WSAGetLastError** returns an error of [WSAEAFNOSUPPORT](windows-sockets-error-codes-2.md), then it means IPv4 is not enabled.</span></span> <span data-ttu-id="ad537-165">In diesem Fall kann ein **setsockopt** -Funktionsfehler auftreten, wenn versucht wird, die IP \_ pktinfo-Socketoption festzulegen, kann die Anwendung ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="ad537-165">In this case, a **setsockopt** function failure when attempting to set the IP\_PKTINFO socket option can be ignored by the application.</span></span> <span data-ttu-id="ad537-166">Andernfalls sollte bei dem Versuch, die \_ Socketoption IP pktinfo festzulegen, ein unerwarteter Fehler behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="ad537-166">Otherwise a failure when attempting to set the IP\_PKTINFO socket option should be treated as an unexpected error.</span></span>

<span data-ttu-id="ad537-167">Beachten Sie, dass die Header Datei " *Ws2ipdef. h* " automatisch in " *Ws2tcpip. h*" enthalten ist und niemals direkt verwendet werden sollte.</span><span class="sxs-lookup"><span data-stu-id="ad537-167">Note that the *Ws2ipdef.h* header file is automatically included in *Ws2tcpip.h*, and should never be used directly.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad537-168">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ad537-168">Requirements</span></span>



| <span data-ttu-id="ad537-169">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ad537-169">Requirement</span></span> | <span data-ttu-id="ad537-170">Wert</span><span class="sxs-lookup"><span data-stu-id="ad537-170">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad537-171">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ad537-171">Minimum supported client</span></span><br/> | <span data-ttu-id="ad537-172">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ad537-172">Windows XP \[desktop apps only\]</span></span><br/>                                                                |
| <span data-ttu-id="ad537-173">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ad537-173">Minimum supported server</span></span><br/> | <span data-ttu-id="ad537-174">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ad537-174">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="ad537-175">Header</span><span class="sxs-lookup"><span data-stu-id="ad537-175">Header</span></span><br/>                   | <dl> <span data-ttu-id="ad537-176"><dt>Ws2ipdef. h (Include Ws2tcpip. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ad537-176"><dt>Ws2ipdef.h (include Ws2tcpip.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad537-177">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ad537-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad537-178">Dual-Stack-Sockets</span><span class="sxs-lookup"><span data-stu-id="ad537-178">Dual-Stack Sockets</span></span>](dual-stack-sockets.md)
</dt> <dt>

[<span data-ttu-id="ad537-179">**getsockopt**</span><span class="sxs-lookup"><span data-stu-id="ad537-179">**getsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[<span data-ttu-id="ad537-180">**in \_ pktinfo**</span><span class="sxs-lookup"><span data-stu-id="ad537-180">**in\_pktinfo**</span></span>](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in_pktinfo)
</dt> <dt>

[<span data-ttu-id="ad537-181">**Ipproto \_ IP-Socketoptionen**</span><span class="sxs-lookup"><span data-stu-id="ad537-181">**IPPROTO\_IP Socket Options**</span></span>](ipproto-ip-socket-options.md)
</dt> <dt>

[<span data-ttu-id="ad537-182">IPv6- \_ pktinfo</span><span class="sxs-lookup"><span data-stu-id="ad537-182">IPV6\_PKTINFO</span></span>](ipv6-pktinfo.md)
</dt> <dt>

[<span data-ttu-id="ad537-183">**setsockopt**</span><span class="sxs-lookup"><span data-stu-id="ad537-183">**setsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> <dt>

[<span data-ttu-id="ad537-184">**Glühbirne**</span><span class="sxs-lookup"><span data-stu-id="ad537-184">**socket**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-socket)
</dt> <dt>

[<span data-ttu-id="ad537-185">**Wsamsg**</span><span class="sxs-lookup"><span data-stu-id="ad537-185">**WSAMSG**</span></span>](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg)
</dt> <dt>

[<span data-ttu-id="ad537-186">**LPFN_WSARECVMSG (wsarecvmsg)**</span><span class="sxs-lookup"><span data-stu-id="ad537-186">**LPFN_WSARECVMSG (WSARecvMsg)**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)
</dt> </dl>

 

 
