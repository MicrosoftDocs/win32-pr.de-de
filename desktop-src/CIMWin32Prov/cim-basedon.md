---
description: Die CIM BasedOn-Klasse stellt eine Zuordnung dar, die beschreibt, wie Speicher extents aus \_ Unterebenen-Extents zusammengestellt werden können.
ms.assetid: 82132012-5851-4be8-82db-edbdb50b70e5
ms.tgt_platform: multiple
title: CIM_BasedOn -Klasse (CIMWin32 WMI-Anbieter)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BasedOn
- CIM_BasedOn.Dependent
- CIM_BasedOn.Antecedent
- CIM_BasedOn.EndingAddress
- CIM_BasedOn.StartingAddress
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0a6bdd4c61628c71dbcb58b7b1d177cf7e936f802165aa9beed0aa195aeef4a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119439260"
---
# <a name="cim_basedon-class-cimwin32-wmi-providers"></a>CIM_BasedOn -Klasse (CIMWin32 WMI-Anbieter)

Die **CIM \_ BasedOn-Klasse** stellt eine Zuordnung dar, die beschreibt, wie Speicher extents aus Unterebenen-Extents zusammengestellt werden können. Physische Extents enthalten z. B. Geschützte Speicherplatz-Extents. Daher werden Volumesätze aus einem oder mehr physischen oder geschützten Speicherplatzbereich zusammengestellt. Cachespeicher kann unabhängig voneinander definiert und in einem physischen Element realisiert werden, oder er kann auf flüchtigen oder nicht flüchtigen Speichermodulen basieren.

> [!IMPORTANT]
> Die CIM-Klassen (Distributed Management Task Force) (DMTF) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)

 

Die folgende Syntax enthält vereinfachten MOF-Code und schließt alle geerbten Eigenschaften ein.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, UUID("{8502C53E-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_BasedOn : CIM_Dependency
{
  CIM_StorageExtent REF Dependent;
  CIM_StorageExtent REF Antecedent;
  uint64                EndingAddress;
  uint64                StartingAddress;
};
```

## <a name="members"></a>Member

Die **CIM \_ BasedOn-Klasse** verfügt über diese Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ BasedOn-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Vorläufer**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ StorageExtent**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

Ein [**\_ CIM-SpeicherExtent,**](cim-storageextent.md) der den Speicherausdungsspeicher auf niedrigerer Ebene beschreibt.

</dd> <dt>

**Abhängigen**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ StorageExtent**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Überschreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("Abhängig")
</dt> </dl>

Ein [**\_ CIM-SpeicherExtent,**](cim-storageextent.md) der den speichererhöheren Speicherausdungsgrad auf höherer Ebene beschreibt.

</dd> <dt>

**EndingAddress**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt das Ende des hohen Umfangs im Speicher auf niedrigerer Ebene an. Diese Eigenschaft ist nützlich, wenn nicht zusammenhängende Extent einer Gruppierung auf höherer Ebene zuordnen.

Weitere Informationen zur Verwendung von **uint64-Werten** in Skripts finden Sie unter [Skripterstellung in WMI.](/windows/desktop/WmiSdk/creating-a-wmi-script)

</dd> <dt>

**StartingAddress**
</dt> <dd> <dl> <dt>

Datentyp: **uint64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt den Anfang des hohen Umfangs im Speicher auf niedrigerer Ebene an.

Weitere Informationen zur Verwendung von **uint64-Werten** in Skripts finden Sie unter [Skripterstellung in WMI.](/windows/desktop/WmiSdk/creating-a-wmi-script)

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **CIM \_ BasedOn-Klasse** wird von der [**\_ CIM-Abhängigkeit abgeleitet.**](cim-dependency.md)

WMI implementiert diese Klasse nicht.

Diese Dokumentation wird von den CIM-Klassenbeschreibungen abgeleitet, die von DMTF veröffentlicht wurden. Microsoft hat möglicherweise Änderungen vorgenommen, um kleinere Fehler zu beheben, die Dokumentationsstandards des Microsoft SDK zu erfüllen oder weitere Informationen zur Verfügung zu stellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**\_CIM-Abhängigkeit**](cim-dependency.md)
</dt> </dl>

 

