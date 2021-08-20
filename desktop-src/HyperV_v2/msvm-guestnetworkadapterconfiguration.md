---
description: Stellt die Konfiguration eines Netzwerkadapters im Gastbetriebssystem dar.
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
ms.openlocfilehash: 0c208a14a8db57303b3ccc857ca15a5d7f88369b7093b9931c0c9cb80012230d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118147975"
---
# <a name="msvm_guestnetworkadapterconfiguration-class"></a>Msvm \_ GuestNetworkAdapterConfiguration-Klasse

Stellt die Konfiguration eines Netzwerkadapters im Gastbetriebssystem dar.

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

Die **Msvm \_ GuestNetworkAdapterConfiguration-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ GuestNetworkAdapterConfiguration-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**DefaultGateways**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")
</dt> </dl>

Ein Array von Zeichenfolgen, die die ip-Standardgateways enthalten, die auf dem Netzwerkadapter im Gastbetriebssystem konfiguriert sind. Die maximale Anzahl von Standard-IP-Gateways, die auf einem einzelnen Netzwerkadapter konfiguriert werden können, beträgt fünf.

</dd> <dt>

**DHCPEnabled**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob DHCP auf dem Netzwerkadapter im Gastbetriebssystem aktiviert ist.

</dd> <dt>

**DNSServers**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")
</dt> </dl>

Ein Array von Zeichenfolgen, die die DNS-Server enthalten, die auf dem Netzwerkadapter im Gastbetriebssystem konfiguriert sind.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Der eindeutige Bezeichner für dieses Objekt.

</dd> <dt>

**IPAddresses**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")
</dt> </dl>

Ein Array von Zeichenfolgen, die die IP-Adressen enthalten, die auf dem Netzwerkadapter im Gastbetriebssystem konfiguriert sind.

</dd> <dt>

**IPAddressOrigins**
</dt> <dd> <dl> <dt>

Datentyp: **UINT16-Array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")
</dt> </dl>

Die Quelle der IP-Adressen, die auf dem Netzwerkadapter im Gastbetriebssystem konfiguriert sind.

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

**ProtocolIFType**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Identifiziert die IP-Protokolle, für die die von dieser Instanz angegebenen Einstellungen gelten.

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

**IPv4/v6** (4098)


</dt> <dd></dd> </dl>

</dd> <dt>

**Subnetze**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolgenarray**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed")
</dt> </dl>

Ein Array von Zeichenfolgen, die die auf dem Netzwerkadapter im Gastbetriebssystem konfigurierten Subnetze enthalten. Jedes Element in diesem Array gilt für das entsprechende Element im **IPAddresses-Array.**

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

