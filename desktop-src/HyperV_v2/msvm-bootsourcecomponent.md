---
description: Ordnet die MSVM- \_ bootsourcesettingdata der allgemeinen MSVM \_ virtualsystemsettingdata zu.
ms.assetid: DB2E66F1-CC2C-49FC-96CE-D9DE441AA809
title: Msvm_BootSourceComponent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_BootSourceComponent
- Msvm_BootSourceComponent.GroupComponent
- Msvm_BootSourceComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 44dfe86fa7882b1b20e5b5abbbdaa9d4f37f231f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349058"
---
# <a name="msvm_bootsourcecomponent-class"></a>MSVM \_ bootsourcecomponent-Klasse

Ordnet die [**MSVM- \_ bootsourcesettingdata**](msvm-bootsourcesettingdata.md) der allgemeinen [**MSVM \_ virtualsystemsettingdata**](msvm-virtualsystemsettingdata.md)zu. Diese Klasse wird von der [**CIM- \_ Komponente**](/windows/desktop/CIMWin32Prov/cim-component)abgeleitet.

Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.

## <a name="syntax"></a>Syntax

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_BootSourceComponent : CIM_Component
{
  CIM_ManagedSystemElement REF GroupComponent;
  CIM_ManagedSystemElement REF PartComponent;
};
```

## <a name="members"></a>Member

Die **MSVM \_ bootsourcecomponent** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM \_ bootsourcecomponent** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ ManagedSystemElement**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Verweis auf das übergeordnete Element in der Zuordnung. Diese Eigenschaft wird von der [**CIM- \_ Komponente**](cim-component.md)geerbt.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ ManagedSystemElement**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Verweis auf das untergeordnete Element in der Zuordnung. Diese Eigenschaft wird von der [**CIM- \_ Komponente**](cim-component.md)geerbt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Nur Desktop-Apps Windows 8.1\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 R2 \[ -Desktop-Apps\]<br/>                                                 |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM- \_ Komponente**](cim-component.md)
</dt> <dt>

[**CIM- \_ Komponente**](/windows/desktop/CIMWin32Prov/cim-component)
</dt> <dt>

[**MSVM \_ bootsourcesettingdata**](msvm-bootsourcesettingdata.md)
</dt> <dt>

[**MSVM \_ virtualsystemsettingdata**](msvm-virtualsystemsettingdata.md)
</dt> </dl>

 

