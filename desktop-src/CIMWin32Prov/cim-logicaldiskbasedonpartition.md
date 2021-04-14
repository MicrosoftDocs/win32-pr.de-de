---
description: Die CIM \_ LogicalDiskBasedOnPartition-Klasse ordnet der Festplatten Partition, auf der Sie sich befindet, einen logischen Datenträger zu.
ms.assetid: 264b62ed-2af2-42dc-9cd2-41b26cc85ca4
ms.tgt_platform: multiple
title: CIM_LogicalDiskBasedOnPartition-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDiskBasedOnPartition
- CIM_LogicalDiskBasedOnPartition.EndingAddress
- CIM_LogicalDiskBasedOnPartition.StartingAddress
- CIM_LogicalDiskBasedOnPartition.Dependent
- CIM_LogicalDiskBasedOnPartition.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 67aac7ae8d295bd6d98e06e0ebb8135d3330f52f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523136"
---
# <a name="cim_logicaldiskbasedonpartition-class"></a>CIM \_ LogicalDiskBasedOnPartition-Klasse

Die **CIM \_ LogicalDiskBasedOnPartition** -Klasse ordnet der Festplatten Partition, auf der Sie sich befindet, einen logischen Datenträger zu.

Beispielsweise kann sich das Laufwerk C eines Computers auf einer Partition auf einem lokalen physischen Medium befinden. Dies stellt fest, dass ein logischer Datenträger nicht mehr als eine Partition umfassen kann. Wenn ein logischer Datenträger mehr als eine Partition umfassen kann, basiert der logische Datenträger jedoch auf der RAID-Konfiguration (z. b. auf einem Spiegel oder einem Stripeset). In diesem Fall basiert der logische Datenträger auf dem Speicher Volume. Um zu verhindern, dass die **CIM \_ LogicalDiskBasedOnPartition** ordnungsgemäß verwendet wird, wurde der **Max (1)** -Qualifizierer auf den **Vorgänger** Verweis auf die Datenträger Partition festgestellt.

> [!IMPORTANT]
> Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).

 

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, UUID("{8502C53F-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_LogicalDiskBasedOnPartition : CIM_BasedOn
{
  uint64                EndingAddress;
  uint64                StartingAddress;
  CIM_LogicalDisk   REF Dependent;
  CIM_DiskPartition REF Antecedent;
};
```

## <a name="members"></a>Member

Die **CIM \_ LogicalDiskBasedOnPartition** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ LogicalDiskBasedOnPartition** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Vorgänger**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ Diskpartition**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("Vorgänger"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Eine [**CIM \_ Diskpartition**](cim-diskpartition.md) , die die Datenträger Partition beschreibt.

</dd> <dt>

**Dependent**
</dt> <dd> <dl> <dt>

Datentyp: **CIM \_ LogicalDisk**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")
</dt> </dl>

Ein [**CIM \_ LogicalDisk**](cim-logicaldisk.md) , der den logischen Datenträger beschreibt, der auf der Partition erstellt wird.

</dd> <dt>

**"Endadresse"**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt das Ende des hohen Wertebereichs in niedrigerer Speicher Ebene an. Diese Eigenschaft ist nützlich, wenn Sie nicht zusammenhängende Blöcke einer Gruppierung auf höherer Ebene zuordnen.

Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

Diese Eigenschaft wird von [**CIM- \_ BasedOn**](cim-basedon.md)geerbt.

</dd> <dt>

**StartingAddress**
</dt> <dd> <dl> <dt>

Datentyp: **UInt64**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Gibt den Anfang des hohen Bereichs in einem Speicher auf niedrigerer Ebene an.

Weitere Informationen zur Verwendung von **UInt64** -Werten in Skripts finden Sie unter [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).

Diese Eigenschaft wird von [**CIM- \_ BasedOn**](cim-basedon.md)geerbt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **CIM \_ LogicalDiskBasedOnPartition** -Klasse wird von [**CIM \_ BasedOn**](cim-basedon.md)abgeleitet.

Diese Klasse wird von WMI nicht implementiert. Informationen zu Klassen, die von **CIM \_ LogicalDiskBasedOnPartition** abgeleitet sind, finden Sie unter [Win32-Klassen](win32-provider.md).

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

[**CIM- \_ BasedOn**](cim-basedon.md)
</dt> </dl>

 

