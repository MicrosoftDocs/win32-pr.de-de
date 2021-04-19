---
description: Ermöglicht es einer Anwendung, Keep-Alive-Pakete für eine Socketverbindung zu aktivieren.
ms.assetid: d6da7761-7a09-4c91-9737-550590a773b3
title: SO_KEEPALIVE Socket-Option (Ws2def. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d829f957e23c48a325444de7d992397fba26d48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359210"
---
# <a name="so_keepalive-socket-option"></a>\_KeepAlive-Socketoption

Die Option " **so \_ KeepAlive** Socket" ermöglicht es einer Anwendung, Keep-Alive-Pakete für eine Socketverbindung zu aktivieren.

Um den Status dieser Socketoption abzufragen, müssen Sie die [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) -Funktion aufrufen. Um diese Option festzulegen, müssen Sie die Funktion [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) mit den folgenden Parametern aufrufen.

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

*Ebene* \[ in\]
</dt> <dd>

Die Ebene, auf der die Option definiert ist. Verwenden Sie für diesen Vorgang den **Sol- \_ Socket** .

</dd> <dt>

*optname* \[ in\]
</dt> <dd>

Die Socketoption, für die der Wert festgelegt werden soll. Verwenden Sie " **\_ KeepAlive** " für diesen Vorgang.

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

Wenn der Vorgang erfolgreich abgeschlossen wird, gibt [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) 0 (null) zurück.

Wenn der Vorgang fehlschlägt, wird der Wert Socket \_ Error zurückgegeben, und es kann ein spezifischer Fehlercode durch Aufrufen von [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)abgerufen werden.



| Fehlercode                                                                                                                                              | Bedeutung                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**[WSANOTINITIALISED](windows-sockets-error-codes-2.md)**</dt> </dl> | Ein erfolgreicher [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) -Befehl muss vor der Verwendung dieser Funktion ausgeführt werden.<br/>                                                                                                                                                     |
| <dl> <dt>**[WSAENETDOWN](windows-sockets-error-codes-2.md)**</dt> </dl>             | Das Netzwerk Subsystem ist fehlgeschlagen.<br/>                                                                                                                                                                                                               |
| <dl> <dt>**[WSAEFAULT](windows-sockets-error-codes-2.md)**</dt> </dl>                 | Einer der *optval* -oder *optlen* -Parameter verweist auf den Arbeitsspeicher, der sich nicht in einem gültigen Teil des Benutzer Adressraums befindet. Dieser Fehler wird auch zurückgegeben, wenn der Wert, auf den der *optlen* -Parameter verweist, kleiner ist als die Größe eines **DWORD** -Werts.<br/> |
| <dl> <dt>**[Wsaeingabe Progress](windows-sockets-error-codes-2.md)**</dt> </dl>       | Ein blockierender Windows Sockets 1,1-Rückruf wird gerade ausgeführt, oder der Dienstanbieter verarbeitet weiterhin eine Rückruffunktion.<br/>                                                                                                                            |
| <dl> <dt>**[Wsaabval](windows-sockets-error-codes-2.md)**</dt> </dl>                 | Der *Level* -Parameter ist unbekannt oder ungültig. Unter Windows Vista und höher wird dieser Fehler auch zurückgegeben, wenn sich der Socket in einem Übergangszustand befunden hat.<br/>                                                                                                 |
| <dl> <dt>**[Wsaumoproumopt](windows-sockets-error-codes-2.md)**</dt> </dl>       | Die Option ist unbekannt oder wird von der angegebener Protokollfamilie nicht unterstützt. Dieser Fehler wird zurückgegeben, wenn der im *s* -Parameter übergebenen socketdeskriptor für einen Datagramm-Socket festgelegt wurde.<br/>                                                                   |
| <dl> <dt>**[Wsaumotsock](windows-sockets-error-codes-2.md)**</dt> </dl>             | Der Deskriptor ist kein Socket.<br/>                                                                                                                                                                                                                 |



 

## <a name="remarks"></a>Bemerkungen

Die [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) -Funktion, die mit der " **so \_ KeepAlive** "-Socketoption aufgerufen wird, ermöglicht es einer Anwendung, den aktuellen Zustand der KeepAlive-Option abzurufen, obwohl diese Funktion normalerweise nicht verwendet wird. Wenn eine Anwendung KeepAlive-Pakete für einen Socket aktivieren muss, ruft Sie die [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) -Funktion auf, um die Option zu aktivieren.

Die [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) -Funktion, die mit der Option " **so \_ KeepAlive** Socket" aufgerufen wird, ermöglicht einer Anwendung, Keep-Alive-Pakete für eine Socketverbindung zu aktivieren Die Option " **so \_ KeepAlive** " für einen Socket ist standardmäßig deaktiviert (auf " **false**" festgelegt).

Wenn diese Socketoption aktiviert ist, sendet der TCP-Stapel Keep-Alive-Pakete, wenn für die Verbindung innerhalb eines Intervalls keine Daten oder Bestätigungs Pakete empfangen wurden. Weitere Informationen zur Keep-Alive-Option finden Sie im Abschnitt 4.2.3.6 zu den *Anforderungen für Internet Hosts –* in RFC 1122 angegebene Kommunikations Schichten auf der [IETF-Website](https://www.ietf.org/rfc/rfc1122.txt). (Diese Ressource ist möglicherweise nur in englischer Sprache verfügbar.)

Die Option " **so \_ KeepAlive** Socket" ist nur für Protokolle gültig, die das Konzept von Keep-Alive (Verbindungs orientierte Protokolle) unterstützen. Bei TCP beträgt das standardmäßige Keep-Alive-Timeout 2 Stunden, und das Keep-Alive-Intervall beträgt 1 Sekunde. Die Standard Anzahl von Keep-Alive-Tests variiert abhängig von der Windows-Version.

Der " [**SIO \_ KeepAlive \_ Vals**](/previous-versions/windows/desktop/legacy/dd877220(v=vs.85)) "-Steuerungs Code kann verwendet werden, um Keep-Alive zu aktivieren bzw. zu deaktivieren und den Timeout und das Intervall für eine einzelne Verbindung anzupassen. Wenn Keep-Alive mit " **so \_ KeepAlive**" aktiviert ist, werden die TCP-Standardeinstellungen für Keep-Alive-Timeout und-Intervall verwendet, es sei denn, diese Werte wurden mithilfe von " **SIO \_ KeepAlive \_ Vals**" geändert.

Der standardmäßige systemweite Wert des Keep-Alive-Timeouts ist über die [KeepAliveTime](/previous-versions/windows/it-pro/windows-server-2003/cc782936(v=ws.10)) -Registrierungs Einstellung steuerbar, die einen Wert in Millisekunden annimmt. Der standardmäßige systemweite Wert des Keep-Alive-Intervalls kann durch die [keepAliveInterval](/previous-versions/windows/it-pro/windows-server-2003/cc758083(v=ws.10)) -Registrierungs Einstellung gesteuert werden, die einen Wert in Millisekunden annimmt.

Unter Windows Vista und höher wird die Anzahl von Keep-Alive-Tests (Neuübertragungen von Daten) auf 10 festgelegt und kann nicht geändert werden.

Unter Windows Server 2003, Windows XP und Windows 2000 ist die Standardeinstellung für die Anzahl von Keep-Alive-Tests 5. Die Anzahl der Keep-Alive-Tests ist über die Registrierungs Einstellungen [TcpMaxDataRetransmissions](/previous-versions/windows/it-pro/windows-server-2003/cc780586(v=ws.10)) und [pptptcpmaxdataretransmissions](/previous-versions/windows/it-pro/windows-server-2003/cc775408(v=ws.10)) steuerbar. Die Anzahl der Keep-Alive-Tests wird auf den größeren der beiden Registrierungsschlüssel Werte festgelegt. Wenn diese Zahl 0 ist, werden Keep-Alive-Tests nicht gesendet. Wenn diese Zahl über 255 liegt, wird Sie an 255 angepasst.

Unter Windows Vista und höher kann die Option " **so \_ KeepAlive** Socket" nur mithilfe der Funktion " [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) " festgelegt werden, wenn sich der Socket in einem bekannten Zustand befindet, der kein Übergangszustand ist. Für TCP muss die Option " **so \_ KeepAlive** Socket" festgelegt werden, bevor die Connect-Funktion ("[**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect)", " [**connectex**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex)", " [**wsaconnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect)", " [**wsaconnectbylist**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist)" oder " [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea)") aufgerufen wird, oder nachdem die Verbindungsanforderung tatsächlich abgeschlossen wurde. Wenn die Connect-Funktion asynchron aufgerufen wurde, erfordert dies das warten auf den Abschluss der Verbindung, bevor versucht wird, die Option " **so \_ KeepAlive** Socket" festzulegen. Wenn eine Anwendung versucht, die Option " **so \_ KeepAlive** Socket" festzulegen, wenn eine Verbindungsanforderung noch verarbeitet wird, schlägt die Funktion " **setsockopt** " fehl und gibt " [WSAEINVAL](windows-sockets-error-codes-2.md)" zurück.

Unter Windows Server 2003, Windows XP und Windows 2000 kann die Option " **so \_ KeepAlive** Socket" mithilfe der Funktion " [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) " festgelegt werden, wenn der Socket ein Übergangszustand ist (eine Verbindungsanforderung wird noch ausgeführt), sowie ein bekannter Zustand.

Beachten Sie, dass die Header Datei " *Ws2def. h* " automatisch in " *Winsock2. h*" enthalten ist und niemals direkt verwendet werden sollte.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Ws2def. h (Include Winsock2. h)</dt> </dl> |



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

[Pptptcpmaxdataretransmissions](/previous-versions/windows/it-pro/windows-server-2003/cc775408(v=ws.10))
</dt> <dt>

[**Glühbirne**](/windows/desktop/api/Winsock2/nf-winsock2-socket)
</dt> <dt>

[**SIO \_ KeepAlive \_ Vals**](/previous-versions/windows/desktop/legacy/dd877220(v=vs.85))
</dt> <dt>

[TcpMaxDataRetransmissions](/previous-versions/windows/it-pro/windows-server-2003/cc780586(v=ws.10))
</dt> <dt>

[**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)
</dt> </dl>

 

 
