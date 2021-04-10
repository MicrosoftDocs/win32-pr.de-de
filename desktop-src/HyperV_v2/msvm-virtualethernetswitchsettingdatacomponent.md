---
description: Eine Zuordnung, die verwendet wird, um &\# 0034; Teil&\# 0034; Beziehungen zwischen einer Instanz von MSVM \_ virtualethernetzwitchsettingdata und einer oder mehreren Instanzen von MSVM \_ ethernettionwitchfeaturesettingdata herzustellen.
ms.assetid: b3adac33-056e-4f39-8022-5d9ef78370e9
title: Msvm_VirtualEthernetSwitchSettingDataComponent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchSettingDataComponent
- Msvm_VirtualEthernetSwitchSettingDataComponent.GroupComponent
- Msvm_VirtualEthernetSwitchSettingDataComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8fa53514c5db3128e13f0504bb883cb802021c20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215368"
---
# <a name="msvm_virtualethernetswitchsettingdatacomponent-class"></a>MSVM \_ virtualethernetzwitchsettingdatacomponent-Klasse

Eine Zuordnung, die verwendet wird, um Beziehungen zwischen einer Instanz von [**MSVM \_ virtualethernettionwitchsettingdata**](msvm-virtualethernetswitchsettingdata.md) und einer oder mehreren Instanzen von [**MSVM \_ ethernettionwitchfeaturesettingdata**](msvm-ethernetswitchfeaturesettingdata.md)herzustellen.

Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualEthernetSwitchSettingDataComponent : CIM_Component
{
  Msvm_VirtualEthernetSwitchSettingData REF GroupComponent;
  Msvm_EthernetSwitchFeatureSettingData REF PartComponent;
};
```

## <a name="members"></a>Member

Die **MSVM \_ virtualethernetzwitchsettingdatacomponent** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM \_ virtualethernetzwitchsettingdatacomponent** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Datentyp: **MSVM \_ virtualethernetungwitchsettingdata**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Verweis auf eine Instanz der [**MSVM \_ virtualethernetswitchsettingdata**](msvm-virtualethernetswitchsettingdata.md) -Klasse, die einen Ethernet-Port darstellt.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Datentyp: **MSVM \_ ethernetzwitchfeaturesettingdata**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

Verweis auf eine Instanz der [**MSVM-Klasse " \_ ethernetzwitchfeaturesettingdata**](msvm-ethernetswitchfeaturesettingdata.md) ", die die auf den Schalter angewendeten Einstellungen darstellt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

