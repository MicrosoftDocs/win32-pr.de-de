---
title: Bluetooth und WSAQUERYSET für Dienstabfragen
description: Verwenden der WSAQUERYSET-Struktur mit den Funktionen WSALookupServiceBegin und WSALookupServiceNext, um Informationen zum Dienstabfrageprozess zu erhalten.
ms.assetid: c52a7e7d-92ab-4103-a6c6-57c3fafec706
keywords:
- Bluetooth und WSAQUERYSET für Dienstabfragen Bluetooth
- WSAQUERYSET Bluetooth , für Dienstabfragen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5db9c6cc3b6cc49f968c4eb39821b8b9857b0df
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467097"
---
# <a name="bluetooth-and-wsaqueryset-for-service-inquiry"></a>Bluetooth und WSAQUERYSET für Dienstabfragen

Bluetooth verwendet die [**WSAQUERYSET-Struktur**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) mit verschiedenen Funktionen, um die Ermittlung von Geräten und Diensten im Bluetooth Namespace NS \_ BTH zu erleichtern.

Die [**Funktionen WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) und [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) verwenden die [**WSAQUERYSET-Struktur,**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) um Daten zum Dienstabfrageprozess zu erhalten. In der folgenden Tabelle wird beschrieben, wie die Memberwerte in der **WSAQUERYSET-Struktur** für diesen Zweck festgelegt werden.




| Member | Eingabe für WSALookupServiceBegin | Zurückgegebener Wert von WSALookupServiceNext | 
|--------|--------------------------------|------------------------------------------|
| <strong>dwSize</strong> | Muss auf <strong>sizeof</strong>(<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET ) festgelegt werden.</strong></a> | <strong>sizeof</strong>(<a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET</strong></a>) wird vom System zurückgegeben. | 
| <strong>dwOutputFlags</strong> | Nicht verwendet. | Nicht verwendet. | 
| <strong>lpszServiceInstanceName</strong> | Nicht verwendet. | Anzeigename des Diensts, konvertiert als UTF-8-codierte Zeichenfolge aus der Standardsprachcodierung des Bluetooth ServiceName SDP-Attributs. Wird zurückgegeben, LUP_RETURN_NAME angegeben ist. | 
| <strong>lpServiceClassId</strong> | Erforderlich. Die spezifischste Bluetooth UUID für die Dienste, für die die Suche durchgeführt wird. Wenn dieser Wert beispielsweise auf die UUID des L2CAP-Protokolls festgelegt ist, werden alle Dienste zurückgegeben, die das L2CAP-Protokoll auf dem Zielgerät verwenden. Wenn sie auf die UUID eines bestimmten Diensts festgelegt ist, werden nur die Instanzen dieses Diensts zurückgeben. | Nicht verwendet. | 
| <strong>lpVersion</strong> | Nicht verwendet. | Nicht verwendet. | 
| <strong>lpszComment</strong> | Nicht verwendet. | Beschreibung des Diensts, konvertiert als UTF-8-codierte Zeichenfolge aus der Standardsprachcodierung des Bluetooth ServiceDescription-SDP-Attributs. Wird <strong>zurückgegeben, LUP_RETURN_COMMENT</strong> angegeben ist. | 
| <strong>dwNameSpace</strong> | Muss NS_BTH. | Gibt NS_BTH. | 
| <strong>lpNSProviderId</strong> | Nicht verwendet. | Nicht verwendet. | 
| <strong>lpszContext</strong> | Erforderlich. Die Bluetooth Geräteadresse, mit der eine SDP-Verbindung hergestellt und Dienste abfragen werden. Dieser Wert muss eine Zeichenfolge sein, die mithilfe des <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa"><strong>WSAAddressToString-Funktionsaufrufs</strong></a> konvertiert wurde. Wenn die lokale Bluetooth angegeben wird, wird die lokale SDP-Datenbank durchsucht. | Nicht verwendet. | 
| <strong>dwNumberOfProtocols</strong> | Nicht verwendet. | Nicht verwendet. | 
| <strong>lpafpProtocols</strong> | Nicht verwendet. | Nicht verwendet. | 
| <strong>lpszQueryString</strong> | Nicht verwendet. | Nicht verwendet. | 
| <strong>dwNumberOfCsAddrs</strong> | Nicht verwendet. | Gibt die Anzahl der Elemente im Array der <a href="/windows/desktop/api/nspapi/ns-nspapi-csaddr_info"><strong>CSADDR_INFO</strong></a> an. | 
| <strong>lpcsaBuffer</strong> | Nicht verwendet. | Zeiger auf eine <a href="/windows/desktop/api/nspapi/ns-nspapi-csaddr_info"><strong>CSADDR_INFO-Struktur,</strong></a> deren <strong>LocalAddr.lpSockaddr-Member</strong> auf eine <a href="/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth"><strong>SOCKADDR_BTH verweist,</strong></a> die die vollständige verbindungsfähige Adresse des Remotediensts enthält, die aus dem ersten Eintrag des Bluetooth ProtocolDescriptorList-SDP-Attributs konvertiert wurde. Wird <strong>zurückgegeben, LUP_RETURN_ADDR</strong> angegeben ist. | 
| <strong>lpBlob</strong> | Optional. Zeiger auf eine <a href="/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service"><strong>BTH_QUERY_SERVICE</strong></a> struktur, die erweiterte Parameter enthält, um die Ergebnisse der Suche zu begrenzen. Falls angegeben, <strong>wird lpServiceClassId</strong> ignoriert, und zwischengespeicherte Abfragen sind nicht erfolgreich. | <ul><li>Wenn eine Dienstsuche ausgeführt wird: Zeiger auf eine <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong>BLOB-Struktur,</strong></a> die die Diensthandles zurückgibt. (<strong>BLOB.cbSize</strong><strong>)/sizeof</strong>(ULONG) berechnet die Anzahl der Handles. <strong>BLOB.pBlobData ist</strong> ein Array von ULONG-Werten, die die Diensthandles darstellen.</li><li>Wenn eine Attribut- oder serviceAttribute-Suche <a href="/windows/desktop/api/nspapi/ns-nspapi-blob"><strong></strong></a> ausgeführt wird: Zeiger auf eine BLOB-Struktur, die den binären SDP-Datensatz zurückgibt. <strong>BLOB.cbSize ist</strong> die Größe des binären SDP-Eintrags. <strong>BLOB.pBlobData</strong> verweist auf den Datensatz selbst. Der binäre SDP-Datensatz ist in vielen Fällen erforderlich, da nur eine begrenzte Anzahl von SDP-Attributen in die <a href="/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw"><strong>WSAQUERYSET-Struktur</strong></a> konvertiert werden kann und nur standardmäßig codierte UTF-8-Zeichenfolgen konvertiert werden. Funktionen zur Unterstützung bei der Analyse des binären SDP-Eintrags finden Sie im Abschnitt <a href="bluetooth-reference.md">Bluetooth Referenz.</a></li><li>Wird zurückgegeben, LUP_RETURN_BLOB angegeben ist.</li></ul> | 




 

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

[**BLOB**](/windows/desktop/api/nspapi/ns-nspapi-blob)
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

 

 
