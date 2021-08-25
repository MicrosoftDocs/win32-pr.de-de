---
description: Die CIM \_ ActionSequence-Zuordnung definiert eine Reihe von Vorgängen, die das Softwareelement (auf das von der CIM \_ SoftwareElementActions-Zuordnung verwiesen wird) in den nächsten Zustand übergehen oder das Softwareelement aus seinem aktuellen Zustand entfernt.
ms.assetid: b539c424-bc2a-414b-b56c-72550004720f
ms.tgt_platform: multiple
title: CIM_ActionSequence-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ActionSequence
- CIM_ActionSequence.Next
- CIM_ActionSequence.Prior
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a199671dd9f88cd81be50af537e156892e8cab653c70677de27c6e5df02f1d3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119801080"
---
# <a name="cim_actionsequence-class"></a>CIM \_ ActionSequence-Klasse

Die **CIM \_ ActionSequence-Zuordnung** definiert eine Reihe von Vorgängen, die das Softwareelement (auf das von der [**CIM \_ SoftwareElementActions-Zuordnung**](cim-softwareelementactions.md) verwiesen wird) in den nächsten Zustand übergehen oder das Softwareelement aus seinem aktuellen Zustand entfernt.

Die aktionen des nächsten Zustands und deinstallationsaktionen, die einem bestimmten Softwareelement zugeordnet sind, müssen eine fortlaufende Sequenz sein. Da **CIM \_ ActionSequence** eine Zuordnung ist, bilden die Schleifen in der [**CIM \_ Action-Klasse**](cim-action.md) mit Rollen für die "vorherige" aktion und die "next"-Aktion eine Sequenz.

Die Notwendigkeit einer fortlaufenden Sequenz impliziert Folgendes:

-   Innerhalb des Satzes der nächsten Status- oder Deinstallationsaktionen gibt es nur eine Aktion, die keine Instanz der **\_ CIM-AktionSequence-Zuordnung** aufweist, die in der Rolle "Next" darauf verweist. Dies ist die erste Aktion in der Sequenz.
-   Innerhalb des Satzes der Nächsten-Zustands- oder Deinstallationsaktionen gibt es nur eine Aktion, die nicht über eine Instanz der **CIM \_ ActionSequence-Zuordnung** verfügt, auf die in der Rolle "prior" verwiesen wird. Dies ist die letzte Aktion in der Sequenz.
-   Alle anderen Aktionen innerhalb der Nächsten-Zustands- und Deinstallationsaktionen müssen an zwei Instanzen der **CIM \_ ActionSequence-Zuordnung** beteiligt sein, eine in einer "vorherigen" Rolle und eine in der Rolle "next".

> [!IMPORTANT]
> Die CIM-Klassen (Distributed Management Task Force) (DMTF (Distributed Management Task Force) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)

 

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, Association, UUID("{F127E50E-E3E0-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_ActionSequence
{
  CIM_Action REF Next;
  CIM_Action REF Prior;
};
```

## <a name="members"></a>Member

Die **CIM \_ ActionSequence-Klasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ ActionSequence-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Nächste**
</dt> <dd> <dl> <dt>

Datentyp: **\_ CIM-Aktion**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Max.**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min.**](/windows/desktop/WmiSdk/standard-qualifiers) (0)
</dt> </dl>

Verweis auf die nächste Aktion.

</dd> <dt>

**Vor**
</dt> <dd> <dl> <dt>

Datentyp: **\_ CIM-Aktion**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Max.**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min.**](/windows/desktop/WmiSdk/standard-qualifiers) (0)
</dt> </dl>

Verweis auf die vorherige Aktion.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die [**CIM \_ Action-Klassen,**](cim-action.md) die an dieser Zuordnung teilnehmen, müssen den gleichen Wert für die **Direction-Eigenschaft** aufweisen.

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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[CIM-Klassen](/windows/desktop/WmiSdk/cimclas)
</dt> </dl>

 

