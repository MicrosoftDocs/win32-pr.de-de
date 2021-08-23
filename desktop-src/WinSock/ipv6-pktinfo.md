---
description: Ermöglicht es einer Anwendung, die Rückgabe von Paketinformationen durch die WSARecvMsg-Funktion auf einem IPv6-Socket zu aktivieren oder zu deaktivieren.
ms.assetid: 7BF17538-BE92-44FE-BA3C-6B44F61D478A
title: IPV6_PKTINFO Socketoption (Ws2ipdef.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1bee015e7a73b803d78ae914e71a863dec83e4f40fc1aea9f631a54b37c586a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119733770"
---
# <a name="ipv6_pktinfo-socket-option"></a>IPV6 \_ PKTINFO-Socketoption

Mit der IpV6-PKTINFO-Socketoption kann eine Anwendung die Rückgabe von Paketinformationen durch die \_ [**LPFN_WSARECVMSG-Funktion (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) auf einem IPv6-Socket aktivieren oder deaktivieren.

Rufen Sie zum Abfragen des Status dieser Socketoption die [**getsockopt-Funktion**](/windows/desktop/api/winsock/nf-winsock-getsockopt) auf. Rufen Sie zum Festlegen dieser Option die [**setsockopt-Funktion**](/windows/desktop/api/winsock/nf-winsock-setsockopt) mit den folgenden Parametern auf.

## <a name="socket-option-value"></a>Wert der Socketoption

Die Konstante, die diese Socketoption darstellt, ist 19.

## <a name="syntax"></a>Syntax


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



## <a name="parameters"></a>Parameter

<dl> <dt>

*s* \[ in\]
</dt> <dd>

Ein Deskriptor, der den Socket identifiziert.

</dd> <dt>

*level* \[ In\]
</dt> <dd>

Die Ebene, auf der die Option definiert ist. Verwenden **Sie IPPROTO \_ IPV6** für diesen Vorgang.

</dd> <dt>

*optname* \[ In\]
</dt> <dd>

Die Socketoption, für die der Wert erhalten oder festgelegt werden soll. Verwenden Sie IPV6 \_ PKTINFO für diesen Vorgang.

</dd> <dt>

*optval* \[ out\]
</dt> <dd>

Ein Zeiger auf den Puffer, der den Wert für die zu festlegende Option enthält. Dieser Parameter sollte auf einen Puffer zeigen, der gleich oder größer als die Größe eines **DWORD-Werts** ist.

Dieser Wert wird als boolescher Wert behandelt, bei dem 0 verwendet wird, um **FALSE** (deaktiviert) anzugeben, und ein Wert ungleich 0 (null), um **TRUE** (aktiviert) anzugeben.

</dd> <dt>

*optlen* \[ in, out\]
</dt> <dd>

Ein Zeiger auf die Größe des *Optvalpuffers* in Bytes. Diese Größe muss gleich oder größer als die Größe eines **DWORD-Werts** sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn der Vorgang erfolgreich abgeschlossen wird, gibt die [**getsockopt-**](/windows/desktop/api/winsock/nf-winsock-getsockopt) oder [**setsockopt-Funktion**](/windows/desktop/api/winsock/nf-winsock-setsockopt) 0 (null) zurück.

Wenn der Vorgang fehlschlägt, wird der Wert SOCKET ERROR zurückgegeben, und ein bestimmter Fehlercode kann durch Aufrufen von \_ [**WSAGetLastError abgerufen werden.**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)



| Fehlercode                                                                                                                                              | Bedeutung                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**[WSANOTINITIALISED](windows-sockets-error-codes-2.md)**</dt> </dl> | Vor der Verwendung dieser Funktion muss ein erfolgreicher [**WSAStartup-Aufruf**](/windows/desktop/api/winsock/nf-winsock-wsastartup) erfolgen.<br/>                                                                                                                                                     |
| <dl> <dt>**[WSAENETDOWN](windows-sockets-error-codes-2.md)**</dt> </dl>             | Fehler beim Netzwerksubsystem.<br/>                                                                                                                                                                                                               |
| <dl> <dt>**[WSAEFAULT](windows-sockets-error-codes-2.md)**</dt> </dl>                 | Einer der *Optval- oder* *optlen-Parameter* zeigen auf den Arbeitsspeicher, der sich nicht in einem gültigen Teil des Benutzeradressenbereichs befindet. Dieser Fehler wird auch zurückgegeben, wenn der Wert, auf den der *optlen-Parameter* verweist, kleiner als die Größe eines **DWORD-Werts** ist.<br/> |
| <dl> <dt>**[WSAEINPROGRESS](windows-sockets-error-codes-2.md)**</dt> </dl>       | Ein blockieren Windows Sockets 1.1-Aufruf wird in Bearbeitung, oder der Dienstanbieter verarbeitet weiterhin eine Rückruffunktion.<br/>                                                                                                                            |
| <dl> <dt>**[WSAEINVAL](windows-sockets-error-codes-2.md)**</dt> </dl>                 | Ein ungültiges Argument wurde angegeben. Dieser Fehler wird zurückgegeben, wenn *der Levelparameter* unbekannt oder ungültig ist. Unter Windows Vista und höher wird dieser Fehler auch zurückgegeben, wenn sich der Socket in einem Übergangszustand befindet.<br/>                                     |
| <dl> <dt>**[WSAENOPROTOOPT](windows-sockets-error-codes-2.md)**</dt> </dl>       | Die Option ist unbekannt oder wird von der angegebenen Protokollfamilie nicht unterstützt. Dieser Fehler wird zurückgegeben, wenn der *Typparameter* für den socket-Deskriptor, der im *s-Parameter* übergeben wurde, nicht **SOCK \_ DGRAM** oder **SOCK \_ RAW war.** <br/>                          |
| <dl> <dt>**[WSAENOTSOCK](windows-sockets-error-codes-2.md)**</dt> </dl>             | Der Deskriptor ist kein Socket.<br/>                                                                                                                                                                                                                 |



 

## <a name="remarks"></a>Hinweise

Die [**getsockopt-Funktion,**](/windows/desktop/api/winsock/nf-winsock-getsockopt) die mit der IPV6 PKTINFO-Socketoption aufgerufen wird, ermöglicht einer Anwendung zu bestimmen, ob Paketinformationen von der \_ LPFN_WSARECVMSG-Funktion [**(WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)für einen IPv6-Socket zurückgegeben werden sollen.

Die [**setsockopt-Funktion,**](/windows/desktop/api/winsock/nf-winsock-setsockopt) die mit der IPV6 PKTINFO-Socketoption aufgerufen wird, ermöglicht es einer Anwendung, die Rückgabe von Paketinformationen durch die \_ LPFN_WSARECVMSG-Funktion [**(WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) zu aktivieren oder zu deaktivieren. Die IPV6-PKTINFO-Option für einen Socket ist standardmäßig deaktiviert \_ (auf **FALSE** festgelegt).

Wenn diese Socketoption auf einem IPv6-Socket vom Typ **SOCK \_ DGRAM** oder **SOCK \_ RAW** aktiviert ist, gibt die [**LPFN_WSARECVMSG-Funktion (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) Paketinformationen in der [**WSAMSG-Struktur**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) zurück, auf die der *lpMsg-Parameter* zeigt. Eines der Steuerelementdatenobjekte in der zurückgegebenen **WSAMSG-Struktur** enthält eine [**\_ pktinfo-Struktur in6,**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in6_pktinfo) die zum Speichern empfangener Paketadresseninformationen verwendet wird.

Für Datagramme, die von der [**LPFN_WSARECVMSG-Funktion (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) über IPv6 empfangen werden, enthält das **Control-Member** der [**empfangenen WSAMSG-Struktur**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) eine [**WSABUF-Struktur,**](/windows/desktop/api/ws2def/ns-ws2def-wsabuf) die eine **WSACMSGHDR-Struktur** enthält. Der **\_ cmsg-Level-Member** dieser **WSACMSGHDR-Struktur** würde **IPPROTO \_ IPV6** enthalten, das **\_ cmsg-Typmitglied** dieser Struktur **würde IPV6 \_ PKTINFO** enthalten, und der **\_ cmsg-Daten** member würde eine [**in6 \_ pktinfo-Struktur**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in6_pktinfo) enthalten, die zum Speichern empfangener IPv6-Paketadresseninformationen verwendet wird. Die IPv6-Adresse in der **\_ pktinfo-Struktur von in6** ist die IPv6-Adresse, von der das Paket empfangen wurde.

Wenn eine Anwendung für einen Dual-Stack-Datagrammsocket erfordert, dass die [**LPFN_WSARECVMSG-Funktion (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) Paketinformationen in einer [**WSAMSG-Struktur**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) für Über IPv4 empfangene Datagramme zurücksendert, muss die [ \_ IP-PKTINFO-Socketoption](ip-pktinfo.md) auf dem Socket auf TRUE festgelegt werden. Wenn auf dem Socket nur die IpV6-PKTINFO-Option auf TRUE festgelegt ist, werden Paketinformationen für Datagramme bereitgestellt, die über IPv6 empfangen werden, aber möglicherweise nicht für Datagramme, die über \_ IPv4 empfangen werden.

Beachten Sie, *dass die Ws2ipdef.h-Headerdatei* automatisch in *Ws2tcpip.h* enthalten ist und nie direkt verwendet werden sollte.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                       |
| Header<br/>                   | <dl> <dt>Ws2ipdef.h (einschließlich Ws2tcpip.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Dual-Stack-Sockets](dual-stack-sockets.md)
</dt> <dt>

[**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[**in6 \_ pktinfo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in6_pktinfo)
</dt> <dt>

[IP \_ PKTINFO](ip-pktinfo.md)
</dt> <dt>

[**IPPROTO \_ IPV6-Socketoptionen**](ipproto-ipv6-socket-options.md)
</dt> <dt>

[**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> <dt>

[**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket)
</dt> <dt>

[**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg)
</dt> <dt>

[**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)
</dt> </dl>

 

 
