---
description: Stellt die Attribute und Verhaltensweisen eines Netzwerkadapters dar. Diese Klasse enthält zusätzliche Eigenschaften und Methoden, die die Verwaltung des TCP/IP-Protokolls unterstützen, das vom Netzwerkadapter unabhängig ist.
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
ms.openlocfilehash: e93ae76ae3c4880c7ad041e6e90d39f1b22820d3
ms.sourcegitcommit: 88049609e29f91a42442235885abf56f598b06b3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/19/2021
ms.locfileid: "110153573"
---
# <a name="win32_networkadapterconfiguration-class"></a>Win32 \_ NetworkAdapterConfiguration-Klasse

Die [WMI-Klasse](../wmisdk/retrieving-a-class.md) **Win32 \_ NetworkAdapterConfiguration** stellt die Attribute und das Verhalten eines Netzwerkadapters dar. Diese Klasse enthält zusätzliche Eigenschaften und Methoden, die die Verwaltung des TCP/IP-Protokolls unterstützen, das vom Netzwerkadapter unabhängig ist.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

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

Die **Win32 \_ NetworkAdapterConfiguration-Klasse** verfügt über folgende Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **Win32 \_ NetworkAdapterConfiguration-Klasse** verfügt über diese Methoden.



| Methode                                                                                                                       | Beschreibung                                                                                                                                           |
|:-----------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DisableIPSec**](disableipsec-method-in-class-win32-networkadapterconfiguration.md)                                       | Deaktiviert IPsec auf diesem TCP/IP-fähigen Netzwerkadapter.<br/>                                                                                     |
| [**EnableDHCP**](enabledhcp-method-in-class-win32-networkadapterconfiguration.md)                                           | Aktiviert das Dynamic Host Configuration Protocol (DHCP) für den Dienst mit diesem Netzwerkadapter.<br/>                                              |
| [**EnableDNS**](enabledns-method-in-class-win32-networkadapterconfiguration.md)                                             | Aktiviert die Domain Name System (DNS) für den Dienst auf diesem TCP/IP-gebundenen Netzwerkadapter.<br/>                                                     |
| [**EnableIPFilterSec**](enableipfiltersec-method-in-class-win32-networkadapterconfiguration.md)                             | Aktiviert IPsec global für alle IP-gebundenen Netzwerkadapter.<br/>                                                                               |
| [**EnableIPSec**](enableipsec-method-in-class-win32-networkadapterconfiguration.md)                                         | Aktiviert IPsec auf diesem spezifischen TCP/IP-fähigen Netzwerkadapter.<br/>                                                                             |
| [**EnableStatic**](enablestatic-method-in-class-win32-networkadapterconfiguration.md)                                       | Aktiviert die statische TCP/IP-Adressierung für den Zielnetzwerkadapter.<br/>                                                                           |
| [**EnableWINS**](enablewins-method-in-class-win32-networkadapterconfiguration.md)                                           | Aktiviert TCP/IP-spezifische WINS-Einstellungen, jedoch unabhängig vom Netzwerkadapter.<br/>                                                          |
| [**ReleaseDHCPLease**](releasedhcplease-method-in-class-win32-networkadapterconfiguration.md)                               | Gibt die IP-Adresse frei, die an einen bestimmten DHCP-fähigen Netzwerkadapter gebunden ist.<br/>                                                                  |
| [**ReleaseDHCPLeaseAll**](releasedhcpleaseall-method-in-class-win32-networkadapterconfiguration.md)                         | Gibt die IP-Adressen frei, die an alle DHCP-fähigen Netzwerkadapter gebunden sind.<br/>                                                                      |
| [**RenewDHCPLease**](renewdhcplease-method-in-class-win32-networkadapterconfiguration.md)                                   | Erneuert die IP-Adresse auf bestimmten DHCP-fähigen Netzwerkadaptern.<br/>                                                                           |
| [**RenewDHCPLeaseAll**](renewdhcpleaseall-method-in-class-win32-networkadapterconfiguration.md)                             | Erneuert die IP-Adressen auf allen DHCP-fähigen Netzwerkadaptern.<br/>                                                                              |
| [**SetArpAlwaysSourceRoute**](setarpalwayssourceroute-method-in-class-win32-networkadapterconfiguration.md)                 | Legt die Übertragung von ARP-Abfragen über TCP/IP fest.<br/>                                                                                        |
| [**SetArpUseEtherSNAP**](setarpuseethersnap-method-in-class-win32-networkadapterconfiguration.md)                           | Ermöglicht Ethernet-Paketen die Verwendung der SNAP-Codierung 802.3.<br/>                                                                                       |
| [**SetDatabasePath**](setdatabasepath-method-in-class-win32-networkadapterconfiguration.md)                                 | Legt den Pfad zu den standardmäßigen Internetdatenbankdateien (HOSTS, LMHOSTS, NETWORKS und PROTOCOLS) fest.<br/>                                           |
| [**SetDeadGWDetect**](setdeadgwdetect-method-in-class-win32-networkadapterconfiguration.md)                                 | Aktiviert die Erkennung von toten Gateways.<br/>                                                                                                            |
| [**SetDefaultTOS**](setdefaulttos-method-in-class-win32-networkadapterconfiguration.md)                                     | Veraltet. Diese Methode legt den Standardwert für den Typ des Diensts (TOS) im Header der ausgehenden IP-Pakete fest.<br/>                                   |
| [**SetDefaultTTL**](setdefaultttl-method-in-class-win32-networkadapterconfiguration.md)                                     | Legt den Standardwert für die Gültigkeitsdauer (Time to Live, TTL) im Header ausgehender IP-Pakete fest.<br/>                                                            |
| [**SetDNSDomain**](setdnsdomain-method-in-class-win32-networkadapterconfiguration.md)                                       | Legt die DNS-Domäne fest.<br/>                                                                                                                       |
| [**SetDNSServerSearchOrder**](setdnsserversearchorder-method-in-class-win32-networkadapterconfiguration.md)                 | Legt die Serversuchreihenfolge als Array von Elementen fest.<br/>                                                                                      |
| [**SetDNSSuffixSearchOrder**](setdnssuffixsearchorder-method-in-class-win32-networkadapterconfiguration.md)                 | Legt die Suffixsuchreihenfolge als Array von Elementen fest.<br/>                                                                                      |
| [**SetDynamicDNSRegistration**](setdynamicdnsregistration-method-in-class-win32-networkadapterconfiguration.md)             | Gibt die dynamische DNS-Registrierung von IP-Adressen für diesen IP-gebundenen Adapter an.<br/>                                                              |
| [**SetForwardBufferMemory**](setforwardbuffermemory-method-in-class-win32-networkadapterconfiguration.md)                   | Gibt an, wie viel Speicher-IP zum Speichern von Paketdaten in der Routerpaketwarteschlange zuweist.<br/>                                                    |
| [**SetGateways**](setgateways-method-in-class-win32-networkadapterconfiguration.md)                                         | Gibt eine Liste von Gateways für das Routing von Paketen an, die für ein anderes Subnetz als das subnetz bestimmt sind, mit dem dieser Adapter verbunden ist.<br/>                |
| [**SetIGMPLevel**](setigmplevel-method-in-class-win32-networkadapterconfiguration.md)                                       | Legt den Umfang fest, in dem das System IP-Multicasting unterstützt und am Internetgruppenverwaltungsprotokoll teilnimmt.<br/>                   |
| [**SetIPConnectionMetric**](setipconnectionmetric-method-in-class-win32-networkadapterconfiguration.md)                     | Legt die Routingmetrik fest, die diesem IP-gebundenen Adapter zugeordnet ist.<br/>                                                                             |
| [**SetIPUseZeroBroadcast**](setipusezerobroadcast-method-in-class-win32-networkadapterconfiguration.md)                     | Legt die IP-0-Broadcastverwendung fest.<br/>                                                                                                              |
| [**SetIPXFrameTypeNetworkPairs**](win32-networkadapterconfiguration-setipxframetypenetworkpairs.md)                         | Legt IPX-Netzwerknummer-/Framepaare (Internetworking Packet Exchange) für diesen Netzwerkadapter fest.<br/>                                            |
| [**SetIPXVirtualNetworkNumber**](win32-networkadapterconfiguration-setipxvirtualnetworknumber.md)                           | Legt die IPX-Netzwerknummer (Internetworking Packet Exchange) auf dem Zielcomputersystem fest.<br/>                                       |
| [**SetKeepAliveInterval**](setkeepaliveinterval-method-in-class-win32-networkadapterconfiguration.md)                       | Legt das Intervall fest, das Keep Alive-Neuübertragungen trennt, bis eine Antwort empfangen wird.<br/>                                                      |
| [**SetKeepAliveTime**](setkeepalivetime-method-in-class-win32-networkadapterconfiguration.md)                               | Legt fest, wie oft TCP versucht, durch Senden eines Keep Alive-Pakets zu überprüfen, ob eine Verbindung im Leerlauf weiterhin verfügbar ist.<br/>                           |
| [**SetMTU**](setmtu-method-in-class-win32-networkadapterconfiguration.md)                                                   | Legt die standardmäßige maximale Übertragungseinheit (Maximum Transmission Unit, MTU) für eine Netzwerkschnittstelle fest.<br/> Diese Methode wird nicht unterstützt.<br/>                         |
| [**SetNumForwardPackets**](setnumforwardpackets-method-in-class-win32-networkadapterconfiguration.md)                       | Legt die Anzahl der IP-Paketheader fest, die der Routerpaketwarteschlange zugeordnet sind.<br/>                                                                |
| [**SetPMTUBHDetect**](setpmtubhdetect-method-in-class-win32-networkadapterconfiguration.md)                                 | Ermöglicht die Erkennung von Black Hole-Routern.<br/>                                                                                                   |
| [**SetPMTUDiscovery**](setpmtudiscovery-method-in-class-win32-networkadapterconfiguration.md)                               | Aktiviert die Ermittlung der maximalen Übertragungseinheit (Maximum Transmission Unit, MTU).<br/>                                                                                         |
| [**SetTcpipNetbios**](settcpipnetbios-method-in-class-win32-networkadapterconfiguration.md)                                 | Legt den Standardvorgang von NetBIOS über TCP/IP fest.<br/>                                                                                         |
| [**SetTcpMaxConnectRetransmissions**](settcpmaxconnectretransmissions-method-in-class-win32-networkadapterconfiguration.md) | Legt die Anzahl der Versuche fest, mit der TCP eine Verbindungsanforderung vor dem Abbruch erneut überträgt.<br/>                                                         |
| [**SetTcpMaxDataRetransmissions**](settcpmaxdataretransmissions-method-in-class-win32-networkadapterconfiguration.md)       | Legt fest, wie oft TCP ein einzelnes Datensegment erneut überträgt, bevor die Verbindung abgebrochen wird.<br/>                                    |
| [**SetTcpNumConnections**](settcpnumconnections-method-in-class-win32-networkadapterconfiguration.md)                       | Legt die maximale Anzahl von Verbindungen fest, die TCP möglicherweise gleichzeitig geöffnet hat.<br/>                                                              |
| [**SetTcpUseRFC1122RolentPointer**](settcpuserfc1122urgentpointer-method-in-class-win32-networkadapterconfiguration.md)     | Gibt an, ob TCP die RFC 1122-Spezifikation für dringende Daten oder den Modus verwendet, der von BSD-abgeleiteten Systemen (California Software Design) verwendet wird.<br/> |
| [**SetTcpWindowSize**](settcpwindowsize-method-in-class-win32-networkadapterconfiguration.md)                               | Legt die maximale TCP-Empfangsfenstergröße fest, die vom System angeboten wird.<br/>                                                                            |
| [**SetWINSServer**](setwinsserver-method-in-class-win32-networkadapterconfiguration.md)                                     | Legt die primären und sekundären WINDOWS-WINS-Server (Internet Naming Service) auf diesem TCP/IP-gebundenen Netzwerkadapter fest.<br/>                        |



 

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ NetworkAdapterConfiguration-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**ArpAlwaysSourceRoute**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| ArpAlwaysSourceRoute")
</dt> </dl>

True gibt an, dass TCP/IP ARP-Abfragen (Address Resolution Protocol) mit aktiviertem Quellrouting in TokenRing-Netzwerken überträgt. Standardmäßig (FALSE) fragt ARP zuerst ohne Quellrouting ab und dann erneut, wenn das Quellrouting aktiviert ist, wenn keine Antwort empfangen wird. Das Quellrouting ermöglicht das Routing von Netzwerkpaketen über verschiedene Netzwerktypen hinweg.

</dd> <dt>

**ArpUseEtherSNAP**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| ArpUseEtherSNAP")
</dt> </dl>

True **gibt an,** dass Ethernet-Pakete der IEEE 802.3-Codierung Sub-Network Access Protocol (SNAP) folgen. Durch Festlegen dieses Parameters auf 1 wird die Übertragung von Ethernet-Paketen durch TCP/IP mithilfe der SNAP-Codierung 802.3 erzwingt. Standardmäßig (FALSE) überträgt der Stapel Pakete im DIX-Ethernet-Format.

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Kurze Textbeschreibung des aktuellen Objekts.

Diese Eigenschaft wird von der [**CIM-Einstellung \_ geerbt.**](cim-setting.md)

</dd> <dt>

**Databasepath**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| DatabasePath")
</dt> </dl>

Gültiger Windows-Dateipfad zu Standardmäßigen Internetdatenbankdateien (HOSTS, LMHOSTS, NETWORKS und PROTOCOLS). Der Dateipfad wird von der Windows Sockets-Schnittstelle verwendet.

</dd> <dt>

**DeadGWDetectEnabled**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| EnableDeadGWDetect")
</dt> </dl>

True **gibt an,** dass die Erkennung von toten Gateways auftritt. Wenn dieses Feature aktiviert ist, fordert TCP (Transmission Control Protocol) das Internetprotokoll (IP) auf, zu einem Sicherungsgateway zu wechseln, wenn es ein Segment mehrmals erneut überträgt, ohne eine Antwort zu erhalten.

</dd> <dt>

**DefaultIPGateway**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services Parameters \| \| DefaultGateway")
</dt> </dl>

Array von IP-Adressen von Standardgateways, die vom Computersystem verwendet werden.

Beispiel: "192.168.12.1 192.168.46.1"

</dd> <dt>

**DefaultTOS**
</dt> <dd> <dl> <dt>

Datentyp: **uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| DefaultTOS")
</dt> </dl>

Der Im Header ausgehender IP-Pakete festgelegte Standardwert für den Diensttyp (Type Of Service, TOS). Request for Comments (RFC) 791 definiert die Werte. Standardwert: 0 (null), Gültiger Bereich: 0 bis 255.

</dd> <dt>

**DefaultTTL**
</dt> <dd> <dl> <dt>

Datentyp: **uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| DefaultTTL")
</dt> </dl>

Der Standardwert für die Gültigkeitsdauer (Time To Live, TTL), der im Header ausgehender IP-Pakete festgelegt ist. Die Gültigkeitsdauer gibt die Anzahl der Router an, die ein IP-Paket passieren kann, um das Ziel zu erreichen, bevor es verworfen wird. Jeder Router dekrementiert die TTL-Anzahl eines Pakets um eins, während es durchläuft, und verwirft die Pakete – wenn die Gültigkeitsdauer 0 (null) ist. Standardwert: 32, gültiger Bereich: 1 bis 255.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **String**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Textbeschreibung des aktuellen -Objekts.

Diese Eigenschaft wird von [**der \_ CIM-Einstellung**](cim-setting.md)geerbt.

</dd> <dt>

**DHCPEnabled**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \| EnableDHCP")
</dt> </dl>

True gibt an, dass der DHCP-Server (Dynamic Host Configuration Protocol) dem Computersystem automatisch eine IP-Adresse zuweist, wenn eine Netzwerkverbindung hergestellt wird.

</dd> <dt>

**DHCPLeaseExpires**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \| LeaseTerminatesTime")
</dt> </dl>

Ablaufdatum und -uhrzeit für eine geleaste IP-Adresse, die dem Computer vom DHCP-Server (Dynamic Host Configuration Protocol) zugewiesen wurde.

Beispiel: 20521201000230.000000000

</dd> <dt>

**DHCPLeaseObtained**
</dt> <dd> <dl> <dt>

Datentyp: **datetime**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \| LeaseObtainedTime")
</dt> </dl>

Datum und Uhrzeit des Leases für die IP-Adresse, die dem Computer vom DHCP-Server (Dynamic Host Configuration Protocol) zugewiesen wurde.

Beispiel: 19521201000230.000000000

</dd> <dt>

**DHCPServer**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \| DhcpServer")
</dt> </dl>

IP-Adresse des DHCP-Servers (Dynamic Host Configuration Protocol).

Beispiel: "10.55.34.2"

</dd> <dt>

**DNSDomain**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| Domain")
</dt> </dl>

Organisationsname, gefolgt von einem Zeitraum und einer Erweiterung, die den Typ der Organisation angibt, z. B. "microsoft.com". Der Name kann eine beliebige Kombination aus den Buchstaben A bis Z, den Ziffern 0 bis 9 und dem Bindestrich (-) sowie dem als Trennzeichen verwendeten Zeitraum (.) sein.

Beispiel: "microsoft.com"

</dd> <dt>

**DNSDomainSuffixSearchOrder**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| SearchList")
</dt> </dl>

Array von DNS-Domänensuffixen, die während der Namensauflösung an das Ende der Hostnamen angefügt werden sollen. Beim Versuch, einen vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) aus einem reinen Hostnamen aufzulösen, fügt das System zuerst den lokalen Domänennamen an. Wenn dies nicht erfolgreich ist, verwendet das System die Domänensuffixliste, um zusätzliche FQDNs in der aufgeführten Reihenfolge zu erstellen und dns-Server für jeden abzufragen.

Beispiel: "samples.microsoft.com example.microsoft.com"

</dd> <dt>

**DNSEnabledForWINSResolution**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| EnableDNS")
</dt> </dl>

**True** gibt an, dass die Domain Name System (DNS) für die Namensauflösung über die WINS-Auflösung (Internet Naming Service) von Windows aktiviert ist. Wenn der Name nicht mit DNS aufgelöst werden kann, wird die Namensanforderung zur Auflösung an WINS weitergeleitet.

</dd> <dt>

**Dnshostname**
</dt> <dd> <dl> <dt>

Datentyp: **String**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| Hostname")
</dt> </dl>

Hostname, der verwendet wird, um den lokalen Computer für die Authentifizierung durch einige Hilfsprogramme zu identifizieren. Andere TCP/IP-basierte Hilfsprogramme können diesen Wert verwenden, um den Namen des lokalen Computers zu erhalten. Hostnamen werden auf DNS-Servern in einer Tabelle gespeichert, in der Namen IP-Adressen zur Verwendung durch DNS zugeordnet werden. Der Name kann eine beliebige Kombination aus den Buchstaben A bis Z, den Ziffern 0 bis 9 und dem Bindestrich (-) sowie dem Punktzeichen (.) sein, das als Trennzeichen verwendet wird. Standardmäßig ist dieser Wert der Name des Microsoft-Netzwerkcomputers, aber der Netzwerkadministrator kann einen anderen Hostnamen zuweisen, ohne dass sich dies auf den Computernamen auswirkt.

Beispiel: "corpdns"

</dd> <dt>

**DNSServerSearchOrder**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| NameServer")
</dt> </dl>

Array von Server-IP-Adressen, die beim Abfragen von DNS-Servern verwendet werden sollen.

</dd> <dt>

**DomainDNSRegistrationEnabled**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

True **gibt** an, dass die IP-Adressen für diese Verbindung nicht nur unter dem vollständigen DNS-Namen des Computers, sondern auch im DNS unter dem Domänennamen dieser Verbindung registriert werden. Der Domänenname dieser Verbindung wird entweder mithilfe der [**SetDNSDomain**](setdnsdomain-method-in-class-win32-networkadapterconfiguration.md)()-Methode festgelegt oder von DSCP zugewiesen. Der registrierte Name ist der Hostname des Computers, an den der Domänenname angefügt ist.

</dd> <dt>

**ForwardBufferMemory**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| ForwardBufferMemory"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")
</dt> </dl>

Durch IP zugewiesener Arbeitsspeicher zum Speichern von Paketdaten in der Routerpaketwarteschlange. Wenn dieser Pufferspeicher gefüllt ist, beginnt der Router damit, Pakete nach dem Zufallsprinzip aus seiner Warteschlange zu verwerfen. Paketwarteschlangen-Datenpuffer haben eine Länge von 256 Bytes, daher sollte der Wert dieses Parameters ein Vielfaches von 256 sein. Mehrere Puffer werden für größere Pakete miteinander verkettet. Der IP-Header für ein Paket wird separat gespeichert. Dieser Parameter wird ignoriert, und es werden keine Puffer zugeordnet, wenn der IP-Router nicht aktiviert ist. Die Puffergröße kann von der Netzwerk-MTU bis zu einem Wert reichen, der kleiner als 0xFFFFFFFF. Standardwert: 74240 (1480-Byte-Pakete, gerundet auf ein Vielfaches von 256).

</dd> <dt>

**FullDNSRegistrationEnabled**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

**True** gibt an, dass die IP-Adressen für diese Verbindung im DNS unter dem vollständigen DNS-Namen des Computers registriert werden. Der vollständige DNS-Name des Computers wird auf der Registerkarte **Netzwerkidentifikation** in der Systemanwendung in Systemsteuerung angezeigt.

</dd> <dt>

**GatewayCostMetric**
</dt> <dd> <dl> <dt>

Datentyp: **uint16-Array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Array ganzzahliger Kostenmetrikwerte (im Bereich von 1 bis 9999), die zum Berechnen der schnellsten, zuverlässigsten oder ressourcenintensivsten Routen verwendet werden sollen. Dieses Argument weist eine 1:1-Entsprechung mit der **DefaultIPGateway-Eigenschaft** auf.

</dd> <dt>

**IGMPLevel**
</dt> <dd> <dl> <dt>

Datentyp: **uint8**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| IGMPLevel")
</dt> </dl>

Umfang, in dem das System IP-Multicast unterstützt und am Internet Group Management Protocol (IGMP) teilnimmt. Auf Ebene 0 (null) bietet das System keine Multicastunterstützung. Auf Ebene 1 kann das System nur IP-Multicastpakete senden. Auf Ebene 2 kann das System IP-Multicastpakete senden und vollständig an IGMP teilnehmen, um Multicastpakete zu empfangen.

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

IP und IGMP Multicast (Standard)

</dd> </dl>

</dd> <dt>

**Index**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**key**](../wmisdk/key-qualifier.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Control Class \\ \\ \\ \\ {4D36E972-E325-11CE-BFC1-08002BE10318}")
</dt> </dl>

Indexnummer der Konfiguration des Windows-Netzwerkadapters. Die Indexnummer wird verwendet, wenn mehrere Konfigurationen verfügbar sind.

</dd> <dt>

**InterfaceIndex**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Indexwert, der eine lokale Netzwerkschnittstelle eindeutig identifiziert. Der Wert in dieser Eigenschaft entspricht dem Wert in der **InterfaceIndex-Eigenschaft** in der Instanz von [**Win32 \_ IP4RouteTable,**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetable) der die Netzwerkschnittstelle in der Routentabelle darstellt.

</dd> <dt>

**IPAddress**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services Parameters \| \\ \\ Tcpip \| IPAddress")
</dt> </dl>

Array aller IP-Adressen, die dem aktuellen Netzwerkadapter zugeordnet sind. Diese Eigenschaft kann entweder IPv6-Adressen oder IPv4-Adressen enthalten. Weitere Informationen finden Sie unter [IPv6- und IPv4-Unterstützung in WMI.](../wmisdk/ipv6-and-ipv4-support-in-wmi.md)

Beispiel-IPv6-Adresse: "2010:836B:4179::836B:4179"

</dd> <dt>

**IPConnectionMetric**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Kosten für die Verwendung der konfigurierten Routen für den IP-gebundenen Adapter und der gewichtete Wert für diese Routen in der IP-Routingtabelle. Wenn die IP-Routingtabelle mehrere Routen zu einem Ziel enthält, wird die Route mit der niedrigsten Metrik verwendet. Der Standardwert ist 1.

</dd> <dt>

**IPEnabled**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services Parameters \| \\ \\ Tcpip")
</dt> </dl>

True **gibt an,** dass TCP/IP gebunden und auf diesem Netzwerkadapter aktiviert ist.

</dd> <dt>

**IPFilterSecurityEnabled**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| IPFilterSecurityEnabled")
</dt> </dl>

**True** gibt an, dass die IP-Portsicherheit global für alle IP-gebundenen Netzwerkadapter aktiviert ist, und die Sicherheitswerte, die einzelnen Netzwerkadaptern zugeordnet sind, sind wirksam. Diese Eigenschaft wird in Verbindung mit **IPSecPermitTCPPorts,** **IPSecPermitUDPPorts** und **IPSecPermitIPProtocols** verwendet. **False** gibt an, dass die IP-Filtersicherheit für alle Netzwerkadapter deaktiviert ist und den ungefilterten Fluss des gesamten Port- und Protokolldatenverkehrs zulässt.

</dd> <dt>

**IPPortSecurityEnabled**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**VERALTET,**](../wmisdk/standard-wmi-qualifiers.md) [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI \| Win32 \_ NetworkAdapterConfiguration \| IPFilterSecurityEnabled")
</dt> </dl>

**True** gibt an, dass die IP-Portsicherheit global für alle IP-gebundenen Netzwerkadapter aktiviert ist. Diese Eigenschaft ist veraltet. Anstelle dieser Eigenschaft sollten Sie **IPFilterSecurityEnabled** verwenden.

</dd> <dt>

**IPSecPermitIPProtocols**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| RawIPAllowedProtocols")
</dt> </dl>

Array der Protokolle, die über die IP-Adresse ausgeführt werden dürfen. Die Liste der Protokolle wird mithilfe der [**EnableIPSec-Methode**](enableipsec-method-in-class-win32-networkadapterconfiguration.md) definiert. Die Liste ist entweder leer oder enthält numerische Werte. Der numerische Wert 0 (null) gibt an, dass die Zugriffsberechtigung für alle Protokolle erteilt wurde. Eine leere Zeichenfolge gibt an, dass keine Protokolle ausgeführt werden dürfen, wenn **IPFilterSecurityEnabled** **TRUE** ist.

</dd> <dt>

**IPSecPermitTCPPorts**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| TCPAllowedPorts")
</dt> </dl>

Array der Ports, denen die Zugriffsberechtigung für TCP erteilt wird. Die Liste der Protokolle wird mithilfe der [**EnableIPSec-Methode**](enableipsec-method-in-class-win32-networkadapterconfiguration.md) definiert. Die Liste ist entweder leer oder enthält numerische Werte. Der numerische Wert 0 (null) gibt an, dass die Zugriffsberechtigung für alle Ports erteilt wird. Eine leere Zeichenfolge gibt an, dass keine Zugriffsberechtigung für Ports erteilt wird, **wenn IPFilterSecurityEnabled** **true ist.**

</dd> <dt>

**IPSecPermitUDPPorts**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| UDPAllowedPorts")
</dt> </dl>

Array der Ports, denen die UDP-Zugriffsberechtigung (User Datagram Protocol) erteilt wird. Die Liste der Protokolle wird mithilfe der [**EnableIPSec-Methode**](enableipsec-method-in-class-win32-networkadapterconfiguration.md) definiert. Die Liste ist entweder leer oder enthält numerische Werte. Der numerische Wert 0 (null) gibt an, dass die Zugriffsberechtigung für alle Ports erteilt wird. Eine leere Zeichenfolge gibt an, dass keine Zugriffsberechtigung für Ports erteilt wird, **wenn IPFilterSecurityEnabled** **true ist.**

</dd> <dt>

**IPSubnet**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| System \\ \\ CurrentControlSet \\ \\ Services Parameters \| \| SubnetMask")
</dt> </dl>

Array aller Subnetzmasken, die dem aktuellen Netzwerkadapter zugeordnet sind.

Beispiel: "255.255.0.0"

</dd> <dt>

**IPUseZeroBroadcast**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| UseZeroBroadcast")
</dt> </dl>

True gibt an, dass IP-Nullen-Broadcasts verwendet werden (0.0.0.0), und das System verwendet Eins-Broadcasts (255.255.255.255). Computersysteme verwenden in der Regel Eins-Broadcasts, aber die von BSD-Implementierungen abgeleiteten Verwenden Nullen-Broadcasts. Systeme, die nicht dieselben Broadcasts verwenden, können nicht im selben Netzwerk zusammenarbeiten. Der Standardwert ist **FALSE.**

</dd> <dt>

**IPXAddress**
</dt> <dd> <dl> <dt>

Datentyp: **String**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**VERALTET,**](../wmisdk/standard-wmi-qualifiers.md) [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Windows Sockets Version 2 \| [**getsockopt**](/windows/win32/api/winsock/nf-winsock-getsockopt) \| IPX \_ ADDRESS")
</dt> </dl>

Die IPX-Technologie (Internetwork Packet Exchange) wird nicht mehr unterstützt, und diese Eigenschaft enthält keine nützlichen Daten.

</dd> <dt>

**IPXEnabled**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**VERALTET,**](../wmisdk/standard-wmi-qualifiers.md) [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WMI")
</dt> </dl>

Die IPX-Technologie (Internetwork Packet Exchange) wird nicht mehr unterstützt, und diese Eigenschaft enthält keine nützlichen Daten.

</dd> <dt>

**IPXFrameType**
</dt> <dd> <dl> <dt>

Datentyp: **uint32-Array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**VERALTET,**](../wmisdk/standard-wmi-qualifiers.md) [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ nwlnkipx \\ \\ Parameters \| PktType")
</dt> </dl>

Die IPX-Technologie (Internetwork Packet Exchange) wird nicht mehr unterstützt, und diese Eigenschaft enthält keine nützlichen Daten.

<dt>

<span id="Ethernet_II"></span><span id="ethernet_ii"></span><span id="ETHERNET_II"></span>

**Ethernet II** (0)


</dt> <dd></dd> <dt>

<span id="Ethernet_802.3"></span><span id="ethernet_802.3"></span><span id="ETHERNET_802.3"></span>

**Ethernet 802.3** (1)


</dt> <dd></dd> <dt>

<span id="Ethernet_802.2"></span><span id="ethernet_802.2"></span><span id="ETHERNET_802.2"></span>

**Ethernet 802.2** (2)


</dt> <dd></dd> <dt>

<span id="Ethernet_SNAP"></span><span id="ethernet_snap"></span><span id="ETHERNET_SNAP"></span>

**Ethernet-SNAP** (3)


</dt> <dd></dd> <dt>

<span id="AUTO"></span><span id="auto"></span>

**AUTO** (255)


</dt> <dd></dd> </dl>

</dd> <dt>

**IPXMediaType**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**VERALTET,**](../wmisdk/standard-wmi-qualifiers.md) [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ nwlnkipx \\ \\ Parameters \| MediaType")
</dt> </dl>

Die IPX-Technologie (Internetwork Packet Exchange) wird nicht mehr unterstützt, und diese Eigenschaft enthält keine nützlichen Daten.

<dt>

<span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>

**Ethernet** (1)


</dt> <dd></dd> <dt>

<span id="Token_ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>

**Tokenring** (2)


</dt> <dd></dd> <dt>

<span id="FDDI"></span><span id="fddi"></span>

**FDDI** (3)


</dt> <dd></dd> <dt>

<span id="ARCNET"></span><span id="arcnet"></span>

**ARCNET** (8)


</dt> <dd></dd> </dl>

</dd> <dt>

**IPXNetworkNumber**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**VERALTET,**](../wmisdk/standard-wmi-qualifiers.md) [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ nwlnkipx \\ \\ Parameters \| NetworkNumber")
</dt> </dl>

Die IPX-Technologie (Internetwork Packet Exchange) wird nicht mehr unterstützt, und diese Eigenschaft enthält keine nützlichen Daten.

</dd> <dt>

**IPXVirtualNetNumber**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**VERALTET**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ nwlnkipx Parameters \\ \\ \| VirtualNetworkNumber")
</dt> </dl>

Die IPX-Technologie (Internetwork Packet Exchange) wird nicht mehr unterstützt, und diese Eigenschaft enthält keine nützlichen Daten.

</dd> <dt>

**KeepAliveInterval**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| KeepAliveInterval"), [**Units**](../wmisdk/standard-qualifiers.md) ("milliseconds")
</dt> </dl>

Intervall, das Keep Alive-Neuübertragungen trennt, bis eine Antwort empfangen wird. Nachdem eine Antwort empfangen wurde, wird die Verzögerung bis zur nächsten Keep Alive-Übertragung wieder durch den Wert von **KeepAliveTime** gesteuert. Die Verbindung wird abgebrochen, nachdem die Anzahl der von **TcpMaxDataRetransmissions angegebenen Neuübertragungen** nicht mehr beantwortet wurde. Standardwert: 1000, Gültiger Bereich: 1 – 0xFFFFFFFF.

</dd> <dt>

**KeepAliveTime**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| KeepAliveInterval"), [**Units**](../wmisdk/standard-qualifiers.md) ("milliseconds")
</dt> </dl>

Die **KeepAliveTime-Eigenschaft** gibt an, wie oft tcp versucht, zu überprüfen, ob eine Leerlaufverbindung noch intakt ist, indem ein Keep Alive-Paket gesendet wird. Ein erreichbares Remotesystem bestätigt die Keep-Alive-Übertragung. Keep Alive-Pakete werden standardmäßig nicht gesendet. Dieses Feature kann in einer Verbindung von einer Anwendung aktiviert werden. Standardwert: 7.200.000 (zwei Stunden).

</dd> <dt>

**MACAddress**
</dt> <dd> <dl> <dt>

Datentyp: **String**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API-Geräteeingabe- \| und -ausgabefunktionen \| DeviceIoControl")
</dt> </dl>

Mac-Adresse (Media Access Control) des Netzwerkadapters. Eine MAC-Adresse wird vom Hersteller zugewiesen, um den Netzwerkadapter eindeutig zu identifizieren.

Beispiel: "00:80:C7:8F:6C:96"

</dd> <dt>

**MTU**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| MTU"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")
</dt> </dl>

Überschreibt die standardmäßige maximale Übertragungseinheit (Maximum Transmission Unit, MTU) für eine Netzwerkschnittstelle. Die MTU ist die maximale Paketgröße (einschließlich des Transportheaders), die der Transport über das zugrunde liegende Netzwerk überträgt. Das IP-Datagramm kann mehrere Pakete umfassen. Der Bereich dieses Werts umfasst die mindeste Paketgröße (68) bis zur MTU, die vom zugrunde liegenden Netzwerk unterstützt wird.

</dd> <dt>

**NumForwardPackets**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| NumForwardPackets")
</dt> </dl>

Anzahl der IP-Paketheader, die der Routerpaketwarteschlange zugeordnet sind. Wenn alle Header verwendet werden, beginnt der Router, Pakete nach dem Zufallsprinzip aus der Warteschlange zu verwerfen. Dieser Wert sollte mindestens so groß sein wie der **ForwardBufferMemory-Wert** dividiert durch die maximale IP-Datengröße der mit dem Router verbundenen Netzwerke. Er sollte nicht größer als der **ForwardBufferMemory-Wert** dividiert durch 256 sein, da mindestens 256 Bytes Vorwärtspufferspeicher für jedes Paket verwendet werden. Die optimale Anzahl von Forward-Paketen für eine bestimmte **ForwardBufferMemory-Größe** hängt vom Typ des Datenverkehrs im Netzwerk ab. Sie liegt zwischen diesen beiden Werten. Wenn der Router nicht aktiviert ist, wird dieser Parameter ignoriert, und es werden keine Header zugeordnet. Standardwert: 50, Gültiger Bereich: 1 – 0xFFFFFFFE.

</dd> <dt>

**PMTUBHDetectEnabled**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| EnablePMTUBHDetect")
</dt> </dl>

True **gibt an,** dass die Erkennung von Routern mit schwarzer Lücke erfolgt, während TCP den Pfad der maximalen Übertragungseinheit entdeckt. Ein Router mit schwarzer Lücke gibt keine ICMP-Zielnachrichten zurück, die nicht erreichbar sind, wenn ein IP-Datagramm fragmentiert werden muss, wenn das Bit Nicht fragmentieren festgelegt ist. TCP hängt vom Empfang dieser Nachrichten ab, um die Pfad-MTU-Ermittlung durchzuführen. Wenn dieses Feature aktiviert ist, versucht TCP, Segmente zu senden, ohne dass das Bit "Nicht fragmentieren" festgelegt ist, wenn mehrere Neuübertragungen eines Segments nicht bestätigt werden. Wenn das Segment als Ergebnis bestätigt wird, wird der MSS verringert, und das Bit Nicht fragmentieren wird in zukünftigen Paketen für die Verbindung festgelegt. Durch die Aktivierung der Erkennung schwarzer Löcher erhöht sich die maximale Anzahl von Neuübertragungen, die für ein bestimmtes Segment ausgeführt werden. Der Standardwert dieser Eigenschaft ist **FALSE.**

</dd> <dt>

**PMTUDiscoveryEnabled**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| EnablePMTUDiscovery")
</dt> </dl>

True gibt an, dass der Pfad der maximalen Übertragungseinheit (Maximum Transmission Unit, MTU) über den Pfad zu einem Remotehost ermittelt wird. Indem der MTU-Pfad entdeckt und TCP-Segmente auf diese Größe beschränkt werden, kann TCP die Fragmentierung an Routern entlang des Pfads beseitigen, die Netzwerke mit unterschiedlichen MTUs verbinden. Fragmentierung wirkt sich negativ auf TCP-Durchsatz und Netzwerküberlastung aus. Wenn Sie diesen Parameter auf **FALSE** festlegen, wird eine MTU von 576 Bytes für alle Verbindungen verwendet, die nicht mit Computern im lokalen Subnetz verbunden sind. Der Standardwert ist **TRUE.**

</dd> <dt>

**Servicename**
</dt> <dd> <dl> <dt>

Datentyp: **String**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Software Microsoft Windows NT \\ \\ \\ \\ \\ \\ CurrentVersion \\ \\ NetworkCards \| ServiceName")
</dt> </dl>

Dienstname des Netzwerkadapters. Dieser Name ist in der Regel kürzer als der vollständige Produktname.

Beispiel: "Elnkii"

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

Datentyp: **String**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Bezeichner, unter dem das aktuelle Objekt bekannt ist.

Diese Eigenschaft wird von der [**CIM-Einstellung \_ geerbt.**](cim-setting.md)

</dd> <dt>

**TcpipNetbiosOptions**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Bitmap der möglichen Einstellungen im Zusammenhang mit NetBIOS über TCP/IP. Werte werden in der folgenden Liste identifiziert.

<dt>

<span id="EnableNetbiosViaDhcp"></span><span id="enablenetbiosviadhcp"></span><span id="ENABLENETBIOSVIADHCP"></span>

**EnableNetbiosViaDhcp** (0)


</dt> <dd></dd> <dt>

<span id="EnableNetbios"></span><span id="enablenetbios"></span><span id="ENABLENETBIOS"></span>

**EnableNetbios** (1)


</dt> <dd></dd> <dt>

<span id="DisableNetbios"></span><span id="disablenetbios"></span><span id="DISABLENETBIOS"></span>

**DisableNetbios** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**TcpMaxConnectRetransmissions**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| TcpMaxConnectRetransmissions")
</dt> </dl>

Gibt an, wie oft TCP versucht, eine Connect-Anforderung erneut zu übertragen, bevor die Verbindung beendet wird. Das anfängliche Timeout für die Neuübertragung beträgt 3 Sekunden. Das Neuübertragungs-Timeout verdoppelt sich für jeden Versuch. Standardwert: 3, Gültiger Bereich: 0 – 0xFFFFFFFF.

</dd> <dt>

**TcpMaxDataRetransmissions**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| TcpMaxDataRetransmissions")
</dt> </dl>

Gibt an, wie oft TCP ein einzelnes Datensegment (Nichtverbindungssegment) erneut überträgt, bevor die Verbindung beendet wird. Das Timeout für die Neuübertragung verdoppelt sich mit jeder nachfolgenden Neuübertragung für eine Verbindung. Standardwert: 5, Gültiger Bereich: 0 – 0xFFFFFFFF.

</dd> <dt>

**Tcpnumconnections**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| TcpNumConnections")
</dt> </dl>

Maximale Anzahl von Verbindungen, die TCP gleichzeitig geöffnet haben kann. Standard: 0xFFFFFE, Gültiger Bereich: 0 – 0xFFFFFE.

</dd> <dt>

**TcpUseRFC1122RolentPointer**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ \\ Tcpip-Parameter \\ \| TcpUseRFC1122PinentPointer")
</dt> </dl>

True gibt an, dass TCP die RFC 1122-Spezifikation für dringende Daten verwendet. False  (Standard) gibt an, dass TCP den Modus verwendet, der von BSD-abgeleiteten Systemen (California Software Design) verwendet wird. Die beiden Mechanismen interpretieren den dringenden Zeiger unterschiedlich und sind nicht interoperabel. Der Standardwert ist **FALSE**.

</dd> <dt>

**TcpWindowSize**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| TcpWindowSize"), [**Units**](../wmisdk/standard-qualifiers.md) ("bytes")
</dt> </dl>

Maximale TCP-Empfangsfenstergröße, die vom System angeboten wird. Das Empfangsfenster gibt die Anzahl der Bytes an, die ein Absender übertragen kann, ohne eine Bestätigung zu empfangen. Im Allgemeinen verbessern größere Empfangsfenster die Leistung gegenüber Netzwerken mit hoher Verzögerung und hoher Bandbreite. Aus Effizienzgründen sollte das Empfangsfenster ein gerades Vielfaches der maximalen TCP-Segmentgröße (MSS) sein. Standardeinstellung: Viermal so groß wie die maximale TCP-Datengröße oder sogar ein Vielfaches der TCP-Datengröße, aufgerundet auf das nächste Vielfache von 8192. Ethernet-Netzwerke sind standardmäßig auf 8760 festgelegt. Gültiger Bereich: 0 bis 65535.

> [!Note]  
> Windows Vista: Diese Eigenschaft greifen auf den Registrierungseintrag zu, der in der aktuellen Implementierung des `"CurrentControlSet\\Services\\Tcpip\\Parameters|TcpWindowSize"` Betriebssystems nicht verwendet wird.

 

</dd> <dt>

**WINSEnableLMHostsLookup**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| EnableLMHOSTS")
</dt> </dl>

True **gibt an,** dass lokale Nachschlagedateien verwendet werden. Suchdateien enthalten eine Zuordnung von IP-Adressen zu Hostnamen. Wenn sie auf dem lokalen System vorhanden sind, finden Sie sie unter \\ %SystemRoot%-System32-Treiber \\ \\ usw.

</dd> <dt>

**WINSHostLookupFile**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Systeminformationen Functions \| [**GetSystemDirectory**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya) \| \\ \\ drivers \\ \\ etc \\ \\ lmhosts")
</dt> </dl>

Pfad zu einer WINS-Nachschlagedatei auf dem lokalen System. Diese Datei enthält eine Zuordnung von IP-Adressen zu Hostnamen. Wenn die in dieser Eigenschaft angegebene Datei gefunden wird, wird sie in den Ordner %SystemRoot% \\ system32 drivers etc des \\ lokalen Systems \\ kopiert. Nur gültig, wenn die **WINSEnableLMHostsLookup-Eigenschaft** **TRUE ist.**

</dd> <dt>

**WINSPrimaryServer**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Device Input and Output Functions \| DeviceIoControl")
</dt> </dl>

IP-Adresse für den primären WINS-Server.

</dd> <dt>

**WINSScopeID**
</dt> <dd> <dl> <dt>

Datentyp: **String**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| SYSTEM \\ \\ CurrentControlSet \\ \\ Services \\ \\ Tcpip \\ \\ Parameters \| ScopeID")
</dt> </dl>

Der Wert wird am Ende des NetBIOS-Namens angefügt, der eine Gruppe von Computersystemen isoliert, die nur miteinander kommunizieren. Sie wird für alle NetBIOS-Transaktionen über TCP/IP-Kommunikation von diesem Computersystem verwendet. Computer, die mit identischen Bereichsbezeichnern konfiguriert sind, können mit diesem Computer kommunizieren. TCP/IP-Clients mit unterschiedlichen Bereichsbezeichnern ignorieren Pakete von Computern mit dieser Bereichs-ID. Nur gültig, wenn die [**EnableWINS-Methode**](enablewins-method-in-class-win32-networkadapterconfiguration.md) erfolgreich ausgeführt wird.

</dd> <dt>

**WINSSecondaryServer**
</dt> <dd> <dl> <dt>

Datentyp: **String**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API-Geräteeingabe- \| und -ausgabefunktionen \| DeviceIoControl")
</dt> </dl>

IP-Adresse für den sekundären WINS-Server.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **Win32 \_ NetworkAdapterConfiguration-Klasse** wird von [**der \_ CIM-Einstellung**](cim-setting.md)abgeleitet.

## <a name="examples"></a>Beispiele

Im VBScript-Codebeispiel für [WMI Information Retriever](https://Gallery.TechNet.Microsoft.Com/e493376c-1286-456b-bd4b-4ac3b0e9bb45) im TechNet-Katalog wird die **Win32 \_ NetworkAdapterConfiguration-Klasse** verwendet, um Netzwerkkonfigurationsinformationen von einer Reihe von Remotecomputern abzurufen.

Das [PowerShell-Beispiel Get-ComputerInfo – Query Computer Info From Local/Remote Computers - (WMI)](https://Gallery.TechNet.Microsoft.Com/Get-ComputerInfo-Query-23dd6042) im TechNet Gallery verwendet eine Reihe von Aufrufen von Hardware und Software, einschließlich **Win32 \_ NetworkAdapterConfiguration,** um Informationen zu einem lokalen oder Remotesystem anzuzeigen.

Der folgende PowerShell-Code ruft die Konfigurationseinstellungen für den Microsoft ISTAP-Adapter ab.


```PowerShell
$IstapAdapterConfig = Get-WmiObject Win32_NetworkAdapterConfiguration | Where-Object {$_.Description -eq "Microsoft ISATAP Adapter"}
$IstapAdapterConfig
```



Im folgenden \# C-Beispiel werden die Beschreibung und die Indexnummer aller Netzwerkadapter-Konfigurationsinstanzen abgerufen. Beachten Sie, dass in diesem C-Beispiel der \# [Namespace Microsoft.Management.Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) verwendet wird, der im Allgemeinen effizienter skaliert wird als die WMI-Klassen des [System.Management-Namespace.](/dotnet/api/system.management)


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



Im folgenden \# C-Beispiel werden die Beschreibung und Indexnummer aller Netzwerkadapter-Konfigurationsinstanzen abgerufen. Beachten Sie, dass in \# diesem C-Beispiel der ursprüngliche [System.Management-Namespace](/dotnet/api/system.management) verwendet wird, der von [Microsoft.Management.Infrastructure ersetzt wurde.](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85))


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



Im folgenden Beispiel werden Informationen aus der **Win32 \_ NetworkAdapterConfiguration-Klasse** abgerufen.


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
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**\_CIM-Einstellung**](cim-setting.md)
</dt> <dt>

[Hardwareklassen des Computersystems](computer-system-hardware-classes.md)
</dt> <dt>

[WMI-Aufgaben: Netzwerk](../wmisdk/wmi-tasks--networking.md)
</dt> <dt>

[WMI-Aufgaben: Konten und Domänen](../wmisdk/wmi-tasks--accounts-and-domains.md)
</dt> <dt>

[IPv6- und IPv4-Unterstützung in WMI](../wmisdk/ipv6-and-ipv4-support-in-wmi.md)
</dt> </dl>

 

 
