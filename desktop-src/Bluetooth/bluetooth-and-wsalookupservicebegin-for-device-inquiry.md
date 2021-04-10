---
title: Bluetooth und wsalookupservicebegin für Geräte Anfrage
description: In diesem Thema wird beschrieben, wie Sie die wsalookupservicebegin-Funktion verwenden, um eine Abfrage von sichtbaren und Ghosting-Geräten auszuführen. Weitere Informationen finden Sie unter Ermitteln von Bluetooth-Geräten und-Diensten.
ms.assetid: 32fa710f-8645-4cf3-a882-cc032d66d979
keywords:
- Bluetooth und wsalookupservicebegin für Geräte Anfrage Bluetooth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dfbcab2a3134289630b4b301390f85e83d1d3d0
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/08/2020
ms.locfileid: "104102474"
---
# <a name="bluetooth-and-wsalookupservicebegin-for-device-inquiry"></a>Bluetooth und wsalookupservicebegin für Geräte Anfrage

In diesem Thema wird beschrieben, wie Sie die [**wsalookupservicebegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) -Funktion verwenden, um eine Abfrage von sichtbaren und Ghosting-Geräten auszuführen. Weitere Informationen finden Sie unter Ermitteln von [Bluetooth-Geräten und-Diensten](discovering-bluetooth-devices-and-services.md).

Die [**wsalookupservicebegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) -Funktion verwendet eine [**wsaqueryset**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) -Struktur in Ihrem ersten Parameter *lpqsrestrictions*, um Suchkriterien zu definieren. Bluetooth bietet spezielle Richtlinien für die Verwendung der **wsalookupservicebegin** -Funktion und von **wsaqueryset**.

In der folgenden Tabelle werden die Einschränkungen aufgelistet, die für die [**wsaqueryset**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) -Struktur gelten, die beim Abfragen von Geräten an den *lpqsrestrictions* -Parameter übergeben wird.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Wsaqueryset-Member</th>
<th>Einschränkung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>dwSize</strong></td>
<td>Auf <strong>sizeof</strong>(<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>wsaqueryset</strong></a>) festgelegt.</td>
</tr>
<tr class="even">
<td><strong>lpblob</strong></td>
<td>Dieser Member enthält einen optionalen Zeiger auf eine <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>BLOB</strong></a> -Struktur. Wenn dieser Member angegeben wird, sind die gültigen Parameter für die Geräte Anfrage für <strong>LUP_FLUSHCACHE</strong> wie folgt:
<ul>
<li>Der <strong>CBSIZE</strong> -Member der <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>BLOB</strong></a> -Struktur muss <strong>sizeof</strong>(<strong>BTH_QUERY_DEVICE</strong>) sein.</li>
<li>Der <strong>pblobdata</strong> -Member ist ein Zeiger auf eine <a href="/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device"><strong>BTH_QUERY_DEVICE</strong></a> -Struktur, für die das <strong>Lap</strong> -Element der Bluetooth-Abfrage Zugriffs Code ist, und der <strong>Längen</strong> Member ist die Länge der Abfrage in Sekunden.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>dwnamespace</strong></td>
<td>Legen Sie auf <strong>NS_BTH</strong>fest.</td>
</tr>
<tr class="even">
<td>Andere Member</td>
<td>Andere <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>Member der wsaqueryset</strong></a> -Struktur werden ignoriert.</td>
</tr>
</tbody>
</table>



 

Die in der folgenden Tabelle aufgeführten Flags werden im *dwcontrolflags* -Parameter verwendet, um die Abfrageergebnisse zu steuern. Die Flags " **Lup \_ Containers** " und " **Lup \_ flushcache** " werden von der [**wsalookupservicebegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) -Funktion verwendet. die restlichen Flags werden bei Aufrufen der [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) -Funktion verwendet.

| Flag               | Ergebnis                                                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_lupcontainer    | Gibt an, dass der Abfrage Zweck darin besteht, eine Liste von Bluetooth-Geräten und keine Liste der Dienste abzurufen. Dieses Flag muss festgelegt werden.                                                                                                                                                                                                                                                                                       |
| \_leeren von flushcache    | Löst eine Abfrage lokaler Geräte aus oder bewirkt, dass zwischengespeicherte Ergebnisse früherer Abfragen zurückgegeben werden.                                                                                                                                                                                                                                                                                                                |
| - \_ \_ Rückgabetyp  | Gibt den Bluetooth-COD (Klasse von Device Bits) direkt im **lpserviceclassid-** Member der [**wsaqueryset**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) -Struktur zurück. Der COD wird dem **data1** -Member der GUID zugeordnet.                                                                                                                                                                                                      |
| Lup \_ Res- \_ Dienst  | Gibt Informationen für die lokale Bluetooth-Adresse zurück. Dieses Flag wirkt sich nur dann aus, wenn die **\_ \_ addr-Rückgabe** Wert-Rückgabe ebenfalls angegeben wird.                                                                                                                                                                                                                                                                                       |
| Name der Lup- \_ Rückgabe \_  | Gibt den anzeigen amen des Geräts im **lpszserviceinstancename** -Member der [**wsaqueryset**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) -Struktur für jeden Aufrufen der [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) -Funktion zurück. Dieses Flag muss auch angegeben werden, um das **Name** -Element der [**BTH- \_ Geräte \_ Informations**](/windows/desktop/api/Bthdef/ns-bthdef-bth_device_info) Struktur abzurufen, wenn das **Lup- \_ rückgabeblobflag \_** angegeben wird. |
| Lup \_ Return \_ addr  | Gibt eine [**sockaddr- \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) -Struktur zurück, die die 48-Bit-Adresse des Peers im **lpcsabuffer** -Member der [**wsaqueryset**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) -Struktur für jeden Aufrufe der [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) -Funktion enthält. Andere Member in der **sockaddr- \_ BTH** -Struktur sind leer.                                                            |
| Lup- \_ Rückgabe- \_ BLOB  | Zurückgeben der [**BTH- \_ Geräte \_ Informations**](/windows/desktop/api/Bthdef/ns-bthdef-bth_device_info) Struktur bei jedem nachfolgenden [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta)-Rückruf.                                                                                                                                                                                                                                                           |
| Lup- \_ flushprevious | Überspringen Sie das nächste verfügbare Gerät, und geben Sie das Gerät an, das darauf folgt.                                                                                                                                                                                                                                                                                                                                             |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Bluetooth und wsalookupservicebegin für die Dienst Ermittlung](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)
</dt> <dt>

[Bluetooth und WSALookupServiceNext](bluetooth-and-wsalookupservicenext.md)
</dt> <dt>

[Bluetooth und wsaqueryset für Geräte Anfrage](bluetooth-and-wsaqueryset-for-device-inquiry.md)
</dt> <dt>

[Ermitteln von Bluetooth-Geräten und -Diensten](discovering-bluetooth-devices-and-services.md)
</dt> <dt>

[**Wsalookupservicebegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)
</dt> <dt>

[**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta)
</dt> <dt>

[**WSALookupServiceEnd**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupserviceend)
</dt> <dt>

[**BLOB**](/windows/desktop/api/nspapi/ns-nspapi-blob)
</dt> <dt>

[**BTH- \_ Abfrage \_ Gerät**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device)
</dt> <dt>

[**sockaddr- \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)
</dt> <dt>

[**Wsaqueryset**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[Windows-Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

 

 