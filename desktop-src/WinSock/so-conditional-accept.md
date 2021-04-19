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
# <a name="so_conditional_accept-socket-option"></a>" \_ Conditional \_ Accept"-Socketoption

Die Option " **so \_ bedingtes \_ akzeptieren** " ermöglicht es einer Anwendung, zu entscheiden, ob eine eingehende Verbindung für einen Abhör Socket angenommen werden soll oder nicht.

## <a name="socket-option-value"></a>Wert der Socketoption

Die Konstante, die diese Socketoption darstellt, ist 0x3002.

## <a name="syntax"></a>Syntax


```C++
int setsockopt(
  (SOCKET) s,      // descriptor identifying a socket 
  (int) SOL_SOCKET,   // level
  (int) SO_CONDITIONAL_ACCEPT, // optname
  (char *) optval,         // input buffer,
  (int) optlen,       // size of input buffer
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

Die Socketoption, für die der Wert festgelegt werden soll. Verwenden Sie **daher den \_ bedingten \_ Accept** für diesen Vorgang.

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
| <dl> <dt>**[Wsaabval](windows-sockets-error-codes-2.md)**</dt> </dl>                 | Der *Level* -Parameter ist unbekannt oder ungültig. Dieser Fehler wird auch zurückgegeben, wenn sich der Socket bereits in einem Empfangs Zustand befunden hat.<br/>                                                                                                                        |
| <dl> <dt>**[Wsaumoproumopt](windows-sockets-error-codes-2.md)**</dt> </dl>       | Die Option ist unbekannt oder wird von der angegebener Protokollfamilie nicht unterstützt.<br/>                                                                                                                                                                          |
| <dl> <dt>**[Wsaumotsock](windows-sockets-error-codes-2.md)**</dt> </dl>             | Der Deskriptor ist kein Socket.<br/>                                                                                                                                                                                                                 |



 

## <a name="remarks"></a>Bemerkungen

Die [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) -Funktion, die mit der " **so \_ Conditional \_ Accept** Socket"-Option aufgerufen wird, ermöglicht einer Anwendung, zu entscheiden, ob eine eingehende Verbindung für einen Abhör Socket angenommen werden soll. Die Option für den bedingten Annahme für einen Socket ist standardmäßig deaktiviert (auf **false** festgelegt).

Wenn diese Socketoption aktiviert ist, akzeptiert der TCP-Stapel keine Verbindungen automatisch. Die Anwendung wartet darauf, dass die Anwendung anzeigt, dass Sie die Verbindung über den bedingten Accept-Rückruf annimmt, der bei der [**wsaaccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) -Funktion registriert ist. Nachdem eine Verbindungsanforderung empfangen wurde, ruft Winsock den von der Anwendung registrierten bedingten Accept-Rückruf auf. Nur wenn der bedingte Accept-Rückruf " **CF \_ Accept** " zurückgibt, benachrichtigt Winsock den Transport, dass die Verbindung vollständig akzeptiert wird.

Wenn die Option für den **sogenannten \_ bedingten \_ Accept** -Socket auf aktiviert (auf **true** festgelegt) festgelegt ist, hat dies mehrere Nebeneffekte auf den Socket:

-   Dadurch wird die integrierte Schutzmaßnahmen für den SYN-Angriff des TCP-Stapels deaktiviert, da die Anwendung jetzt den Besitz nimmt, Verbindungen zu akzeptieren.
-   Dadurch wird der Abhör Rückstand deaktiviert, da Verbindungen im Namen eines Abhör Sockets nicht akzeptiert werden. Eine Verbindung wird niemals vollständig akzeptiert, bis die Anwendung die Verwendung des **CF- \_ Accept** -Mechanismus vollständig akzeptiert.
-   Dies bedeutet auch, dass die Anwendung immer in einem-Zustand sein muss, um die Accept-Rückrufe zur Annahme der Verbindung schnell verarbeiten zu können. Wenn die Anwendung mit einer anderen Verarbeitung ausgelastet ist, kann ein Timeout der Clientseite auftreten, bevor die Anwendung die Verbindung tatsächlich akzeptiert. Dies führt zu einem schlechten Client Verhalten.

Der Hauptgrund für Anwendungen, die die bedingte Annahme verwenden, ist die Überprüfung der Quell-IP-Adresse oder des Ports, der vom Verbindungs Client verwendet wird, und dann die Annahme oder Ablehnung der Verbindung zu beschließen. Allerdings ist es wahrscheinlich, dass Anwendungen besser funktionieren, wenn die Option "so \_ bedingtes \_ akzeptieren" nicht aktiviert ist und die Anwendung zulässt, dass der TCP-Stapel und der Abhör Rückstand erwartungsgemäß funktionieren. Wenn die Anwendung dann die akzeptierte Verbindung verarbeitet, kann die Anwendung, wenn Sie von einer ungültigen IP-Quelladresse oder einem Port entfernt wird, den Socket einfach schließen. Der Sicherheits Nachteil dieses Verhaltens besteht darin, dass der Client nun bestätigt hat, dass die Anwendung eine IP-Adresse und einen Port abhört, da die zuvor akzeptierte Verbindung erzwungen wurde. Allerdings wiegen die Nachteile der Aktivierung von **\_ bedingtem \_ Accept** in der Regel diese Einschränkung aus.

Die [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) -Funktion, die mit der " **so \_ Conditional \_ Accept** Socket"-Option aufgerufen wird, ermöglicht einer Anwendung, den aktuellen Zustand der Option "bedingtes akzeptieren" abzurufen, obwohl diese Funktion normalerweise nicht verwendet wird. Wenn eine Anwendung den bedingten Accept-Vorgang für einen Socket aktivieren muss, ruft Sie Justs die [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) -Funktion auf, um die Option zu aktivieren.

Beachten Sie, dass die Header Datei " *Ws2def. h* " automatisch in " *Winsock2. h*" enthalten ist und niemals direkt verwendet werden sollte.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Ws2def. h (Include Winsock2. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> <dt>

[**Wsaaccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept)
</dt> </dl>

 

 




