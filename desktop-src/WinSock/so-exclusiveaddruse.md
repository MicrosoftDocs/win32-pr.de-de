---
description: Mit der "so \_ exclusiveaddruse"-Socketoption wird verhindert, dass andere Sockets an dieselbe Adresse und denselben Port gebunden werden.
ms.assetid: ce0d8188-54be-46e8-8753-d0680f690b84
title: SO_EXCLUSIVEADDRUSE Socket-Option (Winsock2. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90d4747150f918a7e9c4ce37ec209e7261d1a00c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348772"
---
# <a name="so_exclusiveaddruse-socket-option"></a><span data-ttu-id="da3ea-103">" \_ Exclusiveaddruse"-Socketoption</span><span class="sxs-lookup"><span data-stu-id="da3ea-103">SO\_EXCLUSIVEADDRUSE socket option</span></span>

<span data-ttu-id="da3ea-104">Mit der "so \_ exclusiveaddruse"-Socketoption wird verhindert, dass andere Sockets an dieselbe Adresse und denselben Port gebunden werden.</span><span class="sxs-lookup"><span data-stu-id="da3ea-104">The SO\_EXCLUSIVEADDRUSE socket option prevents other sockets from being forcibly bound to the same address and port.</span></span>

## <a name="syntax"></a><span data-ttu-id="da3ea-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="da3ea-105">Syntax</span></span>

<span data-ttu-id="da3ea-106">Die Option "so \_ exclusiveaddruse" verhindert, dass andere Sockets zwangsweise an dieselbe Adresse und denselben Port gebunden werden, eine Übung, die von der so \_ reuseaddr-Socketoption aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="da3ea-106">The SO\_EXCLUSIVEADDRUSE option prevents other sockets from being forcibly bound to the same address and port, a practice enabled by the SO\_REUSEADDR socket option.</span></span> <span data-ttu-id="da3ea-107">Eine solche Wiederverwendung kann von böswilligen Anwendungen ausgeführt werden, um die Anwendung zu unterbrechen.</span><span class="sxs-lookup"><span data-stu-id="da3ea-107">Such reuse can be executed by malicious applications to disrupt the application.</span></span> <span data-ttu-id="da3ea-108">Die Option "so \_ exclusiveaddruse" ist sehr nützlich für Systemdienste, die Hochverfügbarkeit erfordern.</span><span class="sxs-lookup"><span data-stu-id="da3ea-108">The SO\_EXCLUSIVEADDRUSE option is very useful to system services requiring high availability.</span></span>

<span data-ttu-id="da3ea-109">Im folgenden Codebeispiel wird das Festlegen dieser Option veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="da3ea-109">The following code example illustrates setting this option.</span></span>


```C++
#ifndef UNICODE
#define UNICODE
#endif

#ifndef WIN32_LEAN_AND_MEAN
#define WIN32_LEAN_AND_MEAN
#endif

#include <windows.h>
#include <winsock2.h>
#include <ws2tcpip.h>
#include <stdio.h>
#include <stdlib.h>             // Needed for _wtoi

#pragma comment(lib, "Ws2_32.lib")

int __cdecl wmain(int argc, wchar_t ** argv)
{
    WSADATA wsaData;
    int iResult = 0;
    int iError = 0;

    SOCKET s = INVALID_SOCKET;
    SOCKADDR_IN saLocal;
    int iOptval = 0;

    int iFamily = AF_UNSPEC;
    int iType = 0;
    int iProtocol = 0;

    int iPort = 0;

    // Validate the parameters
    if (argc != 5) {
        wprintf(L"usage: %ws <addressfamily> <type> <protocol> <port>\n", argv[0]);
        wprintf(L"    opens a socket for the specified family, type, & protocol\n");
        wprintf(L"    sets the SO_EXCLUSIVEADDRUSE socket option on the socket\n");
        wprintf(L"    then tries to bind the port specified on the command-line\n");
        wprintf(L"%ws example usage\n", argv[0]);
        wprintf(L"   %ws 0 2 17 5150\n", argv[0]);
        wprintf(L"   where AF_UNSPEC=0 SOCK_DGRAM=2 IPPROTO_UDP=17  PORT=5150\n",
                argv[0]);
        wprintf(L"   %ws 2 1 17 5150\n", argv[0]);
        wprintf(L"   where AF_INET=2 SOCK_STREAM=1 IPPROTO_TCP=6  PORT=5150\n", argv[0]);
        wprintf(L"   See the documentation for the socket function for other values\n");
        return 1;
    }

    iFamily = _wtoi(argv[1]);
    iType = _wtoi(argv[2]);
    iProtocol = _wtoi(argv[3]);

    iPort = _wtoi(argv[4]);

    if (iFamily != AF_INET && iFamily != AF_INET6) {
        wprintf(L"Address family must be either AF_INET (2) or AF_INET6 (23)\n");
        return 1;
    }

    if (iPort <= 0 || iPort >= 65535) {
        wprintf(L"Port specified must be greater than 0 and less than 65535\n");
        return 1;
    }
    // Initialize Winsock
    iResult = WSAStartup(MAKEWORD(2, 2), &wsaData);
    if (iResult != 0) {
        wprintf(L"WSAStartup failed with error: %d\n", iResult);
        return 1;
    }
    // Create the socket
    s = socket(iFamily, iType, iProtocol);
    if (s == INVALID_SOCKET) {
        wprintf(L"socket failed with error: %ld\n", WSAGetLastError());
        WSACleanup();
        return 1;
    }
    // Set the exclusive address option
    iOptval = 1;
    iResult = setsockopt(s, SOL_SOCKET, SO_EXCLUSIVEADDRUSE,
                         (char *) &iOptval, sizeof (iOptval));
    if (iResult == SOCKET_ERROR) {
        wprintf(L"setsockopt for SO_EXCLUSIVEADDRUSE failed with error: %ld\n",
                WSAGetLastError());
    }

    saLocal.sin_family = (ADDRESS_FAMILY) iFamily;
    saLocal.sin_port = htons( (u_short) iPort);
    saLocal.sin_addr.s_addr = htonl(INADDR_ANY);

    // Bind the socket
    iResult = bind(s, (SOCKADDR *) & saLocal, sizeof (saLocal));
    if (iResult == SOCKET_ERROR) {

        // Most errors related to setting SO_EXCLUSIVEADDRUSE
        //    will occur at bind.
        iError = WSAGetLastError();
        if (iError == WSAEACCES)
            wprintf(L"bind failed with WSAEACCES (access denied)\n");
        else
            wprintf(L"bind failed with error: %ld\n", iError);

    } else {
        wprintf(L"bind on socket with SO_EXCLUSIVEADDRUSE succeeded to port: %ld\n",
                iPort);
    }

    // cleanup
    closesocket(s);
    WSACleanup();

    return 0;
}

```



<span data-ttu-id="da3ea-110">Um einen Effekt zu haben, muss die Option "so \_ exclusivaddruse" festgelegt werden, bevor die [**Bind**](/windows/desktop/api/winsock/nf-winsock-bind) -Funktion aufgerufen wird (Dies gilt auch für die \_ Option "reuseaddr").</span><span class="sxs-lookup"><span data-stu-id="da3ea-110">To have any effect, the SO\_EXCLUSIVADDRUSE option must be set before the [**bind**](/windows/desktop/api/winsock/nf-winsock-bind) function is called (this also applies to the SO\_REUSEADDR option).</span></span> <span data-ttu-id="da3ea-111">In Tabelle 1 werden die Auswirkungen der Einstellung der \_ Option "so exclusiveaddruse" aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="da3ea-111">Table 1 lists the effects of setting the SO\_EXCLUSIVEADDRUSE option.</span></span> <span data-ttu-id="da3ea-112">Platzhalter gibt eine Bindung an die Platzhalter Adresse an, z. b. 0.0.0.0 für IPv4 und:: für IPv6.</span><span class="sxs-lookup"><span data-stu-id="da3ea-112">Wildcard indicates binding to the wildcard address, such as 0.0.0.0 for IPv4 and :: for IPv6.</span></span> <span data-ttu-id="da3ea-113">Spezifisch gibt eine Bindung an eine bestimmte Schnittstelle an, z. b. das Binden einer einem Adapter zugewiesenen IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="da3ea-113">Specific indicates binding to a specific interface, such as binding an IP address assigned to an adapter.</span></span> <span data-ttu-id="da3ea-114">Specific2 gibt an, dass die Bindung an eine bestimmte Adresse nicht an die Adresse gebunden ist, die im speziellen Fall an gebunden ist</span><span class="sxs-lookup"><span data-stu-id="da3ea-114">Specific2 indicates binding to a specific address other than the address bound to in the Specific case.</span></span>

> [!Note]  
> <span data-ttu-id="da3ea-115">Der Specific2-Fall ist nur anwendbar, wenn die erste Bindung mit einer bestimmten Adresse ausgeführt wird. für den Fall, in dem der erste Socket an den Platzhalter gebunden ist, deckt der Eintrag für "spezifisch" alle speziellen Adress Fälle ab.</span><span class="sxs-lookup"><span data-stu-id="da3ea-115">The Specific2 case is applicable only when the first bind is performed with a specific address; for the case in which the first socket is bound to the wildcard, the entry for Specific covers all specific address cases.</span></span>

 

<span data-ttu-id="da3ea-116">Nehmen Sie beispielsweise einen Computer mit zwei IP-Schnittstellen an: 10.0.0.1 und 10.99.99.99.</span><span class="sxs-lookup"><span data-stu-id="da3ea-116">For example, consider a computer with two IP interfaces: 10.0.0.1 and 10.99.99.99.</span></span> <span data-ttu-id="da3ea-117">Wenn die erste Bindung an 10.0.0.1 und Port 5150 mit der "so \_ exclusiveaddruse"-Option festgelegt ist, wird die zweite Bindung an 10.99.99.99 und Port 5150 mit einer oder ohne Optionen erfolgreich festgelegt.</span><span class="sxs-lookup"><span data-stu-id="da3ea-117">If the first bind is to 10.0.0.1 and port 5150 with the SO\_EXCLUSIVEADDRUSE option set, then the second bind to 10.99.99.99 and port 5150 with any or no options set succeeds.</span></span> <span data-ttu-id="da3ea-118">Wenn der erste Socket jedoch an die Platzhalter Adresse (0.0.0.0) und Port 5150 gebunden ist, wobei " \_ exclusiveaddruse" festgelegt ist, schlagen alle nachfolgenden Bindungen an denselben Port – unabhängig von der IP-Adresse – entweder mit WSAEADDRINUSE (10048) oder wsaeaccess (10013) fehl</span><span class="sxs-lookup"><span data-stu-id="da3ea-118">However, if the first socket is bound to the wildcard address (0.0.0.0) and port 5150 with SO\_EXCLUSIVEADDRUSE set, any subsequent bind to the same port—regardless of IP address—will fail with either WSAEADDRINUSE (10048) or WSAEACCESS (10013), depending on which options were set on the second bind socket.</span></span>

### <a name="bind-behavior-with-various-options-set"></a><span data-ttu-id="da3ea-119">Bindungsverhalten mit verschiedenen festgelegten Optionen</span><span class="sxs-lookup"><span data-stu-id="da3ea-119">Bind Behavior with Various Options Set</span></span>



<span data-ttu-id="da3ea-120">Zweite Bindung</span><span class="sxs-lookup"><span data-stu-id="da3ea-120">Second bind</span></span>

<span data-ttu-id="da3ea-121">Erste Bindung</span><span class="sxs-lookup"><span data-stu-id="da3ea-121">First bind</span></span>

<span data-ttu-id="da3ea-122">*" \_ exclusiveaddruse"*</span><span class="sxs-lookup"><span data-stu-id="da3ea-122">*SO\_EXCLUSIVEADDRUSE*</span></span>

<span data-ttu-id="da3ea-123">*Keine Optionen* oder *so \_ reuseaddr*</span><span class="sxs-lookup"><span data-stu-id="da3ea-123">*No options* or *SO\_REUSEADDR*</span></span>

<span data-ttu-id="da3ea-124">*Platzhalter*</span><span class="sxs-lookup"><span data-stu-id="da3ea-124">*Wildcard*</span></span>

<span data-ttu-id="da3ea-125">*Zugeschnitten*</span><span class="sxs-lookup"><span data-stu-id="da3ea-125">*Specific*</span></span>

<span data-ttu-id="da3ea-126">*Platzhalter*</span><span class="sxs-lookup"><span data-stu-id="da3ea-126">*Wildcard*</span></span>

<span data-ttu-id="da3ea-127">*Zugeschnitten*</span><span class="sxs-lookup"><span data-stu-id="da3ea-127">*Specific*</span></span>

<span data-ttu-id="da3ea-128">$ {ROWSPAN3} $*so \_ exclusiveaddruse*$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="da3ea-128">${ROWSPAN3}$*SO\_EXCLUSIVEADDRUSE*${REMOVE}$</span></span>  

<span data-ttu-id="da3ea-129">*Platzhalter*</span><span class="sxs-lookup"><span data-stu-id="da3ea-129">*Wildcard*</span></span>

<span data-ttu-id="da3ea-130">Fehlgeschlagen (10048)</span><span class="sxs-lookup"><span data-stu-id="da3ea-130">Fail (10048)</span></span>

<span data-ttu-id="da3ea-131">Fehlgeschlagen (10048)</span><span class="sxs-lookup"><span data-stu-id="da3ea-131">Fail (10048)</span></span>

<span data-ttu-id="da3ea-132">Fehlgeschlagen (10048)</span><span class="sxs-lookup"><span data-stu-id="da3ea-132">Fail (10048)</span></span>

<span data-ttu-id="da3ea-133">Fehlgeschlagen (10048)</span><span class="sxs-lookup"><span data-stu-id="da3ea-133">Fail (10048)</span></span>

<span data-ttu-id="da3ea-134">*Zugeschnitten*</span><span class="sxs-lookup"><span data-stu-id="da3ea-134">*Specific*</span></span>

<span data-ttu-id="da3ea-135">Fehlgeschlagen (10048)</span><span class="sxs-lookup"><span data-stu-id="da3ea-135">Fail (10048)</span></span>

<span data-ttu-id="da3ea-136">Fehlgeschlagen (10048)</span><span class="sxs-lookup"><span data-stu-id="da3ea-136">Fail (10048)</span></span>

<span data-ttu-id="da3ea-137">Fehlgeschlagen (10048)</span><span class="sxs-lookup"><span data-stu-id="da3ea-137">Fail (10048)</span></span>

<span data-ttu-id="da3ea-138">Fehlgeschlagen (10048)</span><span class="sxs-lookup"><span data-stu-id="da3ea-138">Fail (10048)</span></span>

<span data-ttu-id="da3ea-139">*Specific2*</span><span class="sxs-lookup"><span data-stu-id="da3ea-139">*Specific2*</span></span>

<span data-ttu-id="da3ea-140">–</span><span class="sxs-lookup"><span data-stu-id="da3ea-140">n/a</span></span>

<span data-ttu-id="da3ea-141">Erfolg</span><span class="sxs-lookup"><span data-stu-id="da3ea-141">Success</span></span>

<span data-ttu-id="da3ea-142">–</span><span class="sxs-lookup"><span data-stu-id="da3ea-142">n/a</span></span>

<span data-ttu-id="da3ea-143">Erfolg</span><span class="sxs-lookup"><span data-stu-id="da3ea-143">Success</span></span>

<span data-ttu-id="da3ea-144">$ {ROWSPAN3} $*keine Optionen*$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="da3ea-144">${ROWSPAN3}$*No options*${REMOVE}$</span></span>  

<span data-ttu-id="da3ea-145">*Platzhalter*</span><span class="sxs-lookup"><span data-stu-id="da3ea-145">*Wildcard*</span></span>

<span data-ttu-id="da3ea-146">Fehlgeschlagen (10048)</span><span class="sxs-lookup"><span data-stu-id="da3ea-146">Fail (10048)</span></span>

<span data-ttu-id="da3ea-147">Fehlgeschlagen (10048)</span><span class="sxs-lookup"><span data-stu-id="da3ea-147">Fail (10048)</span></span>

<span data-ttu-id="da3ea-148">Fehlgeschlagen (10048)</span><span class="sxs-lookup"><span data-stu-id="da3ea-148">Fail (10048)</span></span>

<span data-ttu-id="da3ea-149">Fehlgeschlagen (10048)</span><span class="sxs-lookup"><span data-stu-id="da3ea-149">Fail (10048)</span></span>

<span data-ttu-id="da3ea-150">*Zugeschnitten*</span><span class="sxs-lookup"><span data-stu-id="da3ea-150">*Specific*</span></span>

<span data-ttu-id="da3ea-151">Fehlgeschlagen (10048)</span><span class="sxs-lookup"><span data-stu-id="da3ea-151">Fail (10048)</span></span>

<span data-ttu-id="da3ea-152">Fehlgeschlagen (10048)</span><span class="sxs-lookup"><span data-stu-id="da3ea-152">Fail (10048)</span></span>

<span data-ttu-id="da3ea-153">Fehlgeschlagen (10048)</span><span class="sxs-lookup"><span data-stu-id="da3ea-153">Fail (10048)</span></span>

<span data-ttu-id="da3ea-154">Fehlgeschlagen (10048)</span><span class="sxs-lookup"><span data-stu-id="da3ea-154">Fail (10048)</span></span>

<span data-ttu-id="da3ea-155">*Specific2*</span><span class="sxs-lookup"><span data-stu-id="da3ea-155">*Specific2*</span></span>

<span data-ttu-id="da3ea-156">–</span><span class="sxs-lookup"><span data-stu-id="da3ea-156">n/a</span></span>

<span data-ttu-id="da3ea-157">Erfolg</span><span class="sxs-lookup"><span data-stu-id="da3ea-157">Success</span></span>

<span data-ttu-id="da3ea-158">–</span><span class="sxs-lookup"><span data-stu-id="da3ea-158">n/a</span></span>

<span data-ttu-id="da3ea-159">Erfolg</span><span class="sxs-lookup"><span data-stu-id="da3ea-159">Success</span></span>

<span data-ttu-id="da3ea-160">$ {ROWSPAN3} $*so \_ reuseaddr*$ {Remove} $</span><span class="sxs-lookup"><span data-stu-id="da3ea-160">${ROWSPAN3}$*SO\_REUSEADDR*${REMOVE}$</span></span>  

<span data-ttu-id="da3ea-161">*Platzhalter*</span><span class="sxs-lookup"><span data-stu-id="da3ea-161">*Wildcard*</span></span>

<span data-ttu-id="da3ea-162">Fehlgeschlagen (10013)</span><span class="sxs-lookup"><span data-stu-id="da3ea-162">Fail (10013)</span></span>

<span data-ttu-id="da3ea-163">Fehlgeschlagen (10013)</span><span class="sxs-lookup"><span data-stu-id="da3ea-163">Fail (10013)</span></span>

<span data-ttu-id="da3ea-164">Erfolgreich\*</span><span class="sxs-lookup"><span data-stu-id="da3ea-164">Success\*</span></span>

<span data-ttu-id="da3ea-165">Erfolg</span><span class="sxs-lookup"><span data-stu-id="da3ea-165">Success</span></span>

<span data-ttu-id="da3ea-166">*Zugeschnitten*</span><span class="sxs-lookup"><span data-stu-id="da3ea-166">*Specific*</span></span>

<span data-ttu-id="da3ea-167">Fehlgeschlagen (10013)</span><span class="sxs-lookup"><span data-stu-id="da3ea-167">Fail (10013)</span></span>

<span data-ttu-id="da3ea-168">Fehlgeschlagen (10013)</span><span class="sxs-lookup"><span data-stu-id="da3ea-168">Fail (10013)</span></span>

<span data-ttu-id="da3ea-169">Erfolg</span><span class="sxs-lookup"><span data-stu-id="da3ea-169">Success</span></span>

<span data-ttu-id="da3ea-170">Erfolgreich\*</span><span class="sxs-lookup"><span data-stu-id="da3ea-170">Success\*</span></span>

<span data-ttu-id="da3ea-171">*Specific2*</span><span class="sxs-lookup"><span data-stu-id="da3ea-171">*Specific2*</span></span>

<span data-ttu-id="da3ea-172">–</span><span class="sxs-lookup"><span data-stu-id="da3ea-172">n/a</span></span>

<span data-ttu-id="da3ea-173">Erfolg</span><span class="sxs-lookup"><span data-stu-id="da3ea-173">Success</span></span>

<span data-ttu-id="da3ea-174">–</span><span class="sxs-lookup"><span data-stu-id="da3ea-174">n/a</span></span>

<span data-ttu-id="da3ea-175">Erfolg</span><span class="sxs-lookup"><span data-stu-id="da3ea-175">Success</span></span>

<span data-ttu-id="da3ea-176">\* Das Verhalten ist nicht definiert, in welchem Socket Pakete empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="da3ea-176">\* The behavior is undefined as to which socket will receive packets.</span></span>



 

<span data-ttu-id="da3ea-177">Wenn die erste Bindung keine Optionen oder " \_ reuseaddr" festlegt und die zweite Bindung eine so \_ reuseaddr ausführt, hat der zweite Socket den Port und das Verhalten überholt, wenn der Socket, der die Pakete empfängt, nicht bestimmt wird.</span><span class="sxs-lookup"><span data-stu-id="da3ea-177">In the case where the first bind sets no options or SO\_REUSEADDR, and the second bind performs a SO\_REUSEADDR, the second socket has overtaken the port and behavior regarding which socket will receive packets is undetermined.</span></span> <span data-ttu-id="da3ea-178">Daher \_ wurde exclusiveaddruse eingeführt, um dieser Situation gerecht zu werden.</span><span class="sxs-lookup"><span data-stu-id="da3ea-178">SO\_EXCLUSIVEADDRUSE was introduced to address this situation.</span></span>

<span data-ttu-id="da3ea-179">Ein Socket mit der " \_ exclusiveaddruse"-Menge kann nicht immer sofort nach dem Socket-Abschluss wieder verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="da3ea-179">A socket with SO\_EXCLUSIVEADDRUSE set cannot always be reused immediately after socket closure.</span></span> <span data-ttu-id="da3ea-180">Wenn ein lausch ender Socket mit dem exklusiven Flagsatz z. b. eine Verbindung akzeptiert, nach der der lausch Ende Socket geschlossen wird, kann ein anderer Socket nicht an denselben Port wie der erste Abhör Socket mit dem exklusiven Flag gebunden werden, bis die akzeptierte Verbindung nicht mehr aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="da3ea-180">For example, if a listening socket with the exclusive flag set accepts a connection after which the listening socket is closed, another socket cannot bind to the same port as the first listening socket with the exclusive flag until the accepted connection is no longer active.</span></span>

<span data-ttu-id="da3ea-181">Diese Situation kann recht kompliziert sein. Obwohl der Socket geschlossen wurde, kann der zugrunde liegende Transport seine Verbindung möglicherweise nicht beenden.</span><span class="sxs-lookup"><span data-stu-id="da3ea-181">This situation can be quite complicated; even though the socket has been closed, the underlying transport may not terminate its connection.</span></span> <span data-ttu-id="da3ea-182">Auch nachdem der Socket geschlossen wurde, muss das System alle gepufferten Daten senden, eine ordnungsgemäße Verbindung mit dem Peer übertragen und auf eine ordnungsgemäße Trennung vom Peer warten.</span><span class="sxs-lookup"><span data-stu-id="da3ea-182">Even after the socket is closed, the system must send all of the buffered data, transmit a graceful disconnect to the peer, and wait for a graceful disconnect from the peer.</span></span> <span data-ttu-id="da3ea-183">Daher ist es möglich, dass der zugrunde liegende Transport die Verbindung niemals freigibt, z. b. wenn der Peer ein Fenster der Größe 0 (null) oder andere derartige Angriffe anweist.</span><span class="sxs-lookup"><span data-stu-id="da3ea-183">It is therefore possible that the underlying transport may never release the connection, such as when the peer advertises a zero-size window, or other such attacks.</span></span> <span data-ttu-id="da3ea-184">Im vorherigen Beispiel wurde der Abhör Socket geschlossen, nachdem eine Client Verbindung akzeptiert wurde.</span><span class="sxs-lookup"><span data-stu-id="da3ea-184">In the previous example, the listening socket was closed after a client connection was accepted.</span></span> <span data-ttu-id="da3ea-185">Auch wenn die Client Verbindung geschlossen ist, wird der Port möglicherweise noch nicht wieder verwendet, wenn die Client Verbindung aufgrund nicht bestätigter Daten in einem aktiven Zustand bleibt usw.</span><span class="sxs-lookup"><span data-stu-id="da3ea-185">Now even if the client connection is closed, the port still may not be reused if the client connection remains in an active state because of unacknowledged data, and so forth.</span></span>

<span data-ttu-id="da3ea-186">Um diese Situation zu vermeiden, sollten Anwendungen ein ordnungsgemäßes herunter [](/windows/desktop/api/winsock/nf-winsock-shutdown) fahren sicherstellen: fahren Sie mit dem SD- \_ sendeflag herunter, und warten Sie dann in einer [**empfangener**](/windows/desktop/api/winsock/nf-winsock-recv) -Schleife, bis null Bytes zurückgegeben werden</span><span class="sxs-lookup"><span data-stu-id="da3ea-186">To avoid this situation, applications should ensure a graceful shutdown: call [**shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) with the SD\_SEND flag, then wait in a [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) loop until zero bytes are returned.</span></span> <span data-ttu-id="da3ea-187">Dadurch wird das Problem im Zusammenhang mit der Port Wiederverwendung vermieden, es wird sichergestellt, dass alle Daten vom Peer empfangen wurden, und der Peer wird sichergestellt, dass alle Daten erfolgreich empfangen wurden.</span><span class="sxs-lookup"><span data-stu-id="da3ea-187">Doing so avoids the problem associated with port reuse, guarantees all data was received by the peer, and assures the peer that all its data was successfully received.</span></span>

<span data-ttu-id="da3ea-188">Die Option "so \_ LINGER" kann für einen Socket festgelegt werden, um zu verhindern, dass der Port in einen der aktiven warte Zustände geht. Dies wird jedoch nicht empfohlen, da dies zu unerwünschten Effekten führen kann, da dies dazu führen kann, dass die Verbindung zurückgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="da3ea-188">The SO\_LINGER option may be set on a socket to prevent the port going into one of the active wait states; however, doing so is discouraged because it can lead to undesired effects, because it can cause the connection to be reset.</span></span> <span data-ttu-id="da3ea-189">Wenn z. b. Daten empfangen, aber noch nicht vom Peer bestätigt wurden und der lokale Computer den Socket mit dem sogenannten \_ LINGER-Satz schließt, wird die Verbindung zurückgesetzt, und der Peer verwirft die nicht bestätigten Daten.</span><span class="sxs-lookup"><span data-stu-id="da3ea-189">For example, if data has been received but not yet acknowledged by the peer, and the local computer closes the socket with SO\_LINGER set, the connection is reset and the peer discards the unacknowledged data.</span></span> <span data-ttu-id="da3ea-190">Außerdem ist es schwierig, eine passende Zeit für den Linger auszuwählen. Wenn ein Wert zu klein ist, werden viele abgebrochene Verbindungen erzielt, während ein großes Timeout das System anfällig für Denial-of-Service-Angriffe ist, indem viele Verbindungen hergestellt werden und dadurch zahlreiche Anwendungsthreads blockiert werden.</span><span class="sxs-lookup"><span data-stu-id="da3ea-190">Also, picking a suitable time to linger is difficult; a value too small results in many aborted connections, while a large timeout can leave the system vulnerable to denial of service attacks by establishing many connections, and thereby stalling numerous application threads.</span></span>

> [!Note]  
> <span data-ttu-id="da3ea-191">Ein Socket, der die Option "so \_ exclusiveaddruse" verwendet, muss vor dem Schließen ordnungsgemäß heruntergefahren werden.</span><span class="sxs-lookup"><span data-stu-id="da3ea-191">A socket that is using the SO\_EXCLUSIVEADDRUSE option must be shut down properly prior to closing it.</span></span> <span data-ttu-id="da3ea-192">Andernfalls kann dies zu einem Denial-of-Service-Angriff führen, wenn der zugeordnete Dienst neu gestartet werden muss.</span><span class="sxs-lookup"><span data-stu-id="da3ea-192">Failure to do so can cause a denial of service attack if the associated service needs to restart.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="da3ea-193">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="da3ea-193">Requirements</span></span>



| <span data-ttu-id="da3ea-194">Anforderung</span><span class="sxs-lookup"><span data-stu-id="da3ea-194">Requirement</span></span> | <span data-ttu-id="da3ea-195">Wert</span><span class="sxs-lookup"><span data-stu-id="da3ea-195">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="da3ea-196">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="da3ea-196">Minimum supported client</span></span><br/> | <span data-ttu-id="da3ea-197">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="da3ea-197">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="da3ea-198">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="da3ea-198">Minimum supported server</span></span><br/> | <span data-ttu-id="da3ea-199">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="da3ea-199">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="da3ea-200">Header</span><span class="sxs-lookup"><span data-stu-id="da3ea-200">Header</span></span><br/>                   | <dl> <span data-ttu-id="da3ea-201"><dt>Winsock2. h</dt></span><span class="sxs-lookup"><span data-stu-id="da3ea-201"><dt>Winsock2.h</dt></span></span> </dl> |



 

 




