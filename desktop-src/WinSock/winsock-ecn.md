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
# <a name="winsock-explicit-congestion-notification-ecn"></a>Explizite Winsock-Überlastungsbenachrichtigung (ECN)

## <a name="introduction"></a>Einführung

Einige Anwendungen und/oder Protokolle, die auf dem User Datagram Protocol (UDP) basieren (z. B. QUIC), versuchen, die Verwendung expliziter ECN-Codepunkte (Congestion Notification) zu nutzen, um die Latenz und jittern in überlasteten Netzwerken zu verbessern.

Die Winsock ECN-APIs erweitern die **getsockopt** / **setsockopt-Schnittstelle** sowie die &mdash; [**WSASendMsg**](/windows/win32/api/winsock2/nf-winsock2-wsasendmsg) / [**LPFN_WSARECVMSG-Steuerungsnachrichtenschnittstelle (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) um Unterstützung für das Ändern und Empfangen von &mdash; ECN-Codepunkten in IP-Headern. Mit der bereitgestellten Funktionalität können Sie ECN-Codepunkte pro Paket erhalten und festlegen.

Weitere Informationen zu ECN finden Sie unter [The Addition of Explicit Congestion Notification (ECN) to IP](https://tools.ietf.org/html/rfc3168).

Ihre Anwendung darf beim Senden von Datagrammen nicht den Ce-Codepunkt (Congestion Encountered) angeben. Das Senden wird mit dem Fehler **WSAEINVAL zurückgegeben.**

## <a name="query-ecn-with-wsagetrecvipecn"></a>Abfragen von ECN mit WSAGetRecvIPEcn

[**WSAGetRecvIPEcn ist**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetrecvipecn) eine in definierte Inlinefunktion. `ws2tcpip.h`

Rufen Sie **WSAGetRecvIPEcn** auf, um die aktuelle Aktivierung des Empfangs der **IP_ECN-Steuernachricht** (oder **IPV6_ECN)** über LPFN_WSARECVMSG [**(WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)zu abfragen.

Siehe auch [**die WSAMSG-Struktur.**](/windows/win32/api/ws2def/ns-ws2def-wsamsg)

- **Protokoll:** IPv4
- **Cmsg_level**: IPPROTO_IP
- **Cmsg_type**: IP_ECN (50 Dezimalstellen)
- **Beschreibung:** Gibt den ECN-Codepunkt im IPv4-Headerfeld "Typ des Diensts (TOS)" an bzw. empfängt diesen.

- **Protokoll:** IPv6
- **Cmsg_level**: IPPROTO_IPV6
- **Cmsg_type**: IPV6_ECN (50 Dezimalstellen)
- **Beschreibung:** Gibt ECN-Codepunkt im IPv6-Headerfeld der Datenverkehrsklasse an/empfängt.

## <a name="specify-ecn-with-wsasetrecvipecn"></a>Angeben des ECN mit WSASetRecvIPEcn

[**WSASetRecvIPEcn**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetrecvipecn) ist eine in definierte `ws2tcpip.h` Inlinefunktion.

Rufen Sie **WSASetRecvIPEcn** auf, um anzugeben, ob der IP-Stapel den Steuerungspuffer mit einer Nachricht auffüllen soll, die den ECN-Codepunkt des IPv4-Headerfelds vom Typ des Diensts (oder des IPv6-Headerfelds der Datenverkehrsklasse) für ein empfangenes Datagramm enthält. Bei Festlegung auf `TRUE` gibt die [**LPFN_WSARECVMSG -Funktion (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) optionale Steuerdaten zurück, die den ECN-Codepunkt des empfangenen Datagramms enthalten. Der zurückgegebene Steuernachrichtentyp wird **IP_ECN** (oder **IPV6_ECN**) mit **IPPROTO_IP** ebene (oder **IPPROTO_IPV6**). Die Steuernachrichtendaten werden als **INT** zurückgegeben. Diese Option ist nur für Datagrammsockets gültig (der Sockettyp muss **SOCK_DGRAM** sein).

## <a name="code-example-1mdashapplication-advertising-ecn-support"></a>Codebeispiel 1: Anwendung zur Ankündigung der &mdash; ECN-Unterstützung

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

## <a name="code-example-2mdashapplication-detecting-congestion"></a>Codebeispiel &mdash; 2: Anwendung, die Überlastung erkennt

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

## <a name="see-also"></a>Siehe auch

* [WSAGetRecvIPEcn](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetrecvipecn)
* [WSASetRecvIPEcn](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetrecvipecn)
