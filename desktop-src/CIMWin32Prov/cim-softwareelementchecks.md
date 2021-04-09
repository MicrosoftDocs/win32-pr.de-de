---
description: Die CIM- \_ softwareelementchecks-Zuordnungs Klasse verknüpft ein Softwareelement mit Bedingungs-oder Standortinformationen, die für eine Funktion erforderlich sind.
ms.assetid: ff130fe9-ddb2-4e4f-86d3-53f1d8ed14aa
ms.tgt_platform: multiple
title: CIM_SoftwareElementChecks-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SoftwareElementChecks
- CIM_SoftwareElementChecks.Check
- CIM_SoftwareElementChecks.Element
- CIM_SoftwareElementChecks.Phase
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ea6fcb02794174e825994f70270745741c9b7713
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860840"
---
# <a name="cim_softwareelementchecks-class"></a>CIM \_ softwareelementchecks-Klasse

Die **CIM- \_ softwareelementchecks** -Zuordnungs Klasse verknüpft ein Softwareelement mit Bedingungs-oder Standortinformationen, die für eine Funktion erforderlich sind.

Da Software Elemente in einem Zustand, der sofort ausgeführt werden kann, nicht in einen anderen Zustand übergehen können, ist der Wert der **Phase** -Eigenschaft auf den Zustand für [**CIM- \_ Softwareelement**](cim-softwareelement.md) -Objekte im Zustand "bereit bis ausgeführt" beschränkt.

> [!IMPORTANT]
> Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).

 

Die folgende Syntax wird aus dem MOF-Code (Managed Object Format) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

``` syntax
[UUID("{24783E8A-DB31-11d2-85FC-0000F8102E5F}"), Association, Aggregation, Abstract, AMENDMENT]
class CIM_SoftwareElementChecks
{
  CIM_Check           REF Check;
  CIM_SoftwareElement REF Element;
  uint16                  Phase;
};
```

## <a name="members"></a>Member

Die **CIM- \_ softwareelementchecks** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM- \_ softwareelementchecks** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Überprüfung**
</dt> <dd> <dl> <dt>

Datentyp: **CIM- \_ Überprüfung**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (false), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Verweis auf die Überprüfung.

</dd> <dt>

**Element**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ Softwareelement**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Aggregat**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Verweis auf das-Element.

</dd> <dt>

**Phase**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt an, ob es sich bei der referenzierten Prüfung um eine Zustands Überprüfung oder eine Überprüfung des nächsten Zustands handelt.

<dt>

<span id="In-State"></span><span id="in-state"></span><span id="IN-STATE"></span>

**In-State** (0)


</dt> <dd></dd> <dt>

<span id="Next-State"></span><span id="next-state"></span><span id="NEXT-STATE"></span>

**Nächster Zustand** (1)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Diese Klasse wird von WMI nicht implementiert. Informationen zu WMI-Klassen, die von **CIM \_ Softwareelement Checks** abgeleitet sind, finden Sie unter [Win32-Klassen](win32-provider.md).

Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet. Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

