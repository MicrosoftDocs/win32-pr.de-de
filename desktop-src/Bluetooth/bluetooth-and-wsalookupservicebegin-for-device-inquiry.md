---
title: Bluetooth und WSALookupServiceBegin für die Geräteanfrage
description: In diesem Thema wird beschrieben, wie Sie die WSALookupServiceBegin-Funktion verwenden, um eine Abfrage von sichtbaren und in ghosted-Geräten durchzuführen. Weitere Informationen finden Sie unter Discovering Bluetooth Devices and Services (Erkennen von Bluetooth Und-Diensten).
ms.assetid: 32fa710f-8645-4cf3-a882-cc032d66d979
keywords:
- Bluetooth und WSALookupServiceBegin für Geräteanfrage-Bluetooth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8af56e1d75a66d21ea4eb94c827f6d37f77ae4336b8aeac5331665288bfeef49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118959289"
---
# <a name="bluetooth-and-wsalookupservicebegin-for-device-inquiry"></a>Bluetooth und WSALookupServiceBegin für die Geräteanfrage

In diesem Thema wird beschrieben, wie Sie die [**WSALookupServiceBegin-Funktion**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) verwenden, um eine Abfrage von sichtbaren und in ghosted-Geräten durchzuführen. Weitere Informationen finden Sie unter [Discovering Bluetooth Devices and Services](discovering-bluetooth-devices-and-services.md).

Die [**WSALookupServiceBegin-Funktion**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) verwendet eine [**WSAQUERYSET-Struktur**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) im ersten Parameter *lpqsRestrictions,* um Suchkriterien zu definieren. Bluetooth enthält spezifische Richtlinien für die Verwendung der **WSALookupServiceBegin-Funktion** und **WSAQUERYSET.**

In der folgenden Tabelle sind die Einschränkungen aufgeführt, die für die [**WSAQUERYSET-Struktur**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) gelten, die beim Abfragen von Geräten an den *lpqsRestrictions-Parameter* übergeben werden.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>WSAQUERYSET-Member</th>
<th>Einschränkung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>dwSize</strong></td>
<td>Legen Sie auf <strong>sizeof</strong>(<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET ) fest.</strong></a></td>
</tr>
<tr class="even">
<td><strong>lpBlob</strong></td>
<td>Dieser Member enthält einen optionalen Zeiger auf eine <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>BLOB-Struktur.</strong></a> Wenn dieser Member angegeben wird, lauten die gültigen Parameter für die <strong>Geräteerkundigung für</strong> LUP_FLUSHCACHE wie folgt:
<ul>
<li>Der <strong>cbSize-Member</strong> der <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>BLOB-Struktur</strong></a> muss <strong>sizeof</strong>( BTH_QUERY_DEVICE)<strong>sein.</strong></li>
<li>Das <strong>pBlobData-Element</strong> ist ein Zeiger auf eine <a href="/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device"><strong>BTH_QUERY_DEVICE-Struktur,</strong></a> für die das <strong>LAP-Element</strong> der <strong></strong> Bluetooth-Abfragezugriffscode und das Längenmitglied die Länge der Anfrage in Sekunden ist.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>dwNameSpace</strong></td>
<td>Legen Sie auf <strong>NS_BTH.</strong></td>
</tr>
<tr class="even">
<td>Andere Mitglieder</td>
<td>Andere Member der <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET-Struktur</strong></a> werden ignoriert.</td>
</tr>
</tbody>
</table>



 

Die in der folgenden Tabelle aufgeführten Flags werden im *dwControlFlags-Parameter* verwendet, um die Abfrageergebnisse zu steuern. Die **FLAGs LUP \_ CONTAINERS** und **LUP \_ FLUSHCACHE** werden von der [**WSALookupServiceBegin-Funktion**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) verwendet. Die restlichen Flags werden in Aufrufen der [**WSALookupServiceNext-Funktion**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) verwendet.

| Flag               | Ergebnis                                                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_LUP-CONTAINER    | Gibt an, dass der Abfragezweck das Abrufen einer Liste Bluetooth Geräte und nicht einer Liste von Diensten ist. Dieses Flag muss festgelegt werden.                                                                                                                                                                                                                                                                                       |
| LUP \_ FLUSHCACHE    | Löst eine Abfrage lokaler Geräte aus oder bewirkt, dass zwischengespeicherte Ergebnisse vorheriger Abfragen zurückgegeben werden.                                                                                                                                                                                                                                                                                                                |
| \_LUP-RÜCKGABETYP \_  | Gibt den Bluetooth COD (Klasse von Gerätebits) direkt im **lpServiceClassId-Member** der [**WSAQUERYSET-Struktur**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) zurück. Der COD wird dem **Data1-Member** der GUID zugeordnet.                                                                                                                                                                                                      |
| LUP \_ \_ RES-DIENST  | Gibt Informationen für die lokale Bluetooth zurück. Dieses Flag hat nur dann Auswirkungen, wenn **LUP \_ RETURN \_ ADDR** ebenfalls angegeben wird.                                                                                                                                                                                                                                                                                       |
| \_LUP-RÜCKGABENAME \_  | Gibt den Anzeigenamen des Geräts im **lpszServiceInstanceName-Member** der [**WSAQUERYSET-Struktur**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) für jeden Aufruf der [**WSALookupServiceNext-Funktion**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) zurück. Dieses Flag muss auch angegeben  werden, um das Namensmitglied der [**BTH \_ DEVICE \_ INFO-Struktur**](/windows/desktop/api/Bthdef/ns-bthdef-bth_device_info) abzurufen, wenn das **LUP \_ RETURN \_ BLOB-Flag angegeben** wird. |
| \_ \_ LUP-RÜCKGABE-ADDR  | Gibt eine [**SOCKADDR-BTH-Struktur \_**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) zurück, die die 48-Bit-Adresse des Peers im **lpcsaBuffer-Member** der [**WSAQUERYSET-Struktur**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) für jeden Aufruf der [**WSALookupServiceNext-Funktion**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) enthält. Andere Member in der **SOCKADDR-BTH-Struktur \_** sind leer.                                                            |
| \_ \_ LUP-RÜCKGABEBLOB  | Gibt die [**BTH \_ DEVICE \_ INFO-Struktur**](/windows/desktop/api/Bthdef/ns-bthdef-bth_device_info) bei jedem nachfolgenden Aufruf von [**WSALookupServiceNext zurück.**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta)                                                                                                                                                                                                                                                           |
| LUP \_ FLUSHPREVIOUS | Überspringen Sie das nächste verfügbare Gerät, und geben Sie das darauf folgende Gerät zurück.                                                                                                                                                                                                                                                                                                                                             |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Bluetooth und WSALookupServiceBegin für die Dienstermittlung](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)
</dt> <dt>

[Bluetooth und WSALookupServiceNext](bluetooth-and-wsalookupservicenext.md)
</dt> <dt>

[Bluetooth und WSAQUERYSET für die Geräteabfrage](bluetooth-and-wsaqueryset-for-device-inquiry.md)
</dt> <dt>

[Ermitteln von Bluetooth-Geräten und -Diensten](discovering-bluetooth-devices-and-services.md)
</dt> <dt>

[**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)
</dt> <dt>

[**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta)
</dt> <dt>

[**WSALookupServiceEnd**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupserviceend)
</dt> <dt>

[**Blob**](/windows/desktop/api/nspapi/ns-nspapi-blob)
</dt> <dt>

[**\_BTH-ABFRAGEGERÄT \_**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device)
</dt> <dt>

[**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)
</dt> <dt>

[**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[Windows-Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

 

 