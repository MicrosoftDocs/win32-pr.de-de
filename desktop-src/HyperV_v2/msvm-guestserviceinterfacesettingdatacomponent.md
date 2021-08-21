---
description: Zuordnungsklasse zwischen einer Gastdienstschnittstellenkomponente und der Gastdienstressource.
ms.assetid: 4c16c3ab-4137-40ab-be2e-f385d8e36a41
title: Msvm_GuestServiceInterfaceSettingDataComponent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestServiceInterfaceSettingDataComponent
- Msvm_GuestServiceInterfaceSettingDataComponent.GroupComponent
- Msvm_GuestServiceInterfaceSettingDataComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cc9f988fcf5c7e4ee1c40f58360a2916b3bc8d82a833fdb69e267d4f27a1aab9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118147796"
---
# <a name="msvm_guestserviceinterfacesettingdatacomponent-class"></a>Msvm \_ GuestServiceInterfaceSettingDataComponent-Klasse

Zuordnungsklasse zwischen einer Gastdienstschnittstellenkomponente und der Gastdienstressource.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GuestServiceInterfaceSettingDataComponent : CIM_Component
{
  Msvm_GuestServiceInterfaceComponentSettingData REF GroupComponent;
  CIM_SettingData                                REF PartComponent;
};
```

## <a name="members"></a>Member

Die **Msvm \_ GuestServiceInterfaceSettingDataComponent-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ GuestServiceInterfaceSettingDataComponent-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Datentyp: **Msvm \_ GuestServiceInterfaceComponentSettingData**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schlüssel**](/windows/desktop/WmiSdk/key-qualifier), [**Außerkraftsetzung**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")
</dt> </dl>

Eine [**Msvm \_ GuestServiceInterfaceComponentSettingData,**](msvm-guestserviceinterfacecomponentsettingdata.md) die auf die Komponente der Gastdienstschnittstelle verweist.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ SettingData**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schlüssel**](/windows/desktop/WmiSdk/key-qualifier), [**Außerkraftsetzung**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

Eine [**\_ CIM-EinstellungSdaten,**](cim-settingdata.md) die auf die Gastdienstressource verweist.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10 Nur Desktop-Apps\]<br/>                                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Root-Virtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_CIM-Komponente**](cim-component.md)
</dt> </dl>

 

