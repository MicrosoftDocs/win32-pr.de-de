---
description: Stellt den konfigurierten Status des TPM-Geräts dar.
ms.assetid: 948ccb47-3626-48f1-b18f-ef1d05978b21
title: Msvm_TPMSettingData-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TPMSettingData
- Msvm_TPMSettingData.Shielded
- Msvm_TPMSettingData.DataProtected
- Msvm_TPMSettingData.EnabledState
- Msvm_TPMSettingData.KeyProtector
- Msvm_TPMSettingData.LastKnownGoodKeyProtector
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8a14f50f01212129ed34cc7e45ee28facbdb991f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527668"
---
# <a name="msvm_tpmsettingdata-class"></a>MSVM \_ tpmsettingdata-Klasse

Stellt den konfigurierten Status des TPM-Geräts dar.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_TPMSettingData : CIM_ResourceAllocationSettingData
{
  boolean Shielded = FALSE;
  boolean DataProtected = FALSE;
  uint16  EnabledState = 3;
  uint8   KeyProtector[];
  uint8   LastKnownGoodKeyProtector[];
};
```

## <a name="members"></a>Member

Die **MSVM \_ tpmsettingdata** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM \_ tpmsettingdata** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Dataprotected**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **erforderlich**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

" **true** ", um eine Richtlinie zum Schutz der Daten eines virtuellen Computers festzulegen. andernfalls **false**. Ein neu erstelltes TPM ist deaktiviert, sodass der anfängliche Datenschutz Status " **false**" lautet.

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **erforderlich**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Der aktivierte und deaktivierte Status eines Elements. Der Standardwert ist **deaktiviert**.

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**Aktiviert** (2)


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Deaktiviert** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**Keyprotector**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**erforderlich**](/windows/desktop/WmiSdk/standard-qualifiers), **octetstring**
</dt> </dl>

Die Schlüssel Schutzvorrichtung von Host-Überwachungsdienst Client.

</dd> <dt>

**Lastknowngoodkeyprotector**
</dt> <dd> <dl> <dt>

Datentyp: **Uint8** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**erforderlich**](/windows/desktop/WmiSdk/standard-qualifiers), **octetstring**
</dt> </dl>

Die letzte bekannte gute Schlüssel Schutzvorrichtung hat beim letzten VM-Start erfolgreich den TPM-Gerätestatus verschlüsselt.

Diese Eigenschaft ist für den WMI-Client schreibgeschützt und kann nur vom TPM-Gerät der VM geändert werden.

</dd> <dt>

**Geschützt**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher** Wert
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **erforderlich**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

**true** , um eine Richtlinie zu definieren, die eine virtuelle Maschine schützt. andernfalls **false**. Ein neu erstelltes TPM ist deaktiviert, sodass der anfängliche Schutzstatus " **false**" lautet.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 10 \[ -Desktop-Apps\]<br/>                                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                          |
| Ende des Supports (Client)<br/>    | Windows 10<br/>                                                                                   |
| Ende des Supports (Server)<br/>    | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM \_ resourcezubesettingdata**](cim-resourceallocationsettingdata.md)
</dt> </dl>

 

