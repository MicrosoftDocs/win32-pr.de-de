---
description: Stellt eine Zuordnung zwischen einem CIM \_ -storageblock-Objekt höherer Ebene und einem CIM-storageblock-Objekt auf niedrigerer Ebene dar \_ . Beispielsweise ist ein CIM \_ protectedspaceblock-Objekt Teil eines CIM- \_ physicalblock-Objekts.
ms.assetid: 40a88927-981b-4fc4-af5f-be91d9933284
title: CIM_BasedOn-Klasse (Hyper-V-Verwaltung)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BasedOn
- CIM_BasedOn.Antecedent
- CIM_BasedOn.Dependent
- CIM_BasedOn.StartingAddress
- CIM_BasedOn.EndingAddress
- CIM_BasedOn.OrderIndex
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 47d2e44d1106eba57f4c46c0957662c348c9ca1e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862464"
---
# <a name="cim_basedon-class-hyper-v-management"></a>CIM_BasedOn-Klasse (Hyper-V-Verwaltung)

Stellt eine Zuordnung zwischen einem CIM- **\_ storageblock** -Objekt höherer Ebene und einem **CIM- \_ storageblock** -Objekt auf niedrigerer Ebene dar. Beispielsweise ist ein [**CIM \_ protectedspaceblock**](/windows/desktop/CIMWin32Prov/cim-protectedspaceextent) -Objekt Teil eines [**CIM- \_ physicalblock**](/windows/desktop/CIMWin32Prov/cim-physicalextent) -Objekts.

## <a name="syntax"></a>Syntax

``` syntax
[Association, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Core::StorageExtent"), AMENDMENT]
class CIM_BasedOn : CIM_Dependency
{
  CIM_StorageExtent REF Antecedent;
  CIM_StorageExtent REF Dependent;
  uint64                StartingAddress;
  uint64                EndingAddress;
  uint16                OrderIndex;
};
```

## <a name="members"></a>Member

Die **CIM- \_ BasedOn** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM- \_ BasedOn** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Vorgänger**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ storageblock**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger")
</dt> </dl>

Das CIM- **\_ storageblock** -Objekt auf niedrigerer Ebene.

</dd> <dt>

**Dependent**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ storageblock**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")
</dt> </dl>

Das CIM- **\_ storageblock** -Objekt der höheren Ebene.

</dd> <dt>

**"Endadresse"**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Adresse, die angibt, an welcher Stelle im Speicher auf niedrigerer Ebene das **CIM- \_ storageblock** -Objekt der höheren Ebene endet. Diese Eigenschaft ist nützlich, wenn Sie nicht zusammenhängende **CIM \_ storageblock** -Objekte einer Gruppierung auf höherer Ebene entspricht.

</dd> <dt>

**Orderindex**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein Index, der verwendet wird, um die Reihenfolge der **CIM- \_ BasedOn** -Zuordnungen in einer Auflistung anzugeben; andernfalls gibt "0" keine Reihenfolge an. **CIM \_ BasedOn** -Instanzen mit demselben abhängigen Wert sollten eindeutige Werte in der **orderindex** -Eigenschaft platzieren. Der niedrigste **orderindex** -Wert gibt den ersten Member der Auflistung an.

Ein Beispiel für die Verwendung dieser Eigenschaft ist das Definieren eines RAID-0-Stripesets von drei Datenträgern. Das resultierende RAID-Array ist ein Speicherblock, der von den Speicherblöcken abhängig ist, die die drei Datenträger beschreiben. Der **orderindex** -Wert jeder **CIM- \_ BasedOn** -Zuordnung aus den Datenträger Blöcken zum RAID-Array kann als 1, 2 und 3 angegeben werden, um die Reihenfolge anzugeben, in der die Datenträger Blöcke für den Zugriff auf die RAID-Daten verwendet werden.

</dd> <dt>

**StartingAddress**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Die Adresse, die angibt, an welcher Stelle im Speicher auf niedrigerer Ebene das **CIM- \_ storageblock** -Objekt der höheren Ebene beginnt.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM- \_ Abhängigkeit**](cim-dependency.md)
</dt> </dl>

 

