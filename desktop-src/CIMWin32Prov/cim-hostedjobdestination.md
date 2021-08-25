---
description: Die CIM \_ HostedJobDestination-Klasse stellt eine Zuordnung zwischen einem Auftragsziel und dem System dar, auf dem es sich befindet. Ein System kann viele Auftragswarteschlangen hosten. Auftragsziele werden auf das Hostingsystem zurückgeleitet.
ms.assetid: 5d853826-1f27-417b-a053-5e0ee9816376
ms.tgt_platform: multiple
title: CIM_HostedJobDestination-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HostedJobDestination
- CIM_HostedJobDestination.Dependent
- CIM_HostedJobDestination.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 072e911471fe6220a7135f45787f5ea8bf9c79279212ed6215a971ff8c1d95cd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119923530"
---
# <a name="cim_hostedjobdestination-class"></a>CIM \_ HostedJobDestination-Klasse

Die **CIM \_ HostedJobDestination-Klasse** stellt eine Zuordnung zwischen einem Auftragsziel und dem System dar, auf dem es sich befindet. Ein System kann viele Auftragswarteschlangen hosten. Auftragsziele werden auf das Hostingsystem zurückgeleitet.

> [!IMPORTANT]
> Die CIM-Klassen (Distributed Management Task Force) (DMTF (Distributed Management Task Force) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)

 

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, UUID("{7880DD16-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_HostedJobDestination : CIM_Dependency
{
  CIM_JobDestination REF Dependent;
  CIM_System         REF Antecedent;
};
```

## <a name="members"></a>Member

Die **CIM \_ HostedJobDestination-Klasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ HostedJobDestination-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Vorläufer**
</dt> <dd> <dl> <dt>

Datentyp: **\_ CIM-System**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Max.**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min.**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Außerkraftsetzung**](/windows/desktop/WmiSdk/standard-qualifiers) ("Vorgänger")
</dt> </dl>

Ein [**\_ CIM-System,**](cim-system.md) das das Hostsystem beschreibt.

</dd> <dt>

**Abhängigen**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ JobDestination**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Überschreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("abhängig"), [**Schwach**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Eine [**\_ CIM-JobDestination,**](cim-jobdestination.md) die das auf dem System gehostete Auftragsziel beschreibt.

</dd> </dl>

## <a name="remarks"></a>Hinweise

**CIM \_ HostedJobDestination** wird von [**\_ CIM-Abhängigkeit**](cim-dependency.md)abgeleitet.

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

[**\_CIM-Abhängigkeit**](cim-dependency.md)
</dt> </dl>

 

