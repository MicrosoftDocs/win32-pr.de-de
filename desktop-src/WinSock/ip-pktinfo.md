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
# <a name="ip_pktinfo-socket-option"></a>IP \_ pktinfo-Socketoption

Die IP \_ pktinfo-Socketoption ermöglicht es einer Anwendung, die Rückgabe von Paketinformationen durch die [**LPFN_WSARECVMSG (wsarecvmsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) -Funktion auf einem IPv4-Socket zu aktivieren oder zu deaktivieren.

Um den Status dieser Socketoption abzufragen, müssen Sie die [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) -Funktion aufrufen. Um diese Option festzulegen, müssen Sie die Funktion [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) mit den folgenden Parametern aufrufen.

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

*Ebene* \[ in\]
</dt> <dd>

Die Ebene, auf der die Option definiert ist. Verwenden Sie **ipproto \_ IP** für diesen Vorgang.

</dd> <dt>

*optname* \[ in\]
</dt> <dd>

Die Socketoption, für die der Wert festgelegt oder festgelegt werden soll. Verwenden Sie \_ für diesen Vorgang IP pktinfo.

</dd> <dt>

*optval* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf den Puffer, der den Wert für die festzulegende Option enthält. Dieser Parameter sollte auf einen Puffer zeigen, der größer oder gleich der Größe eines **DWORD** -Werts ist.

Dieser Wert wird als boolescher Wert behandelt, wobei 0 verwendet wird, um **false** (deaktiviert) und einen Wert ungleich 0 (null) anzugeben, um **true** (aktiviert) anzugeben.

</dd> <dt>

*optlen* \[ in, out\]
</dt> <dd>

Ein Zeiger auf die Größe des *optval* -Puffers in Bytes. Diese Größe muss größer oder gleich der Größe eines **DWORD** -Werts sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn der Vorgang erfolgreich abgeschlossen wird, gibt die Funktion [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) oder [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) NULL zurück.

Wenn der Vorgang fehlschlägt, wird der Wert Socket \_ Error zurückgegeben, und es kann ein spezifischer Fehlercode durch Aufrufen von [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)abgerufen werden.



| Fehlercode                                                                                                                                              | Bedeutung                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**[WSANOTINITIALISED](windows-sockets-error-codes-2.md)**</dt> </dl> | Ein erfolgreicher [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) -Befehl muss vor der Verwendung dieser Funktion ausgeführt werden.<br/>                                                                                                                                                     |
| <dl> <dt>**[WSAENETDOWN](windows-sockets-error-codes-2.md)**</dt> </dl>             | Das Netzwerk Subsystem ist fehlgeschlagen.<br/>                                                                                                                                                                                                               |
| <dl> <dt>**[WSAEFAULT](windows-sockets-error-codes-2.md)**</dt> </dl>                 | Einer der *optval* -oder *optlen* -Parameter verweist auf den Arbeitsspeicher, der sich nicht in einem gültigen Teil des Benutzer Adressraums befindet. Dieser Fehler wird auch zurückgegeben, wenn der Wert, auf den der *optlen* -Parameter verweist, kleiner ist als die Größe eines **DWORD** -Werts.<br/> |
| <dl> <dt>**[Wsaeingabe Progress](windows-sockets-error-codes-2.md)**</dt> </dl>       | Ein blockierender Windows Sockets 1,1-Rückruf wird gerade ausgeführt, oder der Dienstanbieter verarbeitet weiterhin eine Rückruffunktion.<br/>                                                                                                                            |
| <dl> <dt>**[Wsaabval](windows-sockets-error-codes-2.md)**</dt> </dl>                 | Ein ungültiges Argument wurde angegeben. Dieser Fehler wird zurückgegeben, wenn der *Level* -Parameter unbekannt oder ungültig ist. Unter Windows Vista und höher wird dieser Fehler auch zurückgegeben, wenn sich der Socket in einem Übergangszustand befunden hat.<br/>                                     |
| <dl> <dt>**[Wsaumoproumopt](windows-sockets-error-codes-2.md)**</dt> </dl>       | Die Option ist unbekannt oder wird von der angegebener Protokollfamilie nicht unterstützt. Dieser Fehler wird zurückgegeben, wenn der *Typparameter für den socketdeskriptor* , der in den *s* -Parameter übergeben wurde, kein **Sock- \_ dgram** oder **Sock- \_ RAW** ist <br/>                          |
| <dl> <dt>**[Wsaumotsock](windows-sockets-error-codes-2.md)**</dt> </dl>             | Der Deskriptor ist kein Socket.<br/>                                                                                                                                                                                                                 |



 

## <a name="remarks"></a>Bemerkungen

Die [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) -Funktion, die mit der IP \_ pktinfo-Socketoption aufgerufen wird, ermöglicht einer Anwendung, festzustellen, ob Paketinformationen von der [**LPFN_WSARECVMSG (wsarecvmsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)-Funktion für einen IPv4-Socket zurückgegeben werden.

Die [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) -Funktion, die mit der IP \_ pktinfo-Socketoption aufgerufen wird, ermöglicht es einer Anwendung, die Rückgabe von Paketinformationen durch die [**LPFN_WSARECVMSG (wsarecvmsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) -Funktion zu aktivieren oder zu deaktivieren. Die \_ Option IP pktinfo für einen Socket ist standardmäßig deaktiviert (auf **false** festgelegt).

Wenn diese Socketoption auf einem IPv4-Socket vom Typ **Sock \_ dgram** oder **Sock \_ RAW** aktiviert ist, gibt die Funktion [**LPFN_WSARECVMSG (wsarecvmsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) Paketinformationen in der [**wsamsg**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) -Struktur zurück, auf die durch den *lpmsg* -Parameter verwiesen wird. Eines der Steuerungsdaten Objekte in der zurückgegebenen **wsamsg** -Struktur enthält eine [**in \_ pktinfo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in_pktinfo) -Struktur, die zum Speichern von Informationen zu empfangenen Paket Adressen verwendet wird.

Für Datagramme, die von der [**LPFN_WSARECVMSG (wsarecvmsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) -Funktion über IPv4 empfangen werden, enthält das **Steuer** Element Mitglied der [**wsamsg**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) -Struktur eine [**WSABUF**](/windows/desktop/api/ws2def/ns-ws2def-wsabuf) -Struktur, die eine **wsacmsghdr** -Struktur enthält. Der Member der **CMSG- \_ Ebene** dieser **wsacmsghdr** -Struktur würde **ipproto \_ IP** enthalten, der **CMSG- \_ Typmember** dieser Struktur würde **IP \_ pktinfo** enthalten, und der **CMSG- \_ Datenmember** enthält eine [**in \_ pktinfo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in_pktinfo) -Struktur, die zum Speichern der empfangenen IPv4-Paket Adressinformationen verwendet wird. Die IPv4-Adresse in der **in \_ pktinfo** -Struktur ist die IPv4-Adresse, von der das Paket empfangen wurde.

Wenn eine Anwendung für einen Datagramm-Socket mit zwei Stapeln die [**LPFN_WSARECVMSG (wsarecvmsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) -Funktion benötigt, um Paketinformationen in einer [**wsamsg**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) -Struktur für über IPv4 Empfangene Datagramme zurückzugeben, muss die IP \_ pktinfo-Socketoption für den Socket auf true festgelegt werden. Wenn nur die [IPv6- \_ pktinfo](ipv6-pktinfo.md) -Option im Socket auf true festgelegt ist, werden Paketinformationen für über IPv6 Empfangene Datagramme bereitgestellt, jedoch nicht für Datagramme, die über IPv4 empfangen werden.

Wenn eine Anwendung versucht, die IP- \_ pktinfo-Socketoption auf einem Dual-Stack-Datagramm-Socket festzulegen, und IPv4 auf dem System deaktiviert ist, schlägt die Funktion " [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) " fehl, und " [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) " wird mit dem Fehler " [WSAEINVAL](windows-sockets-error-codes-2.md)" zurückgegeben. Dieser Fehler wird auch durch die Funktion " **setsockopt** " aufgrund anderer Fehler zurückgegeben. Wenn eine Anwendung versucht, eine \_ Socketoption auf ipproto-IP-Ebene in einem Dual-Stack-Socket festzulegen, und Sie mit [WSAEINVAL](windows-sockets-error-codes-2.md)fehlschlägt, sollte die Anwendung ermitteln, ob IPv4 auf dem lokalen Computer deaktiviert ist. Eine Methode, die verwendet werden kann, um zu ermitteln, ob IPv4 aktiviert oder deaktiviert ist, besteht darin, die [**Socketfunktion**](/windows/desktop/api/Winsock2/nf-winsock2-socket) mit dem auf AF inet festgelegten *AF* -Parameter aufzurufen, \_ um einen IPv4-Socket zu erstellen. Wenn die **Socketfunktion** ausfällt und **WSAGetLastError** einen Fehler von [WSAEAFNOSUPPORT](windows-sockets-error-codes-2.md)zurückgibt, bedeutet dies, dass IPv4 nicht aktiviert ist. In diesem Fall kann ein **setsockopt** -Funktionsfehler auftreten, wenn versucht wird, die IP \_ pktinfo-Socketoption festzulegen, kann die Anwendung ignoriert werden. Andernfalls sollte bei dem Versuch, die \_ Socketoption IP pktinfo festzulegen, ein unerwarteter Fehler behandelt werden.

Beachten Sie, dass die Header Datei " *Ws2ipdef. h* " automatisch in " *Ws2tcpip. h*" enthalten ist und niemals direkt verwendet werden sollte.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                       |
| Header<br/>                   | <dl> <dt>Ws2ipdef. h (Include Ws2tcpip. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Dual-Stack-Sockets](dual-stack-sockets.md)
</dt> <dt>

[**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[**in \_ pktinfo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in_pktinfo)
</dt> <dt>

[**Ipproto \_ IP-Socketoptionen**](ipproto-ip-socket-options.md)
</dt> <dt>

[IPv6- \_ pktinfo](ipv6-pktinfo.md)
</dt> <dt>

[**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> <dt>

[**Glühbirne**](/windows/desktop/api/Winsock2/nf-winsock2-socket)
</dt> <dt>

[**Wsamsg**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg)
</dt> <dt>

[**LPFN_WSARECVMSG (wsarecvmsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)
</dt> </dl>

 

 
