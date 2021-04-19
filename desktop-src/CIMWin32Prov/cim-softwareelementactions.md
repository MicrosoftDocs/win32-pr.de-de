---
description: Die CIM- \_ softwareelementactions-Zuordnung identifiziert die Aktionen für ein Softwareelement.
ms.assetid: 2f8a584c-dff0-48f8-bc5f-2b833b5c0b18
ms.tgt_platform: multiple
title: CIM_SoftwareElementActions-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SoftwareElementActions
- CIM_SoftwareElementActions.Action
- CIM_SoftwareElementActions.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1f51cc122cdf354be9611ca1cca4ebcbe1635d14
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106338894"
---
# <a name="cim_softwareelementactions-class"></a>CIM \_ softwareelementactions-Klasse

Die **CIM- \_ softwareelementactions** -Zuordnung identifiziert die Aktionen für ein Softwareelement.

> [!IMPORTANT]
> Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).

 

Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

``` syntax
[UUID("{4B82D255-E3CD-11d2-8601-0000F8102E5F}"), Association, Aggregation, Abstract, AMENDMENT]
class CIM_SoftwareElementActions
{
  CIM_Action          REF Action;
  CIM_SoftwareElement REF Element;
};
```

## <a name="members"></a>Member

Die **CIM- \_ softwareelementactions** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM- \_ softwareelementactions** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Aktion**
</dt> <dd> <dl> <dt>

Datentyp: **CIM- \_ Aktion**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (false), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Verweis auf eine [**CIM- \_ Aktions**](cim-action.md) Instanz.

</dd> <dt>

**Element**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ Softwareelement**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Aggregat**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Verweis auf eine [**CIM- \_ Softwareelement**](cim-softwareelement.md) -Instanz.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Klasse wird von WMI nicht implementiert. Informationen zu WMI-Klassen, die von **CIM \_ Softwareelement Actions** abgeleitet sind, finden Sie unter [Win32-Klassen](win32-provider.md).

Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet. Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

