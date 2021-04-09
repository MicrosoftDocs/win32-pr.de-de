---
description: Stellt die Konfiguration eines Netzwerkadapters innerhalb des Gast Betriebssystems dar.
ms.assetid: 154d4a0f-0c57-496a-a351-6caa74011544
title: Msvm_GuestNetworkAdapterConfiguration-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestNetworkAdapterConfiguration
- Msvm_GuestNetworkAdapterConfiguration.InstanceID
- Msvm_GuestNetworkAdapterConfiguration.ProtocolIFType
- Msvm_GuestNetworkAdapterConfiguration.DHCPEnabled
- Msvm_GuestNetworkAdapterConfiguration.IPAddresses
- Msvm_GuestNetworkAdapterConfiguration.Subnets
- Msvm_GuestNetworkAdapterConfiguration.DefaultGateways
- Msvm_GuestNetworkAdapterConfiguration.DNSServers
- Msvm_GuestNetworkAdapterConfiguration.IPAddressOrigins
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ce5738bca4563aa77678cac2b7e33f5c4d5323e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129749"
---
# <a name="msvm_guestnetworkadapterconfiguration-class"></a>MSVM \_ guestnetworkadapterconfiguration-Klasse

Stellt die Konfiguration eines Netzwerkadapters innerhalb des Gast Betriebssystems dar.

Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GuestNetworkAdapterConfiguration
{
  string  InstanceID;
  uint16  ProtocolIFType;
  boolean DHCPEnabled;
  string  IPAddresses[];
  string  Subnets[];
  string  DefaultGateways[];
  string  DNSServers[];
  UINT16  IPAddressOrigins[];
};
```

## <a name="members"></a>Member

Die **MSVM \_ guestnetworkadapterconfiguration** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM \_ guestnetworkadapterconfiguration** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Defaultgateways**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert")
</dt> </dl>

Ein Array von Zeichen folgen, die die Standard-IP-Gateways enthalten, die auf dem Netzwerkadapter innerhalb des Gast Betriebssystems konfiguriert sind. Die maximale Anzahl von Standard-IP-Gateways, die auf einem einzelnen Netzwerkadapter konfiguriert werden können, ist 5.

</dd> <dt>

**DHCPEnabled**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob DHCP auf dem Netzwerkadapter innerhalb des Gast Betriebssystems aktiviert ist.

</dd> <dt>

**DnsServers**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert")
</dt> </dl>

Ein Array von Zeichen folgen, das die DNS-Server enthält, die auf dem Netzwerkadapter innerhalb des Gast Betriebssystems konfiguriert sind.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Der eindeutige Bezeichner für dieses-Objekt.

</dd> <dt>

**IPAddresses**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert")
</dt> </dl>

Ein Array von Zeichen folgen, die die IP-Adressen enthalten, die auf dem Netzwerkadapter innerhalb des Gast Betriebssystems konfiguriert sind.

</dd> <dt>

**Ipaddressorigins**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert")
</dt> </dl>

Die Quelle der IP-Adressen, die auf dem Netzwerkadapter innerhalb des Gast Betriebssystems konfiguriert sind.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Sonstige** (1)


</dt> <dd></dd> <dt>

<span id="Static"></span><span id="static"></span><span id="STATIC"></span>

**Statisch** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**Protocoliftype**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt die IP-Protokolle an, auf die die von dieser Instanz angegebenen Einstellungen angewendet werden.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Sonstige** (1)


</dt> <dd></dd> <dt>

<span id="IPv4"></span><span id="ipv4"></span><span id="IPV4"></span>

**IPv4** (4096)


</dt> <dd></dd> <dt>

<span id="IPv6"></span><span id="ipv6"></span><span id="IPV6"></span>

**IPv6** (4097)


</dt> <dd></dd> <dt>

<span id="IPv4_v6"></span><span id="ipv4_v6"></span><span id="IPV4_V6"></span>

**IPv4/V6** (4098)


</dt> <dd></dd> </dl>

</dd> <dt>

**Subnetze**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert")
</dt> </dl>

Ein Array von Zeichen folgen, die die Subnetze enthalten, die auf dem Netzwerkadapter innerhalb des Gast Betriebssystems konfiguriert sind. Jedes Element in diesem Array gilt für das entsprechende Element im **IPADRESSEN** -Array.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

