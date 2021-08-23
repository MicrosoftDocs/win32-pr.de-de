---
description: Eine Zuordnung zwischen einer Instanz der Msvm \_ EthernetSwitchPort-Klasse und einer Instanz der Msvm \_ EthernetPortData-Klasse, die Daten darstellt, die von einer Switcherweiterung über den Port gesammelt wurden.
ms.assetid: 08677914-af09-47b7-9d4d-406696e1f504
title: Msvm_EthernetPortInfo-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetPortInfo
- Msvm_EthernetPortInfo.Antecedent
- Msvm_EthernetPortInfo.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 3ef8f8f4ab7191400cfead94d20c4f601b97e48d46ee160d31c7b26b8e567b92
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119524890"
---
# <a name="msvm_ethernetportinfo-class"></a>Msvm \_ EthernetPortInfo-Klasse

Eine Zuordnung zwischen einer Instanz der [**Msvm \_ EthernetSwitchPort-Klasse**](msvm-ethernetswitchport.md) und einer Instanz der [**Msvm \_ EthernetPortData-Klasse,**](msvm-ethernetportdata.md) die Daten darstellt, die von einer Switcherweiterung über den Port gesammelt wurden.

Die folgende Syntax ist Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetPortInfo : CIM_Dependency
{
  Msvm_EthernetSwitchPort REF Antecedent;
  Msvm_EthernetPortData   REF Dependent;
};
```

## <a name="members"></a>Member

Die **Msvm \_ EthernetPortInfo-Klasse** verfügt über folgende Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ EthernetPortInfo-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Vorläufer**
</dt> <dd> <dl> <dt>

Datentyp: **Msvm \_ EthernetSwitchPort**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Außerkraftsetzung**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ Dependency.Antecedent")
</dt> </dl>

Eine Instanz der [**Msvm \_ EthernetSwitchPort-Klasse,**](msvm-ethernetswitchport.md) die den Switchport darstellt.

</dd> <dt>

**Abhängigen**
</dt> <dd> <dl> <dt>

Datentyp: **Msvm \_ EthernetPortData**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Überschreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ Dependency.Dependent")
</dt> </dl>

Eine Instanz der [**Msvm \_ EthernetPortData-Klasse,**](msvm-ethernetportdata.md) die die Portdaten darstellt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

