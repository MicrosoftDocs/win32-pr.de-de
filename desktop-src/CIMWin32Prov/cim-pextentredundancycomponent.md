---
description: Die \_ CIM-Klasse PExtentRedundancyComponent stellt die physischen Erweiterungen dar, die teil einer Speicherredundanzgruppe sind.
ms.assetid: 5a4bb1e8-7b99-410a-bba5-2c63beabd00e
ms.tgt_platform: multiple
title: CIM_PExtentRedundancyComponent-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PExtentRedundancyComponent
- CIM_PExtentRedundancyComponent.PartComponent
- CIM_PExtentRedundancyComponent.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d19d1c9fa504b30f7a87dcd1402f47376a0f4613095e9f2ee25d196cd60ae581
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118678654"
---
# <a name="cim_pextentredundancycomponent-class"></a>CIM \_ PExtentRedundancyComponent-Klasse

Die **\_ CIM-Klasse PExtentRedundancyComponent** stellt die physischen Erweiterungen dar, die teil einer Speicherredundanzgruppe sind.

> [!IMPORTANT]
> Die CIM-Klassen (Distributed Management Task Force) (DMTF (Distributed Management Task Force) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)

 

Die folgende Syntax wird aus Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, UUID("{AD3C1FA2-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_PExtentRedundancyComponent : CIM_RedundancyComponent
{
  CIM_PhysicalExtent         REF PartComponent;
  CIM_StorageRedundancyGroup REF GroupComponent;
};
```

## <a name="members"></a>Member

Die **CIM \_ PExtentRedundancyComponent-Klasse** verfügt über folgende Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **\_ CIM-Klasse PExtentRedundancyComponent** verfügt über diese Eigenschaften.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ StorageRedundancyGroup**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Außerkraftsetzung**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")
</dt> </dl>

Eine [**CIM \_ StorageRedundancyGroup,**](cim-storageredundancygroup.md) die die Speicherredundanzgruppe beschreibt.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ PhysicalExtent**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Außerkraftsetzung**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

Ein [**\_ CIM PhysicalExtent,**](cim-physicalextent.md) der den physischen Umfang beschreibt, der teil der Redundanzgruppe ist.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **CIM \_ PExtentRedundancyComponent-Klasse** wird von [**CIM \_ RedundancyComponent**](cim-redundancycomponent.md)abgeleitet.

WMI implementiert diese Klasse nicht.

Diese Dokumentation wird von den CIM-Klassenbeschreibungen abgeleitet, die von dmtf veröffentlicht wurden. Möglicherweise hat Microsoft Änderungen vorgenommen, um kleinere Fehler zu korrigieren, den Dokumentationsstandards des Microsoft SDK zu entsprechen oder weitere Informationen bereitzustellen.

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

[**CIM \_ RedundancyComponent**](cim-redundancycomponent.md)
</dt> </dl>

 

