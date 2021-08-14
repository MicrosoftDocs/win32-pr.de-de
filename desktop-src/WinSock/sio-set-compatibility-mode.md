---
description: Fordert an, wie der Netzwerkstapel bestimmte Verhaltensweisen verarbeiten soll, für die sich die Standardbehandlung des Verhaltens in Windows Versionen unterscheiden kann.
ms.assetid: 9574e21f-5ac4-4210-8031-2f3b07416813
title: SIO_SET_COMPATIBILITY_MODE-Steuerelementcode
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: ee0cb99f4ad55d4b6df60c71845c40fdfa3c2a3c1dff167f8009c0d1711ad997
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119384050"
---
# <a name="sio_set_compatibility_mode-control-code"></a>SIO_SET_COMPATIBILITY_MODE-Steuerelementcode

## <a name="description"></a>BESCHREIBUNG

Der **SIO \_ SET COMPATIBILITY \_ \_ MODE-Steuerungscode** fordert an, wie der Netzwerkstapel bestimmte Verhaltensweisen verarbeiten soll, bei denen sich die Standardbehandlungsart des Verhaltens in Windows Versionen unterscheiden kann.

Rufen Sie zum Ausführen dieses Vorgangs die [**Funktion WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) oder **WSPIoctl** mit den folgenden Parametern auf.

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

Der Steuerelementcode für den Vorgang.
Verwenden Sie für diesen Vorgang **SIO \_ SET COMPATIBILITY \_ \_ MODE.**

### <a name="lpvinbuffer"></a>lpvInBuffer

Ein Zeiger auf den Eingabepuffer.
Dieser Parameter sollte auf eine **WSA \_ COMPATIBILITY \_ MODE-Struktur** verweisen.

### <a name="cbinbuffer"></a>cbInBuffer

Die Größe des Eingabepuffers in Bytes.
Dieser Parameter sollte gleich oder größer als die Größe der **WSA \_ COMPATIBILITY \_ MODE-Struktur** sein, auf die der *lpvInBuffer-Parameter* zeigt.

### <a name="lpvoutbuffer"></a>lpvOutBuffer

Ein Zeiger auf den Ausgabepuffer.
Dieser Parameter wird für diesen Vorgang nicht verwendet.

### <a name="cboutbuffer"></a>cbOutBuffer

Die Größe des Ausgabepuffers in Bytes.
Dieser Parameter muss auf 0 (null) festgelegt werden.

### <a name="lpcbbytesreturned"></a>lpcbBytesReturned

Ein Zeiger auf eine Variable, die die Größe der im Ausgabepuffer gespeicherten Daten in Bytes empfängt.
Dieser zurückgegebene Parameter zeigt auf den **DWORD-Wert** 0 (null) für diesen Vorgang, da keine Ausgabe vorhanden ist.

### <a name="lpvoverlapped"></a>lpvOverlapped

Ein Zeiger auf eine [**WSAOVERLAPPED-Struktur.**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

Wenn *Sockets* ohne das überlappende Attribut erstellt wurden, wird der *lpOverlapped-Parameter* ignoriert.

Wenn *s* mit dem überlappende Attribut geöffnet wurde und der *lpOverlapped-Parameter* nicht **NULL** ist, wird der Vorgang als überlappender (asynchroner) Vorgang ausgeführt.
In diesem Fall muss der *lpOverlapped-Parameter* auf eine gültige [**WSAOVERLAPPED-Struktur**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) verweisen.

Für überlappende Vorgänge gibt die [**WSAIoctl-**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) oder **WSPIoctl-Funktion** sofort zurück, und die entsprechende Vervollständigungsmethode wird signalisiert, wenn der Vorgang abgeschlossen wurde.
Andernfalls gibt die Funktion erst dann zurück, wenn der Vorgang abgeschlossen wurde oder ein Fehler auftritt.

### <a name="lpcompletionroutine"></a>lpCompletionRoutine

Typ: \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)

Ein Zeiger auf die Abschlussroutine, die aufgerufen wird, wenn der Vorgang abgeschlossen wurde (wird für nicht überlappende Sockets ignoriert).

### <a name="lpthreadid"></a>lpThreadId

Ein Zeiger auf eine [**WSATHREADID-Struktur,**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) die vom Anbieter in einem nachfolgenden Aufruf von [**WPUQueueApc**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc)verwendet werden soll.
Der Anbieter sollte die [**referenzierte WSATHREADID-Struktur**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) (nicht den Zeiger auf denselben) speichern, bis die [**WPUQueueApc-Funktion**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc) zurückgegeben wurde.

**Hinweis**  Dieser Parameter gilt nur für die **WSPIoctl-Funktion.**

### <a name="lperrno"></a>lpErrno

Ein Zeiger auf den Fehlercode.

**Hinweis**  Dieser Parameter gilt nur für die **WSPIoctl-Funktion.**

## <a name="return-value"></a>Rückgabewert

Wenn der Vorgang erfolgreich abgeschlossen wurde, gibt die [**WSAIoctl-**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) oder **WSPIoctl-Funktion** 0 (null) zurück.

Wenn der Vorgang fehlschlägt oder aussteht, gibt die [**WSAIoctl-**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) oder **WSPIoctl-Funktion** **SOCKET \_ ERROR** zurück.
Um erweiterte Fehlerinformationen abzurufen, rufen [**Sie WSAGetLastError auf.**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)

| Fehlercode | Bedeutung |
|------------|---------|
| **WSA \_ IO \_ PENDING** | Ein überlappender Vorgang wurde erfolgreich initiiert, und der Abschluss wird zu einem späteren Zeitpunkt angezeigt. |
| **\_WSA-VORGANG \_ ABGEBROCHEN** | Ein überlappender Vorgang wurde aufgrund des Schließens des Sockets oder der Ausführung des **SIO \_ FLUSH** IOCTL-Befehls abgebrochen. |
| **WSAEFAULT** | Der *lpOverlapped-* oder *lpCompletionRoutine-Parameter* ist nicht vollständig in einem gültigen Teil des Benutzeradressraums enthalten. |
| **WSAEINPROGRESS** | Die Funktion wird aufgerufen, wenn ein Rückruf ausgeführt wird. |
| **WSAEINTR** | Ein Blockierungsvorgang wurde unterbrochen. |
| **WSAEINVAL** | Der *dwIoControlCode-Parameter* ist kein gültiger Befehl, oder ein angegebener Eingabeparameter ist nicht akzeptabel, oder der Befehl gilt nicht für den angegebenen Sockettyp. Dieser Fehler wird zurückgegeben, wenn der *cbInBuffer-Parameter* kleiner als die Größe der **WSA \_ COMPATIBILITY \_ MODE-Struktur** ist.
| **WSAENETDOWN** | Fehler beim Netzwerksubsystem. |
| **WSAENOPROTOOPT** | Die Socketoption wird für das angegebene Protokoll nicht unterstützt. |
| **WSAENOTCONN** | Die Sockets sind nicht verbunden. |
| **WSAENOTSOCK** | Der Deskriptor *s* ist kein Socket. |
| **WSAEOPNOTSUPP** | Der angegebene IOCTL-Befehl wird nicht unterstützt. Dieser Fehler wird zurückgegeben, wenn die **SIO \_ SET COMPATIBILITY \_ \_ MODE** IOCTL vom Transportanbieter nicht unterstützt wird. Dieser Fehler wird auch zurückgegeben, wenn versucht wird, **SIO \_ SET COMPATIBILITY \_ \_ MODE** IOCTL für einen Datagrammsocket zu verwenden. |

## <a name="remarks"></a>Hinweise

Der **SIO \_ SET COMPATIBILITY \_ \_ MODE** IOCTL fordert an, wie der Netzwerkstapel bestimmte Verhaltensweisen behandeln soll, bei denen sich die Standardbehandlung des Verhaltens in Windows Versionen unterscheiden kann.
Die Eingabeargumentstruktur für **SIO \_ SET COMPATIBILITY \_ \_ MODE** wird in der **WSA COMPATIBILITY \_ \_ MODE-Struktur** angegeben, die in der *Headerdatei Mswsockdef.h* definiert ist.
Ein Zeiger auf die **WSA \_ COMPATIBILITY \_ MODE-Struktur** wird im *cbInBuffer-Parameter* übergeben.
Diese Struktur ist wie folgt definiert:

```cpp
// Need to #include <mswsock.h>

/* Argument structure for SIO_SET_COMPATIBILITY_MODE */
typedef struct _WSA_COMPATIBILITY_MODE {
    WSA_COMPATIBILITY_BEHAVIOR_ID BehaviorId;
    ULONG TargetOsVersion;
} WSA_COMPATIBILITY_MODE, *PWSA_COMPATIBILITY_MODE;
```

Der im **BehaviorId-Member** angegebene Wert gibt das angeforderte Verhalten an.
Der im **TargetOsVersion-Member** angegebene Wert gibt die Windows Version an, die für das Verhalten angefordert wird.

Der **BehaviorId-Member** kann einer der Werte aus dem **WSA \_ COMPATIBILITY BEHAVIOR \_ ID-Enumerationstyp \_** sein, der in der *Headerdatei "Mswsockdef.h"* definiert ist.
Die möglichen Werte für den **BehaviorId-Member** sind:

| Begriff | BESCHREIBUNG |
|------|-------------|
| WsaBehaviorAll | Dies entspricht dem Anfordern aller möglichen kompatiblen Verhaltensweisen, die für die **WSA \_ COMPATIBILITY BEHAVIOR \_ \_ ID** definiert sind. |
| WsaBehaviorReceiveBuffering | Wenn das **TargetOsVersion-Element** auf einen Wert für Windows Vista oder höher festgelegt ist, sind Reduzierungen der TCP-Empfangspuffergröße für diesen Socket mithilfe der **SO \_ RCVBUF-Socketoption** auch nach dem Herstellen einer TCP-Verbindung zulässig. Wenn das **TargetOsVersion-Element** auf einen Wert vor Windows Vista festgelegt ist, sind Reduzierungen der TCP-Empfangspuffergröße für diesen Socket mithilfe der **SO \_ RCVBUF-Socketoption** nach dem Herstellen der Verbindung nicht zulässig. |
| WsaBehaviorAutoTuning | Wenn das **TargetOsVersion-Element** auf einen Wert für Windows Vista oder höher festgelegt ist, wird die automatische Optimierung des Empfangsfensters aktiviert, und der TCP-Fensterskalierungsfaktor wird vom Standardwert 8 auf 2 reduziert. Wenn **TargetOsVersion** auf einen Wert vor Windows Vista festgelegt ist, ist die automatische Optimierung des Empfangsfensters deaktiviert. Die TCP-Fensterskalierungsoption ist ebenfalls deaktiviert, und die maximale True-Empfangsfenstergröße ist auf 65.535 Bytes beschränkt. Die TCP-Fensterskalierungsoption kann für die Verbindung nicht ausgehandelt werden, auch wenn die **SO \_ RCVBUF-Socketoption** für diesen Socket aufgerufen wurde und einen Wert von mehr als 65.535 Bytes angibt, bevor die Verbindung hergestellt wurde. |

Der **TargetOsVersion-Member** kann eine der NTDDI-Versionskonstanten sein, die in der *Headerdatei Sdkddkver.h* definiert sind.
Einige der möglichen Werte für das **TargetOsVersion-Element** sind wie folgt:

| Begriff | BESCHREIBUNG |
|------|-------------|
| NTDDI \_ LONGHORN | Das Zielverhalten ist die Standardeinstellung für Windows Vista. |
| NTDDI \_ WS03 | Das Zielverhalten ist die Standardeinstellung für Windows Server 2003. |
| NTDDI \_ WINXP | Das Zielverhalten ist die Standardeinstellung für Windows XP. |
| NTDDI \_ WIN2K | Das Zielverhalten ist die Standardeinstellung für Windows 2000. |

Der hauptteilliche Einfluss des **TargetOsVersion-Members** ist, ob dieser Member auf einen Wert festgelegt ist, der gleich oder größer als **NTDDI \_ LONGHORN** ist.

Die TCP-Leistung hängt nicht nur von der Übertragungsrate selbst ab, sondern auch vom Produkt der Übertragungsrate und der Roundtripverzögerungszeit.
Dieses Produkt mit Bandbreitenverzögerung misst die Datenmenge, die "die Pipe füllen" würde.
Dieses Produkt mit Bandbreitenverzögerung ist der Pufferspeicherplatz, der beim Absender und Empfänger erforderlich ist, um den maximalen Durchsatz für die TCP-Verbindung über den Pfad zu erhalten.
Dieser Pufferspeicher stellt die Menge der nicht bestätigten Daten dar, die TCP verarbeiten muss, um die Pipeline voll zu halten.
TCP-Leistungsprobleme treten auf, wenn das Produkt mit Bandbreitenverzögerung groß ist.
Ein Netzwerkpfad, der unter diesen Bedingungen betrieben wird, wird häufig als "long, fat pipe" bezeichnet.
Beispiele hierfür sind Paketsatellitenverbindungen mit hoher Kapazität, Hochgeschwindigkeits-Drahtlosverbindungen und glasfaseroptische Verbindungen über lange Entfernungen.

Der TCP-Header verwendet ein 16-Bit-Datenfeld (das Feld Window im TCP-Paketheader), um die Größe des Empfangsfensters an den Absender zu melden.
Daher ist das größte Fenster, das verwendet werden kann, 65.535 Bytes.
Um diese Einschränkung zu umgehen, wurde die TCP-Erweiterungsoption TCP-Fensterskalierung für Hochleistungs-TCP hinzugefügt, um Fenster zuzulassen, die größer als 65.535 Bytes sind.
Die TCP-Fensterskalierungsoption (WSopt) ist in RFC 1323 definiert, die auf der [IETF-Website](https://www.ietf.org/rfc/rfc1122.txt)verfügbar ist.
Die WSopt-Erweiterung erweitert die Definition des TCP-Fensters mithilfe eines logarithmischen 1-Byte-Skalierungsfaktors auf 32 Bit, um das 16-Bit-Fensterfeld im TCP-Header zu erweitern.
Die WSopt-Erweiterung definiert einen impliziten Skalierungsfaktor (2 bis eine gewisse Leistung), der verwendet wird, um den Wert der Fenstergröße in einem TCP-Header zu multiplizieren, um die tatsächliche Fenstergröße zu erhalten.
Ein Fensterskalationsfaktor von 8 würde also zu einer echten Fenstergröße führen, die dem Wert im Feld Fenster im TCP-Header multipliziert mit 2^8 oder 256 entspricht.
Wenn das Feld Fenster im TCP-Header auf den maximalen Wert von 65.535 Bytes festgelegt und der WSopt-Skalierungsfaktor auf den Wert 8 ausgehandelt wurde, beträgt die tatsächliche Fenstergröße 16.776.960 Bytes.

Die Tatsächliche Größe des Empfangsfensters und somit der Skalierungsfaktor wird durch den maximalen Empfangspufferspeicher bestimmt.
Dieser maximale Pufferspeicherplatz ist die Datenmenge, die ein TCP-Empfänger einem TCP-Absender ermöglicht, bevor er auf eine Bestätigung warten muss.
Nachdem die Verbindung hergestellt wurde, wird die Größe des Empfangsfensters in jedem TCP-Segment angekündigt (das Feld Fenster im TCP-Header).
Die Ankündigung der maximalen Datenmenge, die der Absender senden kann, ist ein empfängerseitiger Ablaufsteuerungsmechanismus, der verhindert, dass der Absender Daten sendet, die der Empfänger nicht speichern kann.
Ein sendende Host kann nur die maximale Datenmenge senden, die vom Empfänger angekündigt wird, bevor er auf eine Bestätigung und eine Aktualisierung der Größe des Empfangsfensters wartet.

Auf Windows Server 2003 und Windows XP verfügt der maximale Empfangspufferspeicherplatz, der die Größe des Empfangsfensters für den TCP/IP-Stapel darstellt, über einen Standardwert, der auf der Linkgeschwindigkeit der sendenden Schnittstelle basiert.
Der tatsächliche Wert wird automatisch an gerade Inkremente der maximalen Segmentgröße (MSS) angepasst, die beim Herstellen der TCP-Verbindung ausgehandelt wurde.
Bei einem Link mit 10 MBit/s wird die Standardgröße des Empfangsfensters normalerweise auf 16.000 Bytes festgelegt, während bei einem Link von 100 MBit/s die Standardgröße des Empfangsfensters auf 65.535 Bytes festgelegt wird.

Auf Windows Server 2003 und Windows XP kann die tatsächliche maximale Empfangsfenstergröße für den TCP/IP-Stapel manuell mithilfe der folgenden Registrierungswerte auf einer bestimmten Schnittstelle oder für das gesamte System konfiguriert werden:

`HKEY_LOCAL_MACHINE\SYSTEM\Current Control Set\Services\Tcpip\Parameters\TCPWindowSize`

`HKEY_LOCAL_MACHINE\SYSTEM\Current Control Set\Services\Tcpip\Parameters\Interface\TCPWindowSize`

Der Registrierungswert für **TCPWindowSize** kann auf maximal 65.535 Bytes festgelegt werden, wenn die WSopt-Erweiterung nicht verwendet wird, oder auf maximal 1.073.741.823 Bytes, wenn die WSopt-Erweiterung verwendet wird (ein maximaler Skalierungsfaktor von 4 wird unterstützt).
Ohne Fensterskalierung kann eine Anwendung auf einem Pfad mit einer Roundtripzeit von 100 Millisekunden (RTT) unabhängig von der Pfadbandbreite nur einen Durchsatz von etwa 5 Megabits pro Sekunde (MBit/s) erzielen.
Dieser Durchsatz kann mit der Fensterskalierung auf über ein Gigabit pro Sekunde (GBit/s) skaliert werden, wodurch TCP den Skalierungsfaktor für die Fenstergröße während der Verbindungseinrichtung aushandeln kann.

Auf Windows Server 2003 und Windows XP kann die WSopt-Erweiterung durch Festlegen des folgenden Registrierungswerts aktiviert werden.

`HKEY_LOCAL_MACHINE\SYSTEM\Current Control Set\Services\Tcpip\Parameters\Tcp1323Opts`

Der **Tcp1323Opts-Registrierungswert** ist ein **DWORD-codierter** Wert, sodass die TCP-WSopt-Erweiterung aktiviert ist, wenn Bit 0 festgelegt ist.
Wenn Bit 1 festgelegt ist, ist die in RFC 1323 definierte TCP-Zeitstempeloption (TSopt) aktiviert.
Der Wert 1 oder 3 aktiviert also die WSopt-Erweiterung.

Auf Windows Server 2003 und Windows XP werden standardmäßig die Registrierungswerte TCPWindowSize und Tcp1323Opts nicht erstellt.
Die Standardeinstellung ist also, dass die WSopt-Erweiterung deaktiviert ist und die TCP-Empfangsfenstergröße vom System auf einen maximalen Wert von bis zu 65.535 Bytes basierend auf der Linkgeschwindigkeit festgelegt wird.
Wenn die Fensterskalierung auf Windows Server 2003 und Windows XP durch Festlegen des Tcp1323Opts-Registrierungswerts aktiviert ist, wird die Fensterskalierung für eine TCP-Verbindung immer noch nur verwendet, wenn absender und empfänger eine TCP-Fensterskalierungsoption in das Synchronisierungssegment (SYN) einschließen, das zum Aushandeln eines Fensterskalierungsfaktors aneinander gesendet wird.
Wenn die Fensterskalierung für eine Verbindung verwendet wird, wird das Feld Fenster im TCP-Header auf 65.535 Bytes festgelegt, und der Fensterskalierungsfaktor wird verwendet, um die tatsächliche Empfangsfenstergröße um den Fensterskalierungsfaktor nach oben anzupassen, der beim Herstellen der Verbindung ausgehandelt wird.

Eine Anwendung kann die TCP-Empfangsfenstergröße für eine Verbindung mithilfe der **SO \_ RCVBUF-Socketoption** angeben.
Die TCP-Empfangsfenstergröße für einen Socket kann jederzeit mit **SO \_ RCVBUF** erhöht werden, kann jedoch nur vor dem Herstellen einer Verbindung verringert werden.
Um die Fensterskalierung zu verwenden, muss eine Anwendung eine Fenstergröße von mehr als 65.535 Bytes angeben, wenn die **SO \_ RCVBUF-Socketoption** verwendet wird, bevor die Verbindung hergestellt wird.

Der ideale Wert für die GRÖßE des TCP-Empfangsfensters ist häufig schwierig zu bestimmen.
Um die Kapazität des Netzwerks zwischen Sender und Empfänger zu füllen, sollte die Größe des Empfangsfensters auf das Produkt bandbreitenverzögerung für die Verbindung festgelegt werden. Dabei handelt es sich um die Bandbreite multipliziert mit der Roundtripzeit.
Auch wenn eine Anwendung das Produkt mit Bandbreitenverzögerung richtig bestimmen kann, ist immer noch nicht bekannt, wie schnell die empfangende Anwendung Daten aus dem eingehenden Datenpuffer abruft (die Abrufrate der Anwendung).
Trotz der Unterstützung der TCP-Fensterskalierung kann die maximale Größe des Empfangsfensters in Windows Server 2003 und Windows XP den Durchsatz weiterhin einschränken, da es sich um eine feste maximale Größe für alle TCP-Verbindungen handelt (sofern nicht pro Anwendung mit **SO \_ RCVBUF** angegeben), was den Durchsatz für einige Verbindungen erhöhen und den Durchsatz für andere verringern kann.
Darüber hinaus variiert die feste maximale Größe des Empfangsfensters für eine TCP-Verbindung nicht mit sich ändernden Netzwerkbedingungen.

Um das Problem der korrekten Bestimmung des Werts der maximalen Empfangsfenstergröße für eine TCP-Verbindung basierend auf den aktuellen Bedingungen des Netzwerks zu beheben, unterstützt der TCP/IP-Stapel in Windows Vista ein Feature zur automatischen Optimierung des Empfangsfensters.
Wenn dieses Feature aktiviert ist, bestimmt die automatische Optimierung des Empfangsfensters kontinuierlich die optimale Tatsächliche Empfangsfenstergröße, indem das Produkt mit Bandbreitenverzögerung und die Abrufrate der Anwendung gemessen werden, und die tatsächliche maximale Empfangsfenstergröße wird basierend auf sich ändernden Netzwerkbedingungen angepasst.
Die automatische Optimierung des Empfangsfensters aktiviert standardmäßig die TCP-WSopt-Erweiterung und ermöglicht bis zu 16.776.960 Bytes für die tatsächliche Fenstergröße.
Während die Daten über die Verbindung übertragen werden, überwacht der TCP/IP-Stapel die Verbindung, misst das aktuelle Produkt mit Bandbreitenverzögerung für die Verbindung und die Empfangsrate der Anwendung und passt die tatsächliche Größe des Empfangsfensters an, um den Durchsatz zu optimieren.
Der TCP/IP-Stapel ändert den Wert des Felds Fenster im TCP-Header basierend auf den Netzwerkbedingungen, da der WSopt-Skalierungsfaktor beim erstmaligen Herstellen der Verbindung festgelegt wird.

Der TCP/IP-Stapel in Windows Vista verwendet nicht mehr die **TCPWindowSize-Registrierungswerte.**
Bei besserem Durchsatz zwischen TCP-Peers steigt die Auslastung der Netzwerkbandbreite während der Datenübertragung.
Wenn alle Anwendungen für den Empfang von TCP-Daten optimiert sind, kann die Gesamtauslastung des Netzwerks erheblich zunehmen, wodurch die Verwendung von Quality of Service (QoS) für Netzwerke, die mit oder in der Nähe der Kapazität betrieben werden, wichtiger wird.

Das Standardverhalten auf Windows Vista für die Empfangspufferung, wenn **der SIO \_ SET COMPATIBILITY \_ \_ MODE** nicht mit **WsaBehaviorReceiveBuffering** angegeben wird, ist, dass keine Größenreduzierungen des Empfangsfensters mit der **SO \_ RCVBUF-Socketoption** zulässig sind, nachdem eine Verbindung hergestellt wurde.

Das Standardverhalten für Windows Vista für die automatische Optimierung, wenn **der SIO \_ SET COMPATIBILITY \_ \_ MODE** nicht mit **WsaBehaviorAutoTuning** angegeben wird, besteht darin, dass der Stapel die automatische Fensteroptimierung mit einem Fensterskalierungsfaktor von 8 empfängt.
Beachten Sie Folgendes: Wenn eine Anwendung eine gültige Empfangsfenstergröße mit der **SO \_ RCVBUF-Socketoption** festlegt, verwendet der Stapel die angegebene Größe, und die automatische Optimierung der Fensterebugging wird deaktiviert.
Windows automatische Optimierung kann auch mit dem folgenden Befehl vollständig deaktiviert werden. `netsh interface tcp set global autotuninglevel=disabled` In diesem Fall hat die Angabe von **WsaBehaviorAutoTuning** keine Auswirkungen.
Die automatische Optimierung von Fensterent empfängt auch basierend auf Gruppenrichtlinien, die auf Windows Server 2008 festgelegt sind, deaktiviert werden.

Die **WsaBehaviorAutoTuning-Option** ist auf Windows Vista für einige Internetgatewaygeräte und Firewalls erforderlich, die Datenflüsse für TCP-Verbindungen, die die WSopt-Erweiterung und einen Windows-Skalierungsfaktor verwenden, nicht ordnungsgemäß unterstützen.
Auf Windows Vista handelt ein Empfänger standardmäßig einen Fensterskalfaktor von 8 für eine maximale true-Fenstergröße von 16.776.960 Bytes aus.
Wenn der Datenfluss über einen schnellen Link beginnt, beginnt Windows zunächst mit einer 64 Kilobyte wahren Fenstergröße, indem das Feld Fenster des TCP-Headers auf 256 und der Fensterskalierungsfaktor in den TCP-Optionen auf 8 festgelegt wird (256*2^8=64 KB).
Einige Internetgatewaygeräte und Firewalls ignorieren den Fensterskalfaktor und sehen sich nur das angekündigte Fensterfeld im TCP-Header an, der als 256 angegeben ist, und löschen eingehende Pakete für die Verbindung, die mehr als 256 Bytes TCP-Daten enthalten.
Zur Unterstützung der TCP-Empfangsfensterskalierung muss ein Gatewaygerät oder eine Firewall den TCP-Handshake überwachen und den ausgehandelten Fensterskalierungsfaktor als Teil der TCP-Verbindungsdaten nachverfolgen.
Außerdem ignorieren einige Anwendungen und TCP-Stapelimplementierungen auf anderen Plattformen die TCP-WSopt-Erweiterung und den Faktor für die Fensterskalierung.
Daher kann der Remotehost, der die Daten sendet, Daten mit der rate senden, die im Feld Fenster des TCP-Headers angekündigt wird (256 Bytes).
Dies kann dazu führen, dass Daten sehr langsam vom Empfänger empfangen werden.

Wenn Sie den **BehaviorId-Member** auf **WsaBehaviorAutoTuning** und **TargetOsVersion** auf Windows Vista festlegen, wird der Fensterskalierungsfaktor auf 2 reduziert, sodass das Feld Fenster im TCP-Header anfänglich auf 16.384 Bytes und der Fensterskalierungsfaktor auf 2 für ein anfängliches true-Fenster mit einer Empfangsgröße von 64.000 Bytes festgelegt wird.
Die Funktion für die automatische Fensteroptimierung kann dann die Empfangsgröße des echten Fensters auf bis zu 262.140 Bytes erhöhen, indem das Feld Fenster im TCP-Header auf 65.535 Bytes festgelegt wird.
Eine Anwendung sollte **SIO \_ SET COMPATIBILITY \_ \_ MODE** IOCTL festlegen, sobald ein Socket erstellt wird, da diese Option nach dem Senden einer SYN nicht sinnvoll ist oder angewendet wird.
Das Festlegen dieser Option hat die gleichen Auswirkungen wie der folgende Befehl: `netsh interface tcp set global autotuninglevel=highlyrestricted`

Beachten Sie, dass die *Headerdatei Mswsockdef.h* automatisch in *Mswsock.h* oder *Netiodef.h* enthalten ist und nicht direkt verwendet werden sollte.

## <a name="see-also"></a>Weitere Informationen

[**Socket**](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)

[**WSAGetOverlappedResult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**WSASocketA**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**WSASocketW**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
