---
description: Stellt den konfigurierten Zustand des TPM-Geräts dar.
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
ms.openlocfilehash: f25cd57e1f3cd6ebf015009af176b3bcc68c1d271836c5bb548b9358e9007086
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119899120"
---
# <a name="msvm_tpmsettingdata-class"></a>Msvm \_ TPMSettingData-Klasse

Stellt den konfigurierten Zustand des TPM-Geräts dar.

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

Die **Msvm \_ TPMSettingData-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ TPMSettingData-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**DataProtected**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Erforderlich**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

**TRUE** zum Festlegen einer Richtlinie zum Schutz der Daten eines virtuellen Computers; andernfalls **FALSE.** Ein neu erstelltes TPM ist deaktiviert, sodass der anfängliche Datenschutzstatus false **ist.**

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Erforderlich**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Der aktivierte und deaktivierte Zustände eines Elements. Der Standardwert ist **Deaktiviert.**

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**Aktiviert** (2)


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Deaktiviert** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**KeyProtector**
</dt> <dd> <dl> <dt>

Datentyp: **uint8 array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Erforderlich,**](/windows/desktop/WmiSdk/standard-qualifiers) **OctetString**
</dt> </dl>

Die Schlüsselschutzvorrichtung des Host-Wächterdienstclients.

</dd> <dt>

**LastKnownGoodKeyProtector**
</dt> <dd> <dl> <dt>

Datentyp: **uint8 array**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Erforderlich,**](/windows/desktop/WmiSdk/standard-qualifiers) **OctetString**
</dt> </dl>

Die letzte bekannte gute Schlüsselschutzvorrichtung hat den TPM-Gerätestatus beim letzten VM-Start erfolgreich verschlüsselt.

Diese Eigenschaft ist schreibgeschützt für den WMI-Client und kann nur vom TPM-Gerät des virtuellen Computers geändert werden.

</dd> <dt>

**Geschützt**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [ **Erforderlich**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

**TRUE,** um eine Richtlinie zu definieren, die einen virtuellen Computer schützt; andernfalls **FALSE.** Ein neu erstelltes TPM ist deaktiviert, sodass der anfängliche Schutzstatus false **ist.**

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 10 Nur Desktop-Apps\]<br/>                                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2016<br/>                                                                          |
| Ende des Supports (Client)<br/>    | Windows 10<br/>                                                                                   |
| Ende des Supports (Server)<br/>    | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md)
</dt> </dl>

 

