---
description: Richten Sie eine Beziehung zwischen einer Instanz der Msvm \_ EmulatedEthernetPortSettingData- oder Msvm \_ SyntheticEthernetPortSettingData-Klasse mit einer Instanz der Msvm \_ GuestNetworkAdapterConfiguration-Klasse ein.
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
ms.openlocfilehash: c96ad2d24291226934e50b338f2a0a4d77e9d966d2a821b73ad38d671b50fa04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950479"
---
# <a name="msvm_settingdatacomponent-class"></a>Msvm \_ SettingDataComponent-Klasse

Richten Sie eine Beziehung zwischen einer Instanz der [**Msvm \_ EmulatedEthernetPortSettingData-**](msvm-emulatedethernetportsettingdata.md) oder [**Msvm \_ SyntheticEthernetPortSettingData-Klasse**](msvm-syntheticethernetportsettingdata.md) mit einer Instanz der [**Msvm \_ GuestNetworkAdapterConfiguration-Klasse**](msvm-guestnetworkadapterconfiguration.md) ein.

Die folgende Syntax ist Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

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

Die **Msvm \_ SettingDataComponent-Klasse** verfügt über folgende Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ SettingDataComponent-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Datentyp: **[ **CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schlüssel,**](/windows/desktop/WmiSdk/key-qualifier) [**Außerkraftsetzung**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Aggregieren**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Ein Verweis auf eine Instanz der [**Msvm \_ EmulatedEthernetPortSettingData-**](msvm-emulatedethernetportsettingdata.md) oder [**Msvm \_ SyntheticEthernetPortSettingData-Klasse,**](msvm-syntheticethernetportsettingdata.md) die einen Ethernet-Port darstellt.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Datentyp: **[ **Msvm \_ GuestNetworkAdapterConfiguration**](msvm-guestnetworkadapterconfiguration.md)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schlüssel**](/windows/desktop/WmiSdk/key-qualifier), [**Außerkraftsetzung**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

Ein Verweis auf eine Instanz der [**Msvm \_ GuestNetworkAdapterConfiguration-Klasse,**](msvm-guestnetworkadapterconfiguration.md) die eine Konfiguration eines Gastnetzwerkadapters darstellt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

