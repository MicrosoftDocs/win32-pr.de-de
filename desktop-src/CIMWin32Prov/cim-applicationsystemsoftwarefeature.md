---
description: Die CIM \_ ApplicationSystemSoftwareFeature-Klasse stellt eine Zuordnung dar, die die Softwarefeatures identifiziert, die ein bestimmtes Anwendungssystem bilden. Die Softwarefeatures können in verschiedenen Produkten enthalten sein.
ms.assetid: e40d0d64-f9f0-4c05-aef6-c759256e408b
ms.tgt_platform: multiple
title: CIM_ApplicationSystemSoftwareFeature-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ApplicationSystemSoftwareFeature
- CIM_ApplicationSystemSoftwareFeature.PartComponent
- CIM_ApplicationSystemSoftwareFeature.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: d751a4564e8ed7357abd9dae5b4773e7180c66a5d0a89781a40d672715e69b11
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119322570"
---
# <a name="cim_applicationsystemsoftwarefeature-class"></a>CIM \_ ApplicationSystemSoftwareFeature-Klasse

Die **CIM \_ ApplicationSystemSoftwareFeature-Klasse** stellt eine Zuordnung dar, die die Softwarefeatures identifiziert, die ein bestimmtes Anwendungssystem bilden. Die Softwarefeatures können in verschiedenen Produkten enthalten sein.

> [!IMPORTANT]
> Die CIM-Klassen (Distributed Management Task Force) (DMTF (Distributed Management Task Force) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)

 

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

## <a name="syntax"></a>Syntax

``` syntax
[UUID("{0E17B9EA-E3D3-11d2-8601-0000F8102E5F}"), Abstract, AMENDMENT]
class CIM_ApplicationSystemSoftwareFeature : CIM_SystemComponent
{
  CIM_SoftwareFeature   REF PartComponent;
  CIM_ApplicationSystem REF GroupComponent;
};
```

## <a name="members"></a>Member

Die **CIM \_ ApplicationSystemSoftwareFeature-Klasse** verfügt über folgende Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ ApplicationSystemSoftwareFeature-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ ApplicationSystem**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Min.**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Außerkraftsetzung**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")
</dt> </dl>

Ein [**\_ CIM-Anwendungssystem,**](cim-applicationsystem.md) das das übergeordnete System in der Zuordnung enthält.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ SoftwareFeature**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Min.**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Außerkraftsetzung**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

Ein [**CIM \_ SoftwareFeature,**](cim-softwarefeature.md) das das untergeordnete Element enthält, das eine Komponente eines Systems ist.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **CIM \_ ApplicationSystemSoftwareFeature-Klasse** wird von [**CIM \_ SystemComponent**](cim-systemcomponent.md)abgeleitet.

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



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CIM \_ SystemComponent**](cim-systemcomponent.md)
</dt> </dl>

 

