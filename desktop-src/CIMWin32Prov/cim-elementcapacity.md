---
description: Die \_ CIM-ElementCapacity-Klasse ordnet ein CIM \_ PhysicalCapacity-Objekt einem oder mehrere physischen Elementen zu. Sie ordnet den beschriebenen physischen Elementen eine Beschreibung der minimalen und maximalen Hardwareanforderungen (oder Funktionen) zu.
ms.assetid: 368c31e8-d56b-4b90-ba3f-20d9b0de8730
ms.tgt_platform: multiple
title: CIM_ElementCapacity-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementCapacity
- CIM_ElementCapacity.Capacity
- CIM_ElementCapacity.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e108fb959b95148b8eb3be2e56346e41d2b2a5ab4d5b97c81394d583b395e9ac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119924120"
---
# <a name="cim_elementcapacity-class"></a>\_CIM-ElementCapacity-Klasse

Die **\_ CIM-ElementCapacity-Klasse** ordnet ein [**CIM \_ PhysicalCapacity-Objekt**](cim-physicalcapacity.md) einem oder mehrere physischen Elementen zu. Sie ordnet den beschriebenen physischen Elementen eine Beschreibung der minimalen und maximalen Hardwareanforderungen (oder Funktionen) zu.

> [!IMPORTANT]
> Die CIM-Klassen (Distributed Management Task Force) (DMTF) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)

 

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, Association, UUID("{FAF76B6A-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_ElementCapacity
{
  CIM_PhysicalCapacity REF Capacity;
  CIM_PhysicalElement  REF Element;
};
```

## <a name="members"></a>Member

Die **\_ CIM-ElementCapacity-Klasse** verfügt über diese Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ CIM-Klasse ElementCapacity** verfügt über diese Eigenschaften.

<dl> <dt>

**Capacity**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ PhysicalCapacity**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Verweis auf die [**CIM \_ PhysicalCapacity-Klasse,**](cim-physicalcapacity.md) die die minimalen und maximalen Anforderungen sowie die Fähigkeit beschreibt, verschiedene Hardwaretypen für ein physisches Element zu unterstützen.

</dd> <dt>

**Element**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ PhysicalElement**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Verweis auf das beschriebene physische Element.

</dd> </dl>

## <a name="remarks"></a>Hinweise

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



 

