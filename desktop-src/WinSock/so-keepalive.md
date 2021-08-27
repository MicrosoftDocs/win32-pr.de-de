---
description: Ist so konzipiert, dass eine Anwendung Keep-Alive-Pakete für eine Socketverbindung aktivieren kann.
ms.assetid: d6da7761-7a09-4c91-9737-550590a773b3
title: SO_KEEPALIVE Socketoption (Ws2def.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d3590b8813f584aad16896a5b990baa2e3ad5607b76a13bd987d87961ee5f6f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097470"
---
# <a name="so_keepalive-socket-option"></a>SO \_ KEEPALIVE-Socketoption

Die **\_ Socketoption SO KEEPALIVE** ist so konzipiert, dass eine Anwendung Keep-Alive-Pakete für eine Socketverbindung aktivieren kann.

Rufen Sie zum Abfragen des Status dieser Socketoption die [**getsockopt-Funktion**](/windows/desktop/api/winsock/nf-winsock-getsockopt) auf. Rufen Sie zum Festlegen dieser Option die [**setsockopt-Funktion**](/windows/desktop/api/winsock/nf-winsock-setsockopt) mit den folgenden Parametern auf.

## <a name="socket-option-value"></a>Wert der Socketoption

Die Konstante, die diese Socketoption darstellt, ist 0x0008.

## <a name="syntax"></a>Syntax


```C++
int getsockopt(
  (SOCKET) s,      // descriptor identifying a socket 
  (int) SOL_SOCKET,   // level
  (int) SO_KEEPALIVE, // optname
  (char *) optval, // output buffer,
  (int) optlen,  // size of output buffer
);
```




```C++
int setsockopt(
  (SOCKET) s,      // descriptor identifying a socket 
  (int) SOL_SOCKET,   // level
  (int) SO_KEEPALIVE, // optname
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

Die Ebene, auf der die Option definiert ist. Verwenden **Sie SOL \_ SOCKET** für diesen Vorgang.

</dd> <dt>

*optname* \[ In\]
</dt> <dd>

Die Socketoption, für die der Wert festgelegt werden soll. Verwenden **Sie SO \_ KEEPALIVE** für diesen Vorgang.

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

Wenn der Vorgang erfolgreich abgeschlossen wurde, [**gibt setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) 0 (null) zurück.

Wenn der Vorgang fehlschlägt, wird der Wert SOCKET ERROR zurückgegeben, und ein bestimmter Fehlercode kann durch Aufrufen von \_ [**WSAGetLastError abgerufen werden.**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)



| Fehlercode                                                                                                                                              | Bedeutung                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**[WSANOTINITIALISED](windows-sockets-error-codes-2.md)**</dt> </dl> | Vor der Verwendung dieser Funktion muss ein erfolgreicher [**WSAStartup-Aufruf**](/windows/desktop/api/winsock/nf-winsock-wsastartup) erfolgen.<br/>                                                                                                                                                     |
| <dl> <dt>**[WSAENETDOWN](windows-sockets-error-codes-2.md)**</dt> </dl>             | Fehler beim Netzwerksubsystem.<br/>                                                                                                                                                                                                               |
| <dl> <dt>**[WSAEFAULT](windows-sockets-error-codes-2.md)**</dt> </dl>                 | Einer der *Optval- oder* *optlen-Parameter* zeigen auf den Arbeitsspeicher, der sich nicht in einem gültigen Teil des Benutzeradressenbereichs befindet. Dieser Fehler wird auch zurückgegeben, wenn der Wert, auf den der *optlen-Parameter* verweist, kleiner als die Größe eines **DWORD-Werts** ist.<br/> |
| <dl> <dt>**[WSAEINPROGRESS](windows-sockets-error-codes-2.md)**</dt> </dl>       | Ein blockieren Windows Sockets 1.1-Aufruf wird in Bearbeitung, oder der Dienstanbieter verarbeitet weiterhin eine Rückruffunktion.<br/>                                                                                                                            |
| <dl> <dt>**[WSAEINVAL](windows-sockets-error-codes-2.md)**</dt> </dl>                 | Der *Levelparameter* ist unbekannt oder ungültig. Bei Windows Vista und höher wird dieser Fehler auch zurückgegeben, wenn sich der Socket in einem Übergangszustand befindet.<br/>                                                                                                 |
| <dl> <dt>**[WSAENOPROTOOPT](windows-sockets-error-codes-2.md)**</dt> </dl>       | Die Option ist unbekannt oder wird von der angegebenen Protokollfamilie nicht unterstützt. Dieser Fehler wird zurückgegeben, wenn der im *s-Parameter* übergebene Socketdeskriptor für einen Datagrammsocket gilt.<br/>                                                                   |
| <dl> <dt>**[WSAENOTSOCK](windows-sockets-error-codes-2.md)**</dt> </dl>             | Der Deskriptor ist kein Socket.<br/>                                                                                                                                                                                                                 |



 

## <a name="remarks"></a>Hinweise

Die [**getsockopt-Funktion,**](/windows/desktop/api/winsock/nf-winsock-getsockopt) die mit der **Socketoption SO \_ KEEPALIVE** aufgerufen wird, ermöglicht es einer Anwendung, den aktuellen Zustand der Keepalive-Option abzurufen, obwohl dies ein Feature ist, das normalerweise nicht verwendet wird. Wenn eine Anwendung Keepalive-Pakete auf einem Socket aktivieren muss, ruft sie nur die [**setsockopt-Funktion**](/windows/desktop/api/winsock/nf-winsock-setsockopt) auf, um die Option zu aktivieren.

Mit [**der setsockopt-Funktion,**](/windows/desktop/api/winsock/nf-winsock-setsockopt) die mit der **Socketoption SO \_ KEEPALIVE** aufgerufen wird, kann eine Anwendung Keep-Alive-Pakete für eine Socketverbindung aktivieren. Die **SO \_ KEEPALIVE-Option** für einen Socket ist standardmäßig deaktiviert (auf **FALSE** festgelegt).

Wenn diese Socketoption aktiviert ist, sendet der TCP-Stapel Keep-Alive-Pakete, wenn innerhalb eines Intervalls keine Daten- oder Bestätigungspakete für die Verbindung empfangen wurden. Weitere Informationen zur Keep-Alive-Option finden Sie in Abschnitt 4.2.3.6 des Themas *Requirements for Internet Hosts – Communication Layers specified* in RFC 1122 available at the IETF website (Anforderungen für Internethosts – Kommunikationsebenen gemäß RFC 1122), die auf der [IETF-Website](https://www.ietf.org/rfc/rfc1122.txt)verfügbar sind. (Diese Ressource ist möglicherweise nur auf Englisch verfügbar.)

Die **\_ Socketoption SO KEEPALIVE** ist nur für Protokolle gültig, die keep-alive (verbindungsorientierte Protokolle) unterstützen. Für TCP beträgt das Standardmäßige Keep-Alive-Timeout 2 Stunden und das Keep-Alive-Intervall 1 Sekunde. Die Standardanzahl von Keep-Alive-Tests variiert je nach Version Windows.

Der [**SIO \_ KEEPALIVE \_ VALS-Steuerungscode**](/previous-versions/windows/desktop/legacy/dd877220(v=vs.85)) kann verwendet werden, um Keep-Alive zu aktivieren oder zu deaktivieren und das Timeout und Intervall für eine einzelne Verbindung anzupassen. Wenn Keep-Alive mit **SO \_ KEEPALIVE** aktiviert ist, werden die TCP-Standardeinstellungen für Keep-Alive-Timeout und -Intervall verwendet, es sei denn, diese Werte wurden mithilfe von **SIO \_ KEEPALIVE \_ VALS geändert.**

Der systemweite Standardwert des Keep-Alive-Timeouts kann über die [KeepAliveTime-Registrierungseinstellung](/previous-versions/windows/it-pro/windows-server-2003/cc782936(v=ws.10)) kontrolliert werden, die einen Wert in Millisekunden erfordert. Der systemweite Standardwert des Keep-Alive-Intervalls kann über die [Registrierungseinstellung KeepAliveInterval](/previous-versions/windows/it-pro/windows-server-2003/cc758083(v=ws.10)) kontrolliert werden, die einen Wert in Millisekunden benötigt.

Bei Windows Vista und höher wird die Anzahl der Keep-Alive-Tests (Datenübertragungen) auf 10 festgelegt und kann nicht geändert werden.

Auf Windows Server 2003, Windows XP und Windows 2000 ist die Standardeinstellung für die Anzahl der Keep-Alive-Tests 5. Die Anzahl der Keep-Alive-Tests kann über die Registrierungseinstellungen [TcpMaxDataRetransmissions](/previous-versions/windows/it-pro/windows-server-2003/cc780586(v=ws.10)) und [PPTPTcpMaxDataRetransmissions](/previous-versions/windows/it-pro/windows-server-2003/cc775408(v=ws.10)) kontrolliert werden. Die Anzahl der Keep-Alive-Tests wird auf den größeren der beiden Registrierungsschlüsselwerte festgelegt. Wenn diese Zahl 0 ist, werden keine Keep-Alive-Tests gesendet. Wenn diese Zahl über 255 liegt, wird sie auf 255 angepasst.

Unter Windows Vista und höher kann die **Socketoption SO \_ KEEPALIVE** nur mithilfe der [**setsockopt-Funktion**](/windows/desktop/api/winsock/nf-winsock-setsockopt) festgelegt werden, wenn sich der Socket in einem bekannten Zustand und nicht in einem Übergangszustand befindet. Für TCP sollte die **Socketoption SO \_ KEEPALIVE** entweder festgelegt werden, bevor die Connect-Funktion ([**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect), [**ConnectEx**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex), [**WSAConnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect), [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist)oder [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea)) aufgerufen wird, oder nachdem die Verbindungsanforderung tatsächlich abgeschlossen wurde. Wenn die Connect-Funktion asynchron aufgerufen wurde, muss vor dem Festlegen der **Socketoption SO \_ KEEPALIVE** auf den Verbindungsabschluss gewartet werden. Wenn eine Anwendung versucht, die **Socketoption SO \_ KEEPALIVE** zu setzen, wenn eine Verbindungsanforderung noch in Bearbeitung ist, ist die **setsockopt-Funktion** nicht verfügbar und gibt [WSAEINVAL zurück.](windows-sockets-error-codes-2.md)

Auf Windows Server 2003, Windows XP und Windows 2000 kann die **Socketoption SO \_ KEEPALIVE** mithilfe der [**setsockopt-Funktion**](/windows/desktop/api/winsock/nf-winsock-setsockopt) festgelegt werden, wenn der Socket einen Übergangszustand (eine Verbindungsanforderung wird noch ausgeführt) sowie einen bekannten Zustand auftrat.

Beachten Sie, *dass die Ws2def.h-Headerdatei* automatisch in *Winsock2.h* enthalten ist und nie direkt verwendet werden sollte.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Ws2def.h (einschließlich Winsock2.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> <dt>

[KeepAliveTime](/previous-versions/windows/it-pro/windows-server-2003/cc782936(v=ws.10))
</dt> <dt>

[KeepAliveInterval](/previous-versions/windows/it-pro/windows-server-2003/cc758083(v=ws.10))
</dt> <dt>

[PPTPTcpMaxDataRetransmissions](/previous-versions/windows/it-pro/windows-server-2003/cc775408(v=ws.10))
</dt> <dt>

[**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket)
</dt> <dt>

[**SIO \_ KEEPALIVE \_ VALS**](/previous-versions/windows/desktop/legacy/dd877220(v=vs.85))
</dt> <dt>

[TcpMaxDataRetransmissions](/previous-versions/windows/it-pro/windows-server-2003/cc780586(v=ws.10))
</dt> <dt>

[**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)
</dt> </dl>

 

 
