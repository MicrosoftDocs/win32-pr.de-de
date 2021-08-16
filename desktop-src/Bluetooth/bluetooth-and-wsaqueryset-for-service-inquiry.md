---
title: Bluetooth und WSAQUERYSET für Dienstabfragen
description: Verwenden der WSAQUERYSET-Struktur mit den Funktionen WSALookupServiceBegin und WSALookupServiceNext, um Informationen zum Dienstabfrageprozess zu erhalten.
ms.assetid: c52a7e7d-92ab-4103-a6c6-57c3fafec706
keywords:
- Bluetooth und WSAQUERYSET für Dienstabfragen Bluetooth
- WSAQUERYSET Bluetooth , für Dienstabfragen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a38bd953f8d205f0afb097ec2d098ee674a01d5fc37cfbaf4109e02cdbb4b395
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118959159"
---
# <a name="bluetooth-and-wsaqueryset-for-service-inquiry"></a>Bluetooth und WSAQUERYSET für Dienstabfragen

Bluetooth verwendet die [**WSAQUERYSET-Struktur**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) mit verschiedenen Funktionen, um die Ermittlung von Geräten und Diensten im Bluetooth Namespace, NS \_ BTH, zu erleichtern.

Die [**Funktionen WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) und [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) verwenden die [**WSAQUERYSET-Struktur,**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) um Daten zum Dienstabfrageprozess zu erhalten. In der folgenden Tabelle wird beschrieben, wie die Memberwerte in der **WSAQUERYSET-Struktur** für diesen Zweck festgelegt werden.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Member</th>
<th>Eingabe für WSALookupServiceBegin</th>
<th>Zurückgegebener Wert von WSALookupServiceNext</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>dwSize</strong></td>
<td>Muss auf <strong>sizeof</strong>(<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET ) festgelegt werden.</strong></a></td>
<td><strong>sizeof</strong>(<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a>) wird vom System zurückgegeben.</td>
</tr>
<tr class="even">
<td><strong>dwOutputFlags</strong></td>
<td>Nicht verwendet.</td>
<td>Nicht verwendet.</td>
</tr>
<tr class="odd">
<td><strong>lpszServiceInstanceName</strong></td>
<td>Wird nicht verwendet.</td>
<td>Anzeigename des Diensts, konvertiert als UTF-8-codierte Zeichenfolge aus der Standardsprachcodierung des Bluetooth ServiceName-SDP-Attributs. Wird zurückgegeben, LUP_RETURN_NAME angegeben ist.</td>
</tr>
<tr class="even">
<td><strong>lpServiceClassId</strong></td>
<td>Erforderlich. Die spezifischste Bluetooth UUID für die Dienste, für die die Suche durchgeführt wird. Wenn dieser Wert beispielsweise auf die UUID des L2CAP-Protokolls festgelegt ist, werden alle Dienste zurückgegeben, die das L2CAP-Protokoll auf dem Zielgerät verwenden. Wenn sie auf die UUID eines bestimmten Diensts festgelegt ist, werden nur die Instanzen dieses Diensts zurückgeben.</td>
<td>Wird nicht verwendet.</td>
</tr>
<tr class="odd">
<td><strong>lpVersion</strong></td>
<td>Nicht verwendet.</td>
<td>Nicht verwendet.</td>
</tr>
<tr class="even">
<td><strong>lpszComment</strong></td>
<td>Wird nicht verwendet.</td>
<td>Beschreibung des Diensts, konvertiert als UTF-8-codierte Zeichenfolge aus der Standardsprachcodierung des Bluetooth ServiceDescription-SDP-Attributs. Wird <strong>zurückgegeben, LUP_RETURN_COMMENT</strong> angegeben ist.</td>
</tr>
<tr class="odd">
<td><strong>dwNameSpace</strong></td>
<td>Muss NS_BTH.</td>
<td>Gibt NS_BTH.</td>
</tr>
<tr class="even">
<td><strong>lpNSProviderId</strong></td>
<td>Nicht verwendet.</td>
<td>Nicht verwendet.</td>
</tr>
<tr class="odd">
<td><strong>lpszContext</strong></td>
<td>Erforderlich. Die Bluetooth Geräteadresse, mit der eine SDP-Verbindung hergestellt und Dienste abfragen werden. Dieser Wert muss eine Zeichenfolge sein, die mithilfe des <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa"><strong>WSAAddressToString-Funktionsaufrufs</strong></a> konvertiert wurde. Wenn die lokale Bluetooth angegeben wird, wird die lokale SDP-Datenbank durchsucht.</td>
<td>Wird nicht verwendet.</td>
</tr>
<tr class="even">
<td><strong>dwNumberOfProtocols</strong></td>
<td>Nicht verwendet.</td>
<td>Nicht verwendet.</td>
</tr>
<tr class="odd">
<td><strong>lpafpProtocols</strong></td>
<td>Nicht verwendet.</td>
<td>Nicht verwendet.</td>
</tr>
<tr class="even">
<td><strong>lpszQueryString</strong></td>
<td>Nicht verwendet.</td>
<td>Nicht verwendet.</td>
</tr>
<tr class="odd">
<td><strong>dwNumberOfCsAddrs</strong></td>
<td>Wird nicht verwendet.</td>
<td>Gibt die Anzahl der Elemente im Array der <a href="/windows/desktop/api/nspapi/ns-nspapi-csaddr_info"><strong>CSADDR_INFO</strong></a> an.</td>
</tr>
<tr class="even">
<td><strong>lpcsaBuffer</strong></td>
<td>Wird nicht verwendet.</td>
<td>Zeiger auf eine <a href="/windows/desktop/api/nspapi/ns-nspapi-csaddr_info"><strong>CSADDR_INFO-Struktur,</strong></a> deren <strong>LocalAddr.lpSockaddr-Member</strong> auf ein <a href="/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth"><strong>SOCKADDR_BTH-Objekt verweist,</strong></a> das die vollständige verbindungsfähige Adresse des Remotediensts enthält, die aus dem ersten Eintrag des Bluetooth ProtocolDescriptorList-SDP-Attributs konvertiert wurde. Wird <strong>zurückgegeben, LUP_RETURN_ADDR</strong> angegeben ist.</td>
</tr>
<tr class="odd">
<td><strong>lpBlob</strong></td>
<td>Optional. Zeiger auf eine <a href="/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service"><strong>BTH_QUERY_SERVICE</strong></a> struktur, die erweiterte Parameter enthält, um die Ergebnisse der Suche zu begrenzen. Falls angegeben, <strong>wird lpServiceClassId</strong> ignoriert, und zwischengespeicherte Abfragen sind nicht erfolgreich.</td>
<td><ul>
<li>Wenn eine Dienstsuche ausgeführt wird: Zeiger auf eine <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>BLOB-Struktur,</strong></a> die die Diensthandles zurückgibt. (<strong>BLOB.cbSize</strong><strong>)/sizeof</strong>(ULONG) berechnet die Anzahl der Handles. <strong>BLOB.pBlobData ist</strong> ein Array von ULONG-Werten, die die Diensthandles darstellen.</li>
<li>Wenn eine Attribut- oder serviceAttribute-Suche <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong></strong></a> ausgeführt wird: Zeiger auf eine BLOB-Struktur, die den binären SDP-Datensatz zurückgibt. <strong>BLOB.cbSize ist</strong> die Größe des binären SDP-Eintrags. <strong>BLOB.pBlobData</strong> verweist auf den Datensatz selbst. Der binäre SDP-Datensatz ist in vielen Fällen erforderlich, da nur eine begrenzte Anzahl von SDP-Attributen in die <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET-Struktur</strong></a> konvertiert werden kann und nur standardmäßig codierte UTF-8-Zeichenfolgen konvertiert werden. Funktionen zur Unterstützung bei der Analyse des binären SDP-Eintrags finden Sie im Abschnitt <a href="bluetooth-reference.md">Bluetooth Referenz.</a></li>
<li>Wird zurückgegeben, LUP_RETURN_BLOB angegeben ist.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Bluetooth und WSAQUERYSET für Set Service](bluetooth-and-wsaqueryset-for-set-service.md)
</dt> <dt>

[Bluetooth und WSAQUERYSET für die Geräteabfrage](bluetooth-and-wsaqueryset-for-device-inquiry.md)
</dt> <dt>

[Bluetooth und BLOB](bluetooth-and-blob.md)
</dt> <dt>

[Bluetooth und WSALookupServiceBegin](bluetooth-and-wsasetservice.md)
</dt> <dt>

Bluetooth und WSALookupServiceNext
</dt> <dt>

[Bluetooth Verweis](bluetooth-reference.md)
</dt> <dt>

[**Blob**](/windows/desktop/api/nspapi/ns-nspapi-blob)
</dt> <dt>

[**\_BTH-ABFRAGEDIENST \_**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service)
</dt> <dt>

[**\_CSADDR-INFORMATIONEN**](/windows/desktop/api/nspapi/ns-nspapi-csaddr_info)
</dt> <dt>

[**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)
</dt> <dt>

[**WSAAddressToString**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa)
</dt> <dt>

[**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[Windows-Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

 

 