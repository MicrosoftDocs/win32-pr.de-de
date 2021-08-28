---
title: Bluetooth und WSALookupServiceBegin für Geräteabfragen
description: In diesem Thema wird beschrieben, wie die WSALookupServiceBegin-Funktion verwendet wird, um eine Abfrage von sichtbaren und ins ghosted-Geräten durchzuführen. Weitere Informationen finden Sie unter Ermitteln von Bluetooth Geräten und Diensten.
ms.assetid: 32fa710f-8645-4cf3-a882-cc032d66d979
keywords:
- Bluetooth und WSALookupServiceBegin für Bluetooth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4423b7c1c27124771c518409d9d1393a5f83afb
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469187"
---
# <a name="bluetooth-and-wsalookupservicebegin-for-device-inquiry"></a>Bluetooth und WSALookupServiceBegin für Geräteabfragen

In diesem Thema wird beschrieben, wie die [**WSALookupServiceBegin-Funktion**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) verwendet wird, um eine Abfrage von sichtbaren und ins ghosted-Geräten durchzuführen. Weitere Informationen finden Sie unter [Ermitteln Bluetooth Geräte und Dienste.](discovering-bluetooth-devices-and-services.md)

Die [**WSALookupServiceBegin-Funktion**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) verwendet eine [**WSAQUERYSET-Struktur**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) im ersten Parameter *lpqsRestrictions,* um Suchkriterien zu definieren. Bluetooth enthält spezifische Richtlinien für die Verwendung der **WSALookupServiceBegin-Funktion** und **von WSAQUERYSET.**

In der folgenden Tabelle sind einschränkungen aufgeführt, die für die [**WSAQUERYSET-Struktur**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) gelten, die beim Abfragen von Geräten an den *lpqsRestrictions-Parameter* übergeben wird.




| WSAQUERYSET-Member | Einschränkung | 
|--------------------|-------------|
| <strong>dwSize</strong> | Legen Sie auf <strong>sizeof</strong>(<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a>) fest. | 
| <strong>lpBlob</strong> | Dieser Member enthält einen optionalen Zeiger auf eine <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>BLOB-Struktur.</strong></a> Wenn dieser Member angegeben ist, sind die gültigen Parameter für die Geräteanfrage für <strong>LUP_FLUSHCACHE</strong> wie folgt:<ul><li>Der <strong>cbSize-Member</strong> der <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>BLOB-Struktur</strong></a> muss <strong>sizeof</strong>(<strong>BTH_QUERY_DEVICE</strong>) sein.</li><li>Das <strong>pBlobData-Element</strong> ist ein Zeiger auf eine <a href="/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device"><strong>BTH_QUERY_DEVICE-Struktur,</strong></a> für die das <strong>LAP-Element</strong> der Bluetooth Abfragezugriffscode und der <strong>Längenmember</strong> die Länge der Abfrage in Sekunden ist.</li></ul> | 
| <strong>dwNameSpace</strong> | Legen Sie auf <strong>NS_BTH</strong>fest. | 
| Andere Member | Andere Member der <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET-Struktur</strong></a> werden ignoriert. | 




 

Die in der folgenden Tabelle aufgeführten Flags werden im *dwControlFlags-Parameter* verwendet, um die Abfrageergebnisse zu steuern. Die **FLAGS LUP \_ CONTAINERS** und **LUP \_ FLUSHCACHE** werden von der [**WSALookupServiceBegin-Funktion**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) verwendet. Die restlichen Flags werden in Aufrufen der [**WSALookupServiceNext-Funktion**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) verwendet.

| Flag               | Ergebnis                                                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_LUP-CONTAINER    | Gibt an, dass der Abfragezweck darin besteht, eine Liste von Bluetooth Geräten und keine Liste von Diensten abzurufen. Dieses Flag muss festgelegt werden.                                                                                                                                                                                                                                                                                       |
| LUP \_ FLUSHCACHE    | Löst eine Abfrage lokaler Geräte aus oder bewirkt, dass zwischengespeicherte Ergebnisse aus vorherigen Abfragen zurückgegeben werden.                                                                                                                                                                                                                                                                                                                |
| \_LUP-RÜCKGABETYP \_  | Gibt die Bluetooth COD (Klasse von Gerätebits) direkt im **lpServiceClassId-Member** der [**WSAQUERYSET-Struktur**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) zurück. Der COD wird dem **Data1-Member** der GUID zugeordnet.                                                                                                                                                                                                      |
| LUP \_ RES \_ SERVICE  | Gibt Informationen für die lokale Bluetooth Adresse zurück. Dieses Flag hat nur dann Eine Auswirkung, wenn **auch LUP \_ RETURN \_ ADDR** angegeben ist.                                                                                                                                                                                                                                                                                       |
| \_LUP-RÜCKGABENAME \_  | Gibt den Anzeigenamen des **Geräts im lpszServiceInstanceName-Member** der [**WSAQUERYSET-Struktur**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) für jeden Aufruf der [**WSALookupServiceNext-Funktion**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) zurück. Dieses Flag muss auch angegeben werden, um den **Namenmember** der [**BTH \_ DEVICE \_ INFO-Struktur**](/windows/desktop/api/Bthdef/ns-bthdef-bth_device_info) abzurufen, wenn das **LUP \_ RETURN \_ BLOB-Flag** angegeben wird. |
| LUP \_ RETURN \_ ADDR  | Gibt eine [**SOCKADDR-BTH-Struktur \_**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth) zurück, die die 48-Bit-Adresse des Peers im **lpcsaBuffer-Member** der [**WSAQUERYSET-Struktur**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) für jeden Aufruf der [**WSALookupServiceNext-Funktion**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) enthält. Andere Member in der **SOCKADDR-BTH-Struktur \_** sind leer.                                                            |
| \_ \_ LUP-RÜCKGABEBLOB  | Gibt die [**BTH \_ DEVICE \_ INFO-Struktur**](/windows/desktop/api/Bthdef/ns-bthdef-bth_device_info) bei jedem nachfolgenden Aufruf von [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta)zurück.                                                                                                                                                                                                                                                           |
| LUP \_ FLUSHPREVIOUS | Überspringen Sie das nächste verfügbare Gerät, und geben Sie das Darauf folgende Gerät zurück.                                                                                                                                                                                                                                                                                                                                             |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Bluetooth und WSALookupServiceBegin für die Dienstermittlung](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)
</dt> <dt>

[Bluetooth und WSALookupServiceNext](bluetooth-and-wsalookupservicenext.md)
</dt> <dt>

[Bluetooth und WSAQUERYSET für Geräteabfragen](bluetooth-and-wsaqueryset-for-device-inquiry.md)
</dt> <dt>

[Ermitteln von Bluetooth-Geräten und -Diensten](discovering-bluetooth-devices-and-services.md)
</dt> <dt>

[**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)
</dt> <dt>

[**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta)
</dt> <dt>

[**WSALookupServiceEnd**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupserviceend)
</dt> <dt>

[**BLOB**](/windows/desktop/api/nspapi/ns-nspapi-blob)
</dt> <dt>

[**\_BTH-ABFRAGEGERÄT \_**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device)
</dt> <dt>

[**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)
</dt> <dt>

[**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[Windows-Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

 

 
