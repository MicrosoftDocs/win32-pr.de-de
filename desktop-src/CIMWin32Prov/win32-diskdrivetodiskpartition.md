---
description: Die \_ WMI-Zuordnungsklasse Win32 DiskDriveToDiskPartition verknüpft ein Laufwerk und eine vorhandene Partition.
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
ms.openlocfilehash: c92e9cc8a71516fa105e350ae8070ca417024c1802e9ea8a676d7355cb3aea7c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118675093"
---
# <a name="win32_diskdrivetodiskpartition-class"></a>Win32 \_ DiskDriveToDiskPartition-Klasse

Die [WMI-Zuordnungsklasse](/windows/desktop/WmiSdk/retrieving-a-class) **Win32 \_ DiskDriveToDiskPartition** verknüpft ein Laufwerk und eine vorhandene Partition.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

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

Die **Win32 \_ DiskDriveToDiskPartition-Klasse** verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ DiskDriveToDiskPartition-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Vorläufer**
</dt> <dd> <dl> <dt>

Datentyp: **Win32 \_ DiskDrive**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Vorgänger"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ DiskDrive")
</dt> </dl>

Verweis auf die -Instanz, die die Eigenschaften des Laufwerks darstellt, auf dem die Partition vorhanden ist.

</dd> <dt>

**Abhängigen**
</dt> <dd> <dl> <dt>

Datentyp: **Win32 \_ DiskPartition**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("WMI \| Win32 \_ DiskPartition")
</dt> </dl>

Verweis auf die Instanz, die die Datenträgerpartition darstellt, die sich auf dem Laufwerk befindet.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **Win32 \_ DiskDriveToDiskPartition-Klasse** wird von [**CIM \_ MediaPresent**](cim-mediapresent.md)abgeleitet.

Eine Erläuterung zur Verwendung dieser Klasse finden Sie in den Blogartikeln [Verwenden von PowerShell zum Zuordnen von Datenträgerlaufwerken und Partitionen](https://blogs.technet.com/b/heyscriptingguy/archive/2012/12/17/use-powershell-to-map-disk-drives-and-partitions.aspx) und Im Blog [How Can I Correlate Logical Drives and Physical Disks? (Wie kann ich logische laufwerke und physische Datenträger korrelieren?).](https://blogs.technet.com/b/heyscriptingguy/archive/2005/05/23/how-can-i-correlate-logical-drives-and-physical-disks.aspx)

## <a name="examples"></a>Beispiele

Im PowerShell-Beispiel [Use PowerShell to Gather Disk/Partition/Mount Point Information](https://Gallery.TechNet.Microsoft.Com/Use-Powershell-to-Gather-b5c746d0) wird **Win32 \_ DiskDriveToDiskPartition** verwendet, um Informationen zu lokalen Datenträgern/Partitionen und Bereitstellungspunkten zurückzugeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**CIM \_ MediaPresent**](cim-mediapresent.md)
</dt> <dt>

[Betriebssystemklassen](/previous-versions//aa392727(v=vs.85))
</dt> <dt>

[WMI-Aufgaben: Datenträger und Dateisysteme](/windows/desktop/WmiSdk/wmi-tasks--disks-and-file-systems)
</dt> </dl>

 

