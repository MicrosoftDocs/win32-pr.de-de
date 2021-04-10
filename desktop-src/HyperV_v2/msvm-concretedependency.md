---
description: Definiert die Zuordnung zwischen einer installierten Ethernet-Switcherweiterung und einer Ethernet-Switcherweiterung.
ms.assetid: 306658ed-03a4-49fa-8704-f4b83a4bdd4f
title: Msvm_ConcreteDependency-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ConcreteDependency
- Msvm_ConcreteDependency.Antecedent
- Msvm_ConcreteDependency.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c74a8431b03389a106cd127933a2c78b842385f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215375"
---
# <a name="msvm_concretedependency-class"></a>MSVM- \_ Klasse "concretedepend"

Definiert die Zuordnung zwischen einer installierten Ethernet-Switcherweiterung und einer Ethernet-Switcherweiterung.

Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ConcreteDependency : CIM_ConcreteDependency
{
  Msvm_InstalledEthernetSwitchExtension REF Antecedent;
  Msvm_EthernetSwitchExtension          REF Dependent;
};
```

## <a name="members"></a>Member

Die **MSVM-Klasse " \_ concretedepend** " verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM-Klasse " \_ concretedepend** " verfügt über diese Eigenschaften.

<dl> <dt>

**Vorgänger**
</dt> <dd> <dl> <dt>

Datentyp: **[ **MSVM \_ installedethernetzwitchextension**](msvm-installedethernetswitchextension.md)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger")
</dt> </dl>

Ein Verweis auf eine Instanz der [**MSVM \_ installedethernetswitchextension**](msvm-installedethernetswitchextension.md) -Klasse, die eine Komponente für eine virtuelle Ethernet-Switcherweiterung darstellt, die auf dem System installiert ist.

</dd> <dt>

**Dependent**
</dt> <dd> <dl> <dt>

Datentyp: **[ **MSVM \_ ethernetungwitchextension**](msvm-ethernetswitchextension.md)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")
</dt> </dl>

Ein Verweis auf eine Instanz der [**MSVM-Klasse \_ ethernetswitchextension**](msvm-ethernetswitchextension.md) , die das Vorkommen des Vorgängers darstellt, der an einen bestimmten virtuellen Ethernet- **Switch gebunden ist** .

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

