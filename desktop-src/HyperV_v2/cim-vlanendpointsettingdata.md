---
description: Stellt Konfigurationsdaten für einen VLAN-Endpunkt dar.
ms.assetid: 5ef3cc55-cf27-40b4-9e94-2e2b42ca41c5
title: CIM_VLANEndpointSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VLANEndpointSettingData
- CIM_VLANEndpointSettingData.PruneEligibleVLANList
- CIM_VLANEndpointSettingData.NativeVLAN
- CIM_VLANEndpointSettingData.DefaultVLAN
- CIM_VLANEndpointSettingData.TrunkedVLANList
- CIM_VLANEndpointSettingData.AccessVLAN
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 443d7b50ae8fe727a95464ec4e7fa589d7a08db770ce4c5090f37e5c988bfa4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119682610"
---
# <a name="cim_vlanendpointsettingdata-class"></a>CIM \_ VLANEndpointSettingData-Klasse

Stellt Konfigurationsdaten für einen VLAN-Endpunkt dar.

## <a name="syntax"></a>Syntax

``` syntax
[Experimental, Abstract, Version("2.11.0"), UMLPackagePath("CIM::Network::VLAN")]
class CIM_VLANEndpointSettingData : CIM_SettingData
{
  uint16 PruneEligibleVLANList[];
  uint16 NativeVLAN;
  uint16 DefaultVLAN;
  uint16 TrunkedVLANList[];
  uint16 AccessVLAN;
};
```

## <a name="members"></a>Member

Die **CIM \_ VLANEndpointSettingData-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ VLANEndpointSettingData-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**AccessVLAN**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**")
</dt> </dl>

Das Zugriffs-VLAN für den Endpunkt.

</dd> <dt>

**DefaultVLAN**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**")
</dt> </dl>

Der Standardwert für das native VLAN auf dem Trunkendpunkt.

> [!Note]  
> Diese Eigenschaft wird nur verwendet, wenn der VLAN-Endpunkt im Trunkingmodus ausgeführt wird, der in der **OperationalEndpointMode-Eigenschaft angegeben** ist.

 

</dd> <dt>

**NativeVLAN**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**")
</dt> </dl>

Die VLAN-ID, die verwendet wird, um nicht mit Tags versehenen Datenverkehr zu kennzeichnen, der am Trunkendpunkt empfangen wird.

> [!Note]  
> Diese Eigenschaft wird nur verwendet, wenn der VLAN-Endpunkt im Trunkingmodus ausgeführt wird, der in der **SwitchEndpointMode-Eigenschaft angegeben** ist.

 

</dd> <dt>

**PruneEligibleVLANList**
</dt> <dd> <dl> <dt>

Datentyp: **uint16 array**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**")
</dt> </dl>

Ein Array, das IDs von VLANs enthält, die das System möglicherweise vom Trunkendpunkt entfernt.

> [!Note]  
> Diese Eigenschaft wird nur verwendet, wenn der VLAN-Endpunkt im Trunkingmodus ausgeführt wird, der in der **OperationalEndpointMode-Eigenschaft angegeben** ist.

 

</dd> <dt>

**TrunkedVLANList**
</dt> <dd> <dl> <dt>

Datentyp: **uint16 array**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**")
</dt> </dl>

Ein Array, das IDs von VLAN-Endpunkten mit aktivierter Trunking enthält.

> [!Note]  
> Diese Eigenschaft wird nur verwendet, wenn der VLAN-Endpunkt im Trunkingmodus ausgeführt wird, der in der **OperationalEndpointMode-Eigenschaft angegeben** ist.

 

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8.1<br/>                                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 R2<br/>                                                                       |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM \_ SettingData**](cim-settingdata.md)
</dt> </dl>

 

