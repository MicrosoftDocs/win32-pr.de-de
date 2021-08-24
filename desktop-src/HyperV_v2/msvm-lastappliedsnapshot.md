---
description: Stellt eine Zuordnung zwischen einem virtuellen System und den Einstellungsdaten der Momentaufnahme dar, die zuletzt auf das virtuelle System angewendet wurde.
ms.assetid: 9231b441-20c4-468b-905f-5baabc32a8cc
title: Msvm_LastAppliedSnapshot-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_LastAppliedSnapshot
- Msvm_LastAppliedSnapshot.Antecedent
- Msvm_LastAppliedSnapshot.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e34260e0bfe77b847437e9b3d49794334b3897d8425981fecb2032098e24fa7a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119521920"
---
# <a name="msvm_lastappliedsnapshot-class"></a>Msvm \_ LastAppliedSnapshot-Klasse

Stellt eine Zuordnung zwischen einem virtuellen System und den Einstellungsdaten der Momentaufnahme dar, die zuletzt auf das virtuelle System angewendet wurde.

Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_LastAppliedSnapshot : CIM_LastAppliedSnapshot
{
  CIM_VirtualSystemSettingData REF Antecedent;
  CIM_ComputerSystem           REF Dependent;
};
```

## <a name="members"></a>Member

Die **Msvm \_ LastAppliedSnapshot-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ LastAppliedSnapshot-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Vorläufer**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ VirtualSystemSettingData**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Überschreiben,** **Min** ( 0 ), **Max** ( 1 )
</dt> </dl>

Verweis auf eine Instanz der [**Msvm \_ VirtualSystemSettingData-Klasse,**](msvm-virtualsystemsettingdata.md) die die Momentaufnahme des virtuellen Systems darstellt, die zuletzt auf das virtuelle System angewendet wurde. Diese Eigenschaft wird von der **CIM-Abhängigkeit \_ geerbt.**

</dd> <dt>

**Abhängigen**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ ComputerSystem**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: **Überschreiben,** **Min** ( 0 ), **Max** ( 1 )
</dt> </dl>

Verweis auf eine Instanz der [**Msvm \_ ComputerSystem-Klasse,**](msvm-computersystem.md) die das virtuelle System darstellt, auf das die von der **Antecedent-Eigenschaft** dargestellte virtuelle Systemmomentaufnahme zuletzt angewendet wurde. Diese Eigenschaft wird von der **CIM-Abhängigkeit \_ geerbt.**

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

 




