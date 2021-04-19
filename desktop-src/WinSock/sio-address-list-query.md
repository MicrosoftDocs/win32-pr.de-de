---
description: Der Steuercode Ruft eine Liste der lokalen Transport Adressen der Protokollfamilie des Sockets ab, an die die Anwendung gebunden werden kann.
ms.assetid: 6b23a019-812c-4623-941b-87928acabbd2
title: SIO_ADDRESS_LIST_QUERY Steuerungs Codes
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 7a728293afa51ceb58d61141e7184077478b787c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349585"
---
# <a name="sio_address_list_query-control-code"></a>SIO_ADDRESS_LIST_QUERY Steuerungs Codes

## <a name="description"></a>BESCHREIBUNG

Der Code für die **\_ \_ \_ Abfrage** Steuerung der Stamm Liste der Stamm Verwaltungs Server erhält eine Liste lokaler Transport Adressen der Protokollfamilie des Sockets, an die die Anwendung gebunden werden kann.
Die Liste der Adressen variiert je nach Adressfamilie, und einige Adressen werden aus der Liste ausgeschlossen.

Um diesen Vorgang auszuführen, wenden Sie die [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) -oder **wspioctl** -Funktion mit den folgenden Parametern an.

```cpp
int WSAIoctl(
  (socket) s,            // descriptor identifying a socket
  SIO_ADDRESS_LIST_QUERY,            // dwIoControlCode
  NULL,                              // lpvInBuffer
  0,                                 // cbInBuffer
  (LPVOID) lpvOutBuffer,          // output buffer
  (DWORD) cbOutBuffer,            // size of output buffer  
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped, // OVERLAPPED structure
  (LPWSAOVERLAPPED_COMPLETION_ROUTINE) lpCompletionRoutine,  // completion routine
);
```

```cpp
int WSPIoctl(
  (socket) s,            // descriptor identifying a socket
  SIO_ADDRESS_LIST_QUERY,            // dwIoControlCode
  NULL,                              // lpvInBuffer
  0,                                 // cbInBuffer
  (LPVOID) lpvOutBuffer,          // output buffer
  (DWORD) cbOutBuffer,            // size of output buffer  
  (LPDWORD) lpcbBytesReturned,    // number of bytes returned
  (LPWSAOVERLAPPED) lpOverlapped, // OVERLAPPED structure
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
Verwenden Sie für diesen Vorgang eine-Abfrage für die- **\_ \_ \_ Abfrage** .

### <a name="lpvinbuffer"></a>lpvinbuffer

Ein Zeiger auf den Eingabepuffer.
Dieser Parameter wird für diesen Vorgang nicht verwendet.

### <a name="cbinbuffer"></a>cbinbuffer

Die Größe des Eingabe Puffers in Bytes.
Dieser Parameter wird für diesen Vorgang nicht verwendet.

### <a name="lpvoutbuffer"></a>lpvoutbuffer

Ein Zeiger auf den Ausgabepuffer.

### <a name="cboutbuffer"></a>cboutbuffer

Die Größe des Ausgabepuffers in Bytes.

### <a name="lpcbbytesreturned"></a>lpcbbyteszurück gegeben

Ein Zeiger auf eine Variable, die die Größe der im Ausgabepuffer gespeicherten Daten (in Bytes) empfängt.

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
| **Wsaabval** | Der *dwIoControlCode* -Parameter ist kein gültiger Befehl, oder ein angegebener Eingabeparameter ist nicht zulässig, oder der Befehl ist nicht auf den angegebenen Sockettyp anwendbar. Dieser Fehler wird zurückgegeben, wenn der *cbinbuffer* -Parameter nicht auf **null** festgelegt ist. |
| **WSAENETDOWN** | Das Netzwerk Subsystem ist fehlgeschlagen. |
| **WSAENOBUFS** | Es ist kein Pufferspeicher verfügbar. |
| **Wsaumoproumopt** | Die Socketoption wird für das angegebene Protokoll nicht unterstützt. |
| **Wsaumotsock** | Der Deskriptor *s* ist kein Socket. |
| **WSAEOPNOTSUPP** | Der angegebene ioctl-Befehl wird nicht unterstützt. Dieser Fehler wird zurückgegeben, wenn die Liste der " **SIO- \_ Adress \_ Liste \_** " ioctl vom Transportanbieter nicht unterstützt wird. |

## <a name="remarks"></a>Bemerkungen

Die Abfrage "ioctl" der Liste "-IP- **\_ Adress \_ Liste \_** " wird unter Windows 2000 und höheren Versionen des Betriebssystems unterstützt.

Der Code für die **\_ \_ \_ Abfrage** Steuerung der Stamm Liste der Stamm Verwaltungs Server erhält eine Liste lokaler Transport Adressen der Protokollfamilie des Sockets, an die die Anwendung gebunden werden kann.
Die Liste der Adressen variiert je nach Adressfamilie.

Für die Gruppe "AF \_ inet6 Address" werden alle Adressen außer den folgenden zurückgegeben:

* Eine beliebige IP-Adresse, bei der der Status der doppelten Adresserkennung (DAD) nicht ipdadstatepreferred ist.
* Eine beliebige IP-Adresse mit einer Bereichs Ebene unterhalb von scopelevelsubnet für eine Schnittstelle, bei der der Schnittstellentyp ist, **Wenn der \_ Typ \_ Software \_ Loopback** ist.
Dies bedeutet, dass Link-Local-Adressen (FE80: *) und Loopback (:: 1) für Schnittstellen von, **Wenn der \_ Typ \_ Software \_ Loopback** Type ausgeschlossen ist, nicht, wenn sich diese Adressen auf einer Schnittstelle mit einem anderen Typ befinden.

Für die **AF \_ inet** -Adressfamilie werden alle Adressen außer den folgenden zurückgegeben:

* Eine beliebige IP-Adresse, bei der der Status der doppelten Adresserkennung (DAD) nicht ipdadstatepreferred ist.
* Eine beliebige IP-Adresse an einer Schnittstelle, bei der der Schnittstellentyp lautet, **Wenn der \_ Typ \_ Software \_ Loopback** und Link lokal ist.
Dies bedeutet, dass Link-Local-Adressen (169,254.*) und Loopback (127.*) für Schnittstellen von, **Wenn der \_ Typ \_ Software \_ Loopback** Type ausgeschlossen wird, nicht, wenn sich diese Adressen auf einer Schnittstelle mit einem anderen Typ befinden.

Weitere Informationen zum Status "Dad" finden Sie in der IP-Hilfsdokumentation zur IP [**- \_ \_ Bundesstaaten**](/windows/desktop/api/nldef/ne-nldef-nl_dad_state) -Enumeration und [**IP- \_ Adapter- \_ \_ unicastadressstruktur**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_unicast_address_lh) sowie in der MIB-Dokumentation der [**MIB \_ unicastipaddress- \_ Zeilen**](/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row) Struktur.
Weitere Informationen zum Schnittstellentyp finden Sie in der IP-Hilfsdokumentation zur Struktur der [**IP- \_ Adapter \_ Adressen**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_addresses_xp) und der Funktion [**getadaptersadressen**](/windows/desktop/api/iphlpapi/nf-iphlpapi-getadaptersaddresses) sowie in der MIB-Dokumentation zu [**MIB_IF_ROW2**](/windows/desktop/api/netioapi/ns-netioapi-mib_if_row2) Struktur.
Weitere Informationen zur Bereichs Ebene finden Sie in der IP-Hilfsobjekt in der [**IP_ADAPTER_ADDRESSES**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_addresses_xp) -Struktur und auf der [**\_ Bereichsebene**](/windows/desktop/api/ws2def/ne-ws2def-scope_level) -Enumeration.

Die im Ausgabepuffer, auf den der *lpvoutbuffer* -Parameter verweist, zurückgegebene Liste hat die Form [**einer \_ socketadresslist \_**](/windows/desktop/api/ws2def/ns-ws2def-socket_address_list) -Struktur.

Wenn der im *lpvoutbuffer* -Parameter angegebene Ausgabepuffer nicht groß genug ist, um die Adressliste aufzunehmen, wird der **\_ Socketfehler** als Ergebnis dieser ioctl zurückgegeben, und [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) gibt [wsaefault](windows-sockets-error-codes-2.md)zurück.
Die erforderliche Größe (in Bytes) für den Ausgabepuffer wird in diesem Fall im *lpcbbytesall* -Parameter zurückgegeben.
Beachten Sie, dass der Fehlercode von [wsaefault](windows-sockets-error-codes-2.md) auch zurückgegeben wird, wenn der Parameter *lpvinbuffer*, *lpvoutbuffer* oder *lpcbbytesall* nicht vollständig in einem gültigen Teil des Benutzer Adressraums enthalten ist.

Die Liste der " **SIO- \_ Adress \_ Liste \_** " wird in der Regel synchron aufgerufen, wobei der *lpvoverllapp* -Parameter auf **null** festgelegt ist, da die Liste der Adressen sofort zurückgegeben wird.

**Hinweis**  In Windows-Plug-and-Play-Umgebungen können Adressen dynamisch hinzugefügt und entfernt werden.
Daher können Anwendungen nicht darauf basieren, dass die von der-Abfrage der- **\_ \_ \_ Abfrage Liste** zurückgegebenen Informationen persistent sind.
Anwendungen können sich für Adress Änderungs Benachrichtigungen über die Übersicht über die Übersicht über die Übersicht über die Übersicht über die IOCTL-Adress **\_ \_ Liste \_** registrieren, die eine Benachrichtigung über das überlappende e/a oder das **\_ \_ \_ Änderungs** Ereignis für die
Die folgende Sequenz von Aktionen kann verwendet werden, um sicherzustellen, dass die Anwendung immer über aktuelle Adresslisten Informationen verfügt:

* Problem bei der Änderung der " **SIO \_ Address \_ List \_** "-ioctl
* Problem mit der Liste "die der-IOCTL- **\_ \_ \_ Abfrage** "
* Immer, wenn der IOCTL-Aufruf der " **SIO- \_ Adress \_ Liste \_** " die Anwendung über eine überlappende e/a-Änderung oder durch Signalisieren eines **FD- \_ Adresslisten- \_ \_ Änderungs** Ereignisses benachrichtigt, sollte die gesamte Sequenz von Aktionen wiederholt werden.

Auf dem Microsoft Windows Software Development Kit (SDK), das für Windows Vista und höher veröffentlicht wurde, hat sich die Organisation der Header Dateien geändert, und der Code der in der *Ws2def. h* -Header Datei definierten Abfrage Steuerungs Code der **SIO- \_ Adress \_ Liste \_** ist definiert.
Beachten Sie, dass die Header Datei " *Ws2def. h* " automatisch in " *Winsock2. h*" enthalten ist und niemals direkt verwendet werden sollte.

## <a name="see-also"></a>Siehe auch

[**Getadaptersadressen**](/windows/desktop/api/iphlpapi/nf-iphlpapi-getadaptersaddresses)

[**IP_ADAPTER_ADDRESSES**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_addresses_xp)

[**IP_ADAPTER_UNICAST_ADDRESS**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_unicast_address_lh)

[**IP_DAD_STATE**](/windows/desktop/api/nldef/ne-nldef-nl_dad_state)

[**MIB_IF_ROW2**](/windows/desktop/api/netioapi/ns-netioapi-mib_if_row2)

[**MIB_UNICASTIPADDRESS_ROW**](/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row)

[**SCOPE_LEVEL**](/windows/desktop/api/ws2def/ne-ws2def-scope_level)

[**SOCKET_ADDRESS_LIST**](/windows/desktop/api/ws2def/ns-ws2def-socket_address_list)

[**Glühbirne**](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)

[**Wsagein verlappedresult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**Wsaoverlgetauscht**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**Wsasocketa**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**Wsasocketw**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
