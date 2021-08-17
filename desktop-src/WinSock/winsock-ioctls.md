---
description: Navigationsthema für Windows Sockets (Winsock)-Socket-IOCTLs.
ms.assetid: 6a63c2c9-4e09-4a62-b39f-3ccb26287da8
title: Winsock IOCTLs (Winsock2.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8d9c47e68433747e341bbc0a082b5d40af76403b473caabe3423f5a186f499f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117739950"
---
# <a name="winsock-ioctls"></a>Winsock-IOCTLs

In diesem Abschnitt werden Winsock Socket-Eingabe-/Ausgabesteuerelemente (IOCTLs) für verschiedene Editionen Windows Betriebssystemen beschrieben. Verwenden Sie [**die WSAIoctl-**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) oder [**WSPIoctl-Funktion,**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) um eine Winsock-IOCTL aus zu geben, um den Modus eines Sockets, des Transportprotokolls oder des Kommunikationssubsystems zu steuern.

Einige Winsock-IOCTLs erfordern mehr Erklärung, als in dieser Tabelle vermittelt werden kann. solche Optionen enthalten Links zu zusätzlichen Themen.

Es ist möglich, ein Codierungsschema zu übernehmen, das die aktuell definierten [**ioctlsocket-Opcodes**](/windows/desktop/api/winsock/nf-winsock-ioctlsocket) beibewahrt und gleichzeitig eine bequeme Möglichkeit bietet, den Opcodebezeichnerbereich so weit zu partitionieren, wie der *dwIoControlCode-Parameter* jetzt eine 32-Bit-Entität ist. Der *dwIoControlCode-Parameter* ist so aufgebaut, dass er protokoll- und herstellerunabhängig ist, wenn neue Steuerungscodes hinzugefügt werden, während gleichzeitig die Abwärtskompatibilität mit den Windows Sockets 1.1- und Unix-Steuerungscodes beibehalten wird. Der *dwIoControlCode-Parameter* hat das folgende Format.

| I  | O  | V  | T  | Anbieter-/Adressfamilie | Code                   |
|-|-|-|-|-|-|
| 3  | 3  | 2  | 2 2 | 2 2 2 2 2 2 2 1 1 1 1 | 1 1 1 1 1 1              |
| 1  | 0  | 9  | 8 7 | 6 5 4 3 2 1 0 9 8 7 6 | 5 4 3 2 1 0 9 8 7 6 5 4 3 2 1 0 |

> [!Note] 
> Die Bits im *dwIoControlCode-Parameter,* die in der Tabelle angezeigt werden, müssen nach Spalte vertikal von oben nach unten gelesen werden. Das linke Bit ist also Bit 31, das nächste Bit bit 30 und das am rechten Ende bit 0.

Ich wird festgelegt, wenn der Eingabepuffer für den Code gültig ist, wie bei **IOC_IN.**

O wird festgelegt, wenn der Ausgabepuffer für den Code gültig ist, wie bei **IOC_OUT.** Steuerungscodes, die sowohl Eingabe- als auch Ausgabepuffer verwenden, legen E und A fest.

V wird festgelegt, wenn keine Parameter für den Code wie bei **IOC_VOID.**

T ist eine 2-Bit-Menge, die den Typ der IOCTL definiert. Die folgenden Werte sind definiert:

0 IOCTL ist ein Unix-IOCTL-Standardcode wie **bei FIONREAD** und **FIONBIO.**

1 IOCTL ist ein generischer Windows Sockets 2-IOCTL-Code. Neue IOCTL-Codes, die für Windows Sockets 2 definiert sind, verfügen über T == 1.

2 Die IOCTL gilt nur für eine bestimmte Adressfamilie.

3 Die IOCTL gilt nur für den Anbieter eines bestimmten Anbieters, wie **bei IOC_VENDOR.** Dieser Typ ermöglicht es Unternehmen, eine Anbieternummer zu erhalten, die im **Parameter Vendor/Address family angezeigt** wird. Anschließend kann der Anbieter neue IOCTLs definieren, die für diesen Anbieter spezifisch sind, ohne die IOCTL bei einem Clearinghouse registrieren zu müssen, wodurch Anbieterflexibilität und Datenschutz bereitgestellt werden.

**Anbieter-/Adressfamilie** Eine 11-Bit-Menge, die den Anbieter definiert, der den Code besitzt (wenn T == 3) oder die die Adressfamilie enthält, auf die der Code angewendet wird (wenn T == 2). Wenn es sich um einen Unix IOCTL-Code (T == 0) handelt, hat dieser Parameter den gleichen Wert wie der Code unter Unix. Wenn es sich um eine generische Windows Sockets 2 IOCTL (T == 1) handelt, kann dieser Parameter als Erweiterung des Codeparameters verwendet werden, um zusätzliche Codewerte zur Verfügung zu stellen.

**Code** Die 16-Bit-Menge, die den spezifischen IOCTL-Code für den Vorgang enthält.

## <a name="unix-ioctl-codes"></a>Unix-IOCTL-Codes

Die folgenden Unix IOCTL-Codes (Befehle) werden unterstützt.

### <a name="fionbio"></a>FIONBIO

Aktivieren oder deaktivieren Sie den nicht blockierenden Modus für socket *s*. Der *lpvInBuffer-Parameter* zeigt auf einen long-Wert ohne Vorzeichen **(Unsigned Long,** QoS), der ungleich 0 (null) ist, wenn der nicht blockierende Modus aktiviert werden soll, und auf 0 (null), wenn er deaktiviert werden soll. Wenn ein Socket erstellt wird, wird er im Blockierungsmodus ausgeführt (d. h. der nicht blockierende Modus ist deaktiviert). Dies ist konsistent mit BSD-Sockets.

Die [**Routine WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) oder [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) legt einen Socket automatisch auf den nicht blockierenden Modus fest. Wenn **WSAAsyncSelect** oder **WSAEventSelect** für einen Socket ausgegeben wurde, wird bei jedem Versuch, [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) zum Festlegen des Sockets wieder in den Blockierungsmodus zu verwenden, WSAEINVAL fehlschlagen. Um den Socket wieder in den Blockierungsmodus zu setzen, muss eine Anwendung **zuerst WSAAsyncSelect** deaktivieren, indem **WSAAsyncSelect** mit dem *lEvent-Parameter* gleich 0 (null) oder **WSAEventSelect** durch Aufrufen von **WSAEventSelect** mit dem *Parameter lNetworkEvents* gleich 0 (null) aufgerufen wird.

### <a name="fionread"></a>FIONREAD

Bestimmen Sie die Menge der Daten, die atomisch aus socket s gelesen *werden können.* Der *lpvOutBuffer-Parameter* zeigt auf einen **long-Wert** ohne Vorzeichen, in dem [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) das Ergebnis speichert.

Wenn der im  s-Parameter übergebene Socket streamorientiert ist (z. B. sock STREAM), gibt FIONREAD die Gesamtmenge der Daten zurück, die in einem einzelnen Empfangsvorgang gelesen werden können. Dies ist normalerweise identisch mit der Gesamtmenge der Daten, die im Socket in die Warteschlange gestellt werden (da ein Datenstrom \_ byteorientiert ist, ist dies nicht garantiert). 

Wenn der im  s-Parameter übergebene Socket nachrichtenorientiert ist (z. B. typ SOCK DGRAM), gibt FIONREAD die Gesamtanzahl der zum Lesen verfügbaren Bytes zurück, nicht die Größe des ersten Datagramms (Nachricht), das in die Warteschlange des Sockets gestellt \_ wird. 

### <a name="siocatmark"></a>SIOCATMARK

Bestimmen Sie, ob alle OOB-Daten gelesen wurden. Dies gilt nur für einen Socket im Streamstil (z. B. typ SOCK STREAM), der für den Inlineempfang von \_ OOB-Daten (SO \_ OOBINLINE) konfiguriert wurde. Wenn keine OOB-Daten darauf warten, gelesen zu werden, gibt der Vorgang TRUE zurück. Andernfalls wird **FALSE zurückgegeben,** und der nächste Empfangsvorgang, der für den Socket ausgeführt wird, ruft einige oder alle Daten vor der Markierung ab. Die Anwendung sollte den **SIOCATMARK-Vorgang verwenden,** um zu bestimmen, ob noch welche übrig sind. Wenn den dringenden (Out-of-Band)-Daten normale Daten vorangehende sind, werden sie in der reihenfolgenfolge empfangen. (Beachten Sie, [**dass recv-Vorgänge**](/windows/desktop/api/winsock/nf-winsock-recv) niemals OOB- und normale Daten im selben Aufruf kombinieren.) *lpvOutBuffer* zeigt auf eine BOOL, in der [**WSAIoctl das**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) Ergebnis speichert.

## <a name="windows-sockets-2-commands"></a>Windows Sockets 2-Befehle

Die folgenden Windows Sockets 2-Befehle werden unterstützt.

### <a name="sio_acquire_port_reservation-opcode-setting-i-t3"></a>SIO_ACQUIRE_PORT_RESERVATION (Opcodeeinstellung: I, T==3)

Fordern Sie eine Laufzeitreservierung für einen Block von TCP- oder UDP-Ports an. Für Laufzeitportreservierungen erfordert der Portpool, dass Reservierungen aus dem Prozess verwendet werden, auf dessen Socket die Reservierung gewährt wurde. Laufzeitportreservierungen dauern nur so lange, wie die Lebensdauer des Sockets, auf dem [**die SIO \_ ACQUIRE PORT \_ \_ RESERVATION**](/previous-versions/windows/desktop/legacy/gg699720(v=vs.85)) IOCTL aufgerufen wurde. Im Gegensatz dazu können persistente Portreservierungen, die mit der [**CreatePersistentTcpPortReservation-**](/windows/win32/api/iphlpapi/nf-iphlpapi-createpersistenttcpportreservation) oder [**CreatePersistentUdpPortReservation-Funktion**](/windows/win32/api/iphlpapi/nf-iphlpapi-createpersistentudpportreservation) erstellt wurden, von jedem Prozess mit der Möglichkeit zum Abrufen persistenter Reservierungen verwendet werden.

Ausführlichere Informationen finden Sie in der [**Referenz zu SIO \_ ACQUIRE PORT \_ \_ RESERVATION.**](/previous-versions/windows/desktop/legacy/gg699720(v=vs.85))

[**SIO \_ ACQUIRE \_ PORT \_ RESERVATION**](/previous-versions/windows/desktop/legacy/gg699720(v=vs.85)) wird unter Windows Vista und neueren Versionen des Betriebssystems unterstützt.

### <a name="sio_address_list_change-opcode-setting-v-t1"></a>SIO \_ ADDRESS LIST CHANGE \_ \_ (Opcodeeinstellung: V, T==1)

Zum Empfangen von Benachrichtigungen über Änderungen in der Liste der lokalen Transportadressen der Protokollfamilie des Sockets, an die die Anwendung gebunden werden kann. Nach Abschluss dieser IOCTL werden keine Ausgabeinformationen bereitgestellt. Die Vervollständigung gibt lediglich an, dass sich die Liste der verfügbaren lokalen Adressen geändert hat und erneut über **SIO \_ ADDRESS LIST QUERY \_ abgefragt \_ werden sollte.**

Es wird davon ausgegangen (obwohl nicht erforderlich), dass die Anwendung überlappende E/A verwendet, um nach Abschluss der **SIO \_ ADDRESS LIST \_ \_ CHANGE-Anforderung** über Änderungen benachrichtigt zu werden. Wenn die SIO ADDRESS **\_ LIST \_ \_ CHANGE** IOCTL für einen nicht blockierenden Socket und ohne überlappende Parameter ausgegeben wird *(lpOverlapped* lpCompletionRoutine sind auf NULL festgelegt), wird sie sofort mit dem Fehler /   [WSAEWOULDBLOCK](windows-sockets-error-codes-2.md)abgeschlossen.  Die Anwendung kann dann durch einen Aufruf von [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) oder [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) mit in der Bitmaske des Netzwerkereignisses festgelegtem FD ADDRESS LIST CHANGE-Bit auf Änderungsereignisse der Adressliste \_ \_ \_ warten.

### <a name="sio_address_list_query-opcode-setting-o-t1"></a>SIO \_ ADDRESS LIST QUERY \_ \_ (Opcodeeinstellung: O, T==1)

Erhält eine Liste der lokalen Transportadressen der Protokollfamilie des Sockets, an die die Anwendung gebunden werden kann. Die Liste der Adressen variiert je nach Adressfamilie, und einige Adressen werden aus der Liste ausgeschlossen.

> [!Note] 
> In Windows Plug-n-Play-Umgebungen können Adressen dynamisch hinzugefügt und entfernt werden. Daher können Sich Anwendungen nicht darauf verlassen, dass die von **SIO \_ ADDRESS LIST \_ \_ QUERY** zurückgegebenen Informationen persistent sind. Anwendungen können sich für Adressänderungsbenachrichtigungen über die **SIO \_ ADDRESS LIST \_ \_ CHANGE** IOCTL registrieren, die Benachrichtigungen über überlappende E/A- oder FD ADDRESS \_ LIST \_ \_ CHANGE-Ereignisse bietet. Die folgende Aktionssequenz kann verwendet werden, um zu gewährleisten, dass die Anwendung immer über aktuelle Adresslisteninformationen verfügt:

-  Issue **SIO \_ ADDRESS \_ LIST \_ CHANGE** IOCTL
-  Issue **SIO \_ ADDRESS \_ LIST \_ QUERY** IOCTL
-  Wenn **SIO \_ ADDRESS LIST \_ \_ CHANGE** IOCTL die Anwendung der Änderung der Adressliste benachrichtigt (entweder durch überlappende E/A oder durch Signalisierung des Ereignisses FD ADDRESS LIST CHANGE), sollte die gesamte Sequenz von Aktionen wiederholt \_ \_ \_ werden.

Ausführlichere Informationen finden Sie in der [**Referenz zu SIO \_ ADDRESS LIST \_ \_ QUERY.**](/previous-versions/windows/desktop/legacy/dd877219(v=vs.85)) **SIO \_ ADDRESS \_ LIST \_ QUERY** wird ab Windows 2000 unterstützt.

### <a name="sio_apply_transport_setting-opcode-setting-i-t3"></a>SIO \_ APPLY TRANSPORT SETTING \_ \_ (Opcodeeinstellung: I, T==3)

Wendet eine Transporteinstellung auf einen Socket an. Die angewendete Transporteinstellung basiert auf der [**TRANSPORT \_ SETTING \_ ID,**](/windows/win32/api/transportsettingcommon/ns-transportsettingcommon-transport_setting_id) die im *lpvInBuffer-Parameter übergeben* wird.

Die einzige Transporteinstellung, die derzeit definiert wird, ist für die **FUNKTION REAL TIME NOTIFICATION \_ \_ \_ CAPABILITY** auf einem TCP-Socket.

Wenn für die übergebene [**TRANSPORT \_ SETTING \_ ID**](/windows/win32/api/transportsettingcommon/ns-transportsettingcommon-transport_setting_id) der **GUID-Member** auf **REAL TIME NOTIFICATION \_ \_ \_ CAPABILITY** festgelegt ist, ist dies eine Anforderung zum Anwenden von Echtzeitbenachrichtigungseinstellungen für den TCP-Socket, der mit [**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) zum Empfangen von Netzwerkbenachrichtigungen im Hintergrund in einer Windows Store-App verwendet wird.

Ausführlichere Informationen finden Sie in der [**Referenz zu SIO \_ APPLY TRANSPORT \_ \_ SETTING.**](/previous-versions/windows/desktop/legacy/jj553481(v=vs.85)) **SIO \_ APPLY \_ TRANSPORT \_ SETTING** wird für Windows 8, Windows Server 2012 und höher unterstützt.

### <a name="sio_associate_handle-opcode-setting-i-t1"></a>SIO \_ ASSOCIATE \_ HANDLE (Opcodeeinstellung: I, T==1)

Ordnet diesen Socket dem angegebenen Handle einer Begleitschnittstelle zu. Der Eingabepuffer enthält den ganzzahligen Wert, der der Manifestkonst constant für die Begleitschnittstelle entspricht (z. B. TH \_ NETDEV und TH TAPI.), gefolgt von einem Wert, der ein Handle der angegebenen Begleitschnittstelle ist, sowie alle anderen erforderlichen \_ Informationen. Einzelheiten zu einer bestimmten Begleitschnittstelle finden Sie im entsprechenden Abschnitt unter [Winsock-](winsock-annexes.md) Datenbank. Die Gesamtgröße wird in der Eingabepufferlänge widergespiegelt. Es ist kein Ausgabepuffer erforderlich. Der [WSAENOPROTOOPT-Fehlercode](windows-sockets-error-codes-2.md) wird für Dienstanbieter angezeigt, die diese IOCTL nicht unterstützen. Das dieser IOCTL zugeordnete Handle kann mithilfe von **SIO \_ TRANSLATE HANDLE abgerufen \_ werden.**

Eine Begleitschnittstelle kann beispielsweise verwendet werden, wenn ein bestimmter Anbieter (1) viele zusätzliche Steuerelemente über das Verhalten eines Sockets bietet und (2) die Steuerelemente anbieterspezifisch genug sind, dass sie nicht vorhandenen Windows Socket-Funktionen oder denen, die wahrscheinlich in der Zukunft definiert werden, zuordnen. Es wird empfohlen, die Component Object Model (COM) anstelle dieser IOCTL zu verwenden, um andere Schnittstellen zu finden und zu verfolgen, die möglicherweise von einem Socket unterstützt werden. Diese IOCTL ist für (umgekehrte) Kompatibilität mit Systemen vorhanden, bei denen COM nicht verfügbar ist oder aus einem anderen Grund nicht verwendet werden kann.

### <a name="sio_associate_port_reservation-opcode-setting-i-t3"></a>SIO \_ ASSOCIATE PORT RESERVATION \_ \_ (Opcodeeinstellung: I, T==3)

Ordnen Sie einen Socket einer persistenten oder Laufzeitreservierung für einen Block von TCP- oder UDP-Ports zu, die durch das Portreservierungstoken identifiziert werden. Die [**SIO \_ ASSOCIATE PORT \_ \_ RESERVATION**](/previous-versions/windows/desktop/legacy/gg699721(v=vs.85)) IOCTL muss ausgegeben werden, bevor der Socket gebunden wird. Wenn und wenn der Socket gebunden ist, wird der ihm zugewiesene Port aus der Portreservierung ausgewählt, die vom angegebenen Token identifiziert wird. Wenn keine Ports aus der angegebenen Reservierung verfügbar sind, ist [**der Aufruf der Bindungsfunktion**](/windows/desktop/api/winsock/nf-winsock-bind) nicht möglich.

Ausführlichere Informationen finden Sie in der [**Referenz zu SIO \_ ASSOCIATE PORT \_ \_ RESERVATION.**](/previous-versions/windows/desktop/legacy/gg699721(v=vs.85))

[**SIO \_ ASSOCIATE \_ PORT \_ RESERVATION**](/previous-versions/windows/desktop/legacy/gg699721(v=vs.85)) wird unter Windows Vista und neueren Versionen des Betriebssystems unterstützt.

### <a name="sio_base_handle-opcode-setting-o-t1"></a>SIO \_ BASE \_ HANDLE (Opcodeeinstellung: O, T==1)

Ruft das Handle des Basisdienstanbieters für einen bestimmten Socket ab. Der zurückgegebene Wert ist ein **SOCKET.**

Ein mehrschichtiger Dienstanbieter würde diese IOCTL nie abfangen, da der Rückgabewert das Sockethandles des Basisdienstanbieters sein muss.

Wenn der Ausgabepuffer für ein Sockethandles nicht groß genug ist *(cbOutBuffer* ist kleiner als die Größe eines **SOCKETs),** oder der *lpvOutBuffer-Parameter* ein **NULL-Zeiger** ist, wird **SOCKET \_ ERROR** als Ergebnis dieser IOCTL zurückgegeben, und [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) gibt [WSAEFAULT zurück.](windows-sockets-error-codes-2.md)

**SIO \_ BASE \_ HANDLE** wird in der *Headerdatei "Mswsock.h"* definiert und auf Windows Vista und höher unterstützt.

### <a name="sio_bsp_handle-opcode-setting-o-t1"></a>SIO \_ BSP \_ HANDLE (Opcodeeinstellung: O, T==1)

Ruft das Handle des Basisdienstanbieters für einen Socket ab, der von der [**WSASendMsg-Funktion verwendet**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) wird. Der zurückgegebene Wert ist ein **SOCKET.**

Diese Ioctl wird von einem mehrschichtigen Dienstanbieter verwendet, um sicherzustellen, dass der Anbieter die [**WSASendMsg-Funktion abfing.**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg)

Wenn der Ausgabepuffer für ein Sockethandles nicht groß genug ist *(cbOutBuffer* ist kleiner als die Größe eines **SOCKETs),** oder der *lpvOutBuffer-Parameter* ein **NULL-Zeiger** ist, wird **SOCKET \_ ERROR** als Ergebnis dieser IOCTL zurückgegeben, und [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) gibt [WSAEFAULT zurück.](windows-sockets-error-codes-2.md)

**SIO \_ BSP \_ HANDLE** wird in der *Headerdatei "Mswsock.h"* definiert und auf Windows Vista und höher unterstützt.

### <a name="sio_bsp_handle_select-opcode-setting-o-t1"></a>SIO \_ BSP \_ HANDLE SELECT \_ (Opcodeeinstellung: O, T==1)

Ruft das Handle des Basisdienstanbieters für einen Socket ab, der von der [**select-Funktion verwendet**](/windows/desktop/api/Winsock2/nf-winsock2-select) wird. Der zurückgegebene Wert ist ein **SOCKET.**

Diese Ioctl wird von einem mehrschichtigen Dienstanbieter verwendet, um sicherzustellen, dass der Anbieter die [**Select-Funktion abfing.**](/windows/desktop/api/Winsock2/nf-winsock2-select)

Wenn der Ausgabepuffer für ein Sockethandles nicht groß genug ist *(cbOutBuffer* ist kleiner als die Größe eines **SOCKETs),** oder der *lpvOutBuffer-Parameter* ein **NULL-Zeiger** ist, wird **SOCKET \_ ERROR** als Ergebnis dieser IOCTL zurückgegeben, und [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) gibt [WSAEFAULT zurück.](windows-sockets-error-codes-2.md)

**SIO \_ BSP \_ HANDLE \_ SELECT** wird in der *Headerdatei "Mswsock.h"* definiert und auf Windows Vista und höher unterstützt.

### <a name="sio_bsp_handle_poll-opcode-setting-o-t1"></a>SIO \_ BSP \_ HANDLE POLL \_ (Opcodeeinstellung: O, T==1)

Ruft das Basis-Dienstanbieterhandle für einen Socket ab, der von der [**WSAPoll-Funktion verwendet**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) wird. Der *lpOverlapped-Parameter* muss ein **NULL-Zeiger** sein. Der zurückgegebene Wert ist ein **SOCKET.**

Diese Ioctl wird von einem mehrschichtigen Dienstanbieter verwendet, um sicherzustellen, dass der Anbieter die [**WSAPoll-Funktion abfing.**](/windows/win32/api/winsock2/nf-winsock2-wsapoll)

Wenn der Ausgabepuffer für ein Sockethandles nicht groß genug ist *(cbOutBuffer* ist kleiner als die Größe eines **SOCKETs),** ist der *lpvOutBuffer-Parameter* ein **NULL-Zeiger,** oder der *lpOverlapped-Parameter* ist kein **NULL-Zeiger,** wird SOCKET **\_ ERROR** als Ergebnis dieser IOCTL zurückgegeben, und [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) gibt [WSAEFAULT zurück.](windows-sockets-error-codes-2.md)

**SIO \_ BSP \_ HANDLE \_ POLL** wird in der *Headerdatei "Mswsock.h"* definiert und auf Windows Vista und höher unterstützt.

### <a name="sio_chk_qos-opcode-setting-i-o-t3"></a>SIO \_ CHK \_ QOS (Opcodeeinstellung: I, O, T==3)

Ruft Informationen zu QoS-Datenverkehrsmerkmalen ab. Während der Übergangsphase des Sendesystems zwischen dem Einrichten des Datenflusses und dem Empfang einer RESV-Nachricht (weitere Informationen zur Übergangsphase finden Sie unter Aufrufen des TC durch den [RSVP-Dienst),](/previous-versions/windows/desktop/qos/how-the-rsvp-service-invokes-tc) wird der einem RSVP-Flow zugeordnete Datenverkehr basierend auf dem Diensttyp[(BEST EFFORT,](/previous-versions/windows/desktop/qos/best-effort) [CONTROLLED LOAD](/previous-versions/windows/desktop/qos/controlled-load)oder [GUARANTEED) gestaltet.](/previous-versions/windows/desktop/qos/guaranteed) Weitere Informationen finden Sie unter Using SIO CHK QOS (Verwenden von [SIO \_ CHK \_ QOS)](/previous-versions/windows/desktop/qos/using-sio-chk-qos) im Quality of Service [Des](/previous-versions/windows/desktop/qos/qos-start-page) Platform SDK.

### <a name="sio_cpu_affinity-opcode-setting-i-t3"></a>SIO_CPU_AFFINITY (Opcodeeinstellung: I, T==3)

Aktiviert die Portfreigabe und die Empfangsanzeigeparallelisierung. Wenn Ihre Anwendung diese Socketoption verwendet, um Sockets verschiedenen Prozessoren zu zuordnen, und dann die Sockets an die gleiche Adresse bindet, werden Empfangsanzeigen basierend auf dem RSS-Hash (Receive Side Scaling) auf die Sockets verteilt. Die RSS-Einstellungen ändern sich nicht, sodass jeder Flow (lokaler Endpunkt, Remoteendpunktpaar) immer auf demselben Prozessor angegeben wird. Daher werden alle Pakete, die zu einem bestimmten Flow gehören, an denselben Socket angezeigt. Diese IOCTL muss vor der Bindung aufgerufen werden, andernfalls wird WSAEINVAL zurückgegeben. Der Eingabepuffer ist ein Prozessorindex (0-basiert) vom Typ USHORT. IOCTL ist nicht kompatibel mit SO_REUSEADDR und SO_REUSE_MULTICASTPORT. Wird nur für UDP-Sockets unterstützt.

> [!NOTE]
> Wenn Sie version 10.0.19041.0 (Windows 10, Version 2004) des Windows SDK als Ziel verwenden, verwenden Sie den Wert anstelle des Namens `0x98000015` **SIO_CPU_AFFINITY**.

### <a name="sio_enable_circular_queueing-opcode-setting-v-t1"></a>SIO \_ ENABLE \_ CIRCULAR \_ QUEUEING (Opcodeeinstellung: V, T==1)

Gibt für den zugrunde liegenden nachrichtenorientierten Dienstanbieter an, dass eine neu eingetroffene Nachricht aufgrund eines Pufferwarteschlangenüberlaufs nie gelöscht werden soll. Stattdessen sollte die älteste Nachricht in der Warteschlange entfernt werden, um die neu eingetroffene Nachricht aufnehmen zu können. Es sind keine Eingabe- und Ausgabepuffer erforderlich. Beachten Sie, dass diese IOCTL nur für Sockets gültig ist, die unzuverlässigen, nachrichtenorientierten Protokollen zugeordnet sind. Der [WSAENOPROTOOPT-Fehlercode](windows-sockets-error-codes-2.md) wird für Dienstanbieter angezeigt, die diese IOCTL nicht unterstützen.

### <a name="sio_find_route-opcode-setting-o-t1"></a>SIO \_ FIND \_ ROUTE (Opcodeeinstellung: O, T==1)

Bei der Ausgabe fordert diese IOCTL an, dass die Route zur Remoteadresse, die als [**Sockaddr**](sockaddr-2.md) im Eingabepuffer angegeben ist, gefunden wird. Wenn die Adresse bereits im lokalen Cache vorhanden ist, wird ihr Eintrag ungültig. Im Fall von "IPX" initiiert dieser Aufruf ein IPX GetLocalTarget (GLT), das das Netzwerk nach der angegebenen Remoteadresse abfragt.

### <a name="sio_flush-opcode-setting-v-t1"></a>SIO \_ FLUSH (Opcodeeinstellung: V, T==1)

Verwirft den aktuellen Inhalt der sendeenden Warteschlange, die diesem Socket zugeordnet ist. Es sind keine Eingabe- und Ausgabepuffer erforderlich. Der [WSAENOPROTOOPT-Fehlercode](windows-sockets-error-codes-2.md) wird für Dienstanbieter angezeigt, die diese IOCTL nicht unterstützen.

### <a name="sio_get_broadcast_address-opcode-setting-o-t1"></a>SIO \_ GET BROADCAST ADDRESS \_ \_ (Opcodeeinstellung: O, T==1)

Diese IOCTL füllt den Ausgabepuffer mit einer [Sockaddr-Struktur](sockaddr-2.md) auf, die eine geeignete Broadcastadresse für die Verwendung mit [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto) /  [**WSASendTo enthält.**](/windows/desktop/api/Winsock2/nf-winsock2-wsasendto) Diese IOCTL wird für IPv6-Sockets nicht unterstützt und gibt den [WSAENOPROTOOPT-Fehlercode](windows-sockets-error-codes-2.md) zurück.

### <a name="sio_get_extension_function_pointer-opcode-setting-o-i-t1"></a>SIO \_ GET EXTENSION FUNCTION \_ \_ \_ POINTER (Opcodeeinstellung: O, I, T==1)

Rufen Sie einen Zeiger auf die angegebene Erweiterungsfunktion ab, die vom zugeordneten Dienstanbieter unterstützt wird. Der Eingabepuffer enthält einen global eindeutigen Bezeichner **(GUID),** dessen Wert die in Frage stellende Erweiterungsfunktion identifiziert. Der Zeiger auf die gewünschte Funktion wird im Ausgabepuffer zurückgegeben. Erweiterungsfunktionsbezeichner werden von Dienstanbieteranbietern eingerichtet und sollten in der Herstellerdokumentation enthalten sein, in der Funktionen und Semantik von Erweiterungsfunktionen beschrieben werden.

Die GUID-Werte für Erweiterungsfunktionen, die Windows TCP/IP-Dienstanbieter unterstützt werden, werden in der *Headerdatei "Mswsock.h"* definiert. Der mögliche Wert für diese GUIDs lautet wie folgt:

| Begriff                                                                                                                | BESCHREIBUNG                                                                               |
|-|-|
| <span id="WSAID_ACCEPTEX"></span><span id="wsaid_acceptex"></span>WSAID \_ ACCEPTEX<br/>                                     | Die [**AcceptEx-Erweiterungsfunktion.**](/windows/win32/api/mswsock/nf-mswsock-acceptex)<br/>                         |
| <span id="WSAID_CONNECTEX"></span><span id="wsaid_connectex"></span>WSAID \_ CONNECTEX<br/>                                  | Die [**ConnectEx-Erweiterungsfunktion.**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex) <br/>                      |
| <span id="WSAID_DISCONNECTEX"></span><span id="wsaid_disconnectex"></span>WSAID \_ DISCONNECTEX<br/>                         | Die [**DisconnectEx-Erweiterungsfunktion.**](/previous-versions/windows/desktop/legacy/ms737757(v=vs.85)) <br/>                |
| <span id="WSAID_GETACCEPTEXSOCKADDRS"></span><span id="wsaid_getacceptexsockaddrs"></span>WSAID \_ GETACCEPTEXSOCKADDRS<br/> | Die [**Erweiterungsfunktion GetAcceptExSockaddrs.**](/windows/win32/api/mswsock/nf-mswsock-getacceptexsockaddrs)<br/> |
| <span id="WSAID_TRANSMITFILE"></span><span id="wsaid_transmitfile"></span>\_WSAID-ÜBERTRAGUNGSDATEI<br/>                         | Die [**TransmitFile-Erweiterungsfunktion.**](/windows/win32/api/mswsock/nf-mswsock-transmitfile)<br/>                 |
| <span id="WSAID_TRANSMITPACKETS"></span><span id="wsaid_transmitpackets"></span>\_WSAID-TRANSMITPACKETS<br/>                | Die [**TransmitPackets-Erweiterungsfunktion.**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_transmitpackets) <br/>          |
| <span id="WSAID_WSARECVMSG"></span><span id="wsaid_wsarecvmsg"></span>WSAID \_ WSARECVMSG<br/>                               | Die [**LPFN_WSARECVMSG -Erweiterungsfunktion (WSARecvMsg).**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)<br/>                     |
| <span id="WSAID_WSASENDMSG"></span><span id="wsaid_wsasendmsg"></span>WSAID \_ WSASENDMSG<br/>                               | Die [**WSASendMsg-Erweiterungsfunktion.**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) <br/>                      |

### <a name="sio_get_group_qos-opcode-setting-o-i-t1"></a>SIO \_ GET \_ GROUP \_ QOS (Opcodeeinstellung: O, I, T==1)

Für die zukünftige Verwendung mit Sockets reserviert.

Rufen Sie die [**QOS-Struktur**](/windows/win32/api/winsock2/ns-winsock2-qos) ab, die der Socketgruppe zugeordnet ist, zu der dieser Socket gehört. Der Eingabepuffer ist optional. Einige Protokolle (z. B. RSVP) ermöglichen die Verwendung des Eingabepuffers, um eine Servicequalitätsanforderung zu qualifizieren. Die **QOS-Struktur** wird in den Ausgabepuffer kopiert. Wenn dieser Socket nicht zu einer entsprechenden Socketgruppe gehört, werden die **SendingFlowspec-** und **ReceivingFlowspec-Member** der zurückgegebenen **QOS-Struktur** auf **NULL festgelegt.** Der [WSAENOPROTOOPT-Fehlercode](windows-sockets-error-codes-2.md) wird für Dienstanbieter angegeben, die die Servicequalität nicht unterstützen.

### <a name="sio_get_interface_list-opcode-setting-o-t0"></a>SIO \_ GET INTERFACE LIST \_ \_ (Opcodeeinstellung: O, T==0)

Gibt eine Liste der konfigurierten IP-Schnittstellen und deren Parameter als Array von [**INTERFACE \_ INFO-Strukturen**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-interface_info) zurück.

> [!Note]  
> Die Unterstützung dieses Befehls ist für Windows Sockets 2-kompatible TCP/IP-Dienstanbieter obligatorisch.

Der *lpvOutBuffer-Parameter* zeigt auf den Puffer, in dem die Informationen zu Schnittstellen als Array von [**INTERFACE \_ INFO-Strukturen**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-interface_info) für Unicast-IP-Adressen auf den Schnittstellen gespeichert werden. Der *cbOutBuffer-Parameter* gibt die Länge des Ausgabepuffers an. Die Anzahl der zurückgegebenen Schnittstellen (Anzahl der im Puffer zurückgegebenen Strukturen, auf die der *lpvOutBuffer-Parameter* zeigt) kann basierend auf der tatsächlichen Länge des Ausgabepuffers bestimmt werden, der im *lpcbBytesReturned-Parameter* zurückgegeben wird.

Wenn die [**WSAIoctl-Funktion**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) mit **SIO \_ GET INTERFACE \_ \_ LIST**  aufgerufen wird und der Level-Member des Sockets s-Parameters nicht als **IPPROTO \_ IP** definiert ist, wird **WSAEINVAL** zurückgegeben. Ein Aufruf der **WSAIoctl-Funktion** mit **SIO \_ GET INTERFACE \_ \_ LIST** gibt **WSAEFAULT** zurück, wenn der *cbOutBuffer-Parameter,* der die Länge des Ausgabepuffers angibt, zu klein ist, um die Liste der konfigurierten Schnittstellen zu empfangen.

**SIO \_ GET \_ INTERFACE \_ LIST** wird unter Windows Me/98 und Windows NT 4.0 mit SP4 und höher unterstützt.

### <a name="sio_get_interface_list_ex-opcode-setting-o-t0"></a>SIO \_ GET INTERFACE LIST EX \_ \_ \_ (Opcodeeinstellung: O, T==0)

Für die zukünftige Verwendung mit Sockets reserviert.

Gibt eine Liste der konfigurierten IP-Schnittstellen und deren Parameter als Array von [**INTERFACE \_ INFO \_ EX-Strukturen**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-interface_info_ex) zurück.

Der *lpvOutBuffer-Parameter* zeigt auf den Puffer, in dem die Informationen zu Schnittstellen als Array von [**INTERFACE INFO \_ \_ EX-Strukturen**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-interface_info_ex) für Unicast-IP-Adressen auf der Schnittstelle gespeichert werden. Der *cbOutBuffer-Parameter* gibt die Länge des Ausgabepuffers an. Die Anzahl der zurückgegebenen Schnittstellen (Anzahl der in *lpvOutBuffer* zurückgegebenen Strukturen) kann basierend auf der tatsächlichen Länge des Ausgabepuffers bestimmt werden, der im *lpcbBytesReturned-Parameter zurückgegeben* wird.

**SIO \_ GET \_ INTERFACE \_ LIST \_ EX** wird derzeit nicht auf Windows.

### <a name="sio_get_qos-opcode-setting-o-t1"></a>SIO \_ GET \_ QOS (Opcodeeinstellung: O, T==1)

Für die zukünftige Verwendung mit Sockets reserviert. Rufen Sie die [**QOS-Struktur**](/windows/win32/api/winsock2/ns-winsock2-qos) ab, die dem Socket zugeordnet ist. Der Eingabepuffer ist optional. Einige Protokolle (z. B. RSVP) ermöglichen die Verwendung des Eingabepuffers, um eine Servicequalitätsanforderung zu qualifizieren. Die **QOS-Struktur** wird in den Ausgabepuffer kopiert. Der Ausgabepuffer muss groß genug sein, um die vollständige **QOS-Struktur enthalten zu** können. Der [WSAENOPROTOOPT-Fehlercode](windows-sockets-error-codes-2.md) wird für Dienstanbieter angegeben, die die Servicequalität nicht unterstützen.

Ein Absender darf **SIO \_ GET \_ QOS** erst aufrufen, wenn der Socket verbunden ist.

Ein Empfänger kann **SIO \_ GET \_ QOS aufrufen,** sobald er gebunden ist.

### <a name="sio_get_tx_timestamp"></a>SIO_GET_TX_TIMESTAMP

Eine Socket-IOCTL, die verwendet wird, um Zeitstempel für übertragene Pakete (TX) zu erhalten. Nur für Datagrammsockets gültig.

Der  SIO_GET_TX_TIMESTAMP-Steuerelementcode entfernt einen Übertragungszeitstempel aus der Übertragungszeitstempelwarteschlange eines Sockets. Aktivieren Sie zuerst den Zeitstempelempfang, indem [**Sie**](#sio_timestamping) SIO_TIMESTAMPING Socket-IOCTL verwenden. Rufen Sie dann tx-Zeitstempel nach ID ab, indem Sie die [**WSAIoctl-Funktion**](/windows/win32/api/winsock2/nf-winsock2-wsaioctl) (oder [**WSPIoctl**](/previous-versions/windows/hardware/network/ff566296(v=vs.85))) mit den folgenden Parametern aufrufen.

Für **SIO_GET_TX_TIMESTAMP** ist die Eingabe eine UINT32-Zeitstempel-ID, und die Ausgabe ist ein **UINT64-Zeitstempelwert.**  Bei Erfolg ist der tx-Zeitstempel verfügbar und wird zurückgegeben. Wenn keine Übertragungszeitstempel verfügbar sind, gibt [**WSAGetLastError**](/windows/win32/api/winsock/nf-winsock-wsagetlasterror) **WSAEWOULDBLOCK zurück.**

> [!NOTE]
> TX-Zeitstempel werden nicht unterstützt, wenn ein zusammenfingiertes Senden **über** UDP_SEND_MSG_SIZE.

Siehe auch [Winsock-Zeitstempel.](/windows/win32/winsock/winsock-timestamping)

### <a name="sio_ideal_send_backlog_change-opcode-setting-v-t0"></a>SIO \_ IDEAL SEND BACKLOG CHANGE \_ \_ \_ (Opcodeeinstellung: V, T==0)

Benachrichtigt eine Anwendung, wenn sich der ideale WERT für den Senderückstand (ISB) für die zugrunde liegende Verbindung ändert.

Beim Senden von Daten über eine TCP-Verbindung mithilfe von Windows-Sockets ist es wichtig, eine ausreichende Menge an ausstehenden (gesendeten, aber noch nicht bestätigten) Daten in TCP zu behalten, um den höchsten Durchsatz zu erzielen. Der ideale Wert für die menge der ausstehenden Daten, um den besten Durchsatz für die TCP-Verbindung zu erzielen, wird als ideale GRÖßE des Senderückstands (SEND Backlog, ISB) bezeichnet. Der ISB-Wert ist eine Funktion des Bandbreitenverzögerungsprodukts der TCP-Verbindung und des angekündigten Empfangsfensters des Empfängers (und teilweise der Überlastung im Netzwerk).

Der ISB-Wert pro Verbindung ist über die TCP-Protokollimplementierung in Windows Server 2008, Windows Vista mit SP1 und neueren Versionen des Betriebssystems verfügbar. Die **SIO \_ IDEAL SEND BACKLOG \_ \_ \_ CHANGE** IOCTL kann von einer Anwendung verwendet werden, um Benachrichtigungen zu erhalten, wenn sich der ISB-Wert für eine Verbindung dynamisch ändert.

Ausführlichere Informationen finden Sie in der [**Referenz zu SIO \_ IDEAL SEND BACKLOG \_ \_ \_ CHANGE.**](/previous-versions/windows/desktop/legacy/bb736548(v=vs.85))

[**SIO \_ IDEAL \_ SEND \_ BACKLOG \_ CHANGE**](/previous-versions/windows/desktop/legacy/bb736548(v=vs.85)) wird auf Windows Server 2008, Windows Vista mit SP1 und neueren Versionen des Betriebssystems unterstützt.

### <a name="sio_ideal_send_backlog_query-opcode-setting-o-t0"></a>SIO \_ IDEAL SEND BACKLOG QUERY \_ \_ \_ (Opcodeeinstellung: O, T==0)

Ruft den idealen ISB-Wert (Send Backlog) für die zugrunde liegende Verbindung ab.

Beim Senden von Daten über eine TCP-Verbindung mithilfe von Windows-Sockets ist es wichtig, eine ausreichende Menge an ausstehenden (gesendeten, aber noch nicht bestätigten) Daten in TCP zu behalten, um den höchsten Durchsatz zu erzielen. Der ideale Wert für die menge der ausstehenden Daten, um den besten Durchsatz für die TCP-Verbindung zu erzielen, wird als ideale GRÖßE des Senderückstands (SEND Backlog, ISB) bezeichnet. Der ISB-Wert ist eine Funktion des Bandbreitenverzögerungsprodukts der TCP-Verbindung und des angekündigten Empfangsfensters des Empfängers (und teilweise der Überlastung im Netzwerk).

Der ISB-Wert pro Verbindung ist über die TCP-Protokollimplementierung in Windows Server 2008 und höher verfügbar. Die **SIO \_ IDEAL SEND BACKLOG \_ \_ \_ QUERY** IOCTL kann von einer Anwendung verwendet werden, um den ISB-Wert für eine Verbindung abfragt.

Ausführlichere Informationen finden Sie in der [**Referenz zu SIO \_ IDEAL SEND BACKLOG \_ \_ \_ QUERY.**](/previous-versions/windows/desktop/legacy/bb736549(v=vs.85))

[**SIO \_ IDEAL \_ SEND \_ BACKLOG \_ QUERY**](/previous-versions/windows/desktop/legacy/bb736549(v=vs.85)) wird auf Windows Server 2008, Windows Vista mit SP1 und neueren Versionen des Betriebssystems unterstützt.

### <a name="sio_keepalive_vals-opcode-setting-i-t3"></a>SIO \_ KEEPALIVE \_ VALS (Opcodeeinstellung: I, T==3)

Aktiviert oder deaktiviert die Verbindungseinstellung der **TCP-Keep-Alive-Option,** die das TCP-Keep-Alive-Timeout und -Intervall angibt. Weitere Informationen zur Keep-Alive-Option finden Sie in Abschnitt 4.2.3.6 des Themas *Requirements for Internet Hosts – Communication Layers specified* in RFC 1122 available at the IETF website (Anforderungen für Internethosts – Kommunikationsebenen gemäß RFC 1122), die auf der [IETF-Website](https://www.ietf.org/rfc/rfc1122.txt)verfügbar sind. (Diese Ressource ist möglicherweise nur auf Englisch verfügbar.)

**SIO \_ KEEPALIVE \_ VALS** kann verwendet werden, um Keep-Alive-Tests zu aktivieren oder zu deaktivieren und das Keep-Alive-Timeout und das Keep-Alive-Intervall zu festlegen. Das Keep-Alive-Timeout gibt das Timeout in Millisekunden ohne Aktivität an, bis das erste Keep-Alive-Paket gesendet wird. Das Keep-Alive-Intervall gibt das Intervall in Millisekunden an, zwischen dem aufeinander folgende Keep-Alive-Pakete gesendet werden, wenn keine Bestätigung empfangen wird.

Die [**SO \_ KEEPALIVE-Option,**](so-keepalive.md) bei der es sich um eine der [ \_ SOL-Socketsocketoptionen](sol-socket-socket-options.md)handelt, kann auch zum Aktivieren oder Deaktivieren des TCP-Keep-Alive für eine Verbindung sowie zum Abfragen des aktuellen Status dieser Option verwendet werden. Um zu abfragen, ob TCP-Keep-Alive für einen Socket aktiviert ist, kann die [**getsockopt-Funktion**](/windows/desktop/api/winsock/nf-winsock-getsockopt) mit der **SO \_ KEEPALIVE-Option aufgerufen** werden. Um TCP-Keep-Alive zu aktivieren oder zu deaktivieren, kann die [**setsockopt-Funktion**](/windows/desktop/api/winsock/nf-winsock-setsockopt) mit der [**SO \_ KEEPALIVE-Option aufgerufen**](so-keepalive.md) werden. Wenn TCP Keep-Alive mit **SO \_ KEEPALIVE** aktiviert ist, werden die TCP-Standardeinstellungen für Keep-Alive-Timeout und -Intervall verwendet, es sei denn, diese Werte wurden mithilfe von **SIO \_ KEEPALIVE \_ VALS geändert.**

Ausführlichere Informationen finden Sie in der [**Referenz zu SIO \_ KEEPALIVE \_ VALS.**](/previous-versions/windows/desktop/legacy/dd877220(v=vs.85)) **SIO \_ KEEPALIVE \_ VALS** wird ab Windows 2000 unterstützt.

### <a name="sio_loopback_fast_path-opcode-setting-i-t3"></a>SIO \_ LOOPBACK \_ FAST PATH \_ (Opcodeeinstellung: I, T==3)

Konfiguriert einen TCP-Socket für geringere Latenz und schnellere Vorgänge auf der Loopbackschnittstelle. Diese IOCTL fordert an, dass der TCP/IP-Stapel einen speziellen schnellen Pfad für Loopbackvorgänge auf diesem Socket verwendet. Die [**SIO \_ LOOPBACK FAST \_ \_ PATH**](/previous-versions/windows/desktop/legacy/jj841212(v=vs.85)) IOCTL kann nur mit TCP-Sockets verwendet werden. Diese IOCTL muss auf beiden Seiten der Loopbacksitzung verwendet werden. Der schnelle TCP-Loopbackpfad wird mithilfe der IPv4- oder IPv6-Loopbackschnittstelle unterstützt. Standardmäßig ist **SIO \_ LOOPBACK \_ FAST \_ PATH** deaktiviert.

Ausführlichere Informationen finden Sie in der [**SIO \_ LOOPBACK-FAST \_ \_ PATH-Referenz.**](/previous-versions/windows/desktop/legacy/jj841212(v=vs.85)) **SIO \_ LOOPBACK \_ FAST \_ PATH** wird für Windows 8, Windows Server 2012 und höher unterstützt.

### <a name="sio_multipoint_loopback-opcode-setting-v-t1"></a>SIO \_ MULTIPOINT \_ LOOPBACK (Opcodeeinstellung: V, T==1)

Steuert, ob daten, die von einer Anwendung auf dem lokalen Computer (nicht notwendigerweise vom gleichen Socket) in einer Multicastsitzung gesendet werden, von einem Socket empfangen werden, der mit der Multicastzielgruppe auf der Loopbackschnittstelle verbunden ist. Der Wert **TRUE bewirkt,** dass von einer Anwendung auf dem lokalen Computer gesendete Multicastdaten an einen lauschenden Socket auf der Loopbackschnittstelle übermittelt werden. Der Wert **FALSE verhindert,** dass von einer Anwendung auf dem lokalen Computer gesendete Multicastdaten an einen lauschenden Socket auf der Loopbackschnittstelle übermittelt werden. Standardmäßig ist **SIO \_ MULTIPOINT \_ LOOPBACK** aktiviert.

### <a name="sio_multicast_scope-opcode-setting-i-t1"></a>SIO \_ MULTICAST \_ SCOPE (Opcodeeinstellung: I, T==1)

Gibt den Bereich an, über den Multicastübertragungen erfolgen. Der Bereich wird als die Anzahl der zu abgedeckten Routennetzwerksegmente definiert. Ein Bereich von 0 (null) gibt an, dass die Multicastübertragung nicht auf dem Kabel platziert wird, sondern über Sockets innerhalb des lokalen Hosts verteilt werden kann. Ein Bereichswert von 1 (Standard) gibt an, dass die Übertragung an das Netzwerk übertragen wird, aber keine Router überquert. Höhere Bereichswerte bestimmen die Anzahl der Router, die überschritten werden können. Beachten Sie, dass dies dem TTL-Parameter (Time-to-Live) beim IP-Multicasting entspricht. Standardmäßig ist der Bereich 1.

### <a name="sio_query_rss_processor_info-opcode-setting-o-t1"></a>SIO \_ QUERY RSS PROCESSOR INFO \_ \_ \_ (Opcodeeinstellung: O, T==1)

Fragt die Zuordnung zwischen einem Socket und einem RSS-Prozessorkern und einem NUMA-Knoten ab.

Die [**SIO \_ QUERY RSS PROCESSOR \_ \_ \_ INFO**](/previous-versions/windows/desktop/legacy/jj553482(v=vs.85)) IOCTL gibt eine [**SOCKET PROCESSOR \_ \_ AFFINITY-Struktur**](/windows/desktop/api/Ws2def/ns-ws2def-socket_processor_affinity) zurück, die [**die PROZESSORNUMMER \_**](/windows/win32/api/winnt/ns-winnt-processor_number) und die NUMA-Knoten-ID enthält. Die **zurückgegebene PROCESSOR \_ NUMBER-Struktur** enthält eine Gruppennummer und eine relative Prozessornummer innerhalb der Gruppe.

Ausführlichere Informationen finden Sie in der [**Referenz zu SIO \_ QUERY RSS PROCESSOR \_ \_ \_ INFO.**](/previous-versions/windows/desktop/legacy/jj553482(v=vs.85)) **SIO \_ QUERY \_ RSS \_ PROCESSOR \_ INFO** wird für Windows 8, Windows Server 2012 und höher unterstützt.

### <a name="sio_query_rss_scalability_info-opcode-setting-o-t3"></a>SIO \_ QUERY \_ RSS \_ SCALABILITY INFO \_ (Opcodeeinstellung: O, T==3)

Fragt Schnittstellen für empfangsseitige Skalierung (RECEIVE-Side Scaling, RSS) ab. Die für **SIO \_ QUERY \_ RSS \_ SCALABILITY \_ INFO** zurückgegebene Argumentstruktur wird in der **RSS \_ SCALABILITY \_ INFO-Struktur** angegeben, die in der *Headerdatei Mstcpip.h* definiert ist. Diese Struktur ist wie folgt definiert:

```cpp
// Scalability info for the transport
typedef struct _RSS_SCALABILITY_INFO {
   BOOLEAN RssEnabled;
} RSS_SCALABILITY_INFO, *PRSS_SCALABILITY_INFO;
```

Der im **RssEnabled-Member zurückgegebene Wert** gibt an, ob RSS auf mindestens einer Schnittstelle aktiviert ist.

Wenn der Ausgabepuffer nicht groß genug für die **RSS \_ SCALABILITY \_ INFO-Struktur** ist *(cbOutBuffer* ist kleiner als die Größe einer **RSS \_ SCALABILITY \_ INFO)** oder der *lpvOutBuffer-Parameter* ein **NULL-Zeiger** ist, wird **SOCKET \_ ERROR** als Ergebnis dieser IOCTL zurückgegeben, und [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) gibt [WSAEINVAL zurück.](windows-sockets-error-codes-2.md)

In Hochgeschwindigkeitsnetzwerken, in denen sich mehrere CPUs innerhalb eines einzelnen Systems befinden, ist die Fähigkeit des Netzwerkprotokollstapels, sich gut auf einem System mit mehreren CPUs zu skalieren, nicht mehr verfügbar, da die Architektur von NDIS 5.1 und früheren Versionen die Protokollverarbeitung auf eine einzelne CPU beschränkt. Die empfangsseitige Skalierung (Receive-Side Scaling, RSS) löst dieses Problem, indem die Netzwerklast eines Netzwerkadapters auf mehrere CPUs verteilt werden kann.

**SIO \_ QUERY \_ RSS \_ SCALABILITY \_ INFO** wird unter Windows Vista und höher unterstützt.

### <a name="sio_query_transport_setting-opcode-setting-i-t3"></a>SIO \_ QUERY TRANSPORT SETTING \_ \_ (Opcodeeinstellung: I, T==3)

Fragt die Transporteinstellungen für einen Socket ab. Die abgefragte Transporteinstellung basiert auf der [**TRANSPORT \_ SETTING \_ ID,**](/windows/win32/api/transportsettingcommon/ns-transportsettingcommon-transport_setting_id) die im *lpvInBuffer-Parameter übergeben* wird.

Die einzige Transporteinstellung, die derzeit definiert wird, ist für die **FUNKTION REAL TIME NOTIFICATION \_ \_ \_ CAPABILITY** auf einem TCP-Socket.

Wenn [**für TRANSPORT \_ SETTING \_ ID**](/windows/win32/api/transportsettingcommon/ns-transportsettingcommon-transport_setting_id) der **GUID-Member** auf **REAL TIME NOTIFICATION \_ \_ \_ CAPABILITY** festgelegt ist, ist dies eine Anforderung zum Abfragen der Echtzeitbenachrichtigungseinstellungen für den TCP-Socket, der mit [**ControlChannelTrigger**](/uwp/api/Windows.Networking.Sockets.ControlChannelTrigger) zum Empfangen von Netzwerkbenachrichtigungen im Hintergrund in einer Windows Store-App verwendet wird. Wenn der [**WSAIoctl-**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) oder [**WSPIoctl-Aufruf**](/previous-versions/windows/hardware/network/ff566296(v=vs.85)) erfolgreich ist, gibt diese IOCTL eine [**REAL TIME NOTIFICATION SETTING \_ \_ \_ \_ OUTPUT-Struktur**](/windows/desktop/api/Mstcpip/ns-mstcpip-real_time_notification_setting_input) mit dem aktuellen Status zurück.

Ausführlichere Informationen finden Sie in der [**Referenz zu SIO \_ QUERY TRANSPORT \_ \_ SETTING.**](/previous-versions/windows/desktop/legacy/jj553483(v=vs.85)) **SIO \_ QUERY \_ TRANSPORT \_ SETTING** wird für Windows 8, Windows Server 2012 und höher unterstützt.

### <a name="sio_query_wfp_ale_endpoint_handle-opcode-setting-o-t3"></a>SIO \_ QUERY \_ WFP \_ ALE ENDPOINT HANDLE \_ \_ (Opcodeeinstellung: O, T==3)

Fragt das ALE-Endpunkthandle (Application Layer Enforcement) ab.

Die Windows Filtering Platform (WFP) unterstützt die Überprüfung und Änderung des Netzwerkdatenverkehrs. In Windows Vista konzentriert sich WFP auf Szenarien, in denen der Hostcomputer der Kommunikationsendpunkt ist. Auf Windows Server 2008 gibt es jedoch Edgefirewallimplementierungen, die die WFP-Plattform nutzen möchten, um Pass-Through-Datenverkehr zu überprüfen und einen Proxy dafür zu erstellen. Der ISA-Server (Internet Security and Acceleration) ist ein Beispiel für ein solches Edgegerät.

Es gibt einige Firewallszenarien, die möglicherweise die Möglichkeit erfordern, ein eingehendes Paket in den einem vorhandenen Endpunkt zugeordneten Sendepfad einzujizieren. Es muss ein Mechanismus zum Entdecken des Endpunkthandpunkts der Transportebene verfügbar sein, der dem Zielendpunkt zugeordnet ist. Die Anwendung, die den Endpunkt erstellt hat, besitzt diese Endpunkte der Transportschicht. Diese IOCTL wird verwendet, um das Sockethandles für die Transport layer endpoint handle mapping (Zuordnung des Endpunkthandles der Transportebene) zu ermöglichen.

Wenn der Ausgabepuffer nicht groß genug für das Endpunkthandles ist *(cbOutBuffer* ist kleiner als die Größe eines **UINT64)** oder der *lpvOutBuffer-Parameter* ein **NULL-Zeiger** ist, wird **SOCKET \_ ERROR** als Ergebnis dieser IOCTL zurückgegeben, und [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) gibt [WSAEINVAL zurück.](windows-sockets-error-codes-2.md)

**SIO \_ QUERY \_ WFP \_ ALE \_ ENDPOINT \_ HANDLE** wird unter Windows Vista und höher unterstützt.

### <a name="sio_query_wfp_connection_redirect_context-opcode-setting-i-t3"></a>SIO \_ QUERY \_ WFP CONNECTION REDIRECT CONTEXT \_ \_ \_ (Opcodeeinstellung: I, T==3)

Fragt den Umleitungskontext nach einem Umleitungsdatensatz ab, der von einem WFP-Umleitungsdienst (Windows Filtering Platform) verwendet wird.

Die [**IOCTL-IOCTL des \_ \_ \_ \_ \_**](/previous-versions/windows/desktop/legacy/hh859712(v=vs.85)) WFP-VERBINDUNGSUMLEITUNGSKONTEXTS von SIO QUERY wird verwendet, um die Nachverfolgung von Verbindungen über einen Weitergeleiteten bei umgeleiteten Sockets zu ermöglichen. Dieses WFP-Feature erleichtert die Nachverfolgung von Umleitungsdatensätzen von der ersten Umleitung einer Verbindung zur endgültigen Verbindung zum Ziel.

Ausführlichere Informationen finden Sie in der [**Referenz zu SIO \_ QUERY \_ WFP CONNECTION REDIRECT \_ \_ \_ CONTEXT.**](/previous-versions/windows/desktop/legacy/hh859712(v=vs.85)) **SIO \_ QUERY \_ WFP \_ CONNECTION REDIRECT \_ \_ CONTEXT** wird für Windows 8, Windows Server 2012 und höher unterstützt.

### <a name="sio_query_wfp_connection_redirect_records-opcode-setting-i-t3"></a>SIO \_ QUERY \_ WFP CONNECTION REDIRECT RECORDS \_ \_ \_ (Opcodeeinstellung: I, T==3)

Fragt den Umleitungsdatensatz für die akzeptierte TCP/IP-Verbindung zur Verwendung durch einen WFP-Umleitungsdienst (Windows Filtering Platform) ab.

Die [**IOCTL-IOCTL für \_ \_ \_ \_ \_**](/previous-versions/windows/desktop/legacy/hh859713(v=vs.85)) WFP-VERBINDUNGSUMLEITUNGsdatensätze der SIO-ABFRAGE wird verwendet, um die Nachverfolgung von Verbindungen mit Einem Proxis für umgeleitete Socketverbindungen zu ermöglichen. Dieses WFP-Feature erleichtert die Nachverfolgung von Umleitungsdatensätzen von der ersten Umleitung einer Verbindung zur endgültigen Verbindung zum Ziel.

Ausführlichere Informationen finden Sie in der [**Referenz zu SIO \_ QUERY \_ WFP CONNECTION REDIRECT \_ \_ \_ RECORDS.**](/previous-versions/windows/desktop/legacy/hh859713(v=vs.85)) **SIO \_ QUERY \_ WFP \_ CONNECTION REDIRECT \_ \_ RECORDS** wird für Windows 8, Windows Server 2012 und höher unterstützt.

### <a name="sio_rcvall-opcode-setting-i-t3"></a>SIO \_ RC COD (Opcodeeinstellung: I, T==3)

Ermöglicht es einem Socket, alle IPv4- oder IPv6-Pakete zu empfangen, die über eine Netzwerkschnittstelle übergeben werden. Das socket-Handle, das an die [**WSAIoctl-Funktion**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) übergeben wird, muss einer der folgenden sein:

-   Ein IPv4-Socket, der erstellt wurde, bei dem die Adressfamilie auf AF INET, der Sockettyp auf SOCK RAW und das Protokoll auf \_ \_ IPPROTO IP festgelegt \_ wurde.
-   Ein IPv6-Socket, der erstellt wurde, bei dem die Adressfamilie auf AF INET6, der Sockettyp auf SOCK RAW und das Protokoll auf \_ \_ IPPROTO \_ IPV6 festgelegt wurde.

Der Socket muss auch an eine explizite lokale IPv4- oder IPv6-Schnittstelle gebunden werden, was bedeutet, dass Sie keine Bindung an **INADDR \_ ANY** oder **in6addr \_ beliebiger -Schnittstelle erstellen können.**

Auf Windows Server 2008 und früher erfasste die [**SIO \_ RCIO**](/previous-versions/windows/desktop/legacy/ee309610(v=vs.85)) IOCTL-Einstellung keine lokalen Pakete, die von einer Netzwerkschnittstelle gesendet wurden. Dies umfasste Pakete, die auf einer anderen Schnittstelle empfangen und die netzwerkschnittstelle weitergeleitet wurden, die für **die SIO \_ RCIO** IOCTL angegeben ist.

In Windows 7 und Windows Server 2008 R2 wurde dies geändert, sodass lokale Pakete, die von einer Netzwerkschnittstelle gesendet werden, ebenfalls erfasst werden. Dies schließt Pakete ein, die auf einer anderen Schnittstelle empfangen und dann die netzwerkgebundene Netzwerkschnittstelle an den Socket mit [**SIO \_ RCIO**](/previous-versions/windows/desktop/legacy/ee309610(v=vs.85)) IOCTL weitergeleitet wurden.

Zum Festlegen dieser IOCTL ist die Administratorberechtigung auf dem lokalen Computer erforderlich.

Dieses Feature wird manchmal auch als promiscuous-Modus bezeichnet.

Die möglichen Werte für die **Option SIO \_ RC HK** IOCTL werden in der RC ENUMERATION **\_ VALUE-Enumeration** angegeben, die in der *Headerdatei Mstcpip.h* definiert ist. Die möglichen Werte für SIO \_ RC WIE FOLGT:

| Begriff                                                                                                                 | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-|-|
| <span id="RCVALL_OFF"></span><span id="rcvall_off"></span>RC RC \_ OFF<br/>                                     | Deaktivieren Sie diese Option, damit ein Socket nicht alle IPv4- oder IPv6-Pakete im Netzwerk erhält. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="RCVALL_ON"></span><span id="rcvall_on"></span>RC RC \_ RC ON<br/>                                        | Aktivieren Sie diese Option, damit ein Socket alle IPv4- oder IPv6-Pakete im Netzwerk empfängt. Diese Option aktiviert den promiscuous-Modus auf der Netzwerkschnittstellenkarte (NIC), wenn die NIC den promiscuous-Modus unterstützt. In einem LAN-Segment mit einem Netzwerkhub erfasst eine NIC, die den promiscuous-Modus unterstützt, den sämtlichen IPv4- oder IPv6-Datenverkehr im LAN, einschließlich des Datenverkehrs zwischen anderen Computern im selben LAN-Segment. Alle erfassten Pakete (IPv4 oder IPv6, je nach Socket) werden an den unformatierten Socket übermittelt. <br/> Diese Option erfasst keine anderen Pakete (z. B. ARP-, IPX- und NetBEUI-Pakete) auf der Schnittstelle.<br/> Netmon verwendet den gleichen Modus für die Netzwerkschnittstelle, aber nicht diese Option, um Datenverkehr zu erfassen.<br/> |
| <span id="RCVALL_SOCKETLEVELONLY"></span><span id="rcvall_socketlevelonly"></span>RCBUCH \_ SOCKETLEVELONLY<br/> | Dieses Feature ist derzeit nicht implementiert, sodass das Festlegen dieser Option keine Auswirkungen hat.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="RCVALL_IPLEVEL"></span><span id="rcvall_iplevel"></span>RC GOVERNANCE \_ IPLEVEL<br/>                         | Aktivieren Sie diese Option, damit ein IPv4- oder IPv6-Socket alle Pakete auf IP-Ebene im Netzwerk empfängt. Mit dieser Option wird der promiscuous-Modus auf der Netzwerkschnittstellenkarte nicht aktiviert. Diese Option wirkt sich nur auf die Paketverarbeitung auf IP-Ebene aus. Die NIC empfängt weiterhin nur Pakete, die an die konfigurierten Unicast- und Multicastadressen geleitet werden. Ein Socket mit aktivierter Option empfängt jedoch nicht nur Pakete, die an bestimmte IP-Adressen geleitet werden, sondern auch alle IPv4- oder IPv6-Pakete, die die NIC empfängt.<br/> Diese Option erfasst keine anderen Pakete (z. B. ARP-, IPX- und NetBEUI-Pakete), die auf der Schnittstelle empfangen werden.<br/>                                                                                             |



 

Ausführlichere Informationen finden Sie in der [**SIO \_ RCIO-Referenz.**](/previous-versions/windows/desktop/legacy/ee309610(v=vs.85))

**SIO \_ RC ZWISCHEN** 2000 und höher wird Windows unterstützt.

### <a name="sio_rcvall_igmpmcast-opcode-setting-i-t3"></a>SIO \_ RC \_ IGMPMCAST (Opcodeeinstellung: I, T==3)

Ermöglicht es einem Socket, den sämtlichen IGMP-Multicast-IP-Datenverkehr im Netzwerk zu empfangen, ohne anderen Multicast-IP-Datenverkehr zu empfangen. Das socket-Handle, das an die [**WSAIoctl-Funktion**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) übergeben wird, muss die AF INET-Adressfamilie, den SOCK RAW-Sockettyp und \_ das \_ IPPROTO \_ IGMP-Protokoll haben. Der Socket muss auch an eine explizite lokale Schnittstelle gebunden werden, was bedeutet, dass Sie keine Bindung an INADDR \_ ANY erstellen können.

Nachdem der Socket gebunden und die IOCTL festgelegt wurde, geben Aufrufe der [**WSARecv-**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv) oder [**recv-Funktionen**](/windows/desktop/api/winsock/nf-winsock-recv) Multicast-IP-Datagramme zurück, die die gegebene Schnittstelle passieren. Beachten Sie, dass Sie einen ausreichend großen Puffer liefern müssen. Zum Festlegen dieser IOCTL ist die Administratorberechtigung auf dem lokalen Computer erforderlich.

**SIO \_ RC \_ IGMPMCAST** wird ab version Windows 2000 unterstützt.

### <a name="sio_rcvall_mcast-opcode-setting-i-t3"></a>SIO \_ RCCAST \_ MCAST (Opcodeeinstellung: I, T==3)

Ermöglicht es einem Socket, den sämtlichen Multicast-IP-Datenverkehr im Netzwerk zu empfangen (d. h. alle IP-Pakete, die für IP-Adressen im Bereich von 224.0.0.0 bis 239.255.255.255 bestimmt sind). Das socket-Handle, das an die [**WSAIoctl-Funktion**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) übergeben wird, muss die AF INET-Adressfamilie, den SOCK RAW-Sockettyp und \_ das \_ \_ IPPROTO-UDP-Protokoll haben. Der Socket muss auch an eine explizite lokale Schnittstelle gebunden werden, was bedeutet, dass Sie keine Bindung an INADDR \_ ANY erstellen können. Der Socket sollte an Port 0 (null) gebunden werden.

Nachdem der Socket gebunden und die IOCTL festgelegt wurde, geben Aufrufe der [**WSARecv-**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv) oder [**recv-Funktionen**](/windows/desktop/api/winsock/nf-winsock-recv) Multicast-IP-Datagramme zurück, die die gegebene Schnittstelle passieren. Beachten Sie, dass Sie einen ausreichend großen Puffer liefern müssen. Zum Festlegen dieser IOCTL ist die Administratorberechtigung auf dem lokalen Computer erforderlich.

**SIO \_ RCCAST \_ MCAST** wird auf Windows 2000 und höher unterstützt.

### <a name="sio_release_port_reservation-opcode-setting-i-t3"></a>SIO \_ RELEASE PORT RESERVATION \_ \_ (Opcodeeinstellung: I, T==3)

Gibt eine Laufzeitreservierung für einen Block von TCP- oder UDP-Ports frei. Die laufzeitreservierung, die freigegeben werden soll, muss vom ausstellenden Prozess mithilfe der [**SIO \_ ACQUIRE PORT \_ \_ RESERVATION**](/previous-versions/windows/desktop/legacy/gg699720(v=vs.85)) IOCTL erhalten worden sein.

Ausführlichere Informationen finden Sie in der [**Referenz zur \_ SIO-RELEASEPORTRESERVIERUNG. \_ \_**](/previous-versions/windows/desktop/legacy/gg699722(v=vs.85))

[**SIO \_ RELEASE \_ PORT \_ RESERVATION**](/previous-versions/windows/desktop/legacy/gg699722(v=vs.85)) wird unter Windows Vista und neueren Versionen des Betriebssystems unterstützt.

### <a name="sio_routing_interface_change-opcode-setting-i-t1"></a>SIO \_ ROUTING INTERFACE CHANGE \_ \_ (Opcodeeinstellung: I, T==1)

Um Benachrichtigungen über eine Routingschnittstellenänderung zu erhalten, die verwendet werden soll, um die Remoteadresse im Eingabepuffer zu erreichen (angegeben als [**sockaddr-Struktur).**](sockaddr-2.md) Nach Abschluss dieser IOCTL werden keine Ausgabeinformationen zur neuen Routingschnittstelle bereitgestellt. Die Vervollständigung gibt lediglich an, dass sich die Routingschnittstelle für ein bestimmtes Ziel geändert hat und mithilfe der ABFRAGE-IOCTL der **\_ SIO-ROUTINGSCHNITTSTELLE \_ \_** abgefragt werden sollte.

Es wird davon ausgegangen, dass die Anwendung überlappende E/A verwendet, um über die Änderung der Routingschnittstelle durch Den Abschluss der **SIO \_ ROUTING INTERFACE \_ CHANGE-Anforderung benachrichtigt \_ zu** werden, obwohl dies nicht erforderlich ist. Wenn die SIO ROUTING **\_ INTERFACE \_ \_ CHANGE** IOCTL für einen nicht blockierenden Socket mit den Parametern *lpOverlapped* und *lpCompletionRoutine* auf **NULL** ausgegeben wird, wird die sofortige Rückgabe und [WSAEWOULDBLOCK](windows-sockets-error-codes-2.md) als Fehler abgeschlossen, und die Anwendung kann dann auf das Routing von Änderungsereignissen warten, indem [**sie WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) oder [**WSAAsyncSelect**](/windows/desktop/api/winsock/nf-winsock-wsaasyncselect) mit in der Netzwerkereignisbitmaske festgelegtem FD \_ ROUTING INTERFACE CHANGE-Bit aufruft. \_ \_

Es wird erkannt, dass Routinginformationen in den meisten Fällen stabil bleiben, sodass die Anwendung mehrere ausstehende IOCTLs behalten muss, um Benachrichtigungen über alle Ziele zu erhalten, an denen sie interessiert ist, und dass der Dienstanbieter diese Benachrichtigungsanforderungen nachverfolgen muss, eine erhebliche Menge an Systemressourcen benötigt. Diese Situation kann vermieden werden, indem die Bedeutung der Eingabeparameter erweitert und die Anforderungen des Dienstanbieters wie folgt angepasst werden:

-   Die Anwendung kann eine protokollfamilienspezifische Platzhalteradresse [](/windows/desktop/api/winsock/nf-winsock-bind) angeben (die gleiche wie beim Bindungsaufruf bei der Anforderung der Bindung an eine beliebige verfügbare Adresse), um Benachrichtigungen über Routingänderungen an fordern zu können. Dadurch kann die Anwendung nur eine ausstehende **SIO \_ ROUTING INTERFACE \_ \_ CHANGE** für alle Sockets und Ziele behalten und dann **SIO ROUTING INTERFACE \_ \_ \_ QUERY** verwenden, um die tatsächlichen Routinginformationen zu erhalten.
-   Ein Dienstanbieter hat die Möglichkeit, die von der Anwendung im Eingabepuffer von **SIO \_ ROUTING INTERFACE \_ \_ CHANGE** angegebenen Informationen zu ignorieren (als ob die Anwendung eine Platzhalteradresse angegeben hätte) und das **SIO ROUTING INTERFACE \_ \_ \_ CHANGE** IOCTL- oder Signal FD ROUTING INTERFACE CHANGE-Ereignis im Falle einer Änderung der Routinginformationen (nicht nur die Route zu dem im Eingabepuffer angegebenen Ziel) zu \_ vervollständigen. \_ \_

### <a name="sio_routing_interface_query-opcode-setting-i-o-t1"></a>SIO \_ ROUTING INTERFACE QUERY \_ \_ (Opcodeeinstellung: I, O, T==1)

Um die Adresse der lokalen Schnittstelle (dargestellt als [**sockaddr-Struktur)**](sockaddr-2.md) zu erhalten, die zum Senden an die Remoteadresse verwendet werden soll, die im Eingabepuffer angegeben ist (als **sockaddr**). Remote-Multicastadressen können im Eingabepuffer übermittelt werden, um die Adresse der bevorzugten Schnittstelle für die Multicastübertragung zu erhalten. In jedem Fall kann die zurückgegebene Schnittstellenadresse von der Anwendung in einer nachfolgenden bind()-Anforderung verwendet werden.

Beachten Sie, dass Routen geändert werden können. Daher können Sich Anwendungen nicht darauf verlassen, dass die von **SIO \_ ROUTING INTERFACE \_ \_ QUERY** zurückgegebenen Informationen persistent sind. Anwendungen können sich für das Routing von Änderungsbenachrichtigungen über die **SIO \_ ROUTING INTERFACE \_ \_ CHANGE** IOCTL registrieren, die Benachrichtigungen über überlappende E/A oder ein FD \_ ROUTING INTERFACE \_ \_ CHANGE-Ereignis bietet. Mit der folgenden Aktionssequenz kann sichergestellt werden, dass die Anwendung immer über aktuelle Routingschnittstelleninformationen für ein bestimmtes Ziel verfügt:

-   Problem bei **der IOCTL-ÄNDERUNG \_ DER \_ \_ SIO-ROUTINGSCHNITTSTELLE**
-   Issue **SIO \_ ROUTING \_ INTERFACE \_ QUERY** IOCTL
-   Wenn **SIO \_ ROUTING INTERFACE \_ \_ CHANGE** IOCTL die Anwendung der Routingänderung benachrichtigt (entweder über überlappende E/A oder durch Signalisierung des FD \_ ROUTING INTERFACE \_ CHANGE-Ereignisses), sollte die gesamte Sequenz von Aktionen wiederholt \_ werden.

Wenn der Ausgabepuffer nicht groß genug ist, um die Schnittstellenadresse zu enthalten, wird SOCKET ERROR als Ergebnis dieser IOCTL zurückgegeben, und \_ [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) gibt [WSAEFAULT zurück.](windows-sockets-error-codes-2.md) Die erforderliche Größe des Ausgabepuffers wird in diesem Fall in *lpcbBytesReturned* zurückgegeben. Beachten Sie, dass der WSAEFAULT-Fehlercode auch zurückgegeben wird, wenn der *Parameter lpvInBuffer,* *lpvOutBuffer* oder *lpcbBytesReturned* nicht vollständig in einem gültigen Teil des Benutzeradressenbereichs enthalten ist.

Wenn die im Eingabepuffer angegebene Zieladresse nicht über eine der verfügbaren Schnittstellen erreicht werden kann, wird SOCKET ERROR als Ergebnis dieser IOCTL zurückgegeben, und \_ [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) gibt [WSAENETUNREACH](windows-sockets-error-codes-2.md) oder sogar [WSAENETDOWN](windows-sockets-error-codes-2.md) zurück, wenn die Netzwerkkonnektivität verloren geht.

### <a name="sio_set_compatibility_mode-opcode-setting-i-t3"></a>SIO \_ SET COMPATIBILITY MODE \_ \_ (Opcodeeinstellung: I, T==3)

Fordert an, wie der Netzwerkstapel bestimmte Verhaltensweisen behandeln soll, bei denen sich die Standardbehandlung für das Verhalten je nach Windows unterscheidet. Die Argumentstruktur für **SIO \_ SET COMPATIBILITY \_ \_ MODE** wird in der **WSA COMPATIBILITY \_ \_ MODE-Struktur** angegeben, die in der *Headerdatei Mswsockdef.h* definiert ist. Diese Struktur ist wie folgt definiert:

```cpp
/* Argument structure for SIO_SET_COMPATIBILITY_MODE */
typedef struct _WSA_COMPATIBILITY_MODE {
    WSA_COMPATIBILITY_BEHAVIOR_ID BehaviorId;
    ULONG TargetOsVersion;
} WSA_COMPATIBILITY_MODE, *PWSA_COMPATIBILITY_MODE;
```

Der im **BehaviorId-Member angegebene Wert** gibt das angeforderte Verhalten an. Der im **TargetOsVersion-Member** angegebene Wert gibt Windows Version an, die für das Verhalten angefordert wird.

Der **BehaviorId-Member** kann einer der Werte aus dem **WSA \_ COMPATIBILITY BEHAVIOR \_ ID-Enumerationstyp \_** sein, der in der *Headerdatei "Mswsockdef.h"* definiert ist. Die möglichen Werte für das **BehaviorId-Member** lauten wie folgt.

| Begriff                                                                                                                                                                             | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-|-|
| <span id="WsaBehaviorAll"></span><span id="wsabehaviorall"></span><span id="WSABEHAVIORALL"></span>WsaBehaviorAll<br/>                                                     | Dies entspricht dem Anfordern aller möglichen kompatiblen Verhaltensweisen, die für die **\_ WSA-KOMPATIBILITÄTsverhaltens-ID \_ \_ definiert sind.**<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="WsaBehaviorReceiveBuffering"></span><span id="wsabehaviorreceivebuffering"></span><span id="WSABEHAVIORRECEIVEBUFFERING"></span>WsaBehaviorReceiveBuffering<br/> | Wenn **der TargetOsVersion-Member** auf einen Wert für Windows Vista oder höher festgelegt ist, sind Reduzierungen der TCP-Empfangspuffergröße auf diesem Socket mithilfe der **Socketoption SO \_ RCVBUF** auch nach der Einrichtung einer TCP-Verbindung zulässig. <br/> Wenn **der TargetOsVersion-Member** auf einen Wert vor Windows Vista festgelegt ist, sind Reduzierungen der TCP-Empfangspuffergröße für diesen Socket mithilfe der **Socketoption SO \_ RCVBUF** nach der Verbindungseinrichtung nicht zulässig. <br/>                                                                                                                                                                                  |
| <span id="WsaBehaviorAutoTuning"></span><span id="wsabehaviorautotuning"></span><span id="WSABEHAVIORAUTOTUNING"></span>WsaBehaviorAutoTuning<br/>                         | Wenn **das TargetOsVersion-Element** auf einen Wert für Windows Vista oder höher festgelegt ist, wird die automatische Optimierung des Empfangsfensters aktiviert, und der Skalierungsfaktor des TCP-Fensters wird vom Standardwert 8 auf 2 reduziert.<br/> Wenn **TargetOsVersion auf einen** Wert vor Windows Vista festgelegt ist, ist die automatische Optimierung des Empfangsfensters deaktiviert. Die Skalierungsoption TCP-Fenster ist ebenfalls deaktiviert, und die maximale Größe des Empfangsfensters ist auf 65.535 Bytes beschränkt. Die Skalierungsoption TCP-Fenster kann nicht für die Verbindung ausgehandelt werden, auch wenn die **Socketoption SO \_ RCVBUF** für diesen Socket aufgerufen wurde, die einen Wert über 65.535 Byte vor dem Herstellen der Verbindung an gab.<br/> |



 

Ausführlichere Informationen finden Sie in der [**Referenz zu SIO \_ SET COMPATIBILITY \_ \_ MODE.**](/previous-versions/windows/desktop/legacy/cc136103(v=vs.85))

**SIO \_ SET \_ COMPATIBILITY \_ MODE** wird unter Windows Vista und höher unterstützt.

### <a name="sio_set_group_qos-opcode-setting-i-t1"></a>SIO \_ SET \_ GROUP \_ QOS (Opcodeeinstellung: I, T==1)

Reserviert.

### <a name="sio_set_priority_hint-opcode-setting-i-t3"></a>SIO_SET_PRIORITY_HINT (Opcodeeinstellung: I, T==3)

Stellt einen Hinweis für das zugrunde liegende Transportprotokoll zur Behandlung des Datenverkehrs auf diesem Socket mit einer bestimmten Priorität zur Seite. Der *lpvInBuffer muss* auf eine Variable vom Typ **PRIORITY_HINT,** bei der *cbInBuffer* auf sizeof(PRIORITY_HINT) festgelegt ist. Die *Parameter lpvOutBuffer* *und cbOutBuffer* müssen **NULL** bzw. 0 sein. Die TCP Windows implementierung von Microsoft unterstützt diese IOCTL ab Windows 10, Version 1809 (10.0; Build 17763) und höher wie folgt: Wenn der angeforderte Prioritätswert auf **IoPriorityHintVeryLow** festgelegt ist, verwendet TCP eine geänderte Version des LEDBAT-Algorithmus (definiert in RFC 6817) zum Steuern der Ausgehenden Datenverkehrsrate auf dem Socket. Der eingehende Datenverkehr ist von dieser IOCTL nicht betroffen. LEDBAT ist ein Scavenger-Algorithmus, dessen Ziel es ist, die Latenz niedrig zu halten und negative Auswirkungen auf den Datenverkehr mit normaler Priorität zu verhindern, indem der Weg aus dem Weg geht, wenn Datenverkehr mit normaler Priorität vorhanden ist.

Siehe auch [RFC 6817](https://tools.ietf.org/html/rfc6817).

**SIO_SET_PRIORITY_HINT** wird auf Windows 10, Version 1809 (10.0; Build 17763) und höher.

### <a name="sio_set_qos-opcode-setting-i-t1"></a>SIO \_ SET \_ QOS (Opcodeeinstellung: I, T==1)

Ordnen Sie die [**angegebene QOS-Struktur**](/windows/win32/api/winsock2/ns-winsock2-qos) dem Socket zu. Es ist kein Ausgabepuffer erforderlich. Die **QOS-Struktur** wird aus dem Eingabepuffer erhalten. Der [WSAENOPROTOOPT-Fehlercode](windows-sockets-error-codes-2.md) wird für Dienstanbieter angegeben, die die Servicequalität nicht unterstützen.

### <a name="sio_tcp_initial_rto-opcode-setting-i-t3"></a>SIO_TCP_INITIAL_RTO (Opcodeeinstellung: I, T==3)

Steuert die Anfänglichen (SYN/SYN+ACK)-Neuübertragungsmerkmale eines TCP-Sockets durch Konfigurieren von RTO-Parametern (Initial Retransmission Timeout). Die Konfigurationsparameter werden in einer [**TCP \_ INITIAL \_ RTO \_ PARAMETERS-Struktur**](/windows/desktop/api/mswsock/ns-mswsock-transmit_file_buffers) angegeben.

Ausführlichere Informationen finden Sie in der [**SIO_TCP_INITIAL_RTO**](./sio-tcp-initial-rto.md) Referenz. [**SIO_TCP_INITIAL_RTO**](./sio-tcp-initial-rto.md) wird für Windows 8, Windows Server 2012 und höher unterstützt.

### <a name="sio_timestamping"></a>SIO_TIMESTAMPING

Eine Socket-IOCTL, die zum Konfigurieren des Empfangs von Socket-Übertragungs-/Empfangszeitstempeln verwendet wird. Nur für Datagrammsockets gültig. Der Eingabetyp für **SIO_TIMESTAMPING** ist die [**TIMESTAMPING_CONFIG**](/windows/win32/api/mstcpip/ns-mstcpip-timestamping_config) Struktur.

Siehe auch [Winsock-Zeitstempel.](/windows/win32/winsock/winsock-timestamping)

### <a name="sio_translate_handle-opcode-setting-i-o-t1"></a>SIO \_ TRANSLATE \_ HANDLE (Opcodeeinstellung: I, O, T==1)

So erhalten Sie ein entsprechendes Handle für *Sockets,* das im Kontext einer Begleitschnittstelle gültig ist (z. B. TH \_ NETDEV und TH \_ TAPI). Eine Manifestkonst constant, die die Begleitschnittstelle zusammen mit allen anderen erforderlichen Parametern identifiziert, wird im Eingabepuffer angegeben. Das entsprechende Handle ist nach Abschluss dieser Funktion im Ausgabepuffer verfügbar. Einzelheiten zu einer bestimmten Begleitschnittstelle finden Sie im entsprechenden Abschnitt unter [Winsock-](winsock-annexes.md) Datenbank. Der [WSAENOPROTOOPT-Fehlercode](windows-sockets-error-codes-2.md) wird für Dienstanbieter angegeben, die diese IOCTL für die angegebene Begleitschnittstelle nicht unterstützen. Diese IOCTL ruft das handle ab, das mithilfe von **SIO \_ TRANSLATE HANDLE zugeordnet \_ ist.**

Es wird empfohlen, die Component Object Model (COM) anstelle dieser IOCTL zu verwenden, um andere Schnittstellen zu finden und zu verfolgen, die möglicherweise von einem Socket unterstützt werden. Diese IOCTL ist aus Gründen der Abwärtskompatibilität mit Systemen vorhanden, bei denen COM nicht verfügbar ist oder aus einem anderen Grund nicht verwendet werden kann.

### <a name="sio_udp_connreset-opcode-setting-i-t3"></a>SIO \_ UDP \_ CONNRESET (Opcodeeinstellung: I, T==3)

**Windows XP:** Steuert, ob UDP-PORT \_ UNREACHABLE-Nachrichten gemeldet werden. Legen Sie auf **TRUE fest,** um die Berichterstellung zu aktivieren. Legen Sie auf **FALSE fest,** um die Berichterstellung zu deaktivieren.

### <a name="sio_set_wfp_connection_redirect_records-opcode-setting-i-t3"></a>SIO \_ SET \_ WFP CONNECTION REDIRECT RECORDS \_ \_ \_ (Opcodeeinstellung: I, T==3)

Legt den Umleitungsdatensatz auf den neuen TCP-Socket fest, der zum Herstellen einer Verbindung mit dem endgültigen Ziel für die Verwendung durch einen WFP-Umleitungsdienst (Windows Filtering Platform) verwendet wird.

Die [**SIO \_ SET \_ WFP CONNECTION REDIRECT \_ \_ \_ RECORDS**](/previous-versions/windows/desktop/legacy/hh859714(v=vs.85)) IOCTL wird als Teil der Nachverfolgung von Verbindungen mit Einem Anderen bei umgeleiteten Socketverbindungen verwendet. Dieses WFP-Feature erleichtert die Nachverfolgung von Umleitungsdatensätzen von der ersten Umleitung einer Verbindung zur endgültigen Verbindung zum Ziel.

Ausführlichere Informationen finden Sie in der [**Referenz zu SIO \_ SET \_ WFP CONNECTION REDIRECT \_ \_ \_ RECORDS.**](/previous-versions/windows/desktop/legacy/hh859714(v=vs.85)) **SIO \_ SET \_ WFP \_ CONNECTION REDIRECT \_ \_ RECORDS** wird für Windows 8, Windows Server 2012 und höher unterstützt.

### <a name="sio_tcp_info-opcode-setting-i-o-t3"></a>SIO \_ TCP \_ INFO (Opcodeeinstellung: I, O, T==3)

Ruft die TCP-Statistik für einen Socket ab. Die TCP-Statistiken werden in einer [**TCP \_ INFO \_ v0-Struktur**](/windows/desktop/api/Mstcpip/ns-mstcpip-tcp_info_v0) bereitgestellt.

Im Gegensatz zum Abrufen von TCP-Statistiken mit der [**GetPerTcpConnectionEStats-Funktion**](/windows/win32/api/iphlpapi/nf-iphlpapi-getpertcpconnectionestats) erfordert das Abrufen von TCP-Statistiken mit diesem Steuerungscode nicht, dass der Benutzercode die TCP-Verbindungstabelle laden, speichern und filtern muss, und es sind keine erhöhten Berechtigungen erforderlich.

Weitere Informationen finden Sie unter [**SIO \_ TCP \_ INFO**](/previous-versions/windows/desktop/legacy/mt823415(v=vs.85)). **SIO \_ TCP \_ INFO** wird für Windows 10 Version 1703, Windows Server 2016 und höher unterstützt.

## <a name="remarks"></a>Hinweise

Winsock Ioctls werden in einer Reihe verschiedener Headerdateien definiert. Dazu gehören die *Headerdatei Winsock2.h,* *Mswsock.h* *und Mstcpip.h.*

Im Microsoft Windows Software Development Kit (SDK), das für Windows Vista und höher veröffentlicht wurde, hat sich die Organisation der Headerdateien geändert, und eine Reihe von Winsock Ioctls sind auch in den Headerdateien *Ws2def.h,* *Ws2ipdef.h* und *Mswsockdef.h* definiert. Die *Headerdatei "Ws2def.h"* wird automatisch in die *Headerdatei "Winsock2.h"* eingeschlossen. Die *Headerdatei Ws2ipdef.h* wird automatisch in die *Headerdatei Ws2tcpip.h* eingeschlossen. Die *Headerdatei "Mswsockdef.h"* ist automatisch in der *Headerdatei "Mswsockdef.h"* enthalten.

## <a name="requirements"></a>Anforderungen

|Anforderung|Wert|
|-|-|
| Header<br/> | <dl> <dt>Winsock2.h;</dt> <dt>Mstcpip.h;</dt> <dt>Mswsock.h;</dt> <dt>Mswsockdef.h unter Windows Vista, Windows Server 2008 und Windows 7 (einschließlich Mswsock.h);</dt> <dt>Ws2def.h unter Windows Vista, Windows Server 2008 und Windows 7 (einschließlich Winsock2.h);</dt> <dt>Ws2ipdef.h unter Windows Vista, Windows Server 2008 und Windows 7 (einschließlich Ws2tcpip.h)</dt> </dl> |
