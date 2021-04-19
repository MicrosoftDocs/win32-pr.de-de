---
description: In der folgenden Tabelle werden die ipproto \_ RM-Socketoptionen beschrieben, die für Sockets gelten, die für die IPv4-Adressfamilie (AF \_ inet) mit dem Protokoll Parameter für die als zuverlässiger Multicast (ipproto RM) angegebene Socketfunktion erstellt wurden \_ .
ms.assetid: cb99960e-428b-4ef1-a6a5-e4bdb497c771
title: IPPROTO_RM Socketoptionen (WSRM. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2144efec9b0a92c1da3f612e707bcb44366a38c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370654"
---
# <a name="ipproto_rm-socket-options"></a>Ipproto \_ RM-Socketoptionen

In der folgenden Tabelle werden die **ipproto \_ RM** -Socketoptionen beschrieben, die für Sockets gelten, die für die IPv4-Adressfamilie (AF \_ inet) mit dem *Protokoll* Parameter für die als zuverlässiger Multicast (ipproto RM) angegebene [**Socketfunktion**](/windows/desktop/api/Winsock2/nf-winsock2-socket) erstellt wurden \_ . Weitere Informationen zum Ermitteln und Festlegen von Socketoptionen finden Sie auf den Referenzseiten zu den Funktionen [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) und [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) .

Verwenden Sie die [**wsaenumprotokolls**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa)-, [**wscenumprotokolle**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols)-oder [**WSCEnumProtocols32**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32) -Funktion, um Protokolle aufzulisten und die unterstützten Eigenschaften für jedes installierte Protokoll zu ermitteln.

**Windows XP:** Die zuverlässige Multicast Programmierung (PGM) wird nicht unterstützt.

Einige Socketoptionen erfordern eine ausführlichere Erläuterung, als diese Tabellen vermitteln können. Diese Optionen enthalten Links zu weiteren Seiten.

<dl> <dt><span id="IPPROTO_RM__Socket_Options"></span><span id="ipproto_rm__socket_options"></span><span id="IPPROTO_RM__SOCKET_OPTIONS"></span>**Ipproto \_ RM-Socketoptionen**</dt> <dd> <dl> <dt> 

| Option                              | Herunterladen | Set | Optval-Typ                                      | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------|-----|-----|--------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RM \_ Add \_ Receive \_ if                |     | ja | ULONG                                            | Nur Empfänger. Fügt eine Schnittstelle hinzu, auf der gelauscht werden soll (Standard ist die erste aufgelistete lokale Schnittstelle). Der optval-Parameter gibt die Netzwerkschnittstelle in der hinzu zufügenden netzwerkbyte Reihenfolge an. Der angegebene Wert ersetzt die Standardschnittstelle beim ersten Aufruf für einen angegebenen Socket und fügt bei nachfolgenden Aufrufen weitere Schnittstellen hinzu. Um das inaddr-Verhalten zu erhalten \_ , muss jede Netzwerkschnittstelle separat hinzugefügt werden. |
| RM-ENTF \_ \_ empfangen, \_ Wenn                |     | ja | ULONG                                            | Nur Empfänger. Entfernt eine Schnittstelle, die mit RM \_ Add \_ Receive if hinzugefügt wurde \_ . Der optval-Parameter gibt die Netzwerkschnittstelle in der zu löschenden netzwerkbyte Reihenfolge an.                                                                                                                                                                                                                                                            |
| RM- \_ flushcache                      |     | ja | –                                              | Nicht implementiert.                                                                                                                                                                                                                                                                                                                                                                                                       |
| RM-Aktivierung mit \_ hoher \_ Geschwindigkeit im \_ Intranet \_      | ja | ja | ULONG                                            | Nur Empfänger. Gibt an, ob eine Verbindung mit hoher Bandbreite (100 Mbit/s) verwendet wird.                                                                                                                                                                                                                                                                                                                                   |
| RM- \_ latejoin                        | ja | ja | ULONG                                            | Nur Absender. Der Prozentsatz der Fenstergröße, die von Empfängern mit späterer Beitritt bei der Sitzungs Annahme angefordert werden darf. Der Maximalwert ist 75% (der Standardwert ist 0). Deaktivieren Sie diese Einstellung, indem Sie erneut aufrufen, wobei der Wert auf NULL festgelegt ist                                                                                                                                                                                                |
| \_ \_ Fenster \_ Größe für RM-Rate              | ja | ja | [**RM- \_ Sende \_ Fenster**](/windows/desktop/api/Wsrm/ns-wsrm-rm_send_window)       | Nur Absender. Legt die Übertragungsraten Begrenzung, die Fenster Vorlaufzeit und die Fenstergröße fest.                                                                                                                                                                                                                                                                                                                                   |
| RM- \_ Empfänger \_ Statistik            | ja |     | [**RM- \_ Empfänger \_ Statistik**](/windows/desktop/api/Wsrm/ns-wsrm-rm_receiver_stats) | Nur Empfänger. Ruft Statistiken für die empfangende Sitzung ab.                                                                                                                                                                                                                                                                                                                                                         |
| \_ \_ \_ ADV- \_ Rate der RM-Sendefenster         | ja | ja | ULONG                                            | Nur Absender. Gibt die inkrementelle Vorlauf Rate für das nachfolgende Edge-Sendefenster an (Standardwert ist 15%). Der Maximalwert ist 50%.                                                                                                                                                                                                                                                                                          |
| RM- \_ Absender \_ Statistik              | ja |     | [**RM- \_ Absender \_ Statistik**](/windows/desktop/api/Wsrm/ns-wsrm-rm_sender_stats)     | Nur Absender. Ruft Statistiken für die Sende Sitzung ab.                                                                                                                                                                                                                                                                                                                                                             |
| vorab Methode des RM- \_ Absender \_ Fensters \_ \_ | ja | ja | ULONG                                            | Nur Absender. Der optval-Parameter gibt die Methode an, die verwendet wird, wenn das nachfolgende Edge-Sendefenster von Der optval-Parameter kann nur E \_ Fenster \_ vor \_ \_ der Zeit (Standard) sein. Beachten Sie, dass die E- \_ Window- \_ Verwendung \_ als \_ Daten \_ Cache nicht unterstützt wird.                                                                                                                                                                     |
| RM \_ - \_ mcast- \_ TTL festlegen                 |     | ja | ULONG                                            | Nur Absender. Legt die maximale Gültigkeitsdauer (Time to Live, TTL) für Multicast Pakete fest. Der maximale und der Standardwert ist 255.                                                                                                                                                                                                                                                                                                      |
| RM \_ Festlegen der \_ Nachrichten \_ Grenze          |     | ja | ULONG                                            | Nur Absender. Gibt die Größe der nächsten zu sendenden Nachricht in Bytes an. Nur für Nachrichten Modus-Sockets (Sock \_ RDM) sinnvoll. Kann festgelegt werden, während die Sitzung ausgeführt wird.                                                                                                                                                                                                                                                |
| RM \_ Set \_ Send \_ if                   | ja | ja | ULONG                                            | Nur Absender. Legt die IP-Adresse der Sende Schnittstelle in der netzwerkbyte Reihenfolge fest                                                                                                                                                                                                                                                                                                                                              |
| RM- \_ Verwendung von \_ FEC                        | ja | ja | [**RM- \_ FEC- \_ Informationen**](/windows/desktop/api/Wsrm/ns-wsrm-rm_fec_info)             | Nur Absender. Benachrichtigt den Absender, dass die Fehlerkorrektur Techniken zum Senden von Reparatur Daten angewendet werden sollen. FEC verfügt über drei Modi: pro-aktive Paritäts Pakete, nur OnDemand-Paritäts Pakete oder beides. Weitere Informationen finden Sie unter [**RM \_ FEC \_ Info**](/windows/desktop/api/Wsrm/ns-wsrm-rm_fec_info) Structure.                                                                                                                                                    |



 

</dt> </dl> </dd> <dt><span id="Windows_Support_for_IPPROTO_RM_options"></span><span id="windows_support_for_ipproto_rm_options"></span><span id="WINDOWS_SUPPORT_FOR_IPPROTO_RM_OPTIONS"></span>**Windows-Unterstützung für ipproto \_ RM-Optionen**</dt> <dd> <dl> <dt> 

| Option                              | Windows 7 | Windows Server 2008 | Windows Vista | Windows Server 2003 | Windows XP | Windows 2000 | Windows NT4 | Windows 9X/ME |
|-------------------------------------|-----------|---------------------|---------------|---------------------|------------|--------------|-------------|---------------|
| RM \_ Add \_ Receive \_ if                | x         | x                   | x             | x                   | x          |              |             |               |
| RM-ENTF \_ \_ empfangen, \_ Wenn                | x         | x                   | x             | x                   | x          |              |             |               |
| RM- \_ flushcache                      | x         | x                   | x             | x                   | x          |              |             |               |
| RM-Aktivierung mit \_ hoher \_ Geschwindigkeit im \_ Intranet \_      | x         | x                   | x             | x                   | x          |              |             |               |
| RM- \_ latejoin                        | x         | x                   | x             | x                   | x          |              |             |               |
| \_ \_ Fenster \_ Größe für RM-Rate              | x         | x                   | x             | x                   | x          |              |             |               |
| RM- \_ Empfänger \_ Statistik            | x         | x                   | x             | x                   | x          |              |             |               |
| \_ \_ \_ ADV- \_ Rate der RM-Sendefenster         | x         | x                   | x             | x                   | x          |              |             |               |
| RM- \_ Absender \_ Statistik              | x         | x                   | x             | x                   | x          |              |             |               |
| vorab Methode des RM- \_ Absender \_ Fensters \_ \_ | x         | x                   | x             | x                   | x          |              |             |               |
| RM \_ - \_ mcast- \_ TTL festlegen                 | x         | x                   | x             | x                   | x          |              |             |               |
| RM \_ Festlegen der \_ Nachrichten \_ Grenze          | x         | x                   | x             | x                   | x          |              |             |               |
| RM \_ Set \_ Send \_ if                   | x         | x                   | x             | x                   | x          |              |             |               |
| RM- \_ Verwendung von \_ FEC                        | x         | x                   | x             | x                   | x          |              |             |               |



 


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **ipproto \_ RM** -Socketoptionen und die von diesen Socketoptionen verwendeten Strukturen werden in der Header Datei " *WSRM. h* " definiert.

Die Konstante **ipproto \_ RM** oder **ipproto \_ PGM** kann verwendet werden, um den *Protokoll* Parameter für die [**Socketfunktion**](/windows/desktop/api/Winsock2/nf-winsock2-socket) anzugeben, um die RM-Socketoptionen zu verwenden. Auf dem Microsoft Windows Software Development Kit (SDK), das für Windows Vista und höher veröffentlicht wurde, wird die **ipproto \_ PGM** -Konstante in der Header Datei " *Ws2def. h* " auf denselben Wert wie die in der Header Datei " *WSRM. h* " definierte **ipproto \_ RM** -Konstante festgelegt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-----------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>WSRM. h</dt> </dl> |



 

 




