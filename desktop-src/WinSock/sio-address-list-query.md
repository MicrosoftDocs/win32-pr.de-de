---
description: Der Steuerungscode erhält eine Liste der lokalen Transportadressen der Protokollfamilie des Sockets, an die die Anwendung gebunden werden kann.
ms.assetid: 6b23a019-812c-4623-941b-87928acabbd2
title: SIO_ADDRESS_LIST_QUERY-Steuerelementcode
ms.topic: reference
ms.date: 05/20/2019
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
api_location:
- mstcpip.h
ms.openlocfilehash: 57d529ed4ea525b01e294efcacc1aa8dd2b118106177bd46cb64ffdf42a31a58
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097530"
---
# <a name="sio_address_list_query-control-code"></a>SIO_ADDRESS_LIST_QUERY-Steuerelementcode

## <a name="description"></a>BESCHREIBUNG

Der **SIO \_ ADDRESS LIST \_ QUERY-Steuerungscode \_** erhält eine Liste der lokalen Transportadressen der Protokollfamilie des Sockets, an die die Anwendung gebunden werden kann.
Die Liste der Adressen variiert je nach Adressfamilie, und einige Adressen werden aus der Liste ausgeschlossen.

Um diesen Vorgang durchzuführen, rufen Sie die [**WSAIoctl-**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) oder **WSPIoctl-Funktion** mit den folgenden Parametern auf.

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

Der Steuerungscode für den Vorgang.
Verwenden **Sie SIO \_ ADDRESS LIST \_ \_ QUERY** für diesen Vorgang.

### <a name="lpvinbuffer"></a>lpvInBuffer

Ein Zeiger auf den Eingabepuffer.
Dieser Parameter wird für diesen Vorgang nicht verwendet.

### <a name="cbinbuffer"></a>cbInBuffer

Die Größe des Eingabepuffers in Bytes.
Dieser Parameter wird für diesen Vorgang nicht verwendet.

### <a name="lpvoutbuffer"></a>lpvOutBuffer

Ein Zeiger auf den Ausgabepuffer.

### <a name="cboutbuffer"></a>cbOutBuffer

Die Größe des Ausgabepuffers in Bytes.

### <a name="lpcbbytesreturned"></a>lpcbBytesReturned

Ein Zeiger auf eine Variable, die die Größe der im Ausgabepuffer gespeicherten Daten in Bytes empfängt.

### <a name="lpvoverlapped"></a>lpvOverlapped

Ein Zeiger auf eine [**WSAOVERLAPPED-Struktur.**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

Wenn *Sockets ohne* das überlappende Attribut erstellt wurden, wird *der lpOverlapped-Parameter* ignoriert.

Wenn *s* mit dem überlappenden Attribut geöffnet wurde und der *lpOverlapped-Parameter* nicht **NULL** ist, wird der Vorgang als überlappende (asynchrone) Operation ausgeführt.
In diesem Fall muss *der lpOverlapped-Parameter* auf eine gültige [**WSAOVERLAPPED-Struktur**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped) verweisen.

Bei überlappenden Vorgängen wird die [**WSAIoctl-**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) oder **WSPIoctl-Funktion** sofort zurückgegeben, und die entsprechende Abschlussmethode wird signalisiert, wenn der Vorgang abgeschlossen wurde.
Andernfalls gibt die Funktion erst dann zurück, wenn der Vorgang abgeschlossen wurde oder ein Fehler auftritt.

### <a name="lpcompletionroutine"></a>lpCompletionRoutine

Typ: \_ In_opt \_ [ **LPWSAOVERLAPPED_COMPLETION_ROUTINE**](/windows/win32/api/winsock2/nc-winsock2-lpwsaoverlapped_completion_routine)

Ein Zeiger auf die Abschlussroutine, die aufgerufen wird, wenn der Vorgang abgeschlossen wurde (bei nicht überlappenden Sockets ignoriert).

### <a name="lpthreadid"></a>lpThreadId

Ein Zeiger auf eine [**WSATHREADID-Struktur,**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) die vom Anbieter in einem nachfolgenden Aufruf von [**WPUQueueApc verwendet werden soll.**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc)
Der Anbieter sollte die [**referenzierte WSATHREADID-Struktur**](/windows/desktop/api/ws2spi/ns-ws2spi-wsathreadid) (nicht den Zeiger auf dieselbe) speichern, bis die [**WPUQueueApc-Funktion**](/windows/desktop/api/Ws2spi/nf-ws2spi-wpuqueueapc) zurückgegeben wurde.

**Hinweis:**  Dieser Parameter gilt nur für die **WSPIoctl-Funktion.**

### <a name="lperrno"></a>lpErrno

Ein Zeiger auf den Fehlercode.

**Hinweis:**  Dieser Parameter gilt nur für die **WSPIoctl-Funktion.**

## <a name="return-value"></a>Rückgabewert

Wenn der Vorgang erfolgreich abgeschlossen wurde, gibt die [**WSAIoctl-**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) oder **WSPIoctl-Funktion** 0 (null) zurück.

Wenn der Vorgang fehlschlägt oder aussteht, gibt die [**WSAIoctl-**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl) oder **WSPIoctl-Funktion** **SOCKET ERROR \_ zurück.**
Um erweiterte Fehlerinformationen zu erhalten, rufen [**Sie WSAGetLastError auf.**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)

| Fehlercode | Bedeutung |
|------------|---------|
| **AUSSTEHENDE \_ \_ WSA-E/A** | Ein überlappende Vorgang wurde erfolgreich initiiert, und der Abschluss wird zu einem späteren Zeitpunkt angezeigt. |
| **\_WSA-VORGANG \_ ABGEBROCHEN** | Ein überlappende Vorgang wurde aufgrund des Schließens des Sockets oder der Ausführung des IOCTL-Befehls **SIO \_ FLUSH** abgebrochen. |
| **WSAEFAULT** | Der *lpOverlapped-* oder *lpCompletionRoutine-Parameter* ist nicht vollständig in einem gültigen Teil des Benutzeradrenraums enthalten. |
| **WSAEINPROGRESS** | Die Funktion wird aufgerufen, wenn ein Rückruf in Bearbeitung ist. |
| **WSAEINTR** | Ein blockierende Vorgang wurde unterbrochen. |
| **WSAEINVAL** | Der *dwIoControlCode-Parameter* ist kein gültiger Befehl, oder ein angegebener Eingabeparameter ist nicht akzeptabel, oder der Befehl gilt nicht für den angegebenen Sockettyp. Dieser Fehler wird zurückgegeben, wenn *der cbInBuffer-Parameter* nicht auf **NULL festgelegt ist.** |
| **WSAENETDOWN** | Fehler beim Netzwerksubsystem. |
| **WSAENOBUFS** | Kein Pufferspeicherplatz verfügbar. |
| **WSAENOPROTOOPT** | Die Socketoption wird für das angegebene Protokoll nicht unterstützt. |
| **WSAENOTSOCK** | Der Deskriptor *s* ist kein Socket. |
| **WSAEOPNOTSUPP** | Der angegebene IOCTL-Befehl wird nicht unterstützt. Dieser Fehler wird zurückgegeben, wenn **die SIO \_ ADDRESS LIST \_ \_ QUERY** IOCTL vom Transportanbieter nicht unterstützt wird. |

## <a name="remarks"></a>Hinweise

Die **SIO \_ ADDRESS LIST \_ \_ QUERY** IOCTL wird unter Windows 2000 und höher des Betriebssystems unterstützt.

Der **SIO \_ ADDRESS LIST \_ QUERY-Steuerungscode \_** erhält eine Liste der lokalen Transportadressen der Protokollfamilie des Sockets, an die die Anwendung gebunden werden kann.
Die Liste der Adressen variiert je nach Adressfamilie.

Für die AF \_ INET6-Adressfamilie werden alle Adressen zurückgegeben, mit Ausnahme der folgenden:

* Jede IP-Adresse, bei der der Status der Erkennung doppelter Adressen (Duplicate Address Detection, DAD) nicht IpDadStatePreferred ist.
* Jede IP-Adresse mit einer Bereichsebene, die niedriger als ScopeLevelSubnet auf einer Schnittstelle ist, bei der der Schnittstellentyp **IF \_ TYPE SOFTWARE \_ \_ LOOPBACK ist.**
Dies bedeutet, dass link-local (fe80:*) und Loopbackadressen (::1) für Schnittstellen des **IF \_ TYPE SOFTWARE \_ \_ LOOPBACK-Typs** ausgeschlossen werden, aber nicht, wenn sich diese Adressen auf einer Schnittstelle mit einem anderen Typ befinden.

Für die **AF \_ INET-Adressfamilie** werden alle Adressen zurückgegeben, mit Ausnahme der folgenden:

* Jede IP-Adresse, bei der der Status der Erkennung doppelter Adressen (Duplicate Address Detection, DAD) nicht IpDadStatePreferred ist.
* Jede IP-Adresse auf einer Schnittstelle, deren Schnittstellentyp **IF \_ TYPE SOFTWARE \_ \_ LOOPBACK** und link local ist.
Dies bedeutet, dass lokale Linkadressen (169.254. ) und *Loopbackadressen (127.*) an Schnittstellen des **IF TYPE SOFTWARE \_ \_ \_ LOOPBACK-Typs** ausgeschlossen werden, aber nicht, wenn sich diese Adressen auf einer Schnittstelle mit einem anderen Typ befinden.

Weitere Informationen zum DAD-Zustand finden Sie in der Dokumentation zum IP-Hilfs hilfs für die [**IP \_ DAD \_ STATE-Enumeration**](/windows/desktop/api/nldef/ne-nldef-nl_dad_state) und die [**\_ \_ UNICAST \_ ADDRESS-Struktur**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_unicast_address_lh) des IP-Adapters und in der MIB-Dokumentation zur [**MIB \_ UNICASTIPADDRESS-ZEILENstruktur. \_**](/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row)
Weitere [**Informationen**](/windows/desktop/api/netioapi/ns-netioapi-mib_if_row2) zum Schnittstellentyp finden Sie in der DOKUMENTATION des IP-Hilfsers zur [**\_ IP-Adapter-ADDRESSES-Struktur \_**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_addresses_xp) und der [**GetAdaptersAddresses-Funktion**](/windows/desktop/api/iphlpapi/nf-iphlpapi-getadaptersaddresses) sowie in der MIB-Dokumentation zur MIB_IF_ROW2 Struktur.
Weitere Informationen zur Bereichsebene finden Sie in der DOKUMENTATION des IP-Hilfsers zur [**IP_ADAPTER_ADDRESSES-Struktur**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_addresses_xp) und der [**SCOPE \_ LEVEL-Enumeration.**](/windows/desktop/api/ws2def/ne-ws2def-scope_level)

Die Liste, die im Ausgabepuffer zurückgegeben wird, auf den der *lpvOutBuffer-Parameter* zeigt, hat die Form einer [**SOCKET ADDRESS \_ \_ LIST-Struktur.**](/windows/desktop/api/ws2def/ns-ws2def-socket_address_list)

Wenn der im *lpvOutBuffer-Parameter* angegebene Ausgabepuffer nicht groß genug ist, um die Adressliste zu enthalten, wird **SOCKET \_ ERROR** als Ergebnis dieser IOCTL zurückgegeben, und [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) gibt [WSAEFAULT zurück.](windows-sockets-error-codes-2.md)
Die erforderliche Größe für den Ausgabepuffer in Bytes wird in diesem Fall im *lpcbBytesReturned-Parameter* zurückgegeben.
Beachten Sie, dass der [WSAEFAULT-Fehlercode](windows-sockets-error-codes-2.md) auch zurückgegeben wird, wenn der *Parameter lpvInBuffer,* *lpvOutBuffer* oder *lpcbBytesReturned* nicht vollständig in einem gültigen Teil des Benutzeradressenbereichs enthalten ist.

Die **ABFRAGE-IOCTL der SIO-ADRESSLISTE \_ \_ \_** wird normalerweise synchron mit dem *Parameter lpvOverlapped* aufgerufen, der auf **NULL** festgelegt ist, da die Liste der Adressen sofort zurückgegeben wird.

**Hinweis:**  In Windows Plug-n-Play-Umgebungen können Adressen dynamisch hinzugefügt und entfernt werden.
Daher können Sich Anwendungen nicht darauf verlassen, dass die von **SIO \_ ADDRESS LIST \_ \_ QUERY** zurückgegebenen Informationen persistent sind.
Anwendungen können sich für Adressänderungsbenachrichtigungen über die **SIO \_ ADDRESS LIST \_ \_ CHANGE** IOCTL registrieren, die Benachrichtigungen über überlappende E/A- oder **FD ADDRESS LIST \_ \_ \_ CHANGE-Ereignisse** bietet.
Die folgende Aktionssequenz kann verwendet werden, um zu gewährleisten, dass die Anwendung immer über aktuelle Adresslisteninformationen verfügt:

* Ausgabe der **IOCTL-ÄNDERUNG \_ \_ DER \_ SIO-ADRESSLISTE**
* Ausgabe der **IOCTL-ABFRAGE DER \_ \_ \_ SIO-ADRESSLISTE**
* Wenn der IOCTL-Aufruf von **SIO \_ ADDRESS LIST \_ \_ CHANGE** die Anwendung über eine Änderung der Adressliste benachrichtigt (entweder durch überlappende E/A oder durch Signalisierung des **Ereignisses FD \_ ADDRESS LIST \_ \_ CHANGE),** sollte die gesamte Sequenz von Aktionen wiederholt werden.

Im Microsoft Windows Software Development Kit (SDK), das für Windows Vista und höher veröffentlicht wurde, hat sich die Organisation der Headerdateien geändert, und der ABFRAGE-Steuerungscode der **SIO-ADRESSLISTE \_ \_ \_** wird in der *Ws2def.h-Headerdatei* definiert.
Beachten Sie, dass die *Headerdatei Ws2def.h* automatisch in *Winsock2.h* enthalten ist und niemals direkt verwendet werden sollte.

## <a name="see-also"></a>Siehe auch

[**GetAdaptersAddresses**](/windows/desktop/api/iphlpapi/nf-iphlpapi-getadaptersaddresses)

[**IP_ADAPTER_ADDRESSES**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_addresses_xp)

[**IP_ADAPTER_UNICAST_ADDRESS**](/windows/desktop/api/iptypes/ns-iptypes-ip_adapter_unicast_address_lh)

[**IP_DAD_STATE**](/windows/desktop/api/nldef/ne-nldef-nl_dad_state)

[**MIB_IF_ROW2**](/windows/desktop/api/netioapi/ns-netioapi-mib_if_row2)

[**MIB_UNICASTIPADDRESS_ROW**](/windows/desktop/api/netioapi/ns-netioapi-mib_unicastipaddress_row)

[**SCOPE_LEVEL**](/windows/desktop/api/ws2def/ne-ws2def-scope_level)

[**SOCKET_ADDRESS_LIST**](/windows/desktop/api/ws2def/ns-ws2def-socket_address_list)

[**Socket**](/windows/desktop/api/winsock2/nf-winsock2-socket)

[**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)

[**WSAGetOverlappedResult**](/windows/desktop/api/winsock2/nf-winsock2-wsagetoverlappedresult)

[**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl)

[**WSAOVERLAPPED**](/windows/desktop/api/winsock2/ns-winsock2-wsaoverlapped)

[**WSASocketA**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketa)

[**WSASocketW**](/windows/desktop/api/winsock2/nf-winsock2-wsasocketw)
