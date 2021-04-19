---
description: Ist so konzipiert, dass eine Anwendung entscheiden kann, ob eine eingehende Verbindung für einen Abhör Socket angenommen werden soll oder nicht.
ms.assetid: 964683eb-5dfc-4441-abb7-315be8b89a19
title: SO_CONDITIONAL_ACCEPT Socket-Option (Ws2def. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: badfdd1f8aac49ae05fa6b77dadb2561ba5ea02f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366073"
---
# <a name="so_conditional_accept-socket-option"></a><span data-ttu-id="d27cc-103">" \_ Conditional \_ Accept"-Socketoption</span><span class="sxs-lookup"><span data-stu-id="d27cc-103">SO\_CONDITIONAL\_ACCEPT socket option</span></span>

<span data-ttu-id="d27cc-104">Die Option " **so \_ bedingtes \_ akzeptieren** " ermöglicht es einer Anwendung, zu entscheiden, ob eine eingehende Verbindung für einen Abhör Socket angenommen werden soll oder nicht.</span><span class="sxs-lookup"><span data-stu-id="d27cc-104">The **SO\_CONDITIONAL\_ACCEPT** socket option is designed to allow an application to decide whether or not to accept an incoming connection on a listening socket.</span></span>

## <a name="socket-option-value"></a><span data-ttu-id="d27cc-105">Wert der Socketoption</span><span class="sxs-lookup"><span data-stu-id="d27cc-105">Socket option value</span></span>

<span data-ttu-id="d27cc-106">Die Konstante, die diese Socketoption darstellt, ist 0x3002.</span><span class="sxs-lookup"><span data-stu-id="d27cc-106">The constant that represents this socket option is 0x3002.</span></span>

## <a name="syntax"></a><span data-ttu-id="d27cc-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d27cc-107">Syntax</span></span>


```C++
int setsockopt(
  (SOCKET) s,      // descriptor identifying a socket 
  (int) SOL_SOCKET,   // level
  (int) SO_CONDITIONAL_ACCEPT, // optname
  (char *) optval,         // input buffer,
  (int) optlen,       // size of input buffer
);
```



## <a name="parameters"></a><span data-ttu-id="d27cc-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="d27cc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d27cc-109">*s* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d27cc-109">*s* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d27cc-110">Ein Deskriptor, der den Socket identifiziert.</span><span class="sxs-lookup"><span data-stu-id="d27cc-110">A descriptor identifying the socket.</span></span>

</dd> <dt>

<span data-ttu-id="d27cc-111">*Ebene* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d27cc-111">*level* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d27cc-112">Die Ebene, auf der die Option definiert ist.</span><span class="sxs-lookup"><span data-stu-id="d27cc-112">The level at which the option is defined.</span></span> <span data-ttu-id="d27cc-113">Verwenden Sie für diesen Vorgang den **Sol- \_ Socket** .</span><span class="sxs-lookup"><span data-stu-id="d27cc-113">Use **SOL\_SOCKET** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="d27cc-114">*optname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d27cc-114">*optname* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d27cc-115">Die Socketoption, für die der Wert festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d27cc-115">The socket option for which the value is to be set.</span></span> <span data-ttu-id="d27cc-116">Verwenden Sie **daher den \_ bedingten \_ Accept** für diesen Vorgang.</span><span class="sxs-lookup"><span data-stu-id="d27cc-116">Use **SO\_CONDITIONAL\_ACCEPT** for this operation.</span></span>

</dd> <dt>

<span data-ttu-id="d27cc-117">*optval* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="d27cc-117">*optval* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d27cc-118">Ein Zeiger auf den Puffer, der den Wert für die festzulegende Option enthält.</span><span class="sxs-lookup"><span data-stu-id="d27cc-118">A pointer to the buffer containing the value for the option to set.</span></span> <span data-ttu-id="d27cc-119">Dieser Parameter sollte auf einen Puffer zeigen, der größer oder gleich der Größe eines **DWORD** -Werts ist.</span><span class="sxs-lookup"><span data-stu-id="d27cc-119">This parameter should point to buffer equal to or larger than the size of a **DWORD** value.</span></span>

<span data-ttu-id="d27cc-120">Dieser Wert wird als boolescher Wert behandelt, wobei 0 verwendet wird, um **false** (deaktiviert) und einen Wert ungleich 0 (null) anzugeben, um **true** (aktiviert) anzugeben.</span><span class="sxs-lookup"><span data-stu-id="d27cc-120">This value is treated as a boolean value with 0 used to indicate **FALSE** (disabled) and a nonzero value to indicate **TRUE** (enabled).</span></span>

</dd> <dt>

<span data-ttu-id="d27cc-121">*optlen* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="d27cc-121">*optlen* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d27cc-122">Ein Zeiger auf die Größe des *optval* -Puffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="d27cc-122">A pointer to the size, in bytes, of the *optval* buffer.</span></span> <span data-ttu-id="d27cc-123">Diese Größe muss größer oder gleich der Größe eines **DWORD** -Werts sein.</span><span class="sxs-lookup"><span data-stu-id="d27cc-123">This size must be equal to or larger than the size of a **DWORD** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d27cc-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d27cc-124">Return value</span></span>

<span data-ttu-id="d27cc-125">Wenn der Vorgang erfolgreich abgeschlossen wird, gibt [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="d27cc-125">If the operation completes successfully, [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) returns zero.</span></span>

<span data-ttu-id="d27cc-126">Wenn der Vorgang fehlschlägt, wird der Wert Socket \_ Error zurückgegeben, und es kann ein spezifischer Fehlercode durch Aufrufen von [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="d27cc-126">If the operation fails, a value of SOCKET\_ERROR is returned and a specific error code can be retrieved by calling [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).</span></span>



| <span data-ttu-id="d27cc-127">Fehlercode</span><span class="sxs-lookup"><span data-stu-id="d27cc-127">Error code</span></span>                                                                                                                                              | <span data-ttu-id="d27cc-128">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="d27cc-128">Meaning</span></span>                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d27cc-129"><dt>**[WSANOTINITIALISED](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="d27cc-129"><dt>**[WSANOTINITIALISED](windows-sockets-error-codes-2.md)**</dt></span></span> </dl> | <span data-ttu-id="d27cc-130">Ein erfolgreicher [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) -Befehl muss vor der Verwendung dieser Funktion ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="d27cc-130">A successful [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) call must occur before using this function.</span></span><br/>                                                                                                                                                     |
| <dl> <span data-ttu-id="d27cc-131"><dt>**[WSAENETDOWN](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="d27cc-131"><dt>**[WSAENETDOWN](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>             | <span data-ttu-id="d27cc-132">Das Netzwerk Subsystem ist fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="d27cc-132">The network subsystem has failed.</span></span><br/>                                                                                                                                                                                                               |
| <dl> <span data-ttu-id="d27cc-133"><dt>**[WSAEFAULT](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="d27cc-133"><dt>**[WSAEFAULT](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>                 | <span data-ttu-id="d27cc-134">Einer der *optval* -oder *optlen* -Parameter verweist auf den Arbeitsspeicher, der sich nicht in einem gültigen Teil des Benutzer Adressraums befindet.</span><span class="sxs-lookup"><span data-stu-id="d27cc-134">One of the *optval* or the *optlen* parameters point to memory that is not in a valid part of the user address space.</span></span> <span data-ttu-id="d27cc-135">Dieser Fehler wird auch zurückgegeben, wenn der Wert, auf den der *optlen* -Parameter verweist, kleiner ist als die Größe eines **DWORD** -Werts.</span><span class="sxs-lookup"><span data-stu-id="d27cc-135">This error is also returned if the value pointed to by the *optlen* parameter is less than the size of a **DWORD** value.</span></span><br/> |
| <dl> <span data-ttu-id="d27cc-136"><dt>**[Wsaeingabe Progress](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="d27cc-136"><dt>**[WSAEINPROGRESS](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>       | <span data-ttu-id="d27cc-137">Ein blockierender Windows Sockets 1,1-Rückruf wird gerade ausgeführt, oder der Dienstanbieter verarbeitet weiterhin eine Rückruffunktion.</span><span class="sxs-lookup"><span data-stu-id="d27cc-137">A blocking Windows Sockets 1.1 call is in progress, or the service provider is still processing a callback function.</span></span><br/>                                                                                                                            |
| <dl> <span data-ttu-id="d27cc-138"><dt>**[Wsaabval](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="d27cc-138"><dt>**[WSAEINVAL](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>                 | <span data-ttu-id="d27cc-139">Der *Level* -Parameter ist unbekannt oder ungültig.</span><span class="sxs-lookup"><span data-stu-id="d27cc-139">The *level* parameter is unknown or invalid.</span></span> <span data-ttu-id="d27cc-140">Dieser Fehler wird auch zurückgegeben, wenn sich der Socket bereits in einem Empfangs Zustand befunden hat.</span><span class="sxs-lookup"><span data-stu-id="d27cc-140">This error is also returned if the socket was already in a listening state.</span></span><br/>                                                                                                                        |
| <dl> <span data-ttu-id="d27cc-141"><dt>**[Wsaumoproumopt](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="d27cc-141"><dt>**[WSAENOPROTOOPT](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>       | <span data-ttu-id="d27cc-142">Die Option ist unbekannt oder wird von der angegebener Protokollfamilie nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d27cc-142">The option is unknown or unsupported by the indicated protocol family.</span></span><br/>                                                                                                                                                                          |
| <dl> <span data-ttu-id="d27cc-143"><dt>**[Wsaumotsock](windows-sockets-error-codes-2.md)**</dt></span><span class="sxs-lookup"><span data-stu-id="d27cc-143"><dt>**[WSAENOTSOCK](windows-sockets-error-codes-2.md)**</dt></span></span> </dl>             | <span data-ttu-id="d27cc-144">Der Deskriptor ist kein Socket.</span><span class="sxs-lookup"><span data-stu-id="d27cc-144">The descriptor is not a socket.</span></span><br/>                                                                                                                                                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="d27cc-145">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d27cc-145">Remarks</span></span>

<span data-ttu-id="d27cc-146">Die [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) -Funktion, die mit der " **so \_ Conditional \_ Accept** Socket"-Option aufgerufen wird, ermöglicht einer Anwendung, zu entscheiden, ob eine eingehende Verbindung für einen Abhör Socket angenommen werden soll.</span><span class="sxs-lookup"><span data-stu-id="d27cc-146">The [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function called with the **SO\_CONDITIONAL\_ACCEPT** socket option allows an application to decide whether or not to accept an incoming connection on a listening socket.</span></span> <span data-ttu-id="d27cc-147">Die Option für den bedingten Annahme für einen Socket ist standardmäßig deaktiviert (auf **false** festgelegt).</span><span class="sxs-lookup"><span data-stu-id="d27cc-147">The conditional accept option for a socket is disabled (set to **FALSE**) by default.</span></span>

<span data-ttu-id="d27cc-148">Wenn diese Socketoption aktiviert ist, akzeptiert der TCP-Stapel keine Verbindungen automatisch.</span><span class="sxs-lookup"><span data-stu-id="d27cc-148">When this socket option is enabled, the TCP stack does not automatically accept connections.</span></span> <span data-ttu-id="d27cc-149">Die Anwendung wartet darauf, dass die Anwendung anzeigt, dass Sie die Verbindung über den bedingten Accept-Rückruf annimmt, der bei der [**wsaaccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) -Funktion registriert ist.</span><span class="sxs-lookup"><span data-stu-id="d27cc-149">It waits for the application to indicate that it accepts the connection via the conditional accept callback registered with [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) function.</span></span> <span data-ttu-id="d27cc-150">Nachdem eine Verbindungsanforderung empfangen wurde, ruft Winsock den von der Anwendung registrierten bedingten Accept-Rückruf auf.</span><span class="sxs-lookup"><span data-stu-id="d27cc-150">Once a connection request is received, Winsock invokes the conditional accept callback registered by the application.</span></span> <span data-ttu-id="d27cc-151">Nur wenn der bedingte Accept-Rückruf " **CF \_ Accept** " zurückgibt, benachrichtigt Winsock den Transport, dass die Verbindung vollständig akzeptiert wird.</span><span class="sxs-lookup"><span data-stu-id="d27cc-151">Only when the conditional accept callback returns **CF\_ACCEPT** will Winsock notify the transport to fully accept the connection.</span></span>

<span data-ttu-id="d27cc-152">Wenn die Option für den **sogenannten \_ bedingten \_ Accept** -Socket auf aktiviert (auf **true** festgelegt) festgelegt ist, hat dies mehrere Nebeneffekte auf den Socket:</span><span class="sxs-lookup"><span data-stu-id="d27cc-152">When the **SO\_CONDITIONAL\_ACCEPT** socket option is set to enabled (set to **TRUE**), this has several side effects on the socket:</span></span>

-   <span data-ttu-id="d27cc-153">Dadurch wird die integrierte Schutzmaßnahmen für den SYN-Angriff des TCP-Stapels deaktiviert, da die Anwendung jetzt den Besitz nimmt, Verbindungen zu akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="d27cc-153">This disables the TCP stack's built-in SYN attack protection defenses, since the application is now taking ownership of accepting connections.</span></span>
-   <span data-ttu-id="d27cc-154">Dadurch wird der Abhör Rückstand deaktiviert, da Verbindungen im Namen eines Abhör Sockets nicht akzeptiert werden.</span><span class="sxs-lookup"><span data-stu-id="d27cc-154">This effectively disables the listen backlog since connections aren't accepted on behalf of a listening socket.</span></span> <span data-ttu-id="d27cc-155">Eine Verbindung wird niemals vollständig akzeptiert, bis die Anwendung die Verwendung des **CF- \_ Accept** -Mechanismus vollständig akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="d27cc-155">A connection is never fully accepted until the application fully accepts using the **CF\_ACCEPT** mechanism.</span></span>
-   <span data-ttu-id="d27cc-156">Dies bedeutet auch, dass die Anwendung immer in einem-Zustand sein muss, um die Accept-Rückrufe zur Annahme der Verbindung schnell verarbeiten zu können.</span><span class="sxs-lookup"><span data-stu-id="d27cc-156">This also means the application take care to always be in a state to readily handle the accept callbacks to accept the connection.</span></span> <span data-ttu-id="d27cc-157">Wenn die Anwendung mit einer anderen Verarbeitung ausgelastet ist, kann ein Timeout der Clientseite auftreten, bevor die Anwendung die Verbindung tatsächlich akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="d27cc-157">If the application is busy doing other processing, then the client side may time out before the application actually accepts the connection.</span></span> <span data-ttu-id="d27cc-158">Dies führt zu einem schlechten Client Verhalten.</span><span class="sxs-lookup"><span data-stu-id="d27cc-158">This leads to a poor client experience.</span></span>

<span data-ttu-id="d27cc-159">Der Hauptgrund für Anwendungen, die die bedingte Annahme verwenden, ist die Überprüfung der Quell-IP-Adresse oder des Ports, der vom Verbindungs Client verwendet wird, und dann die Annahme oder Ablehnung der Verbindung zu beschließen.</span><span class="sxs-lookup"><span data-stu-id="d27cc-159">Generally, the main reason applications use conditional accept is to inspect the source IP address or port used by the connecting client and then decide to accept or reject the connection.</span></span> <span data-ttu-id="d27cc-160">Allerdings ist es wahrscheinlich, dass Anwendungen besser funktionieren, wenn die Option "so \_ bedingtes \_ akzeptieren" nicht aktiviert ist und die Anwendung zulässt, dass der TCP-Stapel und der Abhör Rückstand erwartungsgemäß funktionieren.</span><span class="sxs-lookup"><span data-stu-id="d27cc-160">However, applications are likely to perform better if the SO\_CONDITIONAL\_ACCEPT option is not enabled and the application allows the TCP stack and the listen backlog to work as expected.</span></span> <span data-ttu-id="d27cc-161">Wenn die Anwendung dann die akzeptierte Verbindung verarbeitet, kann die Anwendung, wenn Sie von einer ungültigen IP-Quelladresse oder einem Port entfernt wird, den Socket einfach schließen.</span><span class="sxs-lookup"><span data-stu-id="d27cc-161">Then when the application handles the accepted connection, if it is from a improper IP source address or port, the application can just close the socket.</span></span> <span data-ttu-id="d27cc-162">Der Sicherheits Nachteil dieses Verhaltens besteht darin, dass der Client nun bestätigt hat, dass die Anwendung eine IP-Adresse und einen Port abhört, da die zuvor akzeptierte Verbindung erzwungen wurde.</span><span class="sxs-lookup"><span data-stu-id="d27cc-162">The security drawback to this behavior is that now the client has confirmation that the application is listening on an IP address and port since it forcefully closed the previously accepted connection.</span></span> <span data-ttu-id="d27cc-163">Allerdings wiegen die Nachteile der Aktivierung von **\_ bedingtem \_ Accept** in der Regel diese Einschränkung aus.</span><span class="sxs-lookup"><span data-stu-id="d27cc-163">However, the drawbacks to enabling **SO\_CONDITIONAL\_ACCEPT** generally outweigh this limitation.</span></span>

<span data-ttu-id="d27cc-164">Die [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) -Funktion, die mit der " **so \_ Conditional \_ Accept** Socket"-Option aufgerufen wird, ermöglicht einer Anwendung, den aktuellen Zustand der Option "bedingtes akzeptieren" abzurufen, obwohl diese Funktion normalerweise nicht verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d27cc-164">The [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) function called with the **SO\_CONDITIONAL\_ACCEPT** socket option allows an application to retrieve the current state of the conditional accept option, although this is feature not normally used.</span></span> <span data-ttu-id="d27cc-165">Wenn eine Anwendung den bedingten Accept-Vorgang für einen Socket aktivieren muss, ruft Sie Justs die [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) -Funktion auf, um die Option zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="d27cc-165">If an application needs to enable conditional accept on a socket, it justs calls the [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function to enable the option.</span></span>

<span data-ttu-id="d27cc-166">Beachten Sie, dass die Header Datei " *Ws2def. h* " automatisch in " *Winsock2. h*" enthalten ist und niemals direkt verwendet werden sollte.</span><span class="sxs-lookup"><span data-stu-id="d27cc-166">Note that the *Ws2def.h* header file is automatically included in *Winsock2.h*, and should never be used directly.</span></span>

## <a name="requirements"></a><span data-ttu-id="d27cc-167">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d27cc-167">Requirements</span></span>



| <span data-ttu-id="d27cc-168">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d27cc-168">Requirement</span></span> | <span data-ttu-id="d27cc-169">Wert</span><span class="sxs-lookup"><span data-stu-id="d27cc-169">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d27cc-170">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d27cc-170">Minimum supported client</span></span><br/> | <span data-ttu-id="d27cc-171">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d27cc-171">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d27cc-172">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d27cc-172">Minimum supported server</span></span><br/> | <span data-ttu-id="d27cc-173">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d27cc-173">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d27cc-174">Header</span><span class="sxs-lookup"><span data-stu-id="d27cc-174">Header</span></span><br/>                   | <dl> <span data-ttu-id="d27cc-175"><dt>Ws2def. h (Include Winsock2. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d27cc-175"><dt>Ws2def.h (include Winsock2.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d27cc-176">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d27cc-176">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d27cc-177">**getsockopt**</span><span class="sxs-lookup"><span data-stu-id="d27cc-177">**getsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[<span data-ttu-id="d27cc-178">**setsockopt**</span><span class="sxs-lookup"><span data-stu-id="d27cc-178">**setsockopt**</span></span>](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> <dt>

[<span data-ttu-id="d27cc-179">**Wsaaccept**</span><span class="sxs-lookup"><span data-stu-id="d27cc-179">**WSAAccept**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept)
</dt> </dl>

 

 




