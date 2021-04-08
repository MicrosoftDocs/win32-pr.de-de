---
title: Bluetooth und wsaqueryset für die Dienst Anfrage
description: Verwenden der wsaqueryset-Struktur mit den Funktionen wsalookupservicebegin und WSALookupServiceNext, um Informationen über den Dienst Anfrage Prozess zu erhalten.
ms.assetid: c52a7e7d-92ab-4103-a6c6-57c3fafec706
keywords:
- Bluetooth und wsaqueryset für Dienst Anfrage Bluetooth
- Wsaqueryset Bluetooth, für Dienst Anfrage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 656fa407829112005c9c54c5ab84c9c1bf2f4e33
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/08/2020
ms.locfileid: "103732201"
---
# <a name="bluetooth-and-wsaqueryset-for-service-inquiry"></a>Bluetooth und wsaqueryset für die Dienst Anfrage

Bluetooth verwendet die [**wsaqueryset**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) -Struktur mit verschiedenen Funktionen, um die Ermittlung von Geräten und Diensten im Bluetooth-Namespace (NS BTH) zu vereinfachen \_ .

Die Funktionen [**wsalookupservicebegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) und [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) verwenden die [**wsaqueryset**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) -Struktur zum Abrufen von Daten über den Dienst Anfrage Prozess. In der folgenden Tabelle wird beschrieben, wie die Element Werte in der **wsaqueryset** -Struktur zu diesem Zweck festgelegt werden.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Member</th>
<th>Eingabe für wsalookupservicebegin</th>
<th>Rückgabewert von WSALookupServiceNext</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>dwSize</strong></td>
<td>Muss auf <strong>sizeof</strong>(<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>wsaqueryset</strong></a>) festgelegt werden.</td>
<td><strong>sizeof</strong>(<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>wsaqueryset</strong></a>) vom System zurückgegeben.</td>
</tr>
<tr class="even">
<td><strong>dwoutputflags</strong></td>
<td>Nicht verwendet.</td>
<td>Nicht verwendet.</td>
</tr>
<tr class="odd">
<td><strong>lpszserviceingestancename</strong></td>
<td>Nicht verwendet.</td>
<td>Der Anzeige Name des dienstans, der als UTF-8-codierte Zeichenfolge aus der Standard sprach Codierung des SDP-Attributs für Bluetooth Service Name konvertiert wurde. Wird zurückgegeben, wenn LUP_RETURN_NAME angegeben wird.</td>
</tr>
<tr class="even">
<td><strong>lpserviceclassid</strong></td>
<td>Erforderlich. Die spezifischere einzelne Bluetooth-UUID für die Dienste, für die die Suche durchgeführt wird. Wenn dieser Wert beispielsweise auf die UUID des L2CAP-Protokolls festgelegt ist, werden alle Dienste zurückgegeben, die das L2CAP-Protokoll auf dem Zielgerät verwenden. Wenn die UUID für einen bestimmten Dienst auf festgelegt ist, werden nur die Instanzen dieses Dienstanbieter zurückgegeben.</td>
<td>Nicht verwendet.</td>
</tr>
<tr class="odd">
<td><strong>lpversion</strong></td>
<td>Nicht verwendet.</td>
<td>Nicht verwendet.</td>
</tr>
<tr class="even">
<td><strong>lpszcomment</strong></td>
<td>Nicht verwendet.</td>
<td>Die Beschreibung des Dienstes, konvertiert als UTF-8-codierte Zeichenfolge aus der Standard sprach Codierung des SDP-Attributs für Bluetooth Service Description. Wird zurückgegeben, wenn <strong>LUP_RETURN_COMMENT</strong> angegeben wird.</td>
</tr>
<tr class="odd">
<td><strong>dwnamespace</strong></td>
<td>Muss NS_BTH werden.</td>
<td>Gibt NS_BTH zurück.</td>
</tr>
<tr class="even">
<td><strong>lpnsproviderid</strong></td>
<td>Nicht verwendet.</td>
<td>Nicht verwendet.</td>
</tr>
<tr class="odd">
<td><strong>lpszcontext</strong></td>
<td>Erforderlich. Die Bluetooth-Geräteadresse, mit der eine SDP-Verbindung hergestellt und Dienste abgefragt werden. Dieser Wert muss eine Zeichenfolge sein, die mithilfe des <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa"><strong>wsaadresssstostring</strong></a> -Funktions Aufrufes konvertiert wurde. Wenn die lokale Bluetooth-Geräteadresse angegeben wird, wird die lokale SDP-Datenbank durchsucht.</td>
<td>Nicht verwendet.</td>
</tr>
<tr class="even">
<td><strong>dwnumofprotokolle</strong></td>
<td>Nicht verwendet.</td>
<td>Nicht verwendet.</td>
</tr>
<tr class="odd">
<td><strong>lpafpprotokolle</strong></td>
<td>Nicht verwendet.</td>
<td>Nicht verwendet.</td>
</tr>
<tr class="even">
<td><strong>lpszquerystring</strong></td>
<td>Nicht verwendet.</td>
<td>Nicht verwendet.</td>
</tr>
<tr class="odd">
<td><strong>dwnumofcsaddrs</strong></td>
<td>Nicht verwendet.</td>
<td>Gibt die Anzahl der Elemente im Array von <a href="/windows/desktop/api/nspapi/ns-nspapi-csaddr_info"><strong>CSADDR_INFO</strong></a> Strukturen an.</td>
</tr>
<tr class="even">
<td><strong>lpcsabuffer</strong></td>
<td>Nicht verwendet.</td>
<td>Ein Zeiger auf eine <a href="/windows/desktop/api/nspapi/ns-nspapi-csaddr_info"><strong>CSADDR_INFO</strong></a> -Struktur, deren <strong>localaddr. lpsockaddr</strong> -Member auf einen <a href="/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth"><strong>SOCKADDR_BTH</strong></a> verweist, der die komplette Verbindungs fähigen-Adresse des Remote Dienes enthält, die aus dem ersten Eintrag des SDP-Attributs für Bluetooth protocoldescriptorlist konvertiert wurde. Wird zurückgegeben, wenn <strong>LUP_RETURN_ADDR</strong> angegeben wird.</td>
</tr>
<tr class="odd">
<td><strong>lpblob</strong></td>
<td>Dies ist optional. Ein Zeiger auf eine <a href="/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service"><strong>BTH_QUERY_SERVICE</strong></a> Struktur, die erweiterte Parameter enthält, um die Suchergebnisse einzuschränken. Wenn angegeben, wird " <strong>lpserviceclassid</strong> " ignoriert, und zwischengespeicherte Abfragen sind nicht erfolgreich.</td>
<td><ul>
<li>Wenn eine Dienst Suche durchgeführt wird: Zeiger auf eine <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>BLOB</strong></a> -Struktur, die die Dienst Handles zurückgibt. (<strong>BLOB. cbSize</strong>)/<strong>sizeof</strong>(ULONG) berechnet die Anzahl der Handles. <strong>BLOB. pblobdata</strong> ist ein Array von ULONG-Werten, die die Dienst Handles darstellen.</li>
<li>Wenn ein Attribut oder eine Service Attribute-Suche ausgeführt wird: Zeiger auf eine <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>BLOB</strong></a> -Struktur, die den binären SDP-Datensatz zurückgibt. <strong>BLOB. cbSize</strong> ist die Größe des binären SDP-Datensatzes. <strong>BLOB. pblobdata</strong> verweist auf den Datensatz selbst. Der binäre SDP-Datensatz ist in vielen Fällen erforderlich, da nur eine begrenzte Anzahl von SDP-Attributen in die <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>wsaqueryset</strong></a> -Struktur konvertiert werden kann und nur standardmäßige verschlüsselte UTF-8-Zeichen folgen konvertiert werden. Funktionen zur Unterstützung bei der Verarbeitung des binären SDP-Datensatzes finden Sie im Abschnitt zur <a href="bluetooth-reference.md">Bluetooth-Referenz</a> .</li>
<li>Wird zurückgegeben, wenn LUP_RETURN_BLOB angegeben wird.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Bluetooth und wsaqueryset für Set Service](bluetooth-and-wsaqueryset-for-set-service.md)
</dt> <dt>

[Bluetooth und wsaqueryset für Geräte Anfrage](bluetooth-and-wsaqueryset-for-device-inquiry.md)
</dt> <dt>

[Bluetooth und BLOB](bluetooth-and-blob.md)
</dt> <dt>

[Bluetooth und wsalookupservicebegin](bluetooth-and-wsasetservice.md)
</dt> <dt>

Bluetooth und WSALookupServiceNext
</dt> <dt>

[Bluetooth-Referenz](bluetooth-reference.md)
</dt> <dt>

[**BLOB**](/windows/desktop/api/nspapi/ns-nspapi-blob)
</dt> <dt>

[**BTH- \_ Abfrage \_ Dienst**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service)
</dt> <dt>

[**csaddr- \_ Informationen**](/windows/desktop/api/nspapi/ns-nspapi-csaddr_info)
</dt> <dt>

[**sockaddr- \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)
</dt> <dt>

[**Wsaadresssstostring**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa)
</dt> <dt>

[**Wsaqueryset**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[Windows-Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

 

 