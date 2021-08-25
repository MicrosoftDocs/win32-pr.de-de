---
description: Die CIM \_ InstalledOS-Zuordnungsklasse stellt eine Verbindung zwischen dem Computersystem und dem installierten Betriebssystem dar.
ms.assetid: 6db5b5a2-91b6-4540-83b8-bb9c86c7f94e
ms.tgt_platform: multiple
title: CIM_InstalledOS-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_InstalledOS
- CIM_InstalledOS.PartComponent
- CIM_InstalledOS.GroupComponent
- CIM_InstalledOS.PrimaryOS
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a60bbd71993557eac238d6facd75d99b967b993a075cad726ccdef4625d6dce5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119923410"
---
# <a name="cim_installedos-class"></a>CIM \_ InstalledOS-Klasse

Die **CIM \_ InstalledOS-Zuordnungsklasse** stellt eine Verbindung zwischen dem Computersystem und dem installierten Betriebssystem dar. Ein Betriebssystem wird installiert, wenn es sich im Speicherspeicher eines Computersystems befindet (z. B. auf ein Laufwerk kopiert oder in den Arbeitsspeicher heruntergeladen).

> [!IMPORTANT]
> Die CIM-Klassen (Distributed Management Task Force) (DMTF) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)

 

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, UUID("{8502C575-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_InstalledOS : CIM_SystemComponent
{
  CIM_OperatingSystem REF PartComponent;
  CIM_ComputerSystem  REF GroupComponent;
  boolean                 PrimaryOS;
};
```

## <a name="members"></a>Member

Die **CIM \_ InstalledOS-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ InstalledOS-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ ComputerSystem**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Außerkraftsetzung**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Ein [**\_ CIM-ComputerSystem,**](cim-computersystem.md) das das Computersystem beschreibt.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ OperatingSystem**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Außerkraftsetzung**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**Schwach**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Ein [**\_ CIM-Betriebssystem,**](cim-operatingsystem.md) das das auf dem Computersystem installierte Betriebssystem beschreibt.

</dd> <dt>

**PrimaryOS**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|DMTF-Betriebssystem \| 001.4")
</dt> </dl>

True **gibt** an, dass das installierte Betriebssystem das Standardbetriebssystem für das Computersystem ist.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **CIM \_ InstalledOS-Klasse** wird von [**CIM \_ SystemComponent abgeleitet.**](cim-systemcomponent.md)

WMI implementiert diese Klasse nicht. Informationen zu Klassen, die **von CIM \_ InstalledOS abgeleitet wurden,** finden Sie unter [Win32-Klassen.](win32-provider.md)

Diese Dokumentation wird von den CIM-Klassenbeschreibungen abgeleitet, die von DMTF veröffentlicht wurden. Microsoft hat möglicherweise Änderungen vorgenommen, um kleinere Fehler zu beheben, die Dokumentationsstandards des Microsoft SDK zu erfüllen oder weitere Informationen zur Verfügung zu stellen.

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

 

