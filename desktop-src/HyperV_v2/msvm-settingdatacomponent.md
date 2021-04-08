---
description: Richten Sie eine Beziehung zwischen einer Instanz der MSVM- \_ emulatedethernetportsettingdata-Klasse oder der MSVM \_ syntheticethernetportsettingdata-Klasse mit einer Instanz der MSVM \_ guestnetworkadapterconfiguration-Klasse ein.
ms.assetid: 82262e67-1e72-4bad-974e-f18d00a94c3d
title: Msvm_SettingDataComponent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SettingDataComponent
- Msvm_SettingDataComponent.GroupComponent
- Msvm_SettingDataComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 18ed2d4f37b88509a7517861a9b9d842be86bd97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960070"
---
# <a name="msvm_settingdatacomponent-class"></a>MSVM \_ settingdatacomponent-Klasse

Richten Sie eine Beziehung zwischen einer Instanz der [**MSVM- \_ emulatedethernetportsettingdata**](msvm-emulatedethernetportsettingdata.md) -Klasse oder der [**MSVM \_ syntheticethernetportsettingdata**](msvm-syntheticethernetportsettingdata.md) -Klasse mit einer Instanz der [**MSVM \_ guestnetworkadapterconfiguration**](msvm-guestnetworkadapterconfiguration.md) -Klasse ein.

Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SettingDataComponent : CIM_Component
{
  CIM_ResourceAllocationSettingData     REF GroupComponent;
  Msvm_GuestNetworkAdapterConfiguration REF PartComponent;
};
```

## <a name="members"></a>Member

Die **MSVM \_ settingdatacomponent** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM \_ settingdatacomponent** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Datentyp: **[ **CIM \_ resourcezubesettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Ein Verweis auf eine Instanz der [**MSVM-Klasse \_ emuatedethernetportsettingdata**](msvm-emulatedethernetportsettingdata.md) oder [**MSVM \_ syntheticethernetportsettingdata**](msvm-syntheticethernetportsettingdata.md) , die einen Ethernet-Port darstellt.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Datentyp: **[ **MSVM \_ guestnetworkadapterconfiguration**](msvm-guestnetworkadapterconfiguration.md)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

Ein Verweis auf eine Instanz der [**MSVM \_ guestnetworkadapterconfiguration**](msvm-guestnetworkadapterconfiguration.md) -Klasse, die die Konfiguration eines Gastnetzwerk Adapters darstellt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

