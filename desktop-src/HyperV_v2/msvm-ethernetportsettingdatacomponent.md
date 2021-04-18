---
description: Eine Zuordnung, die verwendet wird, um &\# 0034; Teil&\# 0034; Beziehungen zwischen einer Instanz von MSVM \_ ethernetportzuordcationsettingdata und einer oder mehreren Instanzen von MSVM \_ ethernettionwitchfeaturesettingdata herzustellen.
ms.assetid: fab15342-a134-4d4a-9668-1272041614b9
title: Msvm_EthernetPortSettingDataComponent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetPortSettingDataComponent
- Msvm_EthernetPortSettingDataComponent.GroupComponent
- Msvm_EthernetPortSettingDataComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1c00c056bd5095d945af12fde3556d92b9a2d7ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347612"
---
# <a name="msvm_ethernetportsettingdatacomponent-class"></a>MSVM \_ ethernetportsettingdatacomponent-Klasse

Eine Zuordnung, die verwendet wird, um Beziehungen zwischen einer Instanz eines [**MSVM- \_ ethernetportzuordnungsdateils**](msvm-ethernetportallocationsettingdata.md) und einer oder mehreren Instanzen eines [**MSVM- \_ ethernetzwitchfeaturesettingdata**](msvm-ethernetswitchfeaturesettingdata.md)herzustellen.

Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetPortSettingDataComponent : CIM_Component
{
  Msvm_EthernetPortAllocationSettingData    REF GroupComponent;
  Msvm_EthernetSwitchPortFeatureSettingData REF PartComponent;
};
```

## <a name="members"></a>Member

Die **MSVM-Klasse " \_ ethernetportsettingdatacomponent** " verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM-Klasse " \_ ethernetportsettingdatacomponent** " verfügt über diese Eigenschaften.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Datentyp: **[ **MSVM \_ ethernetportzugecationsettingdata**](msvm-ethernetportallocationsettingdata.md)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Ein Verweis auf eine Instanz der [**MSVM-Klasse " \_ ethernetportzuweisung**](msvm-ethernetportallocationsettingdata.md) ", die den Ethernet-Port darstellt.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Datentyp: **[ **MSVM \_ ethernetzwitchportfeaturesettingdata**](msvm-ethernetswitchportfeaturesettingdata.md)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

Ein Verweis auf eine Instanz der [**MSVM-Klasse " \_ ethernetzwitchportfeaturesettingdata**](msvm-ethernetswitchportfeaturesettingdata.md) ", die die auf den Port angewendeten Funktionseinstellungen darstellt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

