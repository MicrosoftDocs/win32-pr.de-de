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
ms.openlocfilehash: a510c4195c538ab9735e7544acec2c88beeaa1de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869280"
---
# <a name="cim_vlanendpointsettingdata-class"></a>CIM- \_ vlanendpointsettingdata-Klasse

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

Die **CIM- \_ vlanendpointsettingdata** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM- \_ vlanendpointsettingdata** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**AccessVLAN**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ vlanendpoint**](cim-vlanendpoint.md)".**Operationalendpointmode**")
</dt> </dl>

Das Access-VLAN für den Endpunkt.

</dd> <dt>

**Defaultvlan**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ vlanendpoint**](cim-vlanendpoint.md)".**Operationalendpointmode**")
</dt> </dl>

Der Standardwert für das native VLAN auf dem trunk Endpunkt.

> [!Note]  
> Diese Eigenschaft wird nur verwendet, wenn der VLAN-Endpunkt im trunkingmodus betrieben wird, der in der **operationalendpointmode** -Eigenschaft angegeben ist.

 

</dd> <dt>

**Nativevlan**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ vlanendpoint**](cim-vlanendpoint.md)".**Operationalendpointmode**")
</dt> </dl>

Die VLAN-ID, die verwendet wird, um nicht markierten Datenverkehr zu markieren, der auf dem trunk Endpunkt empfangen wurde

> [!Note]  
> Diese Eigenschaft wird nur verwendet, wenn der VLAN-Endpunkt im trunkingmodus betrieben wird, der in der **switchendpointmode** -Eigenschaft angegeben ist.

 

</dd> <dt>

**Pruneeligiblevlanlist**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16** Array
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ vlanendpoint**](cim-vlanendpoint.md)".**Operationalendpointmode**")
</dt> </dl>

Ein Array, das IDs von VLANs enthält, die vom System aus dem trunk Endpunkt entfernt werden können.

> [!Note]  
> Diese Eigenschaft wird nur verwendet, wenn der VLAN-Endpunkt im trunkingmodus betrieben wird, der in der **operationalendpointmode** -Eigenschaft angegeben ist.

 

</dd> <dt>

**TrunkedVLANList**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16** Array
</dt> <dt>

Zugriffstyp: Lesen/Schreiben
</dt> <dt>

Qualifizierer: [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ vlanendpoint**](cim-vlanendpoint.md)".**Operationalendpointmode**")
</dt> </dl>

Ein Array, das IDs von VLAN-Endpunkten mit aktiviertem Trunking enthält.

> [!Note]  
> Diese Eigenschaft wird nur verwendet, wenn der VLAN-Endpunkt im trunkingmodus betrieben wird, der in der **operationalendpointmode** -Eigenschaft angegeben ist.

 

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8.1<br/>                                                                                  |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012 R2<br/>                                                                       |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM- \_ SettingData**](cim-settingdata.md)
</dt> </dl>

 

