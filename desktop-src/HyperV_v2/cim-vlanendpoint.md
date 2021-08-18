---
description: Ein Endpunkt auf einem Switch oder einer Endstation, der einem VLAN zugewiesen ist oder Datenverkehr von einem oder mehreren VLANs akzeptiert.
ms.assetid: 20943be3-35c3-4bf5-8f1a-d4095fa6897e
title: CIM_VLANEndpoint-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VLANEndpoint
- CIM_VLANEndpoint.DesiredEndpointMode
- CIM_VLANEndpoint.OtherEndpointMode
- CIM_VLANEndpoint.OperationalEndpointMode
- CIM_VLANEndpoint.DesiredVLANTrunkEncapsulation
- CIM_VLANEndpoint.OtherTrunkEncapsulation
- CIM_VLANEndpoint.OperationalVLANTrunkEncapsulation
- CIM_VLANEndpoint.GVRPStatus
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: caaedae456ded5b918a19b09f18ebcf7f32c0edf2c0eff6c16d8ff98519b1dd9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068500"
---
# <a name="cim_vlanendpoint-class"></a>CIM \_ VLANEndpoint-Klasse

Ein Endpunkt auf einem Switch oder einer Endstation, der einem VLAN zugewiesen ist oder Datenverkehr von einem oder mehreren VLANs akzeptiert.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, Version("2.26.0"), UMLPackagePath("CIM::Network::VLAN"), AMENDMENT]
class CIM_VLANEndpoint : CIM_ProtocolEndpoint
{
  uint16 DesiredEndpointMode;
  string OtherEndpointMode;
  uint16 OperationalEndpointMode;
  uint16 DesiredVLANTrunkEncapsulation;
  string OtherTrunkEncapsulation;
  uint16 OperationalVLANTrunkEncapsulation;
  uint16 GVRPStatus;
};
```

## <a name="members"></a>Member

Die **CIM \_ VLANEndpoint-Klasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ VLANEndpoint-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**DesiredEndpointMode**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VLANEndpoint**.**OperationalEndpointMode**", "**CIM \_ VLANEndpoint**.**OtherEndpointMode**")
</dt> </dl>

Der angeforderte VLAN-Modus für den Endpunkt.

<dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reserviert** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Andere** (1)


</dt> <dd></dd> <dt>

<span id="Access"></span><span id="access"></span><span id="ACCESS"></span>

**Zugriff** (2)


</dt> <dd></dd> <dt>

<span id="Dynamic_Auto"></span><span id="dynamic_auto"></span><span id="DYNAMIC_AUTO"></span>

**Dynamisch automatisch** (3)


</dt> <dd></dd> <dt>

<span id="Dynamic_Desirable"></span><span id="dynamic_desirable"></span><span id="DYNAMIC_DESIRABLE"></span>

**Dynamisch wünschenswert** (4)


</dt> <dd></dd> <dt>

<span id="Trunk"></span><span id="trunk"></span><span id="TRUNK"></span>

**Trunk** (5)


</dt> <dd></dd> <dt>

<span id="Dot1Q_Tunnel"></span><span id="dot1q_tunnel"></span><span id="DOT1Q_TUNNEL"></span>

**Dot1Q Tunnel** (6)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reserved** (7..32767)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Reservierter Anbieter** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**DesiredVLANTrunkEncapsulation**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ VLANEndpointCapabilities.SupportsTrunkEncapsulationNegotiation", "**CIM \_ VLANEndpoint**.**OperationalVLANTrunkEncapsulation**", "**CIM \_ VLANEndpoint**.**OtherTrunkEncapsulation**")
</dt> </dl>

Der angeforderte VLAN-Kapselungstyp.

> [!Note]  
> Diese Eigenschaft wird nur verwendet, wenn sich der VLAN-Endpunkt im Trunkingmodus befindet.

 

<dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reserviert** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Andere** (1)


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

**Nicht zutreffend** (2)


</dt> <dd></dd> <dt>

<span id="802.1q"></span><span id="802.1Q"></span>

**802.1q** (3)


</dt> <dd></dd> <dt>

<span id="Cisco_ISL"></span><span id="cisco_isl"></span><span id="CISCO_ISL"></span>

**Cisco ISL** (4)


</dt> <dd></dd> <dt>

<span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>

**Aushandeln** (5)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reserved** (6..32767)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Reservierter Anbieter** (32768.)


</dt> <dd></dd> </dl>

</dd> <dt>

**GVRPStatus**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VLANEndpoint**.**OperationalEndpointMode**, CIM \_ VLANEndpointCapabilities.Dot1QTagging")
</dt> </dl>

Gibt an, ob DAS GARP VLAN Registration Protocol (GVRP) auf dem Trunkendpunkt aktiviert oder deaktiviert ist.

> [!Note]  
> Diese Eigenschaft wird nur verwendet, wenn GVRP vom Endpunkt unterstützt wird und der Trunkingmodus aktiviert ist.

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

**Nicht zutreffend** (2)


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**Aktiviert** (3)


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Deaktiviert** (4)


</dt> <dd></dd> </dl>

</dd> <dt>

**OperationalEndpointMode**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VLANEndpoint**.**DesiredEndpointMode**", "**CIM \_ VLANEndpoint**.**OtherEndpointMode**")
</dt> </dl>

Der aktuelle VLAN-Modus für den Endpunkt.

<dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reserviert** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Andere** (1)


</dt> <dd></dd> <dt>

<span id="Access"></span><span id="access"></span><span id="ACCESS"></span>

**Zugriff** (2)


</dt> <dd></dd> <dt>

<span id="Dynamic_Auto"></span><span id="dynamic_auto"></span><span id="DYNAMIC_AUTO"></span>

**Dynamisch automatisch** (3)


</dt> <dd></dd> <dt>

<span id="Dynamic_Desirable"></span><span id="dynamic_desirable"></span><span id="DYNAMIC_DESIRABLE"></span>

**Dynamisch wünschenswert** (4)


</dt> <dd></dd> <dt>

<span id="Trunk"></span><span id="trunk"></span><span id="TRUNK"></span>

**Trunk** (5)


</dt> <dd></dd> <dt>

<span id="Dot1Q_Tunnel"></span><span id="dot1q_tunnel"></span><span id="DOT1Q_TUNNEL"></span>

**Dot1Q Tunnel** (6)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reserved** (7..32767)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Reservierter Anbieter** (..)


</dt> <dd></dd> </dl>

</dd> <dt>

**OperationalVLANTrunkEncapsulation**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VLANEndpoint**.**OtherTrunkEncapsulation**", "**CIM \_ VLANEndpoint**.**DesiredVLANTrunkEncapsulation**")
</dt> </dl>

Der aktuelle VLAN-Kapselungstyp.

> [!Note]  
> Diese Eigenschaft wird nur verwendet, wenn sich der VLAN-Endpunkt im Trunkingmodus befindet.

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Andere** (1)


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

**Nicht zutreffend** (2)


</dt> <dd></dd> <dt>

<span id="802.1q"></span><span id="802.1Q"></span>

**802.1q** (3)


</dt> <dd></dd> <dt>

<span id="Cisco_ISL"></span><span id="cisco_isl"></span><span id="CISCO_ISL"></span>

**Cisco ISL** (4)


</dt> <dd></dd> <dt>

<span id="Negotiating"></span><span id="negotiating"></span><span id="NEGOTIATING"></span>

**Aushandeln** (5)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reserved** (6..32767)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Reservierter Anbieter** (32768.)


</dt> <dd></dd> </dl>

</dd> <dt>

**OtherEndpointMode**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VLANEndpoint**.**DesiredEndpointMode**", "**CIM \_ VLANEndpoint**.**OperationalEndpointMode**")
</dt> </dl>

Der Typ des VLAN-Endpunktmodells, der vom VLANEndpoint unterstützt wird, wenn der Wert von **DesiredEndpointMode** auf "1" festgelegt ist (andere); Andernfalls **NULL.**

</dd> <dt>

**OtherTrunkEncapsulation**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VLANEndpoint**.**DesiredVLANTrunkEncapsulation**", "**CIM \_ VLANEndpoint**.**OperationalVLANTrunkEncapsulation**")
</dt> </dl>

Der Typ der VLAN-Kapselung, der vom VLAN-Endpunkt unterstützt wird, wenn der Wert der **DesiredVLANTrunkEncapsulation-Eigenschaft** auf 1 (sonstige) festgelegt ist. Andernfalls **NULL.**

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | \\Root-Virtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CIM \_ ProtocolEndpoint**](cim-protocolendpoint.md)
</dt> </dl>

 

