---
description: Gibt die lokale Adresse, den lokalen Port, die Remote Adresse, den Remoteport, den Sockettyp und das von einem Socket verwendete Protokoll zurück.
ms.assetid: 2628f47e-3e73-4e02-91b8-ba4cb0800864
title: SO_BSP_STATE Socket-Option (Ws2def. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d10e391d70dd67190e1aec803036d019261c9000
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755057"
---
# <a name="so_bsp_state-socket-option"></a><span data-ttu-id="85ca6-103">Die \_ Option "BSP \_ State Socket"</span><span class="sxs-lookup"><span data-stu-id="85ca6-103">SO\_BSP\_STATE socket option</span></span>

<span data-ttu-id="85ca6-104">Die Option " **so \_ BSP \_ State** Socket" gibt die lokale Adresse, den lokalen Port, die Remote Adresse, den Remoteport, den Sockettyp und das von einem Socket verwendete Protokoll zurück.</span><span class="sxs-lookup"><span data-stu-id="85ca6-104">The **SO\_BSP\_STATE** socket option returns the local address, local port, remote address, remote port, socket type, and protocol used by a socket.</span></span>

<span data-ttu-id="85ca6-105">Um diesen Vorgang auszuführen, müssen Sie die [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) -Funktion mit den folgenden Parametern aufrufen.</span><span class="sxs-lookup"><span data-stu-id="85ca6-105">To perform this operation, call the [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) function with the following parameters.</span></span>

## <a name="socket-option-value"></a><span data-ttu-id="85ca6-106">Wert der Socketoption</span><span class="sxs-lookup"><span data-stu-id="85ca6-106">Socket option value</span></span>

<span data-ttu-id="85ca6-107">Die Konstante, die diese Socketoption darstellt, ist 0x1009.</span><span class="sxs-lookup"><span data-stu-id="85ca6-107">The constant that represents this socket option is 0x1009.</span></span>

## <a name="syntax"></a><span data-ttu-id="85ca6-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="85ca6-108">Syntax</span></span>


```C++
int getsockopt(
  (SOCKET) s,      // descriptor identifying a socket 
  (int) SOL_SOCKET,   // level
  (int) SO_BSP_STATE, // optname
  (char *) optval,         // output buffer,
  (int) *optlen,       // size of output buffer
);
```



## <a name="parameters"></a><span data-ttu-id="85ca6-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="85ca6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85ca6-110">*s* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="85ca6-110">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85ca6-111">Ein Deskriptor, der den Socket identifiziert.</span><span class="sxs-lookup"><span data-stu-id="85ca6-111">A descriptor identifying the socket.</span></span>

</dd> <dt>

<span data-ttu-id="85ca6-112">*Ebene* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="85ca6-112">*level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85ca6-113">Die Ebene, auf der die Option definiert ist.</span><span class="sxs-lookup"><span data-stu-id="85ca6-113">The level at which the option is defined.</span></span> <span data-ttu-id="85ca6-114">Verwenden Sie für diesen Vorgang den **Sol- \_ Socket** .</span><span class="sxs-lookup"><span data-stu-id="85ca6-114">Use **SOL\_SOCKET** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="85ca6-115">*optname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="85ca6-115">*optname* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85ca6-116">Die Socketoption, für die der Wert abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="85ca6-116">The socket option for which the value is to be retrieved.</span></span> <span data-ttu-id="85ca6-117">Verwenden Sie für diesen Vorgang **also den \_ BSP- \_ Zustand** .</span><span class="sxs-lookup"><span data-stu-id="85ca6-117">Use **SO\_BSP\_STATE** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="85ca6-118">*optval* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="85ca6-118">*optval* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="85ca6-119">Ein Zeiger auf den Puffer, in dem der Wert für die angeforderte Option zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="85ca6-119">A pointer to the buffer in which the value for the requested option is to be returned.</span></span> <span data-ttu-id="85ca6-120">Dieser Parameter sollte auf einen Puffer zeigen, der größer oder gleich der Größe einer [**csaddr- \_ Informations**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) Struktur ist.</span><span class="sxs-lookup"><span data-stu-id="85ca6-120">This parameter should point to buffer equal to or larger than the size of a [**CSADDR\_INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) structure.</span></span>

</dd> <dt>

<span data-ttu-id="85ca6-121">*optlen* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="85ca6-121">*optlen* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="85ca6-122">Ein Zeiger auf die Größe des *optval* -Puffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="85ca6-122">A pointer to the size, in bytes, of the *optval* buffer.</span></span> <span data-ttu-id="85ca6-123">Diese Größe muss größer oder gleich der Größe einer [**csaddr- \_ Informations**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) Struktur sein.</span><span class="sxs-lookup"><span data-stu-id="85ca6-123">This size must be equal to or larger than the size of a [**CSADDR\_INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85ca6-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="85ca6-124">Return value</span></span>

<span data-ttu-id="85ca6-125">Wenn der Vorgang erfolgreich abgeschlossen wird, gibt [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) NULL zurück.</span><span class="sxs-lookup"><span data-stu-id="85ca6-125">If the operation completes successfully, [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) returns zero.</span></span>

<span data-ttu-id="85ca6-126">Wenn der Vorgang fehlschlägt, wird der Wert Socket \_ Error zurückgegeben, und es kann ein spezifischer Fehlercode durch Aufrufen von [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="85ca6-126">If the operation fails, a value of SOCKET\_ERROR is returned and a specific error code can be retrieved by calling [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>



| <span data-ttu-id="85ca6-127">Fehlercode</span><span class="sxs-lookup"><span data-stu-id="85ca6-127">Error code</span></span>                                                                                                                                              | <span data-ttu-id="85ca6-128">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="85ca6-128">Meaning</span></span>                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="85ca6-129"><dt>**[WSANOTINITIALISED](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="85ca6-129"><dt>**[WSANOTINITIALISED](windows-sockets-error-codes-2.md)**</dt></span></span> </dl> | <span data-ttu-id="85ca6-130">Ein erfolgreicher [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) -Befehl muss vor der Verwendung dieser Funktion ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="85ca6-130">A successful [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) call must occur before using this function.</span></span><br/>                                                                                                                                                                                     |
| <dl> <span data-ttu-id="85ca6-131"><dt>**[WSAENETDOWN](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="85ca6-131"><dt>**[WSAENETDOWN](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>             | <span data-ttu-id="85ca6-132">Das Netzwerk Subsystem ist fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="85ca6-132">The network subsystem has failed.</span></span><br/>                                                                                                                                                                                                                                               |
| <dl> <span data-ttu-id="85ca6-133"><dt>**[WSAEFAULT](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="85ca6-133"><dt>**[WSAEFAULT](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>                 | <span data-ttu-id="85ca6-134">Einer der *optval* -oder *optlen* -Parameter verweist auf den Arbeitsspeicher, der sich nicht in einem gültigen Teil des Benutzer Adressraums befindet.</span><span class="sxs-lookup"><span data-stu-id="85ca6-134">One of the *optval* or the *optlen* parameters point to memory that is not in a valid part of the user address space.</span></span> <span data-ttu-id="85ca6-135">Dieser Fehler wird auch zurückgegeben, wenn der Wert, auf den der *optlen* -Parameter verweist, kleiner ist als die Größe einer [**csaddr- \_ Informations**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) Struktur.</span><span class="sxs-lookup"><span data-stu-id="85ca6-135">This error is also returned if the value pointed to by the *optlen* parameter is less than the size of a [**CSADDR\_INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) structure.</span></span><br/> |
| <dl> <span data-ttu-id="85ca6-136"><dt>**[Wsaeingabe Progress](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="85ca6-136"><dt>**[WSAEINPROGRESS](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>       | <span data-ttu-id="85ca6-137">Ein blockierender Windows Sockets 1,1-Rückruf wird gerade ausgeführt, oder der Dienstanbieter verarbeitet weiterhin eine Rückruffunktion.</span><span class="sxs-lookup"><span data-stu-id="85ca6-137">A blocking Windows Sockets 1.1 call is in progress, or the service provider is still processing a callback function.</span></span><br/>                                                                                                                                                            |
| <dl> <span data-ttu-id="85ca6-138"><dt>**[Wsaabval](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="85ca6-138"><dt>**[WSAEINVAL](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>                 | <span data-ttu-id="85ca6-139">Der *Level* -Parameter ist unbekannt oder ungültig.</span><span class="sxs-lookup"><span data-stu-id="85ca6-139">The *level* parameter is unknown or invalid.</span></span><br/>                                                                                                                                                                                                                                    |
| <dl> <span data-ttu-id="85ca6-140"><dt>**[Wsaumoproumopt](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="85ca6-140"><dt>**[WSAENOPROTOOPT](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>       | <span data-ttu-id="85ca6-141">Die Option ist unbekannt oder wird von der angegebener Protokollfamilie nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="85ca6-141">The option is unknown or unsupported by the indicated protocol family.</span></span><br/>                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="85ca6-142"><dt>**[Wsaumotsock](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="85ca6-142"><dt>**[WSAENOTSOCK](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>             | <span data-ttu-id="85ca6-143">Der Deskriptor ist kein Socket.</span><span class="sxs-lookup"><span data-stu-id="85ca6-143">The descriptor is not a socket.</span></span><br/>                                                                                                                                                                                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="85ca6-144">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="85ca6-144">Remarks</span></span>

<span data-ttu-id="85ca6-145">Die [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) -Funktion, die mit der " **so \_ BSP \_ State** Socket"-Option aufgerufen wird, ruft die lokale Adresse, den lokalen Port, die Remote Adresse, den Remoteport, den Sockettyp und das Protokoll ab, die von</span><span class="sxs-lookup"><span data-stu-id="85ca6-145">The [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) function called with the **SO\_BSP\_STATE** socket option retrieves the local address, local port, remote address, remote port, socket type, and protocol used by a socket.</span></span> <span data-ttu-id="85ca6-146">Die Option " **so \_ BSP \_ State** Socket" funktioniert mit IPv6-oder IPv4-Sockets (der " **AF \_ inet6** " und " **AF \_ inet** Address Families").</span><span class="sxs-lookup"><span data-stu-id="85ca6-146">The **SO\_BSP\_STATE** socket option works with IPv6 or IPv4 sockets (the **AF\_INET6** and **AF\_INET** address families).</span></span>

<span data-ttu-id="85ca6-147">Wenn die [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) -Funktion erfolgreich ist, werden die Informationen in einer [**csaddr \_**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) -Informationsstruktur im Puffer zurückgegeben, auf den der *optval* -Parameter zeigt.</span><span class="sxs-lookup"><span data-stu-id="85ca6-147">If the [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) function is successful, the information is returned in a [**CSADDR\_INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) structure in the buffer pointed to by the *optval* parameter.</span></span> <span data-ttu-id="85ca6-148">Die Ganzzahl, auf die *optlen* zeigt, sollte ursprünglich die Größe dieses Puffers enthalten. bei der Rückgabe wird die Länge des Werts, der im *optval* -Parameter zurückgegeben wird, auf die Länge in Bytes festgelegt.</span><span class="sxs-lookup"><span data-stu-id="85ca6-148">The integer pointed to by *optlen* should originally contain the size of this buffer; on return, it will be set to the length, in bytes, of the value returned in the *optval* parameter.</span></span>

<span data-ttu-id="85ca6-149">Die Member **isockettype** und **iProtocol** in der zurückgegebenen [**csaddr- \_ Informations**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) Struktur werden für den socketdeskriptor im *s* -Parameter ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="85ca6-149">The **iSocketType** and **iProtocol** members in the returned [**CSADDR\_INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) structure are filled in for the socket descriptor in the *s* parameter.</span></span>

<span data-ttu-id="85ca6-150">Wenn sich der Socket in einem verbundenen oder gebundenen Zustand befindet, wird der **localaddr** -Member der zurückgegebenen [**csaddr- \_ Informations**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) Struktur auf eine [sockaddr](sockaddr-2.md) -Struktur festgelegt, die die lokale Adresse und den Port darstellt.</span><span class="sxs-lookup"><span data-stu-id="85ca6-150">If the socket is in a connected or bound state, then the **LocalAddr** member of the returned [**CSADDR\_INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) structure will be set to a [SOCKADDR](sockaddr-2.md) structure representing the local address and port.</span></span> <span data-ttu-id="85ca6-151">Wenn sich der Socket in einem verbundenen Zustand befindet, wird der **remoteaddr** -Member der zurückgegebenen **csaddr- \_ Informations** Struktur auf eine sockaddr-Struktur festgelegt, die die Remote Adresse und den Port darstellt.</span><span class="sxs-lookup"><span data-stu-id="85ca6-151">If the socket is in a connected state, then the **RemoteAddr** member of the returned **CSADDR\_INFO** structure will be set to a SOCKADDR structure representing the remote address and port.</span></span>

<span data-ttu-id="85ca6-152">Wenn sich der Socket nicht in einem verbundenen oder gebundenen Zustand befindet, wird der **localaddr** -Member der zurückgegebenen [**csaddr- \_ Informations**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) Struktur mit einem **null** -Zeiger im **lpsockaddr** -Member und dem **isockaddrlength** -Element auf 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="85ca6-152">If the socket is not in a connected or bound state, then the **LocalAddr** member of the returned [**CSADDR\_INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) structure is returned with a **NULL** pointer in the **lpSockaddr** member and the **iSockaddrLength** member set to zero.</span></span> <span data-ttu-id="85ca6-153">Wenn sich der Socket nicht in einem gebundenen Zustand befindet, wird der **remoteaddr** -Member der zurückgegebenen **csaddr- \_ Informations** Struktur mit einem **null** -Zeiger im **lpsockaddr** -Member und dem **isockaddrlength** -Element auf 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="85ca6-153">If the socket is not in a bound state, then the **RemoteAddr** member of the returned **CSADDR\_INFO** structure is returned with a **NULL** pointer in the **lpSockaddr** member and the **iSockaddrLength** member set to zero.</span></span>

<span data-ttu-id="85ca6-154">Wenn die [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) -Funktion ausfällt, bleiben die *optval* -und *optlen* -Parameter unverändert, und der *optval* -Parameter verweist nicht auf eine zurückgegebene [**csaddr- \_ Informations**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) Struktur.</span><span class="sxs-lookup"><span data-stu-id="85ca6-154">If the [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) function fails, the *optval* and *optlen* parameters are left unchanged and the *optval* parameter does not point to a returned [**CSADDR\_INFO**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) structure.</span></span>

<span data-ttu-id="85ca6-155">Beachten Sie, dass die Header Datei " *Ws2def. h* " automatisch in " *Winsock2. h*" enthalten ist und niemals direkt verwendet werden sollte.</span><span class="sxs-lookup"><span data-stu-id="85ca6-155">Note that the *Ws2def.h* header file is automatically included in *Winsock2.h*, and should never be used directly.</span></span>

## <a name="requirements"></a><span data-ttu-id="85ca6-156">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="85ca6-156">Requirements</span></span>



| <span data-ttu-id="85ca6-157">Anforderung</span><span class="sxs-lookup"><span data-stu-id="85ca6-157">Requirement</span></span> | <span data-ttu-id="85ca6-158">Wert</span><span class="sxs-lookup"><span data-stu-id="85ca6-158">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85ca6-159">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="85ca6-159">Minimum supported client</span></span><br/> | <span data-ttu-id="85ca6-160">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="85ca6-160">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="85ca6-161">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="85ca6-161">Minimum supported server</span></span><br/> | <span data-ttu-id="85ca6-162">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="85ca6-162">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="85ca6-163">Header</span><span class="sxs-lookup"><span data-stu-id="85ca6-163">Header</span></span><br/>                   | <dl> <span data-ttu-id="85ca6-164"><dt>Ws2def. h (Include Winsock2. h)</dt></span><span class="sxs-lookup"><span data-stu-id="85ca6-164"><dt>Ws2def.h (include Winsock2.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85ca6-165">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="85ca6-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85ca6-166">**getsockopt**</span><span class="sxs-lookup"><span data-stu-id="85ca6-166">**getsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[<span data-ttu-id="85ca6-167">**csaddr- \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="85ca6-167">**CSADDR\_INFO**</span></span>](/windows/win32/api/ws2def/ns-ws2def-csaddr_info)
</dt> <dt>

[<span data-ttu-id="85ca6-168">SOCKADDR</span><span class="sxs-lookup"><span data-stu-id="85ca6-168">SOCKADDR</span></span>](sockaddr-2.md)
</dt> </dl>

 

 
