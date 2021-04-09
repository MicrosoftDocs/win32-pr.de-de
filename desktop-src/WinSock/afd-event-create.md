---
description: Winsock-Netzwerk Ablauf Verfolgungs Ereignis für einen Socket-Erstellungs Vorgang.
ms.assetid: 59B9A570-5AEC-429D-AF71-AB6D8325C341
title: AFD_EVENT_CREATE Ereignis
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AFD_EVENT_CREATE
api_type:
- NA
api_location: ''
ms.openlocfilehash: 3216e1adccca6c7c7d64a22f77babe3cbb699c05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862596"
---
# <a name="afd_event_create-event"></a>Ereignis zum Erstellen von AFD- \_ Ereignissen \_

Das Ereignis für die **AFD- \_ Ereignis \_ Erstellung** ist ein Winsock-Netzwerk Ablauf Verfolgungs Ereignis für einen Socket-Erstellungs Vorgang.


```C++
const EVENT_DESCRIPTOR AFD_EVENT_CREATE = {0x3e8, 0x0, 0x10, 0x4, 0xa, 0x3e8, 0x8000000000000004};
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Enterexit* 
</dt> <dd>

Informationen zu diesem Ereignis.

In der folgenden Tabelle sind die möglichen Werte für den Parameter " *enterexit* " aufgeführt:



| Wert                                                                        | Bedeutung                                                                                              |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Der Start einer Winsock-Anforderung.<br/>                                                           |
| <dl> <dt>1</dt> </dl> | Die Winsock-Anforderung wurde abgeschlossen.<br/>                                                            |
| <dl> <dt>2</dt> </dl> | Der Winsock-AFD-Treiber hat eine interne Aktion ausgeführt (z. b. eine Verbindung abgebrochen).<br/>      |
| <dl> <dt>3</dt> </dl> | Der TCP/IP-Treiber hat dieses Ereignis verursacht. Dies weist normalerweise auf eine Daten Benachrichtigung hin.<br/> |
| <dl> <dt>4</dt> </dl> | Der Winsock-AFD-Treiber hat dieses Ereignis ausgelöst (z. b. das Festlegen einer Socketoption).<br/> |



 

</dd> <dt>

*Location* 
</dt> <dd>

Ein privates Feld, das intern verwendet wird.

</dd> <dt>

*Prozess* 
</dt> <dd>

Die [EPROCESS](/windows-hardware/drivers/kernel/eprocess) -Adresse des Prozesses, der den zugehörigen Socket besitzt. Dies ist eine nicht transparente Struktur, die als Prozess Objekt für einen Prozess dient. Weitere Informationen finden Sie in der Dokumentation zum Windows-Treiberkit für die [EPROCESS](/windows-hardware/drivers/kernel/eprocess) -Struktur.

</dd> <dt>

*Endpunkt* 
</dt> <dd>

Die AFD- \_ Endpunkt Adresse des Sockets.

</dd> <dt>

*AddressFamily* 
</dt> <dd>

Die Adress familienspezifikation für den Socket. Mögliche Werte für die Adressfamilie werden in der Header Datei " *Ws2def. h* " definiert. Beachten Sie, dass die Header Datei " *Ws2def. h* " automatisch in " *Winsock2. h*" enthalten ist und niemals direkt verwendet werden sollte.

Die derzeit unterstützten Werte sind AF \_ inet oder AF \_ inet6, bei denen es sich um die Internet Adress familienformate für IPv4 und IPv6 handelt. Weitere Optionen für die Adressfamilie (z. b. AF \_ NetBIOS für die Verwendung mit NetBIOS) werden unterstützt, wenn ein Windows Sockets-Dienstanbieter für die Adressfamilie installiert ist.

In der folgenden Tabelle sind allgemeine Werte für die Adressfamilie aufgeführt, obwohl viele andere Werte möglich sind.



| AFS                                                                                                                                                                                                                 | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="AF_UNSPEC"></span><span id="af_unspec"></span><dl> <dt>**AF \_ Nicht Spezifikation**</dt> <dt>0</dt> </dl>           | Die Adressfamilie ist nicht angegeben.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="AF_INET"></span><span id="af_inet"></span><dl> <dt>**AF \_ INET**</dt> <dt>2</dt> </dl>                 | Die IPv4-Adressfamilie (Internet Protokollversion 4).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="AF_IPX"></span><span id="af_ipx"></span><dl> <dt>**AF \_ IPX**</dt> <dt>6</dt> </dl>                    | Die IPX/SPX-Adressfamilie. Diese Adressfamilie wird nur unterstützt, wenn das mit dem NWLink IPX/SPX kompatible Transport Protokoll installiert ist. <br/> Diese Adressfamilie wird unter Windows Vista und höher nicht unterstützt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="AF_APPLETALK"></span><span id="af_appletalk"></span><dl> <dt>**AF \_ AppleTalk**</dt> <dt>16</dt> </dl> | Die AppleTalk-Adressfamilie. Diese Adressfamilie wird nur unterstützt, wenn das AppleTalk-Protokoll installiert ist. <br/> Diese Adressfamilie wird unter Windows Vista und höher nicht unterstützt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="AF_NETBIOS"></span><span id="af_netbios"></span><dl> <dt>**AF \_ NetBIOS**</dt> <dt>17</dt> </dl>       | Die NetBIOS-Adressfamilie. Diese Adressfamilie wird nur unterstützt, wenn der Windows Sockets-Anbieter für NetBIOS installiert ist. <br/> Der Windows Sockets-Anbieter für NetBIOS wird in 32-Bit-Versionen von Windows unterstützt. Dieser Anbieter wird standardmäßig auf 32-Bit-Versionen von Windows installiert. <br/> Der Windows Sockets-Anbieter für NetBIOS wird in 64-Bit-Versionen von Windows nicht unterstützt. <br/> Der Windows Sockets-Anbieter für NetBIOS unterstützt nur Sockets, bei denen der *Type* -Parameter auf **Sock \_ dgram** festgelegt ist.<br/> Der Windows Sockets-Anbieter für NetBIOS ist nicht direkt mit der [NetBIOS](/previous-versions/windows/desktop/netbios/portal) -Programmierschnittstelle verknüpft. Die NetBIOS-Programmierschnittstelle wird unter Windows Vista, Windows Server 2008 und höher nicht unterstützt.<br/> |
| <span id="AF_INET6"></span><span id="af_inet6"></span><dl> <dt>**AF \_ Inet6**</dt> <dt>23</dt> </dl>             | Die IPv6-Adressfamilie (Internet Protokollversion 6).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="AF_IRDA"></span><span id="af_irda"></span><dl> <dt>**AF \_ Irren**</dt> <dt>26</dt> </dl>                | Die UNDA-Adressfamilie (Infrarot Data Association). <br/> Diese Adressfamilie wird nur unterstützt, wenn auf dem Computer ein Infrarot Anschluss und Treiber installiert sind.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="AF_BTH"></span><span id="af_bth"></span><dl> <dt>**AF \_ BTH**</dt> <dt>32</dt> </dl>                   | Die Bluetooth-Adressfamilie. <br/> Diese Adressfamilie wird nur unterstützt, wenn auf dem Computer ein Bluetooth-Adapter und-Treiber installiert sind.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

</dd> <dt>

*SocketType* 
</dt> <dd>

Die Typspezifikation für den neuen Socket. Mögliche Werte für den Sockettyp werden in der Header Datei " *Winsock2. h* " definiert.

In der folgenden Tabelle sind die möglichen Werte für den *Typparameter* aufgeführt, die für Windows Sockets 2 unterstützt werden:



| type                                                                                                                                                                                                                    | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SOCK_STREAM"></span><span id="sock_stream"></span><dl> <dt>**Sock \_ Stream**</dt> <dt>1</dt> </dl>          | Ein socketyp, der sequenzierte, zuverlässige bidirektionale Verbindungs basierte Bytestreams mit einem OOB-Daten Übertragungsmechanismus bereitstellt. Dieser socketyp verwendet das Transmission Control Protocol (TCP) für die Internet Adressfamilie (AF \_ inet oder AF \_ inet6).<br/>                                                                                                                                |
| <span id="SOCK_DGRAM"></span><span id="sock_dgram"></span><dl> <dt>**Sock \_ Dgram**</dt> <dt>2</dt> </dl>             | Ein socketyp, der Datagramme unterstützt, bei denen es sich um verbindungslose, unzuverlässige Puffer mit einer festgelegten (normalerweise kleinen) maximalen Länge handelt. Dieser socketyp verwendet das User Datagram-Protokoll (UDP) für die Internet Adressfamilie (AF \_ inet oder AF \_ inet6).<br/>                                                                                                                                       |
| <span id="SOCK_RAW"></span><span id="sock_raw"></span><dl> <dt>**Sock \_ RAW**</dt> <dt>3</dt> </dl>                   | Ein Sockettyp, der einen Rohdaten Socket bereitstellt, mit dem eine Anwendung den nächsten Protokoll Header der obersten Ebene bearbeiten kann. Um den IPv4-Header zu bearbeiten, muss die [**IP \_ hdrincl-**](ipproto-ip-socket-options.md) Socketoption für den Socket festgelegt werden. Zum Bearbeiten des IPv6-Headers muss die [**IPv6- \_ hdrincl**](ipproto-ipv6-socket-options.md) -Socketoption für den Socket festgelegt werden. <br/> |
| <span id="SOCK_RDM"></span><span id="sock_rdm"></span><dl> <dt>**Sock \_ RDM**</dt> <dt>4</dt> </dl>                   | Ein Sockettyp, der ein zuverlässiges nachrichtendatagramm bereitstellt. Ein Beispiel für diesen Typ ist die pragmatische allgemeine Multicast-Protokoll Implementierung (PGM) in Windows, die häufig als [zuverlässige Multicast Programmierung](reliable-multicast-programming--pgm-.md)bezeichnet wird. <br/> Dieser *Typwert* wird nur unterstützt, wenn das zuverlässige Multicast-Protokoll installiert ist.<br/>              |
| <span id="SOCK_SEQPACKET"></span><span id="sock_seqpacket"></span><dl> <dt>**Sock \_ "Abtaket**</dt> <dt>5</dt> " </dl> | Ein Sockettyp, der ein auf Datagramme basierendes Pseudo Strom Paket bereitstellt. <br/>                                                                                                                                                                                                                                                                                                                |



 

</dd> <dt>

*Protokoll* 
</dt> <dd>

Das zu verwendende Protokoll. Die möglichen Optionen für den *Protocol* -Parameter sind spezifisch für die angegebene Adressfamilie und den angegebenen Sockettyp. Mögliche Werte für das *Protokoll* sind in der Header Datei " *WSRM. h* " und dem in der Header Datei " *Ws2def. h* " definierten **ipproto** -Enumerationstyp definiert. Beachten Sie, dass die Header Datei " *Ws2def. h* " automatisch in " *Winsock2. h*" enthalten ist und niemals direkt verwendet werden sollte.

Wenn der Wert 0 angegeben wird, möchte der Aufrufer kein Protokoll angeben, und der Dienstanbieter wählt das zu verwendende *Protokoll* aus.

In der folgenden Tabelle sind allgemeine Werte für das *Protokoll* aufgeführt, obwohl viele andere Werte möglich sind.



| Protokoll                                                                                                                                                                                                                   | Bedeutung                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="IPPROTO_ICMP"></span><span id="ipproto_icmp"></span><dl> <dt>**Ipproto \_ ICMP**</dt> <dt>1</dt> </dl>          | Das Internet Control Message-Protokoll (ICMP). Dies ist ein möglicher Wert, wenn es sich bei dem *AF* -Parameter um **AF \_ unspec**, **AF \_ inet** oder **AF \_ inet6** handelt und der *Typparameter* " **Sock \_ RAW** " oder "nicht angegeben" ist.<br/>                                                                                               |
| <span id="IPPROTO_IGMP"></span><span id="ipproto_igmp"></span><dl> <dt>**Ipproto \_ IGMP**</dt> <dt>2</dt> </dl>          | Das Internet Group Management-Protokoll (IGMP). Dies ist ein möglicher Wert, wenn es sich bei dem *AF* -Parameter um **AF \_ unspec**, **AF \_ inet** oder **AF \_ inet6** handelt und der *Typparameter* " **Sock \_ RAW** " oder "nicht angegeben" ist.<br/>                                                                                              |
| <span id="BTHPROTO_RFCOMM"></span><span id="bthproto_rfcomm"></span><dl> <dt>**Bthproto \_ RFCOMM**</dt> <dt>3</dt> </dl> | Das Bluetooth-Protokoll für Funk Häufigkeit (Bluetooth RFCOMM). Dies ist ein möglicher Wert, wenn der *AF* -Parameter " **AF \_ BTH** " und der *Typparameter* " **Sock \_ Stream**" ist. <br/>                                                                                                                 |
| <span id="IPPROTO_TCP"></span><span id="ipproto_tcp"></span><dl> <dt>**Ipproto \_ TCP**</dt> <dt>6</dt> </dl>             | Das Transmission Control-Protokoll (TCP). Dies ist ein möglicher Wert, wenn der *AF* - **Parameter AF \_ inet** oder **AF \_ inet6** und der *Typparameter* ein Sock- **\_ Stream** ist.<br/>                                                                                                                                 |
| <span id="IPPROTO_UDP"></span><span id="ipproto_udp"></span><dl> <dt>**Ipproto \_ UDP**</dt> <dt>17</dt> </dl>            | Das User Datagram-Protokoll (UDP). Dies ist ein möglicher Wert, wenn der *AF* -Parameter " **AF \_ inet** " oder " **AF \_ inet6** " ist und der *Typparameter* " **Sock \_ dgram**" ist.<br/>                                                                                                                                         |
| <span id="IPPROTO_ICMPV6"></span><span id="ipproto_icmpv6"></span><dl> <dt>**Ipproto \_ ICMPV6**</dt> <dt>58</dt> </dl>   | Internet Control Message Protocol, Version 6 (ICMPv6). Dies ist ein möglicher Wert, wenn es sich bei dem *AF* -Parameter um **AF \_ unspec**, **AF \_ inet** oder **AF \_ inet6** handelt und der *Typparameter* " **Sock \_ RAW** " oder "nicht angegeben" ist.<br/>                                                                                   |
| <span id="IPPROTO_RM"></span><span id="ipproto_rm"></span><dl> <dt>**Ipproto \_ RM**</dt> <dt>113</dt> </dl>              | Das PGM-Protokoll für zuverlässiges Multicast. Dies ist ein möglicher Wert, wenn der *AF* -Parameter " **AF \_ inet** " und der *Typparameter* " **Sock \_ RDM**" ist. Dieses Protokoll wird auch als **ipproto \_ PGM** bezeichnet. <br/> Dieser *Protokoll* Wert wird nur unterstützt, wenn das zuverlässige Multicast Protokoll installiert ist.<br/> |



 

</dd> <dt>

*ProcessId* 
</dt> <dd>

Die tatsächliche Prozess-ID oder ein Indikator, wenn das Ereignis das Ergebnis von Winsock-Code war, der in einem System Prozess oder in einem DPC-Kontext (verzögerte Prozedur Aufrufe) ausgeführt wurde (Kontexte außerhalb des Benutzer Prozesses).

</dd> <dt>

*Status* 
</dt> <dd>

Der NTSTATUS-Code für den Vorgang.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Das Ereignis für die **AFD- \_ Ereignis \_ Erstellung** wird für einen Winsock-Netzwerk Vorgang nachverfolgt, um einen Socket zu erstellen. Der Kanal für dieses Ereignis ist Winsock-AFD. Die Ebene für dieses Ereignis dient nur zu Informationszwecken.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Kontrolle über die Winsock-Ablauf Verfolgung](control-of-winsock-tracing.md)
</dt> <dt>

[**Ereignis \_ Deskriptor**](/windows/desktop/api/evntprov/ns-evntprov-event_descriptor)
</dt> <dt>

[Winsock-Ablauf Verfolgung](winsock-tracing.md)
</dt> <dt>

[Winsock-Ablauf Verfolgungs Ebenen](winsock-tracing-levels.md)
</dt> <dt>

[Details zur Änderung der Winsock-Katalog Änderung](winsock-layered-service-provider-tracing-event-details.md)
</dt> </dl>

 

