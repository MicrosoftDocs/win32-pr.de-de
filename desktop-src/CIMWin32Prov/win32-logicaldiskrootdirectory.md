---
description: Die \_ WMI-Klasse "Win32 logicaldiskrootdirectory Association" verknüpft einen logischen Datenträger und seine Verzeichnisstruktur.
ms.assetid: 860cd28a-2a59-4ce3-be26-8fdc869c70d1
ms.tgt_platform: multiple
title: Win32_LogicalDiskRootDirectory-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_LogicalDiskRootDirectory
- Win32_LogicalDiskRootDirectory.GroupComponent
- Win32_LogicalDiskRootDirectory.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e4b015891a37c5cc92bbf102482f48306d537bb6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860628"
---
# <a name="win32_logicaldiskrootdirectory-class"></a>Win32 \_ logicaldiskrootdirectory-Klasse

Die [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) " **Win32 \_ logicaldiskrootdirectory** Association" verknüpft einen logischen Datenträger und seine Verzeichnisstruktur.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften und Methoden sind in alphabetischer Reihenfolge, nicht in der MOF-Reihenfolge.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{F25FE468-783E-11d2-90BF-0060081A46FD}"), AMENDMENT]
class Win32_LogicalDiskRootDirectory : CIM_Component
{
  Win32_LogicalDisk REF GroupComponent;
  Win32_Directory   REF PartComponent;
};
```

## <a name="members"></a>Member

Die **Win32 \_ logicaldiskrootdirectory** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ logicaldiskrootdirectory** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Datentyp: **Win32 \_ LogicalDisk**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ LogicalDisk")
</dt> </dl>

Verweis auf die-Instanz, die die Eigenschaften des logischen Datenträgers darstellt.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Datentyp: **Win32- \_ Verzeichnis**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32- \_ Verzeichnis")
</dt> </dl>

Verweis auf die-Instanz, die die Eigenschaften der Datei Verzeichnisstruktur darstellt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **Win32 \_ logicaldiskrootdirectory** -Klasse wird von der [**CIM- \_ Komponente**](cim-component.md)abgeleitet.

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

[**CIM- \_ Komponente**](cim-component.md)
</dt> <dt>

[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

