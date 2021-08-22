---
description: Die CIM BootOSFromFS-Klasse ordnet das Betriebssystem und die Dateisysteme zu, aus denen \_ das Betriebssystem geladen wird.
ms.assetid: c5697e9c-9031-4787-a03d-cf713c961cdf
ms.tgt_platform: multiple
title: CIM_BootOSFromFS-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BootOSFromFS
- CIM_BootOSFromFS.Dependent
- CIM_BootOSFromFS.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 91247872045920eacf9d00664731effe48a8ce22cf14e3e1a4086bbaf4b92c5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119284540"
---
# <a name="cim_bootosfromfs-class"></a>CIM \_ BootOSFromFS-Klasse

Die **CIM \_ BootOSFromFS-Klasse** ordnet das Betriebssystem und die Dateisysteme zu, aus denen das Betriebssystem geladen wird. Die Zuordnung ist n:n. Ein verteiltes Betriebssystem kann davon abhängen, dass mehrere Dateisysteme ordnungsgemäß und vollständig geladen werden.

> [!IMPORTANT]
> Die CIM-Klassen (Distributed Management Task Force) (DMTF) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)

 

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, UUID("{5F5B101E-DB35-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_BootOSFromFS : CIM_Dependency
{
  CIM_OperatingSystem REF Dependent;
  CIM_FileSystem      REF Antecedent;
};
```

## <a name="members"></a>Member

Die **CIM \_ BootOSFromFS-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ BootOSFromFS-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Vorläufer**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ FileSystem**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

Das Dateisystem, aus dem das Betriebssystem geladen wird.

</dd> <dt>

**Abhängigen**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ OperatingSystem**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Überschreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("Abhängig")
</dt> </dl>

Dem Betriebssystem

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **CIM \_ BootOSFromFS-Klasse** wird von der [**\_ CIM-Abhängigkeit abgeleitet.**](cim-dependency.md)

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



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_CIM-Abhängigkeit**](cim-dependency.md)
</dt> </dl>

 

