---
description: Eine Zuordnung, die beschreibt, wie Speicherblöcke aus Blöcken auf niedrigerer Ebene zusammengestellt werden können.
ms.assetid: 8be9bb2c-ef46-454b-bfc3-0398c64d17b7
title: Msvm_BasedOn-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_BasedOn
- Msvm_BasedOn.Antecedent
- Msvm_BasedOn.Dependent
- Msvm_BasedOn.StartingAddress
- Msvm_BasedOn.EndingAddress
- Msvm_BasedOn.OrderIndex
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8262ae5e510574bf02630410b584d9df10d64ecf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362660"
---
# <a name="msvm_basedon-class"></a>MSVM- \_ BasedOn-Klasse

Eine Zuordnung, die beschreibt, wie Speicherblöcke aus Blöcken auf niedrigerer Ebene zusammengestellt werden können. Protectedspaceextents sind z. b. Teile von physicalextents, während Volumesets von einem oder mehreren physischen oder protectedspaceextents zusammengestellt werden. Ein weiteres Beispiel ist, dass CacheMemory unabhängig voneinander definiert und in einem PhysicalElement realisiert werden kann oder auf flüchtigen oder nicht volatilestorageextents basieren kann.

Die folgende Syntax wird Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften.

## <a name="syntax"></a>Syntax

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_BasedOn : CIM_BasedOn
{
  CIM_StorageExtent REF Antecedent;
  CIM_StorageExtent REF Dependent;
  uint64                StartingAddress;
  uint64                EndingAddress;
  uint16                OrderIndex;
};
```

## <a name="members"></a>Member

Die **MSVM- \_ BasedOn** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **MSVM- \_ BasedOn** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Vorgänger**
</dt> <dd> <dl> <dt>

Datentyp: **[ **CIM \_ storageblock**](/windows/desktop/CIMWin32Prov/cim-storageextent)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Speicherblock auf niedrigerer Ebene. Diese Eigenschaft wird von [**CIM- \_ BasedOn**](/windows/desktop/CIMWin32Prov/cim-basedon)geerbt.

</dd> <dt>

**Dependent**
</dt> <dd> <dl> <dt>

Datentyp: **[ **CIM \_ storageblock**](/windows/desktop/CIMWin32Prov/cim-storageextent)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Der Speicherblock auf höherer Ebene. Diese Eigenschaft wird von [**CIM- \_ BasedOn**](/windows/desktop/CIMWin32Prov/cim-basedon)geerbt.

</dd> <dt>

**"Endadresse"**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Endadresse, an der sich im Speicher auf niedrigerer Ebene der Umfang der höheren Ebene endet. Diese Eigenschaft ist nützlich, wenn Sie nicht zusammenhängende Blöcke zu einer Gruppierung auf höherer Ebene zuordnen. Diese Eigenschaft wird von [**CIM- \_ BasedOn**](/windows/desktop/CIMWin32Prov/cim-basedon)geerbt.

</dd> <dt>

**Orderindex**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Wenn auf Grundlage von Zuordnungen, die beschreiben, wie ein Speicherblock auf höherer Ebene assembliert wird, eine Bestellung vorhanden ist, gibt die **orderindex** -Eigenschaft dies an. Wenn eine Bestellung vorhanden ist, sollten die Instanzen mit demselben **abhängigen** Wert (dem gleichen höheren Ebenen-Block) eindeutige Werte in der **orderindex** -Eigenschaft platzieren. Der niedrigste Wert impliziert das erste Element der Auflistung von Blöcken auf niedrigerer Ebene, und das Erhöhen der Werte impliziert aufeinander folgende Member der Auflistung. Wenn keine geordnete Beziehung vorhanden ist, sollte der Wert 0 (null) angegeben werden. Ein Beispiel für die Verwendung dieser Eigenschaft ist das Definieren eines RAID-0-Stripesets mit drei Datenträgern. Das resultierende RAID-Array ist ein Speicherblock, der von den Speicherblöcken abhängig ist, die die drei Datenträger beschreiben. Der **orderindex** -Wert jeder Zuordnung von der Datenträger Erweiterung zum RAID-Array kann als 1, 2 und 3 angegeben werden, um die Reihenfolge anzugeben, in der die Datenträger Blöcke für den Zugriff auf die RAID-Daten verwendet werden. Diese Eigenschaft wird von [**CIM- \_ BasedOn**](/windows/desktop/CIMWin32Prov/cim-basedon)geerbt.

</dd> <dt>

**StartingAddress**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Startadresse, an der im Speicher auf niedrigerer Ebene der höhere Ebenen-Block beginnt. Diese Eigenschaft wird von [**CIM- \_ BasedOn**](/windows/desktop/CIMWin32Prov/cim-basedon)geerbt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 8 \[ -Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2012 \[ -Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

