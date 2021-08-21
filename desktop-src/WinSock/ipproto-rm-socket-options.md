---
description: In der folgenden Tabelle werden IPPROTO \_ RM-Socketoptionen beschrieben, die für Sockets gelten, die für die IPv4-Adressfamilie (AF \_ INET) mit dem Protokollparameter für die Socketfunktion erstellt wurden, die als zuverlässiges Multicast (IPPROTO RM) angegeben \_ ist.
ms.assetid: cb99960e-428b-4ef1-a6a5-e4bdb497c771
title: IPPROTO_RM Socketoptionen (Wsrm.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec1710b1135d2c645f5ff55de12b2feb2d62cfbe2b257e3f28367a66a81d5171
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051488"
---
# <a name="ipproto_rm-socket-options"></a>IPPROTO \_ RM Socket-Optionen

In der folgenden Tabelle werden **IPPROTO \_ RM-Socketoptionen** beschrieben, die für Sockets gelten, die für die IPv4-Adressfamilie (AF \_ INET) mit dem *Protokollparameter* für die [**Socketfunktion**](/windows/desktop/api/Winsock2/nf-winsock2-socket) erstellt wurden, die als zuverlässiges Multicast (IPPROTO RM) angegeben \_ ist. Weitere Informationen zum Abrufen und Festlegen von Socketoptionen finden Sie auf den Referenzseiten der Funktionen [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) und [**setsockopt.**](/windows/desktop/api/winsock/nf-winsock-setsockopt)

Um Protokolle aufzulisten und unterstützte Eigenschaften für jedes installierte Protokoll zu ermitteln, verwenden Sie die Funktion [**WSAEnumProtocols,**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) [**WSCEnumProtocols**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols)oder [**WSCEnumProtocols32.**](/windows/desktop/api/Ws2spi/nf-ws2spi-wscenumprotocols32)

**Windows XP:** Reliable Multicast Programming (PGM) wird nicht unterstützt.

Einige Socketoptionen erfordern mehr Erklärung, als diese Tabellen vermitteln können. diese Optionen enthalten Links zu zusätzlichen Seiten.

<dl> <dt><span id="IPPROTO_RM__Socket_Options"></span><span id="ipproto_rm__socket_options"></span><span id="IPPROTO_RM__SOCKET_OPTIONS"></span>**IPPROTO \_ RM Socket-Optionen**</dt> <dd> <dl> <dt> 

| Option                              | Herunterladen | Set | Optval-Typ                                      | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------|-----|-----|--------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RM \_ ADD \_ RECEIVE \_ IF                |     | Ja | ULONG                                            | Nur Empfänger. Fügt eine Schnittstelle hinzu, auf der geleert werden soll (der Standardwert ist die erste aufzählte lokale Schnittstelle). Der optval-Parameter gibt die Netzwerkschnittstelle in der hinzuzufügenden Netzwerk-Bytereihenfolge an. Der angegebene Wert ersetzt die Standardschnittstelle beim ersten Aufruf eines bestimmten Sockets und fügt bei nachfolgenden Aufrufen weitere Schnittstellen hinzu. Um INADDR \_ ANY-Verhalten zu erhalten, muss jede Netzwerkschnittstelle separat hinzugefügt werden. |
| RM \_ DEL \_ RECEIVE \_ IF                |     | Ja | ULONG                                            | Nur Empfänger. Entfernt eine Schnittstelle, die mit RM ADD RECEIVE IF hinzugefügt \_ \_ \_ wurde. Der parameter optval gibt die Netzwerkschnittstelle in der zu löschenden Netzwerk bytereihenfolge an.                                                                                                                                                                                                                                                            |
| RM \_ FLUSHCACHE                      |     | ja | –                                              | Nicht implementiert.                                                                                                                                                                                                                                                                                                                                                                                                       |
| RM \_ HIGH \_ SPEED \_ INTRANET \_ OPT      | Ja | Ja | ULONG                                            | Nur Empfänger. Gibt an, ob eine LAN-Verbindung mit hoher Bandbreite (100 MBit/s+) verwendet wird.                                                                                                                                                                                                                                                                                                                                   |
| RM \_ LATEJOIN                        | Ja | Ja | ULONG                                            | Nur Absender. Prozentsatz der Fenstergröße, die von Empfängern mit später Verbindung bei Der Sitzungsakzeptanz angefordert werden darf. Der Höchstwert beträgt 75 % (der Standardwert ist 0). Deaktivieren Sie diese Einstellung, indem Sie erneut aufrufen, wobei der Wert auf 0 (null) festgelegt ist.                                                                                                                                                                                                |
| GRÖßE \_ DES \_ RM RATE-FENSTERS \_              | Ja | Ja | [**\_ \_ RM-SENDEFENSTER**](/windows/desktop/api/Wsrm/ns-wsrm-rm_send_window)       | Nur Absender. Legt das Übertragungsratenlimit, die Fenstervorlaufzeit und die Fenstergröße fest.                                                                                                                                                                                                                                                                                                                                   |
| \_ \_ RM-EMPFÄNGERSTATISTIKEN            | Ja |     | [**RM \_ RECEIVER \_ STATS**](/windows/desktop/api/Wsrm/ns-wsrm-rm_receiver_stats) | Nur Empfänger. Ruft Statistiken für die empfangende Sitzung ab.                                                                                                                                                                                                                                                                                                                                                         |
| RM \_ SEND \_ WINDOW \_ ADV \_ RATE         | Ja | Ja | ULONG                                            | Nur Absender. Gibt die inkrementelle Vorauszahlung für das nachfolgende Edgesendefenster an (Der Standardwert ist 15 %). Der Höchstwert beträgt 50 %.                                                                                                                                                                                                                                                                                          |
| RM \_ SENDER \_ STATISTICS              | Ja |     | [**RM \_ SENDER \_ STATS**](/windows/desktop/api/Wsrm/ns-wsrm-rm_sender_stats)     | Nur Absender. Ruft Statistiken für die sendende Sitzung ab.                                                                                                                                                                                                                                                                                                                                                             |
| RM \_ SENDER \_ WINDOW \_ ADVANCE \_ METHOD | Ja | Ja | ULONG                                            | Nur Absender. Der optval-Parameter gibt die Methode an, die verwendet wird, wenn das nachfolgende Edge-Sendefenster vorangestellt wird. Der optval-Parameter kann nur E \_ WINDOW ADVANCE BY TIME \_ \_ \_ (Standardeinstellung) sein. Beachten Sie, dass E \_ WINDOW USE AS DATA CACHE nicht unterstützt \_ \_ \_ \_ wird.                                                                                                                                                                     |
| RM \_ SET \_ MCAST \_ TTL                 |     | Ja | ULONG                                            | Nur Absender. Legt die Einstellung für die maximale Gültigkeitsdauer (TTL) für Multicastpakete fest. Der Höchst- und Standardwert ist 255.                                                                                                                                                                                                                                                                                                      |
| RM \_ SET \_ MESSAGE \_ BOUNDARY          |     | Ja | ULONG                                            | Nur Absender. Gibt die Größe der nächsten zu sendenden Nachricht in Bytes an. Nur für Sockets im Nachrichtenmodus (SOCK \_ RDM) sinnvoll. Kann festgelegt werden, während die Sitzung ausgeführt wird.                                                                                                                                                                                                                                                |
| RM \_ SET \_ SEND \_ IF                   | Ja | Ja | ULONG                                            | Nur Absender. Legt die IP-Adresse der sendenden Schnittstelle in der Netzwerk-Bytereihenfolge fest.                                                                                                                                                                                                                                                                                                                                              |
| RM \_ USE \_ FEC                        | Ja | Ja | [**RM \_ FEC \_ INFO**](/windows/desktop/api/Wsrm/ns-wsrm-rm_fec_info)             | Nur Absender. Benachrichtigt den Absender, dass er Verfahren zur Weiterleitungsfehlerkorrektur anwenden soll, um Reparaturdaten zu senden. FEC verfügt über drei Modi: nur proaktive Paritätspakete, nur OnDemand-Paritätspakete oder beides. Weitere Informationen finden Sie unter RM FEC INFO structure [**(RM \_ FEC \_**](/windows/desktop/api/Wsrm/ns-wsrm-rm_fec_info) INFO-Struktur).                                                                                                                                                    |



 

</dt> </dl> </dd> <dt><span id="Windows_Support_for_IPPROTO_RM_options"></span><span id="windows_support_for_ipproto_rm_options"></span><span id="WINDOWS_SUPPORT_FOR_IPPROTO_RM_OPTIONS"></span>**Windows Unterstützung für IPPROTO \_ RM-Optionen**</dt> <dd> <dl> <dt> 

| Option                              | Windows 7 | Windows Server 2008 | Windows Vista | Windows Server 2003 | Windows XP | Windows 2000 | Windows NT4 | Windows 9x/Me |
|-------------------------------------|-----------|---------------------|---------------|---------------------|------------|--------------|-------------|---------------|
| RM \_ ADD \_ RECEIVE \_ IF                | x         | x                   | x             | x                   | x          |              |             |               |
| RM \_ DEL \_ RECEIVE \_ IF                | x         | x                   | x             | x                   | x          |              |             |               |
| RM \_ FLUSHCACHE                      | x         | x                   | x             | x                   | x          |              |             |               |
| RM \_ HIGH \_ SPEED \_ INTRANET \_ OPT      | x         | x                   | x             | x                   | x          |              |             |               |
| RM \_ LATEJOIN                        | x         | x                   | x             | x                   | x          |              |             |               |
| GRÖßE \_ DES \_ RM RATE-FENSTERS \_              | x         | x                   | x             | x                   | x          |              |             |               |
| \_ \_ RM-EMPFÄNGERSTATISTIKEN            | x         | x                   | x             | x                   | x          |              |             |               |
| RM \_ SEND \_ WINDOW \_ ADV \_ RATE         | x         | x                   | x             | x                   | x          |              |             |               |
| RM \_ SENDER \_ STATISTICS              | x         | x                   | x             | x                   | x          |              |             |               |
| RM \_ SENDER \_ WINDOW \_ ADVANCE \_ METHOD | x         | x                   | x             | x                   | x          |              |             |               |
| RM \_ SET \_ MCAST \_ TTL                 | x         | x                   | x             | x                   | x          |              |             |               |
| RM \_ SET \_ MESSAGE \_ BOUNDARY          | x         | x                   | x             | x                   | x          |              |             |               |
| RM \_ SET \_ SEND \_ IF                   | x         | x                   | x             | x                   | x          |              |             |               |
| RM \_ USE \_ FEC                        | x         | x                   | x             | x                   | x          |              |             |               |



 


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Hinweise

Die **IPPROTO \_ RM-Socketoptionen** und die von diesen Socketoptionen verwendeten Strukturen werden in der *Wsrm.h-Headerdatei* definiert.

Der **IPPROTO \_ RM** oder die **IPPROTO \_ PGM-Konstante** kann verwendet werden, um den *Protokollparameter* für die [**Socketfunktion**](/windows/desktop/api/Winsock2/nf-winsock2-socket) anzugeben, um die RM-Socketoptionen zu verwenden. Auf dem Microsoft Windows Software Development Kit (SDK), das für Windows Vista und höher veröffentlicht wurde, wird die **IPPROTO \_ PGM-Konstante** in der *Headerdatei Ws2def.h* auf den gleichen Wert definiert wie die **IPPROTO \_ RM-Konstante,** die in der *Headerdatei Wsrm.h* definiert ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|-----------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Wsrm.h</dt> </dl> |



 

 




