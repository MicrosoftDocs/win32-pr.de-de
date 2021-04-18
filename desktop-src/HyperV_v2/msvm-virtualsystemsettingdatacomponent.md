---
description: Eine generische Zuordnung, die verwendet wird, um einen Teil der Beziehungen zwischen einer Instanz von CIM \_ virtualsystemsettingdata und einer oder mehreren Instanzen von CIM \_ resourcezucationsettingdata herzustellen.
ms.assetid: 936B41E7-1B3B-4A7B-86F0-E2F4497CE610
title: Msvm_VirtualSystemSettingDataComponent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemSettingDataComponent
- Msvm_VirtualSystemSettingDataComponent.GroupComponent
- Msvm_VirtualSystemSettingDataComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: bfff3981d6fdb9fdb0368fa887c559026fc10af3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106341181"
---
# <a name="msvm_virtualsystemsettingdatacomponent-class"></a>MSVM \_ virtualsystemsettingdatacomponent-Klasse

Eine generische Zuordnung, die verwendet wird, um Beziehungen zwischen einer Instanz von [**CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85)) und einer oder mehreren Instanzen von [**CIM \_ resourcezucationsettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)herzustellen.

Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemSettingDataComponent : CIM_VirtualSystemSettingDataComponent
{
  CIM_VirtualSystemSettingData      REF GroupComponent;
  CIM_ResourceAllocationSettingData REF PartComponent;
};
```

## <a name="members"></a>Member

Die **MSVM \_ virtualsystemsettingdatacomponent** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM \_ virtualsystemsettingdatacomponent** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Datentyp: **[ **CIM \_ virtualsystemsettingdata**](/previous-versions//cc136954(v=vs.85))**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **außer Kraft** setzung, **Min** (1), **Max** (1)
</dt> </dl>

Das übergeordnete Element in der Zuordnung. Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdatacomponent**](/previous-versions//cc150674(v=vs.85))geerbt.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Datentyp: **[ **CIM \_ resourcezubesettingdata**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Das untergeordnete-Element in der Zuordnung. Diese Eigenschaft wird von [**CIM \_ virtualsystemsettingdatacomponent**](/previous-versions//cc150674(v=vs.85))geerbt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der Zugriff auf die **MSVM \_ virtualsystemsettingdatacomponent** -Klasse kann durch die UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM \_ virtualsystemsettingdatacomponent**](cim-virtualsystemsettingdatacomponent.md)
</dt> <dt>

[**CIM \_ virtualsystemsettingdatacomponent**](/previous-versions//cc150674(v=vs.85))
</dt> <dt>

[Klassen des virtuellen Systems](virtual-system-classes.md)
</dt> </dl>

 

