---
description: Navigations Thema für Windows Sockets (Winsock) Socket IOCTLs.
ms.assetid: 6a63c2c9-4e09-4a62-b39f-3ccb26287da8
title: Winsock IOCTLs (Winsock2.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de7094f802b815bfbd7511bd67eb4e6b1767cb94
ms.sourcegitcommit: 392c0a56f99f4d19686e734291abcac887fc5ba2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/22/2021
ms.locfileid: "106361096"
---
# <a name="winsock-ioctls"></a>Winsock IOCTLs

In diesem Abschnitt werden die Winsock-Socket-Eingabe-/ausgabesteuerelemente (IOCTLs) für verschiedene Editionen von Windows-Betriebssystemen beschrieben Verwenden Sie die Funktion [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) oder [**wspioctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) , um eine Winsock ioctl zum Steuern des Modus eines Sockets, des Transport Protokolls oder des Kommunikations Subsystems auszustellen.

Einige Winsock IOCTLs erfordern eine ausführlichere Erläuterung, als diese Tabelle vermitteln kann. Diese Optionen enthalten Links zu weiteren Themen.

Es ist möglich, ein Codierungsschema zu übernehmen, das die aktuell definierten [**ioctlsocket**](/windows/desktop/api/winsock/nf-winsock-ioctlsocket) -Opcodes beibehält, während es eine bequeme Möglichkeit bietet, den Opcode-bezeichnerbereich in zu partitionieren, bis der *dwIoControlCode* -Parameter nun eine 32-Bit-Entität ist. Der *dwIoControlCode* -Parameter wird erstellt, um die Protokoll-und Herstellerunabhängigkeit beim Hinzufügen neuer Steuerungs Codes zu ermöglichen und gleichzeitig die Abwärtskompatibilität mit den Windows Sockets 1,1-und UNIX-Steuerungs Codes beizubehalten. Der *dwIoControlCode* -Parameter weist das folgende Format auf.

| I  | O  | V  | T  | Hersteller/Adressfamilie | Code                   |
|-|-|-|-|-|-|
| 3  | 3  | 2  | 2 2 | 2 2 2 2 2 2 2 1 1 1 1 | 1 1 1 1 1 1              |
| 1  | 0  | 9  | 8 7 | 6 5 4 3 2 1 0 9 8 7 6 | 5 4 3 2 1 0 9 8 7 6 5 4 3 2 1 0 |

> [!Note] 
> Die in der Tabelle angezeigten Bits im *dwIoControlCode* -Parameter müssen vertikal von oben nach unten nach Spalte gelesen werden. Das linke Bit ist also Bit 31, das nächste Bit ist Bit 30, und das ganz rechts ist Bit 0.

Ich bin festgelegt, wenn der Eingabepuffer für den Code gültig ist, wie **IOC_IN**.

O wird festgelegt, wenn der Ausgabepuffer für den Code gültig ist, wie **IOC_OUT**. Steuerungs Codes mit Eingabe-und Ausgabe Puffern legen sowohl I als auch O fest.

V wird festgelegt, wenn keine Parameter für den Code vorhanden sind, wie **IOC_VOID**.

T ist eine 2-Bit-Menge, die den Typ der IOCTL definiert. Die folgenden Werte sind definiert:

0: ioctl ist ein standardmäßiger **UNIX-** IOCTL **-Code**.

1 ioctl ist ein generischer Windows Sockets 2 ioctl-Code. Neue ioctl-Codes, die für Windows Sockets 2 definiert werden, haben T = = 1.

2 die IOCTL gilt nur für eine bestimmte Adressfamilie.

3 die IOCTL gilt nur für den Anbieter eines bestimmten Anbieters, wie z. b. **IOC_VENDOR**. Dieser Typ ermöglicht es Unternehmen, eine Anbieter Nummer zuzuweisen, die im **Anbieter-/Adress-Familien-Parameter** angezeigt wird. Anschließend kann der Anbieter für den Anbieter ein spezielles IOCTLs-Element definieren, ohne die IOCTL bei einem Clearinghouse registrieren zu müssen, wodurch die Flexibilität und der Datenschutz des Anbieters gewährleistet werden.

**Hersteller/Adressfamilie** Eine 11-Bit-Menge, die den Hersteller definiert, der den Code besitzt (if t = = 3) oder der die Adressfamilie enthält, auf die der Code angewendet wird (wenn t = = 2). Handelt es sich hierbei um einen UNIX-ioctl-Code (T = = 0), hat dieser Parameter denselben Wert wie der Code auf UNIX. Wenn es sich um eine generische Windows Sockets 2 ioctl (T = = 1) handelt, kann dieser Parameter als Erweiterung des Code-Parameters verwendet werden, um zusätzliche Codewerte bereitzustellen.

**Code** Die 16-Bit-Menge, die den spezifischen ioctl-Code für den Vorgang enthält.

## <a name="unix-ioctl-codes"></a>UNIX-ioctl-Codes

Die folgenden UNIX-ioctl-Codes (Befehle) werden unterstützt.

### <a name="fionbio"></a>FIONBIO

Aktiviert oder deaktiviert den nicht blockierenden Modus für Socket *s*. Der *lpvinbuffer* -Parameter verweist auf einen **Ganzzahl ohne Vorzeichen long** -Wert (QoS), der ungleich 0 (null) ist, wenn der nicht blockierende Modus aktiviert werden soll, und 0 (null), wenn er deaktiviert werden soll. Wenn ein Socket erstellt wird, wird er im Blockierungs Modus ausgeführt (d. h., der nicht blockierende Modus ist deaktiviert). Dies entspricht den BSD-Sockets.

Die Routine [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) oder [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) legt einen Socket automatisch auf den nicht blockierenden Modus fest. Wenn " **WSAAsyncSelect** " oder " **WSAEventSelect** " für einen Socket ausgegeben wurde, schlägt jeder Versuch der Verwendung von [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) zum Zurücksetzen des Sockets auf den Blockierungs Modus mit WSAEINVAL fehl. Damit der Socket wieder in den Blockierungs Modus wechselt, muss eine Anwendung  zuerst WSAAsyncSelect durch Aufrufen von **WSAAsyncSelect** mit dem Parameter " *Levent* " gleich 0 (null) deaktivieren oder **WSAEventSelect** deaktivieren, indem **WSAEventSelect** mit dem Parameter " *lnetworkevents* " gleich 0 (null) aufgerufen wird.

### <a name="fionread"></a>FIONREAD

Bestimmen Sie die Datenmenge, die atomarisch *aus Sockets gelesen* werden kann. Der *lpvoutbuffer* -Parameter verweist auf einen **Ganzzahl ohne Vorzeichen long** -Wert, in dem [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) das Ergebnis speichert.

Wenn der im *s* -Parameter übergebene Socket Datenstrom orientiert ist (z. b. "Sock- \_ Stream"), gibt " **atonread** " die Gesamtmenge der Daten zurück, die in einem einzelnen Empfangsvorgang gelesen werden können. Dies ist normalerweise identisch mit der Gesamtmenge der Daten, die im Socket in die Warteschlange eingereiht werden (da ein Datenstrom Byte orientiert ist)

Wenn der im *s* -Parameter übergebene Socket Nachrichten orientiert ist (z. b. der Typ "Sock \_ dgram"), gibt " **fonread** " die Gesamtzahl der zu lesenden Bytes zurück, nicht die Größe des ersten Datagramms (Nachricht), das im Socket in die Warteschlange eingereiht wurde.

### <a name="siocatmark"></a>Siocatmark

Bestimmen Sie, ob alle OOB-Daten gelesen wurden. Dies gilt nur für einen Socket des streamstils (z. b. den Typ "Sock- \_ Stream"), der für den Inline Empfang beliebiger OOB-Daten (also \_ oobinline) konfiguriert wurde. Wenn keine OOB-Daten darauf warten, gelesen zu werden, gibt der Vorgang true zurück. Andernfalls wird **false** zurückgegeben, und der nächste Empfangsvorgang, der für den Socket ausgeführt wird, ruft einige oder alle Daten ab, die der Markierung vorangestellt sind. die Anwendung sollte den **siocatmark** -Vorgang verwenden, um zu bestimmen, ob eine vorhanden ist. Wenn die Daten mit den dringenden Daten (Out-of-Band-Daten) vorangestellt sind, werden Sie in der richtigen Reihenfolge empfangen. (Beachten Sie, dass [**empfangener**](/windows/desktop/api/winsock/nf-winsock-recv) -Vorgänge niemals OOB-und normale Daten im selben-aufrufmix kombinieren.) *lpvoutbuffer* verweist auf einen booleschen Wert, in dem das Ergebnis von [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) gespeichert wird.

## <a name="windows-sockets-2-commands"></a>Windows Sockets 2-Befehle

Die folgenden Windows Sockets 2-Befehle werden unterstützt.

### <a name="sio_acquire_port_reservation-opcode-setting-i-t3"></a>SIO_ACQUIRE_PORT_RESERVATION (OpCode-Einstellung: I, T = = 3)

Anfordern einer Lauf Zeit Reservierung für einen Block von TCP-oder UDP-Ports. Bei Lauf Zeit Port Reservierungen erfordert der Port Pool, dass Reservierungen von dem Prozess verarbeitet werden, dessen Socket die Reservierung gewährt wurde. Lauf Zeit Port Reservierungen dauern nur so lange, wie die Lebensdauer des Sockets, auf dem die IOCTL-ioctl-Reservierung für den Zertifikat Abruf [**\_ \_ \_ reserviert**](/previous-versions/windows/desktop/legacy/gg699720(v=vs.85)) wurde. Im Gegensatz dazu können persistente Port Reservierungen, die mithilfe der Funktion " [**kreatepersistenttcpportreservation**](/windows/win32/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation) " oder " [**kreatepersistentudpportreservation**](/windows/win32/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation) " erstellt wurden, von jedem Prozess genutzt werden, der über die Möglichkeit zum Abrufen dauerhafter Reservierungen verfügt.

Ausführlichere Informationen finden Sie in der Referenz zur Übersicht über den SIO-Abruf [**\_ \_ Port \_**](/previous-versions/windows/desktop/legacy/gg699720(v=vs.85)) .

[**SIO \_ Das Abrufen von \_ Port \_ Reservierungen**](/previous-versions/windows/desktop/legacy/gg699720(v=vs.85)) wird unter Windows Vista und höheren Versionen des Betriebssystems unterstützt.

### <a name="sio_address_list_change-opcode-setting-v-t1"></a>Änderung der "sio- \_ Adress \_ Liste" \_ (OpCode-Einstellung: V, T = = 1)

, Um Benachrichtigungen über Änderungen in der Liste der lokalen Transport Adressen der Protokollfamilie des Sockets zu erhalten, an die die Anwendung gebunden werden kann. Nach Abschluss dieser ioctl werden keine Ausgabeinformationen bereitgestellt. die Vervollständigung gibt lediglich an, dass die Liste der verfügbaren lokalen Adressen geändert wurde, und sollte erneut durch die **\_ \_ \_ Abfrage** der vollständig abgefragten Adresse abgefragt werden.

Es wird angenommen (obwohl nicht erforderlich), dass die Anwendung überlappende e/a-Vorgänge verwendet, um über Änderungen durch den Abschluss der Anforderungen an die Übersicht über die **SIO- \_ Adress \_ Liste \_** benachrichtigt zu werden. Wenn die Übersicht über die Übersicht über die die **\_ \_ Liste \_** der zu überlappenden Datenbanken in einem nicht blockierenden Socket und ohne überlappende Parameter (*lpoverllapp* /  *lpCompletionRoutine* auf **null**) ausgegeben wird, wird der Vorgang sofort mit dem Fehler " [WSAEWOULDBLOCK](windows-sockets-error-codes-2.md)" abgeschlossen. Die Anwendung kann dann über einen [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) -oder [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) -Vorgang, der \_ \_ \_ in der Netzwerk Ereignis-Bitmaske festgelegt ist, auf Änderungs Ereignisse für die Adressliste warten.

### <a name="sio_address_list_query-opcode-setting-o-t1"></a>Abfrage für die SIO- \_ Adress \_ Liste \_ (OpCode-Einstellung: O, T = = 1)

Ruft eine Liste der lokalen Transport Adressen der Protokollfamilie des Sockets ab, an die die Anwendung gebunden werden kann. Die Liste der Adressen variiert je nach Adressfamilie, und einige Adressen werden aus der Liste ausgeschlossen.

> [!Note] 
> In Windows-Plug-and-Play-Umgebungen können Adressen dynamisch hinzugefügt und entfernt werden. Daher können Anwendungen nicht darauf basieren, dass die von der-Abfrage der- **\_ \_ \_ Abfrage Liste** zurückgegebenen Informationen persistent sind. Anwendungen können sich für Adress Änderungs Benachrichtigungen über die Übersicht über die Übersicht über die Übersicht über die Übersicht über die IOCTL-Adress **\_ \_ Liste \_** registrieren, die eine Benachrichtigung über das überlappende e/a oder das \_ \_ \_ Änderungs Ereignis für die Die folgende Sequenz von Aktionen kann verwendet werden, um sicherzustellen, dass die Anwendung immer über aktuelle Adresslisten Informationen verfügt:

-  Problem bei der " **SIO- \_ Adress \_ Liste \_** " ioctl
-  Problem-Prozessor- **\_ Adress \_ Liste \_ Abfrage** ioctl
-  Immer wenn die IOCTL-Änderung der " **SIO- \_ Adress \_ \_ Liste** " die Anwendung über eine überlappende e/a-Änderung oder durch Signalisieren eines FD- \_ Adresslisten- \_ \_ Änderungs Ereignisses benachrichtigt, sollte die gesamte Sequenz von Aktionen wiederholt werden.

Ausführlichere Informationen finden Sie [**in der Übersicht \_ \_ \_**](/previous-versions/windows/desktop/legacy/dd877219(v=vs.85)) über die Übersicht über die Übersicht über die Übersicht. **SIO \_ Die Adress \_ Listen \_ Abfrage** wird unter Windows 2000 und höher unterstützt.

### <a name="sio_apply_transport_setting-opcode-setting-i-t3"></a>\_Transport Einstellung für "sio anwenden" \_ \_ (OpCode-Einstellung: I, T = = 3)

Wendet eine Transport Einstellung auf einen Socket an. Die angewendete Transport Einstellung basiert auf der [**Transport \_ Einstellungs- \_ ID**](/windows/win32/api/transportsettingcommon/ns-transportsettingcommon-transport_setting_id) , die im *lpvinbuffer* -Parameter übergeben wird.

Die einzige Transport Einstellung, die derzeit definiert, ist die Funktion für die **echt \_ Zeit \_ Benachrichtigungs \_ Funktion** in einem TCP-Socket.

Wenn für die übergebene [**Transport \_ Einstellungs- \_ ID**](/windows/win32/api/transportsettingcommon/ns-transportsettingcommon-transport_setting_id) das **GUID** -Element auf **echt \_ Zeit \_ Benachrichtigungs \_ Funktion** festgelegt ist, ist dies eine Anforderung zum Anwenden von Echt Zeit Benachrichtigungseinstellungen für den TCP-Socket, der mit dem [**controlchannel-**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) Vorgang zum Empfangen von Hintergrund Netzwerk Benachrichtigungen in einer Windows Store-App verwendet wird

Ausführlichere Informationen finden Sie in der Referenz zur Referenz [**\_ \_ Transport \_ Einstellung**](/previous-versions/windows/desktop/legacy/jj553481(v=vs.85)) für "sio". **SIO \_ Die \_ \_ Einstellung Transport anwenden** wird unter Windows 8, Windows Server 2012 und höher unterstützt.

### <a name="sio_associate_handle-opcode-setting-i-t1"></a>SIO-Zuordnungs \_ \_ handle (OpCode-Einstellung: I, T = = 1)

Ordnet diesen Socket dem angegebenen Handle einer Begleitschnittstelle zu. Der Eingabepuffer enthält den ganzzahligen Wert, der der Manifest-Konstante der Begleit Schnittstelle entspricht (z. b. th \_ netdev und Th \_ TAPI), gefolgt von einem Wert, der ein Handle der angegebenen Begleit Schnittstelle ist, zusammen mit allen anderen erforderlichen Informationen. Ausführliche Informationen zu einer bestimmten Begleit Schnittstelle finden Sie im entsprechenden Abschnitt in [Winsock-Anlagen](winsock-annexes.md) . Die Gesamtgröße wird in der Länge des Eingabe Puffers widergespiegelt. Es ist kein Ausgabepuffer erforderlich. Der [wsaenoprodeopt](windows-sockets-error-codes-2.md) -Fehlercode wird für Dienstanbieter angezeigt, die diese IOCTL nicht unterstützen. Das Handle, das dieser ioctl zugeordnet ist, kann mit dem **SIO- \_ Übersetzungs \_ handle** abgerufen werden.

Eine Begleit Schnittstelle kann z. b. verwendet werden, wenn ein bestimmter Anbieter (1) viele zusätzliche Steuerelemente für das Verhalten eines Sockets bereitstellt und (2) die Steuerelemente Anbieter spezifisch sind, sodass Sie nicht vorhandenen Windows-Socketfunktionen zugeordnet werden, oder solche, die wahrscheinlich in Zukunft definiert werden. Es wird empfohlen, dass die Component Object Model (com) anstelle dieser IOCTL verwendet werden, um andere Schnittstellen zu ermitteln und zu verfolgen, die möglicherweise von einem Socket unterstützt werden. Diese IOCTL ist für die (umgekehrte) Kompatibilität mit Systemen vorhanden, in denen com nicht verfügbar ist oder aus einem anderen Grund nicht verwendet werden kann.

### <a name="sio_associate_port_reservation-opcode-setting-i-t3"></a>Port Reservierung für "sio \_ zuordnen" \_ \_ (OpCode-Einstellung: I, T = = 3)

Ordnen Sie einen Socket einer permanenten oder Lauf Zeit Reservierung für einen Block von TCP-oder UDP-Ports zu, der durch das Port Reservierungs Token identifiziert wird. Vor dem Binden des Sockets muss die IOCTL-ioctl für die Zuweisung des [**\_ \_ Ports \_**](/previous-versions/windows/desktop/legacy/gg699721(v=vs.85)) zugewiesen werden. Wenn und wenn der Socket gebunden ist, wird der zugewiesene Port aus der durch das angegebene Token identifizierten Port Reservierung ausgewählt. Wenn keine Ports aus der angegebenen Reservierung verfügbar sind, schlägt der [**Bind**](/windows/desktop/api/winsock/nf-winsock-bind) -Funktionsaufrufe fehl.

Ausführlichere Informationen finden Sie in der Übersicht über die [**\_ Port- \_ \_ Reservierungs**](/previous-versions/windows/desktop/legacy/gg699721(v=vs.85)) Referenz für den Port.

[**SIO \_ Zuordnen der \_ Port \_ Reservierung**](/previous-versions/windows/desktop/legacy/gg699721(v=vs.85)) wird unter Windows Vista und höheren Versionen des Betriebssystems unterstützt.

### <a name="sio_base_handle-opcode-setting-o-t1"></a>Base64- \_ Basis \_ handle (OpCode-Einstellung: O, T = = 1)

Ruft das Basis Dienstanbieter Handle für einen angegebenen Socket ab. Der zurückgegebene Wert ist ein **Socket**.

Ein mehrstufiger Dienstanbieter würde diese IOCTL nie abfangen, da der Rückgabewert das Sockethandle des Basis Dienstanbieters sein muss.

Wenn der Ausgabepuffer für ein Sockethandle nicht groß genug ist (der *cboutbuffer* ist kleiner als die Größe eines **Sockets**) oder der *lpvoutbuffer* -Parameter ein **null** -Zeiger ist, wird der **\_ Socketfehler** als Ergebnis dieser ioctl zurückgegeben, und [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) gibt [wsaefault](windows-sockets-error-codes-2.md)zurück.

**SIO \_ Das Basis \_ handle** ist in der Header Datei " *mswap. h* " definiert und wird unter Windows Vista und höher unterstützt.

### <a name="sio_bsp_handle-opcode-setting-o-t1"></a>SIO- \_ BSP- \_ handle (OpCode-Einstellung: O, T = = 1)

Ruft das Basis Dienstanbieter Handle für einen von der [**wsasendmsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) -Funktion verwendeten Socket ab. Der zurückgegebene Wert ist ein **Socket**.

Diese IOCTL wird von einem geschichteten Dienstanbieter verwendet, um sicherzustellen, dass der Anbieter die [**wsasendmsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) -Funktion abfängt.

Wenn der Ausgabepuffer für ein Sockethandle nicht groß genug ist (der *cboutbuffer* ist kleiner als die Größe eines **Sockets**) oder der *lpvoutbuffer* -Parameter ein **null** -Zeiger ist, wird der **\_ Socketfehler** als Ergebnis dieser ioctl zurückgegeben, und [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) gibt [wsaefault](windows-sockets-error-codes-2.md)zurück.

**SIO \_ Der BSP- \_ handle** ist in der Header Datei " *mswap. h* " definiert und wird unter Windows Vista und höher unterstützt.

### <a name="sio_bsp_handle_select-opcode-setting-o-t1"></a>Auswahl für "sio- \_ BSP- \_ handle" \_ (OpCode-Einstellung: O, T = = 1)

Ruft das Basis Dienstanbieter Handle für einen von der [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) -Funktion verwendeten Socket ab. Der zurückgegebene Wert ist ein **Socket**.

Diese IOCTL wird von einem geschichteten Dienstanbieter verwendet, um sicherzustellen, dass der Anbieter die [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) -Funktion abfängt.

Wenn der Ausgabepuffer für ein Sockethandle nicht groß genug ist (der *cboutbuffer* ist kleiner als die Größe eines **Sockets**) oder der *lpvoutbuffer* -Parameter ein **null** -Zeiger ist, wird der **\_ Socketfehler** als Ergebnis dieser ioctl zurückgegeben, und [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) gibt [wsaefault](windows-sockets-error-codes-2.md)zurück.

**SIO \_ \_ \_ Select** ist in der Header Datei " *mswap. h* " definiert und wird unter Windows Vista und höher unterstützt.

### <a name="sio_bsp_handle_poll-opcode-setting-o-t1"></a>Leistungs Abfrage für das sio- \_ BSP- \_ handle \_ (OpCode-Einstellung: O, T = = 1)

Ruft das Basis Dienstanbieter Handle für einen von der [**wsapoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) -Funktion verwendeten Socket ab. Der *lpoverllapp* -Parameter muss ein **null** -Zeiger sein. Der zurückgegebene Wert ist ein **Socket**.

Diese IOCTL wird von einem geschichteten Dienstanbieter verwendet, um sicherzustellen, dass der Anbieter die [**wsapoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) -Funktion abfängt.

Wenn der Ausgabepuffer für ein Sockethandle nicht groß genug ist (der *cboutbuffer* ist kleiner als die Größe eines **Sockets**), ist der *lpvoutbuffer* -Parameter ein **null** -Zeiger, oder der *lpoverllapp* -Parameter ist kein **null** -Zeiger. der **\_ Socketfehler** wird als Ergebnis dieser ioctl zurückgegeben, und [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) gibt [wsaef](windows-sockets-error-codes-2.md)

**SIO \_ Der BSP- \_ handle \_** -Abruf ist in der Header Datei " *mswap. h* " definiert und wird unter Windows Vista und höher unterstützt.

### <a name="sio_chk_qos-opcode-setting-i-o-t3"></a>\_K- \_ QoS-QoS (OpCode-Einstellung: I, O, T = = 3)

Ruft Informationen zu QoS-Datenverkehrs Merkmalen ab. Während der Übergangsphase des Sende Systems zwischen der Flow-Einrichtung und dem Empfang einer RESV-Nachricht (Weitere Informationen zur Übergangsphase finden Sie [unter wie der RSVP-Dienst TC](/previous-versions/windows/desktop/qos/how-the-rsvp-service-invokes-tc) aufruft), wird der Datenverkehr, der einem RSVP-Flow zugeordnet ist, basierend auf dem Diensttyp ([bewährter Aufwand](/previous-versions/windows/desktop/qos/best-effort), [kontrollierte Auslastung](/previous-versions/windows/desktop/qos/controlled-load)oder [garantiert](/previous-versions/windows/desktop/qos/guaranteed)) strukturiert. Weitere Informationen finden Sie im Abschnitt [Quality of Service](/previous-versions/windows/desktop/qos/qos-start-page) des Platform SDK unter [Verwenden von SIO- \_ chk- \_ QoS](/previous-versions/windows/desktop/qos/using-sio-chk-qos) .

### <a name="sio_cpu_affinity-opcode-setting-i-t3"></a>SIO_CPU_AFFINITY (OpCode-Einstellung: I, T = = 3)

Aktiviert die Port Freigabe und die Parallelisierung der Empfangs Anzeige. Wenn die Anwendung diese Socketoption verwendet, um Sockets verschiedenen Prozessoren zuzuordnen, und dann die Sockets an dieselbe Adresse bindet, werden Empfangs Hinweise auf die Sockets basierend auf dem Empfangs seitigen Skalierungs Hash (RSS) verteilt. Die RSS-Einstellungen ändern sich nicht, sodass ein beliebiger Flow (lokaler Endpunkt, Remote Endpunkt Paar) immer auf demselben Prozessor angegeben wird. Folglich werden alle Pakete, die zu einem bestimmten Flow gehören, dem gleichen Socket angezeigt. Diese IOCTL muss vor der Bindung aufgerufen werden, andernfalls wird wsabinval zurückgegeben. Der Eingabepuffer ist ein Prozessor Index (0-basiert) vom Typ ushort. Ioctl ist mit SO_REUSEADDR und SO_REUSE_MULTICASTPORT nicht kompatibel. Wird nur für UDP-Sockets unterstützt.

> [!NOTE]
> Wenn Sie auf Version 10.0.19041.0 (Windows 10, Version 2004) des Windows SDK abzielen, verwenden Sie den Wert `0x98000015` anstelle des namens **SIO_CPU_AFFINITY**.

### <a name="sio_enable_circular_queueing-opcode-setting-v-t1"></a>SIO \_ Aktivieren von \_ zirkulären \_ Warteschlangen (OpCode-Einstellung: V, T = = 1)

Gibt dem zugrunde liegenden Nachrichten orientierten Dienstanbieter an, dass eine neu empfangene Nachricht nicht gelöscht werden soll, weil ein Puffer Warteschlangen Überlauf besteht. Stattdessen sollte die älteste Nachricht in der Warteschlange entfernt werden, damit Sie der neu eingegangenen Nachricht gerecht wird. Es sind keine Eingabe-und Ausgabepuffer erforderlich. Beachten Sie, dass diese IOCTL nur für Sockets gültig ist, die mit unzuverlässigen, Nachrichten orientierten Protokollen verknüpft sind. Der [wsaenoprodeopt](windows-sockets-error-codes-2.md) -Fehlercode wird für Dienstanbieter angezeigt, die diese IOCTL nicht unterstützen.

### <a name="sio_find_route-opcode-setting-o-t1"></a>SIO \_ - \_ Route suchen (OpCode-Einstellung: O, T = = 1)

Bei der Ausgabe fordert diese IOCTL an, dass die Route zur Remote Adresse, die als [**sockaddr**](sockaddr-2.md) im Eingabepuffer angegeben ist, ermittelt werden kann. Wenn die Adresse bereits im lokalen Cache vorhanden ist, wird der zugehörige Eintrag ungültig. Im Fall von Novell es IPX initiiert dieser Rückruf ein IPX getlocaltarget (GLT), das das Netzwerk nach der angegebenen Remote Adresse abfragt.

### <a name="sio_flush-opcode-setting-v-t1"></a>SIO \_ Flush (OpCode-Einstellung: V, T = = 1)

Verwirft den aktuellen Inhalt der Sende Warteschlange, die diesem Socket zugeordnet ist. Es sind keine Eingabe-und Ausgabepuffer erforderlich. Der [wsaenoprodeopt](windows-sockets-error-codes-2.md) -Fehlercode wird für Dienstanbieter angezeigt, die diese IOCTL nicht unterstützen.

### <a name="sio_get_broadcast_address-opcode-setting-o-t1"></a>"Sio \_ get \_ Broadcast Address" \_ (OpCode-Einstellung: O, T = = 1)

Diese IOCTL füllt den Ausgabepuffer mit einer [sockaddr](sockaddr-2.md) -Struktur aus, die eine passende Broadcast Adresse für die Verwendung mit [**SendTo**](/windows/desktop/api/winsock/nf-winsock-sendto) /  [**WSASendTo**](/windows/desktop/api/Winsock2/nf-winsock2-wsasendto)enthält. Diese IOCTL wird für IPv6-Sockets nicht unterstützt und gibt den [wsaenoprodeopt](windows-sockets-error-codes-2.md) -Fehlercode zurück.

### <a name="sio_get_extension_function_pointer-opcode-setting-o-i-t1"></a>Funktionszeiger für die Erweiterung von "sio \_ Get" \_ \_ \_ (OpCode-Einstellung: O, I, T = = 1)

Ruft einen Zeiger auf die angegebene Erweiterungs Funktion ab, die vom zugeordneten Dienstanbieter unterstützt wird. Der Eingabepuffer enthält einen Globally Unique Identifier (**GUID**), dessen Wert die betreffende Erweiterungs Funktion angibt. Der Zeiger auf die gewünschte Funktion wird im Ausgabepuffer zurückgegeben. Erweiterungs Funktions Bezeichner werden von Dienstanbieter Herstellern eingerichtet und sollten in der Herstellerdokumentation enthalten sein, in der die Funktionen und die Semantik der Erweiterungsfunktionen beschrieben werden.

Die GUID-Werte für Erweiterungsfunktionen, die vom Windows-TCP/IP-Dienstanbieter unterstützt werden, sind in der Header Datei " *mswap. h* " definiert. Der mögliche Wert für diese GUIDs lautet wie folgt:

| Begriff                                                                                                                | BESCHREIBUNG                                                                               |
|-|-|
| <span id="WSAID_ACCEPTEX"></span><span id="wsaid_acceptex"></span>wsaid- \_ Akzeptanz<br/>                                     | Die-Anordnungs Funktion für die [**Annahme**](/windows/win32/api/mswsock/nf-mswsock-acceptex) .<br/>                         |
| <span id="WSAID_CONNECTEX"></span><span id="wsaid_connectex"></span>wsaid- \_ connectex<br/>                                  | Die [**connectex**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex) -Erweiterungs Funktion. <br/>                      |
| <span id="WSAID_DISCONNECTEX"></span><span id="wsaid_disconnectex"></span>wsaid- \_ disconnectex<br/>                         | Die [**disconnectex**](/previous-versions/windows/desktop/legacy/ms737757(v=vs.85)) -Erweiterungs Funktion. <br/>                |
| <span id="WSAID_GETACCEPTEXSOCKADDRS"></span><span id="wsaid_getacceptexsockaddrs"></span>wsaid \_ getaccept texsockaddrs<br/> | Die [**getaccept texsockaddrs**](/windows/win32/api/mswsock/nf-mswsock-getacceptexsockaddrs) -Erweiterungs Funktion.<br/> |
| <span id="WSAID_TRANSMITFILE"></span><span id="wsaid_transmitfile"></span>wsaid \_ TransmitFile<br/>                         | Die [**TransmitFile**](/windows/win32/api/mswsock/nf-mswsock-transmitfile) -Erweiterungs Funktion.<br/>                 |
| <span id="WSAID_TRANSMITPACKETS"></span><span id="wsaid_transmitpackets"></span>wsaid \_ transmitpakete<br/>                | Die [**transmitpaketen**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_transmitpackets) -Erweiterungs Funktion. <br/>          |
| <span id="WSAID_WSARECVMSG"></span><span id="wsaid_wsarecvmsg"></span>wsaid \_ wsarecvmsg<br/>                               | Die [**LPFN_WSARECVMSG (wsarecvmsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) -Erweiterungs Funktion.<br/>                     |
| <span id="WSAID_WSASENDMSG"></span><span id="wsaid_wsasendmsg"></span>wsaid \_ wsasendmsg<br/>                               | Die [**wsasendmsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) -Erweiterungs Funktion. <br/>                      |

### <a name="sio_get_group_qos-opcode-setting-o-i-t1"></a>QoS für die SIO- \_ get- \_ Gruppe \_ (OpCode-Einstellung: O, I, T = = 1)

Reserviert für die zukünftige Verwendung mit Sockets.

Rufen Sie die [**QoS**](/windows/win32/api/winsock2/ns-winsock2-qos) -Struktur ab, die der Socketgruppe zugeordnet ist, zu der dieser Socket gehört. Der Eingabepuffer ist optional. Einige Protokolle (z. b. RSVP) ermöglichen es, den Eingabepuffer zum qualifizieren der Qualität von Service Request zu verwenden. Die **QoS** -Struktur wird in den Ausgabepuffer kopiert. Wenn dieser Socket nicht zu einer geeigneten Socketgruppe gehört, werden die Elemente **sendingflowspec** und **receivingflowspec** der zurückgegebenen **QoS** -Struktur auf **null** festgelegt. Der [wsaenoprodeopt](windows-sockets-error-codes-2.md) -Fehlercode wird für Dienstanbieter angezeigt, die keine Quality of Service-Unterstützung bieten.

### <a name="sio_get_interface_list-opcode-setting-o-t0"></a>Liste der "sio \_ get \_ Interface" \_ (OpCode-Einstellung: O, T = = 0)

Gibt eine Liste konfigurierter IP-Schnittstellen und ihrer Parameter als Array von [**Schnittstellen \_ Informations**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-interface_info) Strukturen zurück.

> [!Note]  
> Die Unterstützung dieses Befehls ist für Windows Sockets 2-kompatible TCP/IP-Dienstanbieter obligatorisch.

Der *lpvoutbuffer* -Parameter verweist auf den Puffer, in dem die Informationen über Schnittstellen als [**Array von Schnittstellen \_ Informationsstrukturen**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-interface_info) für Unicast-IP-Adressen in den Schnittstellen gespeichert werden sollen. Der *cboutbuffer* -Parameter gibt die Länge des Ausgabepuffers an. Die Anzahl der zurückgegebenen Schnittstellen (die Anzahl der im Puffer zurückgegebenen Strukturen, auf die der *lpvoutbuffer* -Parameter verweist) kann basierend auf der tatsächlichen Länge des Ausgabepuffers bestimmt werden, der im *lpcbbytesall* -Parameter zurückgegeben wurde.

Wenn die [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) -Funktion mit der " **SIO \_ get \_ Interface \_ List** " aufgerufen wird und der ebenenmember des Sockets-Parameters nicht als **ipproto \_ IP** definiert ist, wird **wsaabval** zurückgegeben.  Ein Aufrufen der **WSAIoctl** -Funktion mit der " **SIO \_ get \_ Interface \_ List** " gibt " **wsaefault** " zurück, wenn der *cboutbuffer* -Parameter, der die Länge des Ausgabepuffers angibt, die Liste der konfigurierten Schnittstellen empfängt.

**SIO \_ Die \_ \_ Liste "Get Interface** " wird unter Windows Me/98 und Windows NT 4,0 mit SP4 und höher unterstützt.

### <a name="sio_get_interface_list_ex-opcode-setting-o-t0"></a>Liste der "sio \_ get \_ Interface \_ List \_ Ex" (OpCode Setting: O, T = = 0)

Reserviert für die zukünftige Verwendung mit Sockets.

Gibt eine Liste der konfigurierten IP-Schnittstellen und ihrer Parameter als Array von [**Schnittstellen \_ Info- \_ Ex**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-interface_info_ex) -Strukturen zurück.

Der *lpvoutbuffer* -Parameter verweist auf den Puffer, in dem die Informationen über Schnittstellen als Array von [**Schnittstellen \_ Info \_**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-interface_info_ex) --Strukturen für Unicast-IP-Adressen in der Schnittstelle gespeichert werden sollen. Der *cboutbuffer* -Parameter gibt die Länge des Ausgabepuffers an. Die Anzahl der zurückgegebenen Schnittstellen (Anzahl der in *lpvoutbuffer* zurückgegebenen Strukturen) kann basierend auf der tatsächlichen Länge des Ausgabepuffers bestimmt werden, der im Parameter " *lpcbbytesgab* " zurückgegeben wird.

**SIO \_ "Get \_ Interface \_ List \_ Ex** " wird unter Windows derzeit nicht unterstützt.

### <a name="sio_get_qos-opcode-setting-o-t1"></a>QoS für "sio \_ Get" \_ (OpCode-Einstellung: O, T = = 1)

Reserviert für die zukünftige Verwendung mit Sockets. Rufen Sie die [**QoS**](/windows/win32/api/winsock2/ns-winsock2-qos) -Struktur ab, die dem Socket zugeordnet ist. Der Eingabepuffer ist optional. Einige Protokolle (z. b. RSVP) ermöglichen es, den Eingabepuffer zum qualifizieren der Qualität von Service Request zu verwenden. Die **QoS** -Struktur wird in den Ausgabepuffer kopiert. Der Ausgabepuffer muss groß genug groß genug sein, um die vollständige **QoS** -Struktur enthalten zu können. Der [wsaenoprodeopt](windows-sockets-error-codes-2.md) -Fehlercode wird für Dienstanbieter angezeigt, die keine Quality of Service-Unterstützung bieten.

Ein Absender kann erst dann die Datei " **SIO \_ get \_ QoS** " anrufen, wenn der Socket verbunden ist.

Ein Empfänger kann " **SIO \_ get \_ QoS** " abrufen, sobald er gebunden ist.

### <a name="sio_ideal_send_backlog_change-opcode-setting-v-t0"></a>Optimale Änderung bei der Änderung des sendebacklogs \_ \_ \_ \_ (OpCode-Einstellung: V, T = = 0)

Benachrichtigt eine Anwendung, wenn sich der Wert des idealen Sende Rückstands (ISB) für die zugrunde liegende Verbindung ändert.

Beim Senden von Daten über eine TCP-Verbindung mithilfe von Windows Sockets ist es wichtig, dass Sie eine ausreichende Menge an ausstehenden Daten (gesendet, aber noch nicht bestätigt) in TCP aufbewahren, um den höchsten Durchsatz zu erzielen. Der ideale Wert für die Datenmenge, die für den optimalen Durchsatz für die TCP-Verbindung aussteht, wird als ideale Größe des sendebacklogs (ISB) bezeichnet. Der ISB-Wert ist eine Funktion des Produkts zur Bandbreiten Verzögerung der TCP-Verbindung und des angekündigten Empfangs Fensters des Empfängers (und zum Teil der Überlastung im Netzwerk).

Der ISB-Wert pro Verbindung ist über die TCP-Protokoll Implementierung in Windows Server 2008, Windows Vista mit SP1 und höheren Versionen des Betriebssystems verfügbar. Die optimale IOCTL- **\_ \_ \_ \_ Änderung des Sende** Backlogs kann von einer Anwendung verwendet werden, um eine Benachrichtigung zu erhalten, wenn der ISB-Wert für eine Verbindung dynamisch geändert wird.

Ausführlichere Informationen finden Sie in der Referenz zur [**\_ optimalen \_ \_ \_ Änderung**](/previous-versions/windows/desktop/legacy/bb736548(v=vs.85)) des sendebacklogs.

[**SIO \_ Eine \_ ideale \_ \_ Änderung des Sende**](/previous-versions/windows/desktop/legacy/bb736548(v=vs.85)) Backlogs wird unter Windows Server 2008, Windows Vista mit SP1 und höheren Versionen des Betriebssystems unterstützt.

### <a name="sio_ideal_send_backlog_query-opcode-setting-o-t0"></a>\_Optimale optimale \_ Abfrage für Sende \_ Rückstands \_ Abfrage (OpCode-Einstellung: O, T = = 0)

Ruft den idealen ISB-Wert (Send Rückstand) für die zugrunde liegende Verbindung ab.

Beim Senden von Daten über eine TCP-Verbindung mithilfe von Windows Sockets ist es wichtig, dass Sie eine ausreichende Menge an ausstehenden Daten (gesendet, aber noch nicht bestätigt) in TCP aufbewahren, um den höchsten Durchsatz zu erzielen. Der ideale Wert für die Datenmenge, die für den optimalen Durchsatz für die TCP-Verbindung aussteht, wird als ideale Größe des sendebacklogs (ISB) bezeichnet. Der ISB-Wert ist eine Funktion des Produkts zur Bandbreiten Verzögerung der TCP-Verbindung und des angekündigten Empfangs Fensters des Empfängers (und zum Teil der Überlastung im Netzwerk).

Der ISB-Wert pro Verbindung ist über die TCP-Protokoll Implementierung in Windows Server 2008 und höher verfügbar. Der **\_ optimale \_ Abfrage \_ \_** -ioctl-Abfragedienst kann von einer Anwendung verwendet werden, um den ISB-Wert für eine Verbindung abzufragen.

Ausführlichere Informationen finden Sie in der Übersicht über die [**optimale Abfrage der "sio- \_ \_ \_ \_ Abfrage**](/previous-versions/windows/desktop/legacy/bb736549(v=vs.85)) ".

[**SIO \_ Eine \_ ideale \_ \_ Abfrage zum Senden eines Rückstands**](/previous-versions/windows/desktop/legacy/bb736549(v=vs.85)) wird unter Windows Server 2008, Windows Vista mit SP1 und höheren Versionen des Betriebssystems unterstützt.

### <a name="sio_keepalive_vals-opcode-setting-i-t3"></a>SIO \_ KeepAlive \_ Vals (OpCode-Einstellung: I, T = = 3)

Aktiviert oder deaktiviert die Einstellung pro Verbindung der TCP **-Keep-Alive-** Option, die das TCP-Keep-Alive-Timeout und-Intervall angibt. Weitere Informationen zur Keep-Alive-Option finden Sie im Abschnitt 4.2.3.6 zu den *Anforderungen für Internet Hosts –* in RFC 1122 angegebene Kommunikations Schichten auf der [IETF-Website](https://www.ietf.org/rfc/rfc1122.txt). (Diese Ressource ist möglicherweise nur in englischer Sprache verfügbar.)

**SIO \_ KeepAlive \_ Vals** kann verwendet werden, um Keep-Alive-Tests zu aktivieren oder zu deaktivieren und das Keep-Alive-Timeout und-Intervall festzulegen. Das Keep-Alive-Timeout gibt den Timeout Wert (in Millisekunden) ohne Aktivität an, bis das erste Keep-Alive-Paket gesendet wird. Das Keep-Alive-Intervall gibt das Intervall in Millisekunden zwischen dem Senden der nachfolgenden Keep-Alive-Pakete an, wenn keine Bestätigung empfangen wird.

Die Option " [**so \_ KeepAlive**](so-keepalive.md) ", eine der Optionen für den [Sol- \_ socketsocket](sol-socket-socket-options.md), kann auch verwendet werden, um den TCP-Keep-Alive-Vorgang für eine Verbindung zu aktivieren oder zu deaktivieren und den aktuellen Status dieser Option abzufragen. Um abzufragen, ob TCP Keep-Alive für einen Socket aktiviert ist, kann die [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) -Funktion mit der " **so \_ KeepAlive** "-Option aufgerufen werden. Um TCP Keep-Alive zu aktivieren oder zu deaktivieren, kann die Funktion [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) mit der Option [**so \_ KeepAlive**](so-keepalive.md) aufgerufen werden. Wenn TCP Keep-Alive mit " **so \_ KeepAlive**" aktiviert ist, werden die TCP-Standardeinstellungen für Keep-Alive-Timeout und-Intervall verwendet, es sei denn, diese Werte wurden mithilfe von " **SIO \_ KeepAlive \_ Vals**" geändert.

Ausführlichere Informationen finden Sie in der Referenz zu " [**SIO \_ KeepAlive \_ Vals**](/previous-versions/windows/desktop/legacy/dd877220(v=vs.85)) ". **SIO \_ KeepAlive \_ Vals** wird unter Windows 2000 und höher unterstützt.

### <a name="sio_loopback_fast_path-opcode-setting-i-t3"></a>Schneller Pfad für "sio \_ Loopback" \_ \_ (OpCode-Einstellung: I, T = = 3)

Konfiguriert einen TCP-Socket für eine geringere Latenz und schnellere Vorgänge an der Loopback Schnittstelle. Diese IOCTL fordert an, dass der TCP/IP-Stapel einen speziellen schnellen Pfad für Loopback Vorgänge in diesem Socket verwendet. Die IOCTL-Schleife für den " [**SIO \_ Loopback \_ \_**](/previous-versions/windows/desktop/legacy/jj841212(v=vs.85)) " kann nur mit TCP-Sockets verwendet werden. Diese IOCTL muss auf beiden Seiten der Loopback Sitzung verwendet werden. Der schnelle TCP-Loopback Pfad wird entweder über die IPv4-oder IPv6-loopback Schnittstelle unterstützt. Standardmäßig ist **der \_ \_ schnelle \_ Pfad** für die hoch-Loopback Option deaktiviert.

Ausführlichere Informationen finden Sie in der Übersicht über die [**\_ \_ schnell \_ Pfad**](/previous-versions/windows/desktop/legacy/jj841212(v=vs.85)) Übersicht über den SIO-Loopback. **SIO \_ Der schnelle Loopback \_ \_ Pfad** wird unter Windows 8, Windows Server 2012 und höher unterstützt.

### <a name="sio_multipoint_loopback-opcode-setting-v-t1"></a>SIO \_ Multipoint \_ Loopback (OpCode-Einstellung: V, T = = 1)

Steuert, ob von einer Anwendung auf dem lokalen Computer (nicht notwendigerweise durch denselben Socket) gesendete Daten in einer Multicast Sitzung von einem Socket empfangen werden, der der Multicast Zielgruppe in der Loopback Schnittstelle angehört. Der Wert **true** bewirkt, dass von einer Anwendung auf dem lokalen Computer gesendete Multicast Daten an einen Abhör Socket an der Loopback Schnittstelle übermittelt werden. Mit dem Wert " **false** " wird verhindert, dass von einer Anwendung auf dem lokalen Computer gesendete Multicast Daten an einen Abhör Socket an der Loopback Schnittstelle übermittelt werden. Standardmäßig ist **das \_ Multipoint- \_ Loopback von SIO** aktiviert.

### <a name="sio_multicast_scope-opcode-setting-i-t1"></a>SIO- \_ Multicast \_ Bereich (OpCode-Einstellung: I, T = = 1)

Gibt den Bereich an, in dem Multicast Übertragungen stattfinden. Der Bereich wird als die Anzahl der zu deckenden Routing Netzwerksegmente definiert. Ein Bereich von 0 (null) gibt an, dass die Multicast Übertragung nicht bei der Übertragung platziert würde, sondern über Sockets innerhalb des lokalen Hosts verteilt werden könnte. Ein Bereichs Wert von 1 (Standardwert) gibt an, dass die Übertragung in das Netzwerk übertragen wird, ohne Router zu überschreiten. Höhere Bereichs Werte bestimmen die Anzahl von Routern, die überschritten werden können. Beachten Sie, dass dies dem Time-to-Live (TTL)-Parameter in IP-Multicasting entspricht. Standardmäßig ist der Gültigkeitsbereich 1.

### <a name="sio_query_rss_processor_info-opcode-setting-o-t1"></a>\_RSS-Abfrage-RSS- \_ \_ Prozessor \_ Info (OpCode-Einstellung: O, T = = 1)

Fragt die Zuordnung zwischen einem Socket und einem RSS-Prozessor Core und einem NUMA-Knoten ab.

Die IDE- [**\_ Abfrage \_ RSS- \_ Prozessor \_ Info**](/previous-versions/windows/desktop/legacy/jj553482(v=vs.85)) ioctl gibt eine [**\_ socketprozessoraffinitäts \_**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) -Struktur zurück, die die [**Prozessor \_**](/windows/win32/api/winnt/ns-winnt-processor_number) -und NUMA-Knoten-ID enthält. Die zurückgegebene **Prozessor \_ Zahlen** Struktur enthält eine Gruppennummer und eine relative Prozessornummer in der Gruppe.

Ausführlichere Informationen finden Sie in der Referenz zur Übersicht über den [**\_ RSS-Abfrage-RSS- \_ \_ \_ Prozessor**](/previous-versions/windows/desktop/legacy/jj553482(v=vs.85)) . **SIO \_ Die Abfrage- \_ RSS- \_ Prozessor \_ Informationen** werden unter Windows 8, Windows Server 2012 und höher unterstützt.

### <a name="sio_query_rss_scalability_info-opcode-setting-o-t3"></a>\_Leistungsinformationen für die RSS-Abfrage RSS- \_ \_ Skalierbarkeit \_ (OpCode-Einstellung: O, T = = 3)

Abfragen Auslagerung-Schnittstellen für RSS-Funktionen (Receive-Side Scaling). Die Argument Struktur, die für die **\_ RSS- \_ \_ Skalierbarkeits \_ Info von SIO-Abfrage** zurückgegeben wird, wird in der RSS- **\_ Skalierbarkeits \_ Info** -Struktur angegeben, die in der Header Datei " *mstc* Diese Struktur ist wie folgt definiert:

```cpp
// Scalability info for the transport
typedef struct _RSS_SCALABILITY_INFO {
   BOOLEAN RssEnabled;
} RSS_SCALABILITY_INFO, *PRSS_SCALABILITY_INFO;
```

Der Wert, der im **rssaktivierten** -Member zurückgegeben wird, gibt an, ob RSS für mindestens eine Schnittstelle aktiviert ist.

Wenn der Ausgabepuffer für die **RSS- \_ Skalierbarkeits- \_ Informations** Struktur nicht groß genug ist (der *cboutbuffer* ist kleiner als die Größe der **RSS- \_ Skalierbarkeits \_ Informationen**) oder wenn der *lpvoutbuffer* -Parameter ein **null** -Zeiger ist, wird ein **\_ Socketfehler** als Ergebnis dieser ioctl zurückgegeben, und [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) gibt [WSAEINVAL](windows-sockets-error-codes-2.md)zurück

Bei hoch Geschwindigkeits Netzwerken, in denen sich mehrere CPUs innerhalb eines einzelnen Systems befinden, ist die Fähigkeit des Netzwerkprotokoll Stapels, sich auf einem MultiCPU-System zu skalieren, behindert, da die Architektur von NDIS 5,1 und früheren Versionen die Verarbeitung des Empfangs Protokolls auf eine einzelne CPU beschränkt. Die Empfangs seitige Skalierung (Receive-Side Scaling, RSS) löst dieses Problem, indem die Netzwerk Last von einem Netzwerkadapter auf mehrere CPUs verteilt werden kann.

**SIO \_ Die Abfrage- \_ RSS- \_ Skalierbarkeits \_ Informationen** werden unter Windows Vista und höher unterstützt.

### <a name="sio_query_transport_setting-opcode-setting-i-t3"></a>Abfrage Transport Einstellung für "sio" \_ \_ \_ (OpCode-Einstellung: I, T = = 3)

Fragt die Transport Einstellungen für einen Socket ab. Die abgefragte Transport Einstellung basiert auf der [**Transport \_ Einstellungs- \_ ID**](/windows/win32/api/transportsettingcommon/ns-transportsettingcommon-transport_setting_id) , die im *lpvinbuffer* -Parameter übergeben wird.

Die einzige Transport Einstellung, die derzeit definiert, ist die Funktion für die **echt \_ Zeit \_ Benachrichtigungs \_ Funktion** in einem TCP-Socket.

Wenn für die [**Transport \_ Einstellungs- \_ ID**](/windows/win32/api/transportsettingcommon/ns-transportsettingcommon-transport_setting_id) das **GUID** -Element auf **echt \_ Zeit \_ Benachrichtigungs \_ Funktion** festgelegt ist, ist dies eine Anforderung zum Abfragen der Echt Zeit Benachrichtigungseinstellungen für den TCP-Socket, der mit dem [**controlchannel-**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) Vorgang zum Empfangen von Hintergrund Netzwerk Benachrichtigungen in einer Windows Store-App verwendet wird. Wenn der Aufruf von [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) oder [**wspioctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) erfolgreich ist, gibt diese IOCTL eine Ausgabestruktur der [**echt \_ Zeit \_ Benachrichtigungs \_ Einstellung \_**](/windows/desktop/api/Mstcpip/ns-mstcpip-real_time_notification_setting_input) mit dem aktuellen Status zurück.

Ausführlichere Informationen finden Sie in der Referenz zur Übersicht über die [**\_ Abfrage \_ Transport \_ Einstellung**](/previous-versions/windows/desktop/legacy/jj553483(v=vs.85)) . **SIO \_ Die \_ \_ Einstellung für den Abfrage Transport** wird unter Windows 8, Windows Server 2012 und höher unterstützt.

### <a name="sio_query_wfp_ale_endpoint_handle-opcode-setting-o-t3"></a>\_ \_ Zentrale Endpunkt Handle für die WFP-Abfrage \_ \_ \_ (OpCode-Einstellung: O, T = = 3)

Fragt den Endpunkt Handle der Logik Schicht Erzwingung ab.

Die Windows-Filter Plattform (WFP) unterstützt die Überprüfung und Änderung von Netzwerk Datenverkehr. Unter Windows Vista konzentriert sich WFP auf Szenarien, in denen der Host Computer der Kommunikations Endpunkt ist. Unter Windows Server 2008 gibt es jedoch Edge-Firewall-Implementierungen, die die WFP-Plattform nutzen möchten, um den Pass-Through-Datenverkehr zu überprüfen und zu übermitteln. Der Internet Security and Acceleration (ISA)-Server ist ein Beispiel für ein solches Edge-Gerät.

Es gibt einige firewallszenarien, in denen möglicherweise ein eingehender Paket in den mit einem vorhandenen Endpunkt verknüpften sendepfad eingefügt werden muss. Es muss ein Mechanismus vorhanden sein, um das dem Ziel Endpunkt zugeordnete Transportschicht-Endpunkt Handle zu ermitteln. Die Anwendung, die den Endpunkt erstellt hat, besitzt diese Transportschicht Endpunkte. Diese IOCTL wird zur Bereitstellung eines Sockethandles für die Zuordnung von Endpunkt Handles auf Transport Ebene verwendet.

Wenn der Ausgabepuffer für das Endpunkt Handle nicht groß genug ist (der *cboutbuffer* ist kleiner als die Größe eines **UINT64**) oder der *lpvoutbuffer* -Parameter ein **null** -Zeiger ist, wird ein **\_ Socketfehler** als Ergebnis dieser ioctl zurückgegeben, und [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) gibt [WSAEINVAL](windows-sockets-error-codes-2.md)zurück.

**SIO \_ Abfrage- \_ WFP- \_ \_ Endpunkt \_ handle** wird unter Windows Vista und höher unterstützt.

### <a name="sio_query_wfp_connection_redirect_context-opcode-setting-i-t3"></a>Rahmen für den \_ \_ Verbindungs Umleitungs Kontext der "sio Query WFP" \_ \_ \_ (OpCode-Einstellung: I, T = = 3)

Fragt den Umleitungs Kontext für einen von einem Windows-Filter Plattform (WFP)-Umleitungs Dienst verwendeten Umleitungs Daten Satz ab.

Der [**\_ \_ \_ Verbindungs \_ Umleitungs \_ Kontext**](/previous-versions/windows/desktop/legacy/hh859712(v=vs.85)) ioctl für die WFP-Abfrage wird verwendet, um die Proxy Verbindungs Nachverfolgung für umgeleitete Socketverbindungen bereitzustellen. Diese WFP-Funktion ermöglicht das Nachverfolgen von Umleitungs Datensätzen von der anfänglichen Umleitung einer Verbindung zur endgültigen Verbindung zum Ziel.

Ausführlichere Informationen finden Sie in der Übersicht über die [**\_ \_ WFP- \_ Verbindungs \_ Umleitungs \_ Kontext**](/previous-versions/windows/desktop/legacy/hh859712(v=vs.85)) Referenz. **SIO \_ Der \_ \_ Verbindungs \_ Umleitungs \_ Kontext der WFP-Abfrage** wird unter Windows 8, Windows Server 2012 und höher unterstützt.

### <a name="sio_query_wfp_connection_redirect_records-opcode-setting-i-t3"></a>Leistungs \_ \_ Datensätze für die WFP-Verbindungs Umleitung von SIO Abfragen \_ \_ \_ (OpCode-Einstellung: I, T = = 3)

Fragt den Umleitungs Daten Satz für die akzeptierte TCP/IP-Verbindung für die Verwendung durch einen WFP-Umleitungs Dienst (Windows Filtering Platform) ab.

Die [**\_ \_ \_ \_ \_ Datensätze der WFP-Verbindungs Umleitung**](/previous-versions/windows/desktop/legacy/hh859713(v=vs.85)) mit der Datenbank ". ioctl" werden verwendet, um eine Proxy Verbindung für umgeleitete Socketverbindungen herzustellen. Diese WFP-Funktion ermöglicht das Nachverfolgen von Umleitungs Datensätzen von der anfänglichen Umleitung einer Verbindung zur endgültigen Verbindung zum Ziel.

Ausführlichere Informationen finden Sie in der Übersicht über die [**\_ \_ WFP- \_ Verbindungs \_ Umleitungs \_ Einträge**](/previous-versions/windows/desktop/legacy/hh859713(v=vs.85)) in der Übersicht. **SIO \_ \_WFP- \_ Verbindungs \_ Umleitungs \_ Datensätze Abfragen** werden unter Windows 8, Windows Server 2012 und höher unterstützt.

### <a name="sio_rcvall-opcode-setting-i-t3"></a>SIO \_ rcvall (OpCode-Einstellung: I, T = = 3)

Ermöglicht einem Socket, alle IPv4-oder IPv6-Pakete zu empfangen, die über eine Netzwerkschnittstelle übergeben werden. Das an die [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) -Funktion über gegebene Sockethandle muss einer der folgenden sein:

-   Ein IPv4-Socket, der mit der Adressfamilie "AF \_ inet", dem socketyp auf "Sock \_ RAW" und dem Protokoll auf "ipproto IP" erstellt wurde \_ .
-   Ein IPv6-Socket, der mit der Adressfamilie auf AF \_ inet6, dem socketyp auf Sock \_ RAW und dem Protokoll auf ipproto IPv6 erstellt wurde \_ .

Der Socket muss auch an eine explizite lokale IPv4-oder IPv6-Schnittstelle gebunden werden, was bedeutet, dass Sie keine Bindung an **inaddr \_ any** oder **in6addr \_ any** herstellen können.

Unter Windows Server 2008 und früheren Versionen werden von der IOCTL-Einstellung " [**SIO \_ rcvall**](/previous-versions/windows/desktop/legacy/ee309610(v=vs.85)) " keine lokalen Pakete erfasst, die von einer Netzwerkschnittstelle gesendet werden. Diese enthielten Pakete, die auf einer anderen Schnittstelle empfangen wurden, und haben die für die IOCTL " **SIO \_ rcvall** " angegebene Netzwerkschnittstelle weitergeleitet.

Unter Windows 7 und Windows Server 2008 R2 wurde dies geändert, sodass lokale Pakete, die von einer Netzwerkschnittstelle gesendet werden, ebenfalls aufgezeichnet werden. Dies schließt Pakete ein, die auf einer anderen Schnittstelle empfangen werden, und leitet dann die Netzwerkschnittstelle, die an den Socket gebunden ist, mit der " [**SIO \_ rcvall**](/previous-versions/windows/desktop/legacy/ee309610(v=vs.85)) "

Das Festlegen dieser ioctl erfordert Administrator Rechte auf dem lokalen Computer.

Diese Funktion wird manchmal als gemischten-Modus bezeichnet.

Die möglichen Werte für die IOCTL-Option " **SIO \_ rcvall** " werden in der **rcvall \_** -Enumeration angegeben, die in der Header Datei " *MSTCPIP. h* " definiert ist. Die möglichen Werte für "sio \_ rcvall" lauten wie folgt:

| Begriff                                                                                                                 | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-|-|
| <span id="RCVALL_OFF"></span><span id="rcvall_off"></span>rcvall \_ aus<br/>                                     | Deaktivieren Sie diese Option, damit ein Socket nicht alle IPv4-oder IPv6-Pakete im Netzwerk empfängt. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="RCVALL_ON"></span><span id="rcvall_on"></span>rcvall \_ on<br/>                                        | Aktivieren Sie diese Option, damit ein Socket alle IPv4-oder IPv6-Pakete im Netzwerk empfängt. Diese Option aktiviert den gemischten-Modus auf der Netzwerkschnittstellenkarte (NIC), wenn die NIC den gemischten-Modus unterstützt. In einem LAN-Segment mit einem Netzwerkhub erfasst eine NIC, die den gemischten-Modus unterstützt, den gesamten IPv4-oder IPv6-Datenverkehr im LAN, einschließlich des Datenverkehrs zwischen anderen Computern desselben LAN-Segments. Alle aufgezeichneten Pakete (IPv4 oder IPv6, abhängig vom Socket) werden an den Rohdaten Socket übermittelt. <br/> Mit dieser Option werden nicht andere Pakete (z. b. ARP-, IPX-und NetBEUI-Pakete) auf der-Schnittstelle erfasst.<br/> NetMon verwendet den gleichen Modus für die Netzwerkschnittstelle, verwendet diese Option jedoch nicht zum Erfassen von Datenverkehr.<br/> |
| <span id="RCVALL_SOCKETLEVELONLY"></span><span id="rcvall_socketlevelonly"></span>rcvall \_ socketlevelonly<br/> | Diese Funktion ist zurzeit nicht implementiert, sodass das Festlegen dieser Option keine Auswirkung hat.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="RCVALL_IPLEVEL"></span><span id="rcvall_iplevel"></span>rcvall \_ iplevel<br/>                         | Aktivieren Sie diese Option, damit ein IPv4-oder IPv6-Socket alle Pakete auf IP-Ebene im Netzwerk empfängt. Diese Option aktiviert nicht den gemischten-Modus auf der Netzwerkschnittstellenkarte. Diese Option wirkt sich nur auf die Paketverarbeitung auf IP-Ebene aus. Die NIC empfängt weiterhin nur Pakete, die an die konfigurierten Unicast-und Multicast Adressen weitergeleitet werden. Ein Socket, für den diese Option aktiviert ist, empfängt jedoch nicht nur Pakete, die an bestimmte IP-Adressen weitergeleitet werden, sondern empfängt alle IPv4-oder IPv6-Pakete, die die NIC empfängt.<br/> Mit dieser Option werden keine anderen Pakete (z. b. ARP-, IPX-und NetBEUI-Pakete) erfasst, die über die Schnittstelle empfangen werden.<br/>                                                                                             |



 

Ausführlichere Informationen finden Sie in der Referenz zu " [**SIO \_ rcvall**](/previous-versions/windows/desktop/legacy/ee309610(v=vs.85)) ".

**SIO \_ Rcvall** wird unter Windows 2000 und höher unterstützt.

### <a name="sio_rcvall_igmpmcast-opcode-setting-i-t3"></a>SIO \_ rcvall \_ igmpmcast (OpCode-Einstellung: I, T = = 3)

Ermöglicht einem Socket, den gesamten IGMP-Multicast-IP-Datenverkehr im Netzwerk zu empfangen, ohne anderen Multicast-IP-Datenverkehr zu empfangen. Das an die [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) -Funktion über gegebene Sockethandle muss von der AF \_ -Adressfamilie, dem Sock \_ -rohsocketyp und dem ipproto \_ IGMP-Protokoll sein. Der Socket muss auch an eine explizite lokale Schnittstelle gebunden werden, was bedeutet, dass Sie keine Bindung an inaddr any herstellen können \_ .

Sobald der Socket gebunden und der IOCTL-Satz ist, geben Aufrufe der [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv) -oder der [**empfangener**](/windows/desktop/api/winsock/nf-winsock-recv) -Funktion Multicast-IP-Datagramme zurück, die die angegebene Schnittstelle übergeben. Beachten Sie, dass Sie einen ausreichend großen Puffer angeben müssen. Das Festlegen dieser ioctl erfordert Administrator Rechte auf dem lokalen Computer.

**SIO \_ Rcvall \_ igmpmcast** wird unter Windows 2000 und höher unterstützt.

### <a name="sio_rcvall_mcast-opcode-setting-i-t3"></a>Mcast für "sio \_ rcvall" \_ (OpCode-Einstellung: I, T = = 3)

Ermöglicht einem Socket, den gesamten Multicast-IP-Datenverkehr im Netzwerk (d. h. alle IP-Pakete, die für IP-Adressen im Bereich von 224.0.0.0 bis 239.255.255.255 bestimmt sind) zu empfangen. Das an die [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) -Funktion über gegebene Sockethandle muss von der AF \_ -Adressfamilie, dem Sock \_ -rohsocketyp und dem ipproto \_ UDP-Protokoll sein. Der Socket muss auch an eine explizite lokale Schnittstelle gebunden werden, was bedeutet, dass Sie keine Bindung an inaddr any herstellen können \_ . Der Socket sollte an Port NULL gebunden werden.

Sobald der Socket gebunden und der IOCTL-Satz ist, geben Aufrufe der [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv) -oder der [**empfangener**](/windows/desktop/api/winsock/nf-winsock-recv) -Funktion Multicast-IP-Datagramme zurück, die die angegebene Schnittstelle übergeben. Beachten Sie, dass Sie einen ausreichend großen Puffer angeben müssen. Das Festlegen dieser ioctl erfordert Administrator Rechte auf dem lokalen Computer.

**SIO \_ Rcvall \_ mcast** wird unter Windows 2000 und höher unterstützt.

### <a name="sio_release_port_reservation-opcode-setting-i-t3"></a>Port Reservierung für die SIO- \_ Freigabe \_ \_ (OpCode-Einstellung: I, T = = 3)

Gibt eine Lauf Zeit Reservierung für einen Block von TCP-oder UDP-Ports frei. Die zu veröffentlichende Lauf Zeit Reservierung muss vom ausstellenden Prozess mithilfe der Zertifizierungsstellen-ioctl-Reservierung für den Zertifikat erstellungsport abgerufen werden. [**\_ \_ \_**](/previous-versions/windows/desktop/legacy/gg699720(v=vs.85))

Ausführlichere Informationen finden Sie in der Referenz zur Übersicht über den [**SIO- \_ \_ releaseport \_**](/previous-versions/windows/desktop/legacy/gg699722(v=vs.85)) .

[**SIO \_ Die Freigabe \_ Port \_ Reservierung**](/previous-versions/windows/desktop/legacy/gg699722(v=vs.85)) wird unter Windows Vista und höheren Versionen des Betriebssystems unterstützt.

### <a name="sio_routing_interface_change-opcode-setting-i-t1"></a>Änderungen an der \_ Routing Schnittstelle von SIO \_ \_ (OpCode-Einstellung: I, T = = 1)

, Um Benachrichtigungen über eine Änderung der Routing Schnittstelle zu erhalten, die verwendet werden soll, um die Remote Adresse im Eingabepuffer zu erreichen (angegeben als [**sockaddr**](sockaddr-2.md) -Struktur). Nach Abschluss dieser ioctl werden keine Ausgabeinformationen zur neuen Routing Schnittstelle bereitgestellt. der Abschluss gibt lediglich an, dass die Routing Schnittstelle für ein bestimmtes Ziel geändert wurde, und sollte mithilfe der " **SIO \_ Routing \_ Interface \_ Query** ioctl" abgefragt werden.

Es wird davon ausgegangen, dass die Anwendung überlappende e/a-Vorgänge verwendet, um über die Änderungen an der Routing Schnittstelle über den Abschluss der Anforderungen an die Routing **\_ \_ Schnittstellen \_ Änderung** benachrichtigt zu werden. Wenn die **\_ Routing Schnittstelle von SIO \_ \_ geändert** wird, wird ioctl bei einem nicht blockierenden Socket ausgegeben, bei dem die Parameter *lpoverlgetauscht* und *lpCompletionRoutine* auf **null** festgelegt sind. die sofortige Rückgabe von und " [WSAEWOULDBLOCK](windows-sockets-error-codes-2.md) " wird als Fehler beendet, und die Anwendung kann dann auf Routing Änderungs Ereignisse über den [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) -oder [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) -Vorgang mit dem FD-Änderungs Bit für FD- \_ Routing \_ Schnittstellen \_ in der Bitmaske des Netzwerk Ereignisses warten.

Es wurde erkannt, dass die Routing Informationen in den meisten Fällen stabil bleiben, damit die Anwendung mehrere ausstehende IOCTLs-Benachrichtigungen erhalten kann, um Benachrichtigungen über alle Ziele zu erhalten, an denen Sie interessiert ist, und dass der Dienstanbieter diese Benachrichtigungs Anforderungen nachverfolgen kann. Diese Situation kann vermieden werden, indem die Bedeutung der Eingabeparameter erweitert und die Anforderungen des Dienstanbieters wie folgt gelockert werden:

-   Die Anwendung kann eine bestimmte Platzhalter Adresse für die Protokollfamilie angeben (identisch mit der im [**Bind**](/windows/desktop/api/winsock/nf-winsock-bind) -Befehl verwendeten, wenn eine Bindung an eine beliebige verfügbare Adresse angefordert wird), um Benachrichtigungen über Routing Änderungen anzufordern. Dadurch kann die Anwendung nur eine ausstehende Änderung der **" \_ SIO \_ Routing \_ Interface** " für alle Sockets und Ziele behalten, die Sie besitzt, und dann die Routing **\_ \_ Schnittstellen \_ Abfrage "sio** " verwenden, um die eigentlichen Routing Informationen zu erhalten.
-   Ein Dienstanbieter hat die Möglichkeit, die von der Anwendung angegebenen Informationen im Eingabepuffer der Änderungen an der **Routing \_ Schnittstelle \_ \_** der Zertifizierungsstelle zu ignorieren (als ob die Anwendung eine Platzhalter Adresse angegeben hat), und schließt das Änderungs Ereignis der " **SIO- \_ Routing \_ Schnittstelle \_ ändern** ioctl" oder "Signal \_ \_ \_

### <a name="sio_routing_interface_query-opcode-setting-i-o-t1"></a>SIO- \_ Routing \_ Schnittstellen \_ Abfrage (OpCode-Einstellung: I, O, T = = 1)

Zum Abrufen der Adresse der lokalen Schnittstelle (dargestellt als [**sockaddr**](sockaddr-2.md) -Struktur), die zum Senden an die im Eingabepuffer angegebene Remote Adresse (als **sockaddr**) verwendet werden soll. Remote-Multicast Adressen können im Eingabepuffer übermittelt werden, um die Adresse der bevorzugten Schnittstelle für die Multicast Übertragung zu erhalten. In jedem Fall kann die zurückgegebene Schnittstellen Adresse von der Anwendung in einer nachfolgenden BIND ()-Anforderung verwendet werden.

Beachten Sie, dass Routen geändert werden können. Daher können Anwendungen nicht von den Informationen abhängen, die von der **SIO- \_ Routing \_ Schnittstellen \_ Abfrage** zurückgegeben werden. Anwendungen registrieren sich möglicherweise für Routing Änderungs Benachrichtigungen über die **SIO- \_ Routing \_ Schnittstelle \_ ändern** Sie IOCTL, das Benachrichtigungen über überlappende e/a oder ein FD- \_ Routing \_ Schnittstellen \_ Änderungs Ereignis bereitstellt. Die folgende Sequenz von Aktionen kann verwendet werden, um sicherzustellen, dass die Anwendung immer über aktuelle Routing Schnittstellen Informationen für ein bestimmtes Ziel verfügt:

-   Problem **- \_ Routing \_ Schnittstelle \_ Änderung der Routing Schnittstelle** ioctl
-   Problem-Prozessor- **\_ Routing \_ Schnittstellen \_ Abfrage** ioctl
-   Wenn die IOCTL-Änderung durch die **SIO- \_ Routing \_ \_ Schnittstelle** von der Anwendung über eine überlappende e/a oder durch Signalisieren eines FD- \_ Routing \_ Schnittstellen Änderungs Ereignisses benachrichtigt wird \_ , sollte die gesamte Sequenz von Aktionen wiederholt werden.

Wenn der Ausgabepuffer nicht groß genug ist, um die Schnittstellen Adresse aufzunehmen, \_ wird als Ergebnis dieser ioctl ein Socket-Fehler zurückgegeben, und [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) gibt [wsaefault](windows-sockets-error-codes-2.md)zurück. Die erforderliche Größe des Ausgabepuffers wird in diesem Fall in " *lpcbbytes"* zurückgegeben. Beachten Sie, dass der Fehlercode von wsaefault ebenfalls zurückgegeben wird, wenn der Parameter *lpvinbuffer*, *lpvoutbuffer* oder *lpcbbytesall* nicht vollständig in einem gültigen Teil des Benutzer Adressraums enthalten ist.

Wenn die im Eingabepuffer angegebene Zieladresse nicht über eine der verfügbaren Schnittstellen erreicht werden kann, \_ wird als Ergebnis dieser ioctl ein Socket-Fehler zurückgegeben, und [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) gibt [wsaenetunreach](windows-sockets-error-codes-2.md) oder sogar [wsaenetdown](windows-sockets-error-codes-2.md) zurück, wenn alle Netzwerkverbindungen verloren gehen.

### <a name="sio_set_compatibility_mode-opcode-setting-i-t3"></a>Kompatibilitätsmodus für die Betriebs Systemeinrichtung \_ \_ \_ (OpCode-Einstellung: I, T = = 3)

Fordert an, wie der Netzwerk Stapel bestimmte Verhalten verarbeiten soll, bei denen die Standardmethode für die Handhabung des Verhaltens in Windows-Versionen unterschiedlich sein kann. Die Argument Struktur für **den \_ \_ Kompatibilitäts \_ Modus** für den SIO-Satz wird in der **WSA- \_ Kompatibilitäts \_ Modus** -Struktur angegeben, die in der Header Datei " *mswap* Diese Struktur ist wie folgt definiert:

```cpp
/* Argument structure for SIO_SET_COMPATIBILITY_MODE */
typedef struct _WSA_COMPATIBILITY_MODE {
    WSA_COMPATIBILITY_BEHAVIOR_ID BehaviorId;
    ULONG TargetOsVersion;
} WSA_COMPATIBILITY_MODE, *PWSA_COMPATIBILITY_MODE;
```

Der im **Verhaltensweise-** Member angegebene Wert gibt das angeforderte Verhalten an. Der im **targetosversion** -Member angegebene Wert gibt die Windows-Version an, die für das Verhalten angefordert wird.

Der Behavior **orid-** Member kann einer der Werte aus dem Enumerationstyp der **WSA- \_ Kompatibilitäts \_ Verhaltens- \_ ID** sein, der in der Header Datei " *mslisockdef. h* " definiert ist. Die möglichen Werte für den Member " **verhalarid** " lauten wie folgt.

| Begriff                                                                                                                                                                             | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-|-|
| <span id="WsaBehaviorAll"></span><span id="wsabehaviorall"></span><span id="WSABEHAVIORALL"></span>Wsaverhalorall<br/>                                                     | Dies entspricht der Anforderung aller möglichen kompatiblen Verhalten, die für die **WSA- \_ Kompatibilitäts \_ Verhaltens- \_ ID** definiert sind.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="WsaBehaviorReceiveBuffering"></span><span id="wsabehaviorreceivebuffering"></span><span id="WSABEHAVIORRECEIVEBUFFERING"></span>Wsaverhaltereceivepufferung<br/> | Wenn das **targetosversion** -Element auf einen Wert für Windows Vista oder höher festgelegt ist, sind die TCP-Empfangs Puffergröße auf diesem Socket mithilfe der Option " **so \_ rcvbuf** " auch nach der Einrichtung einer TCP-Verbindung zulässig. <br/> Wenn das **targetosversion** -Element auf einen früheren Wert als Windows Vista festgelegt ist, sind nach dem **herstellen der Verbindung \_** keine Reduzierungen der TCP-Empfangs Puffergröße auf diesem Socket zulässig. <br/>                                                                                                                                                                                  |
| <span id="WsaBehaviorAutoTuning"></span><span id="wsabehaviorautotuning"></span><span id="WSABEHAVIORAUTOTUNING"></span>Wsaverhalorautotuning<br/>                         | Wenn das **targetosversion** -Element auf einen Wert für Windows Vista oder höher festgelegt ist, ist die automatische Optimierung des Empfangs Fensters aktiviert, und der TCP-Fenster Skalierungsfaktor wird vom Standardwert 8 auf 2 reduziert.<br/> Wenn **targetosversion** auf einen früheren Wert als Windows Vista festgelegt ist, ist die automatische Optimierung des Empfangs Fensters deaktiviert. Die Option zum Skalieren von TCP-Fenstern ist ebenfalls deaktiviert, und die maximale tatsächliche Empfangs Fenstergröße ist auf 65.535 Bytes begrenzt. Die Option für die TCP-Fenster Skalierung kann für die Verbindung nicht ausgehandelt werden, auch wenn die Option " **\_ rcvbuf** " für diesen Socket aufgerufen wurde und einen Wert größer als 65.535 Bytes angibt, bevor die Verbindung hergestellt wurde.<br/> |



 

Ausführlichere Informationen finden Sie in der Referenz zum [**\_ \_ Kompatibilitäts \_ Modus**](/previous-versions/windows/desktop/legacy/cc136103(v=vs.85)) für den SIO-Satz.

**SIO \_ Der festgelegte \_ Kompatibilitäts \_ Modus** wird unter Windows Vista und höher unterstützt.

### <a name="sio_set_group_qos-opcode-setting-i-t1"></a>\_ \_ \_ QoS-QoS für die Gruppe ' SIO ' (OpCode-Einstellung: I, T = = 1)

Reserviert.

### <a name="sio_set_priority_hint-opcode-setting-i-t3"></a>SIO_SET_PRIORITY_HINT (OpCode-Einstellung: I, T = = 3)

Stellt einen Hinweis für das zugrunde liegende Transportprotokoll bereit, mit dem der Datenverkehr für diesen Socket mit einer bestimmten Priorität behandelt werden soll. Der *lpvinbuffer* muss auf eine Variable vom Typ " **PRIORITY_HINT** " mit " *cbinbuffer* ", die auf sizeof (PRIORITY_HINT) festgelegt ist, verweisen. Der *lpvoutbuffer* -Parameter und der *cboutbuffer* -Parameter müssen NULL bzw. 0 ( **null** ) sein. Die Microsoft Windows-TCP-Implementierung unterstützt diese IOCTL ab Windows 10, Version 1809 (10,0; Build 17763) und höher wie folgt: Wenn der angeforderte Prioritätswert auf **iopriorityhintverylow** festgelegt ist, verwendet TCP eine geänderte Version des ledbat-Algorithmus (definiert in RFC 6817) zum Steuern des ausgehenden Datenverkehrs Satzes für den Socket. Der eingehende Datenverkehr wird von dieser ioctl nicht beeinträchtigt. Ledbat ist ein Scavenger-Algorithmus, und sein Ziel besteht darin, die Latenz niedrig zu halten und jegliche negativen Auswirkungen auf den Datenverkehr mit normaler Priorität zu vermeiden, wenn der Datenverkehr mit normaler Priorität vorhanden ist.

Siehe auch [RFC 6817](https://tools.ietf.org/html/rfc6817).

**SIO_SET_PRIORITY_HINT** wird unter Windows 10, Version 1809 (10,0; Build 17763) und höher.

### <a name="sio_set_qos-opcode-setting-i-t1"></a>\_ \_ QoS-QoS-Satz (OpCode-Einstellung: I, T = = 1)

Ordnen Sie die angegebene [**QoS**](/windows/win32/api/winsock2/ns-winsock2-qos) -Struktur dem Socket zu. Es ist kein Ausgabepuffer erforderlich. die **QoS** -Struktur wird aus dem Eingabepuffer abgerufen. Der [wsaenoprodeopt](windows-sockets-error-codes-2.md) -Fehlercode wird für Dienstanbieter angezeigt, die keine Quality of Service-Unterstützung bieten.

### <a name="sio_tcp_initial_rto-opcode-setting-i-t3"></a>SIO_TCP_INITIAL_RTO (OpCode-Einstellung: I, T = = 3)

Steuert die anfänglichen Neuübertragungs-Eigenschaften (SYN/SYN + ACK) eines TCP-Sockets durch Konfigurieren der anfänglichen RTO-Parameter (Neuübertragungs Timeout). Die Konfigurationsparameter werden in einer [**TCP- \_ Initial- \_ RTO- \_ Parameter**](/windows/desktop/api/mswsock/ns-mswsock-transmit_file_buffers) Struktur angegeben.

Ausführlichere Informationen finden Sie in der [**SIO_TCP_INITIAL_RTO**](./sio-tcp-initial-rto.md) -Referenz. [**SIO_TCP_INITIAL_RTO**](./sio-tcp-initial-rto.md) wird unter Windows 8, Windows Server 2012 und höher unterstützt.

### <a name="sio_translate_handle-opcode-setting-i-o-t1"></a>SIO \_ Translation- \_ handle (OpCode-Einstellung: I, O, T = = 1)

Zum Abrufen eines entsprechenden Handles für Socket *s* , das im Kontext einer Begleit Schnittstelle gültig ist (z. b. th \_ netdev und Th \_ TAPI). Eine Manifest-Konstante, die die Begleit Schnittstelle zusammen mit allen anderen benötigten Parametern identifiziert, wird im Eingabepuffer angegeben. Das entsprechende Handle ist nach Abschluss dieser Funktion im Ausgabepuffer verfügbar. Ausführliche Informationen zu einer bestimmten Begleit Schnittstelle finden Sie im entsprechenden Abschnitt in [Winsock-Anlagen](winsock-annexes.md) . Der [wsaenoprodeopt](windows-sockets-error-codes-2.md) -Fehlercode wird für Dienstanbieter angegeben, die diese IOCTL für die angegebene Begleit Schnittstelle nicht unterstützen. Diese IOCTL Ruft das Handle ab, das mit dem **SIO- \_ Übersetzungs \_ handle** verknüpft ist.

Es wird empfohlen, dass die Component Object Model (com) anstelle dieser IOCTL verwendet werden, um andere Schnittstellen zu ermitteln und zu verfolgen, die möglicherweise von einem Socket unterstützt werden. Diese IOCTL ist aus Gründen der Abwärtskompatibilität mit Systemen vorhanden, in denen com nicht verfügbar ist oder aus einem anderen Grund nicht verwendet werden kann.

### <a name="sio_udp_connreset-opcode-setting-i-t3"></a>Konfigurations-UDP-Verbindung \_ \_ (OpCode-Einstellung: I, T = = 3)

**Windows XP:** Steuert, ob \_ nicht erreichbare UDP-Ports gemeldet werden. Legen Sie auf **true** fest, um die Berichterstellung zu aktivieren Legen Sie auf **false** fest, um die Berichterstellung zu deaktivieren

### <a name="sio_set_wfp_connection_redirect_records-opcode-setting-i-t3"></a>\_ \_ Datensätze der WFP- \_ \_ verbindungsumleitung in der Gruppe \_

Legt den Umleitungs Daten Satz auf den neuen TCP-Socket fest, der zum Herstellen der Verbindung mit dem endgültigen Ziel verwendet wird, um von einem WFP-Umleitungs Dienst (Windows Filtering Platform)

Die [**\_ \_ \_ \_ \_ Datensätze der WFP-Verbindungs Umleitung**](/previous-versions/windows/desktop/legacy/hh859714(v=vs.85)) werden im Rahmen der Proxy Verbindungs Nachverfolgung für umgeleitete Socketverbindungen im Rahmen der Verbindungs Nachverfolgung für die Verbindung mit der Diese WFP-Funktion ermöglicht das Nachverfolgen von Umleitungs Datensätzen von der anfänglichen Umleitung einer Verbindung zur endgültigen Verbindung zum Ziel.

Ausführlichere Informationen finden Sie in der Referenz zur Übersicht über die [**\_ \_ WFP- \_ Verbindungs \_ \_ Umleitung**](/previous-versions/windows/desktop/legacy/hh859714(v=vs.85)) in der Übersicht. **SIO \_ Festlegen der \_ WFP- \_ \_ verbindungsumleitungs- \_ Datensätze** wird unter Windows 8, Windows Server 2012 und höher unterstützt.

### <a name="sio_tcp_info-opcode-setting-i-o-t3"></a>SIO \_ TCP \_ Info (OpCode-Einstellung: I, O, T = = 3)

Ruft die TCP-Statistik für einen Socket ab. Die TCP-Statistiken werden in einer [**TCP- \_ Info \_ v0**](/windows/desktop/api/Mstcpip/ns-mstcpip-tcp_info_v0) -Struktur bereitgestellt.

Im Gegensatz zum Abrufen von TCP-Statistiken mit der [**getpertcpconnectionestats**](/windows/win32/api/iphlpapi/nf-iphlpapi-getpertcpconnectionestats) -Funktion ist es für das Abrufen von TCP-Statistiken mit diesem Steuerungs Code nicht erforderlich, dass der Benutzercode die TCP-Verbindungstabelle lädt, speichert und filtert und keine erhöhten Rechte für die Verwendung erforderlich ist.

Weitere Informationen finden Sie unter Informationen zu den in- [**\_ TCP-TCP \_**](/previous-versions/windows/desktop/legacy/mt823415(v=vs.85)). **SIO \_ TCP- \_ Informationen** werden unter Windows 10, Version 1703, Windows Server 2016 und höher unterstützt.

## <a name="remarks"></a>Bemerkungen

Winsock IOCTLs wird in einer Reihe von unterschiedlichen Header Dateien definiert. Hierzu gehören die Header Datei *Winsock2. h*, *mtauscht. h* und *MSTCPIP. h* .

Im Microsoft Windows Software Development Kit (SDK), das für Windows Vista und höher veröffentlicht wurde, hat sich die Organisation der Header Dateien geändert, und in den Header Dateien *Ws2def. h*, *Ws2ipdef. h* und *mtauscht* ist auch eine Reihe von Winsock IOCTLs definiert. Die Header Datei " *Ws2def. h* " wird automatisch von der *Winsock2. h* -Header Datei eingeschlossen. Die Header Datei " *Ws2ipdef. h* " wird automatisch von der *Ws2tcpip. h* -Header Datei eingeschlossen. Die Header Datei " *mtauschten sockdef. h* " ist automatisch in der Header Datei " *mtauscht. h* " enthalten.

## <a name="requirements"></a>Anforderungen

|||
|-|-|
| Header<br/> | <dl> <dt>Winsock2. h; </dt> <dt>MSTCPIP. h; </dt> <dt>Mtauscht. h; </dt> <dt>Mtausockdef. h unter Windows Vista, Windows Server 2008 und Windows 7 (Include mtausock. h); </dt> <dt>Ws2def. h unter Windows Vista, Windows Server 2008 und Windows 7 (Include Winsock2. h); </dt> <dt>Ws2ipdef. h unter Windows Vista, Windows Server 2008 und Windows 7 (Include Ws2tcpip. h)</dt> </dl> |
