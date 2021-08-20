---
description: Die \_ CIM SoftwareElementActions-Zuordnung identifiziert die Aktionen für ein Softwareelement.
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
ms.openlocfilehash: f3ee22c018c1bcc3a3850ac2b9c4c3bcba32780ea66927245fcf0b02eae74232
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118421291"
---
# <a name="cim_softwareelementactions-class"></a>CIM \_ SoftwareElementActions-Klasse

Die **CIM \_ SoftwareElementActions-Zuordnung** identifiziert die Aktionen für ein Softwareelement.

> [!IMPORTANT]
> Die CIM-Klassen (Distributed Management Task Force) (DMTF (Distributed Management Task Force) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)

 

Die folgende Syntax wird aus Managed Object Format (MOF)-Code vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

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

Die **CIM \_ SoftwareElementActions-Klasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ SoftwareElementActions-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Aktion**
</dt> <dd> <dl> <dt>

Datentyp: **\_ CIM-Aktion**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (FALSE), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Verweis auf eine [**CIM \_ Action-Instanz.**](cim-action.md)

</dd> <dt>

**Element**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ SoftwareElement**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Min.**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max.**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Aggregieren**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Verweis auf eine [**CIM \_ SoftwareElement-Instanz.**](cim-softwareelement.md)

</dd> </dl>

## <a name="remarks"></a>Hinweise

WMI implementiert diese Klasse nicht. Informationen zu WMI-Klassen, die von **CIM \_ SoftwareElementActions** abgeleitet werden, finden Sie unter [Win32-Klassen.](win32-provider.md)

Diese Dokumentation wird von den CIM-Klassenbeschreibungen abgeleitet, die von dmtf veröffentlicht wurden. Möglicherweise hat Microsoft Änderungen vorgenommen, um kleinere Fehler zu korrigieren, den Dokumentationsstandards des Microsoft SDK zu entsprechen oder weitere Informationen bereitzustellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

