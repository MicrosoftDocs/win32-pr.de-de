---
description: Stellt Einstellungen für die Zuordnung des Ethernet-Ports dar, zusätzlich zu den Einstellungen, die von der CIM- \_ Ethernetport-Klasse bereitgestellt werden. Diese Einstellungen werden verwendet, um spezifische Informationen für die Ressource bereitzustellen.
ms.assetid: f59ebaf1-60dd-49bd-b48e-d7a6c2650909
title: CIM_EthernetPortAllocationSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_EthernetPortAllocationSettingData
- CIM_EthernetPortAllocationSettingData.DesiredVLANEndpointMode
- CIM_EthernetPortAllocationSettingData.OtherEndpointMode
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7e77b4387f77e88ceaff273b8be72a354c989e7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106338954"
---
# <a name="cim_ethernetportallocationsettingdata-class"></a>CIM- \_ ethernetportationscationsettingdata-Klasse

Stellt Einstellungen für die Zuordnung des Ethernet-Ports dar, zusätzlich zu den Einstellungen, die von der [**CIM- \_ Ethernetport**](cim-ethernetport.md) -Klasse bereitgestellt werden. Diese Einstellungen werden verwendet, um spezifische Informationen für die Ressource bereitzustellen.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, Version("2.26.0"), UMLPackagePath("CIM::Core::Resource"), AMENDMENT]
class CIM_EthernetPortAllocationSettingData : CIM_ResourceAllocationSettingData
{
  uint16 DesiredVLANEndpointMode;
  string OtherEndpointMode;
};
```

## <a name="members"></a>Member

Die CIM-Klasse " **\_ ethernetportzugewiesene cationsettingdata** " enthält diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die CIM-Klasse " **\_ ethernetportzugewiesene cationsettingdata** " verfügt über diese Eigenschaften.

<dl> <dt>

**Desiredvlanendpointmode**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ vlanendpoint**](cim-vlanendpoint.md)".**Operationalendpointmode**","**CIM \_ vlanendpoint**.**"Desiredendpointmode**", "**CIM \_ ethernetportzuweisung cationsettingdata**".**Otherendpointmode**")
</dt> </dl>

Der angeforderte VLAN-Modus. Diese Eigenschaft wird verwendet, um den ursprünglichen **operationalendpointmode** -Eigenschafts Wert in der Instanz von **CIM \_ vlanendpoint** festzulegen, die dem Ethernet-Port zugeordnet ist.

<dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reserviert** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Sonstige** (1)


</dt> <dd></dd> <dt>

<span id="Access"></span><span id="access"></span><span id="ACCESS"></span>

**Zugriff** (2)


</dt> <dd></dd> <dt>

<span id="Dynamic_Auto"></span><span id="dynamic_auto"></span><span id="DYNAMIC_AUTO"></span>

**Dynamisches Auto** (3)


</dt> <dd></dd> <dt>

<span id="Dynamic_Desirable"></span><span id="dynamic_desirable"></span><span id="DYNAMIC_DESIRABLE"></span>

**Dynamisch erwünscht** (4)


</dt> <dd></dd> <dt>

<span id="Trunk"></span><span id="trunk"></span><span id="TRUNK"></span>

**Trunk** (5)


</dt> <dd></dd> <dt>

<span id="Dot1Q_Tunnel"></span><span id="dot1q_tunnel"></span><span id="DOT1Q_TUNNEL"></span>

**Dot1Q Tunnel** (6)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reserviert** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Anbieter reserviert** (0X8000.. 0xFFFF


</dt> <dd></dd> </dl>

</dd> <dt>

**Otherendpointmode**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ethernetportzuweisung-Daten**.**Desiredvlanendpointmode**")
</dt> </dl>

Der Typ des VLAN-Endpunkt Modells, das von diesem VLAN-Endpunkt unterstützt wird, wenn der Wert der Mode-Eigenschaft auf "1" (sonstige) festgelegt ist. Diese Eigenschaft sollte auf **null** festgelegt werden, wenn die Mode-Eigenschaft einen anderen Wert als "1" hat.

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

[**CIM \_ resourcezubesettingdata**](cim-resourceallocationsettingdata.md)
</dt> </dl>

 

