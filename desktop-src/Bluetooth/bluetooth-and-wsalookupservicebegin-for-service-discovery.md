---
title: Bluetooth und wsalookupservicebegin für die Dienst Ermittlung
description: Um zu ermitteln, ob ein bestimmter Dienst auf einem Bluetooth-Server vorhanden ist, verwenden Clients die Funktionen wsalookupservicebegin, WSALookupServiceNext und WSALookupServiceEnd.
ms.assetid: d9961600-cdca-42ec-92eb-118b8186ed2e
keywords:
- Bluetooth und wsalookupservicebegin für die Dienst Ermittlung Bluetooth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 274b3beb3de7683bd43a0f99350db6e1a347f51e
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/08/2020
ms.locfileid: "103858525"
---
# <a name="bluetooth-and-wsalookupservicebegin-for-service-discovery"></a>Bluetooth und wsalookupservicebegin für die Dienst Ermittlung

Um zu ermitteln, ob ein bestimmter Dienst auf einem Bluetooth-Server vorhanden ist, verwenden Clients die Funktionen [**wsalookupservicebegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina), [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta)und [**WSALookupServiceEnd**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupserviceend) . Abfragen können für lokale und Remote Adressen ausgeführt werden, aber Verbindungen können nur mit Remote Adressen hergestellt werden. Während dieses Vorgangs erkannte Dienst Handles können nicht verwendet werden, um den Dienst über [**wsasetservice**](/windows/desktop/api/winsock2/nf-winsock2-wsasetservicea)zu löschen. Loopback wird von RFCOMM nicht unterstützt.

Es können zwei grundlegende Arten von Service Discovery-Abfragen ausgeführt werden:

-   Abfragen für einen oder mehrere Dienste auf dem lokalen Gerät
-   Abfragen für einen oder mehrere Dienste auf einem angegebenen peergerät

Die [**wsalookupservicebegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) -Funktion empfängt eine [**wsaqueryset**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) -Struktur im *lpqsrestrictions* -Parameter. **Wsalookupservicebegin** führt eine Client Abfrage basierend auf dem Satz von Such Einschränkungen aus, die das **wsaqueryset** enthält. Bluetooth-Clients müssen die in der folgenden Tabelle aufgeführten Einschränkungen in der **wsaqueryset** -Struktur angeben, wenn Sie die **wsalookupservicebegin** -Funktion verwenden, um Dienste abzufragen.



| Wsaqueryset-Member    | Einschränkung                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **dwSize**            | Auf **sizeof**([**wsaqueryset**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)) festgelegt.                                                                                                                                                                                                                                                                                                                    |
| **lpserviceclassid**  | Legen Sie auf die spezifischere Bluetooth-UUID fest, die verwendet werden kann, um den Abfrage Bereich zu bestimmen. Wenn Sie z. **b. lpserviceclassid** auf die UUID des L2CAP-Protokolls festlegen, werden alle L2CAP-Dienste zurückgegeben, wobei im Grunde alle SD-Datensätze auf dem Ziel aufgelistet werden. Wenn Sie die UUID auf einen bestimmten Dienst festlegen, werden jedoch nur die Instanzen dieses Dienstanbieter zurückgegeben.<br/> |
| **dwnamespace**       | Legen Sie auf **NS- \_ BTH** fest.                                                                                                                                                                                                                                                                                                                                                             |
| **dwnumofcsaddrs** | Auf 0 festlegen.                                                                                                                                                                                                                                                                                                                                                                       |
| **lpszcontext**       | Legen Sie auf die Bluetooth-Geräteadresse fest, mit der eine SDP-Verbindung hergestellt werden soll, um die Abfrage der Dienste auszuführen. Dieser Member muss eine Zeichenfolge sein, die mithilfe der [**wsaadresssstostring**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) -Funktion konvertiert wird. Wenn die lokale Radio Adresse angegeben wird, werden die lokalen SDP-Datensätze durchsucht.<br/>                                             |
| Andere Member         | Alle anderen [**Member der wsaqueryset**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) -Struktur werden ignoriert.                                                                                                                                                                                                                                                                                        |



 

Die SDP-Verbindung mit dem Remote Gerät bleibt nach Abschluss einer Dienst [](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) Abfrage nicht mehr aktiv. die Verbindung wird beendet, bevor **wsalookupservicebegin** zurückgegeben wird. Anwendungen, die erfordern, dass die SDP-Verbindung aktiv bleibt, nachdem eine Dienst Abfrage abgeschlossen ist, sollten die Dienstklasse UUID angeben, mit der eine Verbindung hergestellt werden soll, indem der **serviceclassid-** Member der [**sockaddr- \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) -Struktur beim Ausgeben des Windows Sockets [**Connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) -Funktionsaufruf

Die in der folgenden Tabelle aufgeführten Flags werden im *dwcontrolflags* -Parameter der [**wsalookupservicebegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) -Funktion und der [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) -Funktion verwendet, um die Abfrageergebnisse zu steuern. Die Flags " **Lup \_ Containers** " und " **Lup \_ flushcache** " werden von der **wsalookupservicebegin** -Funktion verwendet. die restlichen Flags werden bei Aufrufen der **WSALookupServiceNext** -Funktion verwendet.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Flag</th>
<th>Ergebnis</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>LUP_CONTAINERS</strong></td>
<td>Darf nicht festgelegt werden.</td>
</tr>
<tr class="even">
<td><strong>LUP_FLUSHCACHE</strong></td>
<td>Anwendungen sollten im allgemeinen <strong>LUP_FLUSHCACHE</strong>angeben. Dieses Flag weist das System an, alle zwischengespeicherten Informationen zu ignorieren und eine über-Air-SDP-Verbindung mit dem angegebenen Gerät herzustellen, um die SDP-Suche auszuführen. Dieser nicht zwischengespeicherte Vorgang kann mehrere Sekunden dauern (während eine zwischengespeicherte Suche schnell zurückgegeben wird). Bluetooth speichert SDP-Einträge derzeit nicht proaktiv von Geräten in der Nähe, und es werden zurzeit keine früheren Abfragen zwischengespeichert. Daher sollten Sie davon ausgehen, dass Abfragen möglicherweise keine Ergebnisse zurückgeben (mit dem Fehlercode <strong>WSASERVICE_NOT_FOUND</strong>), wenn <strong>LUP_FLUSHCACHE</strong> nicht angegeben ist. Die zwischengespeicherten Daten, die über die Windows Sockets-Schnittstelle verfügbar sind, können in Zukunft verbessert werden.</td>
</tr>
<tr class="odd">
<td><strong>LUP_RES_SERVICE</strong></td>
<td>Gibt Informationen zur lokalen Bluetooth-Adresse zurück. Dieses Flag hat nur dann Auswirkungen, wenn <strong>LUP_RETURN_ADDR</strong> ebenfalls angegeben ist.</td>
</tr>
<tr class="even">
<td><strong>LUP_RETURN_NAME</strong></td>
<td>Gibt den anzeigen amen des <strong>Dienstanbieter im lpszserviceinstancename</strong> -Member der <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>wsaqueryset</strong></a> -Struktur für jeden Aufrufen der <a href="/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta"><strong>WSALookupServiceNext</strong></a> -Funktion zurück.</td>
</tr>
<tr class="odd">
<td><strong>LUP_RETURN_TYPE</strong></td>
<td>Gibt die Dienst Klassen-ID im <strong>lpserviceclassid-</strong> Member der <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>wsaqueryset</strong></a> -Struktur zurück.
<blockquote>
[!Note]<br />
Die Verwendung dieses Flags gilt nur für die <a href="/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina"><strong>wsalookupservicebegin</strong></a> -Funktion. Dieser Wert ist für <a href="/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta"><strong>WSALookupServiceNext</strong></a>immer 0 (null).
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><strong>LUP_RETURN_ADDR</strong></td>
<td>Gibt eine Adresse im <strong>lpcsabuffer</strong> -Member zurück, die mit <a href="/windows/desktop/api/winsock2/nf-winsock2-connect"><strong>Verbindungs</strong></a> Funktionsaufrufen verwendet werden soll. Die zurückgegebene Adresse enthält die Portnummer.</td>
</tr>
<tr class="odd">
<td><strong>LUP_RETURN_BLOB</strong></td>
<td>Gibt die übereinstimmenden SD-Einträge im <strong>lpblob</strong> -Member zurück, die gemäß der Bluetooth-SDP-Daten Satz Spezifikation formatiert sind.</td>
</tr>
<tr class="even">
<td><strong>LUP_RETURN_ALL</strong></td>
<td>Gibt alle obigen Flags-Informationen zurück.</td>
</tr>
<tr class="odd">
<td><strong>LUP_RETURN_COMMENT</strong></td>
<td>Geben Sie die Dienst Beschreibung im <strong>lpszcomment</strong> -Member der <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>wsaqueryset</strong></a> -Struktur für jeden Aufrufe der <a href="/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta"><strong>WSALookupServiceNext</strong></a> -Funktion zurück.</td>
</tr>
<tr class="even">
<td><strong>LUP_FLUSHPREVIOUS</strong></td>
<td>Überspringen Sie den nächsten verfügbaren Datensatz, und geben Sie den darauf folgenden Datensatz zurück.</td>
</tr>
</tbody>
</table>



 

## <a name="advanced-service-queries"></a>Erweiterte Dienst Abfragen

Die Abfrage Vorgänge, die im vorherigen Abschnitt beschrieben werden, können verwendet werden, um alle Ergebnisse einer einzelnen GUID zurückzugeben, die für die meisten Anwendungen ausreichend sein sollten. Eine erweiterte Abfrage ermöglicht einer Anwendung, eine spezifischere Abfrage zu erstellen. Es bietet die Möglichkeit, UUIDs und Attribute in zurückgegebenen Informationen abzugleichen.

Zum Ausführen einer erweiterten Abfrage für-Dienste müssen Bluetooth-Clients die folgenden Einschränkungen in der [**wsaqueryset**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) -Struktur angeben, die an den *lpqsrestrictions* -Parameter übergeben wird.



| Wsaqueryset-Member   | Einschränkung                                                                                                                                                                                                                                                                                                                         |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **dwSize**           | Auf **sizeof**([**wsaqueryset**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)) festgelegt.                                                                                                                                                                                                                                                                        |
| **lpszcontext**      | Legen Sie auf die Bluetooth-Geräteadresse fest, mit der eine SDP-Verbindung hergestellt werden soll, um die Abfrage der Dienste auszuführen. Dieser Member muss eine Zeichenfolge sein, die mithilfe der [**wsaadresssstostring**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) -Funktion konvertiert wird. Wenn die lokale Radio Adresse angegeben wird, werden die lokalen SDP-Datensätze durchsucht.<br/> |
| **lpblob. pblobdata** | Ein Zeiger auf eine [**BTH- \_ Abfrage \_ Dienst**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service) Struktur, die alle Parameter enthält, die die Ergebnisse der Abfrage einschränken.                                                                                                                                                                                           |
| **dwnamespace**      | Legen Sie auf **NS- \_ BTH** fest.                                                                                                                                                                                                                                                                                                                 |
| Andere Member        | Alle anderen [**Member der wsaqueryset**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) -Struktur werden ignoriert.                                                                                                                                                                                                                                            |



 

Die folgenden Flags werden im *dwcontrolflags* -Parameter von [**wsalookupservicebegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) übergeben, um die Ergebnisse einer erweiterten Abfrage zu steuern.

| Flag                     | Ergebnis                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_lupcontainer**      | Darf nicht festgelegt werden.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| **\_leeren von flushcache**      | Anwendungen sollten in der Regel **Lup \_ flushcache** angeben. Dieses Flag weist das System an, alle zwischengespeicherten Informationen zu ignorieren und eine über-Air-SDP-Verbindung mit dem angegebenen Gerät herzustellen, um die SDP-Suche auszuführen. Dieser nicht zwischengespeicherte Vorgang kann mehrere Sekunden dauern (während eine zwischengespeicherte Suche schnell zurückgegeben wird). Bluetooth speichert SDP-Einträge nicht proaktiv von Geräten in der Nähe zwischen und führt auch keine aggressive Zwischenspeicherung vorheriger Abfragen aus. Daher sollten Anwendungen erwarten, dass Abfragen häufig keine Ergebnisse zurückgeben (**wsaservice \_ nicht \_ gefunden**), wenn " **Lup \_ flushcache** " nicht angegeben ist. Die zwischengespeicherten Daten, die über die Windows Sockets-Schnittstelle verfügbar sind, können in Zukunft verbessert werden. |
| **Lup \_ Res- \_ Dienst**    | Gibt Informationen für die lokale Bluetooth-Adresse zurück. Das Festlegen dieses Flags hat nur Auswirkungen, wenn " **Lup \_ Return \_ addrr** " ebenfalls angegeben wird.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| **Name der Lup- \_ Rückgabe \_**    | Gibt den anzeigen amen des Dienstanbieter zurück. Dieses Flag wird bei der **\_ \_ Suche nach \_ dem SDP-Dienst** ignoriert.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| **- \_ \_ Rückgabetyp**    | Gibt die Dienst Klassen-ID zurück. Dieses Flag wird bei der **\_ \_ Suche nach \_ dem SDP-Dienst** ignoriert.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **Lup \_ Return \_ addr**    | Gibt eine Adresse im **lpcsabuffer** -Member zurück, die mit [**Verbindungs**](/windows/desktop/api/winsock2/nf-winsock2-connect) Funktionsaufrufen verwendet werden soll. Die zurückgegebene Adresse enthält die Portnummer. Dieses Flag wird bei der **\_ \_ Suche nach \_ dem SDP-Dienst** ignoriert.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| **Lup- \_ Rückgabe- \_ BLOB**    | Gibt die übereinstimmenden SD-Einträge in einem Format zurück, das der Bluetooth-SDP-Daten Satz Spezifikation entspricht. Bei der **Such Anforderung des SDP- \_ \_ dienstantrags \_** ist das Ergebnis in **lpblob** für den nachfolgenden [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) -Befehl ein Array von Bluetooth-SDP-Handles. Für die Anforderung des **SDP- \_ Dienst \_ Attributs \_** und des **SDP- \_ Dienst \_ Such \_ Attributs \_** ist das Ergebnis für jeden nachfolgenden **WSALookupServiceNext** -Befehl ein binärer Bluetooth-SDP-Datensatz, dessen Attribute auf die Attribute beschränkt sind, die vom **Prange** -Member der Abfrage angegeben werden. Dieses Flag ist für die **Anforderung der SDP- \_ Dienst \_ \_ Suche** erforderlich.                                                               |
| **Lup- \_ Rückgabe \_ Kommentar** | Geben Sie die Dienst Beschreibung im **lpszcomment** -Member der [**wsaqueryset**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) -Struktur für jeden Aufrufe der [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) -Funktion zurück.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| **Lup- \_ flushprevious**   | Überspringen Sie den nächsten verfügbaren Datensatz, und geben Sie den darauf folgenden Datensatz zurück.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |



 

Bei der Eingabe verweist **lpblob** -> **pblobdata** auf eine [**BTH- \_ Abfrage \_ Dienst**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service) Struktur, die die in der folgenden Tabelle aufgeführten Werte enthält.

> [!Note]  
> Die anfängliche Such Anforderung muss in ein L2CAP-Paket eingefügt werden können. Die Antwort kann jedoch in viele L2CAP Pakete aufgeteilt werden.

 



| Member            | Wert                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|-------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **type**          | Der Typ der durchzuführenden Suche. Bei diesem Wert kann es sich um eine **SDP- \_ Dienst \_ Such \_ Anforderung**, eine **SDP- \_ Dienst \_ Attribut \_ Anforderung** oder eine **Anforderung des SDP- \_ Dienst \_ Such \_ Attributs \_** handeln. Jeder Suchtyp ist mit einem zugrunde liegenden Suchmechanismus verknüpft, der durch die Bluetooth-SDP-Spezifikation definiert wird. Jede Rückgabe ergibt sich in der Form, die von der zuvor in diesem Abschnitt (Advanced Service Queries) definierten [**wsaqueryset**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) -Struktur beschrieben wird. |
| **ServiceHandle** | Wird für Attribut suchen verwendet. Dieser Wert gibt das Dienst Handle an, mit dem die Attribute im **Prange** -Member abgefragt werden sollen.                                                                                                                                                                                                                                                                                                                                            |
| **UUIDs**         | Wird für Dienst-und Service **Attribute** -suchen verwendet. Dieser Wert gibt die UUIDs an, die ein Datensatz enthalten muss, damit er mit der Suche identisch ist. Wenn weniger als die **maximalen \_ UUIDs \_ in den \_ Abfrage** -UUIDs abgefragt werden sollen, legt dieser Wert das sdpqueryuuid-Element fest, das direkt der letzten gültigen UUID auf alle Nullen folgt.                                                                                                                                                                       |
| **numrange**      | Wird für Attribut-und **Service Attribute** -suchen verwendet. Dieser Wert gibt die Anzahl der Elemente in **Prange** an.                                                                                                                                                                                                                                                                                                                                                             |
| **Prange**        | Wird für Attribut-und **Service Attribute** -suchen verwendet. Dieser Wert gibt die Attributwerte an, die für übereinstimmende Datensätze abgerufen werden sollen.                                                                                                                                                                                                                                                                                                                                        |



 

Nach jedem erfolgreichen Aufrufe der [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) -Funktion verweist **lpblob** -> **pblobdata** auf einen Datenblock, der die in der folgenden Tabelle aufgeführten Werte enthält.

| Wert                                                                                | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                          |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **SDP- \_ Dienst \_ Such \_ Anforderung**                                                    | Ein Array von SDP-Daten Satz Handles, das mit der **servicerecordhandlelist** identisch ist, die von Bluetooth 1,1 SDP 4.5.2 definiert wird. Die Anzahl der zurückgegebenen SDP-Handles wird durch (**lpblob**->CBSIZE)/**sizeof**(ULONG) berechnet. Alle Ergebnisse werden in einem einzelnen Rückruf der [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) -Funktion zurückgegeben. |
| **SDP \_ Anforderung von Dienst \_ Attribut \_ Anforderung** oder **SDP- \_ Dienst \_ Such \_ Attribut \_** | Ein binärer Bluetooth-SDP-Datensatz. Bei der **Anforderung des SDP- \_ Dienst \_ Attributs \_** werden alle Ergebnisse in einem einzelnen Befehl der [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) -Funktion zurückgegeben.                                                                                                                                                       |



 

> [!Note]  
> Wenn das **lpblob** -Element während der Eingabe für eine Dienst Abfrage nicht angegeben wird, wird für den Dienst, der im **lpserviceclassid-** Member für Attribute von 0 bis 0xFFFF angegeben ist, eine Dienst-und Attribut Suche ausgeführt.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Bluetooth und wsaqueryset für die Dienst Anfrage](bluetooth-and-wsaqueryset-for-service-inquiry.md)
</dt> <dt>

[Ermitteln von Bluetooth-Geräten und -Diensten](discovering-bluetooth-devices-and-services.md)
</dt> <dt>

[Bluetooth und WSALookupServiceNext](bluetooth-and-wsalookupservicenext.md)
</dt> <dt>

[Bluetooth und wsalookupservicebegin für Geräte Anfrage](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)
</dt> <dt>

[**BTH- \_ Abfrage \_ Dienst**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service)
</dt> <dt>

[**herzustellen**](/windows/desktop/api/winsock2/nf-winsock2-connect)
</dt> <dt>

[**sockaddr- \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)
</dt> <dt>

[**Wsaadresssstostring**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa)
</dt> <dt>

[**Wsalookupservicebegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)
</dt> <dt>

[**WSALookupServiceEnd**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupserviceend)
</dt> <dt>

[**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta)
</dt> <dt>

[**Wsaqueryset**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[Windows-Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

