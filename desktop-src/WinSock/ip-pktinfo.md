---
description: Ermöglicht einer Anwendung das Aktivieren oder Deaktivieren der Rückgabe von Paketinformationen durch die WSARecvMsg-Funktion auf einem IPv4-Socket.
ms.assetid: C6246899-0220-4F88-B43B-CED1B1FF7DC3
title: IP_PKTINFO Socketoption (Ws2ipdef.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56ba653b4ece11086706493b920e1ed650b66eecdd6e788a5edfe259cf9eb9f0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097790"
---
# <a name="ip_pktinfo-socket-option"></a>\_IP-PKTINFO-Socketoption

Mit der \_ IP-PKTINFO-Socketoption kann eine Anwendung die Rückgabe von Paketinformationen durch die [**LPFN_WSARECVMSG -Funktion (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) auf einem IPv4-Socket aktivieren oder deaktivieren.

Um den Status dieser Socketoption abzufragen, rufen Sie die [**getsockopt-Funktion auf.**](/windows/desktop/api/winsock/nf-winsock-getsockopt) Um diese Option festzulegen, rufen Sie die [**setsockopt-Funktion**](/windows/desktop/api/winsock/nf-winsock-setsockopt) mit den folgenden Parametern auf.

## <a name="socket-option-value"></a>Wert der Socketoption

Die Konstante, die diese Socketoption darstellt, ist 19.

## <a name="syntax"></a>Syntax


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



## <a name="parameters"></a>Parameter

<dl> <dt>

*s* \[ in\]
</dt> <dd>

Ein Deskriptor, der den Socket identifiziert.

</dd> <dt>

*-Ebene* \[ In\]
</dt> <dd>

Die Ebene, auf der die Option definiert ist. Verwenden Sie **IPPROTO \_ IP** für diesen Vorgang.

</dd> <dt>

*optname* \[ In\]
</dt> <dd>

Die Socketoption, für die der Wert abzurufen oder festzulegen ist. Verwenden Sie \_ IP PKTINFO für diesen Vorgang.

</dd> <dt>

*optval* \[ out\]
</dt> <dd>

Ein Zeiger auf den Puffer, der den Wert für die festzulegende Option enthält. Dieser Parameter sollte auf einen Puffer zeigen, der gleich oder größer als die Größe eines **DWORD-Werts** ist.

Dieser Wert wird als boolescher Wert behandelt, wobei 0 zur Angabe von **FALSE** (deaktiviert) und ein Wert ungleich 0 (null) verwendet wird, um **TRUE** (aktiviert) anzugeben.

</dd> <dt>

*optlen* \[ in, out\]
</dt> <dd>

Ein Zeiger auf die Größe des *optval-Puffers* in Bytes. Diese Größe muss gleich oder größer als die Größe eines **DWORD-Werts** sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn der Vorgang erfolgreich abgeschlossen wurde, gibt die [**getsockopt-**](/windows/desktop/api/winsock/nf-winsock-getsockopt) oder [**setsockopt-Funktion**](/windows/desktop/api/winsock/nf-winsock-setsockopt) 0 (null) zurück.

Wenn der Vorgang fehlschlägt, wird der Wert SOCKET \_ ERROR zurückgegeben, und ein bestimmter Fehlercode kann durch Aufrufen von [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)abgerufen werden.



| Fehlercode                                                                                                                                              | Bedeutung                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**[WSANOTINITIALISED](windows-sockets-error-codes-2.md)**</dt> </dl> | Vor der Verwendung dieser Funktion muss ein erfolgreicher [**WSAStartup-Aufruf**](/windows/desktop/api/winsock/nf-winsock-wsastartup) erfolgen.<br/>                                                                                                                                                     |
| <dl> <dt>**[WSAENETDOWN](windows-sockets-error-codes-2.md)**</dt> </dl>             | Fehler beim Netzwerksubsystem.<br/>                                                                                                                                                                                                               |
| <dl> <dt>**[WSAEFAULT](windows-sockets-error-codes-2.md)**</dt> </dl>                 | Einer der *optval-* oder *optlen-Parameter* verweist auf den Arbeitsspeicher, der sich nicht in einem gültigen Teil des Benutzeradressraums befindet. Dieser Fehler wird auch zurückgegeben, wenn der Wert, auf den der *optlen-Parameter* zeigt, kleiner als die Größe eines **DWORD-Werts** ist.<br/> |
| <dl> <dt>**[WSAEINPROGRESS](windows-sockets-error-codes-2.md)**</dt> </dl>       | Ein blockierende Windows Sockets 1.1-Aufruf wird ausgeführt, oder der Dienstanbieter verarbeitet weiterhin eine Rückruffunktion.<br/>                                                                                                                            |
| <dl> <dt>**[WSAEINVAL](windows-sockets-error-codes-2.md)**</dt> </dl>                 | Ein ungültiges Argument wurde angegeben. Dieser Fehler wird zurückgegeben, wenn der *Levelparameter* unbekannt oder ungültig ist. Bei Windows Vista und höher wird dieser Fehler auch zurückgegeben, wenn sich der Socket in einem Übergangszustand befand.<br/>                                     |
| <dl> <dt>**[WSAENOPROTOOPT](windows-sockets-error-codes-2.md)**</dt> </dl>       | Die Option ist unbekannt oder wird von der angegebenen Protokollfamilie nicht unterstützt. Dieser Fehler wird zurückgegeben, wenn der *Typparameter* für den im *s-Parameter* übergebenen Socketdeskriptor nicht **SOCK \_ DGRAM** oder **SOCK \_ RAW** war. <br/>                          |
| <dl> <dt>**[WSAENOTSOCK](windows-sockets-error-codes-2.md)**</dt> </dl>             | Der Deskriptor ist kein Socket.<br/>                                                                                                                                                                                                                 |



 

## <a name="remarks"></a>Hinweise

Die [**getsockopt-Funktion,**](/windows/desktop/api/winsock/nf-winsock-getsockopt) die mit der IP-PKTINFO-Socketoption aufgerufen \_ wird, ermöglicht es einer Anwendung zu bestimmen, ob Paketinformationen von der [**WSARecvMsg-Funktion (LPFN_WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)für einen IPv4-Socket zurückgegeben werden sollen.

Die mit der IP-PKTINFO-Socketoption aufgerufene [**setsockopt-Funktion**](/windows/desktop/api/winsock/nf-winsock-setsockopt) \_ ermöglicht einer Anwendung, die Rückgabe von Paketinformationen durch die [**LPFN_WSARECVMSG -Funktion (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) zu aktivieren oder zu deaktivieren. Die \_ IP-PKTINFO-Option für einen Socket ist standardmäßig deaktiviert (auf **FALSE** festgelegt).

Wenn diese Socketoption für einen IPv4-Socket vom Typ **SOCK \_ DGRAM** oder **SOCK \_ RAW** aktiviert ist, gibt die [**funktion LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) Paketinformationen in der [**WSAMSG-Struktur**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) zurück, auf die der *lpMsg-Parameter* zeigt. Eines der Steuerelementdatenobjekte in der zurückgegebenen **WSAMSG-Struktur** enthält eine [**in \_ pktinfo-Struktur,**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in_pktinfo) die zum Speichern empfangener Paketadresseninformationen verwendet wird.

Für Datagramme, die von der [**LPFN_WSARECVMSG-Funktion (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) über IPv4 empfangen werden, enthält der **Control-Member** der empfangenen [**WSAMSG-Struktur**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) eine [**WSABUF-Struktur,**](/windows/desktop/api/ws2def/ns-ws2def-wsabuf) die eine **WSACMSGHDR-Struktur** enthält. Der **\_ cmsg-Ebenenmember** dieser **WSACMSGHDR-Struktur** würde **IPPROTO \_ IP** enthalten, der **cmsg-Typmember \_** dieser Struktur würde **IP \_ PKTINFO** enthalten, und der **cmsg-Datenmember \_** würde eine [**in der \_ pktinfo-Struktur**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in_pktinfo) enthalten, die zum Speichern empfangener IPv4-Paketadresseninformationen verwendet wird. Die IPv4-Adresse in der **\_ pktinfo-Struktur** ist die IPv4-Adresse, von der das Paket empfangen wurde.

Wenn eine Anwendung für einen Dual-Stack-Datagrammsocket die [**LPFN_WSARECVMSG -Funktion (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) benötigt, um Paketinformationen in einer [**WSAMSG-Struktur**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) für über IPv4 empfangene Datagramme zurückzugeben, \_ muss die IP-PKTINFO-Socketoption für den Socket auf TRUE festgelegt werden. Wenn nur die [ \_ IPV6 PKTINFO-Option](ipv6-pktinfo.md) für den Socket auf TRUE festgelegt ist, werden Paketinformationen für Datagramme bereitgestellt, die über IPv6 empfangen werden, aber möglicherweise nicht für Datagramme, die über IPv4 empfangen werden.

Wenn eine Anwendung versucht, die \_ IP-PKTINFO-Socketoption für einen Dual-Stack-Datagrammsocket festzulegen, und IPv4 auf dem System deaktiviert ist, schlägt die [**Setsockopt-Funktion**](/windows/desktop/api/winsock/nf-winsock-setsockopt) fehl, und [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) gibt den Fehler [WSAEINVAL](windows-sockets-error-codes-2.md)zurück. Dieser Fehler wird auch von der **setsockopt-Funktion** als Ergebnis anderer Fehler zurückgegeben. Wenn eine Anwendung versucht, eine \_ IPPROTO-Socketoption auf IP-Ebene für einen Socket mit zwei Stapeln festzulegen, und ein Fehler mit [WSAEINVAL](windows-sockets-error-codes-2.md)auftritt, sollte die Anwendung bestimmen, ob IPv4 auf dem lokalen Computer deaktiviert ist. Eine Methode, mit der ermittelt werden kann, ob IPv4 aktiviert oder deaktiviert ist, ist das Aufrufen der [**Socketfunktion**](/windows/desktop/api/Winsock2/nf-winsock2-socket) mit *dem* af-Parameter, der auf AF INET festgelegt \_ ist, um zu versuchen, einen IPv4-Socket zu erstellen. Wenn die **Socketfunktion** fehlschlägt und **WSAGetLastError** den Fehler [WSAEAFNOSUPPORT](windows-sockets-error-codes-2.md)zurückgibt, bedeutet dies, dass IPv4 nicht aktiviert ist. In diesem Fall kann ein **Setsockopt-Funktionsfehler** beim Festlegen der IP-PKTINFO-Socketoption \_ von der Anwendung ignoriert werden. Andernfalls sollte ein Fehler beim Festlegen der \_ IP-PKTINFO-Socketoption als unerwarteter Fehler behandelt werden.

Beachten Sie, dass die *Headerdatei Ws2ipdef.h* automatisch in *"Ws2tcpip.h"* enthalten ist und niemals direkt verwendet werden sollte.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                       |
| Header<br/>                   | <dl> <dt>Ws2ipdef.h (einschließlich Ws2tcpip.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Dual-Stack-Sockets](dual-stack-sockets.md)
</dt> <dt>

[**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[**in \_ pktinfo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in_pktinfo)
</dt> <dt>

[**\_IPPROTO-IP-Socketoptionen**](ipproto-ip-socket-options.md)
</dt> <dt>

[IPV6 \_ PKTINFO](ipv6-pktinfo.md)
</dt> <dt>

[**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> <dt>

[**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket)
</dt> <dt>

[**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg)
</dt> <dt>

[**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)
</dt> </dl>

 

 
