---
description: Stellt einstellungen für die Zuordnung des Ethernetports dar, zusätzlich zu den Einstellungen, die von der CIM \_ EthernetPort-Klasse bereitgestellt werden. Diese Einstellungen werden verwendet, um spezifische Informationen für die Ressource selbst bereitzustellen.
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
ms.openlocfilehash: 7546af167a6e13712119a081e7dbfaee118dc0c8a4912b8411d898a4ad90bc7b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119695800"
---
# <a name="cim_ethernetportallocationsettingdata-class"></a>CIM \_ EthernetPortAllocationSettingData-Klasse

Stellt einstellungen für die Zuordnung des Ethernetports dar, zusätzlich zu den Einstellungen, die von der [**CIM \_ EthernetPort-Klasse**](cim-ethernetport.md) bereitgestellt werden. Diese Einstellungen werden verwendet, um spezifische Informationen für die Ressource selbst bereitzustellen.

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

Die **CIM \_ EthernetPortAllocationSettingData-Klasse** verfügt über folgende Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ EthernetPortAllocationSettingData-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**DesiredVLANEndpointMode**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**", "**CIM \_ VLANEndpoint**.**DesiredEndpointMode**", "**CIM \_ EthernetPortAllocationSettingData**.**OtherEndpointMode**")
</dt> </dl>

Der angeforderte VLAN-Modus. Diese Eigenschaft wird verwendet, um den **anfänglichen OperationalEndpointMode-Eigenschaftswert** in der Instanz von **CIM \_ VLANEndpoint** festzulegen, die dem Ethernetport zugeordnet ist.

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

**DMTF Reserved** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Reservierter Anbieter** (0x8000. 0xFFFF)


</dt> <dd></dd> </dl>

</dd> <dt>

**OtherEndpointMode**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ EthernetPortAllocationSettingData**.**DesiredVLANEndpointMode**")
</dt> </dl>

Der Typ des VLAN-Endpunktmodells, der von diesem VLAN-Endpunkt unterstützt wird, wenn der Wert der mode-Eigenschaft auf "1" (Sonstige) festgelegt ist. Diese Eigenschaft sollte auf **NULL** festgelegt werden, wenn die Modeeigenschaft einen anderen Wert als "1" hat.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | \\Root-Virtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md)
</dt> </dl>

 

