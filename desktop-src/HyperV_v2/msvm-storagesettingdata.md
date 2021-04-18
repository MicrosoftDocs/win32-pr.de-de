---
description: Stellt die Speicher spezifischen Einstellungen für ein virtuelles System dar.
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
ms.openlocfilehash: db061d048ce45a4d6fa076a5b0367e794cdf16e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352389"
---
# <a name="msvm_storagesettingdata-class"></a>MSVM \_ storagesettingdata-Klasse

Stellt die Speicher spezifischen Einstellungen für ein virtuelles System dar.

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

Die Klasse " **MSVM \_ storagesettingdata** " enthält diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM \_ storagesettingdata** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Disableinterruptbatching**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob die Unterbrechung der Batch Verarbeitung deaktiviert werden soll.

Dabei handelt es sich um eine schreibgeschützte Eigenschaft, die jedoch mithilfe der [**modifysystemcomponentsettings**](msvm-virtualsystemmanagementservice-modifysystemcomponentsettings.md) -Methode der WMI-Klasse " [**\_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md) " geändert werden kann.

</dd> <dt>

**Threadfactperchannel**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Anzahl der Threads pro Speicherkanal für die Verarbeitung von e/a.

Dabei handelt es sich um eine schreibgeschützte Eigenschaft, die jedoch mithilfe der [**modifysystemcomponentsettings**](msvm-virtualsystemmanagementservice-modifysystemcomponentsettings.md) -Methode der [**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md) -Klasse geändert werden kann.

<dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>**Standard** (0)


</dt> <dd>

Standardverhalten

</dd> <dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>**Niedrig** (1)


</dt> <dd>

Geringe Anzahl von Threads pro Speicherkanal.

</dd> <dt>

<span id="Medium"></span><span id="medium"></span><span id="MEDIUM"></span>

<span id="Medium"></span><span id="medium"></span><span id="MEDIUM"></span>**Mittel** (2)


</dt> <dd>

Mittlere Anzahl von Threads pro Speicherkanal.

</dd> <dt>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>**Hoch** (3)


</dt> <dd>

Hohe Anzahl von Threads pro Speicherkanal.

</dd> </dl>

</dd> <dt>

**Virtualprocessorsperchannel**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Anzahl der Prozessoren pro Speicherkanal. Die Anzahl der zu öffnenden Kanäle wird durch angegeben (Anzahl der logischen Prozessoren auf dem Host/**virtualprocessorsperchannel**).

Dabei handelt es sich um eine schreibgeschützte Eigenschaft, die jedoch mithilfe der [**modifysystemcomponentsettings**](msvm-virtualsystemmanagementservice-modifysystemcomponentsettings.md) -Methode der [**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md) -Klasse geändert werden kann.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 10, Version 1703, \[ nur Desktop-Apps\]<br/>                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MSVM \_ systemcomponentsettingdata**](msvm-systemcomponentsettingdata.md)
</dt> </dl>

 

 




