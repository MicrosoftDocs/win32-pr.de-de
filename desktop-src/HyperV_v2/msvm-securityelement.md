---
description: Stellt die Laufzeitsicherheitseinstellungen eines \_ CIM-Computersystems dar.
ms.assetid: fa4448dc-9353-475f-ac9b-5c50f36360d8
title: Msvm_SecurityElement-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecurityElement
- Msvm_SecurityElement.SystemCreationClassName
- Msvm_SecurityElement.SystemName
- Msvm_SecurityElement.CreationClassName
- Msvm_SecurityElement.Shielded
- Msvm_SecurityElement.EncryptStateAndVmMigrationTrafficEnabled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 36b5301fc47033e200a1b1ffdd39443df241544651faff3a0a4fe8a3a2feee85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118147249"
---
# <a name="msvm_securityelement-class"></a>Msvm \_ SecurityElement-Klasse

Stellt die Laufzeitsicherheitseinstellungen eines [**\_ CIM-Computersystems dar.**](cim-computersystem.md)

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SecurityElement : CIM_EnabledLogicalElement
{
  string  SystemCreationClassName;
  string  SystemName;
  string  CreationClassName;
  boolean Shielded;
  boolean EncryptStateAndVmMigrationTrafficEnabled;
};
```

## <a name="members"></a>Member

Die **Msvm \_ SecurityElement-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ SecurityElement-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)
</dt> </dl>

Der Name der Klasse oder Unterklasse, die bei der Erstellung einer -Instanz verwendet wird. Bei Verwendung mit den anderen Schlüsseleigenschaften dieser Klasse ermöglicht **CreationClassName,** dass alle Instanzen dieser Klasse und deren Unterklassen eindeutig identifiziert werden.

</dd> <dt>

**EncryptStateAndVmMigrationTrafficEnabled**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob der Zustand des virtuellen Computers und der Migrationsdatenverkehr derzeit verschlüsselt sind.

</dd> <dt>

**Geschützt**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob der virtuelle Computer derzeit abgeschirmt ist.

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**CreationClassName**")
</dt> </dl>

Der Name der Erstellungsklasse des Bereichssystems.

</dd> <dt>

**Systemname**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256), [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ System**](cim-system.md).**Name**")
</dt> </dl>

Der Name des Bereichssystems.

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

[**CIM \_ EnabledLogicalElement**](cim-enabledlogicalelement.md)
</dt> </dl>

 

