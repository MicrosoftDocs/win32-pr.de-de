---
description: Die CIM \_ associatedprocessormemory-Klasse ordnet den Prozessor-und Systemspeicher oder den Cache eines Prozessors zu.
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
ms.openlocfilehash: f35cdca92cb15e1c6fff215ff1363844e0d47012
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958483"
---
# <a name="cim_associatedprocessormemory-class"></a>CIM \_ associatedprocessormemory-Klasse

Die **CIM \_ associatedprocessormemory** -Klasse ordnet den Prozessor-und Systemspeicher oder den Cache eines Prozessors zu.

> [!IMPORTANT]
> Die Klassen der DMTF-CIM (Common Information Model) sind die übergeordneten Klassen, auf denen WMI-Klassen erstellt werden. WMI unterstützt zurzeit nur die [CIM 2. x-Versions Schemas](https://dmtf.org/standards/cim/schemas).

 

Die folgende Syntax wird durch MOF-Code (Managed Object Format) vereinfacht und schließt alle geerbten Eigenschaften ein. Eigenschaften werden in alphabetischer Reihenfolge und nicht in der MOF-Reihenfolge aufgelistet.

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

Die **CIM \_ associatedprocessormemory** -Klasse verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **CIM \_ associatedprocessormemory** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Vorgänger**
</dt> <dd> <dl> <dt>

Datentyp: **CIM- \_ Speicher**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Ein [**CIM- \_ Speicher**](cim-memory.md) , der den Arbeitsspeicher beschreibt, der auf einem Gerät installiert oder diesem zugeordnet ist.

Diese Eigenschaft wird von [**CIM \_ associatedmemory**](cim-associatedmemory.md)geerbt.

</dd> <dt>

**Busgeschwindigkeit**
</dt> <dd> <dl> <dt>

Datentyp: **UInt32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Einheiten**](/windows/desktop/WmiSdk/standard-qualifiers) ("Megahertz")
</dt> </dl>

Geschwindigkeit des Busses in Megahertz (MHz) zwischen Prozessor und Arbeitsspeicher.

</dd> <dt>

**Dependent**
</dt> <dd> <dl> <dt>

Datentyp: **CIM- \_ Prozessor**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**außer Kraft**](/windows/desktop/WmiSdk/standard-qualifiers) Setzung ("abhängig")
</dt> </dl>

Ein [**CIM- \_ Prozessor**](cim-processor.md) , der den Prozessor beschreibt, der auf den Arbeitsspeicher zugreift oder den Cache verwendet.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die **CIM \_ associatedprocessormemory** -Klasse wird von [**CIM \_ associatedmemory**](cim-associatedmemory.md)abgeleitet.

Diese Klasse wird von WMI nicht implementiert. Weitere Informationen zu Klassen, die von **CIM \_ associatedprocessormemory** abgeleitet sind, finden Sie unter [Win32-Klassen](win32-provider.md).

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

[**CIM \_ associatedmemory**](cim-associatedmemory.md)
</dt> </dl>

 

