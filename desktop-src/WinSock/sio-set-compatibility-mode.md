---
description: Fordert an, wie der Netzwerk Stapel bestimmte Verhalten verarbeiten soll, bei denen die Standardmethode für die Handhabung des Verhaltens in Windows-Versionen unterschiedlich sein kann.
ms.assetid: 9574e21f-5ac4-4210-8031-2f3b07416813
title: SIO_SET_COMPATIBILITY_MODE Steuerungs Codes
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 58972595adb71a30728cb4817a80814cd987a6de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345103"
---
# <a name="sio_set_compatibility_mode-control-code"></a>SIO_SET_COMPATIBILITY_MODE Steuerungs Codes

## <a name="description"></a>BESCHREIBUNG

Der **\_ \_ Kompatibilitätsmodus für den Kompatibilitäts \_ Modus von SIO** fordert an, wie der Netzwerk Stapel bestimmte Verhalten verarbeiten soll, bei denen die Standardmethode zum Verarbeiten des Verhaltens in Windows-Versionen unterschiedlich sein kann.

Um diesen Vorgang auszuführen, wenden Sie die [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) -oder **wspioctl** -Funktion mit den folgenden Parametern an.

```cpp
int WSAIoctl(
  (socket) s,             // descriptor identifying a socket
  SIO_SET_COMPATIBILITY_MODE, // dwIoControlCode
  (LPVOID) lpvInBuffer,    // pointer to WSA_COMPATIBILITY_MODE struct
  (DWORD) cbInBuffer,      // length of input buffer
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
  SIO_SET_COMPATIBILITY_MODE, // dwIoControlCode
  (LPVOID) lpvInBuffer,    // pointer to WSA_COMPATIBILITY_MODE struct
  (DWORD) cbInBuffer,      // length of input buffer
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
Verwenden Sie für diesen Vorgang den **\_ \_ Kompatibilitäts \_ Modus "sio festlegen** ".

### <a name="lpvinbuffer"></a>lpvinbuffer

Ein Zeiger auf den Eingabepuffer.
Dieser Parameter sollte auf eine **WSA- \_ Kompatibilitäts \_ Modus** -Struktur zeigen.

### <a name="cbinbuffer"></a>cbinbuffer

Die Größe des Eingabe Puffers in Bytes.
Dieser Parameter muss größer oder gleich der Größe der **WSA- \_ Kompatibilitäts \_ Modus** -Struktur sein, auf die vom *lpvinbuffer* -Parameter verwiesen wird.

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
| **Wsaabval** | Der *dwIoControlCode* -Parameter ist kein gültiger Befehl, oder ein angegebener Eingabeparameter ist nicht zulässig, oder der Befehl ist nicht auf den angegebenen Sockettyp anwendbar. Dieser Fehler wird zurückgegeben, wenn der *cbinbuffer* -Parameter kleiner als der sizeof der **WSA- \_ Kompatibilitäts \_ Modus** -Struktur ist.
| **WSAENETDOWN** | Das Netzwerk Subsystem ist fehlgeschlagen. |
| **Wsaumoproumopt** | Die Socketoption wird für das angegebene Protokoll nicht unterstützt. |
| **WSAENOTCONN** | Die Socket s ist nicht verbunden. |
| **Wsaumotsock** | Der Deskriptor *s* ist kein Socket. |
| **WSAEOPNOTSUPP** | Der angegebene ioctl-Befehl wird nicht unterstützt. Dieser Fehler wird zurückgegeben, wenn der IOCTL- **\_ \_ Kompatibilitäts \_ Modus** für den-Transport nicht vom Transportanbieter unterstützt wird. Dieser Fehler wird auch zurückgegeben, wenn für einen Datagrammsocket versucht wird, den **\_ \_ Kompatibilitäts \_ Modus** für den SIO-Satz zu verwenden. |

## <a name="remarks"></a>Bemerkungen

die IOCTL- **\_ \_ Kompatibilitätsmodus-Kompatibilitäts \_ Modus** fordert an, wie der Netzwerk Stapel bestimmte Verhalten verarbeiten soll, bei denen die Standardmethode zur Handhabung des Verhaltens in Windows-Versionen unterschiedlich sein kann.
Die Eingabe Argument Struktur für **den \_ \_ Kompatibilitäts \_ Modus für den-Kompatibilitätsmodus** wird in der **WSA- \_ Kompatibilitäts \_ Modus** -Struktur angegeben, die in der Header Datei " *mswap*
Ein Zeiger auf die Struktur des **WSA- \_ Kompatibilitäts \_ Modus** wird im *cbinbuffer* -Parameter übergeben.
Diese Struktur ist wie folgt definiert:

```cpp
// Need to #include <mswsock.h>

/* Argument structure for SIO_SET_COMPATIBILITY_MODE */
typedef struct _WSA_COMPATIBILITY_MODE {
    WSA_COMPATIBILITY_BEHAVIOR_ID BehaviorId;
    ULONG TargetOsVersion;
} WSA_COMPATIBILITY_MODE, *PWSA_COMPATIBILITY_MODE;
```

Der im **Verhaltensweise-** Member angegebene Wert gibt das angeforderte Verhalten an.
Der im **targetosversion** -Member angegebene Wert gibt die Windows-Version an, die für das Verhalten angefordert wird.

Der Behavior **orid-** Member kann einer der Werte aus dem Enumerationstyp der **WSA- \_ Kompatibilitäts \_ Verhaltens- \_ ID** sein, der in der Header Datei " *mslisockdef. h* " definiert ist.
Die möglichen Werte für den Member " **verhalarid** " lauten wie folgt:

| Begriff | BESCHREIBUNG |
|------|-------------|
| Wsaverhalorall | Dies entspricht der Anforderung aller möglichen kompatiblen Verhalten, die für die **WSA- \_ Kompatibilitäts \_ Verhaltens- \_ ID** definiert sind. |
| Wsaverhaltereceivepufferung | Wenn das **targetosversion** -Element auf einen Wert für Windows Vista oder höher festgelegt ist, sind die TCP-Empfangs Puffergröße auf diesem Socket mithilfe der Option " **so \_ rcvbuf** " auch nach der Einrichtung einer TCP-Verbindung zulässig. Wenn das **targetosversion** -Element auf einen früheren Wert als Windows Vista festgelegt ist, sind nach dem **herstellen der Verbindung \_** keine Reduzierungen der TCP-Empfangs Puffergröße auf diesem Socket zulässig. |
| Wsaverhalorautotuning | Wenn das **targetosversion** -Element auf einen Wert für Windows Vista oder höher festgelegt ist, ist die automatische Optimierung des Empfangs Fensters aktiviert, und der TCP-Fenster Skalierungsfaktor wird vom Standardwert 8 auf 2 reduziert. Wenn **targetosversion** auf einen früheren Wert als Windows Vista festgelegt ist, ist die automatische Optimierung des Empfangs Fensters deaktiviert. Die Option zum Skalieren von TCP-Fenstern ist ebenfalls deaktiviert, und die maximale tatsächliche Empfangs Fenstergröße ist auf 65.535 Bytes begrenzt. Die Option für die TCP-Fenster Skalierung kann für die Verbindung nicht ausgehandelt werden, auch wenn die Option " **\_ rcvbuf** " für diesen Socket aufgerufen wurde und einen Wert größer als 65.535 Bytes angibt, bevor die Verbindung hergestellt wurde. |

Der **targetosversion** -Member kann eine der ntddi-Versions Konstanten sein, die in der Header Datei " *sdkddkver. h* " definiert sind.
Einige der möglichen Werte für den **targetosversion** -Member lauten wie folgt:

| Begriff | BESCHREIBUNG |
|------|-------------|
| ntddi \_ Longhorn | Das zielverhalten ist die Standardeinstellung für Windows Vista. |
| Ntddi \_ WS03 | Das zielverhalten ist die Standardeinstellung für Windows Server 2003. |
| ntddi- \_ WinXP | Das zielverhalten ist die Standardeinstellung für Windows XP. |
| Ntddi \_ WIN2K | Das zielverhalten ist die Standardeinstellung für Windows 2000. |

Die Haupt Auswirkung des Members **targetosversion** ist, ob dieser Member auf einen Wert gleich oder größer als **ntddi \_ Longhorn** festgelegt ist.

Die TCP-Leistung hängt nicht nur von der Übertragungsrate selbst, sondern auch vom Produkt der Übertragungsrate und der Roundtrip-Verzögerungszeit ab.
Mit diesem Produkt zur Bandbreiten Verzögerung wird die Menge der Daten gemessen, die "die Pipe füllen".
Dieses Produkt mit Bandbreiten Verzögerung ist der für Absender und Empfänger erforderliche Pufferspeicher, um den maximalen Durchsatz der TCP-Verbindung über den Pfad zu erhalten.
Dieser Pufferspeicher stellt die Menge der nicht bestätigten Daten dar, die von TCP verarbeitet werden müssen, damit die Pipeline voll ist.
TCP-Leistungsprobleme treten auf, wenn das Produkt für die Bandbreiten Verzögerung groß ist.
Ein Netzwerkpfad, der unter diesen Bedingungen betrieben wird, wird häufig als "Long, FAT Pipe" bezeichnet.
Beispiele hierfür sind hochleistungsfähige Paket Satelliten Verknüpfungen, drahtlose Hochgeschwindigkeitsverbindungen und über lange Entfernungen unterirdische Fiber-optische Links.

Der TCP-Header verwendet ein 16-Bit-Datenfeld (das Fenster Feld im TCP-Paket Header), um die Größe des Empfangs Fensters an den Absender zu melden.
Daher ist das größte Fenster, das verwendet werden kann, 65.535 bytes.
Um diese Einschränkung zu umgehen, wurde eine TCP-Erweiterungsoption (TCP-Fenster Skala) für Hochleistungs-TCP hinzugefügt, um Windows mit mehr als 65.535 Bytes zuzulassen.
Die TCP-Fenster Skalierungs Option (wsopt) ist in RFC 1323 definiert, die auf der [IETF-Website](https://www.ietf.org/rfc/rfc1122.txt)verfügbar ist.
Die wsopt-Erweiterung erweitert die Definition des TCP-Fensters auf 32 Bits mithilfe eines logarithmischen 1-Byte-Skalierungsfaktors, um das 16-Bit-Fenster Feld im TCP-Header zu erweitern.
Die wsopt-Erweiterung definiert einen impliziten Skalierungsfaktor (2 zu einer Potenz), der verwendet wird, um den Wert der Fenstergröße zu multiplizieren, der in einem TCP-Header gefunden wird, um die tatsächliche Fenstergröße zu erhalten.
Ein Fenster Skalierungsfaktor von 8 ergibt also eine echte Fenstergröße, die dem Wert im Fenster Feld im TCP-Header entspricht, multipliziert mit 2 ^ 8 oder 256.
Wenn das Fenster Feld im TCP-Header auf den maximalen Wert von 65.535 Bytes festgelegt ist und der wsopt-Skalierungsfaktor mit dem Wert 8 ausgehandelt wurde, wäre die echte Fenstergröße 16.776.960 bytes.

Die tatsächliche Empfangs Fenstergröße und somit der Skalierungsfaktor werden durch den maximalen Empfangs Pufferbereich bestimmt.
Der maximale Pufferspeicher ist die Datenmenge, die ein TCP-Empfänger senden kann, bevor auf eine Bestätigung gewartet werden muss.
Nachdem die Verbindung hergestellt wurde, wird die Empfangs Fenstergröße in jedem TCP-Segment (das Fenster Feld im TCP-Header) angekündigt.
Die Ankündigung der maximalen Datenmenge, die der Absender senden kann, ist ein Empfänger seitiger Fluss Steuerungsmechanismus, der verhindert, dass der Absenderdaten sendet, die der Empfänger nicht speichern kann.
Ein sendender Host kann nur die maximale Datenmenge senden, die vom Empfänger angekündigt wird, bevor er auf eine Bestätigung und eine Aktualisierung der Empfangs Fenstergröße wartet.

Unter Windows Server 2003 und Windows XP hat der maximale Empfangs Pufferspeicher, der die Größe des Empfangs Fensters für den TCP/IP-Stapel darstellt, einen Standardwert, der auf der Verbindungsgeschwindigkeit der Sende Schnittstelle basiert.
Der tatsächliche Wert passt sich automatisch an sogar Inkremente der maximalen Segmentgröße (MSS) an, die während der TCP-Verbindungs Herstellung ausgehandelt werden.
Bei einem Link mit einer Länge von 10 MBit/Sek. ist die Standardgröße des Empfangs Fensters normalerweise auf 16K Bytes festgelegt, während bei einem Link von 100 MBit/Sek die Standardgröße des Empfangs Fensters auf 65.535 Bytes festgelegt ist.

Unter Windows Server 2003 und Windows XP kann die tatsächliche maximale Empfangs Fenstergröße für den TCP/IP-Stapel mithilfe der folgenden Registrierungs Werte für eine bestimmte Schnittstelle oder für das gesamte System manuell konfiguriert werden:

`HKEY_LOCAL_MACHINE\SYSTEM\Current Control Set\Services\Tcpip\Parameters\TCPWindowSize`

`HKEY_LOCAL_MACHINE\SYSTEM\Current Control Set\Services\Tcpip\Parameters\Interface\TCPWindowSize`

Der Registrierungs Wert für **TcpWindowSize** kann auf maximal 65.535 Bytes festgelegt werden, wenn die wsopt-Erweiterung nicht verwendet wird, oder maximal 1.073.741.823 Byte, wenn die wsopt-Erweiterung verwendet wird (ein maximaler Skalierungsfaktor von 4 wird unterstützt).
Ohne Fenster Skalierung kann eine Anwendung unabhängig von der Pfad Bandbreite nur einen Durchsatz von ungefähr 5 meits pro Sekunde (Mbit/s) für einen Pfad mit einer Roundtrip-Zeit von 100 Millisekunden (RTT) erzielen.
Dieser Durchsatz kann auf ein Gigabit pro Sekunde (Gbit/s) mit Fenster Skalierung skaliert werden, wodurch TCP den Skalierungsfaktor für die Fenstergröße während der Verbindungs Herstellung aushandeln kann.

Unter Windows Server 2003 und Windows XP kann die wsopt-Erweiterung aktiviert werden, indem der folgende Registrierungs Wert festgelegt wird.

`HKEY_LOCAL_MACHINE\SYSTEM\Current Control Set\Services\Tcpip\Parameters\Tcp1323Opts`

Der Registrierungs Wert " **Tcp1323Opts** " ist ein **DWORD** -codiertes, sodass beim Festlegen von Bit 0 die TCP-wsopt-Erweiterung aktiviert ist.
Wenn Bit 1 festgelegt ist, wird die in RFC 1323 definierte TCP-Zeitstempel Option (tsopt) aktiviert.
Mit einem Wert von 1 oder 3 wird die wsopt-Erweiterung aktiviert.

Unter Windows Server 2003 und Windows XP ist die Standardeinstellung, dass die Registrierungs Werte TcpWindowSize und Tcp1323Opts nicht erstellt werden.
Der Standardwert ist, dass die wsopt-Erweiterung deaktiviert ist und die Größe des TCP-Empfangs Fensters vom System auf den maximalen Wert von bis zu 65.535 Bytes basierend auf der Verbindungsgeschwindigkeit festgelegt wird.
Wenn die Fenster Skalierung unter Windows Server 2003 und Windows XP aktiviert ist, indem der Registrierungs Wert Tcp1323Opts festgelegt wird, wird die Fenster Skalierung für eine TCP-Verbindung immer noch verwendet, wenn sowohl der Absender als auch der Empfänger eine TCP-Fenster Skalierungs Option im zu gegenseitig gesendeten Bereich synchronisieren (SYN) zum Aushandeln eines Fenster Skalierungsfaktors enthalten.
Wenn für eine Verbindung die Fenster Skalierung verwendet wird, wird das Fenster Feld im TCP-Header auf 65.535 Bytes festgelegt, und der Fenster Skalierungsfaktor wird verwendet, um die tatsächliche Empfangs Fenstergröße nach oben um den Fenster Skalierungsfaktor zu ändern, der beim Herstellen der Verbindung ausgehandelt wird.

Eine Anwendung kann die TCP-Empfangs Fenstergröße für eine Verbindung mit der Option " **so \_ rcvbuf** " angeben.
Die Größe des TCP-Empfangs Fensters für einen Socket kann jederzeit mithilfe von **\_ rcvbuf** gesteigert werden. Sie kann jedoch nur vor dem Herstellen einer Verbindung reduziert werden.
Um die Fenster Skalierung zu verwenden, muss eine Anwendung eine Fenstergröße von mehr als 65.535 Bytes angeben, wenn die Option " **so \_ rcvbuf** Socket" verwendet wird, bevor die Verbindung hergestellt wird.

Der ideale Wert für die TCP-Empfangs Fenstergröße ist oft schwierig zu bestimmen.
Zum Auffüllen der Netzwerkkapazität zwischen dem Absender und dem Empfänger sollte die Empfangs Fenstergröße auf das Produkt für die Bandbreiten Verzögerung für die Verbindung festgelegt werden. dabei handelt es sich um die Bandbreite, multipliziert mit der Roundtrip-Zeit.
Auch wenn eine Anwendung das Produkt für die Bandbreiten Verzögerung ordnungsgemäß bestimmen kann, ist es immer noch nicht bekannt, wie schnell die empfangende Anwendung Daten aus dem eingehenden Datenpuffer (der Abruf Rate der Anwendung) abruft.
Trotz der Unterstützung für die TCP-Fenster Skalierung kann die maximale Empfangs Fenstergröße in Windows Server 2003 und Windows XP weiterhin den Durchsatz begrenzen, da es sich um eine maximale maximale Größe für alle TCP-Verbindungen handelt (es sei denn, Sie werden pro Anwendung mithilfe von **\_ rcvbuf** angegeben), wodurch der Durchsatz für einige Verbindungen verbessert und der Durchsatz für andere verringert wird
Darüber hinaus unterscheidet sich die maximale Größe des Empfangs Fensters für eine TCP-Verbindung nicht von der Änderung der Netzwerkbedingungen.

Der TCP/IP-Stapel in Windows Vista unterstützt die Funktion zum automatischen Optimieren von Empfangs Fenstern, um das Problem zu beheben, mit dem der Wert der maximalen Empfangs Fenstergröße für eine TCP-Verbindung basierend auf den aktuellen Netzwerkbedingungen korrekt festgelegt werden kann.
Wenn dieses Feature aktiviert ist, bestimmt die automatische Optimierung des Empfangs Fensters kontinuierlich die optimale echte Empfangs Fenstergröße, indem das Produkt für die Bandbreiten Verzögerung und die Anwendungs Abruf Rate gemessen wird, und passt die tatsächliche maximale Empfangs Fenstergröße basierend auf den veränderten Netzwerkbedingungen an.
Die automatische Optimierung des Empfangs Fensters ermöglicht die TCP-wsopt-Erweiterung standardmäßig, sodass bis zu 16.776.960 bytes für die echte Fenstergröße zugelassen werden.
Wenn die Daten über die Verbindung übertragen werden, überwacht der TCP/IP-Stapel die Verbindung, misst das aktuelle Bandbreiten Verzögerungs Produkt für die Verbindung und die Empfangs Rate der Anwendung und passt die tatsächliche Empfangs Fenstergröße an, um den Durchsatz zu optimieren.
Der TCP/IP-Stapel ändert den Wert des Fenster Felds im TCP-Header basierend auf den Netzwerkbedingungen, da der wsopt-Skalierungsfaktor beim ersten Herstellen der Verbindung korrigiert wird.

Der TCP/IP-Stapel in Windows Vista verwendet nicht mehr die Registrierungs Werte " **TcpWindowSize** ".
Bei einem besseren Durchsatz zwischen TCP-Peers erhöht sich die Auslastung der Netzwerkbandbreite während der Datenübertragung.
Wenn alle Anwendungen für den Empfang von TCP-Daten optimiert sind, kann sich die Gesamtauslastung des Netzwerks erheblich erhöhen. Dadurch wird die Verwendung von Quality of Service (QoS) in Netzwerken, die mit der Kapazität oder nahezu der Kapazität arbeiten, wichtiger.

Das Standardverhalten von Windows Vista für die Empfangs Pufferung, wenn der **markerset- \_ \_ Kompatibilitäts \_ Modus** nicht mithilfe von **wsaverhalorreceivebuffereing** angegeben wird, ist, dass nach dem Herstellen einer Verbindung keine Größe der Empfangs Fenster **Größe verwendet werden \_** kann.

Das Standardverhalten von Windows Vista für die automatische Optimierung, wenn der **\_ \_ Kompatibilitäts \_ Modus** für die Verwendung von " **wsaverhalorautotuning** " nicht angegeben ist, besteht darin, dass der Stapel eine automatische Optimierung des Fensters mit einem Fenster Skalierungsfaktor von 8 empfängt.
Beachten Sie Folgendes: Wenn eine Anwendung eine gültige Empfangs Fenstergröße mit der " **so \_ rcvbuf** "-Socketoption festlegt, verwendet der Stapel die angegebene Größe, und die automatische Optimierung des Fenster Empfangs wird deaktiviert.
Die automatische Optimierung von Windows kann auch vollständig deaktiviert werden, indem der folgende Befehl verwendet wird `netsh interface tcp set global autotuninglevel=disabled` . in diesem Fall hat die Angabe von " **wsaverhalorautotuning** " keine Auswirkung.
Die automatische Optimierung des Fenster Empfangs kann auch basierend auf der Gruppenrichtlinie deaktiviert werden, die unter Windows Server 2008 festgelegt ist.

Die Option **wsaverhalorautotuning** ist unter Windows Vista für einige Internet Gateway-Geräte und Firewalls erforderlich, die Datenflüsse für TCP-Verbindungen, die die wsopt-Erweiterung und einen Windows-Skalierungsfaktor verwenden, nicht ordnungsgemäß unterstützen.
Unter Windows Vista aushandiert ein Empfänger standardmäßig einen Fenster Skalierungsfaktor von 8 für eine maximale echte Fenstergröße von 16.776.960 bytes.
Wenn Daten über einen schnellen Link fließen, beginnt Windows zunächst mit einer 64 Kilobyte echten Fenstergröße, indem das Fenster Feld des TCP-Headers auf 256 festgelegt und der Fenster Skalierungsfaktor in den TCP-Optionen auf 8 festgelegt wird (256 * 2 ^ 8 = 64 KB).
Einige Internet Gateway-Geräte und Firewalls ignorieren den Fenster Skalierungsfaktor und betrachten nur das Feld "angekündigtes Fenster" im als 256 angegebenen TCP-Header und legen eingehende Pakete für die Verbindung ab, die mehr als 256 Bytes an TCP-Daten enthalten.
Zur Unterstützung der Skalierung von TCP-Empfangs Fenstern muss ein Gatewaygerät oder eine Firewall den TCP-Handshake überwachen und den ausgehandelten Fenster Skalierungsfaktor als Teil der TCP-Verbindungsdaten verfolgen.
Außerdem ignorieren einige Anwendungen und TCP-Stapel Implementierungen auf anderen Plattformen die TCP-wsopt-Erweiterung und den Fenster Skalierungsfaktor.
Daher kann der Remote Host, der die Daten sendet, Daten mit der im Feld "Fenster" des TCP-Headers (256 Bytes) angekündigten Rate senden.
Dies kann dazu führen, dass Daten vom Empfänger sehr langsam empfangen werden.

Wenn Sie das Element **verhalted** auf **wsaverhalorautotuning** und die **targetosversion** auf Windows Vista festlegen, wird der Fenster Skalierungsfaktor auf 2 reduziert, sodass das Fenster Feld im TCP-Header anfänglich auf 16.384 Bytes und der Fenster Skalierungsfaktor auf 2 festgelegt ist, sodass eine anfängliche echte Fenster Empfangs Größe von 64 KB beträgt.
Die Funktion zur automatischen Optimierung von Fenstern kann dann die Größe des echten Fenster Empfangs auf bis zu 262.140 bytes erhöhen, indem das Fenster Feld im TCP-Header auf 65.535 Bytes festgelegt wird.
Eine Anwendung sollte den **\_ Kompatibilitätsmodus für den- \_ Kompatibilitäts \_ Modus von SIO** festlegen, sobald ein Socket erstellt wird, da diese Option nicht sinnvoll ist oder nach dem Senden eines SYN-Vorgangs angewendet wird.
Das Festlegen dieser Option hat dieselbe Auswirkung wie der folgende Befehl: `netsh interface tcp set global autotuninglevel=highlyrestricted`

Beachten Sie, dass die Header Datei " *mtausockdef. h* " automatisch in " *mswap. h* " oder " *nettiodef. h*" enthalten ist und nicht direkt verwendet werden sollte.

## <a name="see-also"></a>Siehe auch

[**Glühbirne**](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)

[**Wsagein verlappedresult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**Wsaoverlgetauscht**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**Wsasocketa**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**Wsasocketw**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
