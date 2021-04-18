---
description: Ermöglicht es einer Anwendung, die Rückgabe von Paketinformationen durch die wsarecvmsg-Funktion auf einem IPv6-Socket zu aktivieren oder zu deaktivieren.
ms.assetid: 7BF17538-BE92-44FE-BA3C-6B44F61D478A
title: IPV6_PKTINFO Socket-Option (Ws2ipdef. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5afd5b19cbaba7f6a66f5ba6fbd85d74eb2f2e3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354474"
---
# <a name="ipv6_pktinfo-socket-option"></a><span data-ttu-id="a54e6-103">IPv6- \_ pktinfo-Socketoption</span><span class="sxs-lookup"><span data-stu-id="a54e6-103">IPV6\_PKTINFO socket option</span></span>

<span data-ttu-id="a54e6-104">Die IPv6- \_ pktinfo-Socketoption ermöglicht es einer Anwendung, die Rückgabe von Paketinformationen durch die [**LPFN_WSARECVMSG (wsarecvmsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) -Funktion auf einem IPv6-Socket zu aktivieren oder zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="a54e6-104">The IPV6\_PKTINFO socket option allows an application to enable or disable the return of packet information by the [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) function on an IPv6 socket..</span></span>

<span data-ttu-id="a54e6-105">Um den Status dieser Socketoption abzufragen, müssen Sie die [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="a54e6-105">To query the status of this socket option, call the [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) function.</span></span> <span data-ttu-id="a54e6-106">Um diese Option festzulegen, müssen Sie die Funktion [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) mit den folgenden Parametern aufrufen.</span><span class="sxs-lookup"><span data-stu-id="a54e6-106">To set this option, call the [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function with the following parameters.</span></span>

## <a name="socket-option-value"></a><span data-ttu-id="a54e6-107">Wert der Socketoption</span><span class="sxs-lookup"><span data-stu-id="a54e6-107">Socket option value</span></span>

<span data-ttu-id="a54e6-108">Die Konstante, die diese Socketoption darstellt, ist 19.</span><span class="sxs-lookup"><span data-stu-id="a54e6-108">The constant that represents this socket option is 19.</span></span>

## <a name="syntax"></a><span data-ttu-id="a54e6-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="a54e6-109">Syntax</span></span>


```C++
int getsockopt(
  (SOCKET) s,      // descriptor identifying a socket 
  (int) IPPROTO_IPV6,   // level
  (int) IPV6_PKTINFO, // optname
  (char *) optval, // output buffer,
  (int) optlen,  // size of output buffer
);
```




```C++
int setsockopt(
  (SOCKET) s,      // descriptor identifying a socket 
  (int) IPPROTO_IPV6,   // level
  (int) IPV6_PKTINFO, // optname
  (char *) optval, // input buffer,
  (int) optlen,  // size of input buffer
);
```



## <a name="parameters"></a><span data-ttu-id="a54e6-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a54e6-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a54e6-111">*s* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a54e6-111">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a54e6-112">Ein Deskriptor, der den Socket identifiziert.</span><span class="sxs-lookup"><span data-stu-id="a54e6-112">A descriptor identifying the socket.</span></span>

</dd> <dt>

<span data-ttu-id="a54e6-113">*Ebene* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a54e6-113">*level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a54e6-114">Die Ebene, auf der die Option definiert ist.</span><span class="sxs-lookup"><span data-stu-id="a54e6-114">The level at which the option is defined.</span></span> <span data-ttu-id="a54e6-115">Verwenden Sie **ipproto \_ IPv6** für diesen Vorgang.</span><span class="sxs-lookup"><span data-stu-id="a54e6-115">Use **IPPROTO\_IPV6** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="a54e6-116">*optname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a54e6-116">*optname* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a54e6-117">Die Socketoption, für die der Wert festgelegt oder festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="a54e6-117">The socket option for which to get or set the value.</span></span> <span data-ttu-id="a54e6-118">Verwenden Sie \_ für diesen Vorgang IPv6 pktinfo.</span><span class="sxs-lookup"><span data-stu-id="a54e6-118">Use IPV6\_PKTINFO for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="a54e6-119">*optval* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a54e6-119">*optval* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a54e6-120">Ein Zeiger auf den Puffer, der den Wert für die festzulegende Option enthält.</span><span class="sxs-lookup"><span data-stu-id="a54e6-120">A pointer to the buffer containing the value for the option to set.</span></span> <span data-ttu-id="a54e6-121">Dieser Parameter sollte auf einen Puffer zeigen, der größer oder gleich der Größe eines **DWORD** -Werts ist.</span><span class="sxs-lookup"><span data-stu-id="a54e6-121">This parameter should point to buffer equal to or larger than the size of a **DWORD** value.</span></span>

<span data-ttu-id="a54e6-122">Dieser Wert wird als boolescher Wert behandelt, wobei 0 verwendet wird, um **false** (deaktiviert) und einen Wert ungleich 0 (null) anzugeben, um **true** (aktiviert) anzugeben.</span><span class="sxs-lookup"><span data-stu-id="a54e6-122">This value is treated as a boolean value with 0 used to indicate **FALSE** (disabled) and a nonzero value to indicate **TRUE** (enabled).</span></span>

</dd> <dt>

<span data-ttu-id="a54e6-123">*optlen* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="a54e6-123">*optlen* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a54e6-124">Ein Zeiger auf die Größe des *optval* -Puffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="a54e6-124">A pointer to the size, in bytes, of the *optval* buffer.</span></span> <span data-ttu-id="a54e6-125">Diese Größe muss größer oder gleich der Größe eines **DWORD** -Werts sein.</span><span class="sxs-lookup"><span data-stu-id="a54e6-125">This size must be equal to or larger than the size of a **DWORD** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a54e6-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a54e6-126">Return value</span></span>

<span data-ttu-id="a54e6-127">Wenn der Vorgang erfolgreich abgeschlossen wird, gibt die Funktion [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) oder [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) NULL zurück.</span><span class="sxs-lookup"><span data-stu-id="a54e6-127">If the operation completes successfully, the [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) or [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function returns zero.</span></span>

<span data-ttu-id="a54e6-128">Wenn der Vorgang fehlschlägt, wird der Wert Socket \_ Error zurückgegeben, und es kann ein spezifischer Fehlercode durch Aufrufen von [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="a54e6-128">If the operation fails, a value of SOCKET\_ERROR is returned and a specific error code can be retrieved by calling [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>



| <span data-ttu-id="a54e6-129">Fehlercode</span><span class="sxs-lookup"><span data-stu-id="a54e6-129">Error code</span></span>                                                                                                                                              | <span data-ttu-id="a54e6-130">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="a54e6-130">Meaning</span></span>                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a54e6-131"><dt>**[WSANOTINITIALISED](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="a54e6-131"><dt>**[WSANOTINITIALISED](windows-sockets-error-codes-2.md)**</dt></span></span> </dl> | <span data-ttu-id="a54e6-132">Ein erfolgreicher [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) -Befehl muss vor der Verwendung dieser Funktion ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="a54e6-132">A successful [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) call must occur before using this function.</span></span><br/>                                                                                                                                                     |
| <dl> <span data-ttu-id="a54e6-133"><dt>**[WSAENETDOWN](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="a54e6-133"><dt>**[WSAENETDOWN](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>             | <span data-ttu-id="a54e6-134">Das Netzwerk Subsystem ist fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="a54e6-134">The network subsystem has failed.</span></span><br/>                                                                                                                                                                                                               |
| <dl> <span data-ttu-id="a54e6-135"><dt>**[WSAEFAULT](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="a54e6-135"><dt>**[WSAEFAULT](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>                 | <span data-ttu-id="a54e6-136">Einer der *optval* -oder *optlen* -Parameter verweist auf den Arbeitsspeicher, der sich nicht in einem gültigen Teil des Benutzer Adressraums befindet.</span><span class="sxs-lookup"><span data-stu-id="a54e6-136">One of the *optval* or the *optlen* parameters point to memory that is not in a valid part of the user address space.</span></span> <span data-ttu-id="a54e6-137">Dieser Fehler wird auch zurückgegeben, wenn der Wert, auf den der *optlen* -Parameter verweist, kleiner ist als die Größe eines **DWORD** -Werts.</span><span class="sxs-lookup"><span data-stu-id="a54e6-137">This error is also returned if the value pointed to by the *optlen* parameter is less than the size of a **DWORD** value.</span></span><br/> |
| <dl> <span data-ttu-id="a54e6-138"><dt>**[Wsaeingabe Progress](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="a54e6-138"><dt>**[WSAEINPROGRESS](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>       | <span data-ttu-id="a54e6-139">Ein blockierender Windows Sockets 1,1-Rückruf wird gerade ausgeführt, oder der Dienstanbieter verarbeitet weiterhin eine Rückruffunktion.</span><span class="sxs-lookup"><span data-stu-id="a54e6-139">A blocking Windows Sockets 1.1 call is in progress, or the service provider is still processing a callback function.</span></span><br/>                                                                                                                            |
| <dl> <span data-ttu-id="a54e6-140"><dt>**[Wsaabval](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="a54e6-140"><dt>**[WSAEINVAL](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>                 | <span data-ttu-id="a54e6-141">Ein ungültiges Argument wurde angegeben.</span><span class="sxs-lookup"><span data-stu-id="a54e6-141">An invalid argument was supplied.</span></span> <span data-ttu-id="a54e6-142">Dieser Fehler wird zurückgegeben, wenn der *Level* -Parameter unbekannt oder ungültig ist.</span><span class="sxs-lookup"><span data-stu-id="a54e6-142">This error is returned if the *level* parameter is unknown or invalid.</span></span> <span data-ttu-id="a54e6-143">Unter Windows Vista und höher wird dieser Fehler auch zurückgegeben, wenn sich der Socket in einem Übergangszustand befunden hat.</span><span class="sxs-lookup"><span data-stu-id="a54e6-143">On Windows Vista and later, this error is also returned if the socket was in a transitional state.</span></span><br/>                                     |
| <dl> <span data-ttu-id="a54e6-144"><dt>**[Wsaumoproumopt](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="a54e6-144"><dt>**[WSAENOPROTOOPT](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>       | <span data-ttu-id="a54e6-145">Die Option ist unbekannt oder wird von der angegebener Protokollfamilie nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a54e6-145">The option is unknown or unsupported by the indicated protocol family.</span></span> <span data-ttu-id="a54e6-146">Dieser Fehler wird zurückgegeben, wenn der *Typparameter für den socketdeskriptor* , der in den *s* -Parameter übergeben wurde, kein **Sock- \_ dgram** oder **Sock- \_ RAW** ist</span><span class="sxs-lookup"><span data-stu-id="a54e6-146">This error is returned if the *type* parameter for the socket descriptor passed in the *s* parameter was not **SOCK\_DGRAM** or **SOCK\_RAW**.</span></span> <br/>                          |
| <dl> <span data-ttu-id="a54e6-147"><dt>**[Wsaumotsock](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="a54e6-147"><dt>**[WSAENOTSOCK](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>             | <span data-ttu-id="a54e6-148">Der Deskriptor ist kein Socket.</span><span class="sxs-lookup"><span data-stu-id="a54e6-148">The descriptor is not a socket.</span></span><br/>                                                                                                                                                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="a54e6-149">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a54e6-149">Remarks</span></span>

<span data-ttu-id="a54e6-150">Die [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) -Funktion, die mit der IPv6- \_ pktinfo-Socketoption aufgerufen wird, ermöglicht einer Anwendung, festzustellen, ob Paketinformationen von der [**LPFN_WSARECVMSG (wsarecvmsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)-Funktion für einen IPv6-Socket zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="a54e6-150">The [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) function called with the IPV6\_PKTINFO socket option allows an application to determine if packet information is to be returned by the [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)function for an IPv6 socket.</span></span>

<span data-ttu-id="a54e6-151">Die [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) -Funktion, die mit der IPv6- \_ pktinfo-Socketoption aufgerufen wird, ermöglicht es einer Anwendung, die Rückgabe von Paketinformationen durch die [**LPFN_WSARECVMSG (wsarecvmsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) -Funktion zu aktivieren oder zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="a54e6-151">The [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function called with the IPV6\_PKTINFO socket option allows an application to enable or disable the return of packet information by the [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) function.</span></span> <span data-ttu-id="a54e6-152">Die IPv6- \_ pktinfo-Option für einen Socket ist standardmäßig deaktiviert (auf **false** festgelegt).</span><span class="sxs-lookup"><span data-stu-id="a54e6-152">The IPV6\_PKTINFO option for a socket is disabled (set to **FALSE**) by default.</span></span>

<span data-ttu-id="a54e6-153">Wenn diese Socketoption auf einem IPv6-Socket vom Typ **Sock \_ dgram** oder **Sock \_ RAW** aktiviert ist, gibt die Funktion [**LPFN_WSARECVMSG (wsarecvmsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) Paketinformationen in der [**wsamsg**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) -Struktur zurück, auf die durch den *lpmsg* -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="a54e6-153">When this socket option is enabled on an IPv6 socket of type **SOCK\_DGRAM** or **SOCK\_RAW**, the [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) function returns packet information in the [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) structure pointed to by the *lpMsg* parameter.</span></span> <span data-ttu-id="a54e6-154">Eines der Steuerungsdaten Objekte in der zurückgegebenen **wsamsg** -Struktur enthält eine [**IN6 \_ pktinfo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in6_pktinfo) -Struktur, die zum Speichern von Informationen zu empfangenen Paket Adressen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a54e6-154">One of the control data objects in the returned **WSAMSG** structure will contain an [**in6\_pktinfo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in6_pktinfo) structure used to store received packet address information.</span></span>

<span data-ttu-id="a54e6-155">Für Datagramme, die von der [**LPFN_WSARECVMSG (wsarecvmsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) -Funktion über IPv6 empfangen werden, enthält das **Steuer** Element Mitglied der [**wsamsg**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) -Struktur eine [**WSABUF**](/windows/desktop/api/ws2def/ns-ws2def-wsabuf) -Struktur, die eine **wsacmsghdr** -Struktur enthält.</span><span class="sxs-lookup"><span data-stu-id="a54e6-155">For datagrams received by the [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) function over IPv6, the **Control** member of the [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) structure received will contain a [**WSABUF**](/windows/desktop/api/ws2def/ns-ws2def-wsabuf) structure that contains a **WSACMSGHDR** structure.</span></span> <span data-ttu-id="a54e6-156">Der Member der **CMSG- \_ Ebene** dieser **wsacmsghdr** -Struktur würde **ipproto \_ IPv6** enthalten, der **CMSG- \_ Typmember** dieser Struktur würde **IPv6 \_ pktinfo** enthalten, und der **CMSG- \_ Datenmember** enthält eine [**IN6 \_ pktinfo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in6_pktinfo) -Struktur, die zum Speichern empfangener IPv6-Paket Adressinformationen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a54e6-156">The **cmsg\_level** member of this **WSACMSGHDR** structure would contain **IPPROTO\_IPV6**, the **cmsg\_type** member of this structure would contain **IPV6\_PKTINFO**, and the **cmsg\_data** member would contain an [**in6\_pktinfo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in6_pktinfo) structure used to store received IPv6 packet address information.</span></span> <span data-ttu-id="a54e6-157">Die IPv6-Adresse in der **IN6 \_ pktinfo** -Struktur ist die IPv6-Adresse, von der das Paket empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="a54e6-157">The IPv6 address in the **in6\_pktinfo** structure is the IPv6 address from which the packet was received.</span></span>

<span data-ttu-id="a54e6-158">Wenn eine Anwendung für einen Datagramm-Socket mit zwei Stapeln die [**LPFN_WSARECVMSG (wsarecvmsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) -Funktion benötigt, um Paketinformationen in einer [**wsamsg**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) -Struktur für über IPv4 Empfangene Datagramme zurückzugeben, muss die [IP \_ pktinfo-](ip-pktinfo.md) Socketoption für den Socket auf true festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="a54e6-158">For a dual-stack datagram socket, if an application requires the [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) function to return packet information in a [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) structure for datagrams received over IPv4, then [IP\_PKTINFO](ip-pktinfo.md) socket option must be set to true on the socket.</span></span> <span data-ttu-id="a54e6-159">Wenn nur die IPv6- \_ pktinfo-Option im Socket auf true festgelegt ist, werden Paketinformationen für über IPv6 Empfangene Datagramme bereitgestellt, jedoch nicht für Datagramme, die über IPv4 empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="a54e6-159">If only the IPV6\_PKTINFO option is set to true on the socket, packet information will be provided for datagrams received over IPv6 but may not be provided for datagrams received over IPv4.</span></span>

<span data-ttu-id="a54e6-160">Beachten Sie, dass die Header Datei " *Ws2ipdef. h* " automatisch in " *Ws2tcpip. h*" enthalten ist und niemals direkt verwendet werden sollte.</span><span class="sxs-lookup"><span data-stu-id="a54e6-160">Note that the *Ws2ipdef.h* header file is automatically included in *Ws2tcpip.h*, and should never be used directly.</span></span>

## <a name="requirements"></a><span data-ttu-id="a54e6-161">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a54e6-161">Requirements</span></span>



| <span data-ttu-id="a54e6-162">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a54e6-162">Requirement</span></span> | <span data-ttu-id="a54e6-163">Wert</span><span class="sxs-lookup"><span data-stu-id="a54e6-163">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a54e6-164">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a54e6-164">Minimum supported client</span></span><br/> | <span data-ttu-id="a54e6-165">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a54e6-165">Windows XP \[desktop apps only\]</span></span><br/>                                                                |
| <span data-ttu-id="a54e6-166">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a54e6-166">Minimum supported server</span></span><br/> | <span data-ttu-id="a54e6-167">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a54e6-167">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="a54e6-168">Header</span><span class="sxs-lookup"><span data-stu-id="a54e6-168">Header</span></span><br/>                   | <dl> <span data-ttu-id="a54e6-169"><dt>Ws2ipdef. h (Include Ws2tcpip. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a54e6-169"><dt>Ws2ipdef.h (include Ws2tcpip.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a54e6-170">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a54e6-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a54e6-171">Dual-Stack-Sockets</span><span class="sxs-lookup"><span data-stu-id="a54e6-171">Dual-Stack Sockets</span></span>](dual-stack-sockets.md)
</dt> <dt>

[<span data-ttu-id="a54e6-172">**getsockopt**</span><span class="sxs-lookup"><span data-stu-id="a54e6-172">**getsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[<span data-ttu-id="a54e6-173">**IN6 \_ pktinfo**</span><span class="sxs-lookup"><span data-stu-id="a54e6-173">**in6\_pktinfo**</span></span>](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in6_pktinfo)
</dt> <dt>

[<span data-ttu-id="a54e6-174">IP- \_ pktinfo</span><span class="sxs-lookup"><span data-stu-id="a54e6-174">IP\_PKTINFO</span></span>](ip-pktinfo.md)
</dt> <dt>

[<span data-ttu-id="a54e6-175">**Ipproto \_ IPv6-Socketoptionen**</span><span class="sxs-lookup"><span data-stu-id="a54e6-175">**IPPROTO\_IPV6 Socket Options**</span></span>](ipproto-ipv6-socket-options.md)
</dt> <dt>

[<span data-ttu-id="a54e6-176">**setsockopt**</span><span class="sxs-lookup"><span data-stu-id="a54e6-176">**setsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> <dt>

[<span data-ttu-id="a54e6-177">**Glühbirne**</span><span class="sxs-lookup"><span data-stu-id="a54e6-177">**socket**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-socket)
</dt> <dt>

[<span data-ttu-id="a54e6-178">**Wsamsg**</span><span class="sxs-lookup"><span data-stu-id="a54e6-178">**WSAMSG**</span></span>](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg)
</dt> <dt>

[<span data-ttu-id="a54e6-179">**LPFN_WSARECVMSG (wsarecvmsg)**</span><span class="sxs-lookup"><span data-stu-id="a54e6-179">**LPFN_WSARECVMSG (WSARecvMsg)**</span></span>](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)
</dt> </dl>

 

 
