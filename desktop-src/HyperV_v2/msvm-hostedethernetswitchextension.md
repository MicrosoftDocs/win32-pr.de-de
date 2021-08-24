---
description: Ordnet den derzeit an ihn gebundenen Erweiterungen einen virtuellen Ethernet-Switch zu.
ms.assetid: d8c87fa2-6859-49ed-abd5-32a836b00e5a
title: Msvm_HostedEthernetSwitchExtension-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_HostedEthernetSwitchExtension
- Msvm_HostedEthernetSwitchExtension.Antecedent
- Msvm_HostedEthernetSwitchExtension.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: dda28d4d5893f05ef067016da771b8dc510ba5588dd4f25ed89dfe7c4a8aa2fe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119522980"
---
# <a name="msvm_hostedethernetswitchextension-class"></a>Msvm \_ HostedEthernetSwitchExtension-Klasse

Ordnet den derzeit an ihn gebundenen Erweiterungen einen virtuellen Ethernet-Switch zu.

Die folgende Syntax ist Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_HostedEthernetSwitchExtension : CIM_HostedDependency
{
  Msvm_VirtualEthernetSwitch   REF Antecedent;
  Msvm_EthernetSwitchExtension REF Dependent;
};
```

## <a name="members"></a>Member

Die **Msvm \_ HostedEthernetSwitchExtension-Klasse** verfügt über folgende Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ HostedEthernetSwitchExtension-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Vorläufer**
</dt> <dd> <dl> <dt>

Datentyp: **[ **Msvm \_ VirtualEthernetSwitch**](msvm-virtualethernetswitch.md)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schlüssel,**](/windows/desktop/WmiSdk/key-qualifier) [**Außerkraftsetzung**](/windows/desktop/WmiSdk/standard-qualifiers) ("Vorgänger"), [**Min(**](/windows/desktop/WmiSdk/standard-qualifiers) 1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Ein Verweis auf eine Instanz der [**Msvm \_ VirtualEthernetSwitch-Klasse,**](msvm-virtualethernetswitch.md) die den virtuellen Switch darstellt.

</dd> <dt>

**Abhängigen**
</dt> <dd> <dl> <dt>

Datentyp: **[ **Msvm \_ EthernetSwitchExtension**](msvm-ethernetswitchextension.md)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schlüssel,**](/windows/desktop/WmiSdk/key-qualifier) [**Außerkraftsetzung**](/windows/desktop/WmiSdk/standard-qualifiers) ("abhängig"), [**Schwach**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Ein Verweis auf eine Instanz der [**Msvm \_ EthernetSwitchExtension-Klasse,**](msvm-ethernetswitchextension.md) die die an den virtuellen Switch gebundene Switcherweiterungsinstanz darstellt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

