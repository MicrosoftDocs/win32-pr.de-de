---
description: Definiert die Zuordnung zwischen einem Ethernet-Switch und einer Switch-Ressource.
ms.assetid: fb29f4cb-50c4-4865-b267-21ff99bb4a8b
title: Msvm_EthernetSwitchInfo-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchInfo
- Msvm_EthernetSwitchInfo.Antecedent
- Msvm_EthernetSwitchInfo.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1106e0930716572b10a95846865d8f90aa991cc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103961013"
---
# <a name="msvm_ethernetswitchinfo-class"></a>MSVM \_ ethernetzwitchinfo-Klasse

Definiert die Zuordnung zwischen einem Ethernet-Switch und einer Switch-Ressource.

Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetSwitchInfo : CIM_Dependency
{
  Msvm_VirtualEthernetSwitch REF Antecedent;
  Msvm_EthernetSwitchData    REF Dependent;
};
```

## <a name="members"></a>Member

Die **MSVM \_ ethernetzwitchinfo** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM-Klasse " \_ ethernetzwitchinfo** " verfügt über diese Eigenschaften.

<dl> <dt>

**Vorgänger**
</dt> <dd> <dl> <dt>

Datentyp: **MSVM \_ virtualethernwitch**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger")
</dt> </dl>

Ein Verweis auf die Klasse " [**MSVM \_ virtualethernwitch**](msvm-virtualethernetswitch.md) ", die das Hostingsystem darstellt. Diese Eigenschaft wird von der [**CIM- \_ Abhängigkeit**](/windows/desktop/CIMWin32Prov/cim-dependency)abgeleitet.

</dd> <dt>

**Dependent**
</dt> <dd> <dl> <dt>

Datentyp: **MSVM \_ ethernetzwitchdata**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")
</dt> </dl>

Ein Verweis auf die [**MSVM-Klasse " \_ ethernetzwitchdata**](msvm-ethernetswitchdata.md) ", die die Switch-Ressource darstellt. Diese Eigenschaft wird von der [**CIM- \_ Abhängigkeit**](/windows/desktop/CIMWin32Prov/cim-dependency)abgeleitet.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

