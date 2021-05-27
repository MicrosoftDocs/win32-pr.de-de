---
title: Explizite Winsock-Überlastungsbenachrichtigung (ECN)
description: Einige Anwendungen und/oder Protokolle, die auf dem User Datagram Protocol (UDP) basieren (z. B. QUIC), versuchen, die Verwendung expliziter ECN-Codepunkte (Congestion Notification) zu nutzen, um die Latenz und jittern in überlasteten Netzwerken zu verbessern.
ms.topic: article
ms.date: 11/13/2020
ms.openlocfilehash: 090ac9b0575cb491aa6d726e7507223156460ace
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/27/2021
ms.locfileid: "110559971"
---
# <a name="winsock-explicit-congestion-notification-ecn"></a><span data-ttu-id="ccb10-103">Explizite Winsock-Überlastungsbenachrichtigung (ECN)</span><span class="sxs-lookup"><span data-stu-id="ccb10-103">Winsock explicit congestion notification (ECN)</span></span>

## <a name="introduction"></a><span data-ttu-id="ccb10-104">Einführung</span><span class="sxs-lookup"><span data-stu-id="ccb10-104">Introduction</span></span>

<span data-ttu-id="ccb10-105">Einige Anwendungen und/oder Protokolle, die auf dem User Datagram Protocol (UDP) basieren (z. B. QUIC), versuchen, die Verwendung expliziter ECN-Codepunkte (Congestion Notification) zu nutzen, um die Latenz und jittern in überlasteten Netzwerken zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="ccb10-105">Some applications and/or protocols that are based on the User Datagram Protocol (UDP) (for example, QUIC) seek to leverage the use of explicit congestion notification (ECN) codepoints in order to improve latency and jitter in congested networks.</span></span>

<span data-ttu-id="ccb10-106">Die Winsock ECN-APIs erweitern die **getsockopt** / **setsockopt-Schnittstelle** sowie die &mdash; [**WSASendMsg**](/windows/win32/api/winsock2/nf-winsock2-wsasendmsg) / [**LPFN_WSARECVMSG-Steuerungsnachrichtenschnittstelle (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) um Unterstützung für das Ändern und Empfangen von &mdash; ECN-Codepunkten in IP-Headern.</span><span class="sxs-lookup"><span data-stu-id="ccb10-106">The Winsock ECN APIs extend the **getsockopt**/**setsockopt** interface&mdash;as well as the [**WSASendMsg**](/windows/win32/api/winsock2/nf-winsock2-wsasendmsg)/[**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) control message interface&mdash;with support for modifying and receiving ECN codepoints in IP headers.</span></span> <span data-ttu-id="ccb10-107">Mit der bereitgestellten Funktionalität können Sie ECN-Codepunkte pro Paket erhalten und festlegen.</span><span class="sxs-lookup"><span data-stu-id="ccb10-107">The functionality provided allows you to get and set ECN codepoints on a per-packet basis.</span></span>

<span data-ttu-id="ccb10-108">Weitere Informationen zu ECN finden Sie unter [The Addition of Explicit Congestion Notification (ECN) to IP](https://tools.ietf.org/html/rfc3168).</span><span class="sxs-lookup"><span data-stu-id="ccb10-108">For more information regarding ECN, see [The Addition of Explicit Congestion Notification (ECN) to IP](https://tools.ietf.org/html/rfc3168).</span></span>

<span data-ttu-id="ccb10-109">Ihre Anwendung darf beim Senden von Datagrammen nicht den Ce-Codepunkt (Congestion Encountered) angeben.</span><span class="sxs-lookup"><span data-stu-id="ccb10-109">Your application isn't allowed to specify the Congestion Encountered (CE) code point when sending datagrams.</span></span> <span data-ttu-id="ccb10-110">Das Senden wird mit dem Fehler **WSAEINVAL zurückgegeben.**</span><span class="sxs-lookup"><span data-stu-id="ccb10-110">The send will return with error **WSAEINVAL**.</span></span>

## <a name="query-ecn-with-wsagetrecvipecn"></a><span data-ttu-id="ccb10-111">Abfragen von ECN mit WSAGetRecvIPEcn</span><span class="sxs-lookup"><span data-stu-id="ccb10-111">Query ECN with WSAGetRecvIPEcn</span></span>

<span data-ttu-id="ccb10-112">[**WSAGetRecvIPEcn ist**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetrecvipecn) eine in definierte Inlinefunktion. `ws2tcpip.h`</span><span class="sxs-lookup"><span data-stu-id="ccb10-112">[**WSAGetRecvIPEcn**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetrecvipecn) is an inline function, defined in `ws2tcpip.h`.</span></span>

<span data-ttu-id="ccb10-113">Rufen Sie **WSAGetRecvIPEcn** auf, um die aktuelle Aktivierung des Empfangs der **IP_ECN-Steuernachricht** (oder **IPV6_ECN)** über LPFN_WSARECVMSG [**(WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)zu abfragen.</span><span class="sxs-lookup"><span data-stu-id="ccb10-113">Call **WSAGetRecvIPEcn** to query the current enablement of receiving the **IP_ECN** (or **IPV6_ECN**) control message via [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg).</span></span>

<span data-ttu-id="ccb10-114">Siehe auch [**die WSAMSG-Struktur.**](/windows/win32/api/ws2def/ns-ws2def-wsamsg)</span><span class="sxs-lookup"><span data-stu-id="ccb10-114">Also see the [**WSAMSG**](/windows/win32/api/ws2def/ns-ws2def-wsamsg) structure.</span></span>

- <span data-ttu-id="ccb10-115">**Protokoll:** IPv4</span><span class="sxs-lookup"><span data-stu-id="ccb10-115">**Protocol**: IPv4</span></span>
- <span data-ttu-id="ccb10-116">**Cmsg_level**: IPPROTO_IP</span><span class="sxs-lookup"><span data-stu-id="ccb10-116">**Cmsg_level**: IPPROTO_IP</span></span>
- <span data-ttu-id="ccb10-117">**Cmsg_type**: IP_ECN (50 Dezimalstellen)</span><span class="sxs-lookup"><span data-stu-id="ccb10-117">**Cmsg_type**: IP_ECN (50 decimal)</span></span>
- <span data-ttu-id="ccb10-118">**Beschreibung:** Gibt den ECN-Codepunkt im IPv4-Headerfeld "Typ des Diensts (TOS)" an bzw. empfängt diesen.</span><span class="sxs-lookup"><span data-stu-id="ccb10-118">**Description**: Specifies/receives ECN codepoint in the Type of Service (TOS) IPv4 header field.</span></span>

- <span data-ttu-id="ccb10-119">**Protokoll:** IPv6</span><span class="sxs-lookup"><span data-stu-id="ccb10-119">**Protocol**: IPv6</span></span>
- <span data-ttu-id="ccb10-120">**Cmsg_level**: IPPROTO_IPV6</span><span class="sxs-lookup"><span data-stu-id="ccb10-120">**Cmsg_level**: IPPROTO_IPV6</span></span>
- <span data-ttu-id="ccb10-121">**Cmsg_type**: IPV6_ECN (50 Dezimalstellen)</span><span class="sxs-lookup"><span data-stu-id="ccb10-121">**Cmsg_type**: IPV6_ECN (50 decimal)</span></span>
- <span data-ttu-id="ccb10-122">**Beschreibung:** Gibt ECN-Codepunkt im IPv6-Headerfeld der Datenverkehrsklasse an/empfängt.</span><span class="sxs-lookup"><span data-stu-id="ccb10-122">**Description**: Specifies/receives ECN codepoint in the Traffic Class IPv6 header field.</span></span>

## <a name="specify-ecn-with-wsasetrecvipecn"></a><span data-ttu-id="ccb10-123">Angeben des ECN mit WSASetRecvIPEcn</span><span class="sxs-lookup"><span data-stu-id="ccb10-123">Specify ECN with WSASetRecvIPEcn</span></span>

<span data-ttu-id="ccb10-124">[**WSASetRecvIPEcn**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetrecvipecn) ist eine in definierte `ws2tcpip.h` Inlinefunktion.</span><span class="sxs-lookup"><span data-stu-id="ccb10-124">[**WSASetRecvIPEcn**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetrecvipecn) is an inline function, defined in `ws2tcpip.h`.</span></span>

<span data-ttu-id="ccb10-125">Rufen Sie **WSASetRecvIPEcn** auf, um anzugeben, ob der IP-Stapel den Steuerungspuffer mit einer Nachricht auffüllen soll, die den ECN-Codepunkt des IPv4-Headerfelds vom Typ des Diensts (oder des IPv6-Headerfelds der Datenverkehrsklasse) für ein empfangenes Datagramm enthält.</span><span class="sxs-lookup"><span data-stu-id="ccb10-125">Call **WSASetRecvIPEcn** to specify whether the IP stack should populate the control buffer with a message containing the ECN codepoint of the Type of Service IPv4 header field (or Traffic Class IPv6 header field) on a received datagram.</span></span> <span data-ttu-id="ccb10-126">Bei Festlegung auf `TRUE` gibt die [**LPFN_WSARECVMSG -Funktion (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) optionale Steuerdaten zurück, die den ECN-Codepunkt des empfangenen Datagramms enthalten.</span><span class="sxs-lookup"><span data-stu-id="ccb10-126">When set to `TRUE`, the [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) function returns optional control data containing the ECN codepoint of the received datagram.</span></span> <span data-ttu-id="ccb10-127">Der zurückgegebene Steuernachrichtentyp wird **IP_ECN** (oder **IPV6_ECN**) mit **IPPROTO_IP** ebene (oder **IPPROTO_IPV6**).</span><span class="sxs-lookup"><span data-stu-id="ccb10-127">The returned control message type will be **IP_ECN** (or **IPV6_ECN**) with level **IPPROTO_IP** (or **IPPROTO_IPV6**).</span></span> <span data-ttu-id="ccb10-128">Die Steuernachrichtendaten werden als **INT** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ccb10-128">The control message data is returned as an **INT**.</span></span> <span data-ttu-id="ccb10-129">Diese Option ist nur für Datagrammsockets gültig (der Sockettyp muss **SOCK_DGRAM** sein).</span><span class="sxs-lookup"><span data-stu-id="ccb10-129">This option is valid only on datagram sockets (the socket type must be **SOCK_DGRAM**).</span></span>

## <a name="code-example-1mdashapplication-advertising-ecn-support"></a><span data-ttu-id="ccb10-130">Codebeispiel 1: Anwendung zur Ankündigung der &mdash; ECN-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="ccb10-130">Code example 1&mdash;application advertising ECN support</span></span>

```cpp
#define ECN_ECT_0 2

void sendEcn(SOCKET sock, PSOCKADDR_STORAGE addr, LPFN_WSASENDMSG sendmsg, PCHAR data, INT datalen)
{
    DWORD numBytes;
    INT error;

    CHAR control[WSA_CMSG_SPACE(sizeof(INT))] = { 0 };
    WSABUF dataBuf;
    WSABUF controlBuf;
    WSAMSG wsaMsg;
    PCMSGHDR cmsg;

    dataBuf.buf = data;
    dataBuf.len = datalen;
    controlBuf.buf = control;
    controlBuf.len = sizeof(control);
    wsaMsg.name = (PSOCKADDR)addr;
    wsaMsg.namelen = (INT)INET_SOCKADDR_LENGTH(addr->ss_family);
    wsaMsg.lpBuffers = &dataBuf;
    wsaMsg.dwBufferCount = 1;
    wsaMsg.Control = controlBuf;
    wsaMsg.dwFlags = 0;

    cmsg = WSA_CMSG_FIRSTHDR(&wsaMsg);
    cmsg->cmsg_len = WSA_CMSG_LEN(sizeof(INT));
    cmsg->cmsg_level = (addr->ss_family == AF_INET) ? IPPROTO_IP : IPPROTO_IPV6;
    cmsg->cmsg_type = (addr->ss_family == AF_INET) ? IP_ECN : IPV6_ECN;
    *(PINT)WSA_CMSG_DATA(cmsg) = ECN_ECT_0;

    error =
        sendmsg(
            sock,
            &wsaMsg,
            0,
            &numBytes,
            NULL,
            NULL);
    if (error == SOCKET_ERROR) {
        printf("sendmsg failed %d\n", WSAGetLastError());
    }
}
```

## <a name="code-example-2mdashapplication-detecting-congestion"></a><span data-ttu-id="ccb10-131">Codebeispiel &mdash; 2: Anwendung, die Überlastung erkennt</span><span class="sxs-lookup"><span data-stu-id="ccb10-131">Code example 2&mdash;application detecting congestion</span></span>

```cpp
#define ECN_ECT_CE 3

int recvEcn(SOCKET sock, PSOCKADDR_STORAGE addr, LPFN_WSARECVMSG recvmsg, PCHAR data, INT datalen, PBOOLEAN congestionEncountered)
{
    DWORD numBytes;
    INT error;
    INT ecnVal;
    SOCKADDR_STORAGE remoteAddr = { 0 };

    CHAR control[WSA_CMSG_SPACE(sizeof(INT))] = { 0 };
    WSABUF dataBuf;
    WSABUF controlBuf;
    WSAMSG wsaMsg;
    PCMSGHDR cmsg;

    dataBuf.buf = data;
    dataBuf.len = datalen;
    controlBuf.buf = control;
    controlBuf.len = sizeof(control);
    wsaMsg.name = (PSOCKADDR)&remoteAddr;
    wsaMsg.namelen = sizeof(remoteAddr);
    wsaMsg.lpBuffers = &dataBuf;
    wsaMsg.dwBufferCount = 1;
    wsaMsg.Control = controlBuf;
    wsaMsg.dwFlags = 0;

    *congestionEncountered = FALSE;

    error =
        recvmsg(
            sock,
            &wsaMsg,
            &numBytes,
            NULL,
            NULL);
    if (error == SOCKET_ERROR) {
        printf("recvmsg failed %d\n", WSAGetLastError());
        return -1;
    }

    cmsg = WSA_CMSG_FIRSTHDR(&wsaMsg);
    while (cmsg != NULL) {
        if ((cmsg->cmsg_level == IPPROTO_IP && cmsg->cmsg_type == IP_ECN) ||
            (cmsg->cmsg_level == IPPROTO_IPV6 && cmsg->cmsg_type == IPV6_ECN)) {
            ecnVal = *(PINT)WSA_CMSG_DATA(cmsg);
            if (ecnVal == ECN_ECT_CE) {
                *congestionEncountered = TRUE;
            }
            break;
        }
        cmsg = WSA_CMSG_NXTHDR(&wsaMsg, cmsg);
    }

    return numBytes;
}

void receiver(SOCKET sock, PSOCKADDR_STORAGE addr, LPFN_WSARECVMSG recvmsg)
{
    DWORD numBytes;
    INT error;
    DWORD enabled;
    CHAR data[512];
    BOOLEAN congestionEncountered;

    error = bind(sock, (PSOCKADDR)addr, sizeof(*addr));
    if (error == SOCKET_ERROR) {
        printf("bind failed %d\n", WSAGetLastError());
        return;
    }

    enabled = TRUE;
    error = WSASetRecvIPEcn(sock, enabled);
    if (error == SOCKET_ERROR) {
        printf(" WSASetRecvIPEcn failed %d\n", WSAGetLastError());
        return;
    }

    do {
        numBytes = recvEcn(sock, addr, recvmsg, data, sizeof(data), &congestionEncountered);
        if (congestionEncountered) {
            // Tell sender to slow down
        }
    } while (numBytes > 0);
}
```

## <a name="see-also"></a><span data-ttu-id="ccb10-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ccb10-132">See also</span></span>

* [<span data-ttu-id="ccb10-133">WSAGetRecvIPEcn</span><span class="sxs-lookup"><span data-stu-id="ccb10-133">WSAGetRecvIPEcn</span></span>](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetrecvipecn)
* [<span data-ttu-id="ccb10-134">WSASetRecvIPEcn</span><span class="sxs-lookup"><span data-stu-id="ccb10-134">WSASetRecvIPEcn</span></span>](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetrecvipecn)
