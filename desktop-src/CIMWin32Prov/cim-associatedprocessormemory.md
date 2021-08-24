---
description: Die CIM \_ AssociatedProcessorMemory-Klasse ordnet den Prozessor- und Systemspeicher oder den Cache eines Prozessors zu.
ms.assetid: a4c28a0a-e4cc-4db2-bd77-b7b5023eace6
ms.tgt_platform: multiple
title: CIM_AssociatedProcessorMemory-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AssociatedProcessorMemory
- CIM_AssociatedProcessorMemory.Antecedent
- CIM_AssociatedProcessorMemory.Dependent
- CIM_AssociatedProcessorMemory.BusSpeed
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 23b2ee879752365e3100866a4ea82a33b01a2236f4f3266539e79b3ee37b94e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119701160"
---
# <a name="cim_associatedprocessormemory-class"></a>CIM \_ AssociatedProcessorMemory-Klasse

Die **CIM \_ AssociatedProcessorMemory-Klasse** ordnet den Prozessor- und Systemspeicher oder den Cache eines Prozessors zu.

> [!IMPORTANT]
> Die CIM-Klassen (Distributed Management Task Force) (DMTF (Distributed Management Task Force) (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt derzeit nur die [CIM 2.x-Versionsschemas.](https://dmtf.org/standards/cim/schemas)

 

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

## <a name="syntax"></a>Syntax

``` syntax
[abstract, UUID("{464FFAB1-946F-11d2-AAE2-006008C78BC7}"), AMENDMENT]
class CIM_AssociatedProcessorMemory : CIM_AssociatedMemory
{
  CIM_Memory    REF Antecedent;
  CIM_Processor REF Dependent;
  uint32            BusSpeed;
};
```

## <a name="members"></a>Member

Die **CIM \_ AssociatedProcessorMemory-Klasse** verfügt über folgende Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ AssociatedProcessorMemory-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**Vorläufer**
</dt> <dd> <dl> <dt>

Datentyp: **\_ CIM-Arbeitsspeicher**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein [**\_ CIM-Arbeitsspeicher,**](cim-memory.md) der den auf einem Gerät installierten oder zugeordneten Arbeitsspeicher beschreibt.

Diese Eigenschaft wird von [**CIM \_ AssociatedMemory**](cim-associatedmemory.md)geerbt.

</dd> <dt>

**BusSpeed**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("megahertz")
</dt> </dl>

Geschwindigkeit des Bus in Megahertz (MHz) zwischen Prozessor und Arbeitsspeicher.

</dd> <dt>

**Abhängigen**
</dt> <dd> <dl> <dt>

Datentyp: **\_ CIM-Prozessor**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Überschreiben**](/windows/desktop/WmiSdk/standard-qualifiers) ("Abhängig")
</dt> </dl>

Ein [**\_ CIM-Prozessor,**](cim-processor.md) der den Prozessor beschreibt, der auf den Arbeitsspeicher zugreift oder den Cache verwendet.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **CIM \_ AssociatedProcessorMemory-Klasse** wird von [**CIM \_ AssociatedMemory**](cim-associatedmemory.md)abgeleitet.

WMI implementiert diese Klasse nicht. Weitere Informationen zu Klassen, die von **CIM \_ AssociatedProcessorMemory** abgeleitet werden, finden Sie unter [Win32-Klassen.](win32-provider.md)

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

[**CIM \_ AssociatedMemory**](cim-associatedmemory.md)
</dt> </dl>

 

