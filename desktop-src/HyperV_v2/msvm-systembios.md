---
description: Wird verwendet, um dem BIOS eine virtuelle Maschine zuzuordnen.
ms.assetid: 494E9D9F-64D5-49D5-A6C7-ABE469ABA4CA
title: Msvm_SystemBIOS-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SystemBIOS
- Msvm_SystemBIOS.GroupComponent
- Msvm_SystemBIOS.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7e1ad159a3ac0b86abd8b01e5c38105590ea8db0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128421"
---
# <a name="msvm_systembios-class"></a>MSVM- \_ Systembios-Klasse

Wird verwendet, um dem BIOS eine virtuelle Maschine zuzuordnen.

Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SystemBIOS : CIM_SystemBIOS
{
  CIM_ComputerSystem REF GroupComponent;
  Msvm_BIOSElement   REF PartComponent;
};
```

## <a name="members"></a>Member

Die **MSVM- \_ Systembios** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM- \_ Systembios** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Datentyp: **[ **CIM \_ Computersystem**](msvm-computersystem.md)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Der virtuelle Computer, der über das BIOS gestartet wird.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Datentyp: **[ **MSVM \_ bioselements**](msvm-bioselement.md)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: über [**Schreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

Das BIOS, das dem virtuellen Computer zugeordnet ist.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Der Zugriff auf die **MSVM- \_ Systembios** -Klasse kann durch die UAC-Filterung eingeschränkt werden. Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[**CIM- \_ Systembios**](cim-systembios.md)
</dt> <dt>

[BIOS-Klassen](bios-classes.md)
</dt> </dl>

 

