---
description: Stellt die speicherspezifischen Einstellungen für ein virtuelles System dar.
ms.assetid: 0b3fcd78-7e9a-4a94-ad18-0ca72b3cfd73
title: Msvm_StorageSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_StorageSettingData
- Msvm_StorageSettingData.VirtualProcessorsPerChannel
- Msvm_StorageSettingData.DisableInterruptBatching
- Msvm_StorageSettingData.ThreadCountPerChannel
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 315eb41b5c445d7ce8856f79054e9a227b2a62fc0986419172e519fc65a9ac31
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950109"
---
# <a name="msvm_storagesettingdata-class"></a>Msvm \_ StorageSettingData-Klasse

Stellt die speicherspezifischen Einstellungen für ein virtuelles System dar.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_StorageSettingData : Msvm_SystemComponentSettingData
{
  uint16  VirtualProcessorsPerChannel;
  boolean DisableInterruptBatching;
  uint16  ThreadCountPerChannel;
};
```

## <a name="members"></a>Member

Die **Msvm \_ StorageSettingData-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ StorageSettingData-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**DisableInterruptBatching**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die Interruptbatchverarbeitung deaktiviert werden soll.

Dies ist eine schreibgeschützte Eigenschaft, die jedoch mithilfe der [**ModifySystemComponentSettings-Methode**](msvm-virtualsystemmanagementservice-modifysystemcomponentsettings.md) der Wmi [**Msvm \_ VirtualSystemManagementService-Klasse geändert werden**](msvm-virtualsystemmanagementservice.md) kann.

</dd> <dt>

**ThreadCountPerChannel**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Anzahl der Threads pro Speicherkanal, um E/A zu verarbeiten.

Dies ist eine schreibgeschützte Eigenschaft, die jedoch mithilfe der [**ModifySystemComponentSettings-Methode**](msvm-virtualsystemmanagementservice-modifysystemcomponentsettings.md) der [**Msvm \_ VirtualSystemManagementService-Klasse geändert werden**](msvm-virtualsystemmanagementservice.md) kann.

<dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>**Standard** (0)


</dt> <dd>

Standardverhalten

</dd> <dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>**Niedrig** (1)


</dt> <dd>

Niedrige Anzahl von Threads pro Speicherkanal.

</dd> <dt>

<span id="Medium"></span><span id="medium"></span><span id="MEDIUM"></span>

<span id="Medium"></span><span id="medium"></span><span id="MEDIUM"></span>**Mittel** (2)


</dt> <dd>

Mittlere Anzahl von Threads pro Speicherkanal.

</dd> <dt>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>**Hoch** (3)


</dt> <dd>

Eine hohe Anzahl von Threads pro Speicherkanal.

</dd> </dl>

</dd> <dt>

**VirtualProcessorsPerChannel**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Anzahl der Prozessoren pro Speicherkanal. Die Anzahl der zu öffnenden Kanäle wird von angegeben (Anzahl der logischen Prozessoren auf dem **Host/VirtualProcessorsPerChannel**).

Dies ist eine schreibgeschützte Eigenschaft, die jedoch mithilfe der [**ModifySystemComponentSettings-Methode**](msvm-virtualsystemmanagementservice-modifysystemcomponentsettings.md) der [**Msvm \_ VirtualSystemManagementService-Klasse geändert werden**](msvm-virtualsystemmanagementservice.md) kann.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10 Desktop-Apps, Version 1703 \[\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Msvm \_ SystemComponentSettingData**](msvm-systemcomponentsettingdata.md)
</dt> </dl>

 

 




