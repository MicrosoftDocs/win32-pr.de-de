---
description: Winsock-Netzwerkablaufverfolgungsereignis für einen Socketerstellungsvorgang.
ms.assetid: 59B9A570-5AEC-429D-AF71-AB6D8325C341
title: AFD_EVENT_CREATE-Ereignis
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
ms.openlocfilehash: 7ae6f50646ad863be711ab6d48e775aeac9023a053e29044f3921e1dee8c9948
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120121480"
---
# <a name="afd_event_create-event"></a>AFD \_ EVENT \_ CREATE-Ereignis

Das **AFD \_ EVENT \_ CREATE-Ereignis** ist ein Winsock-Netzwerkablaufverfolgungsereignis für einen Socketerstellungsvorgang.


```C++
const EVENT_DESCRIPTOR AFD_EVENT_CREATE = {0x3e8, 0x0, 0x10, 0x4, 0xa, 0x3e8, 0x8000000000000004};
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*EnterExit* 
</dt> <dd>

Informationen zu diesem Ereignis.

In der folgenden Tabelle sind die möglichen Werte für den *EnterExit-Parameter* aufgeführt:



| Wert                                                                        | Bedeutung                                                                                              |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Der Anfang einer Winsock-Anforderung.<br/>                                                           |
| <dl> <dt>1</dt> </dl> | Die Winsock-Anforderung wurde abgeschlossen.<br/>                                                            |
| <dl> <dt>2</dt> </dl> | Der Winsock AFD-Treiber hat eine interne Aktion (z. B. das Abbrechen einer Verbindung) ergriffen.<br/>      |
| <dl> <dt>3</dt> </dl> | Der TCP/IP-Treiber hat dieses Ereignis verursacht. Dies weist in der Regel auf eine Datenbenachrichtigung hin.<br/> |
| <dl> <dt>4</dt> </dl> | Der Winsock AFD-Treiber hat dieses Ereignis verursacht (z. B. durch Festlegen einer Socketoption).<br/> |



 

</dd> <dt>

*Standort* 
</dt> <dd>

Ein intern verwendetes privates Feld.

</dd> <dt>

*Process* 
</dt> <dd>

Die [EPROCESS-Adresse](/windows-hardware/drivers/kernel/eprocess) des Prozesses, der den verknüpften Socket besitzt. Dies ist eine nicht transparente Struktur, die als Prozessobjekt für einen Prozess dient. Weitere Informationen finden Sie in der Windows Driver Kit-Dokumentation für die [EPROCESS-Struktur.](/windows-hardware/drivers/kernel/eprocess)

</dd> <dt>

*Endpunkt* 
</dt> <dd>

Die \_ AFD-ENDPUNKTadresse des Sockets.

</dd> <dt>

*Addressfamily* 
</dt> <dd>

Die Adressfamilienspezifikation für den Socket. Mögliche Werte für die Adressfamilie werden in der *Headerdatei Ws2def.h* definiert. Beachten Sie, dass die *Headerdatei Ws2def.h* automatisch in *Winsock2.h* enthalten ist und niemals direkt verwendet werden sollte.

Die derzeit unterstützten Werte sind AF INET oder AF INET6. Dabei handelt es sich um \_ \_ die Formate der Internetadressfamilie für IPv4 und IPv6. Andere Optionen für die Adressfamilie \_ (z.B. AF NETBIOS für die Verwendung mit NetBIOS) werden unterstützt, wenn ein Windows Sockets-Dienstanbieter für die Adressfamilie installiert ist.

In der folgenden Tabelle sind allgemeine Werte für die Adressfamilie aufgeführt, obwohl viele andere Werte möglich sind.



| Af                                                                                                                                                                                                                 | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="AF_UNSPEC"></span><span id="af_unspec"></span><dl> <dt>**AF \_ UNSPEC**</dt> <dt>0</dt> </dl>           | Die Adressfamilie ist nicht angegeben.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="AF_INET"></span><span id="af_inet"></span><dl> <dt>**AF \_ INET**</dt> <dt>2</dt> </dl>                 | Die IPv4-Adressfamilie (Internetprotokoll, Version 4).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="AF_IPX"></span><span id="af_ipx"></span><dl> <dt>**AF \_ IPX**</dt> <dt>6</dt> </dl>                    | Die IPX-/SPX-Adressfamilie. Diese Adressfamilie wird nur unterstützt, wenn das NetBIOS-kompatible Transportprotokoll NWLink IPX/SPX installiert ist. <br/> Diese Adressfamilie wird unter Windows Vista und höher nicht unterstützt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="AF_APPLETALK"></span><span id="af_appletalk"></span><dl> <dt>**AF \_ APPLETALK**</dt> <dt>16</dt> </dl> | Die AppleTalk-Adressfamilie. Diese Adressfamilie wird nur unterstützt, wenn das AppleTalk-Protokoll installiert ist. <br/> Diese Adressfamilie wird unter Windows Vista und höher nicht unterstützt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="AF_NETBIOS"></span><span id="af_netbios"></span><dl> <dt>**AF \_ NETBIOS**</dt> <dt>17</dt> </dl>       | Die NetBIOS-Adressfamilie. Diese Adressfamilie wird nur unterstützt, wenn der Windows Sockets-Anbieter für NetBIOS installiert ist. <br/> Der Windows Sockets-Anbieter für NetBIOS wird in 32-Bit-Versionen von Windows unterstützt. Dieser Anbieter wird standardmäßig auf 32-Bit-Versionen von Windows installiert. <br/> Der Windows Sockets-Anbieter für NetBIOS wird unter 64-Bit-Versionen von Windows nicht unterstützt. <br/> Der Windows Sockets-Anbieter für NetBIOS unterstützt nur Sockets, bei denen der *Typparameter* auf **SOCK \_ DGRAM** festgelegt ist.<br/> Der Windows Sockets-Anbieter für NetBIOS ist nicht direkt mit der [NetBIOS-Programmierschnittstelle](/previous-versions/windows/desktop/netbios/portal) verknüpft. Die NetBIOS-Programmierschnittstelle wird unter Windows Vista, Windows Server 2008 und höher nicht unterstützt.<br/> |
| <span id="AF_INET6"></span><span id="af_inet6"></span><dl> <dt>**AF \_ INET6**</dt> <dt>23</dt> </dl>             | Die IPv6-Adressfamilie (Internet Protocol Version 6).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="AF_IRDA"></span><span id="af_irda"></span><dl> <dt>**AF \_ IRDA**</dt> <dt>26</dt> </dl>                | Die Infrared Data Association(IrDA)-Adressfamilie. <br/> Diese Adressfamilie wird nur unterstützt, wenn auf dem Computer ein Port und treiber installiert sind.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="AF_BTH"></span><span id="af_bth"></span><dl> <dt>**AF \_ BTH**</dt> <dt>32</dt> </dl>                   | Die Bluetooth Adressfamilie. <br/> Diese Adressfamilie wird nur unterstützt, wenn auf dem Computer ein Bluetooth Adapter und Treiber installiert sind.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

</dd> <dt>

*Sockettype* 
</dt> <dd>

Die Typspezifikation für den neuen Socket. Mögliche Werte für den Sockettyp werden in der *Winsock2.h-Headerdatei* definiert.

In der folgenden Tabelle sind die möglichen Werte für den *Typparameter* aufgeführt, der für Windows Sockets 2 unterstützt wird:



| type                                                                                                                                                                                                                    | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SOCK_STREAM"></span><span id="sock_stream"></span><dl> <dt>**SOCK \_ STREAM**</dt> <dt>1</dt> </dl>          | Ein Sockettyp, der sequenzierte, zuverlässige, bidirektionierte, verbindungsbasierte Bytestreams mit einem OOB-Datenübertragungsmechanismus bereitstellt. Dieser Sockettyp verwendet das Transmission Control Protocol (TCP) für die Internetadressfamilie (AF \_ INET oder AF \_ INET6).<br/>                                                                                                                                |
| <span id="SOCK_DGRAM"></span><span id="sock_dgram"></span><dl> <dt>**SOCK \_ DGRAM**</dt> <dt>2</dt> </dl>             | Ein Sockettyp, der Datagramme unterstützt, bei denen es sich um verbindungslose, unzuverlässige Puffer mit fester (normalerweise kleiner) maximaler Länge handelt. Dieser Sockettyp verwendet das User Datagram Protocol (UDP) für die Internetadressfamilie (AF \_ INET oder AF \_ INET6).<br/>                                                                                                                                       |
| <span id="SOCK_RAW"></span><span id="sock_raw"></span><dl> <dt>**SOCK \_ RAW**</dt> <dt>3</dt> </dl>                   | Ein Sockettyp, der einen unformatierten Socket bereitstellt, mit dem eine Anwendung den nächsten Protokollheader der oberen Ebene bearbeiten kann. Um den IPv4-Header zu bearbeiten, muss die [**\_ IP-HDRINCL-Socketoption**](ipproto-ip-socket-options.md) für den Socket festgelegt werden. Um den IPv6-Header zu bearbeiten, muss die [**IPV6 \_ HDRINCL-Socketoption**](ipproto-ipv6-socket-options.md) für den Socket festgelegt werden. <br/> |
| <span id="SOCK_RDM"></span><span id="sock_rdm"></span><dl> <dt>**SOCK \_ RDM**</dt> <dt>4</dt> </dl>                   | Ein Sockettyp, der ein zuverlässiges Nachrichtendatendiagramm bereitstellt. Ein Beispiel für diesen Typ ist die PGM-Multicastprotokollimplementierung (PGM) in Windows, die häufig als [zuverlässige Multicastprogrammierung](reliable-multicast-programming--pgm-.md)bezeichnet wird. <br/> Dieser *Typwert* wird nur unterstützt, wenn das Reliable Multicast-Protokoll installiert ist.<br/>              |
| <span id="SOCK_SEQPACKET"></span><span id="sock_seqpacket"></span><dl> <dt>**SOCK \_ SEQPACKET**</dt> <dt>5</dt> </dl> | Ein Sockettyp, der ein Pseudostreampaket basierend auf Datagrammen bereitstellt. <br/>                                                                                                                                                                                                                                                                                                                |



 

</dd> <dt>

*Protokoll* 
</dt> <dd>

Das zu verwendende Protokoll. Die möglichen Optionen für den *Protokollparameter* sind spezifisch für die angegebene Adressfamilie und den angegebenen Sockettyp. Mögliche Werte für das *Protokoll* werden in der *Wsrm.h-Headerdatei* und dem **IPPROTO-Enumerationstyp** definiert, der in der *Ws2def.h-Headerdatei* definiert ist. Beachten Sie, dass die *Headerdatei Ws2def.h* automatisch in *Winsock2.h* enthalten ist und niemals direkt verwendet werden sollte.

Wenn der Wert 0 angegeben wird, möchte der Aufrufer kein Protokoll angeben, und der Dienstanbieter wählt das zu verwendende *Protokoll* aus.

In der folgenden Tabelle sind allgemeine Werte für das *Protokoll* aufgeführt, obwohl viele andere Werte möglich sind.



| Protokoll                                                                                                                                                                                                                   | Bedeutung                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="IPPROTO_ICMP"></span><span id="ipproto_icmp"></span><dl> <dt>**IPPROTO \_ ICMP**</dt> <dt>1</dt> </dl>          | Das Internet Control Message Protocol (ICMP). Dies ist ein möglicher Wert, wenn der *af-Parameter* **AF \_ UNSPEC,** **AF \_ INET** oder **AF \_ INET6** ist und der *Typparameter* **SOCK \_ RAW** oder nicht angegeben ist.<br/>                                                                                               |
| <span id="IPPROTO_IGMP"></span><span id="ipproto_igmp"></span><dl> <dt>**IPPROTO \_ IGMP**</dt> <dt>2</dt> </dl>          | Das Internet Group Management Protocol (IGMP). Dies ist ein möglicher Wert, wenn der *af-Parameter* **AF \_ UNSPEC,** **AF \_ INET** oder **AF \_ INET6** ist und der *Typparameter* **SOCK \_ RAW** oder nicht angegeben ist.<br/>                                                                                              |
| <span id="BTHPROTO_RFCOMM"></span><span id="bthproto_rfcomm"></span><dl> <dt>**BTHPROTO \_ RFCOMM**</dt> <dt>3</dt> </dl> | Das Bluetooth RFCOMM-Protokoll (Bluetooth Radio Frequency Communications). Dies ist ein möglicher Wert, wenn der *af-Parameter* **AF \_ BTH** und der *Typparameter* **SOCK \_ STREAM** ist. <br/>                                                                                                                 |
| <span id="IPPROTO_TCP"></span><span id="ipproto_tcp"></span><dl> <dt>**IPPROTO \_ TCP**</dt> <dt>6</dt> </dl>             | Das Transmission Control Protocol (TCP). Dies ist ein möglicher Wert, wenn der *af-Parameter* **AF \_ INET** oder **AF \_ INET6** und der *Typparameter* **SOCK \_ STREAM** ist.<br/>                                                                                                                                 |
| <span id="IPPROTO_UDP"></span><span id="ipproto_udp"></span><dl> <dt>**IPPROTO \_ UDP**</dt> <dt>17</dt> </dl>            | Das User Datagram-Protokoll (UDP). Dies ist ein möglicher Wert, wenn der *af-Parameter* **AF \_ INET** oder **AF \_ INET6** und der *Typparameter* **SOCK \_ DGRAM** ist.<br/>                                                                                                                                         |
| <span id="IPPROTO_ICMPV6"></span><span id="ipproto_icmpv6"></span><dl> <dt>**IPPROTO \_ ICMPV6**</dt> <dt>58</dt> </dl>   | Internet Control Message Protocol Version 6 (ICMPv6). Dies ist ein möglicher Wert, wenn der *af-Parameter* **AF \_ UNSPEC,** **AF \_ INET** oder **AF \_ INET6** ist und der *Typparameter* **SOCK \_ RAW** oder nicht angegeben ist.<br/>                                                                                   |
| <span id="IPPROTO_RM"></span><span id="ipproto_rm"></span><dl> <dt>**IPPROTO \_ RM**</dt> <dt>113</dt> </dl>              | Das PGM-Protokoll für zuverlässiges Multicast. Dies ist ein möglicher Wert, wenn der *af-Parameter* **AF \_ INET** und der *Typparameter* **SOCK \_ RDM** ist. Dieses Protokoll wird auch als **IPPROTO \_ PGM** bezeichnet. <br/> Dieser *Protokollwert* wird nur unterstützt, wenn das Reliable Multicast-Protokoll installiert ist.<br/> |



 

</dd> <dt>

*Processid* 
</dt> <dd>

Die tatsächliche Prozess-ID oder ein Indikator, wenn das Ereignis das Ergebnis der Ausführung von Winsock-Code in einem Systemprozess oder in einem DPC-Kontext (verzögerter Prozeduraufruf) (Kontexte außerhalb des Benutzerprozesses) war.

</dd> <dt>

*Status* 
</dt> <dd>

Der NTSTATUS-Code für den Vorgang.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Das **AFD \_ EVENT \_ CREATE-Ereignis** wird für einen Winsock-Netzwerkvorgang zum Erstellen eines Sockets nachverfolgt. Der Kanal für dieses Ereignis ist Winsock-AFD. Die Ebene für dieses Ereignis ist informational.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>              |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Steuerung der Winsock-Ablaufverfolgung](control-of-winsock-tracing.md)
</dt> <dt>

[**\_EREIGNISBESCHREIBUNG**](/windows/desktop/api/evntprov/ns-evntprov-event_descriptor)
</dt> <dt>

[Winsock-Ablaufverfolgung](winsock-tracing.md)
</dt> <dt>

[Winsock-Ablaufverfolgungsebenen](winsock-tracing-levels.md)
</dt> <dt>

[Details zur Ablaufverfolgung von Winsock-Katalogänderungen](winsock-layered-service-provider-tracing-event-details.md)
</dt> </dl>

 

