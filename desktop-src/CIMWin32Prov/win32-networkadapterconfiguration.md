---
description: Stellt die Attribute und Verhalten eines Netzwerkadapters dar. Diese Klasse enthält zusätzliche Eigenschaften und Methoden, die die Verwaltung des vom Netzwerkadapter unabhängigen TCP/IP-Protokolls unterstützen.
ms.assetid: 690b46ed-a065-4973-b044-0df4e81e41a1
ms.tgt_platform: multiple
title: Win32_NetworkAdapterConfiguration-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration
- Win32_NetworkAdapterConfiguration.Caption
- Win32_NetworkAdapterConfiguration.Description
- Win32_NetworkAdapterConfiguration.SettingID
- Win32_NetworkAdapterConfiguration.ArpAlwaysSourceRoute
- Win32_NetworkAdapterConfiguration.ArpUseEtherSNAP
- Win32_NetworkAdapterConfiguration.DatabasePath
- Win32_NetworkAdapterConfiguration.DeadGWDetectEnabled
- Win32_NetworkAdapterConfiguration.DefaultIPGateway
- Win32_NetworkAdapterConfiguration.DefaultTOS
- Win32_NetworkAdapterConfiguration.DefaultTTL
- Win32_NetworkAdapterConfiguration.DHCPEnabled
- Win32_NetworkAdapterConfiguration.DHCPLeaseExpires
- Win32_NetworkAdapterConfiguration.DHCPLeaseObtained
- Win32_NetworkAdapterConfiguration.DHCPServer
- Win32_NetworkAdapterConfiguration.DNSDomain
- Win32_NetworkAdapterConfiguration.DNSDomainSuffixSearchOrder
- Win32_NetworkAdapterConfiguration.DNSEnabledForWINSResolution
- Win32_NetworkAdapterConfiguration.DNSHostName
- Win32_NetworkAdapterConfiguration.DNSServerSearchOrder
- Win32_NetworkAdapterConfiguration.DomainDNSRegistrationEnabled
- Win32_NetworkAdapterConfiguration.ForwardBufferMemory
- Win32_NetworkAdapterConfiguration.FullDNSRegistrationEnabled
- Win32_NetworkAdapterConfiguration.GatewayCostMetric
- Win32_NetworkAdapterConfiguration.IGMPLevel
- Win32_NetworkAdapterConfiguration.Index
- Win32_NetworkAdapterConfiguration.InterfaceIndex
- Win32_NetworkAdapterConfiguration.IPAddress
- Win32_NetworkAdapterConfiguration.IPConnectionMetric
- Win32_NetworkAdapterConfiguration.IPEnabled
- Win32_NetworkAdapterConfiguration.IPFilterSecurityEnabled
- Win32_NetworkAdapterConfiguration.IPPortSecurityEnabled
- Win32_NetworkAdapterConfiguration.IPSecPermitIPProtocols
- Win32_NetworkAdapterConfiguration.IPSecPermitTCPPorts
- Win32_NetworkAdapterConfiguration.IPSecPermitUDPPorts
- Win32_NetworkAdapterConfiguration.IPSubnet
- Win32_NetworkAdapterConfiguration.IPUseZeroBroadcast
- Win32_NetworkAdapterConfiguration.IPXAddress
- Win32_NetworkAdapterConfiguration.IPXEnabled
- Win32_NetworkAdapterConfiguration.IPXFrameType
- Win32_NetworkAdapterConfiguration.IPXMediaType
- Win32_NetworkAdapterConfiguration.IPXNetworkNumber
- Win32_NetworkAdapterConfiguration.IPXVirtualNetNumber
- Win32_NetworkAdapterConfiguration.KeepAliveInterval
- Win32_NetworkAdapterConfiguration.KeepAliveTime
- Win32_NetworkAdapterConfiguration.MACAddress
- Win32_NetworkAdapterConfiguration.MTU
- Win32_NetworkAdapterConfiguration.NumForwardPackets
- Win32_NetworkAdapterConfiguration.PMTUBHDetectEnabled
- Win32_NetworkAdapterConfiguration.PMTUDiscoveryEnabled
- Win32_NetworkAdapterConfiguration.ServiceName
- Win32_NetworkAdapterConfiguration.TcpipNetbiosOptions
- Win32_NetworkAdapterConfiguration.TcpMaxConnectRetransmissions
- Win32_NetworkAdapterConfiguration.TcpMaxDataRetransmissions
- Win32_NetworkAdapterConfiguration.TcpNumConnections
- Win32_NetworkAdapterConfiguration.TcpUseRFC1122UrgentPointer
- Win32_NetworkAdapterConfiguration.TcpWindowSize
- Win32_NetworkAdapterConfiguration.WINSEnableLMHostsLookup
- Win32_NetworkAdapterConfiguration.WINSHostLookupFile
- Win32_NetworkAdapterConfiguration.WINSPrimaryServer
- Win32_NetworkAdapterConfiguration.WINSScopeID
- Win32_NetworkAdapterConfiguration.WINSSecondaryServer
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2bccbe7fc44e75c2448d2eda800fe3c14cd13a9b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127469"
---
# <a name="win32_networkadapterconfiguration-class"></a>Win32 \_ networkadapterconfiguration-Klasse

Die **Win32 \_ networkadapterconfiguration** - [WMI-Klasse](../wmisdk/retrieving-a-class.md)stellt die Attribute und Verhalten eines Netzwerkadapters dar. Diese Klasse enthält zusätzliche Eigenschaften und Methoden, die die Verwaltung des vom Netzwerkadapter unabhängigen TCP/IP-Protokolls unterstützen.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C515-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_NetworkAdapterConfiguration : CIM_Setting
{
  string   Caption;
  string   Description;
  string   SettingID;
  boolean  ArpAlwaysSourceRoute;
  boolean  ArpUseEtherSNAP;
  string   DatabasePath;
  boolean  DeadGWDetectEnabled;
  string   DefaultIPGateway[];
  uint8    DefaultTOS;
  uint8    DefaultTTL;
  boolean  DHCPEnabled;
  datetime DHCPLeaseExpires;
  datetime DHCPLeaseObtained;
  string   DHCPServer;
  string   DNSDomain;
  string   DNSDomainSuffixSearchOrder[];
  boolean  DNSEnabledForWINSResolution;
  string   DNSHostName;
  string   DNSServerSearchOrder[];
  boolean  DomainDNSRegistrationEnabled;
  uint32   ForwardBufferMemory;
  boolean  FullDNSRegistrationEnabled;
  uint16   GatewayCostMetric[];
  uint8    IGMPLevel;
  uint32   Index;
  uint32   InterfaceIndex;
  string   IPAddress[];
  uint32   IPConnectionMetric;
  boolean  IPEnabled;
  boolean  IPFilterSecurityEnabled;
  boolean  IPPortSecurityEnabled;
  string   IPSecPermitIPProtocols[];
  string   IPSecPermitTCPPorts[];
  string   IPSecPermitUDPPorts[];
  string   IPSubnet[];
  boolean  IPUseZeroBroadcast;
  string   IPXAddress;
  boolean  IPXEnabled;
  uint32   IPXFrameType[];
  uint32   IPXMediaType;
  string   IPXNetworkNumber[];
  string   IPXVirtualNetNumber;
  uint32   KeepAliveInterval;
  uint32   KeepAliveTime;
  string   MACAddress;
  uint32   MTU;
  uint32   NumForwardPackets;
  boolean  PMTUBHDetectEnabled;
  boolean  PMTUDiscoveryEnabled;
  string   ServiceName;
  uint32   TcpipNetbiosOptions;
  uint32   TcpMaxConnectRetransmissions;
  uint32   TcpMaxDataRetransmissions;
  uint32   TcpNumConnections;
  boolean  TcpUseRFC1122UrgentPointer;
  uint16   TcpWindowSize;
  boolean  WINSEnableLMHostsLookup;
  string   WINSHostLookupFile;
  string   WINSPrimaryServer;
  string   WINSScopeID;
  string   WINSSecondaryServer;
};
```

## <a name="members"></a>Member

Die **Win32 \_ networkadapterconfiguration** -Klasse verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **Win32 \_ networkadapterconfiguration** -Klasse verfügt über diese Methoden.



| Methode                                                                                                                       | BESCHREIBUNG                                                                                                                                           |
|:-----------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DisableIPSec**](disableipsec-method-in-class-win32-networkadapterconfiguration.md)                                       | Deaktiviert IPSec auf diesem TCP/IP-fähigen Netzwerkadapter.<br/>                                                                                     |
| [**EnableDHCP**](enabledhcp-method-in-class-win32-networkadapterconfiguration.md)                                           | Aktiviert das Dynamic Host Configuration-Protokoll (DHCP) für den Dienst mit diesem Netzwerkadapter.<br/>                                              |
| [**EnableDNS**](enabledns-method-in-class-win32-networkadapterconfiguration.md)                                             | Aktiviert die Domain Name System (DNS) für den Dienst auf diesem TCP/IP-gebundenen Netzwerkadapter.<br/>                                                     |
| [**EnableIPFilterSec**](enableipfiltersec-method-in-class-win32-networkadapterconfiguration.md)                             | Aktiviert IPSec Global über alle IP-gebundenen Netzwerkadapter hinweg.<br/>                                                                               |
| [**EnableIPSec**](enableipsec-method-in-class-win32-networkadapterconfiguration.md)                                         | Aktiviert IPSec auf diesem speziellen TCP/IP-fähigen Netzwerkadapter.<br/>                                                                             |
| [**EnableStatic**](enablestatic-method-in-class-win32-networkadapterconfiguration.md)                                       | Aktiviert die statische TCP/IP-Adressierung für den Zielnetzwerk Adapter.<br/>                                                                           |
| [**EnableWINS**](enablewins-method-in-class-win32-networkadapterconfiguration.md)                                           | Aktiviert WINS-Einstellungen, die für TCP/IP spezifisch sind, aber unabhängig vom Netzwerkadapter.<br/>                                                          |
| [**ReleaseDHCPLease**](releasedhcplease-method-in-class-win32-networkadapterconfiguration.md)                               | Gibt die IP-Adresse frei, die an einen bestimmten DHCP-fähigen Netzwerkadapter gebunden ist.<br/>                                                                  |
| [**ReleaseDHCPLeaseAll**](releasedhcpleaseall-method-in-class-win32-networkadapterconfiguration.md)                         | Gibt die IP-Adressen frei, die an alle DHCP-fähigen Netzwerkadapter gebunden sind.<br/>                                                                      |
| [**RenewDHCPLease**](renewdhcplease-method-in-class-win32-networkadapterconfiguration.md)                                   | Erneuert die IP-Adresse auf bestimmten DHCP-fähigen Netzwerkadaptern.<br/>                                                                           |
| [**RenewDHCPLeaseAll**](renewdhcpleaseall-method-in-class-win32-networkadapterconfiguration.md)                             | Erneuert die IP-Adressen auf allen DHCP-fähigen Netzwerkadaptern.<br/>                                                                              |
| [**"Starpalwayssourceroute"**](setarpalwayssourceroute-method-in-class-win32-networkadapterconfiguration.md)                 | Legt die Übertragung von ARP-Abfragen durch TCP/IP fest.<br/>                                                                                        |
| [**SetArpUseEtherSNAP**](setarpuseethersnap-method-in-class-win32-networkadapterconfiguration.md)                           | Ermöglicht Ethernet-Paketen die Verwendung der 802,3-Snap-Codierung.<br/>                                                                                       |
| [**SetDatabasePath**](setdatabasepath-method-in-class-win32-networkadapterconfiguration.md)                                 | Legt den Pfad zu den standardmäßigen Internet Datenbankdateien (Hosts, LMHOSTS, Netzwerke und Protokolle) fest.<br/>                                           |
| [**Setdeadgwdetect**](setdeadgwdetect-method-in-class-win32-networkadapterconfiguration.md)                                 | Ermöglicht die Erkennung von deadlockgateways.<br/>                                                                                                            |
| [**Setdefaulttos**](setdefaulttos-method-in-class-win32-networkadapterconfiguration.md)                                     | Veraltet. Diese Methode legt den Standardtyp des Dienst Werts (TOS) im Header von ausgehenden IP-Paketen fest.<br/>                                   |
| [**Setdefaultttl**](setdefaultttl-method-in-class-win32-networkadapterconfiguration.md)                                     | Legt den Standardwert für die Gültigkeitsdauer (Time to Live, TTL) im Header von ausgehenden IP-Paketen fest<br/>                                                            |
| [**SetDNSDomain**](setdnsdomain-method-in-class-win32-networkadapterconfiguration.md)                                       | Legt die DNS-Domäne fest.<br/>                                                                                                                       |
| [**SetDNSServerSearchOrder**](setdnsserversearchorder-method-in-class-win32-networkadapterconfiguration.md)                 | Legt die Server Such Reihenfolge als Array von-Elementen fest.<br/>                                                                                      |
| [**SetDNSSuffixSearchOrder**](setdnssuffixsearchorder-method-in-class-win32-networkadapterconfiguration.md)                 | Legt die Suffixsuchreihenfolge als Array von-Elementen fest.<br/>                                                                                      |
| [**SetDynamicDNSRegistration**](setdynamicdnsregistration-method-in-class-win32-networkadapterconfiguration.md)             | Gibt die dynamische DNS-Registrierung von IP-Adressen für diesen IP-gebundenen Adapter an.<br/>                                                              |
| [**SetForwardBufferMemory**](setforwardbuffermemory-method-in-class-win32-networkadapterconfiguration.md)                   | Gibt an, wie viel Arbeitsspeicher-IP zugewiesen wird, um Paketdaten in der Routerpaketwarteschlange<br/>                                                    |
| [**SetGateways**](setgateways-method-in-class-win32-networkadapterconfiguration.md)                                         | Gibt eine Liste von Gateways für das Routing von Paketen an, die für ein anderes Subnetz bestimmt sind als das, mit dem dieser Adapter verbunden ist.<br/>                |
| [**Setigmplevel**](setigmplevel-method-in-class-win32-networkadapterconfiguration.md)                                       | Legt den Umfang fest, in dem das System IP-Multicasting unterstützt und am Internet Group Management-Protokoll teilnimmt.<br/>                   |
| [**"Abkconnectionmetric"**](setipconnectionmetric-method-in-class-win32-networkadapterconfiguration.md)                     | Legt die Routing Metrik fest, die diesem IP-gebundenen Adapter zugeordnet ist.<br/>                                                                             |
| [**"S"**](setipusezerobroadcast-method-in-class-win32-networkadapterconfiguration.md)                     | Legt die Verwendung von IP Zero Broadcast fest.<br/>                                                                                                              |
| [**"Setxframetypetworkpair"**](win32-networkadapterconfiguration-setipxframetypenetworkpairs.md)                         | Legt die IPX-Netzwerk Nummer/-Frame Paare für diesen Netzwerkadapter fest.<br/>                                            |
| [**"Stipxvirtualnetworknumber"**](win32-networkadapterconfiguration-setipxvirtualnetworknumber.md)                           | Legt die virtuelle IPX-Netzwerk Nummer (Internetworking Packet Exchange) auf dem Zielcomputer System fest.<br/>                                       |
| [**Setkeepaliveingeterval**](setkeepaliveinterval-method-in-class-win32-networkadapterconfiguration.md)                       | Legt das Intervall zum Trennen von Keep-Alive-Neuübertragungen fest, bis eine Antwort empfangen wird.<br/>                                                      |
| [**Setkeepalivetime**](setkeepalivetime-method-in-class-win32-networkadapterconfiguration.md)                               | Legt fest, wie oft TCP überprüft, ob eine Verbindung im Leerlauf noch verfügbar ist, indem ein Keep-Alive-Paket gesendet wird.<br/>                           |
| [**"Ab-TU"**](setmtu-method-in-class-win32-networkadapterconfiguration.md)                                                   | Legt die standardmäßige maximale Übertragungseinheit (Maximum Transmission Unit, MTU) für eine Netzwerkschnittstelle fest.<br/> Diese Methode wird nicht unterstützt.<br/>                         |
| [**Setnumforwardpakete**](setnumforwardpackets-method-in-class-win32-networkadapterconfiguration.md)                       | Legt die Anzahl der der Routerpaketwarteschlange zugeordneten IP-Paket Header fest.<br/>                                                                |
| [**SetPMTUBHDetect**](setpmtubhdetect-method-in-class-win32-networkadapterconfiguration.md)                                 | Ermöglicht die Erkennung von Black-Hole-Routern.<br/>                                                                                                   |
| [**SetPMTUDiscovery**](setpmtudiscovery-method-in-class-win32-networkadapterconfiguration.md)                               | Ermöglicht die Ermittlung von maximalen Übertragungs Einheiten (MTU).<br/>                                                                                         |
| [**SetTcpipNetbios**](settcpipnetbios-method-in-class-win32-networkadapterconfiguration.md)                                 | Legt den Standard Vorgang von NetBIOS über TCP/IP fest.<br/>                                                                                         |
| [**Settcpmaxconnectretransmissions**](settcpmaxconnectretransmissions-method-in-class-win32-networkadapterconfiguration.md) | Legt fest, wie viele Versuche TCP eine Verbindungsanforderung erneut übermittelt, bevor Sie abgebrochen werden.<br/>                                                         |
| [**SetTcpMaxDataRetransmissions**](settcpmaxdataretransmissions-method-in-class-win32-networkadapterconfiguration.md)       | Legt fest, wie oft TCP ein einzelnes Daten Segment erneut überträgt, bevor die Verbindung abgebrochen wird.<br/>                                    |
| [**SetTcpNumConnections**](settcpnumconnections-method-in-class-win32-networkadapterconfiguration.md)                       | Legt die maximale Anzahl von Verbindungen fest, die von TCP gleichzeitig geöffnet werden können.<br/>                                                              |
| [**SetTcpUseRFC1122UrgentPointer**](settcpuserfc1122urgentpointer-method-in-class-win32-networkadapterconfiguration.md)     | Gibt an, ob TCP die RFC 1122-Spezifikation für dringende Daten oder den Modus verwendet, der von den von Berkeley (Berkeley Software Design) abgeleiteten Systemen verwendet wird.<br/> |
| [**Settcpwindowsize**](settcpwindowsize-method-in-class-win32-networkadapterconfiguration.md)                               | Legt die maximale TCP-Empfangs Fenstergröße fest, die vom System bereitgestellt wird.<br/>                                                                            |
| [**SetWINSServer**](setwinsserver-method-in-class-win32-networkadapterconfiguration.md)                                     | Legt die primären und sekundären WINS-Server (Windows Internet Naming Service) auf diesem TCP/IP-gebundenen Netzwerkadapter fest.<br/>                        |



 

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ networkadapterconfiguration** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**ArpAlwaysSourceRoute**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| ArpAlwaysSourceRoute")
</dt> </dl>

**True** gibt an, dass TCP/IP-ARP-Abfragen (Address Resolution Protocol) mit aktiviertem Quell Routing in Tokenringnetzwerken überträgt. In der Standardeinstellung (false) werden ARP zuerst ohne Quell Routing abgefragt, und es wird dann erneut versucht, das Quell Routing zu aktivieren, wenn keine Antwort empfangen wird. Das Quell Routing ermöglicht das Routing von Netzwerk Paketen über verschiedene Arten von Netzwerken.

</dd> <dt>

**ArpUseEtherSNAP**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| ArpUseEtherSNAP")
</dt> </dl>

**True** gibt an, dass Ethernet-Pakete die IEEE 802,3-Snap-Codierung (Sub-Network Access Protocol) befolgen. Wenn dieser Parameter auf 1 festgelegt wird, wird TCP/IP zum Übertragen von Ethernet-Paketen mithilfe der 802,3-Snap-Codierung Standardmäßig (false) überträgt der Stapel Pakete im Dix Ethernet-Format.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Kurze Textbeschreibung des aktuellen-Objekts.

Diese Eigenschaft wird von der [**CIM- \_ Einstellung**](cim-setting.md)geerbt.

</dd> <dt>

**DatabasePath**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| DatabasePath")
</dt> </dl>

Gültiger Windows-Dateipfad zu standardmäßigen Internet Datenbankdateien (Hosts, LMHOSTS, Netzwerke und Protokolle). Der Dateipfad wird von der Windows Sockets-Schnittstelle verwendet.

</dd> <dt>

**DeadGWDetectEnabled**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| EnableDeadGWDetect")
</dt> </dl>

**True** gibt an, dass die Erkennung von deadlockgateways erfolgt Wenn diese Funktion aktiviert ist, fordert das Transmission Control Protocol (TCP) das Internet Protokoll (IP) auf, um zu einem Sicherungs Gateway zu wechseln, wenn ein Segment mehrmals neu übermittelt wird, ohne dass eine Antwort empfangen wird.

</dd> <dt>

**DefaultIPGateway**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \| Parameters \| DefaultGateway")
</dt> </dl>

Array von IP-Adressen von Standard Gateways, die vom Computersystem verwendet werden.

Beispiel: "192.168.12.1 192.168.46.1"

</dd> <dt>

**DefaultTOS**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| DefaultTOS")
</dt> </dl>

Der Standardwert für den Diensttyp (TOS), der im Header der ausgehenden IP-Pakete festgelegt ist. Request for Comments (RFC) 791 definiert die Werte. Standardwert: 0 (null), gültiger Bereich: 0-255.

</dd> <dt>

**DefaultTTL**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| DefaultTTL")
</dt> </dl>

Der Standardwert für die Gültigkeitsdauer (TTL), der im Header der ausgehenden IP-Pakete festgelegt ist Die Gültigkeitsdauer gibt an, wie viele Router ein IP-Paket durchlaufen kann, um das Ziel zu erreichen, bevor es verworfen wird. Jeder Router dekrementierungen um die TTL-Anzahl eines Pakets beim durchlaufen und verwirft die Pakete – wenn die Gültigkeitsdauer 0 (null) ist. Standardwert: 32, gültiger Bereich: 1-255.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Textbeschreibung des aktuellen-Objekts.

Diese Eigenschaft wird von der [**CIM- \_ Einstellung**](cim-setting.md)geerbt.

</dd> <dt>

**DHCPEnabled**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \| EnableDHCP")
</dt> </dl>

**True** gibt an, dass der DHCP-Server (Dynamic Host Configuration Protocol) beim Herstellen einer Netzwerkverbindung dem Computersystem automatisch eine IP-Adresse zuweist.

</dd> <dt>

**Dhcpleaseabläuft**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \| leaseterminatestime")
</dt> </dl>

Ablaufdatum und-Uhrzeit für eine geleast-IP-Adresse, die dem Computer vom DHCP-Server (Dynamic Host Configuration-Protokoll) zugewiesen wurde.

Beispiel: 20521201000230,000000000

</dd> <dt>

**Dhcpleasebezogen**
</dt> <dd> <dl> <dt>

**Datentyp: DateTime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \| leaseobtainedtime")
</dt> </dl>

Datum und Uhrzeit, zu der die Lease für die IP-Adresse abgerufen wurde, die dem Computer vom DHCP-Server (Dynamic Host Configuration Protocol) zugewiesen wurde.

Beispiel: 19521201000230,000000000

</dd> <dt>

**Dhcpserver ein**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \| DHCPServer")
</dt> </dl>

Die IP-Adresse des DHCP-Servers (Dynamic Host Configuration Protocol).

Beispiel: "10.55.34.2"

</dd> <dt>

**DNSDomain**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| Domain")
</dt> </dl>

Organisationsname, gefolgt von einem Zeitraum und einer Erweiterung, die den Typ der Organisation angibt, z. b. "Microsoft.com". Der Name kann eine beliebige Kombination der Buchstaben A bis Z, die Ziffern 0 bis 9 und der Bindestrich (-) sowie das Zeichen (.) sein, das als Trennzeichen verwendet wird.

Beispiel: "Microsoft.com"

</dd> <dt>

**DNSDomainSuffixSearchOrder**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| SEARCHLIST")
</dt> </dl>

Array von DNS-Domänen Suffixen, das während der Namensauflösung an das Ende der Hostnamen angehängt werden soll. Wenn Sie versuchen, einen vollständig qualifizierten Domänen Namen (FQDN) aus einem reinen Host Namen aufzulösen, fügt das System zuerst den lokalen Domänen Namen an. Wenn dies nicht erfolgreich ist, verwendet das System die Liste der Domänen Suffixe, um zusätzliche FQDNs in der aufgeführten Reihenfolge zu erstellen und die DNS-Server für jede zu Abfragen.

Beispiel: "Samples.Microsoft.com example.Microsoft.com"

</dd> <dt>

**DNSEnabledForWINSResolution**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| EnableDNS")
</dt> </dl>

**True** gibt an, dass die Domain Name System (DNS) für die Namensauflösung über die WINS-Auflösung (Windows Internet Naming Service) aktiviert ist. Wenn der Name nicht mit DNS aufgelöst werden kann, wird die namens Anforderung zur Auflösung an WINS weitergeleitet.

</dd> <dt>

**DNSHostName**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| Hostname")
</dt> </dl>

Der Hostname, der zum Identifizieren des lokalen Computers für die Authentifizierung durch einige Hilfsprogramme verwendet wird. Andere auf TCP/IP basierende Hilfsprogramme können diesen Wert verwenden, um den Namen des lokalen Computers abzurufen. Hostnamen werden auf DNS-Servern in einer Tabelle gespeichert, die Namen zu IP-Adressen für die Verwendung durch DNS zuordnet. Der Name kann eine beliebige Kombination der Buchstaben A bis Z, die Ziffern 0 bis 9 und der Bindestrich (-) sowie das Zeichen (.) sein, das als Trennzeichen verwendet wird. Standardmäßig ist dieser Wert der Computername des Microsoft-Netzwerks, aber der Netzwerkadministrator kann einen anderen Hostnamen zuweisen, ohne dass sich dies auf den Computernamen auswirkt.

Beispiel: "corpdns"

</dd> <dt>

**DNSServerSearchOrder**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| Nameserver")
</dt> </dl>

Array von Server-IP-Adressen, die zum Abfragen von DNS-Servern verwendet werden sollen.

</dd> <dt>

**Domaindnsregistrationaktiviert**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Wenn der Wert **true** ist, werden die IP-Adressen für diese Verbindung in DNS unter dem Domänen Namen dieser Verbindung registriert, zusätzlich zur Registrierung unter dem vollständigen DNS-Namen des Computers. Der Domänen Name dieser Verbindung wird entweder mit der [**SetDNSDomain**](setdnsdomain-method-in-class-win32-networkadapterconfiguration.md)()-Methode festgelegt oder von DSCP zugewiesen. Der registrierte Name ist der Hostname des Computers, dem der Domänen Name angefügt wird.

</dd> <dt>

**ForwardBufferMemory**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| ForwardBufferMemory"), [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Bytes")
</dt> </dl>

Von IP zugewiesener Arbeitsspeicher zum Speichern von Paketdaten in der Routerpaketwarteschlange Wenn dieser Pufferbereich ausgefüllt ist, beginnt der Router, Pakete zufällig aus der Warteschlange zu verwerfen. Der Datenpuffer der Paket Warteschlange beträgt 256 Bytes, daher sollte der Wert dieses Parameters ein Vielfaches von 256 sein. Mehrere Puffer werden für größere Pakete miteinander verkettet. Der IP-Header für ein Paket wird separat gespeichert. Dieser Parameter wird ignoriert, und es werden keine Puffer zugewiesen, wenn der IP-Router nicht aktiviert ist. Die Puffergröße kann zwischen der Netzwerk-MTU und einem Wert kleiner als 0xffffffff liegen. Standardwert: 74240 (50 1480-Byte-Pakete, gerundet auf ein Vielfaches von 256).

</dd> <dt>

**Fulldnsregistrationaktivierte**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

**True** gibt an, dass die IP-Adressen für diese Verbindung in DNS unter dem vollständigen DNS-Namen des Computers registriert sind. Der vollständige DNS-Name des Computers wird auf der Registerkarte **Netzwerk Identifizierung** in der System Anwendung in der System Steuerung angezeigt.

</dd> <dt>

**GatewayCostMetric**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Array von ganzzahligen Kosten Metrik Werten (im Bereich von 1 bis 9999), die zum Berechnen der schnellsten, zuverlässigsten oder am wenigsten ressourcenintensiven Routen verwendet werden. Dieses Argument weist eine eins-zu-eins-Entsprechung mit der **DefaultIPGateway** -Eigenschaft auf.

</dd> <dt>

**IGMPLevel**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| IGMPLevel")
</dt> </dl>

Der Umfang, in dem das System IP-Multicast unterstützt und am IGMP (Internet Group Management Protocol) teilnimmt. Auf Ebene 0 (null) stellt das System keine Multicast Unterstützung bereit. Auf Ebene 1 kann das System nur IP-Multicast Pakete senden. Auf Ebene 2 kann das System IP-Multicast Pakete senden und für den Empfang von Multicast Paketen vollständig an IGMP teilnehmen.

<dt>

<span id="No_Multicast"></span><span id="no_multicast"></span><span id="NO_MULTICAST"></span>

<span id="No_Multicast"></span><span id="no_multicast"></span><span id="NO_MULTICAST"></span>**Kein Multicast** (0)


</dt> <dd></dd> <dt>

<span id="IP_Multicast"></span><span id="ip_multicast"></span><span id="IP_MULTICAST"></span>

<span id="IP_Multicast"></span><span id="ip_multicast"></span><span id="IP_MULTICAST"></span>**IP-Multicast** (1)


</dt> <dd></dd> <dt>

<span id="IP___IGMP_multicast"></span><span id="ip___igmp_multicast"></span><span id="IP___IGMP_MULTICAST"></span>

<span id="IP___IGMP_multicast"></span><span id="ip___igmp_multicast"></span><span id="IP___IGMP_MULTICAST"></span>**IP-& IGMP-Multicast** (2)


</dt> <dd>

IP-und IGMP-Multicast (Standard)

</dd> </dl>

</dd> <dt>

**Index**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](../wmisdk/key-qualifier.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \\ \\ {4D36E972-E325-11CE-BFC1-08002BE10318}")
</dt> </dl>

Index Nummer der Windows-Netzwerkadapter Konfiguration. Die Indexnummer wird verwendet, wenn mehr als eine Konfiguration verfügbar ist.

</dd> <dt>

**InterfaceIndex**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Indexwert, der eine lokale Netzwerkschnittstelle eindeutig identifiziert. Der Wert in dieser Eigenschaft ist identisch mit dem Wert in der **interfakeindex** -Eigenschaft in der Instanz von [**Win32 \_ IP4RouteTable**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetable) , die die Netzwerkschnittstelle in der Routing Tabelle darstellt.

</dd> <dt>

**IPAddress**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \| Parameters \\ \\ tcpip \| IPAddress")
</dt> </dl>

Array mit allen IP-Adressen, die dem aktuellen Netzwerkadapter zugeordnet sind. Diese Eigenschaft kann entweder IPv6-Adressen oder IPv4-Adressen enthalten. Weitere Informationen finden Sie [unter IPv6-und IPv4-Unterstützung in WMI](../wmisdk/ipv6-and-ipv4-support-in-wmi.md).

Beispiel für eine IPv6-Adresse: "2010:836b: 4179:: 836b: 4179"

</dd> <dt>

**IPConnectionMetric**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Kosten für die Verwendung der konfigurierten Routen für den IP-gebundenen Adapter und sind der gewichtete Wert für diese Routen in der IP-Routing Tabelle. Wenn mehrere Routen zu einem Ziel in der IP-Routing Tabelle vorhanden sind, wird die Route mit der niedrigsten Metrik verwendet. Der Standardwert ist 1.

</dd> <dt>

**IPEnabled**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \| Parameters \\ \\ tcpip")
</dt> </dl>

**True** gibt an, dass TCP/IP auf diesem Netzwerkadapter gebunden und aktiviert ist.

</dd> <dt>

**Ipfiltersecurityaktiviert**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| ipfiltersecurityaktivierte")
</dt> </dl>

Bei " **true**" wird die IP-Port Sicherheit Global über alle IP-gebundenen Netzwerkadapter hinweg aktiviert, und die Sicherheitswerte, die den einzelnen Netzwerkadaptern zugeordnet sind, sind wirksam. Diese Eigenschaft wird in Verbindung mit **IPSecPermitTCPPorts**, **IPSecPermitUDPPorts** und **ipsecperentschärpprotokolls** verwendet. Bei " **false**" wird die IP-Filter Sicherheit auf allen Netzwerkadaptern deaktiviert und ermöglicht, dass der gesamte Port-und Protokoll Datenverkehr ungefiltert erfolgt.

</dd> <dt>

**Ipportsecurityaktivierte**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**veraltet**](../wmisdk/standard-wmi-qualifiers.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ networkadapterconfiguration \| ipfiltersecurityaktivierte")
</dt> </dl>

**True** gibt an, dass die IP-Port Sicherheit Global über alle IP-gebundenen Netzwerkadapter hinweg aktiviert ist. Diese Eigenschaft ist veraltet. Anstelle dieser Eigenschaft sollten Sie **ipfiltersecurityaktivierte** verwenden.

</dd> <dt>

**Ipsecperentschärpprotokolle**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| rawipallowedprotokolls")
</dt> </dl>

Array der Protokolle, die über die IP ausgeführt werden dürfen. Die Liste der Protokolle wird mithilfe der [**EnableIPSec**](enableipsec-method-in-class-win32-networkadapterconfiguration.md) -Methode definiert. Die Liste ist entweder leer oder enthält numerische Werte. Ein numerischer Wert von 0 (null) gibt an, dass für alle Protokolle die Zugriffsberechtigung gewährt wird. Eine leere Zeichenfolge gibt an, dass keine Protokolle ausgeführt werden dürfen, wenn **ipfiltersecurityaktivitrue** ist. 

</dd> <dt>

**IPSecPermitTCPPorts**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| tcpallowedports")
</dt> </dl>

Array der Ports, denen die Zugriffsberechtigung für TCP erteilt wird. Die Liste der Protokolle wird mithilfe der [**EnableIPSec**](enableipsec-method-in-class-win32-networkadapterconfiguration.md) -Methode definiert. Die Liste ist entweder leer oder enthält numerische Werte. Ein numerischer Wert von 0 (null) gibt an, dass für alle Ports die Zugriffsberechtigung gewährt wird. Eine leere Zeichenfolge gibt an, dass keinen Ports die Zugriffsberechtigung erteilt wird, wenn **ipfiltersecurityaktivitrue** ist. 

</dd> <dt>

**IPSecPermitUDPPorts**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| udpallowedports")
</dt> </dl>

Array der Ports, dem die UDP (User Datagram Protocol)-Zugriffsberechtigung gewährt wird. Die Liste der Protokolle wird mithilfe der [**EnableIPSec**](enableipsec-method-in-class-win32-networkadapterconfiguration.md) -Methode definiert. Die Liste ist entweder leer oder enthält numerische Werte. Ein numerischer Wert von 0 (null) gibt an, dass für alle Ports die Zugriffsberechtigung gewährt wird. Eine leere Zeichenfolge gibt an, dass keinen Ports die Zugriffsberechtigung erteilt wird, wenn **ipfiltersecurityaktivitrue** ist. 

</dd> <dt>

**IPSubnet**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \| Parameters \| Subnetmask")
</dt> </dl>

Array aller Subnetzmasken, die dem aktuellen Netzwerkadapter zugeordnet sind.

Beispiel: "255.255.0.0"

</dd> <dt>

**Ipuabzerobroadcast**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| UseZeroBroadcast")
</dt> </dl>

**True** gibt an, dass IP-Nullen-Übertragungen verwendet werden (0.0.0.0), und das System verwendet Übertragungen (255.255.255.255). Computer Systeme verwenden normalerweise solche-Sendungen, aber von BSD-Implementierungen abgeleitete, verwenden Nullen-Sendungen. Systeme, die nicht die gleichen Übertragungen verwenden, werden nicht im selben Netzwerk zusammenarbeiten. Der Standardwert ist **false**.

</dd> <dt>

**IPXAddress**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**veraltet**](../wmisdk/standard-wmi-qualifiers.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Windows Sockets Version 2 \| [**getsockopt**](/windows/win32/api/winsock/nf-winsock-getsockopt) \| IPX \_ Address")
</dt> </dl>

Die IPX-Technologie (Internetwork Packet Exchange) wird nicht mehr unterstützt, und diese Eigenschaft enthält keine nützlichen Daten.

</dd> <dt>

**Ipxaktiviert**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**veraltet**](../wmisdk/standard-wmi-qualifiers.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Die IPX-Technologie (Internetwork Packet Exchange) wird nicht mehr unterstützt, und diese Eigenschaft enthält keine nützlichen Daten.

</dd> <dt>

**IPXFrameType**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**veraltet**](../wmisdk/standard-wmi-qualifiers.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ Nwlnkipx \\ \\ Parameters \| PktType")
</dt> </dl>

Die IPX-Technologie (Internetwork Packet Exchange) wird nicht mehr unterstützt, und diese Eigenschaft enthält keine nützlichen Daten.

<dt>

<span id="Ethernet_II"></span><span id="ethernet_ii"></span><span id="ETHERNET_II"></span>

**Ethernet II** (0)


</dt> <dd></dd> <dt>

<span id="Ethernet_802.3"></span><span id="ethernet_802.3"></span><span id="ETHERNET_802.3"></span>

**Ethernet 802,3** (1)


</dt> <dd></dd> <dt>

<span id="Ethernet_802.2"></span><span id="ethernet_802.2"></span><span id="ETHERNET_802.2"></span>

**Ethernet 802,2** (2)


</dt> <dd></dd> <dt>

<span id="Ethernet_SNAP"></span><span id="ethernet_snap"></span><span id="ETHERNET_SNAP"></span>

**Ethernet-Snap** (3)


</dt> <dd></dd> <dt>

<span id="AUTO"></span><span id="auto"></span>

**Auto** (255)


</dt> <dd></dd> </dl>

</dd> <dt>

**IPXMediaType**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**veraltet**](../wmisdk/standard-wmi-qualifiers.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ Nwlnkipx \\ \\ Parameters \| MediaType")
</dt> </dl>

Die IPX-Technologie (Internetwork Packet Exchange) wird nicht mehr unterstützt, und diese Eigenschaft enthält keine nützlichen Daten.

<dt>

<span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>

**Ethernet** (1)


</dt> <dd></dd> <dt>

<span id="Token_ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>

**TokenRing** (2)


</dt> <dd></dd> <dt>

<span id="FDDI"></span><span id="fddi"></span>

" **F** " (3)


</dt> <dd></dd> <dt>

<span id="ARCNET"></span><span id="arcnet"></span>

**ARCNET** (8)


</dt> <dd></dd> </dl>

</dd> <dt>

**IPXNetworkNumber**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**veraltet**](../wmisdk/standard-wmi-qualifiers.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ Nwlnkipx \\ \\ Parameters \| NetworkNumber")
</dt> </dl>

Die IPX-Technologie (Internetwork Packet Exchange) wird nicht mehr unterstützt, und diese Eigenschaft enthält keine nützlichen Daten.

</dd> <dt>

**IPXVirtualNetNumber**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**veraltet**](../wmisdk/standard-wmi-qualifiers.md), [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ Nwlnkipx \\ \\ Parameters \| VirtualNetworkNumber")
</dt> </dl>

Die IPX-Technologie (Internetwork Packet Exchange) wird nicht mehr unterstützt, und diese Eigenschaft enthält keine nützlichen Daten.

</dd> <dt>

**KeepAliveInterval**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| KeepAliveInterval"), [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Millisekunden")
</dt> </dl>

Intervall zum Trennen von Keep-Alive-reübertragungen, bis eine Antwort empfangen wird. Nachdem eine Antwort empfangen wurde, wird die Verzögerung bis zur nächsten Keep-Alive-Übertragung wieder durch den Wert von **KeepAliveTime** gesteuert. Die Verbindung wird abgebrochen, nachdem die Anzahl der von **TcpMaxDataRetransmissions** angegebenen Neuübertragungen nicht mehr offengelegt wurde. Standardwert: 1000, gültiger Bereich: 1-0xFFFFFFFF.

</dd> <dt>

**KeepAliveTime**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| KeepAliveInterval"), [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Millisekunden")
</dt> </dl>

Die **KeepAliveTime** -Eigenschaft gibt an, wie oft TCP versucht, zu überprüfen, ob eine Verbindung im Leerlauf noch intakt ist, indem ein Keep-Alive-Paket gesendet wird. Ein Remote System, das erreichbar ist, bestätigt die Keep-Alive-Übertragung. Keep-Alive-Pakete werden standardmäßig nicht gesendet. Diese Funktion kann in einer Verbindung von einer Anwendung aktiviert werden. Standardwert: 7,2 Millionen (zwei Stunden).

</dd> <dt>

**MACAddress**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Input and Output Functions \| DeviceIoControl")
</dt> </dl>

Media Access Control (Mac)-Adresse des Netzwerkadapters. Eine Mac-Adresse wird vom Hersteller zugewiesen, um den Netzwerkadapter eindeutig zu identifizieren.

Beispiel: "00:80: C7:8F: 6C: 96"

</dd> <dt>

**MTU**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| MTU"), [**Units**](../wmisdk/standard-qualifiers.md) ("Bytes")
</dt> </dl>

Überschreibt die standardmäßige maximale Übertragungseinheit (Maximum Transmission Unit, MTU) für eine Netzwerkschnittstelle. Die MTU ist die maximale Paketgröße (einschließlich der Transport Kopfzeile), die vom Transport über das zugrunde liegende Netzwerk übertragen wird. Das IP-Datagramm kann mehrere Pakete umfassen. Der Bereich dieses Werts umfasst die minimale Paketgröße (68) für die MTU, die vom zugrunde liegenden Netzwerk unterstützt wird.

</dd> <dt>

**Numforwardpakete**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| numforwardpakete")
</dt> </dl>

Anzahl der IP-Paket Header, die der Routerpaketwarteschlange zugeordnet sind Wenn alle Header verwendet werden, beginnt der Router, Pakete nach dem Zufallsprinzip aus der Warteschlange zu verwerfen. Dieser Wert muss mindestens so groß sein wie der **ForwardBufferMemory** -Wert, dividiert durch die maximale IP-Datengröße der mit dem Router verbundenen Netzwerke. Der Wert darf nicht größer sein als der **ForwardBufferMemory** -Wert dividiert durch 256, da für jedes Paket mindestens 256 Bytes an vorwärts Puffer Arbeitsspeicher verwendet werden. Die optimale Anzahl von vorwärts Paketen für eine bestimmte **ForwardBufferMemory** -Größe hängt von der Art des Datenverkehrs im Netzwerk ab. Sie liegt zwischen diesen beiden Werten. Wenn der Router nicht aktiviert ist, wird dieser Parameter ignoriert, und es werden keine Header zugeordnet. Standardwert: 50, gültiger Bereich: 1-0xFFFFFFFE.

</dd> <dt>

**PMTUBHDetectEnabled**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| EnablePMTUBHDetect")
</dt> </dl>

**True** gibt an, dass die Erkennung von Black-Hole-Routern erfolgt, während TCP den Pfad der maximalen Übertragungseinheit ermittelt. Ein schwarzer Loch Router gibt keine nicht erreichbaren ICMP-Ziele zurück, wenn er ein IP-Datagramm mit dem Bitsatz "nicht Fragment" fragmentieren muss. TCP ist davon abhängig, dass diese Nachrichten zum Durchführen der MTU-Ermittlung empfangen werden Wenn diese Funktion aktiviert ist, versucht TCP, Segmente ohne das Bit "nicht Fragment" zu senden, wenn mehrere Neuübertragungen eines Segments nicht bestätigt werden. Wenn das Segment als Ergebnis bestätigt wird, wird der MSS verringert, und das Bit "nicht Fragment" wird in zukünftigen Paketen der Verbindung festgelegt. Das Aktivieren der Black Hole-Erkennung erhöht die maximale Anzahl von erneuten Übertragungen, die für ein bestimmtes Segment ausgeführt werden. Der Standardwert dieser Eigenschaft ist **false**.

</dd> <dt>

**Pmtudiscoveryaktivierte**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| EnablePMTUDiscovery")
</dt> </dl>

Wenn der Wert **true** ist, wird der Wert für die maximale Übertragungseinheit (MTU) über dem Pfad zu einem Remote Host erkannt. Wenn Sie den MTU-Pfad ermitteln und TCP-Segmente auf diese Größe beschränken, kann TCP die Fragmentierung auf Routern entlang des Pfads eliminieren, der Netzwerke mit verschiedenen MTUs verbindet. Die Fragmentierung beeinträchtigt den TCP-Durchsatz und die Überlastung des Netzwerks. Wenn Sie diesen Parameter auf **false** festlegen, wird eine MTU von 576 Bytes für alle Verbindungen verwendet, die nicht zu Computern im lokalen Subnetz gehören. Der Standardwert ist " **true**".

</dd> <dt>

**Service Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ Network Cards \| ServiceName")
</dt> </dl>

Der Dienst Name des Netzwerkadapters. Dieser Name ist in der Regel kürzer als der vollständige Produktname.

Beispiel: "Elnkii"

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Der Bezeichner, durch den das aktuelle-Objekt bekannt ist.

Diese Eigenschaft wird von der [**CIM- \_ Einstellung**](cim-setting.md)geerbt.

</dd> <dt>

**TcpipNetbiosOptions**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Bitmap der möglichen Einstellungen im Zusammenhang mit NetBIOS über TCP/IP. Werte werden in der folgenden Liste angegeben.

<dt>

<span id="EnableNetbiosViaDhcp"></span><span id="enablenetbiosviadhcp"></span><span id="ENABLENETBIOSVIADHCP"></span>

**Enablenetbiosviadhcp** (0)


</dt> <dd></dd> <dt>

<span id="EnableNetbios"></span><span id="enablenetbios"></span><span id="ENABLENETBIOS"></span>

**Enablenetbios** (1)


</dt> <dd></dd> <dt>

<span id="DisableNetbios"></span><span id="disablenetbios"></span><span id="DISABLENETBIOS"></span>

**DisableNetbios** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**Tcpmaxconnectretransmissions**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| tcpmaxconnectretransmissions")
</dt> </dl>

Gibt an, wie oft TCP versucht, eine Verbindungsanforderung erneut zu übertragen, bevor die Verbindung beendet wird. Der anfängliche Neuübertragungs Timeout beträgt 3 Sekunden. Das Timeout für die erneute Übertragung verdoppelt sich für jeden Versuch. Standardwert: 3, gültiger Bereich: 0-0xFFFFFFFF.

</dd> <dt>

**TcpMaxDataRetransmissions**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| TcpMaxDataRetransmissions")
</dt> </dl>

Gibt an, wie oft TCP ein einzelnes Daten Segment (nonconnect-Segment) erneut überträgt, bevor die Verbindung beendet wird. Das Timeout für die erneute Übertragung verdoppelt sich mit jeder nachfolgenden erneuten Übertragung für eine Verbindung. Standardwert: 5, gültiger Bereich: 0-0xFFFFFFFF.

</dd> <dt>

**TcpNumConnections**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| TcpNumConnections")
</dt> </dl>

Maximale Anzahl von Verbindungen, die von TCP gleichzeitig geöffnet werden können. Standard: 0xfffffe, gültiger Bereich: 0-0xfffffe.

</dd> <dt>

**TcpUseRFC1122UrgentPointer**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| TcpUseRFC1122UrgentPointer")
</dt> </dl>

**True** gibt an, dass TCP die Spezifikation RFC 1122 für dringende Daten verwendet. Der Standardwert **false** gibt an, dass TCP den von den von Berkeley Software Design (BSD) abgeleiteten Systemen verwendeten Modus verwendet. Die beiden Mechanismen interpretieren den dringenden Zeiger anders und sind nicht interoperabel. Der Standardwert ist **FALSE**.

</dd> <dt>

**TcpWindowSize**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| TcpWindowSize"), [**Einheiten**](../wmisdk/standard-qualifiers.md) ("Bytes")
</dt> </dl>

Maximale TCP-Empfangs Fenstergröße, die vom System bereitgestellt wird. Das Empfangs Fenster gibt die Anzahl der Bytes an, die ein Absender übertragen kann, ohne eine Bestätigung zu empfangen. Im allgemeinen verbessern größere empfangende Fenster die Leistung bei Netzwerken mit hoher Verzögerung und hoher Bandbreite. Aus Effizienzgründen sollte das empfangende Fenster ein gleich Vielfaches der maximalen TCP-Segment Größe (MSS) sein. Standardwert: viermal die maximale TCP-Datengröße oder ein gleichmäßiges Vielfaches der TCP-Datengröße, das auf das nächste Vielfache von 8192 aufgerundet wird. Ethernet-Netzwerke werden standardmäßig auf 8760 eingestellt. Gültiger Bereich: 0-65535.

> [!Note]  
> Windows Vista: Diese Eigenschaft greift `"CurrentControlSet\\Services\\Tcpip\\Parameters|TcpWindowSize"` auf den Registrierungs Eintrag zu, der nicht in der aktuellen Implementierung des Betriebssystems verwendet wird.

 

</dd> <dt>

**WINSEnableLMHostsLookup**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| enablelmhosts")
</dt> </dl>

**True** gibt an, dass lokale Suchdateien verwendet werden. Suchdateien enthalten eine Zuordnung von IP-Adressen zu Hostnamen. Wenn Sie auf dem lokalen System vorhanden sind, werden Sie in% SystemRoot% \\ system32 \\ Drivers \\ usw. gefunden.

</dd> <dt>

**WINSHostLookupFile**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| System Information Functions \| [**GetSystemDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya) \| \\ \\ Drivers \\ \\ usw \\ \\ Lmhosts")
</dt> </dl>

Pfad zu einer WINS-Suche-Datei auf dem lokalen System. Diese Datei enthält eine Zuordnung von IP-Adressen zu Hostnamen. Wenn die in dieser Eigenschaft angegebene Datei gefunden wird, wird Sie in den Ordner% systemroot% \\ system32 \\ Drivers \\ usw. des lokalen Systems kopiert. Nur gültig, wenn die **WINSEnableLMHostsLookup** -Eigenschaft auf **true** festgelegt ist.

</dd> <dt>

**WINSPrimaryServer**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Input and Output Functions \| DeviceIoControl")
</dt> </dl>

Die IP-Adresse für den primären WINS-Server.

</dd> <dt>

**WINSScopeID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services \\ \\ tcpip \\ \\ Parameters \| ScopeId")
</dt> </dl>

Der am Ende des NetBIOS-Namens angefügte Wert, der eine Gruppe von Computersystemen isoliert, die miteinander kommunizieren. Sie wird für alle NetBIOS-Transaktionen über die TCP/IP-Kommunikation von diesem Computersystem verwendet. Computer, die mit identischen Bereichs Bezeichners konfiguriert sind, können mit diesem Computer kommunizieren. TCP/IP-Clients mit unterschiedlichen Bereichs Bezeichnern ignorieren Pakete von Computern mit diesem Bereichs Bezeichner. Nur gültig, wenn die [**EnableWINS**](enablewins-method-in-class-win32-networkadapterconfiguration.md) -Methode erfolgreich ausgeführt wird.

</dd> <dt>

**WINSSecondaryServer**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Input and Output Functions \| DeviceIoControl")
</dt> </dl>

Die IP-Adresse für den sekundären WINS-Server.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **Win32- \_ networkadapterconfiguration** -Klasse wird von der [**CIM- \_ Einstellung**](cim-setting.md)abgeleitet.

## <a name="examples"></a>Beispiele

Das Codebeispiel für den [WMI-Informations](https://Gallery.TechNet.Microsoft.Com/e493376c-1286-456b-bd4b-4ac3b0e9bb45) Abruf im VBScript-Code in der TechNet Gallery verwendet die **Win32 \_ networkadapterconfiguration** -Klasse, um Informationen zur Netzwerkkonfiguration von einer Reihe von Remote Computern abzurufen.

Das PowerShell [-Beispiel Get-ComputerInfo-Query Computer Info from Local/Remote Computers-(WMI)](https://Gallery.TechNet.Microsoft.Com/Get-ComputerInfo-Query-23dd6042) in der TechNet Gallery verwendet eine Reihe von Aufrufen von Hardware und Software, einschließlich **Win32 \_ networkadapterconfiguration**, um Informationen über ein lokales oder Remote System anzuzeigen.

Der folgende PowerShell-Code Ruft die Konfigurationseinstellungen für den Microsoft istap-Adapter ab.


```PowerShell
$IstapAdapterConfig = Get-WmiObject Win32_NetworkAdapterConfiguration | Where-Object {$_.Description -eq "Microsoft ISATAP Adapter"}
$IstapAdapterConfig
```



Das folgende C \# -Beispiel ruft die Beschreibung und die Indexnummer aller Netzwerkadapter-Konfigurations Instanzen ab. Beachten Sie, dass in diesem C- \# Beispiel der [Microsoft. Management. Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) -Namespace verwendet wird, der im Allgemeinen effizienter skaliert als die WMI-Klassen des [System. Management](/dotnet/api/system.management) -Namespace.


```CSharp
using Microsoft.Management.Infrastructure;
...
static void QueryInstanceFunc()
{
   CimSession session = CimSession.Create("localHost");
   IEnumerable<CimInstance> queryInstance = session.QueryInstances(@"root\cimv2", "WQL", "SELECT * FROM Win32_NetworkAdapterConfiguration");

   foreach (CimInstance cimObj in queryInstance)
   {
      Console.WriteLine(cimObj.CimInstanceProperties["Index"].ToString());
      Console.WriteLine(cimObj.CimInstanceProperties["Description"].ToString());
      Console.WriteLine();
   }

Console.ReadLine();
}
```



Das folgende C \# -Beispiel ruft die Beschreibung und die Indexnummer aller Netzwerkadapter-Konfigurations Instanzen ab. Beachten Sie, dass in diesem C- \# Beispiel der ursprüngliche [System. Management](/dotnet/api/system.management) -Namespace verwendet wird, der von [Microsoft. Management. Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85))ersetzt wurde.


```CSharp
using System.Management;
...
static void oldSchoolQueryInstanceFunc()
{

   ObjectQuery query = new ObjectQuery("SELECT * FROM Win32_NetworkAdapterConfiguration");
   ManagementObjectSearcher searcher = new ManagementObjectSearcher(query);

   ManagementObjectCollection queryCollection = searcher.Get();
   foreach (ManagementObject m in queryCollection)
   {
      Console.WriteLine("Index : {0}", m["Index"]);
      Console.WriteLine("Description : {0}", m["Description"]);
      Console.WriteLine();
   }
   Console.ReadLine();
}
```



Im folgenden Beispiel werden Informationen aus der **Win32 \_ networkadapterconfiguration** -Klasse abgerufen.


```VB
on error resume next


PrintAll_NICAdapter_information()

'PrintOnlyEnabled_NICAdapter_information()


Function PrintAll_NICAdapter_information()


    strComputer = "."

    Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2")


    Set colItems = objWMIService.ExecQuery("SELECT * FROM Win32_NetworkAdapterConfiguration",,48)


    i = 0

    For Each objItem in colItems

        i = i + 1

        Wscript.Echo "-----------------------------------"

        Wscript.Echo "Win32_NetworkAdapterConfiguration instance: " & i

        Wscript.Echo "-----------------------------------"

        

        strDefaultIPGateway = GetMultiString_FromArray(objitem.DefaultIPGateway, ", ")

        Wscript.Echo "MACAddress                  : " & vbtab & objItem.MACAddress
        Wscript.Echo "Description                 : " & vbtab & objItem.Description
        Wscript.Echo "DHCPEnabled                 : " & vbtab & objItem.DHCPEnabled

        strIPAddress=GetMultiString_FromArray(objitem.IPAddress, ", ")

        Wscript.Echo "IPAddress                   : " & vbtab & strIPAddress

        strIPSubnet = GetMultiString_FromArray(objitem.IPSubnet, ", ")

        Wscript.Echo "IPSubnet                    : " & vbtab & strIPSubnet
        Wscript.Echo "IPConnectionMetric          : " & vbtab & objItem.IPConnectionMetric
        Wscript.Echo "DHCPLeaseExpires            : " & vbtab & objItem.DHCPLeaseExpires
        Wscript.Echo "DHCPLeaseObtained           : " & vbtab & objItem.DHCPLeaseObtained
        Wscript.Echo "DHCPServer                  : " & vbtab & objItem.DHCPServer
        Wscript.Echo "DNSDomain                   : " & vbtab & objItem.DNSDomain
        Wscript.Echo "IPEnabled                   : " & vbtab & objItem.IPEnabled
        Wscript.Echo "DefaultIPGateway            : " & vbtab & strDefaultIPGateway
        Wscript.Echo "GatewayCostMetric           : " & vbtab & strGatewayCostMetric
        Wscript.Echo "IPFilterSecurityEnabled     : " & vbtab & objItem.IPFilterSecurityEnabled
        Wscript.Echo "IPPortSecurityEnabled       : " & vbtab & objItem.IPPortSecurityEnabled

        strDNSDomainSuffixSearchOrder = GetMultiString_FromArray(objitem.DNSDomainSuffixSearchOrder, ", ")

        Wscript.Echo "DNSDomainSuffixSearchOrder  : " & vbtab & strDNSDomainSuffixSearchOrder
        Wscript.Echo "DNSEnabledForWINSResolution : " & vbtab & objItem.DNSEnabledForWINSResolution
        Wscript.Echo "DNSHostName                 : " & vbtab & objItem.DNSHostName

        

        strDNSServerSearchOrder = GetMultiString_FromArray(objitem.DNSServerSearchOrder, ", ")

        Wscript.Echo "DNSServerSearchOrder        : " & vbtab & strDNSServerSearchOrder
        Wscript.Echo "DomainDNSRegistrationEnabled: " & vbtab & objItem.DomainDNSRegistrationEnabled
        Wscript.Echo "ForwardBufferMemory         : " & vbtab & objItem.ForwardBufferMemory
        Wscript.Echo "FullDNSRegistrationEnabled  : " & vbtab & objItem.FullDNSRegistrationEnabled

        strGatewayCostMetric = GetMultiString_FromArray(objitem.GatewayCostMetric, ", ")

        Wscript.Echo "IGMPLevel                   : " & vbtab & objItem.IGMPLevel
        Wscript.Echo "Index                       : " & vbtab & objItem.Index

        strIPSecPermitIPProtocols = GetMultiString_FromArray(objitem.IPSecPermitIPProtocols, ", ")

        Wscript.Echo "IPSecPermitIPProtocols      : " & vbtab & strIPSecPermitIPProtocols


        strIPSecPermitTCPPorts =GetMultiString_FromArray(objitem.IPSecPermitTCPPorts, ", ")

        Wscript.Echo "IPSecPermitTCPPorts         : " & vbtab & strIPSecPermitTCPPorts


        strIPSecPermitUDPPorts = GetMultiString_FromArray(objitem.IPSecPermitUDPPorts, ", ")

        Wscript.Echo "IPSecPermitUDPPorts         : " & vbtab & strIPSecPermitUDPPorts


        Wscript.Echo "IPUseZeroBroadcast          : " & vbtab & objItem.IPUseZeroBroadcast
        Wscript.Echo "IPXAddress                  : " & vbtab & objItem.IPXAddress
        Wscript.Echo "IPXEnabled                  : " & vbtab & objItem.IPXEnabled

        strIPXFrameType=GetMultiString_FromArray(objitem.IPXFrameType, ", ")

        Wscript.Echo "IPXFrameType                : " & vbtab & strIPXFrameType


        strIPXNetworkNumber=GetMultiString_FromArray(objitem.IPXNetworkNumber, ", ")

        Wscript.Echo "IPXNetworkNumber            : " & vbtab & strIPXNetworkNumber
        Wscript.Echo "IPXVirtualNetNumber         : " & vbtab & objItem.IPXVirtualNetNumber
        Wscript.Echo "KeepAliveInterval           : " & vbtab & objItem.KeepAliveInterval

        Wscript.Echo "KeepAliveTime               : " & vbtab & objItem.KeepAliveTime
        Wscript.Echo "MTU                         : " & vbtab & objItem.MTU
        Wscript.Echo "NumForwardPackets           : " & vbtab & objItem.NumForwardPackets
        Wscript.Echo "PMTUBHDetectEnabled         : " & vbtab & objItem.PMTUBHDetectEnabled
        Wscript.Echo "PMTUDiscoveryEnabled        : " & vbtab & objItem.PMTUDiscoveryEnabled
        Wscript.Echo "ServiceName                 : " & vbtab & objItem.ServiceName
        Wscript.Echo "SettingID                   : " & vbtab & objItem.SettingID
        Wscript.Echo "TcpipNetbiosOptions         : " & vbtab & objItem.TcpipNetbiosOptions
        Wscript.Echo "TcpMaxConnectRetransmissions: " & vbtab & objItem.TcpMaxConnectRetransmissions
        Wscript.Echo "TcpMaxDataRetransmissions   : " & vbtab & objItem.TcpMaxDataRetransmissions
        Wscript.Echo "TcpNumConnections           : " & vbtab & objItem.TcpNumConnections
        Wscript.Echo "TcpUseRFC1122UrgentPointer  : " & vbtab & objItem.TcpUseRFC1122UrgentPointer
        Wscript.Echo "TcpWindowSize               : " & vbtab & objItem.TcpWindowSize
        Wscript.Echo "WINSEnableLMHostsLookup     : " & vbtab & objItem.WINSEnableLMHostsLookup
        Wscript.Echo "WINSHostLookupFile          : " & vbtab & objItem.WINSHostLookupFile
        Wscript.Echo "WINSPrimaryServer           : " & vbtab & objItem.WINSPrimaryServer
        Wscript.Echo "WINSScopeID                 : " & vbtab & objItem.WINSScopeID
        Wscript.Echo "WINSSecondaryServer         : " & vbtab & objItem.WINSSecondaryServer
        Wscript.Echo "ArpAlwaysSourceRoute        : " & vbtab & objItem.ArpAlwaysSourceRoute
        Wscript.Echo "ArpUseEtherSNAP             : " & vbtab & objItem.ArpUseEtherSNAP
        Wscript.Echo "DatabasePath                : " & vbtab & objItem.DatabasePath
        Wscript.Echo "DeadGWDetectEnabled         : " & vbtab & objItem.DeadGWDetectEnabled

        Wscript.Echo "DefaultTOS                  : " & vbtab & objItem.DefaultTOS
        Wscript.Echo "DefaultTTL                  : " & vbtab & objItem.DefaultTTL

        

    Next

End Function ' Function PrintAll_NICAdapter_information()


' Script to get comprehensive nic info

sub appendCollection(msg, colctn, nm)

    i=0
    for each t in colctn
        msg = msg & "nic." & nm & "["&i&"]: " & t & vbCRLF
        i = i + 1
    next
end sub


Function PrintOnlyEnabled_NICAdapter_information()

    strComputer = "."

    Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
    Set colNicConfigs = objWMIService.ExecQuery ("SELECT * FROM Win32_NetworkAdapterConfiguration WHERE IPEnabled = True")


    for each nic in colNicConfigs

        msg = "nic.ArpAlwaysSourceRoute: " & nic.ArpAlwaysSourceRoute & vbCRLF _
        & "nic.ArpUseEtherSNAP: " & nic.ArpUseEtherSNAP & vbCRLF _
        & "nic.Caption: " & nic.Caption & vbCRLF _
        & "nic.DatabasePath: " & nic.DatabasePath & vbCRLF _
        & "nic.DeadGWDetectEnabled: " & nic.DeadGWDetectEnabled & vbCRLF _
        & "nic.DefaultTOS: " & nic.DefaultTOS & vbCRLF _
        & "nic.DefaultTTL: " & nic.DefaultTTL & vbCRLF _
        & "nic.Description: " & nic.Description & vbCRLF _
        & "nic.DHCPEnabled: " & nic.DHCPEnabled & vbCRLF _
        & "nic.DHCPLeaseExpires: " & nic.DHCPLeaseExpires & vbCRLF _
        & "nic.DHCPLeaseObtained: " & nic.DHCPLeaseObtained & vbCRLF _
        & "nic.DHCPServer: " & nic.DHCPServer & vbCRLF _
        & "nic.DNSDomain: " & nic.DNSDomain & vbCRLF _
        & "nic.DNSEnabledForWINSResolution: " & nic.DNSEnabledForWINSResolution & vbCRLF _
        & "nic.DNSHostName: " & nic.DNSHostName & vbCRLF _
        & "nic.DomainDNSRegistrationEnabled: " & nic.DomainDNSRegistrationEnabled & vbCRLF _
        & "nic.DNSDomainSuffixSearchOrder: " & nic.DNSDomainSuffixSearchOrder & vbCRLF _
        & "nic.ForwardBufferMemory: " & nic.ForwardBufferMemory & vbCRLF _
        & "nic.FullDNSRegistrationEnabled: " & nic.FullDNSRegistrationEnabled & vbCRLF _
        & "nic.IGMPLevel: " & nic.IGMPLevel & vbCRLF _
        & "nic.Index: " & nic.Index & vbCRLF _
        & "nic.IPConnectionMetric: " & nic.IPConnectionMetric & vbCRLF _
        & "nic.IPEnabled: " & nic.IPEnabled & vbCRLF _
        & "nic.IPFilterSecurityEnabled: " & nic.IPFilterSecurityEnabled & vbCRLF _
        & "nic.IPPortSecurityEnabled: " & nic.IPPortSecurityEnabled & vbCRLF _
        & "nic.IPUseZeroBroadcast: " & nic.IPUseZeroBroadcast & vbCRLF _
        & "nic.IPXAddress: " & nic.IPXAddress & vbCRLF _
        & "nic.IPXEnabled: " & nic.IPXEnabled & vbCRLF _
        & "nic.IPXFrameType: " & nic.IPXFrameType & vbCRLF _
        & "nic.IPXMediaType: " & nic.IPXMediaType & vbCRLF _
        & "nic.IPXNetworkNumber: " & nic.IPXNetworkNumber & vbCRLF _
        & "nic.IPXVirtualNetNumber: " & nic.IPXVirtualNetNumber & vbCRLF _
        & "nic.KeepAliveInterval: " & nic.KeepAliveInterval & vbCRLF _
        & "nic.KeepAliveTime: " & nic.KeepAliveTime & vbCRLF _
        & "nic.MACAddress: " & nic.MACAddress & vbCRLF _
        & "nic.MTU: " & nic.MTU & vbCRLF _
        & "nic.NumForwardPackets: " & nic.NumForwardPackets & vbCRLF _
        & "nic.PMTUBHDetectEnabled: " & nic.PMTUBHDetectEnabled & vbCRLF _
        & "nic.PMTUDiscoveryEnabled: " & nic.PMTUDiscoveryEnabled & vbCRLF _
        & "nic.ServiceName: " & nic.ServiceName & vbCRLF _
        & "nic.SettingID: " & nic.SettingID & vbCRLF _
        & "nic.TcpipNetbiosOptions: " & nic.TcpipNetbiosOptions & vbCRLF _
        & "nic.TcpMaxConnectRetransmissions: " & nic.TcpMaxConnectRetransmissions & vbCRLF _
        & "nic.TcpMaxDataRetransmissions: " & nic.TcpMaxDataRetransmissions & vbCRLF _
        & "nic.TcpNumConnections: " & nic.TcpNumConnections & vbCRLF _
        & "nic.TcpUseRFC1122UrgentPointer: " & nic.TcpUseRFC1122UrgentPointer & vbCRLF _
        & "nic.TcpWindowSize: " & nic.TcpWindowSize & vbCRLF _
        & "nic.WINSEnableLMHostsLookup: " & nic.WINSEnableLMHostsLookup & vbCRLF _
        & "nic.WINSHostLookupFile: " & nic.WINSHostLookupFile & vbCRLF _
        & "nic.WINSPrimaryServer: " & nic.WINSPrimaryServer & vbCRLF _
        & "nic.WINSScopeID: " & nic.WINSScopeID & vbCRLF _
        & "nic.WINSSecondaryServer: " & nic.WINSSecondaryServer & vbCRLF _
        '& "nic.InterfaceIndex: " & "|"&nic.InterfaceIndex & vbCRLF _


        appendCollection msg, nic.DefaultIPGateway, "DefaultIPGateway"
        appendCollection msg, nic.DNSServerSearchOrder, "DNSServerSearchOrder"
        appendCollection msg, nic.GatewayCostMetric, "GatewayCostMetric"
        appendCollection msg, nic.IPAddress, "IPAddress"
        appendCollection msg, nic.IPSecPermitIPProtocols, "IPSecPermitIPProtocols"
        appendCollection msg, nic.IPSecPermitTCPPorts, "IPSecPermitTCPPorts"
        appendCollection msg, nic.IPSecPermitUDPPorts, "IPSecPermitUDPPorts"
        appendCollection msg, nic.IPSubnet, "IPSubnet"


        WScript.Echo msg

    next


    'Vista only code???

    'Set colAdapters = objWMIService.Execquery ("SELECT * FROM Win32_NetworkAdapter WHERE NetEnabled = True")

    'For Each nic in colAdapters

    ' msg = "nic.DeviceId: " & nic.DeviceId & vbCRLF _

    ' & "nic.Name: " & nic.Name & vbCRLF _

    '

    'Next

End Function 'Function PrintOnlyEnabled_NICAdapter_information()

Function GetMultiString_FromArray( ArrayString, Seprator)

    If IsNull ( ArrayString ) Then

        StrMultiArray = ArrayString

    else

        StrMultiArray = Join( ArrayString, Seprator )

   end if

   GetMultiString_FromArray = StrMultiArray

End Function
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM- \_ Einstellung**](cim-setting.md)
</dt> <dt>

[Computer System-Hardware Klassen](computer-system-hardware-classes.md)
</dt> <dt>

[WMI-Tasks: Netzwerk](../wmisdk/wmi-tasks--networking.md)
</dt> <dt>

[WMI-Tasks: Konten und Domänen](../wmisdk/wmi-tasks--accounts-and-domains.md)
</dt> <dt>

[IPv6-und IPv4-Unterstützung in WMI](../wmisdk/ipv6-and-ipv4-support-in-wmi.md)
</dt> </dl>

 

 
