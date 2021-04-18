---
description: Die CIM- \_ Aktion "aktionequenz" definiert eine Reihe von Vorgängen, die das Softwareelement (auf das durch die CIM- \_ softwareelementactions-Zuordnung verwiesen wird) in den nächsten Zustand übergehen oder das Softwareelement aus seinem aktuellen Zustand entfernt.
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
ms.openlocfilehash: 71150d1ad9785d81579d8f305fe46bc6b7e57d00
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106340118"
---
# <a name="cim_actionsequence-class"></a>CIM- \_ Aktions Sequenz Klasse

Die CIM-Aktion " **\_ aktionequenz** " definiert eine Reihe von Vorgängen, die das Softwareelement (auf das durch die [**CIM- \_ softwareelementactions**](cim-softwareelementactions.md) -Zuordnung verwiesen wird) in den nächsten Zustand übergehen oder das Softwareelement aus seinem aktuellen Zustand entfernt.

Die Aktionen des nächsten Zustands und die Deinstallations Aktionen, die einem bestimmten Softwareelement zugeordnet sind, müssen eine fortlaufende Sequenz sein. Da **CIM \_ Action Sequence** eine Zuordnung ist, bilden die Schleifen für die [**CIM- \_ Aktions**](cim-action.md) Klasse mit Rollen für die Aktion "vorheriger" und "Next" eine Sequenz.

Die Notwendigkeit einer kontinuierlichen Sequenz impliziert Folgendes:

-   Innerhalb des Satzes von Aktionen des nächsten Zustands oder der Deinstallation gibt es nur eine Aktion, die nicht über eine Instanz der CIM-Aktion " **\_ Action Sequence** " verfügt, die in der Rolle "Next" darauf verweist. Dies ist die erste Aktion in der Sequenz.
-   Innerhalb des Satzes von Aktionen des nächsten Zustands oder der Deinstallation gibt es nur eine Aktion, die nicht über eine Instanz der CIM-Aktion " **\_ Action Sequence** " verfügt, die in der Rolle "vorheriger" darauf verweist. Dies ist die letzte Aktion in der Sequenz.
-   Alle anderen Aktionen innerhalb des Satzes von Aktionen vom Typ "Nächster Zustand" und "deinstallieren" müssen an zwei Instanzen der CIM-Aktion " **\_ aktionequenz** " teilnehmen, eine in der Rolle "vorheriger" und eine in der Rolle "Next".

> [!IMPORTANT]
> Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).

 

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

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

Die **CIM- \_ Aktions Sequenz** Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM- \_ Aktions Sequenz** Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Nächste**
</dt> <dd> <dl> <dt>

Datentyp: **CIM- \_ Aktion**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)
</dt> </dl>

Verweis auf die nächste Aktion.

</dd> <dt>

**Vor**
</dt> <dd> <dl> <dt>

Datentyp: **CIM- \_ Aktion**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)
</dt> </dl>

Verweis auf die vorherige Aktion.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die [**CIM- \_ Aktions**](cim-action.md) Klassen, die an dieser Zuordnung beteiligt sind, müssen über denselben Wert für die **Direction** -Eigenschaft verfügen.

Diese Klasse wird von WMI nicht implementiert.

Diese Dokumentation wird von den von der DMTF veröffentlichten CIM-Klassen Beschreibungen abgeleitet. Microsoft hat möglicherweise Änderungen an den korrekten geringfügigen Fehlern vorgenommen, den Microsoft SDK-Dokumentations Standards entsprechen oder weitere Informationen bereitstellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Root \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[CIM-Klassen](/windows/desktop/WmiSdk/cimclas)
</dt> </dl>

 

