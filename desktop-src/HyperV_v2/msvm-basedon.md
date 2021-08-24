---
description: Eine Zuordnung, die beschreibt, wie Speichergefässungen aus niedrigeren Speicherebenen zusammengesetzt werden können.
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
ms.openlocfilehash: f3f8138fcc06d5e2d100f38b0333dcbfc5e76c61366da686b313a70d40ffa120
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119790250"
---
# <a name="msvm_basedon-class"></a>Msvm \_ BasedOn-Klasse

Eine Zuordnung, die beschreibt, wie Speichergefässungen aus niedrigeren Speicherebenen zusammengesetzt werden können. ProtectedSpaceExtents sind z. B. Teile von PhysicalExtents, während VolumeSets aus mindestens einem physical- oder ProtectedSpaceExtents-Objekt zusammengestellt werden. Als weiteres Beispiel kann CacheMemory unabhängig definiert und in einem PhysicalElement realisiert werden oder auf Volatile oder NonVolatileStorageExtents basieren.

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

Die **Msvm \_ BasedOn-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Msvm \_ BasedOn-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Vorläufer**
</dt> <dd> <dl> <dt>

Datentyp: **[ **CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Speicherebene auf niedrigerer Ebene. Diese Eigenschaft wird von [**CIM \_ BasedOn geerbt.**](/windows/desktop/CIMWin32Prov/cim-basedon)

</dd> <dt>

**Abhängigen**
</dt> <dd> <dl> <dt>

Datentyp: **[ **CIM \_ StorageExtent**](/windows/desktop/CIMWin32Prov/cim-storageextent)**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Speicherebene auf höherer Ebene. Diese Eigenschaft wird von [**CIM \_ BasedOn geerbt.**](/windows/desktop/CIMWin32Prov/cim-basedon)

</dd> <dt>

**EndingAddress**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Endadresse, an der im Speicher auf niedrigerer Ebene der höhere Grad endet. Diese Eigenschaft ist nützlich, wenn nicht zusammenhängende Extent einer Gruppierung auf höherer Ebene zuordnen. Diese Eigenschaft wird von [**CIM \_ BasedOn geerbt.**](/windows/desktop/CIMWin32Prov/cim-basedon)

</dd> <dt>

**OrderIndex**
</dt> <dd> <dl> <dt>

Datentyp: **uint16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Wenn es eine Reihenfolge für auf Grundlage von Zuordnungen gibt, die beschreiben, wie ein speichererhöherer Bereich auf höherer Ebene zusammengestellt wird, gibt die **OrderIndex-Eigenschaft** dies an. Wenn eine Reihenfolge vorhanden ist, sollten die Instanzen mit demselben **Abhängigen** Wert (der gleiche höhere Wertewert) eindeutige Werte in der **OrderIndex-Eigenschaft** platzieren. Der niedrigste Wert impliziert den ersten Member der Auflistung von Unterebenenwerten, und erhöhende Werte implizieren aufeinander folgende Member der Auflistung. Wenn keine geordnete Beziehung besteht, sollte der Wert 0 angegeben werden. Ein Beispiel für die Verwendung dieser Eigenschaft ist das Definieren eines RAID-0-Striped-Arrays mit drei Datenträgern. Das resultierende RAID-Array ist ein Speicherspeicher, der von den Speicherspeicherdungen abhängig ist, die jeden der drei Datenträger beschreiben. Der **OrderIndex** der einzelnen Zuordnungen aus den Datenträgerdungen zum RAID-Array kann als 1, 2 und 3 angegeben werden, um die Reihenfolge anzugeben, in der die Datenträgerspeicherungen für den Zugriff auf die RAID-Daten verwendet werden. Diese Eigenschaft wird von [**CIM \_ BasedOn geerbt.**](/windows/desktop/CIMWin32Prov/cim-basedon)

</dd> <dt>

**StartingAddress**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Startadresse, an der im Speicher auf niedrigerer Ebene der höhere Grad beginnt. Diese Eigenschaft wird von [**CIM \_ BasedOn geerbt.**](/windows/desktop/CIMWin32Prov/cim-basedon)

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | \[Windows 8 Nur Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | \[Windows Server 2012 Nur Desktop-Apps\]<br/>                                                    |
| Namespace<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

