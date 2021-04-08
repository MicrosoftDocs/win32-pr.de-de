---
description: Der Steuercode benachrichtigt eine Anwendung, wenn sich der ideale Wert für den Sende Rückstand für die Verbindung ändert.
ms.assetid: 337883a5-7ceb-40d3-b318-b86dd488b94a
title: SIO_IDEAL_SEND_BACKLOG_CHANGE Steuerungs Codes
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 4eb07efecd39774c60d47cbcf7245c5831760e06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103755072"
---
# <a name="sio_ideal_send_backlog_change-control-code"></a>SIO_IDEAL_SEND_BACKLOG_CHANGE Steuerungs Codes

## <a name="description"></a>BESCHREIBUNG

Der optimale Änderungs Steuerungs Code für den "sio"- **\_ \_ \_ senderückstand \_** benachrichtigt eine Anwendung, wenn sich der Wert des idealen Sende Rückstands (ISB) für die Verbindung ändert.

Um diesen Vorgang auszuführen, wenden Sie die [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) -oder **wspioctl** -Funktion mit den folgenden Parametern an.

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_IDEAL_SEND_BACKLOG_CHANGE, // dwIoControlCode
  NULL,                         // lpvInBuffer
  0,                            // cbInBuffer
  NULL,         // output buffer
  0,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_IDEAL_SEND_BACKLOG_CHANGE, // dwIoControlCode
  NULL,                         // lpvInBuffer
  0,                            // cbInBuffer
  NULL,         // output buffer
  0,       // size of output buffer
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped,   // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
  (LPWSATHREADID) lpThreadId,   // a WSATHREADID structure
  (LPINT) lpErrno   // a pointer to the error code.
);
```

## <a name="parameters"></a>Parameter

### <a name="s"></a>s

Ein Deskriptor, der einen Socket identifiziert.

### <a name="dwiocontrolcode"></a>dwIoControlCode

Der Steuerelement Code für den Vorgang.
Verwenden Sie für diesen Vorgang die **\_ optimale \_ \_ \_ Änderung** des sendebacklogs von SIO.

### <a name="lpvinbuffer"></a>lpvinbuffer

Ein Zeiger auf den Eingabepuffer.
Dieser Parameter wird für diesen Vorgang nicht verwendet.

### <a name="cbinbuffer"></a>cbinbuffer

Die Größe des Eingabe Puffers in Bytes. Dieser Parameter wird für diesen Vorgang nicht verwendet.

### <a name="lpvoutbuffer"></a>lpvoutbuffer

Ein Zeiger auf den Ausgabepuffer.
Dieser Parameter wird für diesen Vorgang nicht verwendet.

### <a name="cboutbuffer"></a>cboutbuffer

Die Größe des Ausgabepuffers in Bytes.
Dieser Parameter muss auf 0 (null) festgelegt werden.

### <a name="lpcbbytesreturned"></a>lpcbbyteszurück gegeben

Ein Zeiger auf eine Variable, die die Größe der im Ausgabepuffer gespeicherten Daten (in Bytes) empfängt.
Dieser zurückgegebene Parameter verweist auf einen **DWORD** -Wert von 0 (null) für diesen Vorgang, da keine Ausgabe vorhanden ist.

### <a name="lpvoverlapped"></a>lpvoverlgetauscht

Ein Zeiger auf eine [**wsaoverllapp**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) -Struktur.

Wenn Socket *s* ohne das überlappende Attribut erstellt wurde, wird der *lpoverllapp* -Parameter ignoriert.

Wenn *s* mit dem überlappenden Attribut geöffnet wurde und der *lpoverlgetauscht* -Parameter nicht **null** ist, wird der Vorgang als überlappende (asynchrone) Operation ausgeführt.
In diesem Fall muss der *lpoverllapp* -Parameter auf eine gültige [**wsaoverllapp**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) -Struktur zeigen.

Bei überlappenden Vorgängen gibt die Funktion [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) oder **wspioctl** sofort zurück, und die entsprechende Vervollständigungs Methode wird signalisiert, wenn der Vorgang abgeschlossen wurde.
Andernfalls gibt die Funktion nicht zurück, bis der Vorgang abgeschlossen ist oder ein Fehler auftritt.

### <a name="lpcompletionroutine"></a>lpCompletionRoutine

Typ: \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)

Ein Zeiger auf die Vervollständigungs Routine, die aufgerufen wird, wenn der Vorgang abgeschlossen wurde (bei nicht überlappenden Sockets ignoriert).

### <a name="lpthreadid"></a>lpthreadid

Ein Zeiger auf eine [**wsathreadid**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) -Struktur, die vom Anbieter in einem nachfolgenden [**wpuqueueapc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc)-Rückruf verwendet werden soll.
Der Anbieter sollte die referenzierte [**wsathreadid**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) -Struktur (nicht den Zeiger auf dieselbe) speichern, bis die [**wpuqueueapc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc) -Funktion zurückgibt.

**Hinweis**  Dieser Parameter gilt nur für die **wspioctl** -Funktion.

### <a name="lperrno"></a>lperrno

Ein Zeiger auf den Fehlercode.

**Hinweis**  Dieser Parameter gilt nur für die **wspioctl** -Funktion.

## <a name="return-value"></a>Rückgabewert

Wenn der Vorgang erfolgreich abgeschlossen wird, gibt die [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) -oder **wspioctl** -Funktion NULL zurück.

Wenn der Vorgang fehlschlägt oder aussteht, gibt die Funktion [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) oder **wspioctl** einen **\_ Socketfehler** zurück.
Um erweiterte Fehlerinformationen abzurufen, nennen Sie [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).

| Fehlercode | Bedeutung |
|------------|---------|
| **ausstehende WSA-e/a \_ \_** | Ein übergebener Vorgang wurde erfolgreich initiiert, und der Abschluss wird zu einem späteren Zeitpunkt angegeben. |
| **WSA- \_ Vorgang \_ abgebrochen** | Ein über Lapp ender Vorgang wurde aufgrund der Schließung des Sockets oder der Ausführung des Befehls " **SIO \_ Flush** ioctl" abgebrochen. |
| **WSAEFAULT** | Der *lpoverllapp* -oder *lpCompletionRoutine* -Parameter ist nicht vollständig in einem gültigen Teil des Benutzer Adressraums enthalten. |
| **Wsaeingabe Progress** | Die-Funktion wird aufgerufen, wenn ein Rückruf ausgeführt wird. |
| **Wsaeingabe** | Ein Blockierungs Vorgang wurde unterbrochen. |
| **Wsaabval** | Der *dwIoControlCode* -Parameter ist kein gültiger Befehl, oder ein angegebener Eingabeparameter ist nicht zulässig, oder der Befehl ist nicht auf den angegebenen Sockettyp anwendbar. Dieser Fehler wird zurückgegeben, wenn der *cboutbuffer* -Parameter nicht 0 (null) ist. |
| **WSAENETDOWN** | Das Netzwerk Subsystem ist fehlgeschlagen. |
| **Wsaumoproumopt** | Die Socketoption wird für das angegebene Protokoll nicht unterstützt. |
| **WSAENOTCONN** | Die Socket *s* ist nicht verbunden. |
| **Wsaumotsock** | Der Deskriptor *s* ist kein Socket. |
| **WSAEOPNOTSUPP** | Der angegebene ioctl-Befehl wird nicht unterstützt. Dieser Fehler wird zurückgegeben, wenn die IOCTL-IOCTL- **\_ Änderung des idealen \_ Sende \_ Rückstands \_** nicht vom Transportanbieter unterstützt wird. Dieser Fehler wird auch zurückgegeben, wenn ein Versuch der Verwendung der optimalen ioctl-Änderung für das **\_ \_ Sende \_ Rückstands \_** Element für einen Datagramm-Socket durchgeführt wird. |

## <a name="remarks"></a>Bemerkungen

Die optimale IOCTL- **\_ \_ \_ \_ Änderung des Sende** Backlogs wird unter Windows Server 2008, Windows Vista mit Service Pack 1 (SP1) und höheren Versionen des Betriebssystems unterstützt.

Beim Senden von Daten über eine TCP-Verbindung mithilfe von Windows Sockets ist es wichtig, dass Sie eine ausreichende Menge an ausstehenden Daten (gesendet, aber noch nicht bestätigt) in TCP aufbewahren, um den höchsten Durchsatz zu erzielen.
Der ideale Wert für die Datenmenge, die für den optimalen Durchsatz für die TCP-Verbindung aussteht, wird als ideale Größe des sendebacklogs (ISB) bezeichnet.
Der ISB-Wert ist eine Funktion des Produkts zur Bandbreiten Verzögerung der TCP-Verbindung und des angekündigten Empfangs Fensters des Empfängers (und zum Teil der Überlastung im Netzwerk).

Der ISB-Wert pro Verbindung ist über die TCP-Protokoll Implementierung in Windows Server 2008, Windows Vista mit SP1 und höheren Versionen des Betriebssystems verfügbar.
Die optimale IOCTL- **\_ \_ \_ \_ Änderung des Sende** Backlogs kann von einer Anwendung verwendet werden, um eine Benachrichtigung zu erhalten, wenn der ISB-Wert für eine Verbindung dynamisch geändert wird.

Unter Windows Server 2008, Windows Vista mit SP1 und höheren Versionen des Betriebssystems werden die Daten von **der \_ optimalen \_ Sende \_ Rückstands \_ Änderung** und der [**\_ optimalen \_ Sende \_ Rückstand \_ Abfrage**](sio-ideal-send-backlog-query.md) IOCTLs von der optimalen Sende Rückstands Abfrage für Stream-orientierte Sockets unterstützt, die verbunden sind.

Der Bereich für den ISB-Wert einer TCP-Verbindung kann theoretisch von 0 bis maximal 16 Megabyte abweichen.

Eine typische Verwendung des ISB-Mechanismus zur Erzielung eines besseren Durchsatzes bei Produkt Verbindungen mit hoher Bandbreiten Verzögerung finden Sie auf der Referenzseite zur IOCTL- [**\_ \_ \_ \_ Abfrage**](sio-ideal-send-backlog-query.md) für den optimalen sendebackbackdukt.

Die optimale IOCTL- **\_ \_ \_ \_ Änderung des Sende** Backlogs ist nur auf einem Stream-Socket zulässig, der sich im verbundenen Zustand befindet.
Andernfalls schlägt die Funktion [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) oder **wspioctl** mit **wsaenotconn** fehl.

Die optimale IOCTL- **\_ \_ \_ \_ Änderung des Sende** Backlogs von "Port" verwendet keine Eingabe-oder Ausgabepuffer und-IDs oder-Blöcke, bis eine ISB-Änderung an der zugrunde liegenden Verbindung erfolgt
Wenn diese IOCTL abgeschlossen ist, kann eine Winsock-Anwendung die IOCTL- [**Abfrage "sio \_ ideal Send \_ backbackbackquery \_ \_**](sio-ideal-send-backlog-query.md) " verwenden, um den neuen ISB-Wert für die Verbindung abzurufen.

Die optimale IOCTL- **\_ \_ \_ \_ Änderung des Sende** Backlogs unterstützt den nicht blockierenden Modus nicht.
Eine Anwendung ist berechtigt, diese IOCTL für einen nicht blockierenden Socket auszugeben, aber die IOCTL wird einfach blockiert oder per ausgesetzt blockiert, bis der ISB-Wert geändert wird.

Wenn die Parameter *lpoverlgetauscht* und *lpCompletionRoutine* NULL sind, wird der Socket in dieser Funktion als nicht überlappenden Socket behandelt.
Bei einem nicht überlappenden Socket werden die Parameter *lpoverlgetauscht* und *lpCompletionRoutine* ignoriert, mit der Ausnahme, dass die Funktion blockiert werden kann, wenn sich Socket *s* im Blockierungs Modus befindet.
Wenn sich Socket *s* im nicht blockierenden Modus befindet, wird diese Funktion immer noch blockiert, da diese spezielle ioctl den nicht blockierenden Modus nicht unterstützt.

Bei überlappenden Sockets werden Vorgänge, die nicht sofort abgeschlossen werden können, initiiert, und der Abschluss wird zu einem späteren Zeitpunkt angegeben.

Alle ioctl können unbegrenzt blockieren, abhängig von der Implementierung des Dienstanbieters.
Wenn die Anwendung die Blockierung in einem [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) -oder **wspioctl** -Funktions aufrufnis nicht tolerieren kann, werden überlappende e/a-Vorgänge für IOCTLs empfohlen, die besonders wahrscheinlich blockiert werden.

Der optimale ioctl-Wert für die **\_ \_ Sende \_ Rückstands \_ Änderung** von "sio" stellt eine Benachrichtigung bereit und wird erwartet, bis der ISB-Wert geändert wird.
Daher wird er normalerweise asynchron aufgerufen, wenn der *lpoverllapp* -Parameter auf eine gültige, wsaoverllapp Ende Struktur festgelegt ist.

**In den** folgenden Fällen kann bei der Änderung der IOCTL-Änderung bei der **\_ optimalen \_ Sende \_ Rückstands \_ Änderung** **ein Fehler auftreten \_ \_** :

* Die TCP-Verbindung ist in der Senderichtung ordnungsgemäß getrennt. Dies kann ein Ergebnis eines Aufrufs der Funktion zum Herunterfahren mit dem auf **SD \_ Send** festgelegten Parameter, einem Aufrufen der **disconnectex** -Funktion oder eines Aufrufs der Funktion **TransmitFile** oder **transmitpaketen** mit dem Parameter *dwFlags* , der auf **tf \_ Disconnect** oder TF- **\_ Wiederverwendung** festgelegt ist.
* Die TCP-Verbindung wurde zurückgesetzt oder abgebrochen.
* Die Anwendung gibt die IOCTL-Änderung von "sio ideal Send backbackbacklogs" aus, wenn bereits eine Benachrichtigung über eine **\_ \_ gesendete \_ \_** Benachrichtigung Nur 1 1 gesendete SIO-ideale Änderungsanforderungen für den **\_ \_ Sende \_ Rückstand \_** sind gleichzeitig zulässig.
* Die Anforderung wird vom e/a-Manager abgebrochen.
* Der Socket ist geschlossen.

In der Header Datei " *Ws2tcpip. h* " sind zwei Inline-Wrapper Funktionen für diese IOCTLs definiert.
Es wird empfohlen, dass diese Inline Funktionen anstelle der **\_ optimalen optimalen \_ Sende \_ Rückstands \_ Änderung** und der [**\_ optimalen \_ Sende Rückstands Abfrage von der optimalen Sende \_ Rückstands \_ Abfrage**](sio-ideal-send-backlog-query.md) IOCTLs verwendet werden.

Die Funktion "Inline Wrapper" für die IOCTL-Änderung von " **SIO \_ ideal \_ Send \_ \_** Backlogs" ist die Funktion " **idesendbacklognotify** ".

Die Funktion "Inline Wrapper" für die IOCTL- [**\_ \_ \_ \_ Abfrage des optimalen**](sio-ideal-send-backlog-query.md) sendebacklogs ist die Funktion " **ideal Send backlogquery** ".

## <a name="see-also"></a>Siehe auch

[**SIO_IDEAL_SEND_BACKLOG_QUERY**](sio-ideal-send-backlog-query.md)

[**Glühbirne**](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)

[**Wsagein verlappedresult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**Wsaoverlgetauscht**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**Wsasocketa**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**Wsasocketw**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
