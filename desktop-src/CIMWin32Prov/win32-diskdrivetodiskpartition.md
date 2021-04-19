---
description: Die \_ WMI-Klasse "Win32 diskdrivedediskpartition" verknüpft ein Laufwerks und eine vorhandene Partition.
ms.assetid: 82953097-ebfb-42b8-84b4-fb4ed19f3525
ms.tgt_platform: multiple
title: Win32_DiskDriveToDiskPartition-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_DiskDriveToDiskPartition
- Win32_DiskDriveToDiskPartition.Antecedent
- Win32_DiskDriveToDiskPartition.Dependent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b2bd5472bd4ad92ddde47f7d6a492916006a80cb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343183"
---
# <a name="win32_diskdrivetodiskpartition-class"></a>Win32 \_ diskdrivedediskpartition-Klasse

Die [WMI-Klasse](/windows/desktop/WmiSdk/retrieving-a-class) " **Win32 \_ diskdrivedediskpartition** " verknüpft ein Laufwerks und eine vorhandene Partition.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4F9-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_DiskDriveToDiskPartition : CIM_MediaPresent
{
  Win32_DiskDrive     REF Antecedent;
  Win32_DiskPartition REF Dependent;
};
```

## <a name="members"></a>Member

Die **Win32 \_ diskdrivetodiskpartition** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ diskdrivedediskpartition** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Vorgänger**
</dt> <dd> <dl> <dt>

Datentyp: **Win32 \_ diskdrive**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Vorgänger"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ diskdrive")
</dt> </dl>

Verweis auf die-Instanz, die die Eigenschaften des Laufwerks darstellt, auf dem die Partition vorhanden ist.

</dd> <dt>

**Dependent**
</dt> <dd> <dl> <dt>

Datentyp: **Win32 \_ Diskpartition**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ Diskpartition")
</dt> </dl>

Verweis auf die-Instanz, die die auf dem Laufwerk befindliche Datenträger Partition darstellt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **Win32-Klasse \_ diskdrivedediskpartition** ist von [**CIM \_ mediapresent**](cim-mediapresent.md)abgeleitet.

Eine Erläuterung zur Verwendung dieser Klasse finden Sie unter [Verwenden von PowerShell zum Zuordnen von Laufwerken und Partitionen](https://blogs.technet.com/b/heyscriptingguy/archive/2012/12/17/use-powershell-to-map-disk-drives-and-partitions.aspx) und im Blog Artikel [wie kann ich logische Laufwerke und physische Datenträger korrelieren?](https://blogs.technet.com/b/heyscriptingguy/archive/2005/05/23/how-can-i-correlate-logical-drives-and-physical-disks.aspx) .

## <a name="examples"></a>Beispiele

Das PowerShell-Beispiel [Verwenden von PowerShell zum Sammeln von Datenträgern/Partitionen/](https://Gallery.TechNet.Microsoft.Com/Use-Powershell-to-Gather-b5c746d0) einstellungspunktinformationen verwendet **Win32 \_ diskdrivedediskpartition** zum Zurückgeben von Informationen zu lokalen Datenträgern/Partitionen und einfügepunkten.

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

[**CIM- \_ mediapresent**](cim-mediapresent.md)
</dt> <dt>

[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[WMI-Tasks: Datenträger und Dateisysteme](/windows/desktop/WmiSdk/wmi-tasks--disks-and-file-systems)
</dt> </dl>

 

