---
description: Stellt einen Ethernet-Anschluss dar.
ms.assetid: c9a148c2-cf02-466f-b8ca-b1bf616d75dc
title: CIM_EthernetPort-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_EthernetPort
- CIM_EthernetPort.PortType
- CIM_EthernetPort.NetworkAddresses
- CIM_EthernetPort.MaxDataSize
- CIM_EthernetPort.Capabilities
- CIM_EthernetPort.CapabilityDescriptions
- CIM_EthernetPort.EnabledCapabilities
- CIM_EthernetPort.OtherEnabledCapabilities
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a44e93f84178fa2714d3c823735b3d90922e04be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524923"
---
# <a name="cim_ethernetport-class"></a>CIM- \_ Ethernetport-Klasse

Stellt einen Ethernet-Anschluss dar.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, Version("2.10.0"), UMLPackagePath("CIM::Device::Ports"), AMENDMENT]
class CIM_EthernetPort : CIM_NetworkPort
{
  uint16 PortType;
  string NetworkAddresses[];
  uint32 MaxDataSize;
  uint16 Capabilities[];
  string CapabilityDescriptions[];
  uint16 EnabledCapabilities[];
  string OtherEnabledCapabilities[];
};
```

## <a name="members"></a>Member

Die **CIM- \_ Ethernetport** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM- \_ Ethernetport** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Capabilities**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM- \_ Ethernetport**".**Capabilitybeschreibungen**")
</dt> </dl>

Die Funktionen des Ethernet-Ports.

> [!Note]  
> Wenn Failover-oder Lasten Ausgleichs Funktionen aktiviert sind, sollte auch ein [**CIM- \_ SpareGroup**](/windows/desktop/CIMWin32Prov/cim-sparegroup) -Objekt (Failover) oder [**CIM \_ extracapacitygroup**](/windows/desktop/CIMWin32Prov/cim-extracapacitygroup) -Objekt (Lasten Ausgleichs Objekt) definiert werden, um die Funktion vollständig zu beschreiben.

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Sonstige** (1)


</dt> <dd></dd> <dt>

<span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>

**Alertonlan** (2)


</dt> <dd></dd> <dt>

<span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>

**Wake-on-LAN** (3)


</dt> <dd></dd> <dt>

<span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>

**Failover** (4)


</dt> <dd></dd> <dt>

<span id="LoadBalancing"></span><span id="loadbalancing"></span><span id="LOADBALANCING"></span>

**Loadbalancing** (5)


</dt> <dd></dd> </dl>

</dd> <dt>

**Capabilitybeschreibungen**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM- \_ Ethernetport**".**Funktionen**")
</dt> </dl>

Ein Array von Freiform-Zeichen folgen, das Ausführlichere Erläuterungen zu allen Features bereitstellt, die im Funktions Array angegeben sind. Die Elemente in diesem Array entsprechen den Elementen im Funktions Array.

</dd> <dt>

**Enabled-Funktionen**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM- \_ Ethernetport**".**Funktionen**","**CIM- \_ Ethernetport**.**Otherenabledfunktionalitäten**")
</dt> </dl>

Gibt an, welche Funktionen im Funktions Array aktiviert sind. Die Elemente in diesem Array entsprechen den Elementen im Funktions Array.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Sonstige** (1)


</dt> <dd></dd> <dt>

<span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>

**Alertonlan** (2)


</dt> <dd></dd> <dt>

<span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>

**Wake-on-LAN** (3)


</dt> <dd></dd> <dt>

<span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>

**Failover** (4)


</dt> <dd></dd> <dt>

<span id="LoadBalancing"></span><span id="loadbalancing"></span><span id="LOADBALANCING"></span>

**Loadbalancing** (5)


</dt> <dd></dd> </dl>

</dd> <dt>

**Maxdatasize**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Bridge-MIB. dot1dTpPortMaxInfo ")
</dt> </dl>

Die maximale Größe des Felds Info (nicht-Mac), das empfangen oder übertragen wird.

</dd> <dt>

**"Networkaddresses"**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Netzwerkadressen")
</dt> </dl>

Die dem Port zugewiesenen Netzwerkadressen. Die Adresse ist ein 802,3-Mac, der als zwölf hexadezimal Ziffern formatiert ist (z. b. "010203040506"), wobei jedes Ziffern Paar eines der sechs Oktette der Mac-Adresse in kanonischer bitreihenfolge darstellt.

</dd> <dt>

**Otherenabled-Funktionen**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM- \_ Ethernetport**".**Enabledfunktionalitäten**")
</dt> </dl>

Ein Array von Freiform-Zeichen folgen, die Ausführlichere Erläuterungen zu allen **enabledfunktionalitäten** -Array Elementen bereitstellen, die auf 1 (Sonstiges) festgelegt sind. Die Elemente in diesem Array entsprechen den Elementen im **enabledfunktionalitäten** -Array.

</dd> <dt>

**PortType**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("PortType")
</dt> </dl>

Der Modus, der für den Port aktiviert ist. Bei Festlegung auf 1 (Sonstiges) beschreibt die **otherporttype** -Eigenschaft den-Modus.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Sonstige** (1)


</dt> <dd></dd> <dt>

<span id="10BaseT"></span><span id="10baset"></span><span id="10BASET"></span>

**10BaseT** (50)


</dt> <dd></dd> <dt>

<span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>

**10-100-BaseT** (51)


</dt> <dd></dd> <dt>

<span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>

**100 BaseT** (52)


</dt> <dd></dd> <dt>

<span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>

**1000 BaseT** (53)


</dt> <dd></dd> <dt>

<span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>

**2500baset** (54)


</dt> <dd></dd> <dt>

<span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>

**10gbaset** (55)


</dt> <dd></dd> <dt>

<span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>

**10GBase-CX4** (56)


</dt> <dd></dd> <dt>

<span id="100Base-FX"></span><span id="100base-fx"></span><span id="100BASE-FX"></span>

**100Base-FX** (100)


</dt> <dd></dd> <dt>

<span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>

**100BASE-SX** (101)


</dt> <dd></dd> <dt>

<span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>

**1000 Base-SX** (102)


</dt> <dd></dd> <dt>

<span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>

**1000 Base-LX** (103)


</dt> <dd></dd> <dt>

<span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>

**1000 Base-CX** (104)


</dt> <dd></dd> <dt>

<span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>

**10GBASE-SR** (105)


</dt> <dd></dd> <dt>

<span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>

**10GBase-SW** (106)


</dt> <dd></dd> <dt>

<span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>

**10GBASE-LX4** (107)


</dt> <dd></dd> <dt>

<span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>

**10GBASE-LR** (108)


</dt> <dd></dd> <dt>

<span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>

**10GBase-LW** (109)


</dt> <dd></dd> <dt>

<span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>

**10GBase-er** (110)


</dt> <dd></dd> <dt>

<span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>

**10GBase-EW** (111)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Anbieter reserviert** (16000.65535)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM- \_ Netzwerkport**](cim-networkport.md)
</dt> </dl>

 

